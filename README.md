# Langues du clavier AZERTY

919 packs de langue (dictionnaire, paires de mots, disposition, règles), téléchargés par le
clavier depuis ses réglages ou au moment de choisir une langue.

- `packs/<id>/` : les fichiers de chaque pack, en texte.
- `catalogue.tsv` : la liste lue par le clavier (archive, taille, empreinte SHA-256).
- Les archives `dist/<id>.zip` se joignent à une *release* GitHub (elles ne sont pas dans git).

## Licences

Ce que nous avons créé — listes de mots et de paires tirées du corpus FineWeb (ODC-By, cité dans
`NOTICE`), conjugaisons, listes écrites à la main — est sous licence MIT (`LICENSE`). Les fichiers
repris de projets libres gardent leur licence : voir ci-dessous. La licence de chaque fichier est
dans `REUSE.toml` (spécification REUSE), et chaque archive porte un `LICENCE.txt`.

## Forks de projets libres

Une partie des données vient de projets libres : ce dépôt en est un fork pour ces fichiers,
qui GARDENT la licence d'origine (voir `REUSE.toml` et `LICENSES/`).

### Unicode Unihan
- Origine : https://www.unicode.org/charts/unihan.html — Unicode, Inc.
- Licence conservée : `Unicode-3.0`
- Repris : les lectures des caractères (kMandarin, kHanyuPinyin, kXHC1983, kTGHZ2013, kCantonese)
- Modifié : tons ôtés, lectures indexées par mot et classées par la fréquence d'usage
- Packs : yue, zh-hans, zh-hant

### Mozc (dictionnaire OSS : IPAdic, dictionnaire d'Okinawa)
- Origine : https://github.com/google/mozc — Google Inc. ; Nara Institute of Science and Technology (IPAdic)
- Licence conservée : `BSD-3-Clause AND LicenseRef-IPAdic`
- Repris : les lectures et les mots (dictionary_oss)
- Modifié : classement par catégorie et par la fréquence d'usage, entrées les plus rares retirées
- Packs : ja

### iTaigi 華台辭典 (via ChhoeTaigi)
- Origine : https://itaigi.tw — iTaigi
- Licence conservée : `CC0-1.0`
- Repris : les mots en caractères et leur lecture en pe̍h-ōe-jī
- Modifié : lectures sans tons, classées par la fréquence du pack nan
- Packs : nan-hant

### INSEE (fichier des prénoms) et geo.api.gouv.fr (communes)
- Origine : https://geo.api.gouv.fr — INSEE ; Etalab
- Licence conservée : `etalab-2.0`
- Repris : les prénoms et les communes de France
- Modifié : mis au format du clavier (nom, fréquence ou population)
- Packs : fr

### GeoNames (cities15000)
- Origine : https://www.geonames.org — GeoNames
- Licence conservée : `CC-BY-4.0`
- Repris : les villes de plus de 15 000 habitants
- Modifié : une liste par pays, triée par population
- Packs : ar, bar, bg, bn, br, ca, ckb, cs, da, de, el, en, es, et, eu, fi, fil, fr, ga, gd …

### AnCora (Universal Dependencies, espagnol et catalan)
- Origine : https://github.com/UniversalDependencies/UD_Spanish-AnCora — Universitat de Barcelona (CLiC)
- Licence conservée : `CC-BY-4.0`
- Repris : les formes, lemmes, natures, genres et nombres
- Modifié : réduits à un lexique forme → analyses
- Packs : ca, es

Le dictionnaire d'Okinawa, inclus dans celui de Mozc, est dans le domaine public.
Générés par `tools/generateurs/` dans le dépôt du clavier.
