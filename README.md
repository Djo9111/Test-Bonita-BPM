# Test Bonita BPM : serveur Docker

Serveur Bonita Community 2025.2 pour tester des processus en local.
Les identifiants de ce dépôt sont des valeurs de test, à ne jamais réutiliser.

## Contenu

- docker-compose.yml : le serveur Bonita et, plus tard, Mailpit pour les mails de test

## Prérequis

- Docker et Docker Compose
- Bonita Studio Community 2025.2, pour concevoir les processus

## Démarrage

    docker compose up -d

Le serveur est ensuite accessible sur http://localhost:8081/bonita.
Le port 8081 évite le conflit avec le serveur de test intégré à Studio, qui utilise 8080.

## Comptes de test

- Compte technique : tech_user, mot de passe secret
- Les autres comptes sont créés dans l'application Super Administrator

## Notes

- L'image Community s'appelle bonita (image officielle), et non bonitasoft/bonita
- La base H2 intégrée convient pour un test, pas pour la production
- Le projet de processus est dans un autre dépôt : bonita-test