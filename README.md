# Conception et sécurisation d'une infrastructure Active Directory multidomaine

## Présentation du projet

Ce projet académique porte sur la conception, l'implémentation et la sécurisation d'une infrastructure Active Directory sous Windows Server, à partir de scénarios inspirés des besoins d'une entreprise.

L'objectif est de centraliser l'administration des identités, de sécuriser les accès aux ressources et de déployer des stratégies de groupe adaptées aux différents départements et environnements de travail.

## Architecture de l'infrastructure

L'environnement repose sur une forêt Active Directory multidomaine comprenant :

- **Domaine racine :** `sabrinatec.global`
- **Domaine enfant Europe :** `europe.sabrinatec.global`
- **Domaine enfant Recherche :** `research.sabrinatec.global`

L'infrastructure permet de gérer les utilisateurs, les ordinateurs, les ressources et les politiques de sécurité dans plusieurs domaines.

## Réalisations techniques

### 1. Déploiement et administration Active Directory

- Conception d'une architecture AD DS multidomaine.
- Organisation des utilisateurs et ordinateurs dans des unités d'organisation (OU).
- Administration centralisée des comptes et des ressources.
- Configuration des relations d'approbation entre domaines.

### 2. Sécurisation des comptes et des accès

- Mise en œuvre de politiques de mots de passe granulaires (FGPP).
- Configuration des paramètres de verrouillage des comptes.
- Application de politiques de sécurité adaptées aux groupes d'utilisateurs.

### 3. Gestion des stratégies de groupe (GPO)

- Création et déploiement de GPO.
- Configuration de la redirection des dossiers utilisateurs.
- Gestion des paramètres de sécurité des postes.
- Importation et adaptation de GPO entre domaines parent et enfant.

### 4. Contrôle des applications avec AppLocker

- Configuration de règles de restriction d'exécution.
- Mise en place d'un scénario de blocage de Notepad.
- Vérification du comportement des règles sur un poste client.

### 5. Sécurisation des postes partagés — Hot Desk

- Création d'une unité d'organisation dédiée aux postes partagés.
- Configuration du traitement en boucle des GPO (*Loopback Processing*) en mode Replace.
- Application d'un fond d'écran d'entreprise.
- Restriction de l'accès au Panneau de configuration.
- Mise en œuvre de restrictions du bureau et des périphériques USB.

## Tests et validation

Les configurations ont été contrôlées au moyen de tests fonctionnels et d'outils d'administration Windows, notamment :

```powershell
gpupdate /force
gpresult /r
nltest /domain_trusts
```

Les scénarios de validation portent sur l'application des GPO, les restrictions AppLocker, les relations d'approbation et les politiques des postes partagés.

## Compétences démontrées

- Administration Windows Server et Active Directory
- Gestion des identités et des accès
- Sécurisation des comptes utilisateurs
- Administration des stratégies de groupe
- Contrôle des applications et des postes de travail
- Dépannage et validation des politiques de sécurité
- Documentation technique

## Documentation du projet

Des captures issues du laboratoire seront ajoutées pour illustrer l'architecture Active Directory, les configurations de sécurité et les résultats des tests.

---

**Contexte :** Projet académique réalisé au Collège LaSalle, Montréal.

**Environnement :** Windows Server, Active Directory Domain Services, Group Policy Management et PowerShell.
