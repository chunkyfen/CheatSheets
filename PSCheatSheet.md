# **1. Installation des rôles AD DS, DNS, DHCP**

## ✅ Installer Active Directory Domain Services (ADDS)
```powershell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

### ✅ Promouvoir le serveur en contrôleur de domaine (nouvelle forêt)
```powershell
Install-ADDSForest -DomainName "mondomaine.local" -DomainNetbiosName "MONDOMAINE" -InstallDNS
```

### ✅ Ajouter un contrôleur de domaine à un domaine existant
```powershell
Install-ADDSDomainController -DomainName "mondomaine.local" -InstallDNS
```

---

## ✅ Installer DNS
*(Déjà installé si tu fais Install-ADDSForest avec -InstallDNS)*

```powershell
Install-WindowsFeature DNS -IncludeManagementTools
```

---

## ✅ Installer DHCP
```powershell
Install-WindowsFeature DHCP -IncludeManagementTools
```

### Autoriser DHCP dans AD
```powershell
Add-DhcpServerInDC -DnsName "SRV-DC01.mondomaine.local" -IPAddress 10.10.10.10
```

### Créer une plage DHCP
```powershell
Add-DhcpServerv4Scope -Name "LAN" -StartRange 10.10.10.100 -EndRange 10.10.10.200 -SubnetMask 255.255.255.0
```

### Ajouter une passerelle
```powershell
Set-DhcpServerv4OptionValue -Router 10.10.10.1
```

---

# 🧩 **2. Gestion Active Directory : OU, sous-OU, groupes, utilisateurs**

## ✅ Créer une OU
```powershell
New-ADOrganizationalUnit -Name "Utilisateurs" -Path "DC=mondomaine,DC=local"
```

## ✅ Créer une sous-OU
```powershell
New-ADOrganizationalUnit -Name "TI" -Path "OU=Utilisateurs,DC=mondomaine,DC=local"
```

---

## ✅ Créer un groupe
```powershell
New-ADGroup -Name "Groupe-TI" -GroupScope Global -GroupCategory Security -Path "OU=TI,OU=Utilisateurs,DC=mondomaine,DC=local"
```

---

## ✅ Créer un utilisateur
```powershell
New-ADUser -Name "Jean Tremblay" `
    -GivenName "Jean" `
    -Surname "Tremblay" `
    -SamAccountName "jtremblay" `
    -UserPrincipalName "jtremblay@mondomaine.local" `
    -AccountPassword (Read-Host -AsSecureString "Mot de passe") `
    -Enabled $true `
    -Path "OU=TI,OU=Utilisateurs,DC=mondomaine,DC=local"
```

---

## ✅ Ajouter un utilisateur à un groupe
```powershell
Add-ADGroupMember -Identity "Groupe-TI" -Members "jtremblay"
```

---

# 🛰️ **3. Gestion AD à distance (RSAT) sur un poste client Windows 10/11/2025**

## ✅ Installer les outils RSAT (dont AD Management)
```powershell
Get-WindowsCapability -Name RSAT* -Online | Add-WindowsCapability -Online
```

### Installer uniquement ADDS Tools
```powershell
Add-WindowsCapability -Online -Name Rsat.ActiveDirectory.DS-LDS.Tools~~~~0.0.1.0
```

---

# 🔧 **4. Commandes utiles pour administrer AD**

## ✅ Lister les OU
```powershell
Get-ADOrganizationalUnit -Filter *
```

## ✅ Lister les utilisateurs
```powershell
Get-ADUser -Filter * -SearchBase "OU=Utilisateurs,DC=mondomaine,DC=local"
```

## ✅ Réinitialiser un mot de passe
```powershell
Set-ADAccountPassword -Identity "jtremblay" -Reset -NewPassword (Read-Host -AsSecureString)
```

## ✅ Déverrouiller un compte
```powershell
Unlock-ADAccount -Identity "jtremblay"
```

## ✅ Désactiver un compte
```powershell
Disable-ADAccount -Identity "jtremblay"
```

## ✅ Activer un compte
```powershell
Enable-ADAccount -Identity "jtremblay"
```

---

# 🌐 **5. Commandes DNS utiles**

## ✅ Ajouter un enregistrement A
```powershell
Add-DnsServerResourceRecordA -Name "serveurweb" -ZoneName "mondomaine.local" -IPv4Address 10.10.10.50
```

## ✅ Ajouter un enregistrement PTR
```powershell
Add-DnsServerResourceRecordPtr -Name "50" -ZoneName "10.10.10.in-addr.arpa" -PtrDomainName "serveurweb.mondomaine.local"
```

---

# 📡 **6. Commandes DHCP utiles**

## ✅ Voir les baux DHCP
```powershell
Get-DhcpServerv4Lease
```

## ✅ Ajouter un DNS dans DHCP
```powershell
Set-DhcpServerv4OptionValue -DnsServer 10.10.10.10
```

---

# 🛠️ **7. Commandes serveur générales**

## ✅ Renommer le serveur
```powershell
Rename-Computer -NewName "SRV-DC01" -Restart
```

## ✅ Joindre un domaine
```powershell
Add-Computer -DomainName "mondomaine.local" -Credential (Get-Credential) -Restart
```

---

# **8. Commandes avancées**

## ✅ Créer un utilisateur en masse depuis un CSV
```powershell
Import-Csv .\users.csv | ForEach-Object {
    New-ADUser -Name $_.Name `
        -SamAccountName $_.Sam `
        -UserPrincipalName "$($_.Sam)@mondomaine.local" `
        -GivenName $_.Given `
        -Surname $_.Surname `
        -AccountPassword (ConvertTo-SecureString $_.Password -AsPlainText -Force) `
        -Enabled $true `
        -Path $_.OU
}
```

## ✅ Vérifier la réplication AD
```powershell
Get-ADReplicationPartnerMetadata -Target "SRV-DC01"
```

## ✅ Forcer la réplication
```powershell
Sync-ADObject -Object "CN=jtremblay,OU=TI,OU=Utilisateurs,DC=mondomaine,DC=local" -Source "SRV-DC01" -Destination "SRV-DC02"
