Voici une description que vous pouvez inclure dans le fichier `README.md` ou dans la section description de votre dépôt Git :

---

# MediaWiki Azure Container App

Ce dépôt contient la structure, les configurations et les scripts nécessaires pour déployer une instance de **MediaWiki** dans une **Azure Container App**. Il est conçu pour faciliter le développement, l'intégration continue (CI/CD) et l'automatisation du déploiement, tout en offrant une flexibilité pour personnaliser les extensions et les thèmes.

## Contenu du dépôt

- **Dockerfile** : Construisez une image Docker personnalisée pour MediaWiki avec vos extensions et thèmes.
- **Configurations Kubernetes** : Déployez MediaWiki dans un environnement Kubernetes avec des fichiers YAML (deployment, service, ingress).
- **Automatisation Azure** : Modèles Bicep et Terraform pour provisionner l'infrastructure Azure nécessaire (base de données, ACR, réseaux, etc.).
- **Scripts** : Scripts Bash pour automatiser les étapes clés comme la construction, l'initialisation de la base de données, et le déploiement.
- **CI/CD** : Pipeline YAML pour Azure DevOps pour gérer les builds et déploiements.
- **Personnalisation** : Répertoires dédiés pour ajouter des extensions, des skins et des configurations MediaWiki personnalisées.

## Fonctionnalités

- **Déploiement Conteneurisé** : MediaWiki est conteneurisé et prêt à être déployé via Azure Container Apps.
- **Extensibilité** : Prise en charge facile des extensions et thèmes personnalisés.
- **Scalabilité** : Configurations Kubernetes prêtes pour un déploiement dans un cluster AKS.
- **Automatisation** : Scripts et modèles pour simplifier le provisionnement et le déploiement.

## Prérequis

- Compte Azure et configuration CLI (`az login`)
- Docker installé localement pour la construction des images
- Accès à un registre de conteneurs (Azure Container Registry recommandé)
- Kubernetes (optionnel, pour les déploiements avancés)

## Instructions de Déploiement

1. Clonez ce dépôt :
   ```bash
   git clone https://github.com/votre-repo/mediawiki-azure-container-app.git
   cd mediawiki-azure-container-app
   ```

2. Configurez vos variables d'environnement dans le fichier `env/.env`.

3. Construisez l'image Docker :
   ```bash
   ./scripts/build-docker.sh
   ```

4. Déployez l'application dans Azure :
   ```bash
   ./scripts/deploy.sh
   ```

5. Accédez à votre application via l'URL générée.

## Contribution

Les contributions sont les bienvenues ! Veuillez soumettre vos suggestions via des issues ou des pull requests.

## Licence

Ce projet est sous licence MIT. Consultez le fichier `LICENSE` pour plus de détails.

---

Vous pouvez adapter la description en fonction de votre audience et des objectifs spécifiques de votre projet.
