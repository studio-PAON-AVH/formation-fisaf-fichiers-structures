---
title: "Jour 1 – Matin : Histoire & XML"
---

# Jour 1 – Matin

## Histoire de l'édition adaptée  
## et initiation au langage XML

Notes:
Bienvenue dans cette première session de la formation. Nous allons commencer par un tour d'horizon historique de l'édition numérique et de l'édition adaptée, avant d'aborder les fondamentaux du langage XML et du format DTBook.

---

## Au programme ce matin

1. Un peu d'histoire et de culture
   - Les outils numériques pour l'édition
   - L'édition numérique
   - L'édition adaptée et le DAISY Consortium
   - Rendre des publications numériques accessibles
   - Les formats de fichiers
2. Les formats XML
   - Présentation du XML
   - XHTML et XML DTBook
   - Structure et éléments sémantiques du DTBook
   - Logiciels pour lire des fichiers XML

Notes:
Voici le programme de cette matinée. Nous allons d'abord revenir sur l'histoire de l'édition numérique et de l'édition adaptée, puis nous aborderons les formats de fichiers avant d'entrer dans le détail du XML et du DTBook.

---

# Partie 1

## Un peu d'histoire et de culture

Notes:
Cette première partie nous permet de replacer les formats structurés dans leur contexte historique, pour mieux comprendre pourquoi ils ont été créés et quels besoins ils adressent.

---

## Les outils numériques pour l'édition

**1960+** Informatisation des imprimeurs + prestataires
- Généralisation de la photocomposition
- Apparition des premiers copieurs Xerox (xérographie)

**1975+** Généralisation des ordinateurs personnels
- Apple II (1977)

**1980+** Informatisation de l'édition / PAO
- Langage Adobe PostScript (1982)
- Imprimantes PostScript grand public (ex. Apple LaserWriter 1985)
- Logiciels de mise en page PageMaker (1985), QuarkXpress (1987)
  - Approche « WYSIWYG »

Notes:
Dès les années 60, des systèmes informatiques complexes sont mis en place par les imprimeurs et leurs prestataires, notamment Xerox.
- Évolution de la photocomposition et de l'électrophotographie (illustration wikipedia : photocompositeur Lumitype 1965)

1982 - Adobe PostScript : Langage de description d'image vectoriel ou matricielle, pour la rasterization d'images par les imprimantes (ancêtre du PDF)
1985 - Apple LaserWriter : imprimante laser grand public avec interpréteur postscript embarqué
1985 - PageMaker, ancêtre d'InDesign
1987 – QuarkXpress

Notion : WYSIWYG « What you see is what you get », ou littéralement en français : « ce que vous voyez est ce que vous obtenez ». Cette approche vise, en résumé, à permettre à l'utilisateur de créer un document tout en en composant le rendu final. On visualise à l'écran, à mesure que l'on écrit, ce que l'on obtiendra à l'impression pour un document papier, à la vidéo-projection pour un diaporama, ou à la mise en ligne pour un site web.

---

## L'édition numérique

**1971** Projet Gutenberg
- https://www.gutenberg.org/

**1980+** Diffusion d'ouvrages sur support numérique
- Disquette / CD-ROMs
- Réalisé par des informaticiens ≠ éditeurs « papier »
- Concept « WYSIWYM »

**1990+** Web, W3C, IDPF (standardisation)
- W3C : Formats HTML / CSS pour le web
- IDPF : OEB puis EPUB pour les livres numériques

**2017** Combinaison IDPF + W3C

Notes:
L'édition de livres numériques apparaît en 1971 avec le projet Gutenberg visant à créer une bibliothèque de versions électroniques de textes libres de droits.

Durant les années 80, plusieurs ouvrages sont proposés sous forme électronique, sous forme de disquettes ou de CD-ROMs. Le travail éditorial est réalisé essentiellement par des informaticiens, parfois issus du monde de l'édition, mais dont la culture reste différente.

Notion : WYSIWYM, « What you see is what you mean », c'est-à-dire : « Ce que vous voyez est ce que vous voulez dire ». Par opposition au WYSIWYG, cette approche propose à l'utilisateur une interface de création de contenus autonome par rapport à la mise en forme finale. L'utilisateur ne met plus de mots en gras, mais spécifie qu'ils sont importants. C'est le programme qui se chargera, lors d'une phase de publication, d'appliquer le rendu adapté.

Avec la démocratisation du web à partir des années 1990, on voit apparaître de nouveaux acteurs pour répondre à un besoin d'interopérabilité des formats. Le W3C est créé en 1994, et l'IDPF crée en 1995 le format Open eBook, qui deviendra l'EPUB.

En 2017, l'IDPF fusionnera avec le W3C, ce dernier reprenant alors le travail de spécification des différents standards qui composent un EPUB.

---

## L'édition adaptée

**L'édition adaptée** : Production éditoriale pour les publics empêchés de lire le texte imprimé

- **1821** : Invention du **braille**
- **1934** : Premiers **livres audio** aux USA

Production / diffusion par des bibliothèques spécialisées
- *Bénévolat* ou **structures médico-sociales**

Notes:
L'édition adaptée consiste à rendre accessibles des productions éditoriales à des publics empêchés de lire le texte imprimé.

On note en date notoire l'invention du système braille par Louis Braille en 1821, qui permet aux aveugles d'avoir accès à la culture sur papier.
Les premières publications de livre audio quant à elles remontent à 1934, réalisées pour le « Talking book program » créé en 1931 par la « American Foundation for the Blind » et la « Library of Congress Book for the Blind Project ».

Au niveau mondial, cette activité est souvent encadrée et exercée par des bibliothèques spécialisées qui répondent aux demandes des usagers. Les réalités sont très différentes selon les moyens politiques et financiers, une grande majorité de l'activité est exercée par des bénévoles ou des petites structures médico-sociales lorsque celles-ci existent comme en France.

---

## Le DAISY Consortium (1996)

**1996** - Création du DAISY Consortium

Transition analogique (cassettes) → numérique

**Mettre fin à la « famine du livre »**

3 axes de travail :
- **Qualité** de l'expérience de lecture numérique
- **Autonomie** des usagers
- **Quantité** de livres disponibles

Notes:
Les bibliothèques spécialisées pour l'accès à la lecture aux publics empêchés de lire se sont regroupées au niveau international en 1996 en créant le Consortium DAISY. L'objectif premier était d'assurer la transition des formats analogiques (essentiellement la cassette) vers des formats numériques en profitant des bénéfices rendus possibles par l'informatique.

L'objectif du Consortium DAISY est de mettre fin à la famine du livre pour les publics empêchés à travers trois axes principaux :
- Améliorer la qualité de l'expérience de lecture numérique.
- Augmenter l'autonomie des lecteurs à travers le développement d'une édition inclusive permettant de répondre aux besoins du plus grand nombre.
- Augmenter l'offre de lecture spécialisée via les possibilités d'automatisation des chaînes de production et la mutualisation des éditions adaptées grâce à l'alignement de l'offre sur un seul format.

---

## Le DAISY Consortium pour l'édition inclusive

- **Formats numériques**
  - Livre audio « DAISY » (DAISY2 / DAISY3)
  - Braille numérique « eBraille »
  - Participation aux évolutions de l'EPUB3
- **Outils de production**
  - [DAISY Pipeline](https://daisy.org/activities/software/pipeline/)
  - [ACE by DAISY](https://daisy.org/activities/software/ace/)
  - [OBI](https://daisy.org/activities/software/obi/)
  - [TOBI](https://daisy.org/activities/software/tobi/)
  - [FIDO](https://daisy.org/activities/software/fido/)
  - [SaveAsDAISY](https://daisy.org/activities/software/save-as-daisy-ms-word-add-in/)
  - [WordToEPUB](https://daisy.org/activities/software/wordtoepub/)
- **Formations**
  - [kb.daisy.org/publishing/docs/](https://kb.daisy.org/publishing/docs/)
  - [inclusivepublishing.org](https://inclusivepublishing.org/)

Notes:
Pour répondre à ces objectifs, le DAISY Consortium travaille donc à la fois sur les formats de publications numériques, les outils de production de ces formats, et la formation à leur utilisation et leur production.

Le consortium est surtout connu pour son format DAISY : créé comme un standard propriétaire en Suède en 1994, le format DAISY (digital accessible information system) devient une norme ouverte gérée par le consortium en 1997. Une version 2 est publiée en 1998 puis une version 3 en 2005.

Le consortium participe actuellement très activement, via le W3C, à l'amélioration du format EPUB3 pour en maximiser l'accessibilité, mais également à la création d'une extension de l'epub3 spécifique au braille appelée l'eBraille.

Pour produire tous ces livres, le consortium propose un panel d'outils à la fois pour l'édition et la production de livre numérique. Et enfin, le consortium maintient une base de connaissance (en anglais) sur la production de fichier numérique adapté.

---

## Rendre des publications numériques « accessibles »

`Logiciel de lecture + Technologie d'assistance + Compétence usager + Qualité du document`

> **Document = (Contenu + Structure) * Aspect**

**Points clés pour l'accessibilité / choix du type de fichier :**
- Ordre de lecture logique
- Structuration fine (+ respect des standards techniques)
- Séparation contenu / aspect
- Possibilités de navigation
- Description ou alternative pour les contenus visuels

Notes:
L'accessibilité d'un fichier numérique dépend de la combinaison entre la qualité du fichier, le logiciel de lecture, la technologie d'assistance utilisée et les compétences de l'usager.

Le producteur ne peut agir que sur la qualité du fichier. Pour ce faire il doit considérer tout document comme la combinaison de trois éléments.
- **Contenu** : textes, espaces et illustrations contextuelles.
- **Structure** : séquence de chapitres, sections, en-têtes, pieds de pages, sous-titres, paragraphes.
- **Aspect** : typographies, embellissements, disposition géométrique de la page et de son contenu.

Ce qui l'amène à respecter cinq points clefs :
- L'ordre de lecture logique.
- Une structuration fine et respectueuse des standards techniques.
- La séparation du contenu et de l'aspect.
- Des possibilités de navigation variées.
- Des descriptions ou alternatives pour les contenus visuels.

Cette approche, au delà de l'accès à la lecture, permet de structurer la chaîne de production autour de formats pivots privilégiant l'interopérabilité. C'est le choix qui a été fait à l'AVH autour du format pivot xml dtbook permettant d'utiliser les outils développés par le Consortium DAISY et d'assurer une interopérabilité avec les évolutions à venir.

---

## Quelques notions utiles

**Formats propriétaires** vs **formats ouverts**

**Norme** vs **Standard**

**Reconnaître un type de fichier** par extensions de fichiers
- ex. : `nom_fichier.ext`
- Explorateur Windows / bouton `…` / Options / Affichage → décocher **Masquer les extensions des fichiers dont le type est connu**

**Attention aux « fausses extensions »**
- ex. un fichier exécutable renommé en `.pdf`

Notes:
Avant de voir plus en détails les formats de document et donc de fichier que vous pourriez rencontrer pour la réalisation d'une adaptation, les quelques notions suivantes peuvent s'avérer utiles.

Premièrement, il existe des formats dits « propriétaires » et des formats dits « ouverts » :
- Format propriétaire : les spécifications sont contrôlées par des intérêts privés. De ce fait, le format propriétaire fait souvent l'objet d'un brevet et les spécifications sont souvent gardées secrètes ou en accès limité.
- Format ouvert : les spécifications techniques sont publiques et sans restriction d'accès ni de mise en œuvre.

Vous entendrez également souvent parler de normes et de standards concernant les fichiers :
- Norme : Document établi par consensus et approuvé par un organisme reconnu, qui fournit des règles, des lignes directrices ou des caractéristiques pour des activités ou leurs résultats. (ISO)
- Standard : référentiel publié par une entité privée autre qu'un organisme de normalisation national ou international. On parle de standard à partir du moment où le référentiel a une diffusion large (standard de facto).

Un point très important pour la suite sera aussi la reconnaissance du type de fichier qui vous sera fourni ou demandé. Le plus souvent, ce type est identifiable par une extension. Sur Windows, si vous ne voyez pas ces extensions, il vous faudra les « démasquer » en allant dans les options de l'Explorateur.

---

## Quelques formats bureautiques

| Format | Description |
|--------|-------------|
| **TXT** | Format texte seulement |
| **DOC** | Ancien format de document Word |
| **DOCX** | Document Word OpenXML |
| **DOCM** | Document Word avec Macro |
| **DOTM** | Modèle de document avec Macro |
| **RTF** | Rich Text Format |
| **ODT** | Document texte formaté OpenDocument (OpenOffice, LibreOffice) |
| **OTT** | Modèle de document texte OpenDocument |

Notes:
Ces formats bureautiques sont les plus courants dans un environnement de travail classique. Le DOCX est aujourd'hui le format de référence pour Word, et l'ODT est son équivalent libre dans la suite LibreOffice/OpenOffice. Les formats de modèles (DOTM, OTT) permettent de définir des styles réutilisables, très utiles pour la production de documents accessibles.

---

## Quelques formats spécialisés dans l'édition

| Format | Description |
|--------|-------------|
| **INDD** | Format propriétaire d'Adobe InDesign |
| **XML** | Texte balisé |
| **IDML** | Format d'échange XML d'InDesign |
| **XML LG** | XML spécifique Hachette (beaucoup de dérivés : Flammarion, Libella, IGS) |
| **XML DTBook** | XML spécifique DAISY Consortium pour la production de livre numérique |
| **XML TEI** | Format de description de document du TEI Consortium |
| **PEF** | XML pour la mise en page braille par MTM |
| **DTD** | Format de définition de grammaire XML |

Notes:
Ces formats sont utilisés dans des contextes éditoriaux plus spécialisés. InDesign et ses formats associés (INDD, IDML) sont très répandus dans l'édition professionnelle. Le XML DTBook est le format pivot que nous allons étudier en détail dans cette formation. Le TEI (Text Encoding Initiative) est utilisé en recherche en humanités numériques. Le PEF est spécifique à la production braille.

---

## Quelques formats de publication / consultation

| Format | Description |
|--------|-------------|
| **PDF** | Format de mise en page imprimable (Adobe) |
| **AZW** | Format de livre numérique (Amazon) |
| **IBOOKS** | Format de livre numérique (Apple) |
| **DAISY** | Format de livre audio structuré (DAISY Consortium) |
| **(X)HTML** | Format structuré pour le web |
| **CSS** | Fichier de style visuel pour le rendu final |
| **EPUB** | Format de livre numérique (W3C) |
| **EBRL** | (eBraille) Extension de l'EPUB3 pour le braille (DAISY Consortium) |

Notes:
Ces formats sont destinés à la consultation finale des ouvrages. Le PDF reste très répandu mais pose des difficultés d'accessibilité lorsqu'il n'est pas balisé. Les formats propriétaires (AZW, iBooks) limitent la portabilité. L'EPUB, standard ouvert maintenu par le W3C, est le format de référence pour l'édition numérique accessible, et l'eBraille est son extension pour le braille.

---

# Partie 2

## Les formats XML

Notes:
Nous entrons maintenant dans la partie technique de la matinée. Nous allons voir ce qu'est le XML, comment il fonctionne, et comment le format DTBook en est une application concrète pour l'édition accessible.

---

## 2.a – Présentation du XML

**XML** : *eXtensible Markup Language*

- Langage de balisage créé par le **W3C** (1998)
- Séparation **contenu** / **structure** / **présentation**
- Lisible par les humains **et** les machines
- Extensible : on définit ses propres balises

```xml
<?xml version="1.0" encoding="UTF-8"?>
<livre>
  <titre>Mon premier livre</titre>
  <chapitre numero="1">
    <titreSection>Introduction</titreSection>
    <para>Ceci est le premier paragraphe.</para>
  </chapitre>
</livre>
```

Notes:
Le XML, ou eXtensible Markup Language, est un langage de balisage standardisé par le W3C en 1998. Il permet de structurer des données de manière hiérarchique en utilisant des balises. Contrairement au HTML qui a des balises prédéfinies, le XML permet de définir ses propres balises, d'où son caractère « extensible ». La séparation entre contenu, structure et présentation est un principe fondamental qui facilite la conversion entre formats et l'accessibilité.

---

## Les types de balises XML

| Type | Exemple | Description |
|------|---------|-------------|
| **Ouvrante** | `<para>` | Début d'un élément |
| **Fermante** | `</para>` | Fin d'un élément |
| **Auto-fermante** | `<img src="img.jpg"/>` | Élément vide |
| **Attribut** | `class="important"` | Propriété d'un élément |
| **Commentaire** | `<!-- commentaire -->` | Note non rendue |

Notes:
Un document XML est composé d'éléments délimités par des balises ouvrantes et fermantes. Les attributs permettent d'ajouter des propriétés aux éléments. Les balises auto-fermantes sont utilisées pour les éléments qui n'ont pas de contenu textuel, comme les images. Les commentaires sont ignorés par les processeurs XML et servent uniquement à la documentation du code.

---

## Règles de base du XML

1. 📌 Tout élément doit être **ouvert et fermé**
2. 📌 Les éléments doivent être correctement **imbriqués**
3. 📌 Un seul **élément racine** par document
4. 📌 Les attributs doivent être entre **guillemets**
5. 📌 Respect de la **casse** (`<Para>` ≠ `<para>`)

```xml
<!-- ✅ XML valide -->
<document>
  <section><para>Texte</para></section>
</document>

<!-- ❌ XML invalide -->
<document>
  <section><para>Texte</section></para>
</document>
```

Notes:
Ces cinq règles définissent ce qu'on appelle un document XML « bien formé ». Un document XML bien formé peut être parsé par n'importe quel parseur XML standard. En plus d'être bien formé, un document peut être « valide » s'il respecte une grammaire définie (DTD ou schéma). Le DTBook utilise une DTD pour définir quels éléments sont autorisés et dans quel ordre.

---

## 2.b – Comparatif XHTML et XML DTBook

| Critère | XHTML | XML DTBook |
|---------|-------|------------|
| **Origine** | W3C | DAISY Consortium |
| **Usage principal** | Pages web | Livres audio structurés |
| **Éléments sémantiques** | `<h1>`, `<p>`, `<div>`… | `<doctitle>`, `<level1>`, `<p>`… |
| **Multimédia** | Oui (HTML5) | Audio synchronisé (SMIL) |
| **Accessibilité** | ARIA, alt… | Structure native |

Notes:
Le XHTML est une version stricte du HTML conforme aux règles XML. Il est utilisé pour les pages web et constitue la base des fichiers de contenu dans un EPUB. Le XML DTBook est spécifique au DAISY Consortium et possède une sémantique plus riche pour les livres : il distingue les différentes parties d'un livre (frontmatter, bodymatter, rearmatter) et offre des éléments de synchronisation audio via le format SMIL.

---

## 2.c – Structure du XML DTBook

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE dtbook PUBLIC "-//NISO//DTD dtbook 2005-3//EN"
  "http://www.daisy.org/z3986/2005/dtbook-2005-3.dtd">
<dtbook version="2005-3" xml:lang="fr">
  <head>
    <meta name="dtb:uid" content="isbn:978-0-0000-0000-0"/>
    <meta name="dc:Title" content="Mon ouvrage"/>
    <meta name="dc:Language" content="fr"/>
  </head>
  <book>
    <frontmatter>
      <doctitle>Mon ouvrage</doctitle>
      <docauthor>Auteur</docauthor>
    </frontmatter>
    <bodymatter>
      <level1>
        <h1>Chapitre 1</h1>
        <p>Premier paragraphe.</p>
      </level1>
    </bodymatter>
  </book>
</dtbook>
```

Notes:
Voici un exemple minimal de fichier XML DTBook. La déclaration DOCTYPE fait référence à la DTD du DAISY Consortium qui définit la grammaire du format. L'en-tête (head) contient les métadonnées de l'ouvrage comme l'identifiant unique, le titre et la langue. Le corps du livre est divisé en frontmatter (pages liminaires), bodymatter (texte principal) et éventuellement rearmatter (annexes). Les niveaux hiérarchiques sont représentés par les éléments level1 à level6.

---

## Les éléments sémantiques du XML DTBook

| Élément | Rôle |
|---------|------|
| `<dtbook>` | Racine du document |
| `<head>` | Métadonnées (titre, auteur, langue…) |
| `<frontmatter>` | Pages liminaires |
| `<bodymatter>` | Corps du document |
| `<rearmatter>` | Annexes, index, glossaire |
| `<level1>` à `<level6>` | Niveaux hiérarchiques |
| `<h1>` à `<h6>` | Titres de sections |
| `<p>` | Paragraphe |
| `<list>` / `<li>` | Listes |
| `<table>` | Tableaux |
| `<imggroup>` / `<img>` | Images avec description |

Notes:
Le DTBook possède un vocabulaire sémantique riche qui permet de décrire précisément la structure d'un livre. Les éléments level1 à level6 correspondent aux différents niveaux de chapitres et sections, et doivent contenir au minimum un titre (h1 à h6). Les éléments frontmatter, bodymatter et rearmatter permettent de distinguer les différentes parties d'un ouvrage. L'élément imggroup permet d'associer une image à sa description textuelle (caption, prodnote).

---

## 2.d – Logiciels pour lire des fichiers XML

| Logiciel | Plateforme | Rôle |
|----------|------------|------|
| **Notepad++** | Windows | Éditeur texte avec coloration syntaxique |
| **Visual Studio Code** | Multi | Éditeur avancé, extensions XML |
| **XMLSpy** | Windows | Éditeur XML professionnel |
| **oXygen XML Editor** | Multi | Éditeur XML avancé |
| **Firefox / Chrome** | Multi | Visualisation basique XML |

Notes:
Pour travailler avec des fichiers XML, plusieurs outils sont disponibles. Notepad++ est un bon point de départ sur Windows grâce à sa coloration syntaxique et ses plugins. Visual Studio Code est une alternative gratuite et puissante, disponible sur toutes les plateformes, avec des extensions dédiées au XML. Pour une utilisation professionnelle, oXygen XML Editor offre des fonctionnalités avancées comme la validation en temps réel et la transformation XSLT. Les navigateurs web peuvent afficher les fichiers XML mais sans validation ni édition.

---

## Points clés à retenir – Matin J1

- 📚 L'édition numérique adaptée est née dans les années 1990 avec le DAISY Consortium
- 🏗️ Les formats structurés séparent contenu, structure et présentation (WYSIWYM)
- 🔤 XML est un langage de balisage extensible et rigoureux
- 📖 Le XML DTBook est le format DAISY 3 pour les livres structurés
- 🛠️ Des outils gratuits permettent de visualiser et éditer du XML

Notes:
Voici les points essentiels à retenir de cette matinée. La clé de l'accessibilité numérique réside dans la qualité de la structuration des documents. Un document bien structuré avec des styles sémantiques peut être converti vers de nombreux formats accessibles. Cet après-midi, nous allons mettre ces connaissances en pratique avec les outils du DAISY Consortium.

---

## Questions ?

**Pause avant l'après-midi →**

_Après-midi : produire et utiliser des fichiers XML DTBook_

Notes:
Prenons quelques minutes pour répondre aux questions avant la pause. Cet après-midi, nous utiliserons DAISY Pipeline et SaveAsDAISY pour convertir des documents Word en XML DTBook.

