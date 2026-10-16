# Langues du clavier AZERTY

919 packs de langue (dictionnaire, paires de mots, disposition, règles), téléchargés par le
clavier depuis ses réglages ou au moment de choisir une langue.

- `packs/<id>/` : les fichiers de chaque pack, en texte.
- `catalogue.tsv` : la liste lue par le clavier (archive, taille, empreinte SHA-256).
- `interface/` : ce qui ne tient pas à une langue en particulier — le nom de chaque langue
  dans chaque langue (`_names.txt`, CLDR) et le catalogue d'emojis (`emoji.txt`, UTS #51).
  Ces deux-là sont toujours dans l'application, jamais téléchargés.
- Les archives `dist/<id>.zip` se joignent à une *release* GitHub (elles ne sont pas dans git).

## Licences

Ce que nous avons créé — listes de mots et de paires tirées du corpus FineWeb (ODC-By, cité dans
`NOTICE`), conjugaisons, listes écrites à la main — est sous licence MIT (`LICENSE`). Les fichiers
repris de projets libres gardent leur licence : voir ci-dessous. La licence de chaque fichier est
dans `REUSE.toml` (spécification REUSE), et chaque archive porte un `LICENCE.txt`.

## Forks de projets libres

Une partie des données vient de projets libres : ce dépôt en est un fork pour ces fichiers,
qui GARDENT la licence d'origine (voir `REUSE.toml` et `LICENSES/`).

### FineWeb-2 (Hugging Face)
- Origine : https://huggingface.co/datasets/HuggingFaceFW/fineweb-2 — Hugging Face
- Données : extrait d'octobre 2026
- Fork : le projet n'est pas sur GitHub ; il est cité, pas forké.
- Licence conservée : `ODC-By-1.0`
- Repris : les textes, d'où sont comptés les mots et les suites de mots
- Modifié : listes de fréquences par langue, bruit et fautes écartés
- Packs : ab, abq, abt, ace, acf, acu, ada, ady, af, agg, agr, ajg, aji, ak, am, amu, an, ar, ar-ae, ar-bh …

### FineWeb (Hugging Face, anglais)
- Origine : https://huggingface.co/datasets/HuggingFaceFW/fineweb — Hugging Face
- Données : extrait d'octobre 2026
- Fork : le projet n'est pas sur GitHub ; il est cité, pas forké.
- Licence conservée : `ODC-By-1.0`
- Repris : les textes anglais, d'où sont comptés les mots et les suites de mots
- Modifié : listes de fréquences, bruit et fautes écartés
- Packs : en

### Droid Sans Fallback (Android Open Source Project)
- Origine : https://android.googlesource.com/platform/frameworks/base/ — Google Inc. ; The Android Open Source Project
- Données : extrait le 15 octobre 2026
- Fork : https://github.com/Correctors-lang/platform_frameworks_base
- Licence conservée : `Apache-2.0`
- Repris : les dessins des caractères chinois de la police
- Modifié : ramenés à un squelette de 32 × 32 points, pour l'écriture manuscrite
- Packs : yue, zh-hans, zh-hant

### Unicode CLDR
- Origine : https://cldr.unicode.org — Unicode, Inc.
- Données : extrait le 15 octobre 2026
- Fork : https://github.com/Correctors-lang/cldr
- Licence conservée : `Unicode-3.0`
- Repris : le nom de chaque langue dans chaque langue
- Modifié : réduit aux langues du clavier, une ligne par couple
- Packs : interface

### Unicode emoji (UTS #51)
- Origine : https://unicode.org/Public/emoji/ — Unicode, Inc.
- Données : extrait le 15 octobre 2026
- Fork : https://github.com/Correctors-lang/unicodetools
- Licence conservée : `Unicode-3.0`
- Repris : la liste des emojis et leurs noms
- Modifié : rangés par catégorie, teintes de peau ôtées, mots-clés pour la recherche
- Packs : interface

### Unicode Unihan
- Origine : https://www.unicode.org/charts/unihan.html — Unicode, Inc.
- Données : Unihan 16.0, extrait le 15 octobre 2026
- Fork : https://github.com/Correctors-lang/unicodetools
- Licence conservée : `Unicode-3.0`
- Repris : les lectures des caractères (kMandarin, kHanyuPinyin, kXHC1983, kTGHZ2013, kCantonese)
- Modifié : tons ôtés, lectures indexées par mot et classées par la fréquence d'usage
- Packs : yue, zh-hans, zh-hant

### Mozc (dictionnaire OSS : IPAdic, dictionnaire d'Okinawa)
- Origine : https://github.com/google/mozc — Google Inc. ; Nara Institute of Science and Technology (IPAdic)
- Données : dictionary_oss, extrait le 15 octobre 2026
- Fork : https://github.com/Correctors-lang/mozc
- Licence conservée : `BSD-3-Clause AND LicenseRef-IPAdic`
- Repris : les lectures et les mots (dictionary_oss)
- Modifié : classement par catégorie et par la fréquence d'usage, entrées les plus rares retirées
- Packs : ja

### iTaigi 華台辭典 (via ChhoeTaigi)
- Origine : https://itaigi.tw — iTaigi
- Données : extrait le 15 octobre 2026
- Fork : https://github.com/Correctors-lang/ChhoeTaigiDatabase
- Licence conservée : `CC0-1.0`
- Repris : les mots en caractères et leur lecture en pe̍h-ōe-jī
- Modifié : lectures sans tons, classées par la fréquence du pack nan
- Packs : nan-hant

### INSEE (fichier des prénoms) et geo.api.gouv.fr (communes)
- Origine : https://geo.api.gouv.fr — INSEE ; Etalab
- Données : extrait le 13 septembre 2026 (communes) et le 8 septembre 2026 (prénoms)
- Fork : le projet n'est pas sur GitHub ; il est cité, pas forké.
- Licence conservée : `etalab-2.0`
- Repris : les prénoms et les communes de France
- Modifié : mis au format du clavier (nom, fréquence ou population)
- Packs : fr

### GeoNames (cities15000)
- Origine : https://www.geonames.org — GeoNames
- Données : extrait le 15 octobre 2026
- Fork : le projet n'est pas sur GitHub ; il est cité, pas forké.
- Licence conservée : `CC-BY-4.0`
- Repris : les villes de plus de 15 000 habitants
- Modifié : une liste par pays, triée par population
- Packs : ar, bar, bg, bn, br, ca, ckb, cs, da, de, el, en, es, et, eu, fi, fil, fr, ga, gd …

### AnCora (Universal Dependencies, espagnol et catalan)
- Origine : https://github.com/UniversalDependencies/UD_Spanish-AnCora — Universitat de Barcelona (CLiC)
- Données : extrait le 15 octobre 2026
- Fork : https://github.com/Correctors-lang/UD_Spanish-AnCora
- Licence conservée : `CC-BY-4.0`
- Repris : les formes, lemmes, natures, genres et nombres
- Modifié : réduits à un lexique forme → analyses
- Packs : ca, es

Le dictionnaire d'Okinawa, inclus dans celui de Mozc, est dans le domaine public.
Générés par `tools/generateurs/` dans le dépôt du clavier.
