# M1IL-Ansible-25

## Description
Ce projet utilise Ansible pour automatiser le déploiement et la configuration de plusieurs outils de monitoring et de gestion de logs, notamment Grafana, Loki, Prometheus et Promtail. Il est conçu pour être utilisé dans un environnement AWS avec une configuration spécifique.

## Structure du projet

- **ansible.cfg** : Fichier de configuration Ansible.
- **aws/** : Contient les fichiers liés à AWS, comme les clés PEM.
- **inventories/** : Contient les fichiers d'inventaire pour définir les hôtes cibles.
- **playbooks/** : Contient les playbooks Ansible pour exécuter les tâches.
  - `bootstrap.yml` : Playbook pour les tâches de bootstrap.
  - `grafana.yml` : Playbook pour déployer et configurer Grafana.
  - `loki.yml` : Playbook pour déployer et configurer Loki.
  - `prometheus.yml` : Playbook pour déployer et configurer Prometheus.
  - `promtail.yml` : Playbook pour déployer et configurer Promtail.
- **roles/** : Contient les rôles Ansible pour chaque outil.
  - `bootstrap/`
  - `grafana/`
  - `loki/`
  - `prometheus/`
  - `promtail/`

Chaque rôle contient les sous-dossiers suivants :
  - `defaults/` : Variables par défaut.
  - `handlers/` : Gestionnaires pour les notifications.
  - `meta/` : Métadonnées du rôle.
  - `tasks/` : Tâches à exécuter.
  - `templates/` : Fichiers de template.
  - `tests/` : Fichiers de test.
  - `vars/` : Variables spécifiques.

## Prérequis

- Ansible installé sur votre machine locale.
- Accès SSH aux hôtes cibles avec la clé privée spécifiée dans `ansible.cfg`.
- Configuration des hôtes dans `inventories/lab-ipi-m1il.yml`.

## Utilisation

1. Clonez le dépôt :
   ```bash
   git clone <URL-du-dépôt>
   cd M1IL-Ansible-25
   ```

2. Exécutez un playbook :
   ```bash
   ansible-playbook playbooks/<nom-du-playbook>.yml
   ```

3. Vérifiez les résultats dans les outils déployés (Grafana, Loki, etc.).

## Auteur
Adel

## Licence
Ce projet est sous licence MIT.
