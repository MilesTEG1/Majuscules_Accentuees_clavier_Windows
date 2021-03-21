Avoir les Majuscules Accentuées sur un clavier français sous Windows (10) <!-- omit in toc -->
============

L'objectif de ce qui suit est d'avoir les majuscules accentuées suivantes **[ É È Ç À Ù ]** avec la touche "**Verr.Maj**" + une des lettre **[ é è ç à ù ]** du clavier français sous windows (comme sur un mac).

## Table of Contents <!-- omit in toc -->

- [1. Introduction](#1-introduction)
- [2. Préparation et configuration du clavier personnalisé](#2-préparation-et-configuration-du-clavier-personnalisé)
  - [2.1. Installation du logiciel Microsoft Keyboard Layout Creator](#21-installation-du-logiciel-microsoft-keyboard-layout-creator)
  - [2.2. Importation du clavier Apple déjà présent](#22-importation-du-clavier-apple-déjà-présent)
  - [2.3. Modification du layout du clavier importé](#23-modification-du-layout-du-clavier-importé)
  - [2.3. Sauvegarde du layout du clavier personnalisé](#23-sauvegarde-du-layout-du-clavier-personnalisé)
  - [2.4. Installation du layout du clavier personnalisé](#24-installation-du-layout-du-clavier-personnalisé)
  - [3. Fin](#3-fin)
- [4. Addendum - Réaffectation de touches avec SharpKeys](#4-addendum---réaffectation-de-touches-avec-sharpkeys)

# 1. Introduction

J'aime bien avoir des fonctionnement similaire sur mon pc windows et sur mon mac, le problème des majuscules accentuées sous windows qui ne sont pas faisable directement au clavier, comme sur un MAC...

J'ai réussi à faire en sorte que ça fonctionne, et je pense que ça pourrait servir à certains.

Comme j'utilisais un clavier Apple filaire MB110F (avec pavé numérique) sous windows, j'ai du installer les pilotes du clavier apple avec BootCamp. Tout fonctionnait bien pendant plusieurs années, sauf les Majuscules Accentuées... Je n'ai jamais pris le temps de chercher une solution...
Mais comme j'ai récemment acheté un [Logitech MX Keys for Mac](https://www.logitech.fr/fr-fr/products/keyboards/mx-keys-mac-wireless-keyboard.html?crid=27) (car je préfère le layout des claviers mac à celui des PC, et j'utilise depuis longtemps un clavier apple avec windows, en parallèle d'un Macbook Air), j'ai du corriger un soucis d'affectation de touches (la touche @ et > sont interverties quand on les frappe...: voir photo ci-dessous)

[<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/touches-interverties.png" width="100" />](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/touches-interverties.png)


Pour le nouveau clavier Logitech, j'ai installé le [logiciel Option](https://support.logi.com/hc/fr/articles/360051303433-Download-Stub-MX-Keys-for-Mac), il faut que le clavier soit reconnu par l'application
Il se peut donc que la partie [2.1.](#21-importation-du-clavier-apple-déjà-présent) ne soit pas possible pour vous...

[<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Logiciel-Option.png" heigh="100" align="center" />](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Logiciel-Option.png)

_(Mon clavier est bien un AZERTY FR, mais la photo dans l'application Option (que ce soit sous windows ou wous macOS) est un clavier QWERTY... chercher l'erreur..._ :sweat_smile:_)_

# 2. Préparation et configuration du clavier personnalisé

## 2.1. Installation du logiciel Microsoft Keyboard Layout Creator

J'ai utilisé [Microsoft Keyboard Layout Creator](https://www.microsoft.com/en-us/download/details.aspx?id=102134) pour modifier le layout Apple que j'avais installé (à l'époque où j'ai connecté mon clavier apple filaire). Il faudra bien entendu installer cette application.

[<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Microsoft_Keyboard_Layout_Creator.png" heigh="100" align="center" />](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/Microsoft_Keyboard_Layout_Creator.png)


## 2.2. Importation du clavier Apple déjà présent

<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/01.png" align="right" />
<br/><br/><br/>

* Il faut maintenant importer le layout Apple (que j'ai d'installé parce que j'ai installé le pilote du clavier Apple filaire avec BootCamp).  
<br/> <br/> <br/><br/><br/><br/>

<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/02.png" align="right" />

<br/><br/><br/><br/><br/>

* C'est le premier des deux qui apparaissent dans ma liste, le second ne veut pas se sélectionner...<br/><br/>
  _Pour modifier un clavier AZERTY windows classique, choisissez le clavier Français dans la liste :_
  ![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/18.png)

## 2.3. Modification du layout du clavier importé

<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/03.png" align="right" />

* Ensuite, il faut modifier les touches voulues, en cochant cette case-à-cocher à gauche du layout qui s'est affiché :<br/>

<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/04.png" align="right" />

* Par exemple sur la touche 3, ça donne ça si aucune personnalisation n'est faite : <br/> <br/>

* Il faut cliquer sur All... pour avoir la liste suivante où on place le code unicode du caractère à avoir dans **``SGCAPS+<Key>``**, comme avec la touche ``2/é/É`` : <br/>
![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/05.png)
<br/>_(J'ai cherché les code unicode des lettres que je voulais ici : [https://www.compart.com/en/unicode/U+00C9](https://www.compart.com/en/unicode/U+00C9))_

  * Il faut décocher la case **`caps = shift`**, sinon la personnalisation ne fonctionnera pas.

* Il faut ensuite répéter ça pour chacune des touches voulues, et on obtiendra ceci :
![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/06.png)<br/>
J'ai donc décoché la case **`caps = shift`** pour les touches à droites et à gauche des lettres (donc pour ``< ^ $ ` = : ; ,`` ) mais pas pour les touches sur la même lignes que les n° ou ``é è ç à``. Je n'en ai pas l'utilisé, mais on peut le faire car sur MAC c'est désactivé.

* J'ai aussi ajouté quelques mappages avec la touche option/ALTGR qui n'étaient pas présente dans le logiciel, mais qui étaient présentes avec le layout apple d'origine (après coup, je pense que ces caractères sont faits dans word que j'ai utilisé pour faire mes tests...) : il s'agit de ``® ™ ©`` car les autres sont déjà là.
![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/07.png)<br/>
(bon pour cette partie, on est un peu différent de ce qu'il se passe sur macos)

## 2.3. Sauvegarde du layout du clavier personnalisé

* Il faut choisir un nom pour le layout :<br />
![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/08.png)<br/>
_Attention, ici c'est pénible, car le nom ne doit pas faire plus de 8 caractères... un vieil héritage des premiers windows/dos peut-être..._
<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/09.png" align="right" />


* Et après, on construit les DLL et le paquet d'installation :<br />
  Ça me crée des fichiers d'installation et des DLL :

  ![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/10.png) ![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/11.png)<br/>

## 2.4. Installation du layout du clavier personnalisé


* Reste plus qu'a lancer le setup.exe pour installer le layout créé.

* On peut enfin choisir le clavier revisité. Pour celà, il faut aller dans **Paramètres** --> **Heure et langue** --> **Langue** --> **Langue** --> cliquer sur Français, puis sur Options :<br/>
![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/12.png)<br/>
(J'appelle cette capture _**LANGUE-CLAVIER**_, je vais en avoir re-besoin plus bas).

* Puis, si le clavier custom n'est pas dans la liste tout en bas, cliquer sur ajouter un clavier, et choisissez dans la liste le clavier French - Apple - Custom :<br/>
  ![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/13.png)

  On pourrait supprimer l'ancien Apple (si vous en avez un) :<br/>
  ![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/15.png)<br/>
  Mais je préfère le garder au cas-où...

<img src="https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/16.png" align="right" />

* Si comme moi vous avez plusieurs clavier dans la liste des claviers ajoutés, revenez un écran avant, et (capture _**LANGUE-CLAVIER**_) cliquer sur :<br/>

* Puis sélectionner le clavier custom dans la liste entourée en rouge :<br/>
  ![](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Screenshots/17.png)<br/>

## 3. Fin

Voilà, vous avez maintenant la possibilité de faire les lettres ``É È À Ç Ù``  avec la touche **``CAPS-LOCK``** sous windows, comme sur un vrai mac.

Pour ceux qui ne veulent pas faire toutes les étapes de paramétrages, j'ai mis sur ce dépôt GitHub le fichier [**``Apple FR - Custom - v2.klc``**](https://raw.githubusercontent.com/MilesTEG1/Majuscules_Accentuees_clavier_Windows/main/Apple%20FR%20-%20Custom%20-%20v2.klc) que j'ai créé.

Vous trouverez aussi dans le dossier build une archive qui contient les fichiers d'installation créés à l'étape 2.3.

Voilà, j'espère que tout ceci vous aura été utile :smiley:.




# 4. Addendum - Réaffectation de touches avec SharpKeys

Pour cela, je vous invite à aller voir cet autre tuto : [https://github.com/MilesTEG1/Logitech-MX-Keys-for-mac--avec-Windows](https://github.com/MilesTEG1/Logitech-MX-Keys-for-mac--avec-Windows)