# AngularTest
Application Angular sur Github 🛡 Créer un nouveau projet Angular, et changer le titre avec ce format : Bienvenue sur le site de [ton nom] !. Tu dois le faire en gardant l'attribut "title". Tu dois ensuite pousser ton code sur un dépôt Github.




7
Manojan Sivasuthan
Logo Wild Code School

﻿ 00 - Démarrer avec Angular

Angular
3 pairs

﻿ 00 - Démarrer avec Angular



Introduction
Angular est un framework Javascript réalisé par Google qui simplifie le développement d'applications web. Comme la plupart des frameworks modernes (React, Vue.js...), il utilise le principe des composants. Dans cette quête, tu apprendras à :

✅ Créer un projet Angular simple
✅ Modifier le composant principal de ton application

Angular (https://angular.io/) ne doit pas être confondu avec AngularJS (https://angularjs.org/). AngularJS est la première itération du framework faite par Google, la version 1.x.
Angular a commencé avec la version 2.0, et est actuellement en version 14.1.0 (12 septembre 2022). C'est pourquoi Angular est aussi souvent appelé Angular2+.

Avant de démarrer, assure-toi d'avoir terminé les quêtes suivantes👇

🤓 À la fin de cette quête, tu seras capable de :
✅ Installer tous les outils nécessaires pour Angular
✅ Créer ton premier projet Angular
✅ Comprendre la structure d'un projet Angular

🛠 Installer les outils dont tu as besoin
Angular est livré avec un outil génial : le CLI ("commande line interface" ou interface en ligne de commande en français). Avec cet outil, tu peux créer des projets, générer du code automatiquement et bien d'autres choses utiles.

Pour l'installer, tu dois d'abord installer les éléments suivants sur ton ordinateur :

nodejs (une version récente)
npm
→ Détails de l'installation

Maintenant que tu as installé nodeJS et npm, tu peux installer Angular CLI. Tu dois l'installer globalement, ce qui signifie que tu peux l'utiliser depuis n'importe quel répertoire de ton ordinateur avec ton terminal (ce qui est ma foi fort pratique).

Pour installer un paquet globalement avec npm, tu dois ajouter le paramètre -g. Donc, pour installer le CLI Angular, tu dois faire :

npm install -g @angular/cli
Tout est maintenant prêt pour commencer à utiliser Angular ! 💃🏻

Angular QuickStart - Mettre en place l'environnement de développement
Page officielle du QuickStart Angular

https://angular.io/guide/quickstart#devenv
👶 Créer ton premier projet Angular
Créer un projet Angular est assez simple. Tout d'abord, tu dois décider où tu veux le créer, et naviguer vers ce dossier avec ton terminal. Par exemple, tu peux créer un dossier nommé Angular_Projects et ensuite naviguer à l'intérieur de celui-ci :

mkdir Angular_Projects
cd Angular_Projects/
Tu peux maintenant utiliser Angular CLI pour créer un projet et spécifier son nom :

ng permet d'appeler le CLI d'Angular
new demande au CLI de créer un nouveau projet Angular
myFirstApp est le nom que l'on choisit de donner à ce projet (par exemple)
ng new myFirstApp
Le CLI d'Angular va alors te poser quelques questions afin de générer le projet :

? Would you like to add Angular routing? (y/N) 
→ Cela te permet de créer les fichiers de base nécessaires à la navigation entre les pages de ton application. Tu peux accepter en entrant y puis la touche entrer de ton clavier. Tu verras dans la quête dédiée au routing que nous refuserons cette ligne : cela te contraindra à implémenter de toi-même les fichiers nécessaires au routing de ton application Angular. C'est une tâche fastidieuse, mais ça t'aidera à bien comprendre ce que le CLI d'Angular fait pour toi 😌

? Which stylesheet format would you like to use? (Use arrow keys)
❯ CSS 
  SCSS   [ https://sass-lang.com/documentation/syntax#scss                ] 
  Sass   [ https://sass-lang.com/documentation/syntax#the-indented-syntax ] 
  Less   [ http://lesscss.org  
→ Cela te permet de choisir le style tu souhaites utiliser pour tes feuilles de style. Ce choix n'est pas irrévocable mais la migration d'un style vers un autre peut s'avérer fastidieuse.

CSS vs SCSS (Grafikart)
https://grafikart.fr/tutoriels/differences-sass-scss-329
Sass : documentation officielle
https://sass-lang.com/
Less : documentation officielle
https://lesscss.org/
✅La création du projet se lance alors. Elle peut prendre un petit peu de temps : Angular installe tous les éléments dont tu auras besoin pour faire fonctionner le framework.
Une fois l'installation terminée, tu peux naviguer vers ton dossier de projet :

cd myFirstApp
Tu peux ensuite ouvrir ce dossier avec éditeur éditeur de code préféré. Visual Studio Code est un très bon choix.

Angular QuickStart - Créer un nouveau projet
Page officielle du QuickStart Angular

https://angular.io/guide/quickstart#create-proj
🏗 Structure du projet
Commençons par quelques définitions de base des termes propres à Angular :

Module : Tu peux simplement voir un module comme une boîte qui contiendra tous tes composants. La plupart du temps, un seul module est suffisant pour une petite application. Tu n'auras donc pas besoin de créer d'autres modules. Lorsque tu utilises des bibliothèques, tu utilise parfois des modules qui ont été créés par d'autres personnes.
Composant : Tu peux voir un composant comme un très petit élément d'un site web composé de code HTML, CSS et Typescript. Un composant est dédié à une seule fonction particulière à l'intérieur de ton site web. Tu auras besoin de plusieurs composants à l'intérieur de ton projet.
L'utilisation de composants rend ton code plus simple et plus facile à travailler, parce que tu as des petits fichiers qui sont faciles à comprendre.
En d'autres termes, un Module est comme un carton dans lequel sont rangés plusieurs petits cartons (composants).

Si c'est encore flou, pas d'inquiétudes. La prochaine quête détaille le principe et le fonctionnement des composants 🤓

Voici la structure d'un nouveau projet Angular :

image

Bon, ça fait pas mal de choses ! Essayons de les détailler un petit peu :

Le fichier package.json contient la liste de toutes les dépendances du projet. Si tu veux ajouter une bibliothèque à ton projet, tu dois l'installer avec la commande suivante : npm install libraryName --save. Grâce au paramètre --save, la bibliothèque sera ajoutée au fichier package.json. Ensuite, lorsque tu clones ton projet, ou que tu récupères le travail d'un collègue, tu peux lancer npm install pour installer toutes les dépendances listées dans ce fichier. Tu remarqueras aussi que dans le fichier package.json se trouve un objet devDependencies. A l'intérieur sont listées toutes les dépendances de ton projet que tu ne souhaites utiliser qu'en contexte de développement et non de production.
Le dossier src contiendra tout le code du projet Angular. C'est là où tu passeras le plus clair de ton temps 👀
Le dossier app est ton dossier contenant les modules. Lorsque tu crées un projet Angular, un module par défaut nommé app est créé.
Le fichier app.module.ts est en quelque sorte un peu le patron du module app 😎. Il dit à Angular comment construire et lancer l'application dans le module app.
Parfois, lorsque tu veux utiliser une bibliothèque, en plus de l'installer avec npm, ils te sera demandé d'ajouter des modules à l'intérieur de ce fichier. Tu devras également lister l'ensemble de tes services dans ce fichier. (La notion de service et leur implémentation te sera expliqué dans une quête ultérieure).
Déclarer des éléments dans le fichier de configuration app.module.ts te permet de rendre ces derniers visibles, accessibles et donc utilisables au sein de ton module. Tu l'expérimenteras très vite dans une prochaine quête 😌
Le fichier app-routing.module.ts permet de charger et de configurer le router de ton module app.
Le fichier app.component.ts contient le code Typescript du composant app généré par défaut. Il contient une classe nommée AppComponent.
Attention à ne pas confondre : lorsque tu crées ton projet Angular, le premier module par défaut est créé : c'est le module app. À l'intérieur de celui-ci, le premier composant par défaut est également créé : c'est le composant app.

Le fichier app.component.html contient le HTML du composant app de ton projet
Le fichier app.component.css contient le code CSS qui sera appliqué uniquement à ce composant.
Le dossier assets contiendra des fichiers comme des images, des polices, des fichiers pdf, etc...
Tu dois absolument et uniquement placer tes images, polices, PDFs... dans le dossier assets.

Le fichier index.html contiendra la structure HTML de base de ton site web. Si tu souhaites ajouter une "métadonnée" ou d'autres éléments dans la balise "head", tu dois le faire dans ce fichier. Mais nous ne coderons rien dans ce fichier, tout sera fait à l'intérieur des composants.

Le fichier styles.css contiendra le code CSS qui affecte tout le site web. C'est le CSS global en d'autres termes.

Si tu définis un CSS global dans le styles.css mais que tu souhaites re-définir ce CSS localement à l'intérieur d'un composant, tu peux le faire ! Il te suffit d'écrire ton CSS dans la partie CSS de ton composant. Cela écrira par-dessus le CSS global pour ce composant.

Structure de projet Angular
Documentation officielle d'Angular pour mieux comprendre la structure d'un projet

https://angular.io/guide/file-structure
🧠 Gérer le projet
Pour exécuter le projet, il te suffit d'ouvrir un terminal, de te rendre dans le dossier du projet et de lancer la commande suivante :

 ng serve -o
Si tu es sous Windows, il est possible que tu aies une erreur du type Impossible de charger le fichier C:\Users\....\ng.ps1, car l’exécution de scripts est désactivée sur ce système.... Jettes un œil à cette ressource, tu y trouveras la solution : https://www.windows8facile.fr/powershell-execution-de-scripts-est-desactivee-activer/
À noter que cette ressource est dans les premiers résultats Google après avoir copié-collé l'erreur reportée ci-dessus...

Cette commande va transpiler le code Typescript, construire l'application Angular et lancer le serveur en local sur le port 4200. Grâce au paramètre -o, il ouvrira automatiquement le navigateur à cette page : http://localhost:4200/

Après quelques microsecondes d'attente, tu pourras voir un protoype de page web comme celle ci :



Et "Voilà" ! 🎉 🎉

Félicitations, tu as devant tes yeux ébahis la première page de ta toute première application Angular !

Bon, ça fait quand même un peu vaudou, non ?

Tentons de comprendre comment Angular parvient à afficher ce résultat. Pour commencer, tu peux ouvrir les fichiers suivants :

src/index.html
src/app/app.component.html
src/app/app.component.ts
Regarde dans le fichier index.html, il y a cette balise : <app-root></app-root>. Si tu vérifies le début du fichier app.component.ts, tu verras que le sélecteur de ce composant est app-root. Cela signifie que nous pouvons afficher un composant juste en faisant appel à sa balise correspondante.

Pour information, le serveur a une fonction de rechargement en direct, ce qui signifie que si tu fais une modification au code, Angular va reconstruire ton projet et rafraîchir automatiquement la page web dans ton navigateur.

Tu peux par exemple essayer de modifier la valeur de l'attribut title dans src/app/app.component.ts et sauvegarder le fichier. Tu peux voir que la modification apparait automatiquement dans ton navigateur.

Enfin, si tu ouvres src/app/app.component.html, et que tu cherches une occurence de {{ title }}, tu tomberas nez à nez avec le texte qui s'affiche sur la page de ton application. Modifie le fichier, sauvegarde et constates sur ton navigateur que l'affichage s'est mis à jour de lui même.

Ça fait beaucoup d'informations ! Ne t'inquiètes pas, à force de travailler sur Angular, tu prendras vite les réflexes et tu comprendras petit à petit toutes les subtilités du framework.

💪 Challenge
Application Angular sur Github 🛡
Créer un nouveau projet Angular, et changer le titre avec ce format : Bienvenue sur le site de [ton nom] !. Tu dois le faire en gardant l'attribut "title". Tu dois ensuite pousser ton code sur un dépôt Github.

Critères de validation ✅
Le code doit être sur Github
Les fichiers doivent être à la racine du dépôt (et non dans un dossier)
Le titre doit avoir été modifié
Solution postée le mercredi 13 décembre 2023

https://github.com/mjcode6/AngularTest/tree/master
