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
  - Approche *WYSIWYG*

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
- Réalisé par des informaticiens ≠ éditeurs *papier*
- Concept *WYSIWYM*

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

Production éditoriale pour les publics empêchés de lire le texte imprimé

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

## 1996 - Le DAISY Consortium

Regroupement de librairies et organisation pour les personnes aveugles ou malvoyantes.

Transition analogique (cassettes) → promotion du numérique et du format *DAISY*

**Mettre fin à la « famine du livre »** accessible

3 axes de travail :
- **Qualité** de l'expérience de lecture numérique
- **Autonomie** des usagers
- **Quantité** de livres disponibles

Notes:
Des bibliothèques spécialisées pour l'accès à la lecture aux publics empêchés de lire se sont regroupées au niveau international en 1996 en créant le Consortium DAISY. L'objectif premier était d'assurer la transition des formats analogiques (essentiellement la cassette) vers des formats numériques en profitant des bénéfices rendus possibles par l'informatique.

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

Notes:
Pour répondre à ces objectifs, le DAISY Consortium travaille donc à la fois sur les formats de publications numériques, les outils de production de ces formats, et la formation à leur utilisation et leur production.

Le consortium est surtout connu pour son format DAISY : créé comme un standard propriétaire en Suède en 1994, le format DAISY (digital accessible information system) devient une norme ouverte gérée par le consortium en 1997. Une version 2 est publiée en 1998 puis une version 3 en 2005.

Le consortium participe actuellement très activement, via le W3C, à l'amélioration du format EPUB3 pour en maximiser l'accessibilité, mais également à la création d'une extension de l'epub3 spécifique au braille appelée l'eBraille.

---

## Le DAISY Consortium pour l'édition inclusive

- **Outils de production**
  - [DAISY Pipeline](https://daisy.org/activities/software/pipeline/)
  - [ACE by DAISY](https://daisy.org/activities/software/ace/)
  - [OBI](https://daisy.org/activities/software/obi/)
  - [TOBI](https://daisy.org/activities/software/tobi/)
  - [FIDO](https://daisy.org/activities/software/fido/)
  - [SaveAsDAISY](https://daisy.org/activities/software/save-as-daisy-ms-word-add-in/)
  - [WordToEPUB](https://daisy.org/activities/software/wordtoepub/)

Notes:

Pour produire tous ces livres, le consortium propose un panel d'outils à la fois pour l'édition et la production de livre numérique. 

---

## Le DAISY Consortium pour l'édition inclusive


- **Formations**
  - [kb.daisy.org/publishing/docs/](https://kb.daisy.org/publishing/docs/)
  - [inclusivepublishing.org](https://inclusivepublishing.org/)

Notes:

Et enfin, le consortium maintient une base de connaissance (en anglais) sur la production de fichier numérique adapté.*

---

## Rendre des publications numériques « accessibles »

`Logiciel_lecture + Technologie_assistance + Compétence_usager + Qualité_document`

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

**Reconnaître un type de fichier** par son `extension`
- ex. : nom_fichier`.ext`
- Explorateur Windows / bouton `…` / Options / Affichage → décocher **Masquer les extensions des fichiers dont le type est connu**

> **Attention aux « fausses extensions »**<br/>
> (ex. un fichier exécutable renommé en `.pdf`)

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
| `.txt` | Format texte seulement |
| `.doc` | Ancien format de document Word |
| `.docx`, `.docm` | Document Word OpenXML (sans et avec macro) |
| `.dotx`, `.dotm` | Modèle de document (sans et avec Macro) |
| `.rtf` | Rich Text Format |
| `.odt` | Document texte formaté OpenDocument (OpenOffice, LibreOffice) |
| `.ott` | Modèle de document texte OpenDocument |

Notes:
Ces formats bureautiques sont les plus courants dans un environnement de travail classique. Le DOCX est aujourd'hui le format de référence pour Word, et l'ODT est son équivalent libre dans la suite LibreOffice/OpenOffice. Les formats de modèles (DOTM, OTT) permettent de définir des styles réutilisables, très utiles pour la production de documents accessibles.

---

## Quelques formats spécialisés dans l'édition

| Format | Description |
|--------|-------------|
| `.indd` | Format propriétaire d'Adobe InDesign |
| `.idml` | Format d'échange XML d'InDesign |
| `.xml` | Texte balisé en XML |
| **XML LG** | XML spécifique Hachette (beaucoup de dérivés : Flammarion, Libella, IGS) |
| **XML DTBook** | XML spécifique DAISY Consortium pour la production de livre numérique |
| **XML TEI** | Format de description de document du TEI Consortium |
| `.dtd` | Format de définition de grammaire XML |
| `.pef` | XML pour la mise en page braille par MTM |

Notes:
Ces formats sont utilisés dans des contextes éditoriaux plus spécialisés. InDesign et ses formats associés (INDD, IDML) sont très répandus dans l'édition professionnelle. Le XML DTBook est le format pivot que nous allons étudier en détail dans cette formation. Le TEI (Text Encoding Initiative) est utilisé en recherche en humanités numériques. Le PEF est spécifique à la production braille.

---

## Quelques formats de publication / consultation

| Format | Description |
|--------|-------------|
| `.pdf` | Format de mise en page imprimable (Adobe) |
| `.html, .xhtml` | Format structuré pour le web |
| `.css` | Fichier de style visuel pour le rendu final |
| `.epub` | Format de livre numérique (W3C) |
| `.ebrl` | (eBraille) Extension de l'EPUB3 pour le braille (DAISY Consortium) |
| **AZW**, `.mobi`, `.kf8` | Format de livre numérique Amazon / Kindle |
| **IBOOKS** | Format de livre numérique (Apple) |
| **DAISY** | Format de livre audio structuré (DAISY Consortium) |


Notes:
Ces formats sont destinés à la consultation finale des ouvrages. Le PDF reste très répandu mais pose des difficultés d'accessibilité lorsqu'il n'est pas balisé. Les formats propriétaires (AZW, iBooks) limitent la portabilité. L'EPUB, standard ouvert maintenu par le W3C, est le format de référence pour l'édition numérique accessible, et l'eBraille est son extension pour le braille.

---

# Partie 2

## Les formats XML

Notes:
Nous entrons maintenant dans la partie technique de la matinée. Nous allons voir ce qu'est le XML, comment il fonctionne, et comment le format DTBook en est une application concrète pour l'édition accessible.

---

## eXtensible Markup Language

ou plus simplement : **XML**

- **Langage de structuration** extensible - W3C (1998)
  - Version 1.0, édition 5 (2008)
  - Version 1.1, édition 2 (2006)

**Arborescence de `<balises>`**


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
Le XML, ou eXtensible Markup Language, est un langage de balisage standardisé par le W3C en 1998. Il permet de structurer des données de manière hiérarchique en utilisant des balises. 

Vous ne le savez peut être pas mais il existe actuellement 2 versions de XML
- La 1.0 édition 5 créer en 2008 qui est très strict sur ce qui est autorisé
- la 1.1 qui est beaucoup plus souple, avec un changement philosophique et un support étendu des caractères unicode.


Un fichier XML est avant tout … un fichier texte
Mais dans ce fichier texte, on va décrire du contenu d’une certaines façon, en utilisant des marqueurs (d’où le « markup ») qu’on appel en français des ‘balises” (et anglais des « tag »)

Ces balises permettent de structurer un “document” sous la forme d’un arbre de balises.

Contrairement au HTML qui a des balises prédéfinies, le XML permet de définir ses propres balises, d'où son caractère « extensible ». La séparation entre contenu, structure et présentation est un principe fondamental qui facilite la conversion entre formats et l'accessibilité.

---

### Différents types de balises XML

| Type | Exemple | Description |
|------|---------|-------------|
| **Élement** | `<element attribut="valeur">texte</element>` | Noeud de base de la structure |
| **Instruction de traitement** | `<?cible données?>` | Instructions pour des logiciels spécifiques |
| **Commentaire** | `<!-- contenu -->` | Annotation ou information complémentaire |
| **Déclaration DOCTYPE** | `<!DOCTYPE racine SYSTEM "fichier.dtd">` | Indication de la grammaire a respecter |
| **Données brutes** | `<![CDATA[données brutes]]>` | Éviter l’échappement des caractères |


Notes:
Le XML est donc un langage balisé mais il peut y avoir plusieurs types de balises pour présenter différents types de données

On a principalement 5 types de balises avec tout une utilité différentes
La principale c’est la balise de type “élément” sur laquelle on va revenir plus en détail après, et qui représente un noeud de donnée (donc de contenu) dans le document
(Si j’ai mis le mot element en bleu ici, c’est tout simplement parceque le mot “élément” ici n’est ici qu’un exemple)

Vous avez ensuite les “processing instruction” ou PI, ou “instruction de traitement” en français, qui servent à indiqué quelque chose a un programme prévu pour l’utiliser lors du traitement du document.

Vous avez les balises commentaires, qui servent majoritairement a faire de l’annotation pour lecture par un humain.
(On utilise beaucoup de cette balise en développement quand on travaille sur des fichiers de configuration en XML)

Vous avez ensuite une balise un peu spécial qu’on appel le doctype et dont le role est d’indiqué comment le fichier XML

Et enfin on a une balise beaucoup plus rare qui est la balise “CharData” ou CustomData, 

---

```xml
<element>contenu texte ou XML</element>
```

Balise (ou noeud) **élément**

Block de base de la structure d’un document XML

Conteneur dans l’arborescence du contenu<br/>
<small>(un peu comme un dossier dans un système de fichier)</small>


**Arborescence stricte**

Toutes les balises **ouvertes** doivent être **fermées** :
```xml
<elemA></elemA>  == <elemA />
```

---

```xml
<element attribut="VALEUR">
```
**Attributs** : Couples « clé/valeur » dans un élément

Données complémentaires (métadonnée) spécifiques a un élément

- Stylage visuel
- Adresse pour les liens hypertexte
- Identifiants ou références a un identifiant (note et appel de note)
- Texte alternatif pour les images

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

```xml
<!DOCTYPE racine (((PUBLIC PublicID)|SYSTEM) url/schema.dtd)? ([ extensions? ])? >
```
Contraindre la structure XML du contenu via une « grammaire »
- élément `<racine>...</racine>`
- schéma de validation DTD `url/schema.dtd` 
  - `PUBLIC` + identifiant + (url ou identifiant catalogue)
  - `SYSTEM` + `chemin/du/schema.dtd`
- Personnalisation : `[ extensions ]`
  - Format balisé "DTD"

```xml
<!DOCTYPE livre SYSTEM "DTD_LG_NC_V5-2.2.dtd">
<!DOCTYPE dtbook PUBLIC "-//NISO//DTD dtbook 2005-3//EN" "http://www.daisy.org/z3986/2005/dtbook-2005-3.dtd" []>
<!DOCTYPE livre PUBLIC "-//DTD LG Flammarion//FR" "DTD_LG_Flammarion.dtd">
```

Notes: 
Pour information, beaucoup de système spécialisé dans le traitement XML utilise ce que l'on appelle un fichier catalogue
dans lequel vous pouvez indiquez des identifiants ou des urls et les faires correspondre à un fichier

---

```xml
<!DOCTYPE dtbook SYSTEM 'dtbook-2005-3.dtd' [
  <!ENTITY % MATHML.prefixed "INCLUDE" >
  <!ENTITY % MATHML.prefix "mml">
  <!ENTITY % Schema.prefix "sch">
  <!ENTITY % XLINK.prefix "xlp">
  <!ENTITY % MATHML.Common.attrib 
    "xlink:href CDATA #IMPLIED
     xlink:type CDATA #IMPLIED 
     class CDATA #IMPLIED 
     style CDATA #IMPLIED 
     id ID #IMPLIED 
     xref IDREF #IMPLIED 
     other CDATA #IMPLIED 
     xmlns:dtbook CDATA #FIXED 'http://www.daisy.org/z3986/2005/dtbook/’
     dtbook:smilref CDATA #IMPLIED">
  <!ENTITY % mathML2 SYSTEM 'mathml2.dtd'>
  <!ENTITY % externalFlow "| mml:math">
  <!ENTITY % externalNamespaces "xmlns:mml CDATA #FIXED 'http://www.w3.org/1998/Math/MathML'" >
] >
```
---

```xml
<element xmlns="uri" ... >

<pf:element xmlns:pf="http://..." ... >
```

Attributs spéciaux **espcaces des noms**

Différencier des éléments respectant des grammaires XML différents au sein d’un même document

Exemple :
```xml
<img xmlns="uri/identifiant/principale">
  <svg:root xmlns:svg="uri/identifiant/svg">
    ...
  </svg:root>
</img>
```
---

```xml
  <?cible données ?>
```

**Instruction de données**
(Ou *PI* pour **Processing Instruction**)

Permet d'inclure des instructions de traitement pour des logiciels spécifiques.

```xml
<!-- PI spécial "Prologue" en début de fichier XML pour les éditeurs ou lecteurs de fichier XML -->
<?xml version="1.0" encoding="UTF-8"?>
<!-- PI interprétées par certains navigateur pour afficher le XML -->
<?xml-stylesheet href="dtbookbasic.css" type="text/css"?>
<!-- PI présente dans certains fichier XML LG, probablement pour des process internes à Hachette -->
<?verif code=CP1314 date=08/01/2024?>
```

---

```xml
<!-- Commentaire : annotation pour un humain -->
```
**commentaire**

Information complémentaire ne relevant pas du contenu formel du document

Annotations ou informations à destination d'un autre lecteur

<small>(Notamment dans les langages de programmations écrits en XML)</small>

Exemple :
```xml
<!-- Suppression des tags element dans la structure -->
<xsl:template match="element"></xsl:template>
```

---

```xml
&codeEntité;
```

**Entité** : encodage de caractères réservés ou spéciaux

- **Caractères réservés** :
  - `&` → `&amp;amp;`
  - `>` → `&amp;gt;`
  - `<` → `&amp;lt;`
  - `"` → `&amp;quot;`
  - `'` → `&amp;apos;`
- **Caractères Unicode** :
  - 🍺 → `&amp;#x1F37A;` (hexa) ou `&amp;#127866;` (décimal)

Exemple : "Johnson & Jhonson prennent une 🍺 au bar"
```xml
  <p>Johnson &amp;amp; Jhonson prennent une &amp;#x1F37A; au bar</p>
```

---

## Quelques formats XML de structuration de titres

| Format | Description |
|--------|-------------|
| **XHTML** | HTML respectant les règles du XML, utilisé dans les EPUB3, extensible (SVG, MathML) |
| **XML LG** | Format de rétrocession XML « Littérature Générale » de Hachette (version 5.2.2) |
| **XML DTBook** | Format de structuration pour la création de livre numérique DAISY (dernière révision : 2005-3, décembre 2007) |

---

### Le XHTML

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="fr" lang="fr">
  <head>
    <title>Exemple</title>
    <meta charset="UTF-8"/>
    <meta name="author" content="Nicolas Pavie"/>
  </head>
  <body>
    <section>
      <h1>Exemple de section</h1>
      <section>
        <h2>Exemple de sous-section</h2>
        <p>Exemple de paragraphe</p>
      </section>
    </section>
  </body>
</html>
```

---

### Le XML "LG"

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE livre SYSTEM "DTD_LG_NC_V5-2.2.dtd"[]>
<livre compo="AVH">
  <ident>
    <tit>Exemple de titre</tit>
    <auteur>Nicolas Pavie</auteur>
  </ident>
  <corps>
    <part>
      <tit>Exemple de section</tit>
      <chap>
        <tit>Exemple de sous-section</tit>
        <dev>
          <p>Exemple de paragraphe</p>
        </dev>
      </chap>
    </part>
  </corps>
</livre>
```

---

### Le "XML DTBook"

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!-- Le "DOCTYPE" qui va contraindre la structuration et la validation -->
<!DOCTYPE dtbook PUBLIC "-//NISO//DTD dtbook 2005-3//EN" "http://www.daisy.org/z3986/2005/dtbook-2005-3.dtd" []>
<dtbook xmlns="http://www.daisy.org/z3986/2005/dtbook/" version="2005-3" xml:lang="fr-FR">
  <head> <!-- Entête : métadonnées du livre -->
    <meta name="dc:Title" content="Exemple"/>
    <meta name="dc:Creator" content="Nicolas Pavie"/>
  </head>
  <book> <!-- Contenu structuré du livre -->
    <bodymatter>
      <level1>
        <h1>Exemple de section</h1>
        <level2>
          <h2>Exemple de sous-section</h2>
          <p>Exemple de paragraphe</p>
        </level2>
      </level1>
    </bodymatter>
  </book>
</dtbook>
```
---
### Le "XML DTBook"
Contenu du livre : `<book>`

```xml
<book>
  <frontmatter> <!-- Une partie liminaire optionnelle -->
    <doctitle>...</doctitle> <!-- Titre du livre, Obligatoire -->
    <covertitle>...</covertitle> <!-- Titre couverture, Optionnel -->
    <docauthor>...</docauthor> <!-- Auteur(s) du livre, 0 ou N fois -->
    <!-- On peut insérer ci-après l'introduction, la table des matières, etc -->
    <level1>...</level1> <!-- 0 ou N fois -->
  </frontmatter>
  <bodymatter> <!-- Le "corps" du livre (son contenu principale), optionnel  -->
    <level1>...</level1> <!-- 1 ou N fois -->
  </bodymatter>
  <rearmatter> <!-- Une partie postface optionnelle -->
    <!-- On insère généralement ici le quatrième de couverture,
    La bibliographie, les notes de fin, etc. -->
    <level1>...</level1> <!-- 0 ou N fois -->
  </rearmatter>
</book>
```

---
### Le "XML DTBook"
Structuration en "niveau" : `<levelX>` (X = [1..6])

```xml
<bodymatter><!-- ou frontmatter ou rearmatter -->
  <!--Structuration en niveau imbriqué, jusqu'a 6 niveau -->
   <level1>
      <h1>…</h1> <!-- La balise "h" correspondante est obligatoire -->
      <!-- on insère ensuite des paragraphes, des notes des tableaux etc
           puis possiblement des sous niveaux -->
      <level2>
         <h2>…</h2>
         <level3>
            <h3>…</h3>
            <level4>
               <h4>…</h4>
               <level5>
                  <h5>…</h5>
                  <level6>
                     <h6>…</h6>
                  <level6>
               <level5>
            <level4>
         <level3>
      <level2>
   </level1>
   <level1>…</level1>
</bodymatter>
```

---
### Le "XML DTBook"

Les blocs de contenu d'un `<levelX>` 1/2

```xml
<p>paragrapahe simple.</p>
<address>5 rue duroc, 97006 Paris</address>
<author>un auteur</author>
<blockquote>
   <p>Un block de citation</p>
</blockquote>
<dateline>Date de référence</dateline>
<bridgehead>Intertitre</bridgehead>
<epigraph>
   <p>Un épigraphe</p>
</epigraph>
<poem>
   <linegroup>
      <line>Un vers d'un poem</line>
   </linegroup>
</poem>
<note id="note-id"><p>texte de note</p></note>
```

---
### Le "XML DTBook"

Les blocs de contenu d'un `<levelX>` 2/2

```xml
<table>
   <caption>Une légende</caption>
   <thead>
      <tr><th>Un entête de colonne</th></tr>
   </thead>
   <tbody>
      <tr><td>Une donnée</td></tr>
   </tbody>
</table>
<list type="ol"><!-- ou ul ou pl -->
   <hd>Une liste</hd>
   <li>item</li>
</list>
<dl><!--Une liste de définitions-->
   <dt>Un terme</dt>
   <dd>Sa définition</dd>
</dl>
<img src="image.jpg" 
     alt="Description de l'image" />
<imggroup>
   <caption>Une légende</caption>
   <img src="image.jpg" 
        alt="Description de l'image" />
</imggroup>

```

---

### Le XML DTBook

De la sémantique dans le texte
```xml
<p>Quelques enrichissements en ligne :
   <em>italique (emphase)</em> ou 
   <strong>gras (emphase forte)</strong>,
   en <sub>indice</sub>
   ou en <sup>exposant</sup>,
   des <abbr title="abbreviations">abbr.</abbr>
   ou des <acronym title="acronyms">acron.</acronym>,
   des <a href="uneUrl#UnIdentifiant">liens</a>
   <br /><!-- Des retours à la lignes -->
   <code>Du code informatique</code>,
   Un mot à <dfn>définir</dfn> ,
   un appel de <noteref idref="note-id">note</noteref>,
   <cite>Citation en ligne par <author>un auteur</author></cite>,
   le conteneur générique <span>"span"</span>,
   <bdo dir="ltr">Pour le texte bidirectionnel (asie)</bdo>
</p>
```

---

##  Logiciels pour éditer des fichiers XML

| Logiciel | Extension recommandée | Lien |
|----------|-----------------------|------|
| **Notepad++** | XML Tools | [notepad-plus-plus.org](https://notepad-plus-plus.org/) |
| **Sublime Text** | Exalt | [sublimetext.com](https://www.sublimetext.com/) |
| **Visual Studio Code** | XML (par RedHat) | [code.visualstudio.com](https://code.visualstudio.com/) |
| **XML Copy Editor** | - | [xmlcopyeditor.sourceforge.net](http://xmlcopyeditor.sourceforge.net/) (gratuit) |
| **XMLSpy** | - | [altova.com](https://www.altova.com/fr/xmlspy-xml-editor) (payant) |
| **Oxygen XML Editor** | - | [oxygenxml.com](https://www.oxygenxml.com/) (payant) |


Notes:
Pour travailler avec des fichiers XML, plusieurs outils sont disponibles. Notepad++ est un bon point de départ sur Windows grâce à sa coloration syntaxique et ses plugins. Visual Studio Code est une alternative gratuite et puissante, disponible sur toutes les plateformes, avec des extensions dédiées au XML. Pour une utilisation professionnelle, oXygen XML Editor offre des fonctionnalités avancées comme la validation en temps réel et la transformation XSLT. Les navigateurs web peuvent afficher les fichiers XML mais sans validation ni édition.

---

## Points clés à retenir – Matin J1

- 📚 L'édition numérique adaptée : rendre accessibles les livres aux personnes empêchés de lire
- 🏗️ Les formats structurés : séparation du contenu, de la structure et de la présentation (WYSIWYM)
- 🔤 XML : un langage de balisage extensible et rigoureux
- 📖 Le XML DTBook pour la structuration de livre numérique
- 🛠️ Des outils pour visualiser et éditer du XML

Notes:
Voici les points essentiels à retenir de cette matinée. La clé de l'accessibilité numérique réside dans la qualité de la structuration des documents. Un document bien structuré avec des styles sémantiques peut être converti vers de nombreux formats accessibles. Cet après-midi, nous allons mettre ces connaissances en pratique avec les outils du DAISY Consortium.

---

## Questions ?

**Pause avant l'après-midi →**

_Après-midi : produire et utiliser des fichiers XML DTBook_

Notes:
Prenons quelques minutes pour répondre aux questions avant la pause. Cet après-midi, nous utiliserons DAISY Pipeline et SaveAsDAISY pour convertir des documents Word en XML DTBook.

