---
title: "Jour 1 – Matin : Histoire & XML"
---

# Jour 1 – Matin

## Histoire de l'édition adaptée  
## et initiation au langage XML

---

## Au programme ce matin

1. Un peu d'histoire et de culture
   - Histoire de l'édition numérique accessible
   - Les différents formats structurés du domaine
2. Les formats XML
   - Présentation du XML
   - XHTML et XML DTBook
   - Structure et éléments sémantiques du DTBook
   - Logiciels pour lire des fichiers XML

---

# Partie 1

## Un peu d'histoire et de culture

---

## 1.a – Histoire de l'édition numérique accessible

- **Années 1990** : naissance des premiers livres numériques pour personnes déficientes visuelles
- **1996** : création du **DAISY Consortium**
  - *Digital Accessible Information SYstem*
  - Consortium international d'éditeurs et d'organisations
- **1997–2005** : développement du format DAISY 2 & DAISY 3 (XML DTBook)
- **2010** : l'EPUB intègre les travaux du DAISY Consortium
- **2017** : publication de l'**EPUB Accessibility 1.0**
- **2023** : standard européen **EN 301 549** – accessibilité numérique

---

## Les pionniers de l'accessibilité numérique

| Organisation | Rôle |
|---|---|
| **DAISY Consortium** | Norme et outils pour l'édition accessible |
| **Bookshare** | Bibliothèque numérique accessible |
| **RNIB** (UK) | Ressources pour les déficients visuels |
| **BrailleNet** | Accessibilité web et numérique (France) |
| **CERTAM / FISAF** | Formation et expertise en France |

---

## 1.b – Les différents formats structurés du domaine

| Format | Description | Usage |
|--------|-------------|-------|
| **XML DTBook** | Format DAISY 3 structuré | Livres audio structurés |
| **EPUB 2 / EPUB 3** | Standard international e-book | Publications numériques |
| **XHTML** | HTML étendu en XML | Pages web accessibles |
| **PDF balisé** | PDF avec structure sémantique | Documents accessibles |
| **DOCX structuré** | Word avec styles sémantiques | Source de production |

---

## Pourquoi la structuration est essentielle ?

- ✅ **Navigation** : titres, chapitres, sections accessibles
- ✅ **Conversion** : un source structuré → multiples formats
- ✅ **Accessibilité** : lecteurs d'écran, plages braille
- ✅ **Indexation** : métadonnées riches et exploitables
- ✅ **Pérennité** : formats ouverts et documentés

---

# Partie 2

## Les formats XML

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

---

## Les types de balises XML

| Type | Exemple | Description |
|------|---------|-------------|
| **Ouvrante** | `<para>` | Début d'un élément |
| **Fermante** | `</para>` | Fin d'un élément |
| **Auto-fermante** | `<img src="img.jpg"/>` | Élément vide |
| **Attribut** | `class="important"` | Propriété d'un élément |
| **Commentaire** | `<!-- commentaire -->` | Note non rendue |

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

---

## 2.b – Comparatif XHTML et XML DTBook

| Critère | XHTML | XML DTBook |
|---------|-------|------------|
| **Origine** | W3C | DAISY Consortium |
| **Usage principal** | Pages web | Livres audio structurés |
| **Éléments sémantiques** | `<h1>`, `<p>`, `<div>`… | `<doctitle>`, `<level1>`, `<p>`… |
| **Multimédia** | Oui (HTML5) | Audio synchronisé (SMIL) |
| **Accessibilité** | ARIA, alt… | Structure native |

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

---

## 2.d – Logiciels pour lire des fichiers XML

| Logiciel | Plateforme | Rôle |
|----------|------------|------|
| **Notepad++** | Windows | Éditeur texte avec coloration syntaxique |
| **Visual Studio Code** | Multi | Éditeur avancé, extensions XML |
| **XMLSpy** | Windows | Éditeur XML professionnel |
| **oXygen XML Editor** | Multi | Éditeur XML avancé |
| **Firefox / Chrome** | Multi | Visualisation basique XML |

---

## Points clés à retenir – Matin J1

- 📚 L'édition numérique accessible est née dans les années 1990 avec le DAISY Consortium
- 🏗️ Les formats structurés séparent contenu, structure et présentation
- 🔤 XML est un langage de balisage extensible et rigoureux
- 📖 Le XML DTBook est le format DAISY 3 pour les livres structurés
- 🛠️ Des outils gratuits permettent de visualiser et éditer du XML

---

## Questions ?

**Pause avant l'après-midi →**

_Après-midi : produire et utiliser des fichiers XML DTBook_
