# ⚖️ LensJudge-Net 🌐

Bienvenue sur **LensJudge-Net** ! Ce projet est une version distribuée et parallélisée de **LensJudge**, permettant d'exécuter des jugements automatiques de code sur un réseau entièrement configuré. 🚀

## 🏗️ Architecture du projet

Notre système repose sur une architecture distribuée comprenant plusieurs composants :

### 🖥️ Serveur de jobs

- Reçoit les requêtes des **clients** 📩
- Assigne les tâches aux **runners** disponibles 🤖
- Génère un **classement** des scores des équipes 📊

### 🤖 Runners

- Exécutent les vérifications des soumissions 💻
- Utilisent des **threads** pour un traitement parallèle ⚡
- Renvoient les résultats au **serveur de jobs** ✅

### 🏃 Client

- Envoie un **programme** à vérifier au serveur 🎯
- Attend et affiche le résultat de la vérification ⏳

### 🌍 Routeur

- Connecte le réseau **local**, la **DMZ** et **inet** 🔀
- Configure les règles de **sécurité** et le pare-feu 🔒

## 🔌 Configuration du réseau

- 🌐 **Serveur de jobs** : hébergé en **DMZ** 🏢, accessible via `lensjudge.fr`
- 🖥️ **Runners** : situés sur un réseau privé sécurisé 🛡️
- 🌍 **Routeur** : assure la communication et la sécurité du réseau 🚦
- 📡 **Client** : soumet des programmes depuis Internet ou le réseau local 📶

⚠️ **Toutefois, la partie Java (client et serveur TCP) doit encore être retravaillée**, car elle n’a pas pu être finalisée par manque de temps. Certaines fonctionnalités restent incomplètes et nécessitent des ajustements.

## 📦 Déploiement

Chaque type de machine dispose de son **archive d'installation** (`.tar.gz`) et de son **script install.sh** :

- 📜 **Serveur de jobs** : `install.sh` configure le serveur et le lance au démarrage
- ⚙️ **Runners** : `install.sh` installe et configure l’environnement d'exécution
- 📡 **Routeur** : `install.sh` met en place le routage et la sécurité
- 🏃 **Client** : `install.sh` configure l’environnement de soumission

## 🚀 Lancement du projet

1. Cloner ce dépôt :
   ```bash
   git clone https://github.com/Dev-LucasP/LensJudge-Net.git
   cd LensJudge-Net
   ```
