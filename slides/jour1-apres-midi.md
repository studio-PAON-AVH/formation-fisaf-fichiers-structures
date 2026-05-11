---
title: "Jour 1 – Après-midi : XML DTBook en pratique"
---

# Jour 1 – Après-midi

## Produire et utiliser  
## des fichiers XML DTBook

---

## Au programme cet après-midi

1. Les logiciels du DAISY Consortium pour produire du XML DTBook
   - DAISY Pipeline App
   - Le complément Word SaveAsDAISY
2. Du XML DTBook à Word *(exercices pratiques)*
3. Structurer un document dans Word *(exercices pratiques)*
4. Convertir un fichier Word en XML DTBook *(exercices pratiques)*

---

## Retour sur le matin

- Le XML DTBook est un format structuré pour les livres accessibles
- Il utilise des balises sémantiques (`<level1>`, `<h1>`, `<p>`…)
- On peut le lire avec un éditeur texte ou un outil XML

**Aujourd'hui : mettons-le en pratique ! 🛠️**

---

# Partie 1

## Les logiciels du DAISY Consortium

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

---

## SaveAsDAISY – Onglet DAISY dans Word

Fonctions disponibles depuis le ruban Word :

| Bouton | Action |
|--------|--------|
| **Exporter DTBook** | Génère un fichier XML DTBook |
| **Exporter EPUB** | Génère un fichier EPUB 3 |
| **Vérifier** | Contrôle la structure du document |
| **Styles DAISY** | Applique les styles recommandés |

---

# Partie 2

## Du XML DTBook à Word *(exercices)*

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

---

## 2.b – Convertir un DTBook en fichier Word

**Via DAISY Pipeline App :**

1. Lancer DAISY Pipeline App
2. Choisir le script **« DTBook to DOCX »**
3. Sélectionner le fichier DTBook source (`.xml`)
4. Définir le dossier de sortie
5. Lancer la conversion
6. Ouvrir le fichier `.docx` généré dans Word

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

---

# Partie 3

## Structurer un document dans Word *(exercices)*

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

---

# Partie 4

## Convertir un fichier Word en XML DTBook *(exercices)*

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

---

## Points clés à retenir – Après-midi J1

- 🔧 **DAISY Pipeline** convertit entre de nombreux formats accessibles
- 📝 **SaveAsDAISY** intègre la conversion directement dans Word
- 🏗️ La **structuration Word** (styles de titres) est la clé d'une bonne conversion
- ✅ Le **vérificateur d'accessibilité** Word est un allié précieux
- 📄 Le XML DTBook généré reflète fidèlement la structure du Word source

---

## Récapitulatif de la journée 1

| Session | Contenu |
|---------|---------|
| Matin | Histoire de l'édition accessible, XML, DTBook |
| Après-midi | Outils DAISY, conversion Word↔DTBook, structuration |

**Demain : le format EPUB ! 📱**
