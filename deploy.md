# Rapport de déploiement - KEBAIER
## Liens
- **Application en ligne :** https://dashboard.scalingo.com/apps/osc-fr1/doctolib/deploy/list
- **Dépôt de code :** https://github.com/Arix631/doctolib/actions
## Prérequis techniques
PHP 8.4+ avec l'extension pdo_msql
Composer installé
Un compte Scalingo

## Fichier de configuration CI
Le fichier de configuration de l'intégration continue se trouve dans : .github/workflows/ci.yaml
## Procédure de déploiement pas à pas
(⚠️ Rien concernant la base de données )
A. Initialisation sur Scalingo
1. Créer l'application
2. Ajouter l'add-on MySQL
B. Ajout de variables d'environnement
Ajouter des variables d'environnement sur Scalingo
1. APP_ENV = prod
2. APP_SECRET = 4069138afbcf51712e91fd435baa7c8f
3. DATABASE_URL:DATABASE_URL="mysql://app:!ChangeMe!@127.0.0.1:3306/app?serverVersion=10.11.2-MariaDB&charset=utf8mb4"
C. Préparation du code
1. Nettoyer les migration locales: tout supprimer
2. Générer une nouvelle migration : php bin/console make:migration
3. Commit des changement git commit -m "Mise à jour effectuée"
D. Mise en ligne
1. Push des commits : git push