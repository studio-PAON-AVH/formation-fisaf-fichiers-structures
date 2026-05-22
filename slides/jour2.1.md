---
title: "Jour 2 – Matin : Le format EPUB"
---

# Jour 2 – Matin

## Le format EPUB

Notes:
Bienvenue dans cette deuxième journée de formation. Ce matin nous allons découvrir le format EPUB3, son histoire, les différents types d'EPUBs, les standards d'accessibilité associés, et les principaux logiciels pour lire et produire des EPUBs.

---

## Au programme ce matin

> Retour / Questions sur la journée 1

2. Histoire de l'EPUB comme publication accessible
   - Qu'est-ce qu'un EPUB ?
   - Les différents types d'EPUB
   - L'accessibilité numérique
   - Les EPUB accessibles
3. Les logiciels pour lire et produire un EPUB
   - Lire : Thorium, EasyReader, Calibre
   - Produire : Calibre/Codex, Sigil

Notes:
Ce matin couvre à la fois la théorie (l'EPUB et l'accessibilité) et la découverte des outils. Cet après-midi sera entièrement pratique : nous produirons des EPUBs accessibles et les validerons.

---

## Retour sur la journée 1

- **Matin** : histoire de l'édition accessible, formats XML, DTBook
- **Après-midi** : DAISY Pipeline, SaveAsDAISY, structuration Word

**Des questions ? Des points à revoir ?**

Notes:
Prenons quelques minutes pour revenir sur la journée d'hier. Avez-vous des questions sur les formats XML, le DTBook ou les exercices de structuration Word ? C'est le bon moment pour clarifier avant d'aborder un nouveau format.

---

# Partie 1

## Histoire de l'EPUB comme publication accessible

Notes:
L'EPUB est aujourd'hui le format de référence pour l'édition numérique accessible. Comprendre son histoire et sa structure nous permet de mieux appréhender ses possibilités et ses contraintes.

---

## C'est quoi un EPUB ?

**EPUB** : *Electronic PUBlication*

- Format standard créé et maintenu par l'**IDPF** (fusionné avec le W3C en 2017)
- Un EPUB = une **archive ZIP** contenant :
  - Des fichiers XHTML (le contenu)
  - Des fichiers CSS (la mise en forme)
  - Des images, polices, médias
  - Des fichiers de métadonnées (OPF, NCX/NAV)

```
monlivre.epub
├── mimetype
├── META-INF/
│   └── container.xml
└── OEBPS/
    ├── content.opf
    ├── nav.xhtml
    ├── chapitre01.xhtml
    └── styles.css
```

Notes:
Un EPUB est fondamentalement une archive ZIP avec une extension renommée. On peut l'ouvrir avec n'importe quel logiciel de décompression pour voir les fichiers qui le composent. Le fichier content.opf (OPF = Open Packaging Format) est le manifeste qui liste tous les fichiers et leur rôle. Le fichier nav.xhtml est la table des matières navigable. Les fichiers XHTML contiennent le texte du livre.

---

## Chronologie de l'EPUB

| Année | Événement |
|-------|-----------|
| **1999** | OEB (Open eBook) – premier standard |
| **2007** | EPUB 2.0 – première version "EPUB" |
| **2011** | EPUB 3.0 – support multimédia, MathML |
| **2014** | EPUB 3.0.1 – corrections et clarifications |
| **2017** | IDPF fusionne avec le W3C |
| **2017** | EPUB Accessibility 1.0 |
| **2022** | EPUB 3.3 – standard W3C officiel |
| **2023** | EPUB Accessibility 1.1 |

Notes:
L'EPUB a une longue histoire qui remonte à 1999 avec le format Open eBook. La transition vers EPUB 3 en 2011 a été majeure : elle a apporté le support HTML5 et CSS3, les Media Overlays pour la synchronisation texte-audio, MathML pour les mathématiques, et SVG pour les graphiques. EPUB 3.3 est la version actuelle, maintenue par le W3C depuis la fusion avec l'IDPF en 2017.

---

## Les différents types d'EPUB

### EPUB Reflow (recomposable)

- Le texte **s'adapte** à la taille de l'écran
- Idéal pour les **textes longs** (romans, essais)
- Taille de police modifiable par l'utilisateur
- **Le plus courant et le plus accessible**


Notes:
La distinction entre EPUB Reflow et Fixed Layout est fondamentale pour l'accessibilité. L'EPUB Reflow est de loin le plus accessible : l'utilisateur peut adapter la taille de police, les couleurs, l'interlignage selon ses besoins. Le Fixed Layout impose une mise en page figée qui peut rendre la lecture très difficile sur un petit écran ou pour les utilisateurs de lecteurs d'écran. Dans notre contexte d'édition adaptée, nous nous concentrons sur le Reflow.

---

## Les différents types d'EPUB


### EPUB Fixed Layout (Mise en page fixe)

- Mise en page **identique** quelle que soit la taille d'écran
- Idéal pour les **livres illustrés**, BD, livres enfants
- Moins accessible (texte non redimensionnable)
- Similaire à un PDF enrichi

Notes:
La distinction entre EPUB Reflow et Fixed Layout est fondamentale pour l'accessibilité. L'EPUB Reflow est de loin le plus accessible : l'utilisateur peut adapter la taille de police, les couleurs, l'interlignage selon ses besoins. Le Fixed Layout impose une mise en page figée qui peut rendre la lecture très difficile sur un petit écran ou pour les utilisateurs de lecteurs d'écran. Dans notre contexte d'édition adaptée, nous nous concentrons sur le Reflow.

---

## Comparatif Reflow / Fixed Layout

| Critère | Reflow | Fixed Layout |
|---------|--------|--------------|
| Adaptation écran | ✅ Oui | ❌ Non |
| Taille police réglable | ✅ Oui | ❌ Non |
| Accessibilité | ✅ Bonne | ⚠️ Limitée |
| Mise en page complexe | ❌ Limitée | ✅ Précise |
| Usage typique | Romans, essais | BD, livres illustrés |

Notes:
Ce tableau résume les différences entre les deux types d'EPUB. Pour l'édition adaptée, le choix se portera presque toujours sur le Reflow. Si vous recevez un EPUB Fixed Layout à adapter, il faudra le convertir en Reflow et restructurer le contenu, ce qui représente un travail significatif.

---

## L'accessibilité numérique

### Le cadre réglementaire

- **RGAA** (France) : Référentiel Général d'Amélioration de l'Accessibilité
- **Directive européenne** 2016/2102 : accessibilité des sites publics
- **Loi du 11 février 2005** (France) : non-discrimination des personnes handicapées
- **Acte européen sur l'accessibilité** (2019/2025) : livres numériques inclus !

Notes:
L'accessibilité numérique est de plus en plus encadrée par la réglementation. 
L'Acte européen sur l'accessibilité est particulièrement important pour notre domaine : à partir de juin 2025, les livres numériques mis en vente dans l'Union européenne devront répondre à des critères d'accessibilité. 
Cela crée une obligation légale et un marché potentiel pour l'expertise en édition adaptée.

---

## Les standards d'accessibilité numérique

| Standard | Description |
|----------|-------------|
| **[WCAG 2.1/2.2](https://www.w3.org/Translations/WCAG22-fr/)** | Web Content Accessibility Guidelines (W3C) |
| **[EPUB Accessibility 1.1](https://www.w3.org/TR/epub-a11y-11/)** | Profil d'accessibilité pour les EPUBs |
| **[ARIA](https://www.w3.org/TR/wai-aria/)** | Rôles et propriétés pour l'accessibilité web |
| **EN 301 549** | Norme européene d'accessibilité des TIC |

Notes:
Les WCAG (Web Content Accessibility Guidelines) sont la référence internationale pour l'accessibilité numérique. 
Elles s'organisent en trois niveaux : A (minimum), AA (standard courant) et AAA (optimal).
L'EPUB Accessibility 1.1 est un profil spécifique aux EPUBs qui exige la conformité WCAG 2.1 niveau AA. 
Le standard ARIA définit une liste d'attributs pouvant être ajouter aux éléments du (x)html pour en améliorer ou corriger l'accessibilité.

La norme EN 301 549 (v3.2.1 depuis Mars 2021) est la norme européen qui référence les WCAG 2.1 pour les publications numériques dans le cas des marché publiques.
(Mais cette norme ne s'applique pas qu'au publications numériques) 


---

## Les EPUB accessibles

Un EPUB accessible c'est :

- 📖 **Texte alternatif** sur toutes les images
- 🏷️ **Structure sémantique** : titres, listes, tableaux balisés
- 🌐 **Langue** déclarée dans les métadonnées
- 📋 **Table des matières** navigable (NCX / NAV)
- ♿ **Métadonnées d'accessibilité** (schema.org)
- 🎵 **Synchronisation audio** (Media Overlays pour EPUB 3)

Notes:
Un EPUB accessible n'est pas seulement un EPUB techniquement valide. Il doit répondre à des critères qui permettent à tous les utilisateurs, quelles que soient leurs capacités ou leurs technologies d'assistance, d'y accéder dans des conditions équivalentes. La synchronisation audio via les Media Overlays est particulièrement précieuse pour les personnes dyslexiques ou malvoyantes.

---

## Les métadonnées d'accessibilité EPUB

Dans le fichier `content.opf` :

```xml
<meta property="schema:accessibilitySummary">
  Cet ouvrage est conforme aux critères d'accessibilité EPUB.
</meta>
<meta property="schema:accessMode">textual</meta>
<meta property="schema:accessMode">visual</meta>
<meta property="schema:accessModeSufficient">textual</meta>
<meta property="schema:accessibilityFeature">structuralNavigation</meta>
<meta property="schema:accessibilityFeature">alternativeText</meta>
<meta property="schema:accessibilityHazard">none</meta>
<meta property="schema:conformsTo">
  EPUB Accessibility 1.1 - WCAG 2.1 Level AA
</meta>
```

Notes:
Ces métadonnées schema.org permettent aux lecteurs et aux bibliothèques d'identifier rapidement les caractéristiques d'accessibilité d'un EPUB sans avoir à l'ouvrir. Elles alimentent les catalogues et aident les utilisateurs à trouver des livres adaptés à leurs besoins. Les outils WordToEPUB et SaveAsDAISY génèrent automatiquement la plupart de ces métadonnées si vous les configurez correctement lors de la conversion.

---

## Comparaison entre EPUB et DAISY

Quid des formats DAISY ?

**DAISY2** très répandu
  - 📖 Format de publication "historique" du DAISY Consortium
  - ⛔ Options de lecture limitée (i.e. contenu évitable)
  - Application / matériel spécialisés


Notes:
Vous avez peut etre remarquer que nous n'avons pas beaucoup reparler des 
autres formats dont nous avons parler hier, notamment les formats de publication
du DAISY consortium.

Le DAISY2 ou DAISY2.02 est le format le plus ancien et celui que nous distribuons a l'AVH.
C'est le format historique du DAISY Consortium, pour lequel un grand nombre d'usager aveugles ou malvoyants possède du matériel compatible.
Ce format pose cependant quelques problemes, qui sont pour une partie lié aux technologies utilisé par le format pour la structuration du contenu.
Vous avez du coup des limitations sur certaines options de navigation, notamment pour le contenu "évitable" tel que les notes de bas de pages, qui sont généralement structurés au même niveau que le contenu


---

## Comparaison entre EPUB et DAISY

Quid des formats DAISY ?


**DAISY3**, mieux qu'avant mais moins répandu
  - Plus de sémantique embarquée
    - XML DTBook pour le contenu texte
    - Plus d'options de lecture
  - Application / matériel spécialisés



Notes:

Le DAISY3 corrige des probleme du DAISY2, surtout du point des éléments skipables, mais pour ça il utilise un format de contenu beacuoup plus contraint qui est le XML DTBook

---

## Comparaison entre EPUB et DAISY

Quid des formats DAISY ?

**EPUB3**, un format qui évolue
  - Plus de liberté sans sacrifier l'accessibilité
  - Cible/public plus large
  - Mais manque encore de support pour les malvoyants


Notes:

Si nous nous concentrons aujourd'hui sur l'EPUB3, c'est d'abord parceque le 
format continue a évoluer, et le DAISY Consortium fait le pari que ce format
sera plus facile a faire adopter aux fabricants de logiciels et de matériel spécialisé, 
celui-ci étant déjà répandu pour les publications numériques de nombreux éditeurs de par le monde.

---

# Partie 2

## Les logiciels pour lire et produire un EPUB

Notes:
Dans cette partie, nous allons passer en revue les principaux logiciels disponibles pour lire, produire et éditer des EPUBs. Ces outils seront utilisés lors des exercices de l'après-midi.

---

## Lire des EPUBs

### Thorium Reader

- 🌐 [edrlab.org/thorium-reader](https://www.edrlab.org/thorium-reader/)
- Développé par EDRLab (France)
- **Accessible** : lecteurs d'écran, navigation clavier
- Support EPUB 3, PDF, audiobooks, DAISY
- Disponible Windows, macOS, Linux
- **Recommandé pour les tests d'accessibilité**

Notes:
Thorium Reader est développé par EDRLab, le European Digital Reading Lab, basé à Paris. C'est aujourd'hui la référence en matière de liseuse EPUB accessible. Il est utilisé par de nombreuses bibliothèques et établissements scolaires. Pour nos tests d'accessibilité, c'est l'outil idéal car il supporte toutes les fonctionnalités EPUB 3 : Media Overlays, TTS, personnalisation de l'affichage.

---

## Thorium Reader – Fonctionnalités clés

| Fonctionnalité | Description |
|----------------|-------------|
| Navigation structurée | Table des matières, repères |
| Personnalisation | Police, taille, espacement, couleurs |
| Audio | TTS (synthèse vocale), Media Overlays |
| Recherche | Plein texte dans le livre |
| Annotations | Surlignages et notes personnelles |
| Accessibilité | NVDA, JAWS, VoiceOver compatibles |

Notes:
Thorium Reader offre de nombreuses possibilités de personnalisation qui sont essentielles pour les personnes avec des difficultés visuelles ou cognitives. La compatibilité avec les lecteurs d'écran NVDA (Windows), JAWS (Windows) et VoiceOver (macOS/iOS) en fait l'outil de référence pour tester l'accessibilité d'un EPUB.

---

## EasyReader

- 🌐 [yourdolphin.com](https://www.yourdolphin.com/)
- Pour les personnes déficientes visuelles
- Support EPUB et DAISY
- Interface simplifiée et très accessible
- Connexion aux bibliothèques numériques

Notes:
EasyReader est une application spécialement conçue pour les personnes déficientes visuelles. 
Son interface est simplifiée et son intégration avec les bibliothèques numériques comme Bookshare et la BNFA en fait un outil apprécié des usagers. Il est disponible sur Windows, macOS, iOS et Android. Il existe une version gratuite limitée et une version complète payante.

---

## Calibre

- 🌐 [calibre-ebook.com](https://calibre-ebook.com/)
- Logiciel libre et gratuit
- Gestion de bibliothèque numérique
- **Conversions** entre formats (EPUB, MOBI, PDF, DOCX…)
- Visionneuse intégrée
- Éditeur de métadonnées

Notes:
Calibre est un logiciel de gestion de bibliothèque numérique très complet et gratuit. Sa capacité de conversion entre de nombreux formats en fait un outil précieux, même si la qualité des conversions peut varier selon les fichiers source. Il intègre également un éditeur EPUB (Codex) que nous allons voir maintenant.

---

## Calibre/Codex

**Codex** est l'éditeur EPUB intégré à Calibre :

- Accessible depuis Calibre via **Éditer le livre**
- Édition directe des fichiers XHTML, CSS, OPF
- Vue triée par type des fichiers de l'EPUB
- Aperçu en temps réel
- Outils de nettoyage et validation

Notes:
L'éditeur Codex intégré à Calibre permet d'ouvrir et de modifier directement les fichiers internes d'un EPUB. C'est utile pour des corrections ciblées qu'il serait difficile de faire autrement : supprimer un style CSS problématique, corriger une métadonnée, ajouter un attribut d'accessibilité manquant. Il n'est pas recommandé pour créer un EPUB de zéro.

**Usage typique :**
- Corrections mineures après conversion
- Ajout/modification de métadonnées
- Vérification de la structure interne

---


## Sigil + PageEdit

- 🌐 [sigil-ebook.com](https://sigil-ebook.com/)
- Éditeur EPUB libre et gratuit (Windows, macOS, Linux)
- Spécialisé dans la **création et l'édition d'EPUBs**
- Vue code dans SIGIL, liaison avec PageEdit pour WYSIWYG
  - *SIGIL > Edition > Preferences > Paramètres généraux > Editeurs XHTML externe*
  - *SIGIL > Lancer l'éditeur XHTML Externe*
- Gestion de la table des matières + prévisualisation
- Plugins pour l'accessibilité et la validation
  - [ACE dans SIGIL](https://www.mobileread.com/forums/showthread.php?t=294678)
  - [Access-Aide](https://www.mobileread.com/forums/showthread.php?t=294900)

Notes:
Sigil est un éditeur EPUB dédié, plus complet que Codex pour la création et l'édition avancée d'EPUBs.
L'equipe de SIGIL a décider depuis peu de sortir leur éditeur WYSIWYG pour en faire une application externe, mais vous pouvez relier les 2 via les paramètres de SIGIL.
(Si installation locale, PageEdit sera ici : `%LOCALAPPDATA%\Programs\PageEdit\PageEdit.exe`)

L'affichage des fichiers dans SIGIL est un peu moins "clean" que celui de calibre mais vous avez accès à des compléments/plugins pour l'accessibilité.

---

## Comparatif des logiciels

| Logiciel | Lire | Produire | Convertir | Gratuit |
|----------|------|----------|-----------|---------|
| **Thorium Reader** | ✅ | ❌ | ❌ | ✅ |
| **EasyReader** | ✅ | ❌ | ❌ | ✅ (+💰premium) |
| **Calibre** | ✅ | ⚠️ | ✅ | ✅ |
| **Sigil** | ✅ | ✅ | ❌ | ✅ |

Notes:
Ce tableau récapitulatif vous aide à choisir le bon outil selon votre besoin.
Pour la lecture et les tests, Thorium Reader est incontournable. 
Pour la production à partir de Word, SaveAsDAISY ou WordToEPUB sont recommandés. Pour les corrections ciblées sur un EPUB existant, Calibre/Codex ou Sigil sont adaptés.

---

## Points clés à retenir – Matin J2

- 📦 L'EPUB est une archive ZIP contenant du XHTML, CSS et des métadonnées
- 🔄 EPUB 3.3 est le standard actuel maintenu par le W3C
- ♿ L'EPUB accessible suit les critères WCAG et EPUB Accessibility 1.1
- 📱 Thorium Reader est la référence pour lire et tester les EPUBs accessibles
- 🛠️ Calibre/Sigil permettent de créer et éditer des EPUBs

Notes:
Pour résumer cette matinée : l'EPUB est le format de référence pour l'édition numérique accessible, et son écosystème s'est considérablement enrichi ces dernières années avec des outils gratuits et performants. Cet après-midi, nous allons utiliser ces outils pour produire et valider des EPUBs accessibles.

---

## Questions ?

**Pause déjeuner →**

_Après-midi : produire des EPUBs accessibles_

Notes:
Prenons quelques minutes pour les questions avant la pause déjeuner. Cet après-midi, nous commencerons directement par les exercices de production d'EPUBs accessibles avec WordToEPUB et SaveAsDAISY.
