## 1. Cloud computing – concepts de base

### 1.1 Définition

- **Cloud computing :**  
  Modèle permettant un accès réseau omniprésent, pratique et à la demande à un ensemble partagé de ressources informatiques configurables (réseaux, serveurs, stockage, applications, services) pouvant être rapidement provisionnées et libérées, avec un minimum d’efforts de gestion.

### 1.2 5 caractéristiques essentielles

- **Libre-service à la demande :**  
  L’utilisateur provisionne des ressources automatiquement sans contact humain avec le fournisseur.
- **Accès réseau large bande :**  
  Accès via le réseau avec des mécanismes standard (HTTP, etc.).
- **Mutualisation des ressources :**  
  Les ressources sont partagées entre plusieurs clients (multi-tenant).
- **Élasticité rapide :**  
  Ressources extensibles et réductibles rapidement selon la demande.
- **Service mesuré :**  
  Utilisation surveillée, contrôlée, facturée de manière transparente (pay-as-you-go).

### 1.3 Avantages du cloud

#### Avantages économiques

- Réduction du **CAPEX** (pas d’investissement lourd initial).
- Passage au modèle **OPEX** (paiement à l’usage).
- Élimination des coûts de **maintenance matérielle**.
- **Optimisation** de l’utilisation des ressources (right-sizing).

#### Avantages techniques

- **Évolutivité** quasi instantanée.
- **Haute disponibilité** et redondance intégrée.
- **Accès mondial** aux ressources.
- **Mises à jour automatiques** des plateformes/services.
- **Récupération après sinistre** simplifiée.

#### Avantages organisationnels

- Déploiement **rapide** de nouvelles applications.
- Concentration sur le **cœur de métier**, pas sur l’infrastructure.
- **Flexibilité** et **agilité** accrues.
- Accès simplifié aux **technologies de pointe**.

---

## 2. Modèles de service cloud (IaaS, PaaS, SaaS)

### 2.1 IaaS – Infrastructure as a Service

- **Définition :**  
  Le fournisseur fournit l’infrastructure (serveurs, stockage, réseau). Le client gère OS, applications, données.

- **Caractéristiques :**
  - Contrôle total des **VMs**.
  - Gestion des **systèmes d’exploitation** par le client.
  - Installation/configuration des **applications** par le client.
  - Responsabilité de la **sécurité OS et applications** côté client.

- **Exemples Azure :**
  - Azure Virtual Machines  
  - Azure Virtual Network  
  - Azure Storage  
  - Azure Load Balancer  

- **Cas d’usage typiques :**
  - Migration **lift-and-shift** d’applications existantes.
  - Environnements de **dev/test**.
  - Hébergement de **sites web**.
  - **Calcul haute performance**.

- **Responsabilités :**
  - **Client :** Applications, données, runtime, middleware, OS.
  - **Fournisseur :** Virtualisation, serveurs, stockage, réseau.

### 2.2 PaaS – Platform as a Service

- **Définition :**  
  Le fournisseur gère l’infrastructure + plateforme (OS, runtime, middleware). Le client gère applications + données.

- **Caractéristiques :**
  - Pas de gestion de **serveurs ni OS**.
  - **Outils de développement** intégrés.
  - **Mise à l’échelle automatique**.
  - Services **managés**.

- **Exemples Azure :**
  - Azure App Service (web)  
  - Azure SQL Database  
  - Azure Functions (serverless)  
  - Azure Container Instances  

- **Cas d’usage typiques :**
  - Apps web modernes.
  - APIs / microservices.
  - Backends mobiles.
  - Solutions **serverless**.

- **Responsabilités :**
  - **Client :** Applications, données.
  - **Fournisseur :** Runtime, middleware, OS, virtualisation, serveurs, stockage, réseau.

### 2.3 SaaS – Software as a Service

- **Définition :**  
  Le fournisseur gère tout (infra + plateforme + appli). Le client **utilise l’appli** (web/API).

- **Caractéristiques :**
  - Application **prête à l’emploi**.
  - Accès via **navigateur web**.
  - **Mises à jour automatiques**.
  - Configuration minimale.

- **Exemples Microsoft :**
  - Microsoft 365 (Office, Teams, SharePoint)
  - Dynamics 365
  - Azure DevOps Services
  - Power BI

- **Cas d’usage typiques :**
  - Suite bureautique.
  - CRM.
  - Messagerie électronique.
  - Collaboration d’équipe.

- **Responsabilités :**
  - **Client :** Données utilisateur, configuration applicative.
  - **Fournisseur :** Application complète, données, runtime, middleware, OS, virtualisation, serveurs, stockage, réseau.

### 2.4 Comparaison IaaS / PaaS / SaaS

| Critère                | IaaS       | PaaS       | SaaS       |
|------------------------|-----------|-----------|-----------|
| Contrôle               | Maximum   | Moyen     | Minimum   |
| Flexibilité            | Élevée    | Moyenne   | Faible    |
| Complexité de gestion  | Élevée    | Moyenne   | Faible    |
| Temps de déploiement   | Long      | Moyen     | Immédiat  |
| Expertise requise      | Élevée    | Moyenne   | Faible    |
| Coût initial           | Variable  | Moyen     | Faible    |

---

## 3. Microsoft Azure – concepts et services clés

### 3.1 Vue d’ensemble

- **Microsoft Azure :** plateforme cloud de Microsoft avec + de 200 services.
- **Régions :** > 60 régions. Au Canada :
  - Canada Central (Toronto)
  - Canada East (Québec)
- **Principe des régions :**
  - Chaque région = ≥ 1 datacenter.
  - Régions souvent organisées en **paires** pour réplication et DR.

### 3.2 Services essentiels pour Windows Server

#### 3.2.1 Azure Virtual Machines

- Service IaaS pour créer des VMs Windows ou Linux.
- **Caractéristiques :**
  - Choix de **taille** (CPU, RAM, stockage).
  - Images Windows Server 2016/2019/2022/2025.
  - **Disques managés** avec réplication.
  - **Snapshots** et **sauvegardes** intégrés.
- **Séries de VM populaires :**
  - Série B : Économique, charges variables (burstable).
  - Série D : Usage général, équilibré.
  - Série E : Optimisé mémoire (bases de données).
  - Série F : Optimisé calcul.

#### 3.2.2 Azure Virtual Network (VNet)

- Réseau virtuel privé isolé dans Azure.

- **Composants :**
  - Sous-réseaux (subnets).
  - NSG (Network Security Groups).
  - Passerelles VPN.
  - VNet Peering (appairage de réseaux).

#### 3.2.3 Azure Active Directory (Entra ID)

- Service d’**identité** et d’**accès** cloud.

- **Fonctionnalités :**
  - Gestion des identités cloud.
  - **SSO** (Single Sign-On).
  - **MFA** (authentification multifacteur).
  - Accès conditionnel.
  - Synchronisation avec AD on-premise.

#### 3.2.4 Azure Storage

- Stockage cloud hautement disponible, sécurisé.

- **Types :**
  - **Blob Storage :** objets (fichiers, images, vidéos).
  - **File Storage :** partages de fichiers SMB.
  - **Queue Storage :** files de messages.
  - **Table Storage :** NoSQL clé/valeur.

#### 3.2.5 Azure Backup & Site Recovery

- **Azure Backup :**
  - Sauvegarde de VMs Azure.
  - Sauvegarde de serveurs on-premise.
  - Rétention long terme.
  - Restauration granulaire.
- **Azure Site Recovery :**
  - Réplication de VMs.
  - Basculement automatisé.
  - Plans de récupération.
  - Tests de DR sans impact.

### 3.3 Services de gestion Azure

- **Azure Portal :** interface web graphique.
- **Azure PowerShell :** modules PowerShell Az pour automatiser Azure.
- **Azure CLI :** interface CLI multiplateforme.
- **Azure Cloud Shell :** shell intégré dans le portail (PowerShell + Bash).
- **Azure Resource Manager (ARM) :** couche de gestion/unification d’API.

### 3.4 Modèle de tarification Azure

- **Facteurs de coût :**
  - Taille et type de ressource.
  - Région de déploiement.
  - Utilisation réseau (bande passante).
  - Licences (Windows, SQL, etc.).
  - Services managés additionnels.

- **Options de réduction :**
  - **Instances réservées (RI) :** jusqu’à ~72 % de réduction (engagement 1–3 ans).
  - **Azure Hybrid Benefit :** réutilisation de licences Windows Server existantes.
  - **Arrêt automatique** pour environnements de dev/test.
  - **Dimensionnement approprié** (right-sizing) des VMs.

---

## 4. Hybridation on-premise / cloud

### 4.1 Concept d’infrastructure hybride

- Combinaison de ressources **on-premise** (sur site) et **cloud**.
- Environnement unifié, scénarios progressifs de migration.

#### Avantages

- Migration **progressive** vers le cloud.
- Respect des contraintes **réglementaires**.
- Optimisation des coûts.
- Flexibilité de déploiement.
- Continuité avec l’infrastructure existante.

#### Scénarios hybrides typiques

1. **Extension de datacenter :** débordement vers le cloud lors de pics.
2. **Site de secours / DR :** datacenter secondaire dans Azure.
3. **Dev/Test dans le cloud, prod on-premise.**
4. **Applications distribuées :** front-end cloud, back-end on-premise.

### 4.2 Technologies Microsoft d’hybridation

#### 4.2.1 Azure AD Connect

- Synchronisation AD on-premise ↔ Azure AD.

- **Fonctionnalités :**
  - Synchronisation des **utilisateurs**.
  - Synchronisation des **groupes**.
  - Synchronisation des **mots de passe** (Password Hash Sync).
  - **Pass-Through Authentication** (PTA).
  - Fédération avec **AD FS**.

- **Flux :** AD on-premise + Azure AD Connect → Azure AD → M365, SaaS, ressources Azure.

#### 4.2.2 Azure Arc

- Extension d’Azure sur serveurs on-premise et multi-cloud.

- **Capacités :**
  - Gestion centralisée de serveurs Windows/Linux.
  - Application de **politiques Azure**.
  - Monitoring unifié.
  - Gestion des mises à jour.
  - Intégration avec Defender for Cloud (sécurité).

#### 4.2.3 VPN Site-to-Site

- Tunnel sécurisé entre réseau on-premise et VNet Azure.

- **Composants :**
  - Passerelle VPN Azure.
  - Appareil VPN local (routeur/firewall).
  - Tunnel chiffré **IPsec/IKE**.

#### 4.2.4 Azure ExpressRoute

- Connexion privée dédiée (pas d’Internet public).

- **Avantages vs VPN :**
  - Bande passante élevée (50 Mbps → 100 Gbps).
  - Latence plus faible/stable.
  - Connexion privée.
  - SLA de disponibilité élevé.

### 4.3 Stratégies de migration – les 6 R

1. **Rehost (Lift & Shift)**
   - Migration directe sans modification.
   - Rapide.
   - Bénéfices cloud limités.

2. **Replatform (Lift, Tinker & Shift)**
   - Petites optimisations.
   - Utilisation de services managés.
   - Bon compromis rapidité/optimisation.

3. **Repurchase (Drop & Shop)**
   - Remplacement par SaaS.
   - Ex : Exchange on-prem → Microsoft 365.

4. **Refactor / Re-architect**
   - Réécriture cloud-native.
   - Maximise les avantages du cloud.
   - Très coûteux en temps/effort.

5. **Retire**
   - Décommissionnement d’apps obsolètes.
   - Réduction des coûts, simplification.

6. **Retain**
   - Garder on-premise (temporaire ou permanent).
   - Pour raisons réglementaires/techniques.
   - Migration envisagée plus tard.

### 4.4 Phases typiques d’un projet de migration

1. **Phase 1 – Évaluation :**
   - Inventaire (apps, serveurs).
   - Analyse de dépendances.
   - Évaluation compatibilité avec Azure.
   - Estimation des coûts.

2. **Phase 2 – Planification :**
   - Choix de la (ou des) stratégie(s) 6 R.
   - Conception de l’architecture cible.
   - Plan de migration par vagues.
   - Gestion des risques.

3. **Phase 3 – Migration pilote :**
   - Migration d’un environnement test.
   - Validation des processus.
   - Formation des équipes.
   - Ajustements.

4. **Phase 4 – Migration production :**
   - Migration par vagues.
   - Tests de validation.
   - Bascule des utilisateurs.
   - Monitoring renforcé.

5. **Phase 5 – Optimisation :**
   - Ajustement de la taille des VMs.
   - Mise en place de l’auto-scaling.
   - Optimisation de coûts.
   - Amélioration continue.

---

## 5. Infrastructure as Code (IaC) & ARM Templates

### 5.1 Concept d’Infrastructure as Code

- **IaC :** gestion/provisionnement d’infrastructure via **code** (fichiers texte) plutôt que configs manuelles GUI.

- **Principes :**
  - Défini dans des fichiers texte.
  - Versionnable (Git).
  - Reproductible et cohérent.
  - Automatisable et testable.

- **Avantages :**
  1. Répétabilité.
  2. Rapidité (minutes vs heures).
  3. Documentation implicite (le code décrit l’infra).
  4. Historique des changements (versionnement).
  5. Collaboration (code review).
  6. Réduction des erreurs humaines.

### 5.2 Azure Resource Manager (ARM) Templates

- **Format :** fichiers **JSON** décrivant les ressources et leur configuration.

- **Structure générale :**
  ```json
  {
    "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": { },
    "variables": { },
    "resources": [ ],
    "outputs": { }
  }
  ```

#### Exemple simplifié – compte de stockage

- **Ressource principale :**
  ```json
  {
    "type": "Microsoft.Storage/storageAccounts",
    "apiVersion": "2021-04-01",
    "name": "[parameters('storageAccountName')]",
    "location": "[resourceGroup().location]",
    "sku": { "name": "Standard_LRS" },
    "kind": "StorageV2"
  }
  ```

#### Avantages ARM

- Déploiement **déclaratif** (on décrit l’état cible).
- Déploiement **parallèle** de ressources.
- Gestion automatique des **dépendances** (`dependsOn`).
- **Idempotence** (même résultat si relancé).
- **Validation** du template avant déploiement.

---

## 6. Monitoring, sécurité et conformité

### 6.1 Azure Monitor

- Service de monitoring complet pour **applications** + **infrastructure**.

#### Composants

1. **Métriques :**
   - Valeurs numériques en temps réel.
   - Ex : CPU, mémoire, réseau, disque.
   - Graphiques + alertes.

2. **Journaux (Logs) :**
   - Événements détaillés.
   - Stockés dans un **Log Analytics Workspace**.
   - Langage de requête **KQL** (Kusto Query Language).

3. **Alertes :**
   - Basées sur **métriques** ou **logs**.
   - Déclenchent notifications ou actions automatiques.
   - Groupes d’action (email, SMS, webhook, etc.).

4. **Application Insights :**
   - Monitoring d’applications (APM).
   - Perf, disponibilité, traces.
   - Détection d’anomalies.

#### Métriques importantes pour VMs Windows

- Pourcentage CPU.
- Mémoire disponible.
- Octets disque lus/écrits par seconde.
- Octets réseau entrant/sortant.
- Disponibilité (uptime).

### 6.2 Azure Security Center / Microsoft Defender for Cloud

- Service de posture de sécurité + protection contre menaces.

- **Fonctionnalités :**
  - Évaluation continue de la sécurité.
  - Recommandations de sécurité.
  - Score de sécurité global.
  - Protection contre menaces (détections).
  - Conformité réglementaire (benchmarks).

- **Recommandations typiques :**
  - Activer le **chiffrement des disques**.
  - Appliquer les **mises à jour** OS.
  - Configurer des **NSG**.
  - Activer **MFA**.
  - Activer les **sauvegardes**.

### 6.3 Sécurité & conformité – Azure

#### 6.3.1 Modèle de responsabilité partagée

- **Microsoft (toujours) :**
  - Sécurité physique des datacenters.
  - Infrastructure réseau.
  - Hyperviseur.

- **Client (toujours) :**
  - Données.
  - Comptes et identités.
  - Appareils des utilisateurs finaux.

- **Responsabilités variables (IaaS/PaaS/SaaS) :**
  - OS.
  - Réseau virtuel.
  - Applications.
  - Contrôles d’accès réseau.

#### 6.3.2 Principes de sécurité Azure

1. **Défense en profondeur :**
   - Plusieurs couches de sécurité.
   - Éviter le point de défaillance unique.

2. **Moindre privilège :**
   - Don’t give plus de droits que nécessaire.
   - Utilisation de **RBAC** (Role-Based Access Control).

3. **Chiffrement :**
   - **Au repos** (disques, stockage).
   - **En transit** (TLS).
   - Gestion des clés via **Azure Key Vault**.

4. **Surveillance continue :**
   - Logging détaillé.
   - Détection d’anomalies.
   - Réponse aux incidents.

#### 6.3.3 Conformité & réglementations

- Certifications Azure :  
  - ISO/IEC 27001  
  - SOC 1, 2, 3  
  - PIPEDA (Canada)  
  - HIPAA (US, santé)  
  - RGPD (EU)  

- Pour le Québec :
  - **Loi 25** (protection des renseignements personnels).
  - Résidence des données au Canada (Canada Central/Est).
  - Souveraineté des données.

---

## 7. Laboratoire 1 – Environnement Azure de base

### 7.1 Objectifs

- Créer un compte Azure (ou utiliser un existant).
- Se familiariser avec le portail.
- Créer un **groupe de ressources**.
- Configurer **Cloud Shell**.
- Mettre en place une **alerte de budget**.

### 7.2 Étapes clés

#### 7.2.1 Compte Azure gratuit

- URL : `https://azure.microsoft.com/fr-ca/free/`
- 200 $ CAD de crédits (30 jours).
- Services gratuits 12 mois + services toujours gratuits.
- Carte de crédit uniquement pour vérification.

#### 7.2.2 Portail Azure

- URL : `https://portal.azure.com`
- Barre du haut :
  - Menu principal, recherche, Cloud Shell, notifications, paramètres, aide, profil.
- Menu gauche :
  - Tableau de bord, Tous les services, ressources récentes, favoris.
- Catégories de services :
  - Calcul, mise en réseau, stockage, bases de données, identité (Azure AD).

#### 7.2.3 Personnalisation du portail

- Paramètres :
  - Langue : Français (Canada).
  - Thème : clair/sombre.
  - Comportement du menu (ancré/volant).
  - Format date/heure : Canada (en-CA).

#### 7.2.4 Abonnement

- Menu **Abonnements** :
  - Nom (ex : Essai gratuit).
  - ID d’abonnement.
  - État (Actif).
  - Utilisation + quotas.

#### 7.2.5 Groupe de ressources

- Nom : `RG-Formation-Cloud`.
- Région : Canada Central ou Canada East (pour :
  - Conformité lois canadiennes.
  - Latence réduite au Québec.
  - Respect Loi 25).
- Tags :
  - Environnement = Formation.
  - Propriétaire = [Votre nom].
  - Cours = CloudComputing.

#### 7.2.6 Cloud Shell

- Icône `>_` dans le portail.
- Choisir **PowerShell**.
- Création automatique de compte de stockage.
- Commandes de base :
  - `Get-AzSubscription`
  - `Get-AzResourceGroup`
  - `Get-AzResourceGroup -Name "RG-Formation-Cloud"`

#### 7.2.7 Gestion des coûts

- Menu **Gestion des coûts + facturation**.
- Analyse du coût :  
  coûts à ce jour, prévisionnels, par service, par RG.
- **Budget :**
  - Nom : `Budget-Formation`.
  - Montant : 50 CAD, mensuel.
  - Alerte à 80 % (40 $) par email.

---

## 8. Laboratoire 2 – VM Windows Server + IIS

### 8.1 Objectifs

- Créer une **VM Windows Server 2025/2022**.
- Configurer le réseau (VNet + NSG).
- Se connecter par RDP.
- Installer IIS et tester.

### 8.2 VNet

- Nom : `VNet-Formation`.
- RG : `RG-Formation-Cloud`.
- Région : Canada Central.
- Address space : `10.0.0.0/16`.
- Subnet :  
  - Nom : `Subnet-Serveurs`.  
  - Plage : `10.0.1.0/24`.

### 8.3 NSG

- Nom : `NSG-Serveurs`.
- Règles entrantes :
  - **Allow-RDP** :
    - Service : RDP (port 3389).
    - Source : Any.
    - Priorité : 300.
  - **Allow-HTTP** :
    - Service : HTTP (port 80).
    - Source : Any.
    - Priorité : 310.

> En production : restreindre les sources IP.

### 8.4 VM Azure

- Nom : `VM-WinServer2025`.
- RG : `RG-Formation-Cloud`.
- Région : Canada Central.
- Image :
  - Windows Server 2025 Datacenter Azure Edition x64 Gen2  
  - ou Windows Server 2022 Datacenter Gen2 si 2025 indisponible.
- Taille : `Standard_B2s` (2 vCPU, 4 Go RAM).
- Compte admin :
  - `adminlocal` / `P@ssword2025!` (ou similaire).
- Ports publics autorisés : RDP (3389).
- Licence Windows : cocher l’option Azure Hybrid Benefit si applicable.
- Disques :
  - OS : **Premium SSD**, chiffrement au repos par défaut.
  - Data : disque supplémentaire, ex. 32 GiB (P4).
- Réseau :
  - VNet : `VNet-Formation`.
  - Subnet : `Subnet-Serveurs`.
  - IP publique : statique, SKU Standard.
  - NIC : associée au NSG `NSG-Serveurs`.
- Gestion :
  - Activer Defender (plan gratuit).
  - Diagnostics de démarrage activés.
  - Arrêt automatique : 19h, fuseau UTC-05:00 (Eastern).

- Tags :
  - Environnement = Formation.
  - Serveur = WebServer.
  - OS = WindowsServer2025.

### 8.5 Connexion RDP

- Se connecter à l’IP publique via `mstsc` ou fichier `.rdp`.
- Utilisateur : `adminlocal`.
- Mot de passe : celui défini à la création.

### 8.6 Configuration Windows Server

- Vérifier **Gestionnaire de serveur**.
- Configurer fuseau horaire : (UTC-05:00) Eastern Time.
- Désactiver la configuration de sécurité renforcée d’IE (pour test).

### 8.7 Installation IIS

- Gestionnaire de serveur → Gérer → Ajouter des rôles.
- Rôle : **Serveur Web (IIS)**.
- Ajouter les fonctionnalités proposées.
- Accepter le redémarrage auto si nécessaire.
- Vérifier :
  - `http://localhost`
  - `http://[IP publique]`

### 8.8 Personnalisation page IIS

- Fichier : `C:\inetpub\wwwroot\iisstart.htm`.
- Modifier `<title>`, ajouter `<h1>` personnalisé.
- Recharger la page.

### 8.9 Métriques VM & arrêt

- **Métriques :** CPU, réseau, disque.
- **Arrêt pour coûts :**
  - Arrêter via portail (`Arrêt` → état : Arrêté (libéré)).
  - Important : un simple shutdown depuis Windows **continue** la facturation du compute.

---

## 9. Laboratoire 3 – Azure AD (Entra ID)

### 9.1 Objectifs

- Configurer **Azure AD / Entra ID**.
- Créer utilisateurs + groupes.
- Attribuer des rôles.
- Activer **MFA** via accès conditionnel.

### 9.2 Locataire & domaine

- Noter :
  - Nom du locataire.
  - Domaine principal : `xxxx.onmicrosoft.com`.
  - ID de locataire (GUID).
- Domaine personnalisé (optionnel) via enregistrement TXT DNS.

### 9.3 Groupes

- Type : **Sécurité**, appartenance : affectée.
- Groupes :
  - `Groupe-Informatique`.
  - `Groupe-Etudiants`.
  - `Groupe-Enseignants`.

### 9.4 Utilisateurs

- Tech 1 :
  - `tech1@[domaine].onmicrosoft.com`
  - Nom : Marc Tremblay.
  - Mot de passe temporaire : `P@ssword123!`.
  - Doit changer le mot de passe à la première connexion.
  - Groupe : `Groupe-Informatique`.
  - Rôle : utilisateur standard.
- Étudiant :
  - `etudiant1@[domaine].onmicrosoft.com` (Sophie Gagnon).
  - Groupe : `Groupe-Etudiants`.
- Prof :
  - `prof1@[domaine].onmicrosoft.com` (Jean Laporte).
  - Groupe : `Groupe-Enseignants`.

### 9.5 Rôles administratifs

- Exemple de rôle : **Administrateur de support technique** pour `tech1`.

  - Peut :
    - Réinitialiser mots de passe des non-admin.
    - Gérer MFA.
    - Surveiller l’état du service.

- Autres rôles importants :
  - Administrateur général.
  - Administrateur d’utilisateurs.
  - Administrateur de facturation.
  - Administrateur Exchange (si applicable).

### 9.6 MFA via accès conditionnel

- Sécurité → Accès conditionnel → Nouvelle stratégie.
- Nom : `MFA-Administrateurs`.
- Utilisateurs :
  - Rôles d’annuaire → sélectionner **Administrateur de support technique**.
- Ressources : toutes les applications cloud.
- Contrôles d’accès :
  - Accorder l’accès **en exigeant la MFA**.
- Activer la stratégie.

- Test : connexion avec `tech1`, configuration de Microsoft Authenticator + téléphone (SMS).

### 9.7 Journaux

- **Journaux d’activité → Connexions :**
  - Qui, quand, IP, statut, application.
- **Journaux d’audit :**
  - Création d’utilisateurs.
  - Modif de groupes.
  - Changements de rôles.

---

## 10. Laboratoire 4 – Azure AD Connect (AD on-prem ↔ Azure AD)

### 10.1 Objectifs

- Installer/configurer **Azure AD Connect**.
- Synchroniser utilisateurs, groupes, mots de passe.
- Tester la connexion avec identifiants synchronisés.

### 10.2 AD on-prem (VM Windows Server 2025)

- Installer rôle **AD DS**.
- Promouvoir en **contrôleur de domaine** :
  - Nouvelle forêt : `formation.local`.
  - DC : catalogue global + DNS.
  - DSRM password : `P@ssw0rdDSRM2025!`.

### 10.3 Structure AD

- UO :
  - `UtilisateursEntreprise`.
  - `UtilisateursEntreprise\Informatique`.
  - `UtilisateursEntreprise\RessourcesHumaines`.
  - `UtilisateursEntreprise\Comptabilite`.

- Utilisateurs (exemples) :
  - Informatique : `plavoie`, `amelanger`, `jdubois`.
  - RH : `lmartin`, `mbouchard`.
  - Comptabilité : `sroy`, `rcote`.
  - Mot de passe commun labo : `P@ssw0rd2025!` (mot de passe n’expire jamais).

- Groupes :
  - `GRP-Informatique`.
  - `GRP-RessourcesHumaines`.
  - `GRP-Comptabilite`.
  - Ajouter les utilisateurs correspondants.

### 10.4 Compte de service AD Connect

- UO : `ComptesServices`.
- Utilisateur : `ADConnect` (Sync AzureAD).
- Mot de passe : `P@ssw0rdSync2025!`.
- Mot de passe non expirant, non modifiable par l’utilisateur.

### 10.5 Installation Azure AD Connect

- Télécharger `AzureADConnect.msi`.
- Choisir **Personnaliser** (pour voir options).
- Mode : **Synchronisation de hachage de mot de passe**.
- Se connecter avec **administrateur global** Azure AD.
- Ajouter la forêt `formation.local` :
  - Utiliser le compte `FORMATION\ADConnect`.
- UPN source : `userPrincipalName`.
- Filtrage :
  - **Synchroniser seulement** `UtilisateursEntreprise` (et sous-UO).
- Identifier unique : `ms-DS-ConsistencyGuid`.
- Fonctionnalités facultatives :
  - Password hash sync (déjà).
  - Writeback de mot de passe.
  - Group writeback (si souhaité).
- Démarrer la synchronisation immédiatement.

### 10.6 Vérification dans Azure

- Azure AD → Utilisateurs :
  - Les comptes on-prem deviennent `xxx@[domaine].onmicrosoft.com`.
  - Source : Windows Server AD.
  - Synchronisé : Oui.
- Azure AD → Azure AD Connect :
  - État d’approvisionnement : Active.
  - Dernière synchro récente.
  - Password hash sync activé.

### 10.7 Synchronisation et tests

- Planificateur :
  - Intervalle : 30 min (par défaut).
  - Cmdlets :
    - `Get-ADSyncScheduler`
    - `Start-ADSyncSyncCycle -PolicyType Delta`
    - `Start-ADSyncSyncCycle -PolicyType Initial`
    - `Set-ADSyncScheduler -CustomizedSyncCycleInterval 01:00:00`

- Test :
  - Connexion à `portal.azure.com` avec `plavoie@[domaine].onmicrosoft.com` + mot de passe AD on-prem (`P@ssw0rd2025!`).

### 10.8 Modifications & groupes

- Modifier un utilisateur on-prem (téléphone, service, adresse).
- Forcer une synchro Delta.
- Vérifier les champs mis à jour dans Azure AD.
- Groupes :
  - `GRP-Informatique`, etc. synchronisés avec leurs membres.
  - Utilisables dans Azure (RBAC, accès apps, etc.).

### 10.9 Monitoring des erreurs de synchro

- Outil : **Synchronization Service**.
  - Onglet **Operations** : exécutions, statuts, erreurs.
  - Onglet **Connectors** : connecteur AD on-prem, connecteur Azure AD.
- Erreurs courantes :
  - Attribut manquant.
  - Duplication.
  - Permissions insuffisantes.

---

## 11. Laboratoire 5 – Automatisation avec PowerShell + ARM

### 11.1 Objectifs

- Automatiser :
  - Création de RG.
  - Création de VMs + infra réseau.
  - Gestion de l’état des VMs (start/stop/restart/status).
  - Déploiement via **ARM Templates**.
- Utiliser **Az PowerShell**.

### 11.2 Préparation PowerShell

- Installer module Az :
  - `Install-Module -Name Az -Repository PSGallery -Force -AllowClobber`.
- Importer :
  - `Import-Module Az`.
- Connexion :
  - `Connect-AzAccount`.
  - `Get-AzSubscription`.
  - `Select-AzSubscription -SubscriptionName "..."`.

### 11.3 Script – création groupe de ressources

- Paramètres :
  - `NomGroupe` (obligatoire).
  - `Region` (CanadaCentral, CanadaEast).
- Logique :
  - Vérifier si connecté à Azure (`Get-AzContext` sinon `Connect-AzAccount`).
  - Vérifier existence du RG (`Get-AzResourceGroup -ErrorAction SilentlyContinue`).
  - Créer si absent :
    - `New-AzResourceGroup -Name ... -Location ... -Tag @{ Environnement="Formation"; CréePar="PowerShell"; DateCreation=... }`.
  - Affichage formaté : `Get-AzResourceGroup -Name ... | Format-List`.

### 11.4 Script – création VM complète

- Paramètres :
  - NomVM, GroupeRessources (obligatoires).
  - Region, TailleVM, NomUtilisateur (options).
  - MotDePasse (SecureString, obligatoire).
- Étapes :
  1. Vérifier/créer VNet (`VNet-[RG]`) + subnet `Subnet-Serveurs`.
  2. Créer IP publique statique (`[NomVM]-IP`, SKU Standard).
  3. Créer NSG + règles RDP (3389) et HTTP (80).
  4. Créer NIC associée au subnet, IP publique, NSG.
  5. Crédentials (`PSCredential`).
  6. Créer config VM :
     - OS Windows, VM agent, updates.
     - Image Windows Server 2022 datacenter-azure-edition.
     - OS Disk Premium_LRS.
  7. `New-AzVM` pour créer la VM.
  8. Afficher résumé (Nom, RG, Région, Taille, IP, user, commande RDP).

- Exemple d’appel :
  ```powershell
  $mdp = ConvertTo-SecureString "P@ssword2025!" -AsPlainText -Force
  .\CreerVM.ps1 -NomVM "VM-Auto01" -GroupeRessources "RG-Automatisation" -MotDePasse $mdp
  ```

### 11.5 Script – gestion des VMs (Start/Stop/Restart/Status)

- Paramètres :
  - GroupeRessources.
  - Action (Start, Stop, Restart, Status).
  - NomVM (optionnel, `*` par défaut pour toutes).
- Logique :
  - Récupérer VMs dans RG.
  - Boucler :
    - Start : `Start-AzVM -NoWait`.
    - Stop : `Stop-AzVM -Force -NoWait`.
    - Restart : `Restart-AzVM -NoWait`.
    - Status : `Get-AzVM -Status` → `PowerState`.

### 11.6 ARM Template – VM simple

- Fichier `template-vm.json` :
  - Paramètres :
    - nomVM, tailleVM, nomUtilisateur, motDePasse (securestring).
  - Variables :
    - nomVNet, nomSubnet, nomIPPublique, nomNSG, nomNIC.
  - Resources :
    - NSG (Allow-RDP).
    - VirtualNetwork + subnet.
    - Public IP.
    - NIC (avec IP publique, subnet, NSG).
    - VM (Windows Server 2022 datacenter-azure-edition, Premium_LRS).
  - Outputs :
    - IP publique.
    - nomVM.

- Fichier `parameters.json` :
  - Valeurs pour nomVM, tailleVM, nomUtilisateur, motDePasse.

### 11.7 Script – déploiement ARM

- Paramètres :
  - GroupeRessources.
  - CheminTemplate.
  - CheminParametres.
- Étapes :
  - `Test-AzResourceGroupDeployment` pour **valider**.
  - Si erreurs → affichage & stop.
  - Sinon `New-AzResourceGroupDeployment ... -Verbose`.
  - Vérifier `ProvisioningState`.
  - Afficher `Outputs`.

### 11.8 ARM Template – infrastructure multi-VM

- Paramètres :
  - prefixeNom (ex. `Prod`).
  - nombreVMs (1–5).
  - nomUtilisateur.
  - motDePasse (securestring).
- Variables :
  - nomVNet, nomNSG.
- Resources :
  - NSG (Allow-RDP, Allow-HTTP).
  - VNet avec subnets : Subnet-Web (10.0.1.0/24), Subnet-App, Subnet-DB.
  - Public IP avec `copy` (une par VM).
  - NICs avec `copy`.
  - VMs avec `copy` (Windows 2022, Standard_B2s, tags Environnement=Production, Tier=Web).
- Outputs :
  - Liste des VMs + IP publiques (array, `copy` dans outputs).

### 11.9 Script d’orchestration (automatisation complète)

- Paramètres :
  - NomEnvironnement (ex : `Prod`, `Test`, etc.).
  - NombreVMs (par défaut 2).
  - Region (CanadaCentral par défaut).
- Étapes :
  1. Créer/valider RG `RG-[NomEnvironnement]`.
  2. Déployer infra réseau via template.
  3. Déployer VMs via template.
  4. Créer workspace Log Analytics `LogAnalytics-[NomEnvironnement]`.
  5. Afficher résumé (RG, région, nb VMs, workspace, etc.).
