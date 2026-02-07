# 1. Sécurisation d’un serveur web Apache

### 1.1 Objectif

Déployer et sécuriser un serveur web Apache avec des restrictions d’accès et des permissions avancées.

---

### 1.2 Description

Ce mini-projet consiste à mettre en place un serveur Apache sécurisé sur une distribution Linux (Ubuntu ou CentOS), en appliquant des mécanismes de contrôle d’accès, de permissions avancées et de filtrage réseau.

---

### 1.3 Étapes du projet

#### 🔹 Installation du serveur web
- Installer un serveur **Apache** sur une distribution Linux (**Ubuntu** ou **CentOS**).

#### 🔹 Création du site web
- Créer un site web simple.
- Ajouter une page HTML dans le répertoire : /var/www/html

#### 🔹 Configuration des permissions avancées
- Créer un groupe nommé `webmasters`.
- Utiliser les **ACL (Access Control Lists)** pour donner les droits :
- Lecture
- Écriture  
au groupe `webmasters` sur le répertoire `/var/www/html`.

- Appliquer le **SGID** sur le répertoire afin que tous les nouveaux fichiers héritent automatiquement du groupe.

- Configurer le **sticky bit** pour empêcher la suppression de fichiers par des utilisateurs non autorisés.

#### 🔹 Sécurisation réseau avec iptables
- Configurer **iptables** pour limiter l’accès au port **80 (HTTP)** :
- Autoriser uniquement une plage d’adresses IP spécifique (ex. : réseau local).

#### 🔹 Configuration de sudo
- Créer une règle **sudoers** permettant à un administrateur :
- De redémarrer le service Apache
- Sans demander de mot de passe

#### 🔹 Tests de sécurité
- Tester l’accès au site web depuis :
- Une adresse IP non autorisée
- Tester la modification ou la suppression de fichiers :
- Avec un utilisateur non privilégié

---

### 1.4 Résultat attendu

- Le serveur Apache est fonctionnel.
- L’accès au site est restreint par IP.
- Les permissions et ACL sont correctement appliquées.
- Seuls les utilisateurs autorisés peuvent modifier les fichiers.
- L’administrateur peut redémarrer Apache via sudo sans mot de passe.

---

### 1.5 Technologies utilisées

- Apache
- Linux (Ubuntu / CentOS)
- ACL
- iptables
- sudo

---

✅ **Projet orienté sécurité système et administration Linux**
