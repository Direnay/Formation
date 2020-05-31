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

## Les variable globale

Pour faire apparître des élémnts automatiquement il suffit de renseigner dans le document adéquat les "formule" necessaire. 

La page _config.yml détient les information du _**site**_ et paramètres de configuration. Il nous faut dans cette page inscrire l'information. Exemple : titre: Dix reine conteuse
Pour que le titre apparaisse il faut ecrire dans un autre document : {{site.titre}}

Sur une page du site ex: index.md, il détient les informations spécifiques à la page et le sujet principal. 
Dans le layout on informe l'élément qu'on souhaite voir apparaître. Et dans le document on le mentionnel comme dans l'exemple suivant. 
Ex:   layout: default
      auteur: Rendi
      `---
      `{{page.auteur}}

layout

Informations spécifiques à la mise en page + le sujet principal . Les variables personnalisées définies via le sujet dans les mises en page seront disponibles ici.

content

Dans les fichiers de mise en page, le contenu rendu de la publication ou de la page enveloppée. Non défini dans les fichiers Post ou Page.

paginator

Lorsque l' paginateoption de configuration est définie, cette variable devient disponible pour utilisation. Voir Pagination pour plus de détails.

## Les variable du site

site.time = L'heure actuelle (lorsque vous exécutez la jekyllcommande).

site.pages = Une liste de toutes les pages.

Site.posts = Une liste chronologique inversée de tous les messages.

site.related_posts = Si la page en cours de traitement est une publication, celle-ci contient une liste de dix publications associées. Par défaut, ce sont les dix articles les plus récents. Pour des résultats de haute qualité mais lents à calculer, exécutez la jekyllcommande avec l' option --lsi( indexation sémantique latente ). Notez également que GitHub Pages ne prend pas en charge l' lsioption lors de la génération de sites.

site.static_files = Une liste de tous les fichiers statiques (c'est-à-dire les fichiers non traités par les convertisseurs de Jekyll ou le moteur de rendu Liquid). Chaque fichier a cinq propriétés: path, modified_time, name, basenameet extname.

site.html_pages = Un sous-ensemble de la site.pagesliste de ceux qui se terminent par .html.

site.html_files = Un sous-ensemble de la site.static_filesliste de ceux qui se terminent par .html.

site.collections = Une liste de toutes les collections (y compris les articles).

site.data = Une liste contenant les données chargées à partir des fichiers YAML situés dans le _datarépertoire.

site.documents = Une liste de tous les documents de chaque collection.

site.categories.CATEGORY = La liste de tous les messages de la catégorie CATEGORY.

site.tags.TAG = La liste de tous les messages avec balise TAG.

site.url = Contient l'url de votre site tel qu'il est configuré dans le _config.yml. Par exemple, si vous en avez url: http://mysite.comdans votre fichier de configuration, il sera accessible dans Liquid as site.url. Pour l'environnement de développement il y a une exception , si vous exécutez jekyll servedans un environnement de développement site.urlsera mis à la valeur host, portet les options liées à SSL. C'est par défaut url: http://localhost:4000.

site.[CONFIGURATION_DATA] = Toutes les variables définies via la ligne de commande et votre _config.ymlsont disponibles via la sitevariable. Par exemple, si vous en avez foo: bardans votre fichier de configuration, il sera accessible dans Liquid as site.foo. Jekyll n'analyse pas les modifications _config.ymlen watchmode, vous devez redémarrer Jekyll pour voir les modifications des variables.

## Variables de page

page.content = Le contenu de la page, rendu ou non, selon ce que Liquid est en cours de traitement et ce qui pageest.

page.title = Le titre de la page.

page.excerpt = Extrait non rendu d'un document.

page.url = L'URL de la publication sans le domaine, mais avec une barre oblique, par exemple /2008/12/14/my-post.html

page.date = La date attribuée à la publication. Cela peut être annulé dans la première page d'une publication en spécifiant une nouvelle date / heure au format YYYY-MM-DD HH:MM:SS(en supposant UTC), ou YYYY-MM-DD HH:MM:SS +/-TTTT(pour spécifier un fuseau horaire en utilisant un décalage par rapport à UTC, par exemple 2008-12-14 10:30:00 +0900).

page.id = Un identifiant unique à un document dans une collection ou une publication (utile dans les flux RSS). par exemple/2008/12/14/my-post/my-collection/my-document

page.categories = La liste des catégories auxquelles ce post appartient. Les catégories sont dérivées de la structure de répertoires au-dessus du _postsrépertoire. Par exemple, un poste à /work/code/_posts/2008-12-24-closures.mdaurait ce champ défini sur ['work', 'code']. Celles-ci peuvent également être spécifiées dans la première page .

page.collection = L'étiquette de la collection à laquelle appartient ce document. par exemple postspour une publication, ou puppiespour un document au chemin _puppies/rover.md. S'il ne fait pas partie d'une collection, une chaîne vide est renvoyée.

page.tags = La liste des tags auxquels ce post appartient. Celles-ci peuvent être spécifiées dans la première partie .

page.dir = Le chemin entre le répertoire source et le fichier de la publication ou de la page, par exemple /pages/. Cela peut être annulé par permalinkdans la première page .

page.name = Le nom de fichier de la publication ou de la page, par exemple about.md

page.path = Chemin d'accès à la publication ou à la page brute. Exemple d'utilisation: lien vers la page ou la source du message sur GitHub. Cela peut être annulé dans la matière première .

page.next = Le message suivant par rapport à la position du message actuel dans site.posts. Renvoie nilla dernière entrée.

page.previous = Le message précédent par rapport à la position du message actuel dans site.posts. Renvoie nilpour la première entrée

## PaginateurLien permanent

paginator.page = Le numéro de la page courante

paginator.per_page = Nombre de publications par page

paginator.posts = Messages disponibles pour la page actuelle

paginator.total_posts = Nombre total de messages

paginator.total_pages = Nombre total de pages

paginator.previous_page = Le numéro de la page précédente, ou nilsi aucune page précédente n'existe

paginator.previous_page_path = Le chemin d'accès à la page précédente, ou nils'il n'existe aucune page précédente

paginator.next_page = Le numéro de la page suivante, ou nils'il n'existe aucune page suivante

paginator.next_page_path = Le chemin d'accès à la page suivante, ou nils'il n'existe aucune page suivante








