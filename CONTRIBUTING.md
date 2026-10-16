# Contribuer

Les contributions sont bienvenues : ajouts de loci, corrections de dominance, précisions de chromosomes, nouvelles
références. Ce dépôt est une synthèse documentaire destinée à être **utilisable en sélection comme en recherche**, donc
la rigueur de la source prime sur l'abondance.

*This repository is bilingual. If you want to contribute to the English edition, read the*
[*« Deux langues » section*](#deux-langues-une-seule-génétique) *below — the rule is simple: the genetics is written once,
in the French tables; the English file only re-words `name`, `effect` and `note`.*

## Ce qui est le bienvenu

1. **Une référence manquante** pour un locus déjà listé (clonage récent, cartographie fine, valeur de `d/a`).
2. **Une correction** : mauvaise dominance, chromosome erroné, espèce d'origine mal attribuée, synonymie de gène.
3. **Un locus absent** d'une famille déjà couverte (par ex. les nouveaux allèles de `SP`, les QTL d'un pathogène émergent).
4. **Une épistasie publiée** qui manque au chapitre 16 (les doubles mutants documentés sont la partie la plus rare de la littérature).
5. **Une amélioration de la traduction anglaise** : tournure plus idiomatique, terme technique corrigé, précision ajoutée
dans `note` — tout ce qui ne touche pas au chromosome ni au code de dominance.

## Ce qui ne sera pas fusionné

* Une affirmation **sans référence primaire** (un forum, un catalogue de semences ou une notice variétale ne suffisent pas ;
une prépublication avec DOI si, oui).
* Un chiffre de phénotype **sans conditions de mesure** (°Brix, masse, rendement) : ces valeurs dépendent du milieu, de la
conduite et du stade de récolte.
* Un chromosome « probable ». Si la source ne le donne pas, écrivez **`n.d.`** — c'est une information en soi.
* Une prédiction de croisement présentée comme un fait : marquez-la **\[extrapolation]**, comme le font déjà les lignes
`Cu × c / tf / e / rg`.
* Une ligne ajoutée dans `data\_en/` **sans sa jumelle dans `data/`** (et inversement) : le build le refuse, et il a raison.

## Format des données

Tout part des fichiers TSV de [`data/`](data) (8 champs) et de leur reflet anglais dans [`data\_en/`](data_en)
(6 champs). Le format complet est décrit dans [`data/README.md`](data/README.md). Règles essentielles :

* séparateur `|`, **8 champs par ligne** (`data/`) ou **6 champs** (`data\_en/`), aucun `|` dans le texte d'un champ ;
* préfixe `# SECTION|<clé>|<titre>|<sous-titre>` pour ouvrir un chapitre (`data\_en` : `# SECTION|<clé>|<titre>|<sous-titre>`,
sans numéro — le numéro vient du fichier français) ;
* codes de dominance : `D` `S` `R` `Q` `O` `E` `M`, éventuellement qualifiés (`D (partiel)`, `R à S`) ;
* une ligne = un locus (ou un groupe d'allèles alléliques, ex. `og`/`og^c`), pas une variété.

```
ovate|Ovate|2|R à S|Fruit ovale, en poire ou piriforme|Codon stop prématuré (SNP G→T) = allèle nul de la famille OFP|Cultivé + S. pimpinellifolium|RÉCESSIF chez S. pimpinellifolium, ADDITIF dans l'IL2-5 de S. pennellii
```

```
ovate|Ovate|2|R à S|Oval, pear or pyriform fruit (Yellow Pear, Mountain Vineyard)|Premature stop (G→T) = null allele of the OFP family; recessive in S. pimpinellifolium, additive in IL2-5|Grown + S. pimpinellifolium
```

## Deux langues, une seule génétique

|Édition|Source|Champs|Rôle|
|-|-|:-:|-|
|[`README.md`](README.md) (français)|`data/\*.tsv`|8|**référence** : ajoute la base moléculaire et l'origine de l'allèle|
|[`README.en.md`](README.en.md) (anglais)|`data\_en/\*.tsv`|6|même contenu utile au sélectionneur, sans la couche moléculaire|

À chaque build, le script compare les deux et **échoue** si elles divergent :

* mêmes 16 chapitres, dans le même ordre ;
* même nombre de lignes par chapitre, **dans le même ordre** ;
* mêmes chromosomes (les chiffres doivent tomber juste) et mêmes codes de dominance ;
* mêmes symboles, à l'exception assumée des lignes descriptives (QTL non clonés, germoplasme, épistasies) dont
l'intitulé est traduit.

Concrètement : **une nouvelle ligne se déclare deux fois** (une par langue), mais une correction de chromosome ou de
dominance se propage automatiquement à la traduction — vous n'avez rien à faire de ce côté-là, le contrôle le vérifie.
Pour traduire une ligne existante, gardez `sym`, `chr` et `dom` caractère par caractère ; seul le texte change.

## Comment proposer

### Par issue (le plus simple)

Ouvrez **Issues → New issue**, puis choisissez le modèle *Correction d'un locus* ou *Nouveau locus*. Remplissez le
champ *Référence* avec un lien ouvert et vérifiable : c'est la seule partie que personne ne peut deviner à votre place.

### Par pull request (le plus rapide)

1. Forkez, éditez le TSV concerné (une ligne = un changement vérifiable). Si vous touchez à `sym`, `chr` ou `dom`,
corrigez les deux langues ; si vous touchez au texte, une seule suffit.
2. Régénérez tout :

```bash
   python3 scripts/build\_fiche.py
   ```

   Le script régénère `README.md`, `README.en.md`, `docs/index.html` et les quatre exports. **Ne modifiez jamais un
README à la main** : ils sont produits, pas écrits.

3. Lisez la sortie du contrôle automatique — les cinq lignes doivent être propres (le nombre de lignes de chaque
README dépend du contenu : ne le comparez pas, comparez le **compte de loci** et les mentions `aucun`) :

```
   216 loci · 16 chapitres FR · 216 loci EN   ← seul compte à vérifier : 216
   README.md — lignes : … · lignes de gènes : 455 · liens internes cassés : aucun · fichiers cités absents : aucun
   README.en.md — lignes : … · lignes de gènes : 239 · liens internes cassés : aucun · fichiers cités absents : aucun
   exports : genes\_tomate.csv / genes\_tomate\_en.csv / genes\_tomate.xlsx
   contrôle FR↔EN : 216 loci alignés (sections, chromosomes, dominance) — aucun écart
   ```

   Un compte de lignes qui bouge est normal quand vous ajoutez une ligne ; une ligne `liens internes cassés`,
`fichiers cités absents` ou `désynchronisation FR/EN` non vide doit être corrigée avant la PR (le script sort alors
en `1`).

4. **Aucun diff parasite** : un rebuild sans changement de donnée produit des fichiers **octet pour octet identiques**,
y compris le classeur (conteneur .xlsx ré-empaqueté avec horodatages figés). Si `git status` affiche un fichier
modifié après un simple
`python3 scripts/build\_fiche.py`, c'est que quelque chose a réellement changé — ou que votre environnement réécrit
l'heure du fichier.
5. Contrôles demandés :

   * la référence primaire a été **ouverte**, pas seulement citée de mémoire ;
   * si vous changez un mode de dominance, dites **sur quoi repose la valeur** (ratio F2 publié, `d/a` calculé sur NIL,
revue, hétérozygote décrit) et sur **quel fond génétique** ;
   * si vous ajoutez une ligne, ajoutez aussi la **conséquence en sélection** (colonne de droite) : c'est la raison d'être
de cette fiche ;
   * le fichier `SOURCES.md` reçoit la référence (une entrée suffit pour les deux langues).
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
* **Identifiants** : dès que possible, donnez le locus ITAG 4.0 (`SolycNNgNNNNNN`) — c'est ce qui rend une ligne
réutilisable par un script ou un BLAST.

## Licence des contributions



