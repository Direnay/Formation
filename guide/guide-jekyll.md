# Jekyll

C’est un site statique qui est uploadé sur le serveur (donc pas besoin de Ruby).
C’est difficile de faire plus rapide qu’un site statique.
On peux modifier l'apparence des URL du site, les données affichées sur le site, etc.
Jekyll est un Ruby Gem qui peut être installé sur la plupart des systèmes.

Un générateur permet de gérer plus facilement tous les assets du projet (CSS, JS, images et compression, etc.)
On peu utiliser des _**layout**_ et des partials pour ne pas avoir à ré-écrire chaque fois son code.
Le contenu de chaque page est séparé de son affichage et lorsqu’on lance la génération du site, le générateur injecte le contenu dans le moule correspondant.
Jekyll utilise par défaut Liquid comme langage de templating.

## Installation jekyll sur ubuntu

1. Pour installer l'environnement de développement Ruby complet il faut dans un premier temps écrire cette formule dans le terminal; 
_**sudo apt-get install ruby-full build-essential zlib1g-dev**_

Il est préférable d'éviter d'installer Ruby Gems en tant qu'utilisateur root. Par conséquent, nous devons configurer un répertoire d'installation de gem pour votre compte d'utilisateur. Les commandes suivantes ajouteront des variables d'environnement à votre _**~/.bashrcfichier**_ pour configurer le chemin d'installation de gem. Exécuter:

_**echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc**_

Enfin, installer Jekyll:

_**gem install jekyll bundler**_

2. Installez les gemmes Jekyll et bundler .
_**gem install jekyll bundler**_

3. Créez un nouveau site Jekyll sur ./myblog.
_**jekyll new myblog**_
4. Accédez à votre nouveau répertoire.
cd myblog
Créez le site et rendez-le disponible sur un serveur local.
bundle exec jekyll serve
Accédez à http: // localhost: 4000

## Verification version 

La version ruby peut être vérifiée en exécutant _**ruby -v**_
RubyGems, on peux vérifier en exécutant _**gem -v**_
GCC et Make, au cas où votre système ne les aurait pas installés, on peux le vérifier en exécutant _**gcc -v, g++ -v et make -v**_ dans l'interface de ligne de commande du système

### Exemple simple de blog avec Jekyll
Dans le cas d’un blog, nous avons :

* Un fichier de _**layout**_ général qui contient tout l’HTML principal (doctype, head, métas) avec éventuellement footer, header et sidebars en partials. Ce fichier va également définir le comportement de la page d’accueil (affichage des X derniers posts). On peut également définir un layout différent de celui par défaut.

* Un autre layout pour l’affichage des billets de blogs.

* Un répertoire contenant le contenu proprement dit (les billets).

* Pusieurs choix sont possibles, mais par défaut ce sont des fichiers markdown un peu spéciaux. Ils ont un en-tête avec différentes variables pour le titre, l’auteur, la date et éventuellement les catégories du billet.

* Un fichier de configuration (en yaml) qui va servir de chef d’orchestre et dire à Jekyll quoi faire pour la génération.
Nous pouvons sur ce fichier modifier le titre de la page, élément en bas de page... tout se qui apparait en fixe sur le blog. 

## Lorsqu’on lance la génération

Jekyll compile les différents assets suivant les règles prédéfinies ;
Génère les pages HTML à parti des fichiers sources markdown.
Jekyll peut générer également une sitemap, des archives, etc.
Il peut également parser les fichiers sources et transformer par exemple des liens vers flickr en mini-galeries d’images ou des liens youtube en players intégrés à la page. Il existe de nombreux plugins pour cela.
A noter que Jekyll permet aussi d’avoir un mode serveur où la compilation se fait à la volée et où on peut voir les résultats sur un serveur local.

Jekyll très bien intégré à Github et c’est la solution recommandée pour générer les pages de présentation d’un projet.

Jekyll n’est pas limité aux blogs, on peut tout à fait réaliser un portfolio ou des pages produits en rajoutant les layouts correspondants. Il suffit en suite de définir dans chaque fichier source le layout à utiliser pour sa génération.

