# Rapport de déploiement - KEBAIER
## Liens
- **Application en ligne :** https://doctolib.osc-fr1.scalingo.io/
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



D. Mise en ligne
1. Push des commits : git push