---
title: "Jour 1 – Après-midi : XML DTBook en pratique"
---

# Jour 1 – Après-midi

## Produire et utiliser  
## des fichiers XML DTBook

Notes:
Bienvenue dans la session pratique de ce premier après-midi. Nous allons mettre en œuvre les connaissances acquises ce matin en utilisant les outils du DAISY Consortium pour produire et manipuler des fichiers XML DTBook.

---

## Au programme cet après-midi

1. Les logiciels du DAISY Consortium pour produire du XML DTBook
   - DAISY Pipeline App
   - Le complément Word SaveAsDAISY
2. Du XML DTBook à Word *(exercices pratiques)*
3. Structurer un document dans Word *(exercices pratiques)*
4. Convertir un fichier Word en XML DTBook *(exercices pratiques)*

Notes:
Cet après-midi est organisé en quatre parties. Nous commençons par une présentation des outils, puis nous enchaînons avec trois exercices pratiques progressifs : d'abord comprendre un fichier DTBook existant en le convertissant en Word, puis structurer un document Word correctement, et enfin le convertir en XML DTBook.

---

## Retour sur le matin

- Le XML DTBook est un format structuré pour les livres accessibles
- Il utilise des balises sémantiques (`<level1>`, `<h1>`, `<p>`…)
- On peut le lire avec un éditeur texte ou un outil XML

**Aujourd'hui : mettons-le en pratique ! 🛠️**

Notes:
Pour rappel, le XML DTBook est le format numérique développé par le DAISY Consortium pour les livres accessibles. Sa structure hiérarchique (level1 à level6) correspond aux chapitres et sections d'un ouvrage. Aujourd'hui nous allons voir comment produire ce format à partir de documents Word, et inversement.

---

# Partie 1

## Les logiciels du DAISY Consortium

Notes:
Le DAISY Consortium propose plusieurs outils gratuits et open source pour la production de publications accessibles. Nous allons nous concentrer sur les deux outils principaux utilisés dans notre chaîne de production : DAISY Pipeline et SaveAsDAISY.

---

## 1.a – DAISY Pipeline App

**DAISY Pipeline** est une application de conversion de documents accessibles

- 🌐 Site : [daisy.org/pipeline](https://daisy.org/pipeline)
- 💻 Disponible sur Windows, macOS, Linux
- 🔄 Convertit entre de nombreux formats :
  - DTBook → EPUB 3
  - DTBook → MP3 (synthèse vocale)
  - DOCX → EPUB 3
  - et bien d'autres…

Notes:
DAISY Pipeline est l'outil de transformation central du DAISY Consortium. Il fonctionne sur la base de scripts de transformation XSLT et propose une interface graphique simple pour les utilisateurs non techniques. Il peut traiter des fichiers par lots, ce qui est très utile pour les centres de transcription qui produisent de nombreux ouvrages.

---

## DAISY Pipeline – Fonctionnement

```
[Fichier source]
      ↓
[DAISY Pipeline App]
      ↓
  ┌───────────┐
  │ Script de │
  │ conversion│
  └───────────┘
      ↓
[Fichier de sortie]
```

- Interface graphique simple
- Scripts de transformation préconfigurés
- Traitement par lots possible

Notes:
Le fonctionnement de DAISY Pipeline est basé sur des scripts de transformation. Chaque script correspond à une conversion entre deux formats. L'utilisateur choisit le script approprié, fournit le fichier source et le dossier de destination, et lance la conversion. Le traitement par lots permet de convertir plusieurs fichiers en une seule opération.

---

## 1.b – Le complément Word SaveAsDAISY

**SaveAsDAISY** est un complément Microsoft Word

- 🌐 Site : [daisy.org/save-as-daisy-microsoft-word-add-in](https://daisy.org/save-as-daisy-microsoft-word-add-in)
- 🖥️ Compatible Word 2010 – 2019 / Office 365
- ⚙️ Ajoute un onglet **« DAISY »** dans Word

**Fonctionnalités :**
- Exporter un document Word en XML DTBook
- Exporter en EPUB 3
- Vérifier la structure du document
- Ajouter des styles spécifiques DAISY

Notes:
SaveAsDAISY est un complément qui s'installe directement dans Microsoft Word. Une fois installé, il ajoute un nouvel onglet « DAISY » dans le ruban de Word, accessible depuis lequel vous pouvez exporter vers différents formats accessibles. C'est l'outil le plus simple pour un producteur qui travaille déjà dans Word, car il ne nécessite pas de changer d'application.

---

## SaveAsDAISY – Onglet DAISY dans Word

Fonctions disponibles depuis le ruban Word :

| Bouton | Action |
|--------|--------|
| **Exporter DTBook** | Génère un fichier XML DTBook |
| **Exporter EPUB** | Génère un fichier EPUB 3 |
| **Vérifier** | Contrôle la structure du document |
| **Styles DAISY** | Applique les styles recommandés |

Notes:
L'onglet DAISY propose quatre fonctions principales. La vérification est particulièrement utile avant l'export : elle signale les problèmes de structure qui pourraient nuire à la qualité de la conversion. Les styles DAISY étendent les styles Word natifs avec des styles spécifiques à l'édition accessible, comme les notes de production ou les encadrés.

---

# Partie 2

## Du XML DTBook à Word *(exercices)*

Notes:
Dans cette partie, nous allons voir comment récupérer des fichiers DTBook et les convertir en Word pour les modifier ou les utiliser comme base de travail.

---

## 2.a – Où récupérer des fichiers DTBook ?

Sources de fichiers XML DTBook :

| Source | Description |
|--------|-------------|
| **Médiathèque Valentin Haüy** | Bibliothèque numérique française |
| **Bookshare** | Bibliothèque internationale (en anglais) |
| **BNFA** | Bibliothèque Numérique Francophone Accessible |
| **DAISY Consortium** | Fichiers d'exemple sur daisy.org |
| **Productions locales** | Fichiers produits par les centres de transcription |

Notes:
Les fichiers DTBook proviennent principalement des bibliothèques spécialisées et des centres de transcription. La Médiathèque Valentin Haüy et la BNFA sont les deux principales sources francophones. Bookshare est la plus grande bibliothèque internationale mais ses collections sont majoritairement en anglais. Le DAISY Consortium propose des fichiers d'exemple sur son site pour la formation et les tests.

---

## 2.b – Convertir un DTBook en fichier Word

**Via DAISY Pipeline App :**

1. Lancer DAISY Pipeline App
2. Choisir le script **« DTBook to DOCX »**
3. Sélectionner le fichier DTBook source (`.xml`)
4. Définir le dossier de sortie
5. Lancer la conversion
6. Ouvrir le fichier `.docx` généré dans Word

Notes:
La conversion DTBook vers Word via DAISY Pipeline préserve la structure sémantique du fichier : les éléments level1/h1 deviennent des Titres 1 Word, les level2/h2 des Titres 2, etc. Les listes, tableaux et images sont également convertis. Il peut subsister des ajustements à faire manuellement, notamment pour les mises en page complexes.

---

## 🛠️ Exercice 1

**Convertir un fichier DTBook en Word**

1. Ouvrir DAISY Pipeline App
2. Charger le fichier `exercice1.xml` fourni
3. Choisir le script de conversion DTBook → DOCX
4. Exécuter la conversion
5. Ouvrir le fichier Word résultant
6. Observer la structure : styles, titres, paragraphes

**Durée : 15 minutes**

Notes:
Pour cet exercice, vous disposez d'un fichier DTBook préparé à l'avance. L'objectif est de se familiariser avec l'interface de DAISY Pipeline et d'observer comment la structure XML se traduit en styles Word. Prenez le temps d'explorer le fichier Word résultant : vérifiez le panneau de styles et la table des matières.

---

# Partie 3

## Structurer un document dans Word *(exercices)*

Notes:
La qualité d'un fichier DTBook ou EPUB dépend directement de la qualité de la structuration du document Word source. Cette partie est essentielle : une bonne structuration dès la saisie évite de nombreux problèmes lors de la conversion.

---

## 3.a – Les règles d'accessibilité d'un document Word

**Règles fondamentales :**

1. 🏷️ **Styles de titres** : utiliser Titre 1, Titre 2, Titre 3… (jamais du gras seul)
2. 🖼️ **Images** : toujours renseigner le texte alternatif
3. 📋 **Listes** : utiliser les listes automatiques (pas de tirets manuels)
4. 📊 **Tableaux** : définir les en-têtes de colonnes
5. 🔗 **Liens** : un texte descriptif (pas « cliquez ici »)
6. 🌐 **Langue** : indiquer la langue du document
7. 📄 **Métadonnées** : titre, auteur, description

Notes:
Ces sept règles constituent la base de l'accessibilité d'un document Word. La plus importante est l'utilisation des styles de titres : sans eux, il n'y a pas de structure sémantique et la conversion ne peut pas produire un DTBook ou un EPUB de qualité. Le vérificateur d'accessibilité intégré à Word (Révision → Vérifier l'accessibilité) peut aider à identifier les problèmes.

---

## Structure hiérarchique recommandée

```
Document Word
├── Titre 1 : Chapitre 1
│   ├── Titre 2 : Section 1.1
│   │   └── Titre 3 : Sous-section 1.1.1
│   └── Titre 2 : Section 1.2
├── Titre 1 : Chapitre 2
│   └── Titre 2 : Section 2.1
└── Titre 1 : Conclusion
```

**Important :** Ne pas sauter de niveau (pas de Titre 3 après Titre 1) !

Notes:
La hiérarchie des titres doit être respectée sans sauter de niveaux. Un Titre 3 doit toujours être précédé d'un Titre 2, lui-même précédé d'un Titre 1. Sauter des niveaux (par exemple passer directement de Titre 1 à Titre 3) crée des incohérences dans la structure qui seront répercutées dans le DTBook et l'EPUB, et peuvent nuire à la navigation.

---

## 3.b – Les styles SaveAsDAISY

En plus des styles Word natifs, SaveAsDAISY ajoute :

| Style | Usage |
|-------|-------|
| **DAISY Note** | Note de bas de page enrichie |
| **DAISY Annotation** | Annotation du transcripteur |
| **DAISY Sidebar** | Encadré informatif |
| **DAISY Poem** | Poème (préserve les retours à la ligne) |
| **DAISY Epigraph** | Citation en exergue |
| **DAISY Prodnote** | Note de production (pour le transcripteur) |

Notes:
Les styles DAISY étendent les possibilités de structuration de Word pour couvrir des éléments spécifiques à l'édition adaptée. Le style DAISY Prodnote est particulièrement important : il permet au transcripteur d'ajouter des informations qui ne figurent pas dans le texte original mais qui sont nécessaires pour l'accessibilité, comme la description d'une image complexe. Ces notes de production ne sont pas lues dans l'édition grand public.

---

## 🛠️ Exercice 2

**Structurer un document Word pour la conversion DTBook**

1. Ouvrir le fichier `exercice2.docx` (document non structuré)
2. Appliquer les **styles de titres** corrects (Titre 1, 2, 3…)
3. Structurer les **listes** automatiquement
4. Ajouter les **textes alternatifs** des images
5. Renseigner les **métadonnées** (Fichier → Propriétés)
6. Vérifier avec le **Vérificateur d'accessibilité** Word

**Durée : 30 minutes**

Notes:
Ce document d'exercice contient intentionnellement des problèmes de structuration : titres mis en gras sans style, listes créées avec des tirets manuels, images sans texte alternatif. Votre objectif est de corriger tous ces problèmes en appliquant les règles vues précédemment. Utilisez le vérificateur d'accessibilité de Word pour vous assurer de n'avoir rien oublié.

---

# Partie 4

## Convertir un fichier Word en XML DTBook *(exercices)*

Notes:
Cette dernière partie boucle le cycle de production : après avoir structuré notre document Word, nous allons l'exporter en XML DTBook et vérifier le résultat.

---

## Processus de conversion Word → DTBook

```
[Document Word structuré]
         ↓
  [SaveAsDAISY Add-in]
   Onglet DAISY → Exporter DTBook
         ↓
   [Vérification]
   Structure correcte ?
         ↓
[Fichier XML DTBook généré]
```

Notes:
Le processus de conversion est simple lorsque le document Word est correctement structuré. SaveAsDAISY lit les styles Word et les traduit en éléments DTBook correspondants. La vérification intégrée de SaveAsDAISY peut détecter certains problèmes avant l'export, mais il est préférable d'utiliser d'abord le vérificateur d'accessibilité Word.

---

## Bonnes pratiques avant la conversion

Checklist avant d'exporter :

- ☑ Tous les titres utilisent les styles Word Titre 1/2/3…
- ☑ Pas de mise en forme manuelle à la place des styles
- ☑ Toutes les images ont un texte alternatif
- ☑ Les listes sont automatiques
- ☑ La langue du document est définie
- ☑ Les métadonnées (titre, auteur) sont renseignées
- ☑ Le vérificateur d'accessibilité Word ne signale pas d'erreur

Notes:
Cette checklist doit être complétée avant chaque export. Il vaut mieux prendre quelques minutes pour vérifier ces points que de découvrir des problèmes dans le fichier DTBook généré. La règle d'or : si le vérificateur d'accessibilité Word signale des erreurs, corrigez-les avant d'exporter.

---

## 🛠️ Exercice 3

**Convertir le document Word en XML DTBook**

1. Ouvrir le document structuré de l'exercice 2
2. Cliquer sur l'onglet **DAISY** dans Word
3. Cliquer sur **« Exporter DTBook »**
4. Choisir le dossier de destination
5. Ouvrir le fichier `.xml` généré dans un éditeur
6. Vérifier la structure XML produite

**Durée : 20 minutes**

Notes:
Pour cet exercice, utilisez le document que vous avez structuré lors de l'exercice 2. Une fois le DTBook généré, ouvrez-le dans Notepad++ ou Visual Studio Code et examinez sa structure : vérifiez que les niveaux level1/level2 correspondent bien aux titres Word, que les images ont bien un élément imggroup avec une description, et que les métadonnées sont correctement renseignées dans l'en-tête.

---

## Points clés à retenir – Après-midi J1

- 🔧 **DAISY Pipeline** convertit entre de nombreux formats accessibles
- 📝 **SaveAsDAISY** intègre la conversion directement dans Word
- 🏗️ La **structuration Word** (styles de titres) est la clé d'une bonne conversion
- ✅ Le **vérificateur d'accessibilité** Word est un allié précieux
- 📄 Le XML DTBook généré reflète fidèlement la structure du Word source

Notes:
Pour résumer cette après-midi : la qualité du fichier DTBook ou EPUB produit est directement proportionnelle à la qualité de la structuration du document Word source. Les outils ne peuvent pas compenser une mauvaise structuration. L'investissement dans la structuration dès la saisie est toujours rentable à long terme.

---

## Récapitulatif de la journée 1

| Session | Contenu |
|---------|---------|
| Matin | Histoire de l'édition accessible, XML, DTBook |
| Après-midi | Outils DAISY, conversion Word↔DTBook, structuration |

**Demain : le format EPUB ! 📱**

Notes:
Nous avons couvert aujourd'hui les bases théoriques et pratiques de l'édition adaptée avec le format XML DTBook. Demain matin, nous aborderons le format EPUB3, son histoire, et les outils disponibles. L'après-midi sera consacrée à la production d'EPUBs accessibles et à leur validation.
