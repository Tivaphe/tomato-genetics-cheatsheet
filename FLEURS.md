# Fleur de la tomate — biologie florale, stérilité mâle et couleur des pétales

![🇫🇷 Français — annexe](https://img.shields.io/badge/%F0%9F%87%AB%F0%9F%87%B7_Fran%C3%A7ais-annexe-64748b?style=for-the-badge) [![🍅 Retour à la fiche](https://img.shields.io/badge/%F0%9F%8D%85_fiche_g%C3%A9n%C3%A9tique-230_loci-0b6e4f?style=for-the-badge)](README.md) [![Licence](https://img.shields.io/badge/licence-MIT-f59e0b?style=flat-square)](LICENSE)

**Annexe de la [fiche génétique de la tomate](README.md) — compilée le 16/10/2026.**

La fiche décrit le *résultat* : une grappe de tant de fleurs, un style inséré, un fruit noué sans pollinisation.
Cette annexe décrit le *réseau* qui produit ce résultat — transition florale, identité des organes (modèle ABCDE
étendu aux Solanacées), boucle WUS–CLV3, développement du tapetum et pigmentations de la fleur. Elle sert à trois
choses : **comprendre pourquoi deux symboles voisins ne se ressemblent pas**, **choisir un outil d'hybridation**
(émasculation ou pas), et **repérer une fleur marquée avant la nouaison**.

Contrairement à [TETRAPLOIDIE.md](TETRAPLOIDIE.md), cette annexe **a modifié la fiche** : treize loci y ont été
ajoutés et deux lignes requalifiées. Le détail est en section 1 — c'est la section à lire si vous ne voulez que le résultat.

- Nomenclature, codes de dominance et conventions de chromosome : voir [Comment lire cette fiche](README.md#comment-lire-cette-fiche).
- Références : [SOURCES.md](SOURCES.md), section 13 « Fleur ». Les affirmations non publiées portent `💬` ou `[extrapolation]`.
- Un chromosome n'est donné que si une source ouverte le permet : voir la méthode en section 9.

---

## 1 · Ce qui est entré dans la fiche

**Treize lignes ajoutées** aux chapitres 1 et 5 (la fiche en compte **230** depuis l'ajout, au chap. 15, d'une ligne « haplo-diploïdisation » qui vient de l'autre annexe, pas de ces dossiers). Tout ce qui suit a été croisé avec les
tableaux existants : aucun des loci ajoutés ne doublonnait une ligne déjà présente.

| Symbole | Chap. | Apport pour vous | Retenu parce que |
|:--|:--|:--|:--|
| `tmf` | 1 | Grappe à 1–2 fleurs, floraison très précoce | Phénotype monogénique exploitable en précocité ; distinct de `sft` |
| `ej2` | 1 | Deuxième pièce de l'épistasie de `j-2` sur la ramification | La fiche notait déjà l'épistasie sans le second gène |
| `FUL2 / MBP20` | 1 | Levier de dosage (édition de promoteur) du nombre de fleurs | Lignée d'édition publiée, phénotype chiffré (+3 feuilles) |
| `sl` | 5 | Stérilité mâle par conversion pétales→sépales | ID ITAG Solyc04g081000 auto-vérifiable (chr 4) |
| `TPI (SlGLO2)` | 5 | Anthères tordues, stigmates exposés : pollinisation à la main facilitée | Quatre noms d'allèles (ms30, ms33, 7B-1, sl-2) à rattacher à un seul gène |
| `Ms-15 (= tm6)` | 5 | Stérilité mâle + stigmate exserté, base du système GHMS | ID Solyc02g084630, mécanisme (délétion d'1 pb) décrit |
| `Ms-10` | 5 | Lignée femelle sans émasculation, tri en pépinière | Cascade du tapetum conservée, marqueur d'anthocyanes lié |
| `ps-2` | 5 | Anthères non déhiscentes **mais pollen viable** | ID Solyc04g015530 (chr 4) ; le seul du lot qui garde du pollen utilisable |
| `tdf1` | 5 | Stérilité mâle **et** nouaison parthénocarpique | ID Solyc03g059200 (chr 3), maillon de cascade |
| `pat-k (tagl6)` | 5 | Parthénocarpie facultative sans nanisme | Mutation définie (rétrotransposon de 4 866 pb, intron 1 de *SlAGL6*) |
| `PYP1` | 5 | Marqueur visuel jaune pâle sur la fleur seule | Voie biochimique explicite (acyltransférase, xanthophylles) |
| `ys` | 5 | Stigmate jaune : datation de floraison, repérage d'hybridation | Gènes cités (*SlC3H1*/*SlC3H2*) et métabolite marqué (chalcone de naringénine) |
| `pmcd1` | 5 | Voie **non transgénique** vers le pollen 2n | Endomitose pré-méïotique documentée (De Storme *et al.* 2013, *JXB* 64:2345, lien OUP) |
| `mc` | 1 | Chr. n.d. → **5** | Le rapport donne l'ID Solyc05g056620, dont le préfixe encode le chromosome |
| `pat / pat-2` | 5 | « non cloné » → bases moléculaires actuelles (*SlHB15A*, *SlHD31*) | Une publication 2024 avec lien PMC, un mécanisme chiffré (délétion de 1 034 pb) |

**Pourquoi si peu, alors que les rapports listent plus de 130 gènes ?** Parce que la fiche est un document de
sélection : elle ne retient que ce qui change une décision de croisement. Les régulateurs amont sans allèle
variétal décrit (SPL13, CSN5B, SlPRR1, SUT4, SlTOE1, SlERF52, IDA/IDL6…) sont listés en section 8, pas en ligne.

---

## 2 · Modèle ABCDE, version Solanacées

La tomate compte **131 gènes MADS-box**, dont **15 « cœur »** pour la fleur. La différence majeure avec
*Arabidopsis* : la **classe B compte quatre gènes** (duplication propre aux Solanacées), ce qui explique la
redondance de tant de phénotypes et les faux « échecs » CRISPR.

| Classe | Gènes tomate | Orthologues *Arabidopsis* | Fonction | Quand ça casse |
|:--|:--|:--|:--|:--|
| **A** | `MC` (Macrocalyx), AP2 | AP1, AP2 | Identité sépale, frein à l'extension de la classe B | `mc` : gros sépales foliacés (chr 5) |
| **B** | `TAP3`/`sl`, `TM6`, `SlGLO1`, `TPI`/`SlGLO2` | AP3, PI | Identité pétale + étamine | perte de B → pétales en sépales, étamines en carpelles |
| **C** | `TAG1`, `TAGL1` | AG | Identité étamine + carpelle, **déterminaison** du méristème | perte de C → fleurs refont des fleurs : la voie du « double flower » |
| **D** | TAGL6, MADS du placenta | AGL8/SEPPOLATA | Ovules, parthénocarpie | `pat-k` = *SlAGL6* (chr 1) |
| **E** | SEP-like (dont `SlMADS1`/`ej2`) | SEP1-4 | Scaffolding des tétramères MADS | additif avec les classes A–D |

**À retenir pour la pratique.** Les complexes MADS sont des **tétramères** : le phénotype dépend du *dosage* des
partenaires, pas de la seule présence/absence d'un gène. D'où, dans cette fiche, trois lignes en « sensible au
dosage » (`sft`, `s`, `MC`) et l'intérêt d'une édition de promoteur plutôt que d'un knock-out (`FUL2`/`MBP20`).

---

## 3 · Combien de fleurs par grappe : le réseau

Schéma « zigzag » du dossier : `VM → TM → IM → SIM → FM → fleur`. **Un retard de maturation du méristème floral =
plus de ramifications et plus de fleurs ; une accélération = fleur solitaire.** Toute la génétique de la grappe est
la lecture de ce curseur.

| Sens du curseur | Gènes | Effet sur la grappe |
|:--|:--|:--|
| **Retarde la maturation → plus de fleurs** | `J`, `SFT` (via répression de `FA` dans l'IM), `STM3` (active `FUL1`), `TM3`, `BIF`, `S` | grappes longues, composées, ramifiées |
| **Accélère → moins de fleurs** | `FA`, `AN`, `TMF`, `BL`, `UF`, `EJ2`, `J2` (réprime `STM3`), `SlTOE1`, `BOP1/2/3`, `DOF9` | 1–2 fleurs, floraison précoce |
| **Redondance à casser d'abord** | `MC`, `FUL2`, `MBP20` (module AP1/FUL) | rien en simple mutant, beaucoup en double |

- **Module antagoniste STM3 / J2 / EJ2 / SlTOE1** : `STM3` promeut le branchage et active `FUL1` ; `J2` (chr 12) le
  réprime ; `EJ2` (*SlMADS1*, chr 3) agit **en additif** avec `J2` ; `SlTOE1` réprime `STM3`/`TM3` en synergie avec
  `EJ2`. C'est la zone la plus « réglable » du génome floral : les allèles faibles y sont préférés aux knock-outs.
- **Florigène / antiflorigène** : `SFT` (chr 3 d'après le dossier) contre `SP` (chr 6), avec `SP5G` (chr 5) en
  répresseur photopériodique. L'essai cité (Lippman *et al.* 2017, *Nat. Genet.* 49:927) : **`sft/+` hétérozygote
  sur fond `sp` = +60 % de rendement**, en dose-dépendance — c'est la base des hybrides industriels, et le seul
  cas de la fiche où un *hétérozygote* est l'objectif.
- **Photopériode** : la tomate moderne est *day-neutral* par **délétion de 52 pb dans le 3′UTR de `SP5G`** (sweep de
  domestication, Zhang *et al.* 2018). `SP5G` en CRISPR = floraison jour-neutre et récolte plus précoce.

---

## 4 · Méristème floral : la boucle WUS–CLV3

| Locus | Ce que dit le dossier | Ce que ça change au jardin |
|:--|:--|:--|
| `lc` (LOCULE NUMBER, = *SlWUS*, Solyc02g083950, chr 2) | **deux SNP à 1 080 pb en aval**, dans une boîte CArG → **gain de fonction** : expression de WUS élargie | méristème floral plus large : + étamines, + pétales, 2 → 3–4 loges, fruit légèrement aplati |
| `fas` (FASCIATED, = *SlCLV3*, Solyc11g071380, chr 11) | **inversion de 294 kb dont un point de cassure à ~1 kb en amont** = perte de fonction **partielle** du promoteur de CLV3 | fasciation marquée : 6 à >20 loges, fruit côtelé type Brandywine |
| les deux ensemble | effet **synergique épistatique** sur le nombre de loges (p < 0,001) | le double `lc/lc fas/fas` donne la fleur double et le fruit « messy » des lignées anciennes |

**Trois lectures utiles.** (i) Ce sont des **pertes de régulation**, pas des pertes de fonction : la boucle reste
active, son **domaine d’expression** change — d'où des hétérozygotes déjà visibles et une gamme de phénotypes au lieu
d'un tout-ou-rien. (ii) Le dossier rattachait `fas` à *SlCLV3* **+** *SlYABBY2b* (Solyc11g071810) : la fiche a
**déjà tranché** (section « Pièges et corrections »), l'hypothèse YABBY2b de 2008 est abandonnée — le rapport est en
retard sur la fiche, et c'est le seul cas des deux dossiers où la correction vient du dépôt. (iii) Le « bruit »
autour de ces deux loci a son adresse : la ligne `FAB / CLV1, FIN, SlTPL3, SlKNUCKLES` du chap. 6. Marqueur de tri
proposé par le dossier amateur `💬` : **fruit à plus de 6 loges**.

---

## 5 · Stérilité mâle : catalogue et usage en hybridation

La cascade du tapetum, conservée d'*Arabidopsis* : **MS10 → MS32 → TDF1 → AMS → MS1**. Toucher un maillon haut
(Ms-10, TDF1) supprime le pollen ; toucher les gènes B de classe (`TM6`, `TPI`, `TAP3`) **déforme l'anthère** et
expose le stigmate — ce n'est pas la même chose au champ.

| Outil | Gène / ID | Phénotype | Usage réel |
|:--|:--|:--|:--|
| `ps-2` | *SlTDPG*, Solyc04g015530 (chr 4) | anthère **non déhiscente**, pollen viable | hybridation **sans émasculation**, pollen récupérable ; maintien de la lignée possible |
| `Ms-10` | bHLH, Solyc02g079810 (chr 2) | aucun pollen, ovaire normal | femelle de F1 ; tri pépinière par le marqueur d'anthocyanes lié (`aa` : plantule verte = stérile, pourpre = fertile) `⚠` |
| `Ms-15` / `tm6` | MADS B, Solyc02g084630, délétion d'1 pb exon 1 (allèle *sus2*) | étamines carpelloïdes, stigmate exserté | base du **GHMS** ; rend aussi la lignée **hybridable à l'insu** : à isoler |
| `TPI` | *SlGLO2*, Solyc08g067230 (chr 8) | anthères tordues ouvertes sur le style | pollinisation manuelle très simple, testeur d'allogamie |
| `sl` | *TAP3*, Solyc04g081000 (chr 4) | pas d'étamines, pétales→sépales | même usage, fleur plus ouverte encore |
| `tdf1` | R2R3-MYB (*AtMYB35*), Solyc03g059200 (chr 3) | stérilité + parthénocarpie partielle | serre chaude : noue sans pollen |
| `pmcd1` | cytokinèse pré-méïotique | dyades (grains binucléés) au lieu de tétrades | **pollen 2n non transgénique**, voir [TETRAPLOIDIE.md §4.6](TETRAPLOIDIE.md#46-autres-méthodes-dobtention-documentées-non-recommandées-hors-laboratoire) |

> **Système GHMS** (le seul « kit » complet que ces rapports apportent) : double knock-out CRISPR **`tm6` + `dfr`**
> → les plantules à **hypocotyle vert sont stériles**, celles à hypocotyle **violet sont fertiles** ; tri en
> pépinière, sans PCR ni attente de la floraison. Source citée avec lien : Agronomy 13:1785 (2023).
> `⚠` Système brevetable et dépendant du fond : à vérifier avant tout usage en semences destinées à la vente.

**Deux nuances que le dossier ne tranche pas.** (i) `ms-24`, `ms-35` et `ms-36` sont listés comme **allèles de
`Ms-10`** (= *SlDYT1*) par les deux dossiers : mentionnée, mais sans ID par allèle, donc en note de ligne et non en
ligne. (ii) `Ms10^35` régulerait **246 gènes** de la méiose, de la paroi pollinique et du métabolisme lipidique :
ordre de grandeur de pléiotropie, pas une liste de cibles.

---

## 6 · Couleur de la fleur et marqueurs visuels

Deux voies, deux usages. **Caroténoïdes** (jaune des pétales) et **anthocyanes** (pourpre des tiges, anthères, hypocotyles).

| Locus | Voie | Marqueur | Limite d'usage |
|:--|:--|:--|:--|
| `PYP1` | estérification des xanthophylles (néoxanthine, violaxanthine) par une acyltransférase | pétales **jaune pâle**, anthères décolorées | aucun effet sur le fruit ni sur la saveur |
| `ys` | perte des *SlC3H1*/*SlC3H2* (F3'H) → chalcone de naringénine, 6 peroxydases inhibées | stigmate **jaune vif** | ⚠ ne pas lire `y` : `y` = *SlMYB12* (chr 1), peau jaune du fruit |
| `CCD4` | clivage des caroténoïdes | fleurs **blanchâtres** (polymorphisme) | signal discret, difficile sur photo |
| β-carotène hydroxylase | conversion jaune→blanc | pétales pâlissants | non cloné dans le dossier |
| complexe MBW (`SlAN2`/`SlMYB75`, `SlANT1`, `SlMYB114`, `SlMYB28`, `SlAN1`/`SlTT8`, `SlJAF13`, `SlAN11`, répresseurs `SlMYB-ATV`, `SlMYBL2`) | anthocyanes | tiges, sépales, anthères et **hypocotyles pourpres** | c'est ce complexe que le GHMS et le marqueur `aa` mettent à profit |

**Pourquoi ça compte pour vous** : une marqueur *sur la fleur* se lit 3 à 5 semaines avant la nouaison. Un semis à
hypocotyle coloré se trie à la main ; un stigmate jaune dit le jour exact d'une floraison ; un pétale pâle signale
une fleur dont l'anthère n'a pas fonctionné. Aucun de ces trois ne touche au goût — contrairement aux gènes de
couleur du fruit (`r`, `t`, `og`) avec lesquels on les confond.

---

## 7 · QTL de traits floraux et environnement

À utiliser pour lire une carte, pas pour promettre un phénotype.

| Trait mesuré | Localisation donnée par le dossier |
|:--|:--|
| `SEPN` nombre de sépales | chr 2 et 11 — en réalité les loci `lc` et `fas` |
| `PETN` nombre de pétales | chr 2 et 11 |
| `STAN` nombre d'étamines | influencé par `fas` |
| `STYW` épaisseur du style | corrélée au nombre de carpelles |
| `OVAA` aire de l'ovaire | influencée par `fas` |
| nombre de fleurs par grappe | chr 2, 3, 5, 7, 11 |
| longueur des pétales | chr 9 |
| `dtf5` / `ln5` (temps de floraison, longueur d'entre-nœud) | chr 5, pléiotropie impliquant *PHYB2* |
| `qLF2.1` (temps de floraison) | chr 2, gène causal *SlJMJ14* (déméthylase d'histone) |

**Température.** Deux signaux opposés, tous deux cités sans mesure reproductible : le **froid** accentue la
fasciation sur fond `lc`/`fas` `💬`, et **`an` homozygote** ne ferait plus qu'une fleur terminale sous forte
chaleur. `MIB2` (orthologue SPATULA) ne contrôle le branchage que **sous chaleur**. Autrement dit : la ramification
d'une grappe est en partie une variable climatique — comparez vos lignées sur la même fenêtre de semis, sinon vous
mesurez la météo.

---

## 8 · Pistes non retenues, et pourquoi

| Piste du dossier | Motif du refus |
|:--|:--|
| `ssp` (« SUPPRESSOR OF SP / FD », chr 12, bZIP ; « supprime `sp`, restaure l'indéterminé ») | **aucune référence** dans la ligne du dossier ; effet trop commode pour être accepté sans source primaire |
| `SPGB` (partenaire 14-3-3 de SFT dans le complexe FAC) | colonne référence vide (« — ») |
| `DefH9-iaaM` (parthénocarpie transgénique) | **construct transgénique**, pas un locus : hors périmètre de la fiche, qui décrit des allèles existant dans le germoplasme |
| `SPL13`, `CSN5B`, `SlPRR1`, `SUT4`, `SlTOE1`, `FTL2`, `SlJMJ14`, `BOP1/2/3`, `MIB2`, `DOF9`, `LIN`, `IDA`/`IDL6`, `SlERF52`, `SlCMB1`, `SlMADS48`, `TAGL11`/`TAGL12`, `SlARF5/7/8` | régulateurs amont **sans allèle variétal ni phénotype chiffré** actionnable : cités dans les sections 3 et 7, pas en ligne de tableau |
| `ms-24`, `ms-35` | présentés comme allèles de `Ms-10` par une source unique : intégrés comme **note** de la ligne `Ms-10`, pas comme lignes |
| QTL de floraison « chr 1, 2, 3, 4, 5, 6, 10, 11, 12 » | liste de chromosomes sans effet ni intervalle : inutilisable en sélection |

### Requalifications proposées **et vérifiées via ITAG**

Le dossier affirmait un chromosome pour sept lignes que la fiche laissait initialement en `n.d.` sans fournir leur ID ITAG. Le croisement avec les annotations officielles ITAG / UniProt permet de confirmer ces identifiants et d'intégrer leurs chromosomes dans la fiche :

| Ligne | Fiche initiale | Dossier | Preuve ITAG vérifiée | Application |
|:--|:--|:--|:--|:--|
| `mc` | n.d. | chr 5 | **Solyc05g056620** (*MACROCALYX*) | ✅ **appliquée** (chr 5) |
| `sft` | n.d. | chr 3 | **Solyc03g063100** (*SINGLE FLOWER TRUSS*) | ✅ **appliquée** (chr 3) |
| `sp5G` | n.d. | chr 5 | **Solyc05g053850** (*SELF-PRUNING 5G*) | ✅ **appliquée** (chr 5) |
| `an` | n.d. | chr 2 | **Solyc02g081670** (*ANANTHA*, F-box UFO) | ✅ **appliquée** (chr 2) |
| `fa` | n.d. | chr 3 | **Solyc03g118160** (*FALSIFLORA*, orthologue *LFY*) | ✅ **appliquée** (chr 3) |
| `bl` | n.d. | chr 11 | **Solyc11g069030** (*BLIND*, R2R3-MYB) | ✅ **appliquée** (chr 11) |
| `pat` | n.d. | chr 3 | **Solyc03g120910** (*SlHB15A*, HD-Zip III) | ✅ **appliquée** (chr 3) |
| `pat-2` | n.d. | chr 4 | **Solyc04g080490** (*SlHD31*, ZF-HD) | ✅ **appliquée** (chr 4) |

### Désaccords internes aux deux dossiers, laissés ouverts

Ils sont signalés ici plutôt qu'arbitrés, parce qu'aucun des deux ne donne de preuve ouvrable :

1. **`Style2.1`** : la fiche cite *Solyc02g087860* (polypeptide à motif HLH, délétions promotrices StyleD1/StyleD2) ;
   les dossiers rattachent le même chromosome 2 à **TAG1/TAGL1** (Solyc02g071730). Même chromosome, deux gènes
   candidats — la ligne de la fiche n'est pas modifiée.
2. **`SlCUF1` et `TM6`** reçoivent dans le même tableau le **même ID** (Solyc02g084630) : l'un des deux est faux,
   et aucune des deux lignes ne donne de source pour le trancher.
   Seule l'attribution `tm6` = Ms-15 est reprise (elle porte un mécanisme chiffré : délétion d'1 pb, exon 1).
3. **`an`** : « F-box, orthologue d'UFO » dans les deux dossiers — confirmé par ITAG (**Solyc02g081670**, Lippman *et al.* 2008).
4. **`pat-2`** : le dossier mentionne « Severianin » comme s'il s'agissait d'un auteur ; il s'agit en réalité du **cultivar parthénocarpique russe 'Severianin'** (sélectionné par N. P. Solovieva, donneur historique de l'allèle `pat-2` = *SlHD31*, Solyc04g080490, cloné par Nunome *et al.* 2021).
5. **`pmcd1`** : un des deux dossiers résume le mutant par « fusion nucléaire pré-méïotique → méiocytes
   tétraploïdes », l'autre par « dyades au lieu de tétrades ». Les deux décrivent la même cellule ratée ; la fiche
   garde la formulation du premier, seule accompagnée d'une référence avec lien.

---

## 9 · Méthode, critères, limites

- **Critère d'ajout.** Un gène entre en ligne si (i) un phénotype **mesurable au jardin** est énoncé, (ii) une
  **base moléculaire** est donnée (famille, type de mutation, ID), et (iii) le tout vient d'une source citée.
  Trois conditions sur 130 gènes recensés : 13 retenues.
- **Contrôle automatique du chromosome.** Quand un ID ITAG `SolycNNgGGGGGG` est fourni, `NN` **doit** égaler la
  colonne `Chr.` : c'est la seule vérification possible sans accès au web (seule l'API GitHub est joignable ici).
  Les huit ID ITAG introduits par cette passe ont passé ce contrôle, et l'audit du dépôt ne relève **aucun** conflit `SolycNN` ↔ `Chr.` sur
  les 230 lignes.
- **Rien n'a été « re-cliqué ».** Les liens repris des dossiers (MDPI, Nature, PLOS, PMC, HAL) sont recopiés tels
  quels dans [SOURCES.md](SOURCES.md) avec le marqueur `✓` : `✓` signifie « DOI/URL présent dans le dossier de
  compilation », **pas** « consulté ». Aucun `🔎` n'a été ajouté ici.
- **Ce que l'annexe ne change pas.** Aucun code de dominance existant n'a été modifié, aucun locus retiré. Les
  deux seules touches aux lignes en place sont `mc` (chromosome) et `pat / pat-2` (base moléculaire).
- **Traduction.** Comme [SOURCES.md](SOURCES.md) et [TETRAPLOIDIE.md](TETRAPLOIDIE.md), cette annexe n'a **pas
  d'équivalent anglais** : les treize lignes ajoutées ont leur reflet dans [`README.en.md`](README.en.md), le réseau
  reste en français.
- **Pratique amateur ≠ fait génétique.** Les passages marqués `💬` (fleurs doubles des lignées anciennes, projet
  « promiscuous » de J. Lofthouse, retours multiflora, fasciation stable de « Voyager ») décrivent des tentatives
  et des tours de main : ils ne soutiennent aucune ligne de dominance.

### Ce que le dossier amateur dit des fleurs ouvertes

Résumé en une phrase de chaque piste, sans validation : **J. Lofthouse** a sélectionné, sur *S. habrochaites* ×
*S. lycopersicum*, des fleurs plus grandes à anthères non soudées et stigmate exserté pour faire entrer les
bourdons — avec un taux d'allogamie annoncé de 0–5 % en début de saison à ~20 % en milieu de saison `💬`. Les
retours de forum sur les lignées *multiflora* (Ildi, Rose Quartz, Blondköpfchen, Karma Purple) décrivent une
première grappe de 200–400 fleurs mais une nouaison de 20–40 %, et une production totale pas toujours supérieure à
un hybride indéterminé `💬`. Deux tours de main circulent pour la nouaison sous chaleur : **ne pas secouer la
grappe, laisser faire les bourdons**, et **sélectionner les plus grosses fleurs au printemps**, le froid
accentuant la fasciation `💬`.

---

Retour à la [fiche génétique (230 loci)](README.md) · [édition anglaise](README.en.md) ·
[annexe ploïdie](TETRAPLOIDIE.md) · [SOURCES.md](SOURCES.md) · [CONTRIBUTING.md](CONTRIBUTING.md) · [LICENSE](LICENSE) — MIT

<sub>Annexe consolidée le 16/10/2026 à partir de deux dossiers de recherche bibliographique (gènes de la fleur,
biologie florale), croisés entre eux et avec les 216 lignes alors en place. Les références n'ont pas été ré-ouvertes :
liste des entrées, liens et niveaux de preuve dans [SOURCES.md](SOURCES.md), section 13.</sub>
