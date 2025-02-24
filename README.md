# Knowledge should be free

## Hébergement et confidentialité

Le site est pour l'instant hébergé par l'hébergeur islandais
[1984.hosting](https://1984.hosting/), que j'ai choisi pour sa bonne réputation
en matière de confidentialité et respect des données, ainsi que sa simplicité.
Le nom de domaine est loué par l'intermédiaire de [Njalla](https://njal.la/).
Le coût annuel de ces deux services est de respectivement 35,40 USD et 15 €,
soit environ 48,80 €.

Ayant conscience de l'importance primordiale de la protection des données de
nos étudiantes et étudiants, j'aimerais à terme faire héberger le site par une
institutions académique française. Toute proposition en accord avec les valeurs
dont ce site se réclame sera étudiée sérieusement.

Aucune collecte de la moindre donnée n'est nécessaire, et ne sera effectuée. En
particulier, aucun mécanisme de collecte ne sera utilisé ou implémenté.

## Pour les développeurs et développeuses

Le site est *statique*. En particulier, il n'est bâti qu'avec HTML et CSS, et
sans JS. Pour limiter la redondance de code, nous utilisons
[Hugo](https://gohugo.io/), un [*générateur de sites
statiques*](https://jamstack.org/generators/). Cela permet de définir un unique
*template* HTML pour les pages de cours, et d'écrire le contenu des pages web
en Markdown. C'est bien plus digeste.

Il y a donc une phase de compilation (*build*) pour pouvoir visualiser le site.
Après avoir installé Hugo, et cloné le dépôt, ouvrir un terminal, aller dans le
répertoire du dépôt, et exécuter :

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
