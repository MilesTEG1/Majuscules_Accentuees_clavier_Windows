Avoir les Majuscules Accentuées sur un clavier français sous Windows (10) <!-- omit in toc -->
============

L'objectif de ce qui suit est d'avoir les majuscules accentuées suivantes **[ É È Ç À Ù ]** avec la touche "**Verr.Maj**" + une des lettre **[ é è ç à ù ]** du clavier français sous windows (comme sur un mac).

## Table of Contents <!-- omit in toc -->

- [1. Introduction](#1-introduction)
- [2. Préparation et configuration du clavier personnalisé](#2-préparation-et-configuration-du-clavier-personnalisé)
  - [2.1. Installation du logiciel Microsoft Keyboard Layout Creator](#21-installation-du-logiciel-microsoft-keyboard-layout-creator)
  - [2.2. Importation du clavier Apple déjà présent](#22-importation-du-clavier-apple-déjà-présent)

# 1. Introduction

J'aime bien avoir des fonctionnement similaire sur mon pc windows et sur mon mac, le problème des majuscules accentuées sous windows qui ne sont pas faisable directement au clavier, comme sur un MAC...

J'ai réussi à faire en sorte que ça fonctionne, et je pense que ça pourrait servir à certains.

Comme j'utilisais un clavier Apple filaire MB110F (avec pavé numérique) sous windows, j'ai du installer les pilotes du clavier apple avec BootCamp. Tout fonctionnait bien pendant plusieurs années, sauf les Majuscules Accentuées... Je n'ai jamais pris le temps de chercher une solution...
Mais comme j'ai récemment acheté un [Logitech MX Keys for Mac](https://www.logitech.fr/fr-fr/products/keyboards/mx-keys-mac-wireless-keyboard.html?crid=27) (car je préfère le layout des claviers mac à celui des PC, et j'utilise depuis longtemps un clavier apple avec windows, en parallèle d'un Macbook Air), j'ai du corriger un soucis d'affectation de touches (la touche @ et > sont interverties quand on les frappe...: voir photo ci-dessous)

[<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/touches-interverties.png" width="100" />](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/touches-interverties.png)


Pour le nouveau clavier Logitech, j'ai installé le [logiciel Option](https://support.logi.com/hc/fr/articles/360051303433-Download-Stub-MX-Keys-for-Mac), il faut que le clavier soit reconnu par l'application
Il se peut donc que la partie [2.1.](#21-importation-du-clavier-apple-déjà-présent) ne soit pas possible pour vous...
[<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Logiciel-Option.png" heigh="100" />](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Logiciel-Option.png)
_(Mon clavier est bien un AZERTY FR, mais la photo dans l'application Option (que ce soit sous windows ou wous macOS) est un clavier QWERTY... chercher l'erreur..._ :sweat_smile:_)_

# 2. Préparation et configuration du clavier personnalisé

## 2.1. Installation du logiciel Microsoft Keyboard Layout Creator

J'ai utilisé [Microsoft Keyboard Layout Creator](https://www.microsoft.com/en-us/download/details.aspx?id=102134) pour modifier le layout Apple que j'avais installé (à l'époque où j'ai connecté mon clavier apple filaire). Il faudra bien entendu installer cette application.
[<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Microsoft_Keyboard_Layout_Creator.png" heigh="100" />](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Microsoft_Keyboard_Layout_Creator.png)


## 2.2. Importation du clavier Apple déjà présent

Il faut maintenant importer le layout Apple (que j'ai d'installé parce que j'ai installé le pilote du clavier Apple filaire avec BootCamp).

![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/01.png)

C'est le premier des deux qui apparaissent dans ma liste, le second ne veut pas se sélectionner...



Ensuite, il faut modifier les touches voulues, en cochant  à gauche du layout qui s'est affiché.
Par exemple sur la touche 3, ça donne ça si aucune personnalisation n'est faite :


Il faut cliquer sur All... pour avoir la liste suivante où on place le code unicode du caractère à avoir dans "SGCAPS+<Key>", comme avec la touche 2/é/É :

( J'ai cherché les code unicode des lettres que je voulais ici : https://www.compart.com/en/unicode/U+00C9 )



Il faut décocher la case "caps = shift", sinon la personnalisation ne fonctionnera pas.



Il faut ensuite répéter ça pour chacune des touches voulues, et on obtiendra ceci :

(j'ai décoché la case "caps = shift" pour les touches à droites et à gauche des lettres (donc pour < ^ $ ` = : ; , ) mais pas pour les touches sur la même lignes que les n° ou é è ç à. Je n'en ai pas l'utilisé, mais on peut le faire car sur MAC c'est désactivé.





J'ai aussi ajouté quelques mappages avec la touche option/ALTGR qui n'étaient pas présente dans le logiciel, mais qui étaient présentes avec le layout apple d'origine (après coup, je pense que ces caractères sont faits dans word que j'ai utilisé pour faire mes tests...) : il s'agit de ®™© car les autres sont déjà là.

(bon pour cette partie, on est un peu différent de ce qu'il se passe sur macos)


Je choisi un nom pour le layout :

Attention, ici c'est relou, car le nom ne doit pas faire plus de 8 caractères... un vieil héritage des premiers windows/dos peut-être...


Et après, on construit les DLL et le paquet d'installation :


Ca me crée des fichiers d'installation et des DLL :


Reste plus qu'a lancer le setup.exe, et on peut enfin choisir le clavier revisité.
Pour celà, il faut aller dans Paramètres --> Heure et langue --> Langue --> Langue --> cliquer sur Français, puis sur Options :



(J'appelle cette capture LANGUE-CLAVIER, je vais en avoir re-besoin plus bas).



Puis, si le clavier custom n'est pas dans la liste tout en bas, cliquer sur ajouter un clavier, et choisissez dans la liste le clavier French - Apple - Custom :





On pourrait supprimer l'ancien Apple (si vous en avez un) :



Mais je préfère le garder au cas-où...

Si comme moi vous avez plusieurs clavier dans la liste des claviers ajoutés, revenez un écran avant, et (capture LANGUE-CLAVIER) cliquer sur 

Puis sélectionner le clavier custom dans la liste entourée en rouge :





Voilà, vous avez la possibilité de faire les lettres ÉÈÀÇÙ  avec la touche CAPS-LOCK sous windows, comme sur un vrai mac.


Pour ceux qui ne veulent pas faire toutes les étapes de paramétrages, j'ai envoyé sur GitHub le fichier Apple FR - Custom - v2.klc que j'ai créé.

https://github.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows



Demain je ferais un readme car le copier coller de ce message ne fonctionnera probablement pas...
