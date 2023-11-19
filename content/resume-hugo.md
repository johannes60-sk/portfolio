---
title: "Resume Hugo"
description: "Un petit resume sur hugo"
draft: false
cover:
    image: "/blog/HTML5-CSS3/htmlcss.png"

---


## Introduction à Hugo :

Hugo, un générateur de sites Web statiques, se distingue par sa simplicité d'utilisation et ses performances exceptionnelles.Hugo crée des fichiers HTML statiques, adaptés à tout serveur web

## Installation de Hugo :

- Téléchargez le fichier d'installation Hugo pour Windows depuis le site officiel **(https://gohugo.io/getting-started/installing/#windows)**.

- Extrayez le contenu du fichier téléchargé.

- Copiez le fichier exécutable Hugo (hugo.exe) dans un répertoire accessible depuis la ligne de commande.

- Ajoutez le chemin du répertoire contenant Hugo à la variable d'environnement "PATH".

- Vérifiez l'installation en ouvrant une nouvelle fenêtre de commande et en exécutant la commande suivante : **hugo version**

## Création et Gestion de Contenu avec Hugo :

Le langage de balisage léger Markdown est au cœur de la création et de la gestion de contenu dans Hugo. Conçu pour permettre la rédaction de contenu formaté avec une syntaxe simple en texte brut, Markdown est utilisé par Hugo pour les articles de blog et les pages, convertissant ces fichiers en HTML lors de la construction du site.

- [ ] Titres : Utilisez # pour les titres, ## pour les sous-titres, etc.
- [ ] Paragraphes : Séparez les paragraphes par des lignes vides.
- [ ] Liens : Texte du lien.
- [ ] Images : ![Texte alternatif](URL de l’image).
- [ ] Listes : Utilisez - ou * pour les listes à puces, et des chiffres pour les listes ordonnées.
- [ ] Gras et Italique : gras, italique.


## Arborescence de Base d'un projet hugo :

**archetypes/** / : Contient des modèles de contenu prédéfinis pour faciliter la création de nouveaux contenus.

**content/** : C'est l'emplacement principal pour les fichiers de contenu au format Markdown.

**data/**  : Permet de stocker des fichiers de données, comme des fichiers JSON ou YAML, utilisés dans les modèles.

**layouts/**  : Contient les modèles utilisés pour générer les pages HTML du site.

**static/**  : Pour les fichiers statiques tels que les images, les fichiers CSS, et d'autres 

**ressources/** qui seront directement servies sans traitement par Hugo.

**themes/**  : Si un thème est utilisé, il est stocké dans ce répertoire.
Fichiers Clés :

**config.toml/** (ou config.yaml, config.json) : Fichier de configuration principal du site, où sont définies des options telles que le titre du site, la langue, et d'autres paramètres.
archetypes/default.md : Le modèle par défaut pour la création de nouveaux contenus.
Contenu :

Les fichiers Markdown dans le répertoire content/ contiennent le contenu principal du site, organisé en sections et pages.
Modèles :

Les fichiers dans layouts/ définissent la structure HTML du site. Hugo utilise la syntaxe de template Go pour générer les pages à partir du contenu Markdown.
Thèmes (optionnel) :

Si un thème est utilisé, il est stocké dans le répertoire themes/. Les thèmes peuvent contenir des fichiers de modèles, des fichiers statiques, et d'autres éléments pour définir l'apparence du site.

## Héberger un Site Hugo sur GitHub Page

**Construction du Site :**

Générez votre site en utilisant la commande Hugo : **hugo** a la racine de son projet.
Cela créera un répertoire **public/**  contenant les fichiers HTML générés

**Ajout et Validation des Changements :**

On se place sur dans le dossier **public/** et on initialise un depot git avec la commande **git init**

On creer une branche gh-pages avec git branch -M gh-pages.

On ajoute le dépôt GitHub comme remote (git remote add origin [URL du Dépôt GitHub]) et envoie 
 le contenu avec git push -u origin gh-pages.

 **Activation de GitHub Pages :**

 Accédez aux paramètres de votre dépôt sur GitHub.
Dans la section GitHub Pages, choisissez la branche (par exemple, master) comme source pour la publication de GitHub Pages. Mais si on a creer une branch gh-pages elle est choisir par github par defaut

**Accès à votre Site :**

Après quelques instants, votre site sera accessible à l'URL spécifiée dans les paramètres GitHub Pages, généralement sous la forme **<nom-d'utilisateur>.github.io/<nom-du-dépôt>.**