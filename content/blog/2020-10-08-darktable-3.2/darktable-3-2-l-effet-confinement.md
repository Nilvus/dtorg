URL:     https://linuxfr.org/redaction/news/darktable-3-2-l-effet-confinement
Title:   darktable 3.2 : l'effet confinement !
Authors: Nilvus
         aurelienpierre, jpg54, hgmarty, jpv, teoB, Pascal Obry, JM40, play0ad, zakfm, palm123 et Ysabeau
Date:    2020-06-03T18:12:15+02:00
License: CC By-SA
Tags:    darktable, photographie, raw, photos, photo, mots-clés et métadonnées
Score:   0


Comme ne le veut pas la tradition, pour la première fois de son histoire, darktable voit sa nouvelle version majeure 3.2, sortir quelques mois plus tôt, en plein été. Le confinement de cette année, déjà bien particulière, a entraîné un nombre record de contributions et d’améliorations sur darktable 3. Cerise sur le gâteau, une version majeure, 3.4, est toujours programmée pour Noël. 2020 sera donc la première année où l’équipe darktable aura le plaisir de vous proposer deux versions majeures.

Avant d’entamer la lecture des nouveautés de cette 3.2, pour ceux qui souhaitent se rafraîchir la mémoire, vous trouverez les nouveautés de la 3.0 (et en fin d’article la majorité des nouveautés des 3.0.1 et 3.0.2 ; la 3.0.2 n’apportant pas de nouveauté significative) sur [l’article 3.0](https://linuxfr.org/news/darktable-3-0-une-version-plus-que-majeure) sorti à Noël.

Une interface affinée, dans les moindres détails : pour un look professionnel
=============================================================================

L’interface a connu un profond changement via la 3.0. L’équipe darktable a peaufiné ce travail jusque dans les moindres détails. Ainsi, darktable 3.2 vous apporte une interface et de nouveaux apports améliorant encore plus l’expérience utilisateur. Le style 3.0 se confirme et s’améliore… pour un look plus professionnel. Plusieurs développeurs ont travaillé d’arrache-pied pour vous apporter une interface soignée, à commencer par une réécriture complète de la table lumineuse qui s’accompagne également de belles améliorations de performance.

Les améliorations de l’interface sont nombreuses, certaines seront détaillées plus bas, comme la refonte des préférences, les boutons dynamiques ou les infos-bulles, ou encore le plus gros morceau, à savoir le remaniement en profondeur de la table lumineuse.

Ce travail sur l’interface a été l’occasion d’une restructuration complète du CSS, afin de le rendre plus clair à la lecture. Ainsi, il est plus aisé, à l’appui par ailleurs de plus de commentaires, de repérer la partie qu’on souhaite personnaliser sur l’interface. Vous pourrez d’autant mieux en saisir l’utilité en découvrant plus bas les nouvelles préférences proposées par darktable 3.2. Par ailleurs, cet important travail a permis d’aller encore plus loin dans l’objectif de rendre le plus possible l’interface personnalisable via le CSS.

Enfin, la cohérence de l’interface entre les différents thèmes a également été drastiquement améliorée par ce travail d’optimisation du CSS. Il en est de même pour chaque élément de l’interface (exemple : les cases à cocher n’avaient pas, partout, le même aspect avant cette 3.2).

## Table lumineuse : un remaniement en profondeur sur tous les plans

La table lumineuse est certainement la partie qui a le plus évoluée. Grâce, notamment, au travail majeur d’AlicVB (Aldric Renaudin), la table lumineuse est tout simplement plus performante. La vitesse d’affichage est notable, particulièrement via le mode table lumineuse zoomable et sur des configurations un peu plus anciennes. Le bandeau d’images bénéficie également d’une refonte et d’améliorations de performance.

Dans cet article, pour des simplifications d’écriture, la refonte de la table lumineuse s’entend sur tous les modes liées à celle-ci, à savoir aussi bien le mode _table lumineuse zoomable_, le _navigateur de fichier_, le mode _sélection_ ou encore _l'aperçu_. Toutes ces parties sont, de par cette refonte, déjà prêtes pour un usage via une résolution écran 8k.

Aldric a également intégré de nouvelles options de surimpression des informations des vignettes, applicable indépendamment dans chacun des modes existants (_table lumineuse zoomable_, _navigateur de fichier_, _sélection_, _aperçu_ et _bandeau d’images_). Désormais, en cliquant sur l’icône étoile en haut à droite, vous découvrirez un menu proposant ces nouvelles options d’affichage des vignettes, incluant sept modes d’affichage des informations (étoiles, icônes groupe, développement, labels couleurs, informations), dont un mode minimaliste sans distractions (« pas de surimpression »). Une option permet également d’afficher ou non les infos-bulles en survolant les vignettes. Le contenu de ces infos-bulles est personnalisable dans les préférences.
**_Attention :_** laisser vide le champ gérant le contenu dans les préférences n’affichera rien, quelle que soit l’option sélectionnée dans le menu ci-dessous.

![Menu popover de sélection des modes de surimpression](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/popover-overlays-fr.png)

Les sept nouveaux modes de surimpression des vignettes, permettent d’aller d’un mode qui n’affiche que l’image, à un mode complet étendu. Globalement, ces modes de surimpression sont progressifs, du premier qui ne précise aucune information aux derniers affichant toutes les informations de manière différente. Voici un aperçu de certains modes, à commencer par une vue globale de l’interface peaufinée, en mode de surimpression n° 6 (ligne sélectionnée ci-dessus). Ce mode affiche donc en permanence certaines infos et les infos étendues (ici le nom du fichier de l’image et infos principales) au survol de la souris. À noter que les informations étendues affichées sont également paramétrables dans les préférences (onglet table lumineuse).

![Mode de surimpression permanent et étendu au survol de la souris](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/lighttable-mode6-fr.png)

Les deux premiers modes sont très proches. Par défaut, ils n’affichent aucune information autour des images. Seul le deuxième mode ajoutera l’affichage de certaines informations au survol de la souris. Voir ci-dessous :

![surimpression lors du survol souris](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/overlays-on-mouse-hover.png)

Le mode le plus détaillé par défaut pour les vignettes, est le cinquième (surimpressions étendues permanentes) et ressemble à cela :

![surimpressions étendues permanentes](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/permanent-extended-overlays.png)

Enfin, le septième et dernier mode a été particulièrement créé pour être adapté aux modes _sélection_ et _aperçu_ (et celui appliqué par défaut à ces modes). Ce mode permet de personnaliser la durée d’affichage, au survol par le curseur de l’image, fixé à 3s par défaut, peut être fixé à -1 pour un affichage permanent. Dans tous les cas, cet affichage ne se fait que si l’image est survolée par le curseur. Enfin, ce nouveau mode permet d’afficher le niveau de zoom de l’image dans les modes _sélection_ et _aperçu_.

![Bloc de superposition en mode aperçu et sélection](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/block-overlays-fr.png)

Les autres modes sont donc intermédiaires à ceux présentés ici et si vous voulez les découvrir, installez et ouvrez darktable 3.2. Rien ne vaut mieux que de les tester tous vous-même.

Le bandeau d’images, qui peut être affiché via `Ctrl` + `F` en bas de certaines vues (_chambre noire_, modes _sélection_ et _aperçu_, vue _carte_ ou _impression_…) peut également être défini avec ces nouveaux modes d’affichage. Dans les vues où ce bandeau est affiché, c’est toujours via l’icône étoile que vous pourrez personnaliser l’affichage. Ainsi, par exemple, en _chambre noire_, l’icône étoile n’est utilisable que si le bandeau images est affiché et le menu n’est donc applicable que pour le bandeau. Autre exemple, en mode _sélection_, si le bandeau d’images est affiché, le menu « étoile » permettra donc de personnaliser, et la vue _sélection_, et l’affichage des vignettes du bandeau.

À noter également que le bandeau d’images voit la visualisation de l’image sélectionnée (ou des images sélectionnées, en vue _sélection_), améliorée. Cet affichage était plutôt confus jusque-là. Désormais, la sélection est bien plus visible. Voyez plutôt :

![Sélection image du bandeau images](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/select-image-filmstrip.png)

## Refonte des préférences : pour mieux s’y retrouver

Avec l’introduction des nouvelles fonctionnalités depuis la 3.0, les préférences ont été réorganisées, augmentant le nombre d’onglets, afin d’offrir une lisibilité plus importante. Un des objectifs a par ailleurs été d’éviter les longs défilements pour accéder à une option. Ainsi, chaque onglet ne fait pas plus d’une page (sauf l’onglet pré-réglage). Chaque onglet a de plus un nom qui décrit clairement les options qui y sont paramétrables.

Parce que des captures d’écran en parlent mieux, voici deux exemples d’onglet pour montrer cette refonte très efficace :

![Préférences darktable v3.2, onglet général](https://raw.githubusercontent.com/hgmarty/images-dt/master/preferences-fr.png)

Comme vous pouvez le voir sur cette image, de nouvelles options d’interface sont également apparues. Il est désormais possible, soit d’utiliser la police système (ou taille de police si le thème utilisé est un thème élégant), comme auparavant, soit de personnaliser la taille de la police et la mise à l’échelle pour les écrans à très haute résolution, directement depuis darktable. Une option demandée depuis un bon moment, enfin là !

D’autres options permettant d’affiner aussi la taille de l’ensemble des éléments de l’interface, au bon vouloir de l’utilisateur. Attention à rester raisonnable sur ces options DPI, les options par défaut restent recommandées pour la majorité des utilisateurs.

Enfin, elstoc, le développeur ayant fait cette refonte a intégré la possibilité, directement depuis les préférences, de personnaliser l’affichage de l’interface en intégrant vos propres personnalisations CSS, comme vous pouvez le voir sur la capture d’écran ci-dessus.

Pour donner un autre exemple :

![Préférences darktable v3.2, onglet traitement](https://raw.githubusercontent.com/hgmarty/images-dt/master/preferences-traitement-fr.png)

## Boutons dynamiques : selon vos actions

Et darktable devient « vivant » !

Une nouvelle fonction de boutons dynamiques a été intégrée, pour une meilleure expérience utilisateur. Elle est surtout visuelle mais aussi bien pratique. Mais de quoi il me parle l’auteur ici ? Eh bien, pour illustrer, rien de plus simple, ouvrez un module à droite de la table lumineuse, par exemple, _images sélectionnées_. Selon la position du curseur et la sélection faite (ou pas de sélection), vous verrez que certains boutons deviennent cliquables et d’autres non.

Les boutons dynamiques, c’est tout simplement l’affichage des boutons selon qu’ils sont utilisables ou non dans le contexte actuel.

Un autre exemple, sélectionnez une image, ouvrez le module _développement_ et cliquez sur copier. Tant que vous restez sur l’image sélectionnée, coller n’est pas utilisable (aucun intérêt de coller le développement d’une image sur elle-même). Sélectionnez maintenant une autre image et coller devient utilisable.

Quelques autres détails
-----------------------

### Infos-bulles améliorées

Les infos-bulles ont été améliorées. En effet, les infos-bulles ont parfois le défaut de s’afficher là où on ne veut pas. Malheureusement, ce problème ne peut pas être corrigé par l’équipe darktable puisque c’est un défaut inhérent à la bibliothèque graphique utilisée par darktable, à savoir Gtk+. Pour contourner cela autant que possible, l’équipe darktable a intégré deux choses (après de longs débats) :

- la possibilité d’afficher/masquer les infos-bulles à tout moment via un simple raccourci : `Maj` + `T` ;
- un affichage des infos-bulles visuellement amélioré (légèrement).

Un nouveau type d’infos-bulles fait également son apparition, utilisé principalement en chambre noire. Elles apparaissent en haut de l’image et permettent de rendre visible quelques informations essentielles comme, par exemple, le réglage d’opacité d’un masque ou encore l’ajustement d’exposition… Afficher ou désactiver les infos-bulles est également confirmé par un message via ce nouveau type d’info-bulle.

![Info-bulle](https://raw.githubusercontent.com/Nilvus/dtorg/c8618d10360ce9fdba64a954446177cc2d99be00/content/blog/2020-10-08-darktable-3.2/fr/info-bulle-fr.png)

### Une nouvelle ligne de comparaison d’instantanés et la coloration de l’affichage sur image

darktable 3.2 apporte aussi quelques améliorations visuelles sur l’image en chambre noire. La ligne de comparaison d’un instantané avec la ligne d’historique comparée est plus visible, intégrant un repère visuel de l’instantané sélectionné (une flèche avec le symbole S pour snapshot).

Vous trouverez également une nouvelle option en bas à droite, via une icône quadrillée rouge et verte, permettant de choisir la couleur d’affichage de cette ligne d’instantanée ainsi que tout élément visuel qui s’afficherait sur l’image, comme, par exemple, les éléments de sélection de masque dessiné. Six couleurs sont disponibles (gris, rouge, vert, jaune, cyan et magenta). Il est aussi possible de modifier directement la couleur de ces éléments via le raccourci `Ctrl` + `O` (la lettre), jusqu’à la couleur adaptée. La couleur change instantanément et est confirmée via le nouveau type d’info-bulle qui s’affiche en haut de l’image.

Voir ci-dessous un exemple de la nouvelle ligne de comparaison d’instantané en rouge et l’icône de sélection de couleur entourée en rouge.

![instantané et option couleur](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/overlay-darkroom-color.png)

### Changements mineurs sur l’interaction utilisateur

Tous ces changements entraînent aussi quelques modifications d’usage des raccourcis. Tout d’abord, la sélection d’image via le bandeau d’images en chambre noire, change. Désormais, un simple clic permet de changer l’image à traiter (et non plus un double-clic).

La gestion de l’affichage des panneaux évolue. Il est désormais possible de modifier l’affichage des panneaux du haut (en-tête et barre d’infos) et de même pour le bas avec une seule combinaison de touches. Par défaut, les raccourcis de la 3.0.x sont désactivés (`Maj` + `Ctrl` + `T` et `Maj` + `Ctrl` + `B`) mais peuvent être redéfinis dans les préférences.

### Mais encore

Plusieurs icônes ont été redessinées, des quatre icônes en haut à droite (groupe, étoile, aide et préférences) en passant par les icônes de masques. Ce travail permet un bien meilleur affichage, particulièrement sur les écrans HiDPI (haute résolution) sous Windows et donc une meilleure cohérence d’affichage selon le type d’écran (LoDPI (basse résolution) ou HiDPI (haute résolution)), quelle que soit la taille des icônes.

Toutes les pipettes ont été retravaillées pour un comportement global et un affichage plus homogène dans toute l’interface. Ce travail ajoute également une fonctionnalité de redimensionnement des zones définies par une pipette.

L'interface du sélectionneur de fichiers a également été revue.

La barre de progression d’export et d’impression a été visuellement revue pour une intégration plus fine à l’interface.

En chambre noire, le module actif est signalé par un nouvel effet visuel sur l’icône de statut et le titre du module : voir la capture d’écran de filmique v4, dans la présentation de cette nouvelle version, plus bas dans l’article.

La liste de résultats de recherche de localisation en vue carte a enfin un aspect convenable et plus lisible.

Toutes les barres de réglages ont été affinées : les barres sont plus fines et les curseurs de contrôle plus visibles.

Et quelques autres petits détails un peu partout.

Gestion du patrimoine numérique
===============================

## Éditeur de métadonnées et mots-clés évoluent

Les évolutions ne sont pas énormes mais plus que bienvenues.

### L’éditeur de métadonnées

Jusque-là, l’éditeur comportait 5 champs, il en compte désormais deux de plus : un champ « notes », pour ajouter des notes ; et un champ « nom de version » pour, par exemple, personnaliser le nom de différentes versions d’une même image. Ces nouveaux champs ont bien entendu été intégrés aux options d’importation. Ces options d’importation ont, par la même occasion, été harmonisées entre les possibilités d’import de darktable (et chaque champ peut directement être activé ou non à l’import).

Tous les champs de l’éditeur sont enfin multi-lignes. Il suffit d’appuyer sur `Ctrl` + `entrée` pour ajouter une ligne à un champ (appuyer sur entrée vous amène au champ suivant en enregistrant le champ précédemment complété). De ce fait, les champs peuvent également être agrandis avec `Ctrl` + `défilement`.

En ouvrant ce nouvel éditeur, vous constaterez également l’apparition d’une icône de préférence. Pour chaque champ de l’éditeur, vous pouvez décider de le cacher (donc le masquer de l’éditeur) ou de le rendre privé (non exportable).

### Les mots-clés

darktable 3.2 améliore un peu plus la gestion des mots-clés. Via darktable 3.0.2, il n’était pas toujours possible d’ajouter un mot-clé à un parent existant, c’est désormais possible systématiquement en améliorant la gestion des mots-clés virtuels (non utilisés). Ces derniers s’affichent en italiques désormais.

La création de mots-clés fonctionne maintenant sans image sélectionnée. Il est possible de créer une balise sur un nœud virtuel, d’insérer un caractère pipe | dans la balise de création. L’affichage de l’arbre montre les balises nouvellement créées.

Mais surtout, un nettoyage important a été fait, résolvant quelques bugs. Par exemple, la mise à jour d’un mot-clé pouvait nécessiter le redémarrage de darktable pour être prise en compte ; ce n’est plus nécessaire. En bref, darktable 3.0 a initié un nouveau module mots-clés, darktable 3.2 l’affine et le finalise.

## De nouveaux filtres de collection

Sept nouveaux filtres s’ajoutent aux nombreux déjà existants. darktable est déjà très riche en filtres sur les métadonnées des photos (données EXIFS et données IPTC/XMP). Par contre très peu de filtres existaient sur les divers événements ou traitements propres à darktable. Vous connaissiez déjà les filtres **pellicule**, **mot-clé** et **copie locale**. La version 3.2 ajoute maintenant les nouveaux filtres suivants : **historique**, **module**, **ordre des modules**, **date importation**, **date traitement**, **date exportation** et **date impression**. Voici une description rapide du rôle de ces nouveaux filtres.

* **historique** - permet de sélectionner les photos développées ou les photos non développées.
* **module** - permet de sélectionner les photos dont la pile de développement contient un module précis. Tous les modules utilisés au moins une fois sont présentés.
* **ordre des modules** - permet de sélectionner les photos traitées avec un ordre de modules précis. Tous les ordres de modules existants sont présentés.
* **date importation** - permet de sélectionner les photos importées à un horodatage précis (horodatage = date et heure). Tous les horodatages sont présentés.
* **date traitement** - permet de sélectionner les photos traitées à un horodatage précis. Tous les horodatages sont présentés.
* **date exportation** - permet de sélectionner les photos exportées à un horodatage précis. Tous les horodatages sont présentés.
* **date impression** - permet de sélectionner les photos imprimées à un horodatage précis. Tous les horodatages sont présentés.

## De nouvelles informations sur l’image

Le module informations de l’image affiche également de nouvelles informations. Les quatre horodatages mentionnés ci-dessus : **date importation**, **date traitement**, **date exportation** et **date impression**, ainsi qu’une nouvelle information EXIF : le **biais d’exposition**.

La fenêtre du module est plus petite, mais elle est maintenant scrollable et redimensionnable avec `Ctrl` + `défilement`.

Un nouveau module : _docteur néga_
==================================

Le module actuel d’inversion de négatifs argentiques possède un défaut majeur : il fonctionne obligatoirement sur le signal non-dématricé du capteur, si le négatif a été numérisé avec un appareil photo numérique, et donc obligatoirement avant le profil de couleur d’entrée, quoi qu’il arrive. Ceci implique deux problèmes insolubles :

1. si le fichier numérique provient d’un vrai scanner, et qu’il est encodé avec une fonction de transfert (le « gamma »), celui-ci n’est pas annulé avant l’inversion. Suivant le type de numérisation que vous travaillez (« RAW » en 16 bits linéaire d’un scanner de film spécialisé, ou scan JPEG 8 bits encodé en gamma d’un scanner grand public), vous n’aurez pas du tout le même comportement. Notez que si la numérisation est faite à partir d’un autre appareil, le signal est linéaire, donc le problème ne se pose pas ici.
2. on inverse la couleur avant de corriger l’espace de couleur du scanner ou de l’appareil numérique, ce qui fait que les profils de couleurs deviennent alors faux (il faudrait les inverser eux aussi), et qu’on ne peut pas soustraire proprement la déviation colorimétrique (inévitable) du capteur utilisé pour la numérisation.

Il s’ensuit donc de fastidieuses séances de rattrapage de couleur, utilisant différents modules pour rattraper à la main ce qui aurait dû être fait automatiquement par le profil de couleur d’entrée s’il avait été appliqué au bon moment, c’est-à-dire avant l’inversion des couleurs du négatif.

_Docteur néga_ règle ça, et bien d’avantage, en se basant sur le système de sensitométrie Kodak Cineon, développé dans les années 1990 pour numériser les bobines de films au cinéma.

Depuis l’avènement de la photo numérique, beaucoup de photographes argentiques aimeraient bien retrouver leurs anciennes photos dans leur flux de travail numérique. Plusieurs méthodes existent :

* les faire numériser par un professionnel mais, pour avoir une bonne résolution, cela coûte relativement cher ;
* les numériser soi-même avec un scanner de films : les scanners bas de gamme ne numérisent pas à plus de 10 Mpx et généralement ne proposent que le format JPEG avec une bonne perte des possibilités de post-traitement ; les scanners haut de gamme proposent des résolutions un peu supérieures et le format Tiff en 16 bits meilleurs pour le post-traitement. Par contre, ils sont très lents pour obtenir des résolutions élevées et nécessitent d’utiliser son ordinateur : ces scanners proposent d’inverser directement les négatifs à partir de leur logiciel

Et pourquoi ne pas utiliser son APN avec un système de prise de vue macro pour reprographier ses négatifs argentiques et utiliser darktable pour faire ce travail ?

Pour les besoins de l’article, un Lumix Gx8 (20 MP en RAW) avec un Leica Elmarit f:2.8 de 45mm macro a été utilisé pour digitaliser des photos argentiques : négatifs N/B et couleur et diapos N/B et couleur. Notez que : 
1. Les diapositives ne posent aucun problème de traitement avec darktable (pas besoin d’inversion),
2. Les négatifs N/B sont relativement simples à inverser et la plupart des logiciels proposent cette inversion. Dans darktable, le module d’inversion classique est suffisant, mais docteur néga les gère également,
3. Les négatifs couleur sont plus capricieux à cause de la couleur de base du film (orange) et de la balance des blancs. Pour les logiciels qui les gèrent, il faut un échantillon du film non exposé pour récupérer les valeurs RGB du filtre orangé pour les soustraire du négatif exposé.

_Docteur néga_ permet de traiter les négatifs N/B et couleur. Pour en tirer le meilleur résultat possible, il est important de garder une portion du film non-exposé autour de l’image (pour prélever le Dmin, voir plus bas) et de suivre une routine rigoureuse qui corrige la couleur en deux temps :

1. on corrige d’abord la numérisation, c’est à dire les déviations colorimétriques apportées par l’appareil photo ou le scanner qui ont numérisé la pellicule,
2. on corrige ensuite la pellicule proprement dite, c’est-à-dire les déviations colorimétriques apportées par la pellicule et par son éventuel vieillissement.

La première étape s’effectue tôt dans le pipeline, en neutralisant la balance des blancs capteur, en ajustant l’exposition pour que l’histogramme de l’image occupe toute la plage 0–100 % sans valeurs négatives ni écrêtage, et en appliquant le profil de couleur d’entrée (ICC) du capteur utilisé.

La deuxième étape s’effectue dans _docteur néga_ :

![negadoctor](https://raw.githubusercontent.com/jpg54/dtorg/8e7b5db86e11dfd830b433b1652fc40b00a55982/negadoctor%20FR.png)

Un sélecteur permet de passer au négatif N/B :

![selecteur couleur - N/B](https://raw.githubusercontent.com/jpg54/dtorg/8e7b5db86e11dfd830b433b1652fc40b00a55982/negadoctor%20selection%20N-B%20Couleur%20FR.png)

En ouvrant un négatif argentique N/B :

![Ouverture N/B](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20FR.png)

Vous n’avez qu’à cliquer sur « noir et blanc » à la place de « couleur » pour inverser le négatif, puis à régler les paramètres impérativement dans l’ordre dans lequel ils se trouvent dans l’interface : 

1. pour le Dmin, sélectionnez avec la pipette une partie non exposée du film. Ceci récupère la densité minimale du film, correspondant aux zones où il est le plus transparent,
2. pour le Dmax, sélectionnez avec la pipette une zone de hautes lumières **exemptée de poussières ou rayures**. Ceci récupère la densité maximale du film, correspondant aux zones où il est le plus opaque,
3. pour le biais d’exposition du scanner, sélectionnez une zone censée être noire, ou même toute l’image. Il permet d’ajuster l’exposition du scanner de sorte que les noirs soient bien noirs.

![Inversion par défaut](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20defaut%20FR.png)

La teinte verte avant inversion, et indigo après inversion, vient de la balance des blancs de l’appareil photo, puisque la numérisation est faite en RGB. Il faudra la neutraliser avec la balance des blancs classique (avant docteur néga). Pour simuler un tirage des négatifs sur du papier à tons chauds, on peut utiliser l’onglet « corrections » de _docteur néga_, qui permet de teinter le tirage virtuel en utilisant les mêmes algorithmes que la balance couleur.

![Inversion tons chauds](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20Tons%20Chauds%20FR.png)

Quelques réglages, dans l’onglet « corrections », permettent de corriger la balance des blancs de l’émulsion ou de teinter le négatif à des fins créatives. Quelques remarques importantes :

1. si le film couleur a été exposé exactement à sa température couleur nominale (D50 pour un film « lumière du jour »), la correction de balance des blancs dans _docteur néga_ devrait être inutile (les deux valeurs devraient être blanc pur), sous réserve que le capteur de numérisation ait été correctement corrigé au préalable (balance des blancs et profil d’entrée),
2. si le film couleur a été exposé à une température couleur différente de celle pour laquelle il a été équilibré, seule la correction de **balance des blancs des hautes lumières** est nécessaire. Cette correction était utilisée dans le système Kodak Cineon et simule une correction de l’émulsion au niveau du film lui-même.
3. la **dérive de couleurs des ombres** est un ajout par rapport au Cineon classique, qui sert à récupérer des virages de couleur importants, notamment sur des négatifs endommagés qui ont été mal conservés. Pour l’utiliser, assurez-vous que le **biais d’exposition du scan**, dans l’onglet « film », soit non nul ou le réglage sera sans effet. Réglez alors la dérive de couleur des ombres en premier, en pipettant sur des noirs, puis la balance des blancs des hautes lumières en second, en pipettant dans les blancs (en suivant l’ordre de l’interface). La **dérive de couleurs des ombres** simule un étalonnage à la tireuse couleur à lumière additive.
4. les corrections de couleurs sont proposées aussi si vous travaillez des négatifs noir et blanc, pour vous permettre d’effectuer des virages de ton dans un espace logarithmique non inversé. Les mêmes algorithmes sont disponibles dans la balance couleur, mais travaillent dans un espace pseudo-linéaire et après inversion.
5. _docteur néga_ utilise l’espace RGB de travail du pipeline, soit Rec 2020 linéaire par défaut. Si ceci fonctionne raisonnablement bien, l’espace de couleur réel du film n’est pas Rec 2020 et il peut être utile d’utiliser l’espace RGB réel du film pour travailler la couleur. Un [développeur de Rawtherapee](https://discuss.pixls.us/t/any-interest-in-a-film-negative-feature-in-rt/12569/177) qui a travaillé sur un module d’inversion similaire a créé un profil de couleur RGB à partir de la sensibilité spectrale des émulsions Fuji et Kodak. Il suffit de le [télécharger](https://discuss.pixls.us/uploads/short-url/1MgJasUWznCk2pU6pTupLFJ21xU.icc), de l’ajouter dans `~/.config/darktable/color/out`, puis de choisir `FilmNegRGB_650_550_460-elle-V4-g10.icc` comme profil de travail dans le module _profil de couleur d’entrée_. Il n’est pas clair, à ce stade, si ce profil marche mieux en général que Rec2020 pour compenser la couleur, mais c’est une option.
6. des corrections de couleur définies dans un espace de travail deviendront fausses et devront être refaites si l’espace de couleur de travail est changé.

![Corrections pour obtenir les tons chauds](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20%20correction%20FR.png)

L’onglet « impression » permet d’ajuster les paramètres de l’impression virtuelle en fonction du papier utilisé ou du système de reproduction. En effet, le négatif est un support transparent dont l’opacité (la densité) ne peut pas être nulle, à la fois physiquement (il suffit de regarder le film) mais aussi mathématiquement (on travaille en espace logarithmique, et le logarithme de 0 n’existe pas). C’est au moment de l’impression virtuelle qu’on recale le noir de la pellicule (le Dmin) avec la valeur RGB (0, 0, 0) afin d’ajuster l’image aux hypothèses de base du pipeline numérique.

Le niveau de noir définit la correction de densité du noir et permet d’ancrer l’histogramme à gauche. Le grade correspond à la courbe de contraste du papier, aussi appelé dureté ou gamma (qui n’a rien à voir avec le gamma écran ou celui du profil ICC… simple). La brillance correspond à une compression des hautes lumières : 100 % signifie pas de compression ; plus on descend la valeur, plus on comprime les hautes lumières et on avale leur contraste local. Utilisé en combinaison avec l’ajustement d’exposition, ceci permet d’augmenter la luminosité générale de l’image sans écrêter les valeurs.

![Impression](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20Impression%20FR.png)

Pour le traitement d’un négatif couleur :

![docteur néga - couleur](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20couleur%20FR.png)

il suffit d’activer _docteur néga_ (le filtre orangé va être neutralisé avec la valeur par défaut) :

![Inversion par défaut](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20couleur%20positif%20FR.png)

Et après avoir fait quelques corrections :

![Inversion corrigée](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20couleur%20positif%20Corr%20FR.png)

_Docteur néga_ est un de ces modules qui peut dérouter, car plusieurs paramètres vont avoir apparemment le même effet sur l’image finale. Par exemple, le Dmin, le biais d’exposition du scan, et la correction de densité du noir vont tous impacter la densité finale du noir, mais le Dmin travaille en linéaire avant inversion, le biais d’exposition en logarithme avant inversion, et la correction d’exposition en pseudo-gamma après inversion. Chacune de ces corrections du noir a une justification mathématique non-intuitive (liée aux fonctions utilisées, acceptant ou non des valeurs nulles) qu’une simple évaluation visuelle du résultat final ne fera pas apparaître.

Il est donc important d’être méthodique dans l’utilisation pour éviter de perdre pied dans les nombreuses combinaisons de paramètres qui peuvent produire un résultat visuel similaire, en respectant l’ordre d’utilisation des réglages défini par l’interface (utilisez les onglets de gauche à droite, et de haut en bas). Retenez qu’on ne fait ici que simuler numériquement un processus d’impression en chambre noire, en corrigeant d’abord le scanner, puis le négatif, puis le tirage papier, en suivant la chaîne de production d’image. Chaque valeur, chaque opération, chaque étape est liée à une réalité physique mise en pratique sans forcément s’en rendre compte au laboratoire photo.

Enfin, pour utiliser _docteur néga_, pensez à désactiver la courbe de base et filmique, puisqu’ils feraient doublon avec le film lui-même. Une fois toutes vos corrections de couleur effectuées, vous pourrez alors recadrer l’image pour supprimer le cadre non-exposé.

Nouveaux flux de travail par défaut
===================================

Le conflit de fonctionnalité entre _filmique_ et la _courbe de base_, pour fournir la nécessaire transformation de tons du RVB linéaire vers le RVB écran, était jusqu’à présent géré via une option, dans les préférences, qui permettait d’activer par défaut la _courbe de base_, ou pas. Cependant, rien n’était disponible pour activer _filmique_ automatiquement. C’est désormais réglé avec les flux de travail par défaut, disponibles dans les préférences à l’onglet traitement. 

Le flux « relatif à l’affichage », utilisé par défaut, active automatiquement la _courbe de base_ et ordonne les modules dans le pipeline tels qu’ils étaient pour darktable 2.6 et précédents. À ce titre, il va appliquer la transformation non-linéaire au début du pipeline, et toute la retouche sera ensuite effectuée sur du RGB non-linéaire, comme le font la quasi-totalité des logiciels de retouche photo. Le seul mérite de ce flux de travail est qu’il correspond à ce à quoi beaucoup de photographes sont habitués, mais il va poser de nombreux problèmes de cohérence des couleurs et de crédibilité de certains filtres locaux (flou ou accentuation de netteté), notamment dans les scènes à large dynamique.

Le flux « relatif à la scène » est pensé autour de _filmique_, pour offrir le même niveau de fonctionnalité que le flux « relatif à l’affichage ». Il consiste à ajouter, par défaut, +0,75 IL d’exposition (dans le module exposition), afin d’ajuster la luminosité générale et le gris moyen à une valeur similaire à celle utilisée par la plupart des JPEG retouchés par les boîtiers réflex.
**_Nouveauté :_** le module _exposition_ compensera également le biais d’exposition défini sur l’appareil (la correction d’EV du posemètre), couramment utilisé pour éviter l’écrêtage des hautes lumières, pour les photographes qui exposent à droite de l’histogramme. Cette fonctionnalité repose sur la lecture du champ EXIF `ExposureBiasValue` qui doit être correctement renseigné dans le fichier RAW par l’appareil photo pour qu’elle fonctionne. À noter : pour les RAW Fuji, il sera nécessaire d’ajouter encore +0,75 IL, soit une correction globale de +1,45 IL, pour compenser leur sous-exposition native.
Ensuite, _filmique_ est appliqué par défaut et ses paramètres de base tiennent compte de la correction globale d’exposition (incluant la correction de +0,75 IL du gris moyen et le biais d’exposition). Ceci permet donc d’avoir une base de travail raisonnablement proche du JPEG boîtier, directement en ouvrant le RAW dans darktable. Mais comme tout pré-réglage par défaut, il est pensé pour fonctionner correctement 80 % du temps, et des ajustements manuels additionnels seront nécessaires dans les 20 % restants ; en particulier, certains appareils appliquent une correction de +0,5 IL et d’autres de +1 IL, il est donc illusoire de chercher à satisfaire tout le monde. 

Rappelons ici que l’intérêt de _filmique_ est d’appliquer une courbe de mappage des tonalités en fin de pipeline, permettant une retouche physiquement réaliste sur des valeurs RGB encodées linéairement auparavant, mais aussi de gérer la cohérence des couleurs à travers le mappage des tonalités, afin de préserver les teintes autant que possible et d’éviter les dépassements de gamut.

Enfin, il est possible de n’utiliser aucun flux de travail pour désactiver tous les modules automatiques et gérer votre pipeline manuellement.

**L’option « Utiliser la courbe de base » dans les préférences est donc supprimée, et il vous faudra redéfinir manuellement le flux de travail que vous souhaitez utiliser après avoir installé darktable 3.2.**

_Filmique_ évolue encore
======================

_Filmique_ a été créé pour darktable 2.6 dans l’objectif d’améliorer la robustesse de la couleur dans des scènes à large plage dynamique, par rapport à la _courbe de base_. Il vise à effectuer un mappage des tonalités et du gamut entièrement paramétrable par l’utilisateur, en quelques réglages (au lieu d’une courbe à 6-12 points obtenue par rétro-ingénierie des JPEG constructeur), en s’inspirant de la sensibilité de la pellicule. Une fonctionnalité similaire existe dans tous les logiciels de traitement d’image, photo (courbe de contraste), vidéo (LUT de prévisualisation ou transformations d’affichage OpenColorIO), et rendu 3D (filmique Blender et OpenColorIO), car le redimensionnement de plage dynamique entre media de capture et d’affichage est une contrainte commune à tous les arts graphiques.

Après avoir remis le nez dans des documentations de Kodak sur la sensitométrie argentique pour le module _docteur néga_, Aurélien a eu de nouvelles idées pour améliorer _filmique RVB_ :

1. une nouvelle science de la couleur pour gérer la « désaturation » des luminances extrêmes de façon plus progressive, en évitant notamment les cassures de bleus sur les ciels contrastés. L’idée est de rendre le spectre lumineux plus « pointu » (proche d’une lumière laser monochromatique) pour « saturer » ou plus « plat » (proche de la lumière blanche) pour « désaturer ». On passe donc à une approche plus physique et métaphorique de la saturation, qui n’a plus de lien direct avec la perception colorée, mais qui a l’avantage de se contrôler de façon plus progressive.
2. une stratégie de désaturation différente, qui force le blanc et le noir à une saturation nulle peu importent les réglages, mais qui autorise à l’inverse à resaturer les tons moyens, afin de contre-balancer l’effet du mappage de tonalité. Rappelons que l’objectif de cette désaturation est d’effectuer un mappage de gamut basique visant à assurer que le maximum et le minimum de luminance (conventionnellement appelés blanc et noir) soient bien achromatiques (donc un blanc… non coloré). Il est, en effet, impossible de représenter une couleur saturée dont la luminance serait 0 % ou 100 %, dans aucun espace de couleur disponible. Une telle couleur serait écrêtée de façon plus ou moins aléatoire, et produirait notamment des couchers de soleil jaune urine (ce qui veut dire que le rouge est écrêté). _Filmique_ produit donc une courbe de désaturation progressive qui assure une transition douce vers des couleurs achromatiques aux extrémités.
3. une reconstruction des hautes lumières basée sur l’exposition du blanc. En effet, en argentique couleur, en plus de désaturer les hautes lumières pour un mappage de gamut intégré, la chimie a tendance à flouter la transition entre les zones brûlées et les zones valides, par diffusion spatiale des espèces chimiques de la solution développante. Dans _filmique v3_, on manquait encore de douceur dans les transitions valide/écrêté, puisqu’il prenait en compte seulement la luminance des pixels, mais pas leur voisinage. _Filmique v4_ introduit donc une reconstruction des hautes lumières dans le domaine des ondelettes, donc multi-échelle, qui vise non seulement à adoucir les transitions valides/écrêté, mais aussi à essayer de récupérer les détails nets dans les canaux RVB non écrêtés (si possible), et à propager la couleur des zones voisines par diffusions successives (le processus est itératif et l’utilisateur peut régler le nombre d’itérations). L’utilisateur peut choisir les paramètres pour privilégier une reconstruction plus texturée (récupération des canaux non écrêtés) ou plus lisse (interpolation des hautes fréquences), plus colorée ou plus achromatique, et finalement plus nette (à la mode numérique) ou plus floue (comme le blooming argentique).
4. _filmique_ permet d’ajouter du bruit, en utilisant différents profils statistiques (gaussien, poissonien ou uniforme), dans les hautes lumières écrêtées (voir l’onglet « Options »). Ceci permet d’homogénéiser le bruit et de simuler de la texture dans les hautes lumières, afin d’éviter des hautes lumières reconstruites anormalement lisses par rapport au reste de l’image, tout ça dans le but de mieux fusionner les transitions visuelles entre hautes lumières écrêtées et reconstruites et tonalités valides. Ceci se rapproche encore du rendu de la pellicule argentique, qui présente du grain aussi dans les hautes lumières.
4. le réglage de gris de la scène disparaît par défaut, mais peut être optionnellement réactivé. Ceci répond à un besoin de simplification pour les utilisateurs suite à des incompréhensions de la différence entre l’exposition globale et le gris de la scène, sur le plan du résultat visuel (il n’y en a pas) et sur le plan de la chaîne de travail globale (attention, danger). La façon « canonique » d’utiliser _filmique_ est donc d’utiliser le module exposition pour pré-ajuster l’exposition (la luminosité) générale de l’image, puis d’utiliser _filmique_ seulement pour contraindre la plage dynamique de l’image dans la plage disponible du medium d’affichage. Dans cette configuration, la compression de plage dynamique se fait autour du gris moyen (conventionnellement fixé à 18 %), qui est la seule valeur non affectée par la transformation, préservant ainsi la luminosité globale. Ensuite, libre à vous de sortir de ces recommandations, mais il vous en coûtera une étape de plus pour achever de vous convaincre que ce n’est pas une bonne idée. Dans cette configuration, _filmique_ n’affecte plus la luminosité générale, mais seulement la compression des luminosités extrêmes.
5. Les réglages par défaut de _filmique_ sont ajustés par le logiciel en fonction du biais d’exposition stocké dans les métadonnées de la photo. Ainsi, pour les photographes numériques qui ont l’habitude d’exposer à droite de l’histogramme, en forçant une correction d’exposition manuelle sur le boîtier, pour protéger les hautes lumières de l’écrêtage (ce qui est la seule bonne façon d’exposer en numérique, n’en déplaise aux puristes qui ne comprennent pas les différences technologiques entre semi-conducteur photo-électrique et ions halogénures d’argent photo sensibilisés) auront leur pipeline relatif à la scène réglé automatiquement pour eux (en première approximation, car filmique ne peut toujours pas deviner quelle est la valeur du gris moyen exact pour une scène donnée).

_Filmique_ v3 reste toujours accessible via le dernier onglet de _filmique rvb_. Tout comme il est possible de mettre à jour une image de _filmique_ v3 vers v4 via le même onglet. Voici un aperçu du nouveau _filmique_ et la sélection de la version visible via le menu science couleur :

![filmique rvb v4](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/filmicv4-fr.png)

À noter : la reconstruction des hautes lumières est effectuée au moyen d’une décomposition en ondelettes par itération, ce qui induit une certaine pénalité de performance. Il est possible de désactiver complètement la reconstruction en réglant un seuil de hautes lumières très élevé, car le programme court-circuite la reconstruction si aucun pixel n’est détecté au-delà de ce seuil. Néanmoins, compte tenu de la difficulté de reconstruire des hautes lumières de façon convaincante, on peut considérer le compromis acceptable.

Il est aussi possible de désactiver, dans certains cas, le module par défaut de reconstruction des hautes lumières si _filmique_ reconstruit les hautes lumières, afin de préserver plus de détails. Pensez alors à piloter la désaturation des hautes lumières de façon à absorber les hautes lumières magenta que vous pourriez créer en désactivant ce module.

Autres améliorations
====================

Cette 3.2, à l’instar de la 3.0, est riche de nouveautés et évolutions. Cet article n’a pas vocation à être exhaustif mais à présenter les évolutions principales et à vous permettre de les appréhender. Vous trouverez ci-dessous, pêle-mêle, quelques autres améliorations à connaître.

## Une meilleure gestion du pipeline de traitement de l’image

Pour rappel, darktable 3.0 a instauré non seulement un nouvel ordre du pipeline de traitement mais également la possibilité de modifier l’ordre de ce pipeline en réordonnant les modules soi-même (fonction très avancée). De fait, certains utilisateurs se sont trouvés perdus et n’avaient pas de moyen de retrouver l’ordre par défaut de la 3.0 ou celui des versions 2.6.x et antérieures.

Ainsi, un nouveau module permanent a été ajouté en chambre noire (en bas sur le panneau de droite) intitulé _ordre des modules_. Ce module permet de vérifier quel ordre du pipeline est actuellement appliqué à l’image : 3.0, originel (ordre par défaut antérieur à la 3.0) et personnalisé (ordre personnel que vous avez défini, même involontairement). Ce même module vous permet donc d’appliquer le pré-réglage 3.0 ou originel si besoin mais également d’enregistrer un ordre personnalisé. Ce sont ces ordres que vous pourrez retrouver dans les nouveaux filtres de collection présentés plus haut dans cet article.

## Améliorations de performance et importantes corrections de bugs

Il a été remarqué que des bugs, parfois importants, sont présents dans la version 3.0.x (jusque dans la 3.0.2). Et tout particulièrement des bugs d’affichage d’images, notamment en cas de multiples instances (mais pas que). La plupart de ces bugs résultaient du nouvel ordre de traitement des images (pipeline), intégré en version 3.0. Une refonte complète du pipeline de traitement a été faite par Pascal Obry pour une gestion plus robuste du nouveau pipeline intégré en 3.0. Cette refonte rend ce dernier à la fois plus stable et plus performant.

La détection de modification des images a été améliorée. Cela permet surtout d’éviter de recalculer l’affichage d’une image qui n’aurait pas été modifiée, par exemple en ayant été ouverte en chambre noire sans aucune modification. La modification des XMP et vignettes en est ainsi plus fiable et impactée seulement en cas de réelle modification.

De nombreuses autres améliorations de performances ont été intégrées dans cette version 3.2, notamment dans certains modules. Ce travail est en cours puisque déjà plusieurs autres propositions d’améliorations de performances d’autres modules sont en cours pour intégration dans la future 3.4. Ainsi, la prochaine 3.4 semble se profiler sous de notables améliorations de performance.

darktable 3.2 instaure également une option automatique (paramétrable dans les préférences) de maintenance de la base de données, permettant de conserver une base de données plus saine dans la durée.

Enfin, avec les différentes améliorations de codes, beaucoup de parties similaires ont été unifiés, permettant par la suite une intégration plus rapide et facile de nouveaux modules ainsi qu’une bien meilleure cohérence sur les parties similaires (comme, par exemple, ce qui a été fait sur les pipettes, décrit plus haut).
À également été ajouté des outils de tests permettant aux développeurs de tester plus aisément les nouveaux ajouts et la rétrocompatibilité et stabilité de vos traitements d’images, notamment en cas de réécriture d’un module en vue de meilleures performances. 

Et bien évidemment, de nombreux bugs ont été corrigés, faisant de cette 3.2 la version 3 la plus stable à ce jour. Et très nettement. Si vous utilisez déjà une version 3.0.x, je ne peux que vous recommander la mise à jour vers cette 3.2, ne serait-ce que pour sa stabilité supérieure.

## De nouvelles options dans les préférences

En dehors des nouveaux flux de travail (workflows) présentés plus haut et des quelques préférences déjà présentées, vous trouverez quelques nouvelles options de préférences qui peuvent être bien utiles. Voici les principales :

- En table lumineuse, vous pouvez trier les pellicules par numéro ou par dossier. Suite à la refonte de la table lumineuse, vous pouvez également définir les catégories de tailles (via séparateurs de catégories de tailles) différentes qui permettront notamment de définir un mode de surimpression différent selon la taille des vignettes. La taille se spécifie en pixels et la taille des vignettes s’affiche dans le menu de sélection du mode de surimpression présenté plus haut.

- En chambre noire, il est désormais possible de réduire la résolution de la pré-visualisation, permettant de réduire la mobilisation du processeur utilisé et un gain possible de performances.
**_Attention :_** comme indiqué dans l’info-bulle de cette option, cela peut réduire un peu la précision des masques guidés.

- Dans l’onglet divers, des options pour gérer les raccourcis clavier en cas d’instances multiples.

- L’onglet raccourcis voit, enfin, un champ de recherche permettant de plus rapidement trouver le raccourci que vous souhaitez personnaliser.

Et enfin, un nouvel onglet d’options lua qui, à ce jour, ne comporte qu’une option permettant d’afficher/masquer l’installateur de scripts lua, présenté ci-dessous.

À noter que les préférences modifiées sont enregistrées dynamiquement. La fermeture des préférences maintient donc les préférences modifiées.

## Installateur du gestionnaire de scripts Lua

Bill Ferguson, qui s’occupe de la gestion des scripts Lua, avait fait un script Lua pour gérer (activer/désactiver) les scripts Lua beaucoup plus facile à utiliser que cette méthode : [Installation scripts Lua](https://darktable.fr/2018/03/installation-des-scripts-lua-sous-linux/). J’avais présenté cette nouvelle méthode : [script-manager](https://darktable.fr/2018/08/nouveau-script-pour-gerer-les-lua/). Toutefois, l’installation du gestionnaire de scripts (script manager) Lua se faisait toujours manuellement.

Tout ceci est désormais de l’histoire ancienne. L’auteur vient d’inclure, directement dans darktable, un installateur lua. Celui-ci peut être activé ou désactivé au premier démarrage et, si besoin, ultérieurement, dans les préférences. L’installateur télécharge les derniers scripts disponibles depuis le dépôt.

Bien entendu, ceci n’est que pour ceux n’ayant pas déjà le script manager installé. Voici à quoi ressemble ce nouvel installateur :

![Installateur scripts lua](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/lua-scripts-installer.png)

Pour les non-anglophones, cet installateur vous propose simplement trois options :

- installer les scripts (install scripts), en incluant l’ajout du gestionnaire de scripts (script manager) dans darktable.
- me le rappeler plus tard (remind me later)
- ne plus le montrer (don’t show again)

Une fois installé, le script manager apparaît donc à gauche sur la table lumineuse :
![script-manager](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/script-manager-en.png)

À noter également que, malheureusement, les scripts lua ne sont pas traduisibles et sont donc intégralement en anglais.

## Un histogramme ajustable et un nouveau mode : parade RVB

Deux nouveautés sur l’histogramme dans darktable 3.2. La première est l’ajustement en hauteur de la taille de l’histogramme. Cet ajustement se fait très simplement et de la même manière que plusieurs modules de la table lumineuse. Pointez le curseur sur l’histogramme puis `Ctrl` + `défilement` ; et ajustez sa hauteur comme vous le souhaitez.

Un nouveau mode, parade RVB, fait son apparition et affiche des formes d’ondes qui représente les niveaux de chaque couche (rouge, vert et bleu). Ce mode permet donc de visualiser comment sont distribuées les composantes de couleur d’une partie de l’image.

Ce mode s’affiche en sélectionnant l’affichage de l’histogramme en mode d’onde (via l’icône en haut à gauche sur l’histogramme) puis en changeant le mode d’onde via le bouton situé tout juste à droite vers ce mode Parade RVB.

![Mode parade RVB](https://raw.githubusercontent.com/Nilvus/dtorg/93d487046710633be46a130566f1484f8b2d4f8a/content/blog/2020-08-10-darktable-3.2/en/rgb-parade.png)

Ajoutez à tout cela, une réécriture importante du code de l’histogramme pour de meilleures performances.

## Masque dessiné : courber la forme gradient

Lors de l’ajout d’un masque dessiné, il est désormais possible de courber la forme gradient (dégradé). Pour cela, pointer le curseur de la souris sur la barre du gradient et faire un défilement molette (ou pavé tactile) vers le haut ou le bas, selon la courbure souhaitée. `Ctrl` + `défilement` permet de définir l’opacité et `Maj` + `défilement` gère la dureté.

## Un historique amélioré

Le fonctionnement de l’historique a été amélioré selon différentes remontées d’utilisateurs. Ainsi, lors de la compression de l’historique ou du chargement d’une nouvelle image, l’historique se comportera désormais de cette manière :

- tout module actif et qui ne peut être désactivé, apparaît systématiquement en premier dans la pile historique
- tout module qui est activé par défaut mais qui peut être désactivé, apparaît ensuite dans la pile historique
- enfin, tous les modules activés par des préréglages ou à la suite d’un réglage de préférence (flux de travail ou netteté sélectionné dans les préférences) sont ajoutés

## Mais encore

- ajout du support du format de fichier AVIF (>= 0.7). Cela requiert d’avoir la librairie [libavif](https://github.com/AOMediaCodec/libavif) installée ;
- ajout d’une option d’export en échelle de gris pour les images monochromes en TIFF ;
- l’export des masques est désormais possible sur les images au format TIFF ;
- il est désormais possible d’utiliser plus de 500 images en vue capture, notamment pour les time-lapse ;
- l’application d’un style peut désormais aussi bien être appliqué en mode _empiler_ (ajouté à l’historique existant de l’image) ou en mode _écraser_ (en remplacement de l’historique existant de l’image). Ceci rend son usage cohérent avec le module _développement_.
- plusieurs styles peuvent être sélectionnés en même temps afin de pouvoir les gérer (les supprimer, exporter, etc.) plus rapidement.
- l’orientation d’une image faite depuis la table lumineuse ne pouvait pas être annulée ou refaite. C’est désormais possible via les traditionnels raccourcis `Ctrl` + `Z` et `Ctrl` + `Y`.
- en utilisant `Ctrl` + `clic` sur les formes de masques, il est possible de permettre la création en continue de plusieurs formes similaires.
- le rejet d’une image conserve en mémoire le nombre d’étoiles précédemment défini. En cas d’annulation du rejet, l’image retrouve ainsi directement le nombre d’étoiles défini.

Cette liste n’est pas exhaustive. Quelques autres améliorations mineures peuvent être découvertes via les notes de sortie de darktable (release notes) ici : https://github.com/darktable-org/darktable/releases/tag/release-3.2.0

Une future 3.4 en chemin
========================

Comme déjà précisé plus haut, une deuxième version majeure, 3.4, est prévue pour Noël. Cette version se profile déjà sous l’amélioration de performances. Elle devrait également voir l’arrivée d’un nouveau module de mixeur de canaux, plus performant, efficace et intégrant une balance des blancs moderne utilisant au choix la transformée de Bradford, l’espace CIECAT16, et munie d’une détection de balance des blancs par apprentissage machine supervisé.

Une refonte visuelle du module retouche est également en cours ainsi que de la balance des blancs. Des discussions et propositions sont également en cours afin d’améliorer la gestion des modules en chambre noire (réorganisation des onglets, amélioration des pré-réglages, etc.).

Et très certainement, d’autres surprises en vue.

À propos de cet article
=======================

Cet article est sous les termes de la licence [Attribution 2.0 générique (CC BY 2.0)](https://creativecommons.org/licenses/by/2.0/deed.fr) ou, selon, de la [licence Creative Commons BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/deed.fr).

**Article co-écrit par :** [Nilvus](https://github.com/Nilvus), [aurelienpierre](https://aurelienpierre.com/), [jpg54](https://www.flickr.com/photos/113336874@N07/), hgmarty, [jpv](http://jpverrue.fr/) et [Pascal Obry](http://photos.obry.net)
Et merci également aux lecteurs/correcteurs de passage.
