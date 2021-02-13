# Majuscules_Accentuees_clavier_Windows
Pour avoir des majuscules accentuées via la touche Caps-Lock du clavier avec windows (comme sur un mac)


Comme j'aime bien avoir des fonctionnement similaire sur mon pc windows et sur mon mac, il restait le problème des majuscules accentuées sous windows qui ne sont pas faisable directement au clavier, comme sur un MAC...

J'ai réussi à les avoir, et je pense que ça pourrait servir à certains (vu que ce n'est pas lié au MX Keys).


Donc j'ai trouvé pour avoir le comportement de macOS sur les lettres accentuées en majuscules :)
J'ai utilisé MS Keyboard Layout Creator pour modifier/créer le layout Apple que j'avais installé (à l'époque où j'ai connecté mon clavier apple filaire).
Donc pour avoir les majuscules accentuées avec la touche "Verr.Maj" + une des lettre [é è ç à ù], j'ai importé le layout Apple.  : 

 

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
