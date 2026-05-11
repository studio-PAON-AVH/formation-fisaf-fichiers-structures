---
title: "Jour 2 – Après-midi : EPUB accessibles en pratique"
---

# Jour 2 – Après-midi

## Produire des EPUBs accessibles

---

## Au programme cet après-midi

1. Convertir un fichier EPUB vers Word
   - Via Calibre/Codex
   - Via WordToEPUB du DAISY Consortium
2. Retour à la structuration dans Word
   - Structuration et métadonnées
3. Générer un EPUB accessible *(exercices)*
   - Via WordToEPUB
   - Via SaveAsDAISY
   - Créer un EPUB Media Overlay
4. Contrôler et valider un EPUB

---

# Partie 1

## Convertir un EPUB vers Word

---

## 1.a – Via Calibre/Codex

**Calibre** peut convertir un EPUB en DOCX :

1. Ouvrir Calibre et importer le fichier EPUB
2. Sélectionner le livre → **Convertir les livres**
3. Choisir le **format de sortie : DOCX**
4. Options de conversion :
   - Conserver les styles
   - Convertir les images
   - Structure des chapitres
5. Lancer la conversion
6. Exporter et ouvrir dans Word

⚠️ La qualité dépend de la structure de l'EPUB source

---

## 1.b – Via WordToEPUB du DAISY Consortium

**WordToEPUB** est un outil en ligne développé par le DAISY Consortium

- 🌐 [daisy.org/wordtoepub](https://daisy.org/wordtoepub)
- Application web gratuite (traitement local, pas d'envoi de données)
- Spécialisé dans la **conversion Word → EPUB 3 accessible**

**Il peut aussi reconvertir un EPUB en Word :**
1. Exporter l'EPUB en DOCX via les outils internes
2. Réutiliser la source Word si disponible

---

## Bonne pratique : conserver les sources !

> **Toujours conserver le fichier Word source**  
> C'est la meilleure base pour toute modification ou reconversion.

Flux de travail recommandé :

```
[Source Word structurée] → [EPUB accessible]
         ↑                        ↓
    Modifications          Tests / Corrections
         ↑                        ↓
    [Source Word mise à jour] ← [Retour si nécessaire]
```

---

# Partie 2

## Retour à la structuration dans Word

---

## 2.a – Rappel : structuration dans Word

Les éléments essentiels pour un EPUB de qualité :

| Élément | Règle |
|---------|-------|
| **Titres** | Utiliser les styles Titre 1, 2, 3 |
| **Paragraphes** | Style Corps de texte ou Normal |
| **Listes** | Listes automatiques (puces/numéros) |
| **Images** | Texte alternatif obligatoire |
| **Tableaux** | Ligne d'en-tête définie |
| **Notes de bas de page** | Via l'outil Word dédié |

---

## 2.b – Les métadonnées pour l'accessibilité

**Fichier → Propriétés → Propriétés avancées dans Word :**

| Métadonnée | Exemple |
|------------|---------|
| **Titre** | « Guide de jardinage biologique » |
| **Auteur** | Nom de l'auteur |
| **Langue** | fr (français) |
| **Sujet** | Mots-clés descriptifs |
| **Description** | Résumé de l'ouvrage |

Ces métadonnées seront intégrées dans l'EPUB généré.

---

## Métadonnées d'accessibilité supplémentaires

**Dans WordToEPUB et SaveAsDAISY :**

- **Mode d'accès** : textuel, visuel, auditif
- **Fonctionnalités d'accessibilité** : navigation structurée, texte alternatif
- **Risques d'accessibilité** : clignotements, sons forts (aucun dans la plupart des cas)
- **Résumé d'accessibilité** : description des mesures prises
- **Conformité** : EPUB Accessibility 1.1 – WCAG 2.1 niveau AA

---

# Partie 3

## Générer un EPUB accessible *(exercices)*

---

## 3.a – Conversion via WordToEPUB

**WordToEPUB** : conversion Word → EPUB 3 accessible

1. 🌐 Aller sur [daisy.org/wordtoepub](https://daisy.org/wordtoepub)
2. Cliquer sur **« Choisir un fichier »** et sélectionner le DOCX
3. Configurer les options :
   - Langue du document
   - Métadonnées de l'ouvrage
   - Options d'accessibilité
4. Cliquer sur **« Convertir »**
5. Télécharger le fichier EPUB généré

✅ Avantage : simple, en ligne, très accessible

---

## 🛠️ Exercice 4

**Convertir un Word en EPUB accessible avec WordToEPUB**

1. Ouvrir [daisy.org/wordtoepub](https://daisy.org/wordtoepub)
2. Charger le fichier `exercice4.docx`
3. Renseigner les métadonnées (titre, auteur, langue)
4. Lancer la conversion
5. Télécharger et ouvrir l'EPUB dans Thorium Reader
6. Tester la navigation (table des matières, titres)

**Durée : 20 minutes**

---

## 3.b – Conversion via SaveAsDAISY

**Depuis Word avec le complément SaveAsDAISY :**

1. Ouvrir le document Word structuré
2. Cliquer sur l'onglet **DAISY**
3. Sélectionner **« Exporter EPUB »**
4. Configurer :
   - Titre, auteur, langue
   - Options d'accessibilité
   - Couverture (optionnel)
5. Choisir le dossier de destination
6. Lancer l'export

---

## Comparatif WordToEPUB vs SaveAsDAISY

| Critère | WordToEPUB | SaveAsDAISY |
|---------|------------|-------------|
| **Mode** | En ligne | Dans Word |
| **Installation** | Aucune | Complément Word |
| **Métadonnées d'accessibilité** | ✅ Guidé | ✅ Disponible |
| **EPUB Media Overlay** | ❌ | ✅ |
| **DTBook** | ❌ | ✅ |
| **Facilité d'utilisation** | ⭐⭐⭐⭐ | ⭐⭐⭐ |

---

## 3.c – Créer un EPUB Media Overlay avec SaveAsDAISY

**Media Overlay** = synchronisation texte + audio dans un EPUB 3

**Principe :**
1. Préparer le document Word structuré
2. Enregistrer une narration audio (ou utiliser une synthèse vocale)
3. Dans SaveAsDAISY : **Exporter EPUB avec Media Overlay**
4. L'audio se synchronise mot à mot ou phrase par phrase

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

---

## 🛠️ Exercice 5

**Créer un EPUB avec Media Overlay**

1. Utiliser le fichier `exercice5.docx` + `exercice5-audio.mp3`
2. Ouvrir Word avec le complément SaveAsDAISY
3. Aller dans l'onglet **DAISY** → **« Exporter EPUB avec Media Overlay »**
4. Associer le fichier audio
5. Générer l'EPUB
6. Ouvrir dans Thorium Reader et tester la lecture synchronisée

**Durée : 25 minutes**

---

# Partie 4

## Contrôler et valider un EPUB

---

## 4.a – Contrôler un EPUB avec EPUBCheck

**EPUBCheck** est l'outil de validation officiel du W3C

- 🌐 [github.com/w3c/epubcheck](https://github.com/w3c/epubcheck)
- Outil en ligne de commande (Java)
- Vérifie la **conformité technique** au standard EPUB
- Détecte les erreurs de structure, de métadonnées, de liens…

**Utilisation en ligne :**
- 🌐 [validator.idpf.org](https://validator.idpf.org/) *(IDPF/W3C)*

---

## EPUBCheck – Types d'erreurs détectées

| Type | Exemple |
|------|---------|
| **Erreur fatale** | Archive ZIP corrompue |
| **Erreur** | Fichier manquant référencé dans l'OPF |
| **Avertissement** | Attribut déprécié |
| **Info** | Caractéristique EPUB 3 utilisée |

**Objectif :** 0 erreur, 0 avertissement (ou justifiés)

---

## 🛠️ Exercice 6a

**Valider un EPUB avec EPUBCheck**

1. Aller sur [validator.idpf.org](https://validator.idpf.org/)
   _ou utiliser EPUBCheck en ligne de commande_
2. Charger le fichier EPUB généré lors de l'exercice 4
3. Analyser le rapport :
   - Nombre d'erreurs / avertissements
   - Type de problèmes signalés
4. Identifier les corrections à apporter

**Durée : 15 minutes**

---

## 4.b – Contrôler un EPUB avec ACE du DAISY Consortium

**ACE** (*Accessibility Checker for EPUB*) est l'outil d'audit d'accessibilité

- 🌐 [daisy.org/ace](https://daisy.org/ace)
- Développé par le DAISY Consortium
- Vérifie la **conformité WCAG** et **EPUB Accessibility**
- Génère un rapport HTML détaillé

**Installation :**
```bash
npm install -g @daisy/ace
ace --version
```

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

---

## ACE – Rapport de conformité

Le rapport ACE inclut :

- 📊 **Score global** de conformité
- 🔍 **Liste des violations** avec explications
- 📋 **Données structurées** du livre analysé
- 💡 **Recommandations** de corrections
- 🏷️ **Vérification des métadonnées** d'accessibilité

---

## 🛠️ Exercice 6b

**Analyser un EPUB avec ACE**

1. Lancer ACE sur le fichier EPUB de l'exercice 4 :
   ```
   ace monlivre.epub -o rapport-ace/
   ```
2. Ouvrir le rapport HTML généré
3. Analyser :
   - Violations détectées
   - Critères WCAG non respectés
4. Identifier les 3 principales améliorations possibles
5. Corriger dans le Word source et reconvertir

**Durée : 25 minutes**

---

## Workflow complet de production EPUB accessible

```
1. Rédaction dans Word
   (styles + métadonnées + images alt)
        ↓
2. Vérification Word
   (vérificateur d'accessibilité intégré)
        ↓
3. Conversion en EPUB
   (WordToEPUB ou SaveAsDAISY)
        ↓
4. Validation technique
   (EPUBCheck → 0 erreur)
        ↓
5. Audit accessibilité
   (ACE → conformité WCAG)
        ↓
6. Corrections et itérations
        ↓
7. Publication ✅
```

---

## Points clés à retenir – Après-midi J2

- 🔄 **Calibre** permet de convertir des EPUBs existants
- 🌐 **WordToEPUB** : outil en ligne simple pour EPUB 3 accessible
- 🔧 **SaveAsDAISY** : production dans Word, supporte les Media Overlays
- ✅ **EPUBCheck** : validation technique obligatoire (0 erreur)
- ♿ **ACE** : audit d'accessibilité complet selon WCAG et EPUB Accessibility

---

## Récapitulatif des 2 jours

| Session | Contenu |
|---------|---------|
| J1 Matin | Histoire, formats structurés, XML, DTBook |
| J1 Après-midi | DAISY Pipeline, SaveAsDAISY, Word → DTBook |
| J2 Matin | EPUB : formats, accessibilité, logiciels |
| J2 Après-midi | Production EPUB accessible, validation |

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

---

## Merci pour votre participation ! 🎉

**Formation FISAF – Fichiers Structurés  
pour la Transcription et l'Édition Numérique Adaptée**

_Questions ? Contactez-nous !_
