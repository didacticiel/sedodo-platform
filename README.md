Sèdodo : L'artisan de confiance, à portée de clic.

Sèdodo est une plateforme qui met en relation les utilisateurs du Bénin avec des artisans et prestataires de services vérifiés, notés et garantis. Nous transformons la recherche d'artisan d'une loterie en un choix éclairé et sécurisé.

Table des Matières
Vue d'Ensemble
Fonctionnalités
Stack Technique
Structure du Projet
Démarrage Rapide (Développement)
Documentation de l'API
Tests
Déploiement
Contribuer
Politique de Sécurité
Licence
Contact
Vue d'Ensemble
Le secteur informel au Bénin, bien que vibrant, souffre d'un manque de structure et de confiance. Trouver un plombier, un électricien ou un coiffeur fiable est un défi quotidien, source de stress et de mauvaises expériences.

Notre Mission : Construire la colonne vertébrale numérique de confiance pour l'économie des services au Bénin. Nous nous engageons à :

Vérifier rigoureusement chaque professionnel sur notre plateforme.
Garantir la transparence grâce à un système de notation authentique.
Sécuriser chaque transaction pour la tranquillité d'esprit de nos utilisateurs.
Sèdodo n'est pas seulement une application, c'est un engagement envers la qualité et la fiabilité.

# Fonctionnalités
🔍 Recherche Avancée d'Artisans: Filtrez par métier, localisation, note et disponibilité.
✅ Profils d'Artisans Vérifiés: Badge "Sèdodo Certifié" pour les professionnels ayant passé notre audit.
⭐ Système de Notation et Avis: Laissés uniquement après une transaction validée pour garantir l'authenticité.
💳 Paiement Sécurisé via Mobile Money: Intégration de Moov Money et MTN Mobile Money.
🛡️ Garantie de Satisfaction: Service couvert par notre garantie en cas de litige.
📱 Interface Web Responsive: Une expérience utilisateur optimale sur desktop et mobile.
📊 Tableau de Bord Artisan: Gérez vos missions, vos revenus et votre réputation.

# Stack Technique
Backend: Python 3.10+, Django 4.2+, Django REST Framework
Frontend: HTML5, Tailwind CSS, Alpine.js (pour l'interactivité légère)
Base de Données: PostgreSQL 14+
Cache: Redis 6+
Authentification: Simple JWT (JSON Web Tokens)
Déploiement: Docker, Docker Compose, Gunicorn, Nginx
Outils de Dév: Black (formateur), Flake8 (linting), pytest (tests)

# Structure du Projet
sedodo_platform/
├── .env.example
├── .gitignore
├── docker-compose.yml
├── Dockerfile
├── manage.py
├── requirements.txt
├── requirements-dev.txt
├── pytest.ini
├── .flake8
├── sedodo_platform/
│   ├── __init__.py
│   ├── settings/
│   │   ├── __init__.py
│   │   ├── base.py
│   │   ├── development.py
│   │   ├── production.py
│   │   └── testing.py
│   ├── urls.py
│   └── wsgi.py
├── apps/
│   ├── __init__.py
│   ├── accounts/
│   ├── marketplace/
│   ├── payments/
│   └── core/
└── static/
└── templates/

Démarrage Rapide (Développement)
Pour exécuter ce projet localement, assurez-vous d'avoir les prérequis installés.

Prérequis
Python 3.10+
PostgreSQL 14+
Redis 6+
Docker & Docker Compose (recommandé)
Installation avec Docker (Recommandé)

# Cloner le dépôt
git clone https://github.com/didacticiel/sedodo-platform.git
cd sedodo-platform
# ---- Configurer les variables d'environnement
cp .env.example .env
# ---Éditez le fichier .env avec vos configurations locales (clés secrètes, BDD, etc.)

# Lancer les services avec Docker Compose
docker-compose up --build

Cette commande va construire les images, lancer les conteneurs pour l'application, PostgreSQL et Redis, et appliquer les migrations automatiquement.
Accéder à l'application
API : http://localhost:8000/api/
Documentation API (Swagger) : http://localhost:8000/api/docs/
Admin Django : http://localhost:8000/admin/
Installation Manuelle
Cloner le dépôt et créer l'environnement virtuel

git clone git@github.com:didacticiel/sedodo-platform.gitt
cd sedodo-platform
python -m venv venv
source venv/bin/activate  # Sur Windows: venv\Scripts\activate

# Installer les dépendances
pip install -r requirements-dev.txt

# lancer les migrations
python manage.py migrate

#   créer un superutilisateur
python manage.py createsuperuser

# Lancer le server de developpement
python manage.py runserver

# Documentation de l'API
La documentation interactive de l'API est générée avec drf-spectacular (OpenAPI 3.0).
Une fois le serveur lancé, accédez à :

Swagger UI: http://localhost:8000/api/docs/
ReDoc: http://localhost:8000/api/redoc/

# Tests
Nous utilisons pytest pour nos tests. Pour exécuter la suite de tests :

# Pour exécuter tous les tests
pytest

# Pour exécuter les tests avec un rapport de couverture
pytest --cov=. --cov-report=html

Déploiement
Le déploiement en production est conçu pour être effectué avec Docker et Docker Compose sur un serveur Linux.

Configurer l'environnement de production en copiant .env.example vers .env et en remplissant les variables de production (settings/production.py).

# Construire et lancer les conteneurs en mode production :

docker-compose -f docker-compose.prod.yml up --build -d
# Collecter les fichiers statiques :
docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input




Contribuer
Nous apprécions votre intérêt pour contribuer à Sèdodo ! Veuillez lire notre Guide de Contribution pour connaître nos procédures et nos standards de code.

Politique de Sécurité
Nous prenons la sécurité très au sérieux. Si vous découvrez une vulnérabilité, ne l'ouvrez pas dans un issue. Veuillez consulter notre Politique de Sécurité pour nous contacter de manière responsable.

Licence
Ce projet est sous licence MIT. Consultez le fichier LICENSE pour plus de détails.

Contact
Projet: https://github.com/your-username/sedodo-platform
Site Web: https://www.sedodo.bj (lorsque disponible)
Email: contact@sedodo.bj


