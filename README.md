Conçue pour aider à suivre ses données et à prendre des décisions éclairées concernant votre traitement du diabète, MyPod est un projet qui permet d'utiliser les pompes à insuline Omnipod Dash directement depuis votre téléphone personnel. 


![Diagramme du projet](diagramme_projet.pdf)



# Guide de déploiement pour MyPod

Ce guide fournit des instructions sur la manière de déployer MyPod, une application Android, ainsi que les étapes nécessaires pour installer le projet Flutter sous Linux.

## Déploiement de MyPod sur des appareils Android

Pour tester MyPod sur des appareils Android, suivez ces étapes :

1. **Transférez les fichiers APK sur un appareil Android** :
   - Connectez votre appareil Android à votre ordinateur via USB.
   - Transférez les fichiers APK vers votre appareil Android.
   - Sur votre appareil Android, ouvrez les fichiers APK pour les installer et suivez les instructions à l'écran.

   Assurez-vous d'avoir deux appareils Android, l'un pour MyPod et l'autre pour simuler la pompe (podapp).

## Installation du projet Flutter sous Linux

Si vous souhaitez installer et développer MyPod sur un système Linux, suivez ces étapes :

1. **Téléchargement de Flutter** :
   - Ouvrez un terminal sur votre système Linux.
   - Téléchargez l'archive Flutter depuis le site officiel en utilisant la commande suivante :

     ```
     curl -O https://storage.googleapis.com/flutter_infra/releases/stable/linux/flutter_linux_2.5.3-stable.tar.xz
     ```

   - Extrayez l'archive Flutter dans un répertoire de votre choix :

     ```
     tar xf flutter_linux_2.5.3-stable.tar.xz
     ```

   - Ajoutez le chemin du répertoire `flutter/bin` à votre variable d'environnement `PATH` en éditant votre fichier `.bashrc` ou `.zshrc` :

     ```
     export PATH="$PATH:`pwd`/flutter/bin"
     ```

   - Rechargez votre terminal ou exécutez la commande suivante pour appliquer les modifications :

     ```
     source ~/.bashrc
     ```

2. **Configuration de Flutter** :
   - Vérifiez l'installation de Flutter en exécutant la commande suivante :

     ```
     flutter doctor
     ```

   - Suivez les instructions pour installer les dépendances manquantes telles que les outils de développement Android Studio, les packages nécessaires pour Android et/ou iOS, etc.

3. **Récupération du projet Flutter existant** :
   - Ouvrez un terminal.
   - Accédez au répertoire de votre projet Flutter existant en utilisant la commande `cd`.

4. **Installation des dépendances du projet** :
   - Exécutez la commande `flutter pub get` pour installer toutes les dépendances déclarées dans le fichier `pubspec.yaml`.

     ```
     flutter pub get
     ```

## Développement et test

Utilisez `flutter run` pour tester votre application sur un émulateur ou un appareil Android.
