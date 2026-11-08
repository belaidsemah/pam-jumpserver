# Documentation Technique - Bastion PAM (JumpServer v5.0.0-ce)

## 1. Architecture des composants
- **Core / Web / SSH (Port 80 / 2222)** : Gère l'interface d'administration et les passerelles de rebond SSH/RDP.
- **Base de données (PostgreSQL 15)** : Stocke les utilisateurs, les actifs, les rôles et les journaux d'audit.
- **Cache (Redis 7)** : Gère les sessions, les jetons OAuth2 et les statistiques de ressources en temps réel.

## 2. Commandes de maintenance
- Démarrer la pile : `docker compose up -d`
- Consulter les logs : `docker logs -f jumpserver-core`
- Effectuer une mise à jour des migrations : `docker exec -it jumpserver-core ./jms upgrade`
