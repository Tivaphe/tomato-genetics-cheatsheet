# Contribuer

Les contributions sont bienvenues : ajouts de loci, corrections de dominance, précisions de chromosomes, nouvelles
références. Ce dépôt est une synthèse documentaire destinée à être **utilisable en sélection comme en recherche**, donc
la rigueur de la source prime sur l'abondance.

*This repository is bilingual, including chapter 17 and the ploidy section (only the bibliography stays French). To contribute to the English edition, read the* [*« Trois fichiers, une seule génétique »
section*](#trois-fichiers-une-seule-génétique) *below — the rule is simple: the genetics is written once, in the French
tables; the English file only re-words the phenotype and the selection note.*

## Le dépôt en sept fichiers

Il n'y a **ni dossier `data/`, ni script de génération** : les tableaux markdown sont la source, on les édite
directement. Le seul dossier, [`assets/`](assets/), accueille les illustrations décoratives des README (aucune donnée
génétique). Voir [README.md → Reproductibilité du dépôt](README.md#reproductibilité-du-dépôt) pour le détail.

| Fichier | Rôle | Édition conjointe obligatoire |
|:--|:--|:--|
| [`README.md`](README.md) | édition **française**, référence : 6 colonnes + bloc dépliable (biologie moléculaire, origine de l'allèle) | — |
| [`README.en.md`](README.en.md) | édition anglaise : mêmes loci, mêmes chromosomes, mêmes dominance, sans le bloc dépliable | ✅ une ligne par langue |
| [`index.html`](index.html) | version interactive (recherche, filtres, calculateur F2) : 230 lignes `<tr>`, 8 colonnes | ✅ si un locus est ajouté ou si `chr`/`dom` change |
| [`SOURCES.md`](SOURCES.md) | bibliographie commune aux deux langues, avec niveau de vérification | ✅ toute nouvelle référence |
| chapitre 17 et section Ploïdie (`README.md` / `README.en.md`) | **chapitre 17 · fleur** (réseau, stérilité mâle, pièges de nomenclature, pistes **non retenues**) et **section Ploïdie** (hors des 230 loci, 40 sources) | ✅ dans les **deux langues**, à la même place et avec le même contenu : un nouveau locus ajouté aux chapitres ? les quatre formats le portent |
| [`assets/banner.png`](assets/banner.png) | bannière décorative des deux README (aucune donnée génétique) | — |
| `LICENSE` | MIT — texte et données | — |
| `CONTRIBUTING.md` | ce fichier | — |

## Ce qui est le bienvenu

1. **Une référence manquante** pour un locus déjà listé (clonage récent, cartographie fine, valeur de `d/a`).
2. **Une correction** : mauvaise dominance, chromosome erroné, espèce d'origine mal attribuée, synonymie de gène.
3. **Un locus absent** d'une famille déjà couverte (par ex. les nouveaux allèles de `SP`, les QTL d'un pathogène émergent).
4. **Une épistasie publiée** qui manque au chapitre 16 (les doubles mutants documentés sont la partie la plus rare de la littérature).
5. **Une amélioration de la traduction anglaise** : tournure plus idiomatique, terme technique corrigé, précision ajoutée — tout ce qui ne touche pas au chromosome ni au code de dominance.

## Ce qui ne sera pas fusionné

* Une affirmation **sans référence primaire** (un forum, un catalogue de semences ou une notice variétale ne suffisent pas ;
une prépublication avec DOI si, oui).
* Un chiffre de phénotype **sans conditions de mesure** (°Brix, masse, rendement) : ces valeurs dépendent du milieu, de la
conduite et du stade de récolte.
* Un chromosome « probable ». Si la source ne le donne pas, écrivez **`n.d.`** — c'est une information en soi.
* Une prédiction de croisement présentée comme un fait : marquez-la **\[extrapolation]**, comme le font déjà les lignes
`Cu × c / tf / e / rg`.
* Une ligne ajoutée dans `README.en.md` **sans sa jumelle dans `README.md`** (et sans sa ligne dans `index.html`) :
le contrôle de cohérence le refuse, et il a raison.
* Un `README` modifié sans que le fichier jumeau le soit dans la même PR dès qu'il s'agit de `Symbole`, `Chr.` ou `Dominance`.

## Format d'une ligne

Un locus = **une ligne de tableau par fichier**, jamais une ligne par variété. Les groupes d'allèles alléliques tiennent
sur la même ligne (`og`/`og^c`, `Ip`/`Del`).

**Édition française** — six colonnes, dans l'ordre :

```markdown
| `OVATE (o)` | Ovate | 2 | 🔵 → 🟡 RÉCESSIF → SEMI-DOMINANT | Fruit ovale, en poire ou piriforme (Yellow Pear, Mountain Vineyard) | RÉCESSIF chez S. pimpinellifolium (rond dominant) mais ADDITIF dans l'IL2-5 de S. pennellii : la dominance dépend du fond. |
```

Puis, dans le bloc `<details>` du même chapitre, la ligne de détail — cinq colonnes :

```markdown
| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
```

**Édition anglaise** — mêmes six colonnes, `Symbole`, `Chr.` et le code de dominance **recopiés caractère par caractère**,
seul le texte est traduit :

```markdown
| `OVATE (o)` | Ovate | 2 | 🔵 → 🟡 RECESSIVE → SEMI-DOMINANT | Oval, pear or pyriform fruit (Yellow Pear, Mountain Vineyard) | G→T premature stop = null allele of the OFP family · Recessive in S. pimpinellifolium (round dominant) but additive in the S. pennellii IL2-5. |
```

**Version interactive** — une ligne `<tr>` par locus, huit cellules dans l'ordre
`symbole, nom, chr., dominance, effet, base moléculaire, origine de l'allèle, conséquence`, avec :

* `data-dom` : **un code parmi `D` `S` `R` `Q` `O` `E` `M`** (les deux premiers de la liste pour un cas qualifié, ex. `R S`),
  ou `-` pour une ligne non mendélienne — c'est ce code qui alimente les filtres ;
* `data-t` : le texte indexé par la recherche plein texte, en **minuscules**, sans balise, regroupant toutes les cellules ;
* l'apostrophe typographique encodée `&#x27;` (le contenu est dans un attribut HTML).

### Conventions

* Codes de dominance : `D` DOMINANT · `S` SEMI-DOMINANT · `R` RÉCESSIF · `Q` QTL/ADDITIF · `O` SURDOMINANCE ·
  `E` ÉPIGÉNÉTIQUE · `M` MIXTE/SELON FOND. Ils peuvent être qualifiés (`RÉCESSIF → SEMI-DOMINANT`) : gardez alors la
  nuance dans les trois fichiers.
* `—` en dominance = ligne de germoplasme ou combinaison épistatique, pas un locus mendélien.
* `Chr.` = chromosome de la carte **SL4.0** (ITAG 4.0) ; `n.d.` = non cartographié finement dans les sources compilées.
* Donnez le locus ITAG (`SolycNNgNNNNNN`) dès qu'il est connu : c'est ce qui rend une ligne réutilisable par un script ou un BLAST.
* Aucun `|` dans le texte d'une cellule (il casserait le tableau) : remplacez-le par `·` ou par une virgule.

## Trois fichiers, une seule génétique

À chaque contribution, la parité est vérifiée à la main — les trois commandes suivantes, **lancées à la racine du dépôt**,
doivent converger. Elles sont décrites en détail dans
[README.md → Reproductibilité du dépôt](README.md#reproductibilité-du-dépôt).

```bash
# 1. 230 dans les deux éditions
for f in README.md README.en.md; do printf '%s : ' "$f"
  grep -oE '\*\*[0-9]+ loci\*\*' "$f" | tr -dc '0-9\n' | awk '{s+=$1} END {print s}'; done
# 2. 230 lignes dans le site
grep -o '<tr data-dom=' index.html | wc -l
# 3. aucun lien mort
python3 -c "import re,os,glob
for fn in sorted(glob.glob('*.md')):
    s=open(fn,encoding='utf-8').read()
    heads={re.sub(r'[^\w \-]','',h.lower().replace('&amp;','&')).replace(' ','-') for h in re.findall(r'^#{2,4}\s+(.*)$',s,re.M)}
    print(fn,'-> ancres cassées :',sorted({l for l in re.findall(r'\]\(#([^)]+)\)',s) if l not in heads}) or 'aucune')
    miss=[f for f in sorted({l for l in re.findall(r'\]\((?!#|https?:|mailto:)([^)]+)\)',s)}) if not os.path.exists(f.split('#')[0])]
    print(fn,'-> fichiers absents :',miss or 'aucun')"
```

Concrètement, la parité impose :

* les **mêmes 17 chapitres**, dans le même ordre, avec le **même nombre de loci** dans chacun des chapitres 1 à 16 (l'intitulé `**N loci**`
de l'italique sous le titre est ce qui est comparé) ;
* les **mêmes chromosomes** — les chiffres doivent tomber juste — et les **mêmes codes de dominance** ;
* les **mêmes symboles**, à l'exception assumée des lignes descriptives (QTL non clonés, germoplasme, épistasies) dont
l'intitulé est logiquement traduit : `QTL psylle` ↔ `QTL psyllid`.

Le chapitre 17 (fleur) et la section Ploïdie vivent **dans les deux READMEs** : leur texte suit la même règle de parité, mais aucun des trois contrôles ne l'attrape — relisez-les à la main. Si l'un cite une source, elle s'ajoute à SOURCES.md (section 12 pour la ploïdie, 13 pour la fleur).

Autrement dit : **une nouvelle ligne se déclare trois fois** (FR, EN, `index.html`), mais une correction de chromosome
ou de dominance doit être reportée dans les trois formats — c'est le seul point où la mécanique est fastidieuse, et le
seul que le contrôle attrape.

## Comment proposer

### Par issue (le plus simple)

Ouvrez une **issue** en mentionnant le locus concerné (symbole + chapitre) et en remplissant le champ *Référence* avec un
lien ouvert et vérifiable : c'est la seule partie que personne ne peut deviner à votre place. Le minimum attendu :

```
Locus          : ovate (o) — chap. 6
Problème       : dominance indiquée « RÉCESSIF » alors que le fond IL2-5 la donne additive
Référence      : lien vers l'article (DOI ou PMC ouvert)
Valeur proposée: RÉCESSIF → SEMI-DOMINANT, avec mention du fond génétique
```

### Par pull request (le plus rapide)

1. Forkez, éditez les lignes en cause — **une ligne de tableau = un changement vérifiable**, une seule par commit si
   vous pouvez. Si vous touchez à `sym`, `chr` ou `dom`, corrigez les trois formats ; si vous touchez au texte seulement,
   le fichier concerné suffit (et `index.html` pour la FR, qui indexe aussi la conséquence).
2. Ajoutez la référence dans [`SOURCES.md`](SOURCES.md) — une entrée suffit pour les deux langues ; cochez-la 🔎 si vous
   avez réellement ouvert le texte.
3. Relisez la sortie des trois commandes de la section précédente : `230 · 230 · 230`, `aucune`, `aucun`.
4. **Aucun diff parasite** : une correction de texte ne doit pas reformater le reste du fichier. Si `git diff --stat`
   affiche un fichier touché en bloc, votre éditeur a réécrit les fins de ligne — remettez-les en `\n`.
5. Contrôles demandés :
   * la référence primaire a été **ouverte**, pas seulement citée de mémoire ;
   * si vous changez un mode de dominance, dites **sur quoi repose la valeur** (ratio F2 publié, `d/a` calculé sur NIL,
     revue, hétérozygote décrit) et sur **quel fond génétique** ;
   * si vous ajoutez une ligne, ajoutez aussi la **conséquence en sélection** (colonne de droite) : c'est la raison d'être
     de cette fiche ;
   * le bloc dépliable (FR) est rempli : une ligne sans base moléculaire ni origine d'allèle est une ligne invérifiable.
6. Ouvrez la PR avec, dans le corps, le lien vers la source et une phrase sur ce qu'elle établit.

## Cadre scientifique

* **Niveau de preuve affiché dans SOURCES.md** : 🔎 référence revérifiée à la date de consolidation ; ✓ reprise des
dossiers compilés sans re-ouverture du lien. En ajoutant une source, vous pouvez la passer à 🔎 si vous la vérifiez.
* **La dominance n'est pas une propriété absolue d'un locus.** Pour un caractère quantitatif, elle change avec le fond
génétique et avec le caractère mesuré. Écrivez donc de préférence « récessif chez *X*, additif dans *Y* » plutôt qu'un
code sec.
* **Nomenclature** : symboles en minuscule pour les pertes de fonction, majuscule pour les gains dominants
(`sp` vs `SP`, `c` vs `C`), italique dans le texte pour les gènes, romain pour les protéines ; espèces en italique ;
anciens noms signalés entre parenthèses (*Lycopersicon hirsutum* = *S. habrochaites*).
* **Identifiants** : dès que possible, donnez le locus ITAG 4.0 (`SolycNNgNNNNNN`).

## Licence des contributions

Le dépôt est sous **[licence MIT](LICENSE)** — texte et données. En soumettant une contribution, vous acceptez de placer
celle-ci sous cette même licence : réutilisation, modification et redistribution (y compris commerciale) libres, à
condition de conserver la mention de copyright et le texte de la licence. Aucun CLA, aucune cession de droits : vous
restez titulaire du droit d'auteur de ce que vous écrivez, et la licence MIT est ce qui permet aux autres de s'en servir.

Deux conséquences pratiques pour les contributeurs :

* **ne copiez pas** un tableau, une figure ou un texte protégé par une autre licence (CC BY-NC, tous droits réservés,
notice commerciale) : seule une synthèse **reformulée** et **sourcée** a sa place ici ;
* les données brutes publiques d'une publication (tableau supplémentaire, fichier ITAG, descripteur d'accession) sont
réutilisables, mais **citez la publication d'origine** dans `SOURCES.md` à la ligne concernée.
