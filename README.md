# Knowledge should be free

> Code source pour le site web
[knowledgeshouldbefree.org](https://knowledgeshouldbefree.org).

Ce site web héberge des polycopiés et exercices de mathématiques, de licence ou
master, dont la qualité est jugée exceptionnelle. Il est aussi un hommage à
Alain Kraus, mathématicien et enseignant-chercheur à Sorbonne Université de
1991 à 2022, dont les cours ont marqué plusieurs génération d'étudiantes et
étudiants. Nous attirons en particulier l'attention sur le [cours de
cryptographie](https://knowledgeshouldbefree.org/cours/crypto-2021-m1/), et
[celui sur les corps
locaux](https://knowledgeshouldbefree.org/cours/corps_locaux-2000-m2/). Plus
généralement, notre démarche s'inscrit dans une vision universitaire de partage
des connaissances, basée sur l'exigence de qualité et la rigueur.

## Table des matières

* [Knowledge should be free](#knowledge-should-be-free)
   * [Objectifs futurs](#objectifs-futurs)
   * [Hébergement et confidentialité](#hébergement-et-confidentialité)
   * [Pour les développeurs et développeuses](#pour-les-développeurs-et-développeuses)

<!-- Created by https://github.com/ekalinin/github-markdown-toc -->

## Objectifs futurs

Le site est minimaliste. Si la forme doit le rester, nous suggérons quelques
améliorations possibles.

Sur le fond :

- Ajout de matériels de cours d'autres professeurs et professeures. À long
terme, cela pourra prendre la forme d'un forum où étudiants et professeurs
pourront proposer de nouveaux ajouts, et en discuter (éventuellement sous
pseudonyme). Un système de vote, dont les modalités sont encore à définir,
pourra être mis en place. Grâce à leur expérience, des professeurs pourraient
aussi écrire des *reviews* de matériels déjà hébergés. Toutefois, pour que de
tels changements soient mis en place, le site internet devra être établi comme
outil utile d'une communauté active — pour l'heure, la pertinence du projet au
delà d'un hommage à un professeur est encore à prouver.
- Ajout d'une barre de recherche, et de *tags* (disciplines, années scolaires,
niveau, auteurs, etc). D'un point de vue technique, cela doit être possible en
n'utilisant que des fonctionnalités natives d'Hugo.
- Une meilleure présentation du téléchargement. Pour l'instant, le bouton
`Télécharger le cours` renvoie vers un `.zip`. Il serait plus utile et pratique
de renvoyer vers une nouvelle page qui présente l'arborescence de chaque
fichier en arbre (comme le programme `tree`). L'utilisateur ou utilisatrice
pourrait voir précisément le contenu des archives, et décider de ne télécharger
qu'un fichier, ou toute l'archive.
- Un système de versionnage précis. Cela commande de fixer une convention sur
le nommage des url.
- Comme sur Wikipédia, des instances dans d'autres langues. Nous n'hébergeons
que du matériel en langue française, mais il est envisageable de créer des
sous-domaines comme `fr.knowledgeshouldbegree.org` ou
`en.knowledgeshouldbegree.org`. Cela ne peut se faire qu'avec le soutien d'une
communauté active.

Sur la forme :
- Un mode sombre.
- Faire renvoyer [cours/](https://knowledgeshouldbefree.org/cours/) à la page
d'accueil.

## Hébergement et confidentialité

Le site est pour l'instant hébergé par l'hébergeur islandais
[1984.hosting](https://1984.hosting/), choisi pour sa bonne réputation en
matière de confidentialité et respect des données, ainsi que sa simplicité. Le
nom de domaine est loué par l'intermédiaire de [Njalla](https://njal.la/). Le
coût annuel de ces deux services est de respectivement 35,40 USD et 15 €, soit
environ 48,80 €.

Ayant conscience de l'importance primordiale de la protection des données de
nos étudiantes et étudiants, nous aimerions à terme faire héberger le site par
une institution académique française. Toute proposition en accord avec les
valeurs dont ce site se réclame sera étudiée sérieusement.

Aucune collecte de la moindre donnée n'est nécessaire, et ne sera effectuée. En
particulier, aucun mécanisme de collecte ne sera utilisé ou implémenté.

## Pour les développeurs et développeuses

Le site est *statique*. En particulier, il n'est bâti qu'avec HTML et ~~CSS~~
SASS, et sans JS. Pour limiter la redondance de code, nous utilisons
[Hugo](https://gohugo.io/), un [*générateur de sites
statiques*](https://jamstack.org/generators/). Cela permet de définir un unique
*template* HTML pour les pages de cours, et d'écrire le contenu des pages web
en Markdown. C'est bien plus digeste.

Il y a donc une phase de compilation (*build*) pour pouvoir visualiser le site.
Il faut donc installer Hugo, ainsi que [Dart
Sass](https://gohugo.io/functions/css/sass/#dart-sass) pour réaliser cette
étape. Cela fait, et après avoir cloné le dépôt, il faut ouvrir un terminal,
aller dans le répertoire du dépôt, et exécuter :

```sh
hugo server
```

Parmi les lignes renvoyées par Hugo, et en cas de succès, nous trouvons les
informations importantes suivantes :

```
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1) 
Press Ctrl+C to stop
```

Cela indique que pour visualiser le site, il faut ouvrir un navigateur, et se
rendre à l'adresse [http://localhost:1313/](http://localhost:1313/). Bien sûr,
cette adresse peut changer chez vous !

Sur Ubuntu ou Debian, la chaîne totale de commandes serait :

```sh
sudo apt install hugo
git clone https://github.com/kryzar/knowledge-should-be-free
cd knowledge-should-be-free
hugo server
```

Et pour compiler l'intégralité du site, remplacer `hugo server` par `hugo
build`. Un répertoire `public` est alors créé ; la page d'accueil est le
fichier `index.html`, il faut l'ouvrir dans un navigateur pour commencer la
navigation.
