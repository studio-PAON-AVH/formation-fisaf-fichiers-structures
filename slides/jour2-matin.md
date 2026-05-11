---
title: "Jour 2 – Matin : Le format EPUB"
---

# Jour 2 – Matin

## Le format EPUB

---

## Au programme ce matin

1. Retour / Questions sur la journée 1
2. Histoire de l'EPUB comme publication accessible
   - Qu'est-ce qu'un EPUB ?
   - Les différents types d'EPUB
   - L'accessibilité numérique
   - Les EPUB accessibles
3. Les logiciels pour lire et produire un EPUB
   - Lire : Thorium, EasyReader, Calibre
   - Produire : Calibre/Codex, Sigil

---

## Retour sur la journée 1

- **Matin** : histoire de l'édition accessible, formats XML, DTBook
- **Après-midi** : DAISY Pipeline, SaveAsDAISY, structuration Word

**Des questions ? Des points à revoir ?**

---

# Partie 2

## Histoire de l'EPUB comme publication accessible

---

## 2.a – C'est quoi un EPUB ?

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

---

## 2.b – Les différents types d'EPUB

### EPUB Reflow (Reflowable)

- Le texte **s'adapte** à la taille de l'écran
- Idéal pour les **textes longs** (romans, essais)
- Taille de police modifiable par l'utilisateur
- **Le plus courant et le plus accessible**

### EPUB Fixed Layout (Mise en page fixe)

- Mise en page **identique** quelle que soit la taille d'écran
- Idéal pour les **livres illustrés**, BD, livres enfants
- Moins accessible (texte non redimensionnable)
- Similaire à un PDF enrichi

---

## Comparatif Reflow / Fixed Layout

| Critère | Reflow | Fixed Layout |
|---------|--------|--------------|
| Adaptation écran | ✅ Oui | ❌ Non |
| Taille police réglable | ✅ Oui | ❌ Non |
| Accessibilité | ✅ Bonne | ⚠️ Limitée |
| Mise en page complexe | ❌ Limitée | ✅ Précise |
| Usage typique | Romans, essais | BD, livres illustrés |

---

## 2.c – L'accessibilité numérique

### Le cadre réglementaire

- **RGAA** (France) : Référentiel Général d'Amélioration de l'Accessibilité
- **Directive européenne** 2016/2102 : accessibilité des sites publics
- **Loi du 11 février 2005** (France) : non-discrimination des personnes handicapées
- **Acte européen sur l'accessibilité** (2019 / 2025) : livres numériques inclus !

---

## Les standards d'accessibilité numérique

| Standard | Description |
|----------|-------------|
| **WCAG 2.1/2.2** | Web Content Accessibility Guidelines (W3C) |
| **EPUB Accessibility 1.1** | Profil d'accessibilité pour les EPUBs |
| **ARIA** | Rôles et propriétés pour l'accessibilité web |
| **EN 301 549** | Standard européen d'accessibilité TIC |

---

## 2.d – Les EPUB accessibles

Un EPUB accessible c'est :

- 📖 **Texte alternatif** sur toutes les images
- 🏷️ **Structure sémantique** : titres, listes, tableaux balisés
- 🌐 **Langue** déclarée dans les métadonnées
- 📋 **Table des matières** navigable (NCX / NAV)
- 🎵 **Synchronisation audio** (Media Overlays pour EPUB 3)
- ♿ **Métadonnées d'accessibilité** (schema.org)

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

---

# Partie 3

## Les logiciels pour lire et produire un EPUB

---

## 3.a – Lire des EPUBs

### Thorium Reader

- 🌐 [edrlab.org/thorium-reader](https://www.edrlab.org/thorium-reader/)
- Développé par EDRLab (France)
- **Très accessible** : lecteurs d'écran, navigation clavier
- Support EPUB 3, PDF, audiobooks, DAISY
- Disponible Windows, macOS, Linux
- **Recommandé pour les tests d'accessibilité**

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

---

## EasyReader

- 🌐 [dolphincomputeraccess.com](https://www.dolphincomputeraccess.com/)
- Développé par Dolphin Computer Access
- Conçu **spécifiquement** pour les personnes déficientes visuelles
- Support EPUB, DAISY, MP3, PDF
- Interface simplifiée et très accessible
- Connexion aux bibliothèques numériques (Bookshare, BNFA…)

---

## Calibre

- 🌐 [calibre-ebook.com](https://calibre-ebook.com/)
- Logiciel libre et gratuit
- Gestion de bibliothèque numérique
- **Conversions** entre formats (EPUB, MOBI, PDF, DOCX…)
- Visionneuse intégrée
- Éditeur de métadonnées

---

## 3.b – Calibre/Codex

**Codex** est l'éditeur EPUB intégré à Calibre :

- Accessible depuis Calibre via **Modifier le livre**
- Édition directe des fichiers XHTML, CSS, OPF
- Vue arborescence des fichiers de l'EPUB
- Aperçu en temps réel
- Outils de nettoyage et validation

**Usage typique :**
- Corrections mineures après conversion
- Ajout/modification de métadonnées
- Vérification de la structure interne

---

## 3.c – Sigil

- 🌐 [sigil-ebook.com](https://sigil-ebook.com/)
- Éditeur EPUB libre et gratuit (Windows, macOS, Linux)
- Spécialisé dans la **création et l'édition d'EPUBs**
- Interface WYSIWYG + vue code
- Gestion de la table des matières
- Plugins pour l'accessibilité et la validation

---

## Sigil – Interface

| Zone | Contenu |
|------|---------|
| **Panneau fichiers** | Structure interne de l'EPUB |
| **Éditeur** | Vue WYSIWYG ou code source |
| **Table des matières** | NCX/NAV éditables |
| **Métadonnées** | Éditeur de propriétés Dublin Core |

---

## Comparatif des logiciels

| Logiciel | Lire | Produire | Convertir | Gratuit |
|----------|------|----------|-----------|---------|
| **Thorium Reader** | ✅ | ❌ | ❌ | ✅ |
| **EasyReader** | ✅ | ❌ | ❌ | 💰 |
| **Calibre** | ✅ | ⚠️ | ✅ | ✅ |
| **Sigil** | ✅ | ✅ | ❌ | ✅ |
| **DAISY Pipeline** | ❌ | ✅ | ✅ | ✅ |
| **SaveAsDAISY** | ❌ | ✅ | ✅ | ✅ |

---

## Points clés à retenir – Matin J2

- 📦 L'EPUB est une archive ZIP contenant du XHTML, CSS et des métadonnées
- 🔄 EPUB 3.3 est le standard actuel maintenu par le W3C
- ♿ L'EPUB accessible suit les critères WCAG et EPUB Accessibility 1.1
- 📱 Thorium Reader est la référence pour lire et tester les EPUBs accessibles
- 🛠️ Calibre/Sigil permettent de créer et éditer des EPUBs

---

## Questions ?

**Pause déjeuner →**

_Après-midi : produire des EPUBs accessibles_
