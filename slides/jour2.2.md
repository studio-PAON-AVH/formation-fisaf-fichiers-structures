---
title: "Jour 2 – Après-midi : EPUB accessibles en pratique"
---

# Jour 2 – Après-midi

## Produire des EPUBs accessibles

Notes:
Bienvenue dans cette dernière session de la formation. Cet après-midi est entièrement consacré à la pratique : nous allons produire des EPUBs accessibles, les tester et les valider.

---

## Au programme cet après-midi

1. Convertir un fichier EPUB vers Word *(exercice)*
   - Via Calibre/Codex
   - Via WordToEPUB du DAISY Consortium
2. Retour à la structuration dans Word
   - Structuration et métadonnées
3. Générer un EPUB accessible *(exercices)*
   - Via WordToEPUB
   - Via SaveAsDAISY
   - Créer un EPUB Media Overlay
4. Contrôler et valider un EPUB

Notes:
Cet après-midi comprend quatre parties. Nous commençons par voir comment récupérer un fichier Word à partir d'un EPUB existant, puis nous revoyons la structuration dans Word avant de nous concentrer sur la production d'EPUBs accessibles avec deux outils différents. Nous terminerons par la validation technique et d'accessibilité.

---

# Partie 1

## Convertir un EPUB vers Word

Notes:
Cette première partie couvre la conversion dans le sens inverse : partir d'un EPUB existant pour obtenir un fichier Word modifiable. C'est utile lorsqu'on reçoit un EPUB sans le fichier Word source.

---

## Via Calibre/Codex

**Calibre** peut convertir un EPUB en DOCX :

1. Ouvrir Calibre et importer le fichier EPUB
2. Sélectionner le livre → **Convertir les livres**
3. Choisir le **format de sortie : DOCX**
4. Options de conversion :
   - Conserver les styles
   - Convertir les images
   - Structure des chapitres
5. Lancer la conversion
6. *Enregistrer sous un seul format* > *DOCX* > choisir le dossier de sortie

⚠️ La qualité dépend de la structure de l'EPUB source

Notes:
La conversion EPUB vers DOCX via Calibre fonctionne bien pour les EPUBs bien structurés. Le résultat peut nécessiter des ajustements, notamment pour les styles qui ne correspondent pas exactement aux styles Word natifs. Pour les EPUBs Fixed Layout ou avec des mises en page complexes, la conversion sera moins fidèle.

---

## Via WordToEPUB du DAISY Consortium

**[WordToEPUB](https://daisy.org/wordtoepub)**, complément word du DAISY Consortium

- Spécialisé dans la **conversion Word → EPUB 3 accessible**

> **Peut aussi reconvertir un EPUB en Word :**

Outils `EPUBToWord.exe` *caché* dans `C:\Program Files (x86)\DAISY\WordToEPUB`

![outils caché EpubToWord](images/epubtoword.png)

Notes:
C'est un peu moins connu mais WordToEPUB, qui est d'abord un outil de génération d'epub accessible a partir de word, fournis aussi un outil "EPUBToWord" dans son répertoire d'installation.
Selon vos objectifs, cette option peut s'avérer beaucoup plus rapide et pratique si vous n'avez pas besoin de toutes les options de conversions de styles.

---

## 🛠️ Exercice 4

1. Télécharger et installer [WordToEPUB](https://daisy.org/wordtoepub)
2. Récupérer le fichier [`exercice4.epub`](exercices/exercice4.epub)
3. Convertisser le fichier en docx
  - Via Calibre, en fichier `exercice4_calibre.docx`
  - Via WordToEPUB, puis renommer le fichier en `exercice4_WordToEPUB.docx`
4. Ouvrez les fichiers et comparer les résultats.

Notes:
A vous de jouer !

---

## Bonne pratique : conserver vos fichiers

Hormis si le fichier est un manuscrit d'un éditeur

<small>(protégé par le droit d'auteur)</small>

> **Conserver votre fichier Word de travail**  
> C'est la meilleure base pour toute modification ou reconversion.

Flux de travail recommandé :

```
[Source Word structurée] → [EPUB accessible]
         ↑                        ↓
    Modifications          Validation / Corrections
         ↑                        ↓
    [Source Word mise à jour] ← [Retour si nécessaire]
```

Notes:
La conservation du fichier Word source est une règle d'or de la production d'EPUBs. Toute modification ultérieure (correction d'erreur, mise à jour du contenu, reconversion dans un nouveau format) sera beaucoup plus simple et fiable à partir du Word structuré que depuis l'EPUB. Il est recommandé de versionner les fichiers sources et de les archiver systématiquement.

---

# Partie 2

## Retour à la structuration dans Word

Notes:
Avant de générer nos EPUBs, rappelons les règles de structuration dans Word. La qualité de l'EPUB produit dépend directement de la qualité de la structuration du fichier source.

---

## Rappel : structuration dans Word

Les éléments essentiels pour un EPUB de qualité :

| Élément | Règle |
|---------|-------|
| **Titres** | Utiliser les styles Titre 1, 2, 3 |
| **Paragraphes** | Style Corps de texte ou Normal |
| **Listes** | Listes typées (puces/numéros) |
| **Images** | Texte alternatif |
| **Tableaux** | Ligne d'en-tête définie, légende |
| **Notes de bas de page** | Via l'outil Word dédié |

Notes:
Ces règles sont identiques à celles que nous avons vues hier pour la production de DTBook. C'est une force de l'approche WYSIWYM : un document bien structuré dans Word peut être converti en DTBook, en EPUB ou dans d'autres formats avec une bonne qualité. La structuration est faite une seule fois et sert pour tous les formats de sortie.

---

## Les métadonnées pour l'accessibilité

Les métadonnées du document, via Word :

**Fichier → Informations → Propriétés**

<small>et cliquer sur *Montrer toutes les propriétés*</small>

| Métadonnée | Exemple |
|------------|---------|
| **Titre** | Titre du document (obligatoire dans SaveAsDAISY) |
| **Auteur** | Nom de l'auteur |
| **Langue** | Langue principal du document |
| **Entreprise** | correspondance pour l'éditeur du livre|
| **Sujet** | Mots-clés descriptifs |
| **Commentaire** | Résumé de l'ouvrage |

Ces métadonnées seront intégrées dans l'EPUB généré.

Notes:
Les métadonnées Word sont récupérées par les outils de conversion et intégrées dans les fichiers de métadonnées de l'EPUB (content.opf). Il est important de les renseigner correctement avant la conversion. Le titre et la langue sont les plus critiques pour l'accessibilité : le titre sera affiché dans la liseuse et la langue est nécessaire pour la synthèse vocale.

---

## Métadonnées d'accessibilité supplémentaires


Problèmes JOUR 1 : il manque des métadonnées !

**Dans WordToEPUB**

![Les métadonnées dans WordToEPUB](images/wordtoepub-metadata.png)


Inclus des raccourcis vers les métadonnées de word

---

## Métadonnées d'accessibilité supplémentaires

Problèmes JOUR 1 : il manque des métadonnées !

**Dans SaveAsDAISY**

![Les métadonnées dans SaveAsDAISY](images/SAD-metadata.png)

Inclus des raccourcis vers les métadonnées de word

Notes:
Ces métadonnées supplémentaires sont spécifiques à l'accessibilité EPUB. Elles permettent d'indiquer précisément comment le livre peut être lu (mode textuel seulement, ou aussi visuel/auditif), quelles fonctionnalités d'accessibilité il supporte, et à quel niveau de conformité WCAG il répond. WordToEPUB et SaveAsDAISY proposent des interfaces guidées pour renseigner ces informations.

---

# Partie 3

## Générer un EPUB accessible *(exercices)*

Notes:
Passons maintenant à la pratique. Nous allons générer des EPUBs accessibles avec deux outils différents, puis créer un EPUB avec synchronisation audio.

---

## Conversion via WordToEPUB

**WordToEPUB** : conversion Word → EPUB 3 accessible

1. Dans Word, Ouvrez un document
2. Dans l'onglet `Accueil`, cliquez sur `WordToEPUB`
  - Attendez que l'analyse du fichier soit terminé
2. Renseignez les champs `Enregistrer sous` et `Dans le dossier`
3. Ouvrez le `Mode avancé` et configurer les options suivantes :
   - Langue du document
   - Métadonnées de l'ouvrage
   - Options d'accessibilité
4. Cliquer sur **« Convertir »**
5. Télécharger le fichier EPUB généré

✅ Avantage : simple, fichier epub accessible, éditeur de couverture<br/>
❌ controle limité de la sémantique, seulement du texte

Notes:
WordToEPUB est l'outil le plus simple pour produire un EPUB 3 accessible à partir de Word. Il gère automatiquement la structure de l'EPUB, la table des matières, et propose un assistant pour les métadonnées d'accessibilité. Seule limitation : il ne supporte pas les Media Overlays (synchronisation audio). Pour les livres audio structurés, il faudra utiliser SaveAsDAISY.

---

## 🛠️ Exercice 5

**Convertir un Word en EPUB accessible avec WordToEPUB**

1. Ouvrez votre fichier structuré `exercice2_structuré.docx`
2. Ouvrez `WordToEPUB`
3. Vérifier/Renseigner les métadonnées (titre, auteur, langue)
4. Lancer la conversion
5. Ouvrir l'EPUB dans Thorium Reader
6. Tester la navigation (table des matières, titres)

**Durée : 20 minutes**

Notes:
Pour cet exercice, utilisez le fichier exercice4.docx fourni. Après la conversion, testez soigneusement l'EPUB dans Thorium Reader : vérifiez que la table des matières est complète et navigable, que les titres sont bien hiérarchisés, et que les images s'affichent correctement avec leur texte alternatif. Nous utiliserons cet EPUB dans les exercices de validation qui suivent.

---

## Conversion via SaveAsDAISY

**Depuis Word avec le complément SaveAsDAISY :**

1. Ouvrir le document Word structuré
2. Cliquer sur l'onglet **Accessibilité**
3. Sélectionner **Exporter en format DAISY** puis **EPUB3**
4. Cliquez sur **Detailed metadata** et renseignez les métadonnées d'accessibilité
   - Titre, auteur, langue etc.
5. Cliquez sur **Conversion Options** et choisissez vos options de conversion
  - Désactiver l'option *Enable texte-to-speech* pour les essais
6. Cliquez sur **Convert** pour lancer l'export

Notes:
SaveAsDAISY produit également des EPUBs 3 accessibles directement depuis Word. La configuration est similaire à WordToEPUB mais l'interface est intégrée dans Word. Un avantage de SaveAsDAISY est la possibilité de sauvegarder les paramètres de configuration pour les réutiliser lors de conversions ultérieures.

---

## Comparatif compléments Word | WordToEPUB vs SaveAsDAISY

| Critère | WordToEPUB | SaveAsDAISY |
|---------|------------|-------------|
| **Métadonnées d'accessibilité** | ✅ Complet | ✅ Limité |
| **EPUB Media Overlay** | ❌ | ✅ |
| **Autres formats (XML,DAISY,MP3)** | ❌ | ✅ |
| **Accessibilité EPUB** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| **Facilité d'utilisation** | ⭐⭐⭐⭐ | ⭐⭐⭐ |

Notes:
Le choix entre WordToEPUB et SaveAsDAISY dépend de vos besoins. WordToEPUB est plus simple et plus complet en terme de controle sur les métadonnées, ce qui en fait un bon point d'entrée *si vous n'avez besoin que d'un epub texte accessible*.
SaveAsDAISY est moins à jour sur l'accessibilité des EPUB mais il peut générer des Media Overlays pour les livres audio structurés en plus d'autres format de publications ou dy XML DTBook.
Le consortium à pour objectif à terme de réunir les 2 compléments en un seul via SaveAsDAISY pour reconcentrer les ressources en développements, mais aussi pour mettre plus en avant les epub Media Overlay avec audio embarqué.

---

## EPUB Media Overlay – Schéma de fonctionnement

```
[Texte XHTML]          [Fichiers Audio MP3]
     ↓                        ↓
[Fichier SMIL - Synchronisation]
     ↓
[EPUB 3 avec Media Overlay]
     ↓
[Lecture synchronisée dans Thorium / EasyReader]
```

**Usage :** livres audio structurés, ouvrages pour lecteurs avec difficultés de lecture

Notes:

Les EPUB Media Overlay sont une fonctionnalité puissante d'EPUB 3 qui permet de synchroniser le texte avec un enregistrement audio.

Le principe est repris des formats DAISY, qui utilise des fichiers dit SMIL pour synchroniser un segment de texte et un segment d'audio.
Sur les lecteurs compatibles, lors de la lecture, le texte est mis en surbrillance au fur et à mesure de la narration, à la manière d'un karaoké. C'est particulièrement bénéfique pour les personnes dyslexiques et pour l'apprentissage des langues. 

Le fichier SMIL (Synchronized Multimedia Integration Language) est le cœur du Media Overlay. Il contient les références temporelles qui associent chaque segment audio à l'élément XHTML correspondant. SaveAsDAISY génère automatiquement ces fichiers SMIL lors de l'export. Le résultat est lisible dans Thorium Reader et EasyReader, les deux liseuses qui supportent les Media Overlays.

---

## Créer un EPUB Media Overlay 

Dans **SaveAsDAISY**, activer l'option *text-to-speech* :
- *Exporter* / *EPUB3* / *Enable text-to-speech*
- Nécessite des voix de synthèse installer (Microsoft ou autre)


Dans **DAISY Pipeline app**, en repartant d'un dtbook XML
- Script **DTBOOK to EPUB**
- Cocher l'option *Enable text-to-speech*
- CLiquer sur **run** pour lancer la conversion

> **DAISY Pipeline app** recommandé pour plus de choix de fournisseurs de voix

Notes:

Avec les outils utilisant le DAISY Pipeline, tel que SaveAsDAISY, il est possible de générer des epubs media overlay simplement en activant l'option dans le script approprié.

---

## 🛠️ Exercice 5 bis

**Créer un EPUB avec Media Overlay via SaveAsDAISY**

1. Ouvrez a nouveau votre fichier structuré `exercice2_structuré.docx`
2. Lancer l'export en EPUB3 via **SaveAsDAISY**
3. Activer l'option *enable text-to-speech*
4. Lancer la conversion
5. Ouvrir l'EPUB dans Thorium Reader
6. Tester la navigation (table des matières, titres)

**Durée : 25 minutes**

Notes:
Après la génération de l'EPUB, testez la lecture synchronisée dans Thorium Reader : activez l'option de lecture audio et observez comment le texte est mis en surbrillance. Vérifiez également que la navigation par chapitre fonctionne avec la synchronisation audio.

---

# Partie 4

## Contrôler et valider un EPUB

Notes:
La production d'un EPUB ne s'arrête pas à la conversion. Il est indispensable de valider le fichier produit pour s'assurer qu'il est techniquement correct (EPUBCheck) et accessible (ACE). Cette étape de validation fait partie intégrante du workflow de production.

---

## Contrôler un EPUB avec EPUBCheck

**EPUBCheck** est l'outil de validation officiel du W3C

- 🌐 [github.com/w3c/epubcheck](https://github.com/w3c/epubcheck)
- Outil en ligne de commande (Java)
- Vérifie la **conformité technique** au standard EPUB
- Détecte les erreurs de structure, de métadonnées, de liens…


Notes:
EPUBCheck est l'outil de référence pour la validation technique des EPUBs. Il est utilisé par les éditeurs, les bibliothèques et les distributeurs pour vérifier la conformité des fichiers avant publication. Un EPUB qui ne passe pas EPUBCheck sans erreur peut poser des problèmes dans certaines liseuses ou lors de la distribution. EPUBCheck ne vérifie pas l'accessibilité (c'est le rôle d'ACE), mais seulement la conformité technique au standard EPUB.

Nous ne le testeront pas ici, parceque je ne me sens pas de vous faire faire de la ligne de commande.

---

## EPUBCheck – Types d'erreurs détectées

| Type | Exemple |
|------|---------|
| **Erreur fatale** | Archive ZIP corrompue |
| **Erreur** | Fichier manquant référencé dans l'OPF |
| **Avertissement** | Attribut déprécié |
| **Info** | Caractéristique EPUB 3 utilisée |

**Objectif :** 0 erreur, 0 avertissement (ou justifiés)

Notes:
Les erreurs fatales empêchent complètement la lecture de l'EPUB. Les erreurs signalent des non-conformités qui doivent être corrigées. Les avertissements indiquent des pratiques déconseillées qui peuvent poser problème sur certaines liseuses. L'objectif est d'obtenir un rapport EPUBCheck sans erreur ni avertissement, ou en pouvant justifier chaque avertissement restant.

---

## Contrôler un EPUB avec ACE du DAISY Consortium

**ACE** (*Accessibility Checker for EPUB*) est l'outil d'audit d'accessibilité

- 🌐 [daisy.org/ace](https://daisy.org/ace)
- Développé par le DAISY Consortium
- Vérifie la **conformité WCAG** et **EPUB Accessibility**
- Génère un rapport HTML détaillé

**Installation en ligne de commande**
```bash
npm install -g @daisy/ace
ace --version
```
Sinon, télécharger la [**DAISY ACE App**](http://daisy.github.io/ace/getting-started/ace-app/#where-can-i-download-the-ace-app)
  - [Pour Windows](https://github.com/daisy/ace-gui/releases/download/v1.4.6/Ace.by.DAISY.Setup.1.4.6.exe)

Notes:
ACE (Accessibility Checker for EPUB) est le complément d'EPUBCheck pour l'accessibilité. Là où EPUBCheck vérifie la conformité technique, ACE vérifie les critères WCAG et EPUB Accessibility 1.1. ACE est disponible en ligne de commande via npm (Node.js) et génère un rapport HTML très lisible qui détaille chaque violation avec des explications et des recommandations de correction. Il existe aussi une interface graphique ACE App.

---

## ACE – Ce qu'il vérifie

| Critère | Vérification |
|---------|--------------|
| **Images** | Texte alternatif présent |
| **Structure** | Hiérarchie des titres correcte |
| **Langue** | Déclarée dans les métadonnées |
| **Tables** | En-têtes définis |
| **Liens** | Textes descriptifs |
| **Métadonnées** | Propriétés schema.org présentes |
| **Navigation** | Table des matières disponible |
| **Contraste** | Ratio de contraste suffisant |

Notes:
ACE vérifie automatiquement une liste de critères WCAG applicables aux EPUBs. Ces vérifications couvrent les problèmes les plus courants dans les EPUBs mal produits : images sans texte alternatif, structure de titres incohérente, langue non déclarée, métadonnées d'accessibilité manquantes. Certains critères WCAG ne peuvent pas être vérifiés automatiquement (par exemple, la pertinence d'une description alternative) : ACE les signale comme nécessitant une vérification manuelle.

---

## ACE – Rapport de conformité

Le rapport ACE inclut :

- 🔍 **Liste des erreurs et violations** avec score, catégorie et détails
- 🏷️ **Vérification des métadonnées**, y compris d'accessibilité
- 📋 **Structure** du livre analysé (Table des matières)
- 💡 **Images** et texte alternatifs détectés


Notes:
Le rapport HTML généré par ACE est très complet. Il inclut une visualisation de la structure du livre, une liste des violations organisées par critère WCAG, et pour chaque violation une explication et une suggestion de correction. Le rapport peut être partagé avec l'équipe de production ou archivé comme preuve de conformité. ACE génère également un fichier EARL (Evaluation And Report Language) en JSON pour une intégration dans des workflows automatisés.

---

## 🛠️ Exercice 6

**Analyser un EPUB avec ACE**

1. Lancer ACE sur l'epub [`exercice4.epub`](exercices/exercice4.epub)
3. Analyser :
   - Violations détectées
   - Critères WCAG non respectés
   - Métadonnées manquantes
4. Identifier les améliorations possibles
5. Corriger dans le Word source et reconvertir

**Durée : 25 minutes**

Notes:
Pour cet exercice, utilisez l'EPUB de l'exercice 4. Si ACE est installé sur votre machine, exécutez la commande indiquée. Sinon, l'ACE App (interface graphique) peut être utilisée. Après l'analyse, identifiez les trois violations les plus impactantes pour l'accessibilité. Corrigez-les dans le Word source, convertissez à nouveau, et relancez ACE pour vérifier que les violations sont résolues.

---

## Workflow complet de production EPUB accessible


1. Rédaction dans Word
   - (styles + métadonnées + images alt)
2. Vérification Word
   - (vérificateur d'accessibilité intégré)
3. Conversion en EPUB
   - (WordToEPUB ou SaveAsDAISY)
4. Audit accessibilité
   - (ACE → conformité WCAG)
5. Corrections et itérations
6. Publication ✅


Notes:
Ce workflow en six étapes représente la chaîne de production complète d'un EPUB accessible. 
Si des erreurs sont détectées, on corrige le fichier Word source et on recommence. Il est préférable de ne pas chercher à corriger directement dans l'EPUB sauf si ce n'est pas possible autrement : toute modification doit être faite dans le Word source pour garantir la cohérence entre les versions.

---

## Points clés à retenir – Après-midi J2

- 🔄 **Calibre** permet de convertir des EPUBs existants
- 🌐 **WordToEPUB** : outil en ligne simple pour EPUB 3 accessible
- 🔧 **SaveAsDAISY** : production dans Word, supporte les Media Overlays
- ✅ **EPUBCheck** : validation technique obligatoire (0 erreur)
- ♿ **ACE** : audit d'accessibilité complet selon WCAG et EPUB Accessibility

Notes:
Pour résumer cet après-midi : nous avons vu que la production d'un EPUB accessible est un processus itératif qui commence par une bonne structuration dans Word et se termine par une validation complète. Les outils WordToEPUB et SaveAsDAISY automatisent une grande partie du travail, mais la validation reste indispensable.

---

## Récapitulatif des 2 jours

| Session | Contenu |
|---------|---------|
| J1 Matin | Histoire, formats structurés, XML, DTBook |
| J1 Après-midi | DAISY Pipeline, SaveAsDAISY, Word → DTBook |
| J2 Matin | EPUB : formats, accessibilité, logiciels |
| J2 Après-midi | Production EPUB accessible, validation |

Notes:
Ces deux jours vous ont donné les bases théoriques et pratiques pour produire des publications numériques accessibles. Le format XML DTBook reste la référence pour les livres audio structurés, tandis que l'EPUB3 est le format de référence pour l'édition numérique grand public et accessible. Les deux partagent les mêmes principes de structuration sémantique.

---

## Ressources pour aller plus loin

| Ressource | URL |
|-----------|-----|
| **DAISY Consortium** | daisy.org |
| **WordToEPUB** | daisy.org/wordtoepub |
| **Thorium Reader** | edrlab.org/thorium-reader |
| **ACE** | daisy.org/ace |
| **EPUBCheck** | github.com/w3c/epubcheck |
| **EPUB Accessibility 1.1** | w3.org/TR/epub-a11y-11 |
| **WCAG 2.1** | w3.org/TR/WCAG21 |

Notes:
Ces ressources vous permettront de continuer à approfondir vos connaissances après la formation. Le site du DAISY Consortium propose notamment une base de connaissance très complète (kb.daisy.org) et inclusivepublishing.org propose des formations et ressources en ligne sur l'édition inclusive.

---

## C'est tout pour moi ! 🎉

_Questions ? [Contactez-moi](mailto:n.pavie@avh.asso.fr) !_

> (La suite avec M. Chomel pour InDesign)

Notes:
Et ce sera tout pour moi sur cette sessions, j'espère vous avoir appris des choses utilises.
N'hésitez pas à nous contacter si vous avez des questions après la formation. 
