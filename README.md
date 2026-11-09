# 🏥 TuniCare
### Plateforme intelligente de gestion des services de santé et d'assurance maladie

## 📌 Présentation du projet

**TuniCare** est une plateforme web qui permet de centraliser et de simplifier la gestion des services de santé et d'assurance maladie.

Elle offre aux assurés un accès facile à leurs couvertures médicales, aux professionnels de santé, aux rendez-vous médicaux et aux dossiers médicaux.

Le projet repose sur une architecture **Microservices**, garantissant la modularité, la sécurité et l'évolutivité de l'application.

## 🎯 Problématique

La gestion traditionnelle des services de santé présente plusieurs difficultés :

- Dispersion des informations médicales et administratives.
- Difficulté d'accès aux couvertures médicales.
- Complexité de la prise de rendez-vous.
- Difficulté de suivi des réclamations.
- Protection des données médicales sensibles.

## 🎯 Objectifs

- Centraliser les services de santé et d'assurance.
- Faciliter la communication entre les différents acteurs.
- Sécuriser les données personnelles et médicales.
- Simplifier la gestion des rendez-vous et des réclamations.
- Proposer une architecture évolutive basée sur les microservices.

## 👥 Acteurs du système

- **Assuré :** consulter sa couverture, rechercher un médecin, prendre un rendez-vous et déposer une réclamation.
- **Professionnel de santé :** gérer ses informations et les rendez-vous.
- **Agent administratif :** assurer le suivi des opérations administratives.
- **Administrateur :** gérer les utilisateurs et superviser la plateforme.

## ⚙️ Principales fonctionnalités

| Microservice | Responsabilités |
|---|---|
| User Service | Gestion des utilisateurs, des comptes, des rôles et de l'authentification |
| Coverage Service | Gestion des contrats, garanties et remboursements |
| Provider Service | Gestion des médecins, cliniques et pharmacies |
| Reclamation Service | Création et suivi des réclamations |
| Appointment Service | Gestion et réservation des rendez-vous |
| MedicalRecord Service | Gestion et consultation des dossiers médicaux |

## 🏗️ Architecture technique

Le projet utilise une architecture distribuée basée sur plusieurs microservices indépendants.

### Composants principaux

- **Angular :** développement de l'interface utilisateur.
- **API Gateway :** point d'entrée unique qui redirige les requêtes vers les microservices.
- **Eureka Server :** découverte et enregistrement des microservices.
- **Config Server :** centralisation de la configuration.
- **Keycloak :** gestion de l'authentification et des autorisations.
- **RabbitMQ :** communication asynchrone entre les microservices.
- **Docker :** conteneurisation et déploiement des composants.

### Fonctionnement général

1. L'utilisateur accède à l'application Angular.
2. Il s'authentifie à travers Keycloak.
3. Angular envoie une requête accompagnée d'un token JWT à l'API Gateway.
4. L'API Gateway identifie le microservice concerné.
5. Le microservice traite la requête et communique avec sa propre base de données.
6. Le résultat est retourné à l'application Angular.

## 🗄️ Microservices et bases de données

Chaque microservice possède sa propre base de données afin de garantir son indépendance.

| Microservice | Base de données |
|---|---|
| User Service | Base partagée |
| Coverage Service | MySQL |
| Provider Service | MongoDB |
| Reclamation Service | PostgreSQL |
| Appointment Service | CouchDB |
| MedicalRecord Service | Oracle Database |

## 🔄 Modes de communication

Deux modes de communication sont utilisés :

**1. Communication synchrone (REST)**

Utilisée lorsqu'un microservice a besoin d'une réponse immédiate d'un autre microservice.

Exemple : Appointment Service vérifie l'éligibilité d'un patient auprès de Coverage Service avant de confirmer un rendez-vous.

**2. Communication asynchrone (RabbitMQ)**

Utilisée pour transmettre des événements sans attendre une réponse immédiate.

Exemple : Appointment Service publie un événement `AppointmentCreated` après la création d'un rendez-vous.

## 🛠️ Technologies utilisées

- Frontend : Angular
- Backend : Spring Boot
- Architecture : Microservices
- API : REST
- Sécurité : Keycloak, JWT
- Service Discovery : Eureka Server
- Configuration : Spring Cloud Config Server
- Communication asynchrone : RabbitMQ
- Bases de données : MySQL, MongoDB, PostgreSQL, CouchDB et Oracle Database
- Conteneurisation : Docker
- Gestion du code source : Git et GitHub

## 👩‍💻 Organisation de l'équipe

Projet réalisé par l'équipe **Care Innovators** dans le cadre de la formation à ESPRIT.

| Membre | Microservice |
|---|---|
| Safa Alouani | Coverage Service |
| Malek Alouani | Provider Service |
| Islem Sallemi | Reclamation Service |
| Fatma Abdelaziz | Appointment Service |
| Safa Baalouch | MedicalRecord Service |
| Tous les membres | User Service (partagé) |

## 📅 Contexte du projet

- Établissement : ESPRIT
- Année : 2026
- Équipe : Care Innovators
- Projet : TuniCare

## 🚀 Conclusion

TuniCare vise à améliorer la gestion des services de santé et d'assurance maladie grâce à une plateforme centralisée et intelligente.

L'utilisation d'une architecture microservices permet de développer une solution modulaire, indépendante, sécurisée et évolutive, adaptée aux besoins des différents acteurs du domaine médical.

---

**© 2026 – TuniCare | Care Innovators**
