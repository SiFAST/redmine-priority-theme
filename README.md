## Thèmes
Redmine fournit un support de base pour les thèmes.
Les thèmes Redmine peuvent uniquement remplacer les feuilles de style (comme application.css).

## Installation d'un thème
1. Tout d'abord, copiez le répertoire-thème dans '''/public/themes/'''. Cela résulterait en un chemin d'accès au répertoire application.css comme : '''/public/themes/<themename>/stylesheets/application.css'''
2. Vous devrez peut-être redémarrer Redmine afin qu'il affiche le thème nouvellement installé dans la liste des thèmes disponibles
3. Allez dans "Administration" -> "Paramètres" -> "Affichage" et sélectionnez votre thème nouvellement créé dans la liste déroulante "Thème". Enregistrez vos paramètres.

## Création de thèmes personnalisés

### Création d'un nouveau thème
Créer un répertoire dans le dossier '''public/themes'''. Le nom du répertoire sera utilisé comme nom de thème.
```
Exemple:
 public/themes/my_theme
Créez votre application.css personnalisée et enregistrez-la dans un sous-répertoire nommé stylesheets:
 public/themes/my_theme/stylesheets/application.css
Voici un exemple de feuille de style personnalisé qui ne remplace que quelques paramètres:
 /* Charger la feuille de style Redmine par défaut */
 @import url(../../../stylesheets/application.css);
 /* Ajouter un logo dans l'en-tête */
 #header {
    background: #507AAA url(../images/logo.png) no-repeat 2px;
    padding-left: 86px;
 }
 /* Déplacer le menu du projet vers la droite */
 #main-menu { 
    left: auto;
    right: 0px;
 }
Cet exemple suppose que vous avez une image my_theme/images/logo.png.
Vous pouvez télécharger cet exemple de thème comme point de départ de votre propre thème. Extrayez-le dans le répertoire '''public/themes'''.
```

### Ajout d'un javascript personnalisé
Il suffit de mettre votre javascript dans '''javascripts/theme.js''' et il sera automatiquement chargé sur chaque page (Redmine >= 1.1.0 uniquement).

### Appliquer le thème
Allez dans "Administration -> Paramètres" et sélectionnez votre thème nouvellement créé dans la liste déroulante "Thème". Enregistrez vos paramètres.
Si vous utilisez une version Redmine inférieure à 1.1.0, vous devrez peut-être redémarrer l'application afin qu'elle s'affiche dans la liste des thèmes disponibles.

## Thème Sifast 
Le thème spécifique SiFAST est déposé sur GitHub : [https://github.com/SiFAST/redmine-priority-theme GitHub]

Ce thème spécifique SiFAST est basé sur le thème par défaut de Redmine qu'on a pris comme point de départ, ensuite on y a ajouté le changement de couleur du numéro de ticket en fonction de la priorité du ticket.

## Imprimer ecran Thème Sifast


## Liens utiles
* http://www.redmine.org/projects/redmine/wiki/Theme_List
* http://www.redmine.org/projects/redmine/wiki/HowTo_create_a_custom_Redmine_theme

