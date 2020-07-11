URL:     https://linuxfr.org/redaction/news/darktable-3-2-l-effet-confinement
Title:   darktable 3.2 : l'effet confinement !
Authors: Nilvus
         jpg54, jpv, hgmarty, aurelienpierre, JM40, play0ad, zakfm et Ysabeau
Date:    2020-06-03T18:12:15+02:00
License: CC By-SA
Tags:    darktable, photographie et raw
Score:   0


Comme ne le veut pas la tradition, pour la première fois de son histoire, darktable voit sa nouvelle version majeure 3.2, sortir quelques mois plus tôt, en plein été. Le confinement de cette année, déjà bien particulière, a entraîné un nombre record de contributions et d’améliorations sur darktable 3. Cerise sur le gâteau, une version majeure, 3.4, est toujours programmée pour Noël. 2020 sera donc la première année où l’équipe darktable aura le plaisir de vous proposer deux versions majeures.

----


----

Une interface affinée, dans les moindres détails : pour un look professionnel
=============================================================================



L’interface a connu un profond changement via la 3.0. L’équipe darktable a peaufiné ce travail jusque dans les moindres détails. Ainsi, darktable 3.2 vous apporte une interface et de nouveaux apports améliorant encore plus l’expérience utilisateur. Le style 3.0 perdure mais s’améliore… pour un look plus professionnel. Plusieurs développeurs ont travaillé d’arrache-pied pour vous apporter une interface soignée, à commencer par une réécriture complète de la table lumineuse qui s’accompagne également de belles améliorations de performance.


Les améliorations de l’interface sont nombreuses, certaines seront détaillées plus bas, comme la refonte des préférences, les boutons dynamiques ou les bulles d’aide, ou encore le plus gros morceau, à savoir le remaniement en profondeur de la table lumineuse.


J’ai profité des mes contributions CSS, à ce travail sur l'interface, pour restructurer complètement le CSS, afin de le rendre plus clair à la lecture. Ainsi, il est plus aisé, à l’appui par ailleurs de plus de commentaires, de repérer la partie qu'on souhaite personnaliser sur l’interface. Vous pourrez d’autant mieux en saisir l’utilité en découvrant plus bas les nouvelles préférences proposées par darktable 3.2.

Enfin, la cohérence de l’interface entre les différents thèmes a également été drastiquement améliorée par ce travail d'optimisation du CSS.

## Table lumineuse : un remaniement en profondeur sur tous les plans



La table lumineuse est certainement la partie qui a le plus évoluée. Grâce, notamment, au travail majeur d’AlicVB (Aldric Renaudin), la table lumineuse est tout simplement plus performante. La vitesse d’affichage est notable, particulièrement sur des configurations un peu plus anciennes. Le bandeau d'images bénéficie également d'une refonte et d'améliorations de performance.

Aldric a également intégré de nouvelles options de surimpression des informations des vignettes, applicable indépendamment dans chacun des modes existants (table lumineuse zoomable, navigateur de fichier, sélection, aperçu et bandeau d’images). Désormais, en cliquant sur l’icône étoile en haut à droite, vous découvrirez un menu proposant ces nouvelles options d’affichage des vignettes, incluant sept modes d’affichage des informations (étoiles, icônes groupe, développement, labels couleurs, informations). Une option permet également d’afficher ou non les bulles d’aides en survolant les vignettes. Ces bulles d’aide sont personnalisables dans les préférences.
**_Attention :_** même en sélectionnant l’affichage des bulles d’aide, il se peut que rien ne s’affiche, si le champ dans les préférences permettant de les personnaliser est vide (voir pour cela, l'onglet table lumineuse des préférences puis le champ patron pour les infos bulles des miniatures).

![Menu popover de sélection des modes de surimpression](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/popover-overlays-fr.png)


Les sept nouveaux modes de surimpression des vignettes, permettent d’aller d’un mode qui n’affiche que l’image à un mode complet étendu en passant par des modes qui affichent certaines informations seulement au survol de la souris. Voici un aperçu de certains modes, à commencer par une vue globale de l'interface peaufinée, en mode de surimpression n° 6 (ligne sélectionnée ci-dessus). Ce mode affiche donc en permanence certaines infos et les infos étendues (nom du fichier de l'image et infos principales) au survol de la souris.

![Mode de surimpression permanent et étendu au survol de la souris](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/lighttable-mode6-fr.png)


Les 2 premiers modes sont très proches. Par défaut, ils n'affichent aucun information autour des images. Seul le 2ème mode ajoutera l'affichage de certaines informations au survol de la souris. Voir ci-dessous :


![surimpression lors du survol souris](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/overlays-on-mouse-hover.png)


Le mode le plus détaillé par défaut pour les vignettes, est le cinquième (surimpressions étendues permanentes) et ressemble à cela :


![surimpressions étendues permanentes](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/permanent-extended-overlays.png)

Enfin, le septième et dernier mode a été particulièrement créé pour être adapté aux modes sélection et aperçu (et celui appliqué par défaut à ces modes). Ce mode permet de personnaliser la durée d’affichage, au survol par le curseur de l’image, de 3s par défaut à -1 pour un affichage permanent. Dans tous les cas, cet affichage ne se fait que si l’image est survolée par le curseur. Enfin, ce nouveau mode permet d'afficher le niveau de zoom de l'image dans les modes sélection et aperçu.

![Bloc de superposition en mode aperçu et sélection](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/block-overlays-fr.png)


Les autres modes sont intermédiaires à ceux présentés ici et si vous voulez les découvrir, installez et ouvrez darktable 3.2. Rien ne vaut mieux que de les tester tous vous-même.

Le bandeau d’images, qui peut être affiché via Ctrl+f en bas de certaines vues (_chambre noire_, modes _sélection_ et _aperçu_, vue _carte_ ou _impression_…) permet également d’être affiné par ces nouveaux modes d’affichage. Dans les vues où ce bandeau est affiché, c’est toujours via l’icône étoile que vous pourrez personnaliser l’affichage. Ainsi, par exemple, en _chambre noire_, l’icône étoile n’est utilisable que si le bandeau images est affiché et le menu n’est donc applicable que pour le bandeau. Autre exemple, en mode _sélection_, si le bandeau d’images est affiché, le menu « étoile » permettra donc de personnaliser et la vue _sélection_ et l’affichage des vignettes du bandeau.


À noter également que le bandeau d’images voit la visualisation de l’image (ou des images en vue sélection) améliorée. Cet affichage était plutôt confus jusque-là. Désormais la sélection est bien plus visible. Voyez plutôt :


![Sélection image du bandeau images](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/select-image-filmstrip.png)


## Refonte des préférences : pour mieux s’y retrouver



Avec l’introduction des nouvelles fonctionnalités depuis la 3.0, les préférences ont été réorganisées, augmentant le nombre d’onglets, afin d’offrir une lisibilité plus importante. Un des objectifs a par ailleurs été d’éviter les longs défilements pour accéder à une option. Ainsi, chaque onglet ne fait pas plus d’une page (sauf l’onglet pré-réglage). Chaque onglet a de plus un nom qui décrit clairement les options qui y sont paramétrables.



Parce que des captures d’écran en parlent mieux, voici deux exemples d’onglet pour montrer cette refonte très efficace :


![Préférences darktable v3.2, vue général](https://raw.githubusercontent.com/hgmarty/images-dt/master/preferences(fr).png)



Comme vous pouvez le voir sur cette image, de nouvelles options d’interface sont également apparues. Il est désormais possible, soit d’utiliser la police (ou taille de police si le thème utilisé est un thème élégant), comme auparavant, soit de personnaliser la taille de la police directement depuis darktable. Une option demandée depuis un bon moment, enfin là !



D’autres options permettant d’affiner aussi la taille de l’ensemble des éléments de l’interface au bon vouloir de l’utilisateur. Attention, à rester raisonnable sur ces options DPI. Les options par défaut restant recommandées pour la majorité des utilisateurs.



Enfin, le développeur ayant fait cette refonte a intégré la possibilité, directement depuis les préférences, de personnaliser l’affichage de l’interface en intégrant vos propres personnalisations CSS, comme vous pouvez le voir sur la capture d’écran.


![Préférences darktable v3.2, vue traitement](https://raw.githubusercontent.com/hgmarty/images-dt/master/preferences-traitement(fr).png)


## Boutons dynamiques : selon vos actions



Un développeur darktable a intégré une nouvelle fonction, surtout visuelle mais aussi bien pratique. Et cette fonction n’est autre que le fait d’avoir, en table lumineuse, des boutons dynamiques. Mais de quoi il me parle l’auteur ici ? Eh bien, pour illustrer, rien de plus simple, ouvrez un module à droite de la table lumineuse, par exemple, images sélectionnées. Selon la position du curseur et la sélection faite (ou pas de sélection, vous verrez que certains boutons deviennent cliquables et d’autres non.



Les boutons dynamiques, c’est tout simplement l’affichage des boutons selon qu’ils sont utilisables ou non dans le contexte actuel.



Un autre exemple, sélectionnez une image, ouvrez le module développement et cliquez sur copier. Tant que vous restez sur l’image sélectionnée, coller n’est pas utilisable (aucun intérêt de coller le développement d’une image sur elle-même). Sélectionnez maintenant une autre image et coller devient utilisable.



Quelques autres détails
-----------------------



**Bulles d’aides améliorées**



Les bulles d’aides ont été améliorées. En effet, les bulles d’aides ont parfois le défaut de s’afficher là où on ne veut pas. Malheureusement ce problème ne peut pas être corrigé par l’équipe darktable puisque c’est un défaut inhérent à la librairie graphique utilisée par darktable, à savoir Gtk+. Pour contourner cela autant que possible, l’équipe darktable a intégré deux choses (après de longs débats) :



- la possibilité d’afficher/masquer les bulles d’aide à tout moment via un simple raccourci : maj+t
- un affichage des bulles d’aide visuellement amélioré (légèrement)


**Une nouvelle ligne de comparaison d'instantanées et la coloration de l'affichage sur image**


darktable 3.2 apporte aussi quelques améliorations visuelles sur l'image en chambre noire. La ligne de comparaison d'un instantané avec la ligne d’historique comparée est plus visible, intégrant un repère visuel de l'instantané sélectionné (une flèche avec le symbole S pour snapshot).

Vous trouverez également une nouvelle option en bas à droite, via une icône quadrillée rouge et verte, permettant de choisir la couleur d'affichage de cette ligne d'instantanée ainsi que tout élément visuel qui s'afficherait sur l'image, comme par exemple les éléments de sélection de masque dessiné. Six couleurs sont disponibles (gris, rouge, vert, jaune, cyan et magenta).


Voir ci-dessous un exemple de la nouvelle ligne de comparaison d'instantané en rouge et l’icône de sélection de couleur entourée en rouge.

![instantané et option couleur](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-release/content/blog/2020-08-10-darktable-3.2/en/overlay-darkroom-color.png)

**Raccourcis (sélection d’images dans le bandeau d’images…)**



**Mais encore :**

Plusieurs icônes ont été redessinées, des quatre icônes en haut à droite (groupe, étoile, aide et préférences) en passant par les icônes de masques. Ce travail permet un bien meilleur affichage particulièrement sur les écrans HiDPI (haute résolution) sous Windows et donc une meilleure cohérence d'affichage selon le type d'écran (LoDPI (basse résolution ou HiDPI (haute résolution)).

Le sélectionneur de fichiers a également été revu.

La barre de progression d'export et d'impression a été visuellement revue pour une intégration visuelle plus fine à l'interface.


En chambre noire, le module actif est signalé par un nouvel effet visuel sur l'icône de statut et le titre du module (voir la capture d'écran de filmique v4, dans la présentation de cette nouvelle version, plus bas dans l'article.

Gestion du patrimoine numérique
===============================



##Un éditeur de métadonnées qui évolue



##De nouveaux filtres de collection
Sept nouveaux filtres s’ajoutent aux nombreux déjà existants. darktable est déjà très riche en filtres sur les méta données des photos (données EXIFS et données IPTC/XMP). Par contre très peu de filtres existaient sur les divers événements ou traitements propres à darktable. Vous connaissiez déjà les filtres **pellicule**, **mot-clé** et **copie locale**. La version 3.2 ajoute maintenant les nouveaux filtres suivants : **historique**, **module**, **ordre des modules**, **date importation**, **date traitement**, **date exportation** et **date impression**. Voici une description rapide du rôle de ces nouveaux filtres.


* **historique** - Permet de sélectionner les photos développées ou les photos non développées.
* **module** - Permet de sélectionner les photos dont la pile de développement contient un module précis (Tous les modules utilisés au moins une fois sont présentés).
* **ordre des modules** - Permet de sélectionner les photos traitées avec un ordre de modules précis (tous les ordres de modules existants sont présentés).
* **date importation** - Permet de sélectionner les photos importées à un horodatage précis (horodatage = date et heure). Tous les horodatages de la collection sont présentés.
* **date traitement** - Permet de sélectionner les photos traitées à un horodatage précis. Tous les horodatages de la collection sont présentés.
* **date exportation** - Permet de sélectionner les photos exportées à un horodatage précis. Tous les horodatages de la collection sont présentés.
* **date impression** - Permet de sélectionner les photos imprimées à un horodatage précis. Tous les horodatages de la collection sont présentés.


##De nouvelles informations sur l’image.
Le module informations de l’image affiche également de nouvelles informations Les quatre horodatages mentionnés ci-dessus : **date importation**, **date traitement**, **date exportation** et **date impression**, ainsi qu’une nouvelle information EXIF : le **biais d’exposition**.


La fenêtre du module est plus petite, mais elle est maintenant scrollable et redimensionnable avec ctrl+molette.



Nouveaux flux de travail par défaut
===================================



Le conflit de fonctionnalité entre filmique et la courbe de base, pour fournir la nécessaire transformation de tons du RVB linéaire vers le RVB écran, était jusqu’à présent gérée via une option, dans les préférences, qui permettait d’activer par défaut la courbe de base, ou pas. Cependant, rien n’était disponible pour activer filmique automatiquement. C’est désormais réglé avec les flux de travail par défaut, disponibles dans les préférences à l’onglet traitement. 



Le flux « relatif à l’affichage », utilisé par défaut, active automatiquement la courbe de base et ordonne les modules dans le pipeline tels qu’ils étaient pour darktable 2.6 et précédents. À ce titre, il va appliquer la transformation non-linéaire au début du pipeline, et toute la retouche sera ensuite effectuée sur du RGB non-linéaire, comme le font la quasi-totalité des logiciels de retouche photo. Le seul mérite de ce flux de travail est qu’il correspond à ce à quoi beaucoup de photographes sont habitués, mais il va poser de nombreux problèmes de cohérence des couleurs et de crédibilité de certains filtres locaux (flou ou accentuation de netteté), notamment dans les scènes à large dynamique.


Le flux « relatif à la scène ».


Filmique évolue encore
======================



Après avoir remis le nez dans des documentations de Kodak sur la sensitométrie argentique pour le module négadoctor, Aurélien a eu de nouvelles idées pour améliorer filmique RGB :



1. une nouvelle science de la couleur pour gérer la « désaturation » des luminances extrêmes de façon plus progressive, en évitant notamment les cassures de bleus sur les ciels contrastés. L’idée est de rendre le spectre lumineux plus « pointu » (proche d’une lumière laser monochromatique) pour « saturer » ou plus « plat » (proche de la lumière blanche) pour « désaturer ». On passe donc à une approche plus physique et métaphorique de la saturation, qui n’a plus de lien direct avec la perception colorée, mais qui a l’avantage de se contrôler de façon plus progressive.
2. une stratégie de désaturation différente, qui force le blanc et le noir à une saturation nulle peu importent les réglages, mais qui autorise à l’inverse à resaturer les tons moyens, afin de contre-balancer l’effet du mappage de tonalité. Rappelons que l’objectif de cette désaturation est d’effectuer un mappage de gamut basique visant à assurer que le maximum et le minimum de luminance (conventionnellement appelés blanc et noir) soient bien achromatiques (donc un blanc… non coloré). Il est, en effet, impossible de représenter une couleur saturée dont la luminance serait 0 % ou 100 %, dans aucun espace de couleur disponible. Une telle couleur serait écrêtée de façon plus ou moins aléatoire, et produirait notamment des couchers de soleil jaune urine (ce qui veut dire que le rouge est écrêté). Filmique produit donc une courbe de désaturation progressive qui assure une transition douce vers des couleurs achromatiques aux extrémités.
3. une reconstruction des hautes lumières basée sur l’exposition du blanc. En effet, en argentique couleur, en plus de désaturer les hautes lumières pour un mappage de gamut intégré, la chimie a tendance à flouter la transition entre les zones brûlées et les zones valides, par diffusion spatiale des espèces chimiques de la solution développante. Dans filmique v3, on manquait encore de douceur dans les transitions valide/écrêté, puisqu’il prenait en compte seulement la luminance des pixels, mais pas leur voisinage. Filmique v4 introduit donc une reconstruction des hautes lumières dans le domaine des ondelettes, donc multi-échelle, qui vise non seulement à adoucir les transitions valide/écrêté, mais aussi à essayer de récupérer les détails nets dans les canaux RGB non écrêtés (si possible), et à propager la couleur des zones voisines par diffusions successives (le processus est itératif et l’utilisateur peut régler le nombre d’itérations). L’utilisateur peut choisir les paramètres pour privilégier une reconstruction plus texturée (récupération des canaux non écrêtés) ou plus lisse (interpolation des hautes fréquences), plus colorée ou plus achromatique, et finalement plus nette (à la mode numérique) ou plus floue (comme le blooming argentique).
4. le réglage de gris de la scène disparaît par défaut, mais peut être optionnellement réactivé. Ceci répond à un besoin de simplification pour les utilisateurs suite à des incompréhensions de la différence entre l’exposition globale et le gris de la scène, sur le plan du résultat visuel (il n’y en a pas) et sur le plan de la chaîne de travail globale (attention, danger). La façon « canonique » d’utiliser filmique est donc d’utiliser le module exposition pour pré-ajuster l’exposition (la luminosité) générale de l’image, puis d’utiliser filmique seulement pour contraindre la plage dynamique de l’image dans la plage disponible du medium d’affichage. Dans cette configuration, la compression de plage dynamique se fait autour du gris moyen (conventionnellement fixé à 18 %), qui est la seule valeur non affectée par la transformation, préservant ainsi la luminosité globale. Ensuite, libre à vous de sortir de ces recommandations, mais il vous en coûtera une étape de plus pour achever de vous convaincre que ce n’est pas une bonne idée.
5. Les réglages par défaut de filmique sont ajustés par le logiciel en fonction du biais d’exposition stocké dans les métadonnées de la photo. Ainsi, pour les photographes numériques qui ont l’habitude d’exposer à droite de l’histogramme, en forçant une correction d’exposition manuelle sur le boîtier, pour protéger les hautes lumières de l’écrêtage (ce qui est la seule bonne façon d’exposer en numérique, n’en déplaise aux puristes qui ne comprennent pas les différences technologiques entre semi-conducteur photo-électrique et ions halogénures d’argent photo sensibilisés) auront leur pipeline relatif à la scène réglé automatiquement pour eux (en première approximation, car filmique ne peut toujours pas deviner quelle est la valeur du gris moyen exact pour une scène donnée).


Filmique v3 reste toujours accessible via le dernier onglet de _filmique rvb_. Tout comme il est possible de mettre à jour une image de filmique v3 vers v4 via le même onglet. Voici un aperçu du nouveau filmique et la sélection de la version visible via le menu science couleur :

![filmique rvb v4](https://raw.githubusercontent.com/Nilvus/dtorg/3.2-fr-images/content/blog/2020-10-08-darktable-3.2/fr/filmicv4-fr.png)

Un nouveau module : docteur néga
================================


Le module actuel d’inversion de négatifs argentiques possède un défaut majeur : il fonctionne obligatoirement sur le signal non-dématricé du capteur, si le négatif a été numérisé avec un appareil photo numérique, et donc obligatoirement avant le profil de couleur d’entrée, quoi qu’il arrive. Ceci implique deux problèmes insolubles :



1. si le fichier numérique provient d’un vrai scanner, et qu’il est encodé avec une fonction de transfert (le « gamma »), celui-ci n’est pas annulé avant l’inversion. Suivant le type de numérisation que vous travaillez (« RAW » en 16 bits linéaire d’un scanner de film spécialisé, ou scan JPEG 8 bits encodé en gamma d’un scanner grand public), vous n’aurez pas du tout le même comportement. Notez que si la numérisation est faite à partir d’un autre appareil, le signal est linéaire, donc le problème ne se pose pas ici.
2. on inverse la couleur avant de corriger l’espace de couleur du scanner ou de l’appareil numérique, ce qui fait que les profils de couleurs deviennent alors faux (il faudrait les inverser eux aussi), et qu’on ne peut pas soustraire la déviation colorimétrique du capteur de scan proprement.



Il s’ensuit donc de fastidieuses séances de rattrapage de couleur, utilisant différents modules pour rattraper à la main ce qui aurait dû être fait par le profil de couleur d’entrée s’il avait été appliqué au bon moment.



Négadoctor règle ça, et bien d’avantage, en se basant sur le système de densitométrie Kodak Cineon, développé dans les années 1990 pour numériser les bobines de films au cinéma.



Depuis l’avènement de la photo numérique, beaucoup de photographes argentiques aimeraient bien retrouver leurs anciennes photos dans leur workflow numérique. Plusieurs méthodes existent :



* les faire digitaliser par un professionnel mais pour en avoir avec une bonne résolution coûte relativement cher ;
* les digitaliser soi-même avec un scanner de films : les scanners bas de gamme ne digitalisent pas à plus de 10 Mpx et généralement ne proposent que le format JPEG avec une bonne perte des possibilités de post-traitement ; les scanners haut de gamme proposent des résolutions un peu supérieures et le format Tiff en 16 bits meilleurs pour le post-traitement, par contre, ils sont très lents pour obtenir des résolutions élevées et nécessitent d’utiliser son ordinateur : ces scanners proposent d’inverser directement les négatifs à partir de leur logiciel



Et pourquoi ne pas utiliser son APN avec un système de prise de vue macro pour reprographier ses négatifs argentiques et d’utiliser darktable pour faire ce travail ?
Depuis longtemps, je cherchais une méthode efficace pour digitaliser mes anciennes photos et j’en ai essayé plusieurs.
J’utilise un scanner relativement bon marché Reflecta X-10 qui travaille sans l’ordinateur et sort des JPeg de 14 MP qui remplace mon ancien Rollei DF-S 190 SE qui m’a lâché et me donnait des JPEG très corrects. Ce scanner me sert de visionneuse de négatifs pour faire une sélection des photos que je veux en très bonne qualité.
Aurélien Pierre m’a prêté son PrimeFilmXE (reflecta scanner proscan 10t), j’ai eu du mal à trouver de bons réglages dans le logiciel fourni qui fonctionne sous Windows. En essayant de traiter les négatifs avec darktable, il était difficile de trouver facilement à traiter ces scans. Après des recherches sur le Net, il a eu l’idée de développer un module pour améliorer ce traitement des négatifs surtout couleur.
J’utilise donc un Lumix Gx8 (20 MP en RAW) avec un Leica Elmarit f:2.8 de 45mm macro pour digitaliser mes photos argentiques : négatifs N/B et couleur et diapos N/B et couleur.
Les diapositives ne posent aucun problème de traitement avec darktable.
Les négatifs N/B sont relativement simples à inverser et la plupart des logiciels proposent cette inversion.
Pour les négatifs couleur, pour les logiciels qui le permettent, il faut un échantillon du film non exposé pour récupérer les valeurs du filtre orangé pour le retirer du négatif exposé.



Négadoctor permet de traiter les négatifs N/B et couleur : le module propose de traiter des négatifs couleurs par défaut :
![negadoctor](https://raw.githubusercontent.com/jpg54/dtorg/8e7b5db86e11dfd830b433b1652fc40b00a55982/negadoctor%20FR.png)


Un sélecteur permet de passer au négatif N/B :
![selecteur couleur - N/B](https://raw.githubusercontent.com/jpg54/dtorg/8e7b5db86e11dfd830b433b1652fc40b00a55982/negadoctor%20selection%20N-B%20Couleur%20FR.png)


En ouvrant un négatif argentique N/B :
![Ouverture N/B](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20FR.png)


Vous n’avez qu’à cliquer sur « noir et blanc » à la place de « couleur » pour inverser le négatif :
![Inversion par défaut](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20defaut%20FR.png)


J’ai toujours tiré mes négatifs sur du papier tons chauds et je me suis fait un pré-réglage pour renforcer le contraste que je trouve faible à l’ouverture par défaut :
![Inversion tons chauds](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20Tons%20Chauds%20FR.png)


et j’ai fait des réglages dans l’onglet « corrections » pour obtenir :
![Corrections pour obtenir les tons chauds](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20%20correction%20FR.png)


L’onglet « impression » permet d’ajuster en fonction du papier utilisé ou du système de reproduction :
![Impression](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20N_B%20Impression%20FR.png)

Pour le traitement d’un négatif couleur :
![negadoctor couleur](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20couleur%20FR.png)


il suffit d’activer negadoctor (le filtre orangé va être neutralisé avec la valeur par défaut) :
![Inversion par défaut](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20couleur%20positif%20FR.png)


Et après avoir fait quelques corrections :
![Inversion corrigée](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/negadoctor%20couleur%20positif%20Corr%20FR.png)

Autres améliorations
====================



### Améliorations de performance et importantes corrections de bugs


Il a été remarqué que des bugs, parfois importants, sont présents dans la version 3.0.x (jusque dans la 3.2). Et tout particulièrement des bugs d'affichage d'images, notamment en cas de multiples instances (mais pas que). La plupart de ces bugs résultaient du nouvel ordre de traitement des images (pipeline), intégré en version 3.0. Une refonte complète a été faite par Pascal Obry du pipeline de traitement pour une gestion plus robuste du nouveau pipeline intégré en 3.0. Cette refonte rend le pipeline 3.0 à la fois plus stable et plus performant.


De nombreuses autres améliorations ont été intégrés dans cette version 3.2, notamment dans certains modules. Ce travail reste un travail en cours puisque déjà plusieurs autres propositions d'améliorations de performances d'autres modules sont en cours pour intégration dans la future 3.4. Ainsi, la prochaine 3.4 semble se profiler sous de notables améliorations de performance.


Et bien évidemment, de nombreux bugs ont été corrigés, faisant de cette 3.2 la version 3 la plus stable à ce jour. Et très nettement. Si vous utilisez déjà une version 3.0.x, je ne peux que vous recommander la mise à jour vers cette 3.2, ne serait-ce que pour sa stabilité supérieure.

### De nouvelles options dans les préférences


En dehors des nouveaux flux de travail (workflows) présentés plus haut et des quelques préférences déjà présentées, vous trouverez quelques nouvelles options de préférences qui peuvent être bien utiles. Voici les principales :


- En table lumineuse, vous pouvez trier les pellicules par numéro ou par dossier. Suite à la refonte de la table lumineuse, vous pouvez également définir les catégories de tailles (via séparateurs de catégories de tailles) différentes qui permettront notamment de définir un mode de surimpression différent selon la taille des vignettes. La taille se spécifie en pixels et la taille des vignettes s'affiche dans le menu de sélection du mode de surimpression présenté plus haut.


- En chambre noire, il est désormais possible de réduire la résolution de la pré-visualisation, permettant de réduire la mobilisation du processeur utilisé et un gain possible de performances.
**_Attention :_** comme indiqué dans la bulle d'aide de cette option, cela peut réduire un peu la précision des masques.


- Dans l’onglet divers, des options pour gérer les raccourcis clavier en cas d'instances multiples.

- L'onglet raccourcis voit, enfin, un champ de recherche permettant de plus rapidement trouver le raccourci que vous souhaitez personnaliser.

Et enfin, un nouvel onglet d’options lua qui à ce jour, ne comporte qu’une option permettant d'afficher/masquer l’installateur de scripts lua, présenté ci-dessous.


A noter que les préférences modifiées sont enregistrées dynamiquement. La fermeture des préférences maintient donc les préférences modifiées.

### Installateur Lua



Bill Ferguson avait fait un script Lua pour gérer (activer/désactiver) les scripts Lua beaucoup plus facile à utiliser que cette méthode : [Installation scripts Lua](https://darktable.fr/2018/03/installation-des-scripts-lua-sous-linux/)
J’avais présenté cette nouvelle méthode : [script-manager](https://darktable.fr/2018/08/nouveau-script-pour-gerer-les-lua/) et aussi [script-manager](https://darktable.fr/2016/09/un-gestionnaire-de-scripts-lua/). script-manager.lua dysfonctionnait depuis la version 3.0.

Tout ceci est désormais de l'histoire ancienne. L’auteur vient d’inclure, dans la master, une nouvelle version de l'installateur lua, directement activable et désactivable dans darktable (au premier démarrage et, si besoin, ultérieurement, dans les préférences).

Une fois installé, un nouveau menu peut être ouvert à gauche dans la table lumineuse :
![script-manager](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/script-manager%20FR.png)

En ouvrant script-manager la première fois, il va falloir initialiser les différents scripts Lua soit en les téléchargeant ou ceux déjà installés dans les différents répertoires de .config/lua ou les mettre à jour :
![script-manager Initialisation](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/script-manager%20Init%20FR.png)

Ainsi fait, le module est prêt à fonctionner en cliquant sur « Enable/Disable Scripts » :
![script-manager Utilisation](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/script-manager%20util%20FR.png)

Il est possible de choisir le répertoire avec « Category » :
![script-manager utilisation](https://raw.githubusercontent.com/jpg54/dtorg/darktable-3.2/script-manager%20util%201%20FR.png)


script manager.lua ne nécessite pas la fermeture de darktable pour activer un ou plusieurs modules. Par contre, désactiver un module n'est pris en compte qu’au prochain redémarrage du logiciel.

À noter également que, malheureusement, les scripts lua ne sont pas traduisibles et sont donc intégralement en anglais.


### Un nouveau mode d’histogramme : parade RVB

Ce nouveau mode affiche des formes d'ondes qui représente les niveaux de chaque couche (rouge, vert et bleu). Ce mode permet donc de visualiser comment sont distribuées les composantes de couleur d'une partie de l'image.


Ce mode s'affiche en sélectionnant l'affichage de l'histogramme en mode d'onde (via l'icône en haut à gauche sur l'histogramme) puis en changeant le mode d’onde via le bouton situé tout juste à droite vers ce mode Parade RVB.

![Mode parade RVB](https://raw.githubusercontent.com/Nilvus/dtorg/93d487046710633be46a130566f1484f8b2d4f8a/content/blog/2020-08-10-darktable-3.2/en/rgb-parade.png)
 
