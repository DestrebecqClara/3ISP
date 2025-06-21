# Ansible DunderMifflin

## Schéma de l'infrastructure


## Prérequis

* Un environnement Linux avec Python installé.
* Installer les dépendances Python grâce au `requirements.txt` :

  ```sh
  pip install -r requirements.txt
  ```
* Un utilisateur Linux identique sur toutes les machines cibles.
* La clé SSH de cet utilisateur doit être déployée et autorisée sur tous les serveurs distants.

---

## Installation

### Déploiement complet

```sh
ansible-playbook -i inventory.yml deploy.yml
```

Ce playbook install et configure automatiquement tous les services sur les hôtes définis dans `inventory.yml`.

---

## Maintenance

```sh
ansible-playbook -i inventory.yml maintenance.yml
```

---

## Structure du projet

* `inventory.yml` : liste des hôtes et groupes cibles.
* `deploy.yml` : playbook principal de déploiement.
* `maintenance.yml` : playbook pour les opérations de maintenance.
* `roles/` : répertoires contenant les rôles Ansible correspondant à chaque services souhaité
* `requirements.txt` : dépendances Python nécessaires pour le projet.