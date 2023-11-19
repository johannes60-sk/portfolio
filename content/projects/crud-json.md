---
title: "Projet Gestionnaire de Fichiers JSON avec API Node.js et Interface React.js"
description: "Ce projet a pour but d’apporter une solution a un problème interne a l'entreprise dans laquelle j'ai effectuer mon stage en simplifiant le processus d'ajout de flux vidéo pour les tests sur une plateforme en ligne"
dateString: Mars 2023 
draft: false
tags: ["JavaScript", "ReactJS", "Trello", "GitHub", "NodeJS", "ExpressJS"]
weight: 201
cover:
    image: "/projects/crud-json/addNewJson.png"
---

## Intro
Ce projet a pour but d’apporter une solution a un problème interne en **simplifiant le processus d'ajout de flux vidéo pour les tests sur une plateforme en ligne**. En effet, lorsque l’on avait besoin de tester un nouveau flux vidéo sur la plateforme, il fallait faire une demande à la personne chargée d’ajouter le JSON  contenant le nouveau  flux vidéo sur le serveur ftp afin de le rentre ensuite disponible sur la plateforme de test. L’interface de gestion de fichier JSON  réalisée en reactjs permettra à toute personne lambda  de créer, modifier et supprimer facilement les fichiers JSON contenant les liens des flux vidéo. Et grâce à une api connectée à cette interface le fichier JSON créé est directement envoyé sur le serveur ftp le rendant ainsi disponibles immédiatement sur la plateforme de test. 

## Presentation des interfaces

 **Page d'inscription** 

Afin de pouvoir utiliser la plateforme on est invités à créer un compte et à s'y connecter. Pour stocker les données des utilisateur, j’ai eu a créer une base de donné
NoSQL sur firebase.
Concernant les problème de sécurité lors de l'inscription et  d’authentification à la plateforme, firebase dispose de fonction que j’ai eu à implémenter et adapté pour l'inscription et la connexion de l’utilisateur


<!-- ![](/projects/crud-json/register.png) ![](/projects/crud-json/register_function.png) -->
<div style="display: flex; justify-content: space-between;">
    <img src="/projects/crud-json/register.png" id="register_img" alt="Image 1" width="100%">
    <img src="/projects/crud-json/register_function.png" id="register_function_img" style="display: none;" alt="Image 2" width="100%">
</div>

<script>
    document.getElementById('register_img').addEventListener('mouseover', (e) => {
        e.target.style.display='none'
        document.getElementById('register_function_img').style.display='block'
    })

     document.getElementById('register_img').addEventListener('mouseleave', (e) => {
        e.target.style.display='block'
        document.getElementById('register_function_img').style.display='none'
     })

</script>


**Page de création d’un fichier JSON**

Sur cette page l’utilisateur désirant créer son fichier json est invité à renseigner les informations nécessaires(nom du fichier json, nom du flux,l’url du flux vidéo et l’id) . L'utilisateur a la possibilité d’ajouter dans son fichier JSON autant de flux vidéo qu’il souhaite et une fois terminé il fait la validation qui lance ensuite la création de son fichier JSON



<div style="display: flex; justify-content: space-between;">
    <img src="/projects/crud-json/addNewJson.png" id="addNewJson" alt="Image 1" width="100%">
    <img src="/projects/crud-json/requete_create_json.png" id="requete_create_json" style="display: none;" alt="Image 2" width="70%" height="50%">
</div>

<script>
    document.getElementById('addNewJson').addEventListener('mouseover', (e) => {
        e.target.style.display='none'
        document.getElementById('requete_create_json').style.display='block'
    })

     document.getElementById('addNewJson').addEventListener('mouseleave', (e) => {
        e.target.style.display='block'
        document.getElementById('requete_create_json').style.display='none'
     })

</script>

**Edition ou suppression d’un fichier JSON**

Sur cette page l’utilisateur pourra voir dans la liste déroulante  les fichiers json disponibles sur le serveur ftp. Il pourra donc choisir le fichier qu’il souhaite modifier ou supprimer . Lorsque l’utilisateur choisit son fichier, un éditeur JSON s’ouvre automatiquement et charge le contenu du fichier. L’utilisateur pourra donc interagir directement dans l'éditeur et faire ces modifications. 

<div style="display: flex; justify-content: space-between;">
    <img src="/projects/crud-json/edit.png" id="edit" alt="Image 1" width="100%">
    <img src="/projects/crud-json/route_edit.png" id="route_edit" style="display: none;" alt="Image 2" width="70%" height="50%">
</div>

<script>
    document.getElementById('edit').addEventListener('mouseover', (e) => {
        e.target.style.display='none'
        document.getElementById('route_edit').style.display='block'
    })

     document.getElementById('edit').addEventListener('mouseleave', (e) => {
        e.target.style.display='block'
        document.getElementById('route_edit').style.display='none'
     })

</script>


**suppression d’un fichier JSON**

Sur cette page l’utilisateur pourra voir dans la liste déroulante  les fichiers json disponibles sur le serveur ftp. Il pourra donc choisir le fichier qu’il souhaite modifier ou supprimer . Lorsque l’utilisateur choisit son fichier, un éditeur JSON s’ouvre automatiquement et charge le contenu du fichier. L’utilisateur pourra donc interagir directement dans l'éditeur et faire ces modifications. 


<div style="display: flex; justify-content: space-between;">
    <img src="/projects/crud-json/confirm_delete.png" id="confirm_delete" alt="Image 1" width="100%">
    <img src="/projects/crud-json/route_delete.png" id="route_delete" style="display: none;" alt="Image 2" width="70%" height="50%">
</div>

<script>
    document.getElementById('confirm_delete').addEventListener('mouseover', (e) => {
        e.target.style.display='none'
        document.getElementById('route_delete').style.display='block'
    })

     document.getElementById('confirm_delete').addEventListener('mouseleave', (e) => {
        e.target.style.display='block'
        document.getElementById('route_delete').style.display='none'
     })

</script>



## Resources
- [Depot Git du projet](https://github.com/johannes60-sk/stream-easy)
