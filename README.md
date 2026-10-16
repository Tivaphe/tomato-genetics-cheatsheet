# Fiche génétique de la tomate 🍅

![🇫🇷 Français — cette édition](https://img.shields.io/badge/%F0%9F%87%AB%F0%9F%87%B7_Fran%C3%A7ais-cette_%C3%A9dition-64748b?style=for-the-badge)  [![🇬🇧 English — lire cette fiche en anglais →](https://img.shields.io/badge/%F0%9F%87%AC%F0%9F%87%A7_English-lire_cette_fiche_en_anglais_%E2%86%92-0b6e4f?style=for-the-badge)](README.en.md)

**216 loci documentés — gènes du port, du feuillage, du fruit, de la saveur, de la nutrition et des résistances — avec leur mode de dominance et ce que ça change concrètement en croisement.**

[![Loci](https://img.shields.io/badge/loci-216-0b6e4f?style=flat-square)](#sommaire) [![Chapitres](https://img.shields.io/badge/chapitres-16-1d4ed8?style=flat-square)](#sommaire) [![Version interactive](https://img.shields.io/badge/version%20interactive-index.html-6d28d9?style=flat-square)](index.html) [![Annexe ploïdie](https://img.shields.io/badge/annexe%20plo%C3%AFdie-TETRAPLOIDIE.md-1d4ed8?style=flat-square)](TETRAPLOIDIE.md) [![Licence](https://img.shields.io/badge/licence-MIT-f59e0b?style=flat-square)](LICENSE) ![MAJ](https://img.shields.io/badge/mis%20%C3%A0%20jour-15%2F10%2F2026-64748b?style=flat-square)

> **Deux éditions, une seule génétique.** Le bouton ci-dessus bascule vers [l'édition anglaise](README.en.md) : mêmes loci, mêmes chromosomes, mêmes codes de dominance — la parité se vérifie à chaque retouche (procédure dans [CONTRIBUTING.md](CONTRIBUTING.md)). La couche moléculaire — nature de la mutation, origine de l'allèle, accessions — n'existe que dans cette édition-ci, et `index.html` n'en est que le reflet interactif.

> **Pour qui ?** Sélectionneurs amateurs avancés, maraîchers, étudiants et chercheurs en amélioration des plantes. Chaque ligne répond à trois questions : *quel gène, sur quel chromosome, dominant ou récessif* — et *donc : est-ce que je le vois dès la F1, ou faut-il que je sème 200 plants*.

`216 loci` · `16 chapitres` · `1 annexe ploïdie` · littérature vérifiée jusqu'en 2026 · les affirmations non publiées sont explicitement marquées **[extrapolation]**.

## L'essentiel en 12 points

1. Le phénotype **sauvage** de la tomate est rond, rouge, à peau jaune-mate, indéterminé, à feuille composée et de taille normale : la quasi-totalité des allèles « mutants » utilisés par les sélectionneurs sont donc **récessifs** (perte de fonction).
2. **Le meilleur prédicteur de la dominance n'est pas le phénotype mais la nature de la mutation** : gain de fonction (duplication, promoteur, surexpression) ⇒ dominant ou semi-dominant ; perte de fonction (codon stop, délétion, frameshift) ⇒ récessif.
3. Le **port déterminé** est récessif (`sp/sp`) : contrairement à une idée reçue, c'est l'indéterminé qui domine, parce que `SP` est un antiflorigène et que son allèle fonctionnel suffit.
4. La forme du fruit se lit sur **deux axes indépendants** (longueur : `SUN`, `OVATE`, `FS8.1`, `PT` ; loges/aplati : `LC`, `FAS`, `ENO`, `globe`) plus un troisième pour la masse (`fw2.2`, `fw3.2`, `fw11.3`).
5. La couleur = **3 couches cumulables** : caroténoïdes de la chair (`r`, `t`, `B`, `og`) × flavonoïdes de la peau (`Y`/`y`) × chlorophylle résiduelle (`gf`, `u`). Trois gènes en homozygotie suffisent à obtenir un fruit entièrement vert.
6. Le **rose** n'est pas une couleur de chair : c'est un fruit rouge `R_` vu à travers une peau **dépourvue de flavonols** (`y/y`, *SlMYB12*, chr 1) — donc aussi privé d'une part de sa valeur nutritionnelle.
7. Le **goût** est un puzzle à 5 pièces (sucres, acides, ~15 volatils clés, acides aminés libres dont le glutamate, amertume) : la sélection sur le seul °Brix est insuffisante, car certains volatils augmentent la douceur *perçue* sans changer le sucre mesuré.
8. **`TomLoxC` est en surdominance** : l'hétérozygote exprime plus d'arôme que les deux homozygotes. C'est l'argument génétique fort pour évaluer — et parfois vendre — des **F1** plutôt que des lignées pures sur ce caractère.
9. La **conservation** et l'**arôme** sont aux mains des mêmes régulateurs (`RIN`, `NOR`, `FUL1/2`) : bloquer la maturation (`rin`, `nor`, `Cnr`) détruit aussi le parfum. Le compromis est génétique, pas une question de chance.
10. Presque tous les allèles d'intérêt gustatif ou nutritionnel ont été **perdus à la domestication** (`TomLoxC` rare, `SlCDPK27` haut-sucre, allèles forts de `DXR`, `GAME9`/`GE1`) : les récupérer suppose une introgression depuis les sauvages ou une édition ciblée (CRISPR).
11. Chez les **Galápagos** (*cheesmaniae*, *galapagense*) et chez *habrochaites*, les introgressions traversent des **inversions chromosomiques** (jusqu'à 18–21 Mb) : la recombinaison y est bloquée, le linkage drag est structurel — prévoyez des populations fines.
12. La dominance **n'est pas une constante du locus** : `d/a` change avec le couple de parents et avec le caractère mesuré (`fs8.1` : −0,47 pour la forme, +1,14 pour le poids). Toute valeur de ce dépôt est une *bonne supposition à vérifier sur votre population*, jamais une loi.

## Comment lire cette fiche

Une ligne = un locus. La colonne **Dominance** est l'information qui décide de tout le protocole de croisement :

| | Mode de dominance | Signification | Conséquence pratique |
|:--|:--|:--|:--|
| 🟢 | **DOMINANT** | S'exprime dès la F1 : un seul parent donneur suffit. | Un seul parent donneur suffit : le caractère est acquis dès la F1, donc rentable aussi en hybride. |
| 🟡 | **SEMI-DOMINANT** | Hétérozygote intermédiaire : effet de dosage. | L'hétérozygote est intermédiaire : le marqueur (ou la mesure en F2) devient indispensable pour savoir ce que vous avez vraiment. |
| 🔵 | **RÉCESSIF** | Deux copies nécessaires : à fixer à l'homozygotie (25 % en F2). | Tri en F2 (25 % par caractère) ou marquage co-dominant sur semis ; à fixer en lignée pure avant de juger le fruit. |
| 🟣 | **QTL / ADDITIF** | Caractère quantitatif : sélection par marqueurs ou génomique. | Aucun tri monogénique possible : progresser par QTL cumulés, sélection phénotypique répétée sur plusieurs années/locations, ou sélection génomique. |
| 🟠 | **SURDOMINANCE** | L'hétérozygote dépasse les deux homozygotes (hétérosis). | Ne PAS fixer : l'état optimal est l'hétérozygote. Évaluez vos F1, pas vos lignées. |
| ⚫ | **ÉPIGÉNÉTIQUE** | Méthylation : hors dominance mendélienne, l'ADN ne prédit pas tout. | Le génotype ADN peut mentir : prévoir un phénotypage direct ou un épi-marqueur (méthylation). |
| ⚪ | **MIXTE / SELON FOND** | La dominance change avec le fond génétique ou le caractère mesuré. | Repérer la dominance sur VOTRE population : la valeur publiée vaut pour un fond donné, pas pour le vôtre. |

**Notation.** `R_` = au moins un allèle *R* (dominant exprimé) · `yy` et `gf/gf` = homozygote récessif · `Sp/sp` = hétérozygote — chez les semi-dominants, c'est là que se joue le *niveau* d'expression (port, résistance, Brix). `n.d.` = locus non cartographié finement dans les sources compilées : **à ne pas inventer**. `Chr.` = chromosome de la carte SL4.0 (ITAG 4.0). `—` en dominance = ligne de germoplasme ou combinaison épistatique, pas un locus mendélien ; un libellé qualifié (`Q (additif)`, `RÉCESSIF → SEMI-DOMINANT`) garde la précision du fichier d'entrée.

Les loci sont rangés en **16 chapitres** : plante (port, feuillage, trichomes, pigmentation, fleur), fruit (forme, couleur, maturation), saveur (sucres, acides, volatils), nutrition, résistances biotiques, tolérances abiotiques, sources alléliques et épistasies. La **ploïdie** — doublement chromosomique, dosage tétrasomique, triploïdes sans pépins — n'est pas un chapitre : elle occupe une annexe dédiée, [TETRAPLOIDIE.md](TETRAPLOIDIE.md), parce qu'elle change les règles de ségrégation de tous les loci ci-dessous sans devenir un locus elle-même. **Ces tableaux sont la source** : le dépôt ne contient ni fichier de données ni script de génération — il se relit et se corrige directement ici. [`index.html`](index.html), à la racine, en est le pendant interactif (aucune dépendance réseau) : recherche plein texte, filtres par mode de dominance, calculateur d'effectif F2 et style d'impression A4 paysage, publiable tel quel sur GitHub Pages. Une correction se reporte donc à la main dans les trois fichiers concernés — `README.md`, `README.en.md` et `index.html`.

## Sommaire

- [1. Port, architecture & inflorescence](#1-port-architecture--inflorescence) — *29 loci*
- [2. Feuillage — morphologie foliaire](#2-feuillage--morphologie-foliaire) — *15 loci*
- [3. Trichomes & pubescence](#3-trichomes--pubescence) — *6 loci*
- [4. Feuillage — couleur & pigmentation](#4-feuillage--couleur--pigmentation) — *12 loci*
- [5. Fleur, autogamie & nouaison](#5-fleur-autogamie--nouaison) — *5 loci*
- [6. Fruit — forme, loges & poids](#6-fruit--forme-loges--poids) — *16 loci*
- [7. Fruit — couleur (peau × chair)](#7-fruit--couleur-peau--chair) — *12 loci*
- [8. Fruit — maturation & conservation](#8-fruit--maturation--conservation) — *5 loci*
- [9. Saveur — sucres & solides solubles](#9-saveur--sucres--solides-solubles) — *13 loci*
- [10. Saveur — acidité, umami & GABA](#10-saveur--acidité-umami--gaba) — *8 loci*
- [11. Saveur — volatils & arôme](#11-saveur--volatils--arôme) — *17 loci*
- [12. Nutrition & innocuité](#12-nutrition--innocuité) — *17 loci*
- [13. Résistances biotiques](#13-résistances-biotiques) — *27 loci*
- [14. Tolérances abiotiques & racines](#14-tolérances-abiotiques--racines) — *11 loci*
- [15. Sources alléliques : votre germoplasme](#15-sources-alléliques--votre-germoplasme) — *7 loci*
- [16. Combinaisons & épistasies](#16-combinaisons--épistasies) — *16 loci*
- **Annexe · [Ploïdie : diploïdie, tétraploïdisation, triploïdes sans pépins](TETRAPLOIDIE.md)** — *hors des 216 loci*
- [Prédire la couleur du fruit](#prédire-la-couleur-du-fruit)
- [Calculer la taille de sa descendance](#calculer-la-taille-de-sa-descendance)
- [Les 10 règles d'or](#les-10-règles-dor)
- [Marqueurs et génotypage](#marqueurs-et-génotypage)
- [Pièges et corrections apportées](#pièges-et-corrections-apportées)
- [Protocole de programme](#protocole-de-programme)
- [Reproductibilité du dépôt](#reproductibilité-du-dépôt)
- [Sources, licence et citation](#sources-licence-et-citation)
- [SOURCES.md](SOURCES.md) — bibliographie complète · [CONTRIBUTING.md](CONTRIBUTING.md) · [LICENSE](LICENSE)

---

## 1. Port, architecture & inflorescence

*Déterminaison, ramification, taille, organogenèse de la grappe — le moteur SP/SFT.* — **29 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `sp` | Self-pruning (SP) | 6 | 🔵 RÉCESSIF | Port déterminé : la tige se termine par 1–2 inflorescences, croissance arrêtée, maturation groupée | F1 SP/sp = indéterminé ; 25 % de déterminés en F2. Pour un plant « vivant » continu (type bonsaï), garder SP. |
| `sft` | Single flower truss | n.d. | 🟡 SEMI-DOMINANT | Inflorescences à 1–3 fleurs, feuilles dans l'inflorescence, arrêt précoce | Récessif mais SENSIBLE AU DOSAGE : sft/+ = port semi-déterminé (très utilisé en sélection). Ne pas le traiter en 3:1 simple. |
| `sp5G` | Self-pruning 5G | n.d. | 🔵 RÉCESSIF | Perte de sensibilité au jour long → floraison précoce, port plus compact | Combine précocité et croissance continue. |
| `uf` | Uniflora | n.d. | 🔵 RÉCESSIF | Sympodes allongés, floraison tardive, tige unique | Mutant de référence (sympodes allongés, floraison tardive) : rarement utilisé en variétal, précieux pour décrypter un port anormal. |
| `s` | Compound inflorescence | 2 | 🔵 RÉCESSIF | Grappes très ramifiées, jusqu'à ~200 fleurs (grappes « multiflores ») | j est épistatique sur s : j supprime la ramification de l'inflorescence. |
| `an` | Anantha | n.d. | 🔵 RÉCESSIF | Inflorescences indéfiniment ramifiées, fleurs peu différenciées | Fleurs peu différenciées, stérilité partielle : outil de laboratoire, pas un caractère à introduire en variétal. |
| `fa` | Falsiflora | n.d. | 🔵 RÉCESSIF | Inflorescences feuillues, conversion des fleurs en tiges | Inflorescences feuillues : diminue la récolte ; sert surtout à diagnostiquer une grappe « Leafy ». |
| `j` | Jointless | 11 | 🔵 RÉCESSIF | Absence de zone d'abscission du pédoncule ; épistatique sur s ; réversion végétative de l'inflorescence | Casse la ramification des grappes mais provoque un excès de feuillage → préférer j-2. |
| `j-2` | Jointless-2 | 12 | 🔵 RÉCESSIF | Pédoncule court, droit, sans coude : le fruit se cueille net, sans calice ni blessure | Quasi ubiquitaire en tomate de transformation. Épistasie négative avec ej2 (chr 3), levée par suppresseurs. |
| `mc` | Macrocalyx | n.d. | 🔵 RÉCESSIF | Grand calice, inflorescence modifiée | Calice hypertrophié, gène MADS-box : utile en génétique florale, sans intérêt commercial direct. |
| `to` | Torosa | n.d. | 🔵 RÉCESSIF | Fleurs et ovaires « en tire-bouchon » | Fleurs en tire-bouchon, nouaison aléatoire : à éliminer en sélection, pas à introduire. |
| `bif` | Bifurcate flower truss | n.d. | 🔵 RÉCESSIF | Grappes ramifiées (comme s), renforcées par le froid | Grappes ramifiées aggravées par le froid : attention dans les programmes plein champ en climat frais (méprise fréquente avec `s`). |
| `Nr` | Never ripe | n.d. | 🟢 DOMINANT | Sénescence et abscission retardées (feuilles, fleurs, fruits) ; fruit qui ne mûrit pas | SEMI-DOMINANT À DOMINANT NÉGATIF : la protéine mutante empoisonne le complexe. Voir aussi section Maturation. |
| `ls` | Lateral suppressor | n.d. | 🔵 RÉCESSIF | Absence de bourgeons axillaires → plante non ramifiée ; parfois moins de folioles | Absence totale de gourmands = conduite simplifiée, MAIS rendement en berne sur les premiers bouquets ; jamais retenu en variétal. |
| `bl` | Blind | n.d. | 🔵 RÉCESSIF | Ramification très réduite, bourgeons axillaires absents/réduits | Le même module MYB dissèque aussi la feuille. |
| `slbrc1 / slbrc2` | Blind-like / BRC-like | n.d. | 🔵 RÉCESSIF | Contrôle de la dormance des bourgeons axillaires (interagit avec WO) | Dormance des bourgeons : cible de recherche sur le buissonnage, pas de variété portant ces mutants documentée. |
| `d (dx, d-im)` | Dwarf | 2 | 🔵 RÉCESSIF | Nain compact : entre-nœuds courts, tige épaisse, feuilles rugueuses vert sombre | Base des variétés naines. F1 toujours haute ; d/d ressort chez 25 % des F2. Micro-Tom = d + sp (+ mnt). |
| `br` | Brachytic | 1 | 🔵 RÉCESSIF | Entre-nœuds ultra-courts, tige robuste, ramifications latérales fortes, fruits regroupés | Idéal pour de gros fruits sur plant compact : N'ALTÈRE PAS le calibre. |
| `mnt` | Miniature | n.d. | 🔵 RÉCESSIF | Micro-nain extrême (15–20 cm), insensible aux gibbérellines | Se combine avec d et sp. |
| `dpy` | Dumpy | n.d. | 🔵 RÉCESSIF | Nain, ramification réduite, feuilles altérées ; rattrapé par application de brassinolide | Nain BR rattrapé par la brassinolide : outil de diagnostic de la voie des brassinostéroïdes (distingue `d`/`cu-3`). |
| `cu-3` | Curl-3 | 4 | 🔵 RÉCESSIF | Nain extrême, feuilles recourbées vert sombre, insensible au BR | ⚠ À NE PAS CONFONDRE avec Cu (curl, dominant) ni cu/cu-2 (curled). |
| `dgt` | Diageotropica | n.d. | 🔵 RÉCESSIF | Croissance diageotrope (horizontale), feuilles hyponastiques, racines altérées | Croissance diageotrope + racines anormales : intéressant en génétique racinaire, pénalisant en culture. |
| `pro` | Procera | n.d. | 🔵 RÉCESSIF | Plante plus grande, internœuds allongés, feuilles fines et moins lobées ; réponse GA constitutive | Plante haute à tige fragile, feuilles moins lobées : contre-épreuve de la voie GA (les nains `gib` sont l'opposé). |
| `gib-1` | Gibberellin deficient-1 | n.d. | 🔵 RÉCESSIF | Nain, germination dépendante des GA, feuilles plus petites vert sombre | Les nains GA sont souvent plus compacts que les nains BR. |
| `gib-2` | Gibberellin deficient-2 | n.d. | 🔵 RÉCESSIF | Nain sévère | Nain sévère réversible par GA : test de diagnostic — un nain `gib` verdit et s'allonge à l'application de GA, un nain `d` non. |
| `gib-3` | Gibberellin deficient-3 | n.d. | 🔵 RÉCESSIF | Nain sévère | Nain sévère (KS) : idem `gib-2`, sert à distinguer déficience GA et insensibilité aux GA (`cu-3`). |
| `epi` | Epinastic | n.d. | 🔵 RÉCESSIF | Feuilles fortement épinastiques (recourbées vers le bas), tiges épaissies | ⚠ À NE PAS CONFONDRE avec un stress hydrique, un herbicide ou une virémie : épinastie ici est génétique et récessive, présente dès le jeune plant. |
| `not / fl / sit` | Notabilis / Flacca / Sitiens | n.d. | 🔵 RÉCESSIF | Feuilles enroulées, flétrissement (déficience en ABA) | Sensibles au stress hydrique. |
| `erl` | Erectoid leaf | 10 | 🟡 SEMI-DOMINANT | Feuilles érigées : angle d'insertion réduit, port dressé | Semi-dominant : l'hétérozygote suffit pour un effet net. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (29 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `sp` | SP = PEBP antiflorigène (orthologue TFL1/CEN), Solyc06g074350 ; mutation P76L ; allèles faibles (sp-weak) → compacités intermédiaires | Cultivé (mutant classique) | RÉCESSIF | 6 |
| `sft` | SFT = florigène FT (interrupteur SP antiflorigène / SFT florigène) | Cultivé | SEMI-DOMINANT | n.d. |
| `sp5G` | Paralogue FT-like SP5G / FTL1 | Cultivé, S. l. cerasiforme | RÉCESSIF | n.d. |
| `uf` | UF, gène PEBP sœur de SFT | Cultivé | RÉCESSIF | n.d. |
| `s` | WOX homéoboîte (Solyc02g077390) | Cultivé (mutant) | RÉCESSIF | 2 |
| `an` | Protéine F-box | Cultivé (mutant) | RÉCESSIF | n.d. |
| `fa` | FA, orthologue de LEAFY | Cultivé (mutant) | RÉCESSIF | n.d. |
| `j` | MADS-box J | Cultivé | RÉCESSIF | 11 |
| `j-2` | SlMBP21 (Solyc12g038510) ; codon stop prématuré (LA0166) ; allèle transposon j2^TE en industriel | S. cheesmaniae LA0166 | RÉCESSIF | 12 |
| `mc` | MADS-box | Cultivé (mutant) | RÉCESSIF | n.d. |
| `to` | Clonage non confirmé | Cultivé (mutant) | RÉCESSIF | n.d. |
| `bif` | MAPK défectueuse | Cultivé (mutant) | RÉCESSIF | n.d. |
| `Nr` | SlETR3 = récepteur d'éthylène (ETR3/SR) | Cultivé (mutant) | DOMINANT | n.d. |
| `ls` | GRAS (orthologue LAS) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `bl` | R2R3-MYB (homologue BL) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `slbrc1 / slbrc2` | TCP TB1/CYC | Cultivé (mutant) | RÉCESSIF | n.d. |
| `d (dx, d-im)` | D = CYP85A1, C-6 oxydase de la voie des brassinostéroïdes | Cultivé (mutant) | RÉCESSIF | 2 |
| `br` | Locus cartographié, marqueurs MAS disponibles (non cloné) | Cultivé (mutant, tomate fraîche Floride) | RÉCESSIF | 1 |
| `mnt` | Non cloné | Cultivé (Micro-Tom) | RÉCESSIF | n.d. |
| `dpy` | Biosynthèse des brassinostéroïdes (BR) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `cu-3` | SlBRI1 / CURL-3, récepteur des BR (LRR-RLK), Solyc04g051510 | Cultivé (mutant) | RÉCESSIF | 4 |
| `dgt` | Cyclophiline (signalisation auxine) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `pro` | PRO / LeGAI = protéine DELLA (domaine VHVID→VHEID) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `gib-1` | CPS (copalyl-diphosphate synthase) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `gib-2` | Étape ent-7α-hydroxykaurenoic → GA12 | Cultivé (mutant) | RÉCESSIF | n.d. |
| `gib-3` | KS (ent-kaurène synthase) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `epi` | Surproduction d'éthylène | Cultivé (mutant) | RÉCESSIF | n.d. |
| `not / fl / sit` | Biosynthèse de l'ABA (NCED et autres) | Cultivé (mutants) | RÉCESSIF | n.d. |
| `erl` | Perte de fonction d'un gène SlTAC1-like (chr 10) | Cultivé (mutant) | SEMI-DOMINANT | 10 |

</details>

## 2. Feuillage — morphologie foliaire

*Regular / potato / carrot leaf : les quatre étages du contrôle (fenêtre, indétermination, frontières, extension).* — **15 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `c (c-2, clt, bli2)` | Cutleaf / Potato leaf | 6 | 🔵 RÉCESSIF | Feuille simple : limbe continu non divisé, bords lisses, vert plus foncé | C_ = « regular leaf » (dominant). F1 d'un croisement Potato leaf × regular = regular ; ressort chez 25 % des F2. |
| `e` | Entire | n.d. | 🔵 RÉCESSIF | Folioles à marges entières, feuille moins découpée + croissance laminaire ectopique | Malgré son nom, RÉCESSIF (perte de fonction). SlIAA9 = même gène que la parthénocarpie. |
| `La (La-2)` | Lanceolate | n.d. | 🟡 SEMI-DOMINANT | Feuilles simples, petites, lancéolées, maturité précoce | SEMI-DOMINANT MAJEUR. La/+ = feuille simple ; La/La = LÉTAL embryonnaire. Épistasique sur toutes les autres mutations de forme foliaire. |
| `gob (Gob-4d)` | Goblet | 7 | 🔵 RÉCESSIF | Moins de folioles secondaires, marges lisses ; l'allèle Gob-4d (semi-dominant) donne au contraire des lobes très profonds | C'est le « ciseau » qui découpe les frontières entre folioles, à l'intérieur de la fenêtre ouverte par LA/TCP4. |
| `tf` | Trifoliate | 5 | 🔵 RÉCESSIF | 3 folioles seulement, moins de bourgeons axillaires | Épistasique sur clau, bip et Me/+ : l'effet trifolié est conservé, seule la découpure de chaque foliole varie. |
| `lyr` | Lyrate | 5 | 🔵 RÉCESSIF | Réduction de la croissance laminaire et de l'initiation des folioles, anomalies florales | Feuilles simplifiées + anomalies florales : effet pléiotrope fort, sans usage en sélection maraîchère. |
| `wi, wi3, wi4, wi6 (+wl)` | Wiry (« feuilles lacet ») | n.d. | 🔵 RÉCESSIF | Feuilles filiformes sans limbe (shoestring), perte de dorsiventralité, floraison précoce | — |
| `Me` | Mouse ear | n.d. | 🟢 DOMINANT | Feuilles très découpées, plus de folioles et de denticulations, méristèmes hyperactifs, inflorescences anormales | Étroitement lié, voire identique, à Cu (jamais séparés par recombinaison). |
| `Cu` | Curl | n.d. | 🟢 DOMINANT | Feuillage en pompon, tiges « bâton », quasi-absence de gourmands, fruits plus verts (chloroplastes ++) | ⚠ Ne pas confondre avec cu-3 (récepteur BR) ni avec le virus « leaf curl » (TYLCV, gènes Ty). |
| `Pts` | Peteroselinum | n.d. | 🟡 SEMI-DOMINANT | Hyper-complexité foliaire (type persil), folioles primaires et secondaires surnuméraires | Décrit tantôt dominant, tantôt semi-dominant selon la source. |
| `bip` | Bipinnata | 2 | 🔵 RÉCESSIF | Feuilles bipinnées très subdivisées, folioles étroites (« feuille de carotte ») | Regular leaf ≻ carrot leaf ≻ potato leaf dans les croisements amateur (F2 ≈ 56/19/19/6). |
| `clau` | Clausa | n.d. | 🔵 RÉCESSIF | Feuilles extrêmement composées (jusqu'à ~11× le sauvage), morphogenèse continue, méristèmes ectopiques | Complexité foliaire extrême avec méristèmes ectopiques : stérilité et floraltérations → à éviter en croisement de retour. |
| `rg` | Rugose | n.d. | 🟢 DOMINANT | Feuillage gaufré/crispé, vert foncé (feuillage « nain ») | Combiné à Cu : donnerait un « pompon gaufré » (extrapolation non publiée). |
| `cu / cu-2` | Curled | n.d. | 🔵 RÉCESSIF | Feuilles recourbées/ondulées (série curl) | Recourbure du limbe sans nanisme : à distinguer de `cu-3` (nain, insensible au BR) et du curl du TYLCV. |
| `clf-2` | Curly leaf-2 | n.d. | 🔵 RÉCESSIF | Feuilles recourbées, floraison altérée | Recourbure + floraison altérée (Polycomb) : outil épigénétique, pas un caractère de sélection. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (15 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `c (c-2, clt, bli2)` | C = BLI2, facteur R2R3-MYB (classe BL) ; allèles c, clt (coalita), bli2 | Cultivé (heirloom, ~5 % des anciennes variétés) | RÉCESSIF | 6 |
| `e` | E = SlIAA9, protéine Aux/IAA (inhibiteur de la signalisation auxine) ; délétion d'1 base | Cultivé (mutant) | RÉCESSIF | n.d. |
| `La (La-2)` | LA / TCP4, mutation du site de liaison de miR319 = gain de fonction | Cultivé (mutant) | SEMI-DOMINANT | n.d. |
| `gob (Gob-4d)` | GOB = NAC/CUC2 (orthologue CUC2), Solyc07g062840, site ciblé par miR164 | Cultivé (mutant) | RÉCESSIF | 7 |
| `tf` | TF, facteur R2R3-MYB | Cultivé (mutant) | RÉCESSIF | 5 |
| `lyr` | LYR, orthologue de JAGGED (Solyc05g009380) | Cultivé (mutant) | RÉCESSIF | 5 |
| `wi, wi3, wi4, wi6 (+wl)` | Voie des ta-siARN : RDR6, SGS3, AGO7, DCL4 (dérégulation d'ARF3/ARF4) | Cultivé (4 groupes de complémentation) | RÉCESSIF | n.d. |
| `Me` | Expression anormale de TKN2/LeT6 (KNOX-I) ; ARN de fusion PFP–TKN2 | Cultivé (mutant dominant) | DOMINANT | n.d. |
| `Cu` | Surexpression de TKN2 (KNOX-I), gain de fonction | Cultivé (mutant dominant, PI 330725 « Stick ») | DOMINANT | n.d. |
| `Pts` | Délétion d'1 pb dans le promoteur de PTS/TKD1, protéine KNOX atypique sans homéodomaine | S. galapagense (feuilles profondes) / cultivé | SEMI-DOMINANT | n.d. |
| `bip` | BIP = protéine BEL-like homeodomain (Solyc02g089940) → surexpression de Tkn1/TKN2 | Cultivé (mutant) | RÉCESSIF | 2 |
| `clau` | CLAU, facteur MYB ; atténue la signalisation cytokinine, réprime GOB/LeT6 | Cultivé (mutant) | RÉCESSIF | n.d. |
| `rg` | Non cloné | Cultivé (mutant dominant) | DOMINANT | n.d. |
| `cu / cu-2` | Non cloné | Cultivé (mutants) | RÉCESSIF | n.d. |
| `clf-2` | PcG (type CLF) | Cultivé (mutant) | RÉCESSIF | n.d. |

</details>

## 3. Trichomes & pubescence

*Poils glandulaires = défense, arôme et colle à aleurodes. Module WO + H.* — **6 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `wo` | Woolly | n.d. | 🔵 RÉCESSIF | Poils denses sur tiges et feuilles (trichomes type I), ramifications affectées | Le couple WO + H (HD-ZIP IV × C2H2) est le module central du développement des poils. |
| `h` | Hair | n.d. | 🔵 RÉCESSIF | Trichomes clairsemés / anormaux | Poils anormaux : réduit la colle à insectes ; sensible aux aleurodes — à surveiller si vous croisez avec un trichome-dense. |
| `hl` | Hairless | n.d. | 🔵 RÉCESSIF | Trichomes déformés, tiges « chauves » | Tiges « chauves » : même conséquence défensive que `h` ; feuille luisante, sensible à la sunscald. |
| `hl-2` | Hairless-2 | n.d. | 🔵 RÉCESSIF | Déformation sévère de tous les types de trichomes | Déformation de tous les types de trichomes (NAP1, cytosquelette) : port chétif, non exploitable en variétal. |
| `sh` | Sparse hair | n.d. | 🔵 RÉCESSIF | Poils rares | Poils rares : même lecture que `h`/`hl` — la pubescence n'est pas qu'esthétique, c'est la première barrière anti-ravageurs. |
| `glandless` | Glandless | 9 | 🔵 RÉCESSIF | Trichomes glandulaires de type VI sans glande : perte des terpènes | À l'inverse, les trichomes type I/IV produisent les acylsucres de défense. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (6 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `wo` | Wo, facteur HD-ZIP IV (maître régulateur des trichomes I, III, V, VI, VII) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `h` | H, zinc finger C2H2 (partenaire de WO) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `hl` | Complexe WAVE / actine | Cultivé (mutant) | RÉCESSIF | n.d. |
| `hl-2` | Hl-2 = NAP1 (sous-unité SCAR/WAVE) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `sh` | Zinc finger C2H2 (partenaire de WO) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `glandless` | SlHDZ38 (HD-ZIP IV, sous-famille I) | Cultivé (mutant) | RÉCESSIF | 9 |

</details>

## 4. Feuillage — couleur & pigmentation

*High pigment, chlorophylle et anthocyanes végétatives.* — **12 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `au` | Aurea | n.d. | 🔵 RÉCESSIF | Jeunes plants jaune-vert (déficit de chromophore du phytochrome) | Aurea jaune-vert : à ne pas confondre avec une carence en azote ; le déficit porte sur le chromophore du phytochrome. |
| `v` | Virescent | n.d. | 🔵 RÉCESSIF | Jeunes feuilles blanchâtres → verdissement progressif | Virescent : verdissement différé, piège classique au semis sous lumière faible (diagnostic de lampe, pas de fertilisation). |
| `yv` | Yellow virescent | n.d. | 🔵 RÉCESSIF | Comme v, plus marqué | Yellow virescent : identique à `v` mais plus marqué, s'aggrave à basse température — ne fertilisez pas, génotypez. |
| `xan` | Xantha | n.d. | 🔵 RÉCESSIF | Feuilles jaunes (chlorophylle réduite) | Xantha : chlorophylle réduite du début à la fin (contrairement à `v` qui verdit) ; plante fragile, sans intérêt commercial. |
| `ch` | Chloronerva | n.d. | 🔵 RÉCESSIF | Chlorose interveinale (aspect carence en fer) | Chloronerva : chlorose interveinale qui MIME une carence en fer, mais le fer du sol est suffisant — c'est le transport qui est cassé. |
| `gh` | Ghost | n.d. | 🔵 RÉCESSIF | Feuillage pâle, plastes altérés | Ghost : plastes altérés, feuillage pâle ; à distinguer d'une viroses (mosaïque) par l'absence de déformation du limbe. |
| `hp-1 (hp-1W)` | High pigment-1 | n.d. | 🔵 RÉCESSIF | Feuillage vert très sombre (chlorophylle ++, feuilles plus épaisses), réponse lumineuse exagérée, vitamine C et anthocyanes ↑ | ⚠ Les « high pigment » hp-1 / hp-2 sont RÉCESSIFS — Ip, lui, est dominant. |
| `hp-2 (hp-2J, hp-2DG = dg)` | High pigment-2 / Dark green | n.d. | 🔵 RÉCESSIF | Fruit immature vert foncé, lycopène ×1,5–2, β-carotène ×3 | Vert sombre ++ mais port compact, feuilles épaisses, croissance ralentie (DET1) : le « beau feuillage » a un coût végétatif. |
| `Ip` | Intense pigmentation | n.d. | 🟢 DOMINANT | Pigmentation intense, réponse lumineuse exagérée ; fruit immature vert foncé, +34–38 % de solides solubles, +62 % de caroténoïdes | L'un des RARES « high pigment » DOMINANTS, et sans les défauts des hp. Fruit souvent plus petit (pléiotropie). |
| `atv` | Atroviolacea | 7 | 🔵 RÉCESSIF | Anthocyanes accrues (teintes violacées), surtout végétatives | Seul : effet modéré. Combiné à Aft ou Abg : synergie → peau violette intense (Indigo Rose, Sun Black). |
| `Aft` | Anthocyanin fruit | 10 | 🟢 DOMINANT | Épicarpe violet tacheté (dépendant de la lumière), tiges et feuilles violacées | Monogénique dominant : s'exprime dès la F1 (mais intensité lumineuse requise). |
| `abg` | Aubergine | 10 | 🔵 RÉCESSIF | Pigmentation anthocyanique de distribution cellulaire différente de Aft | Historiquement décrit récessif ; allélique ou très proche de Aft. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (12 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `au` | Biosynthèse du phytochromobiline | Cultivé (mutant) | RÉCESSIF | n.d. |
| `v` | Non cloné | Cultivé (mutant) | RÉCESSIF | n.d. |
| `yv` | Non cloné | Cultivé (mutant) | RÉCESSIF | n.d. |
| `xan` | Non cloné | Cultivé (mutant) | RÉCESSIF | n.d. |
| `ch` | Absorption / transport du fer | Cultivé (mutant) | RÉCESSIF | n.d. |
| `gh` | Non cloné | Cultivé (mutant) | RÉCESSIF | n.d. |
| `hp-1 (hp-1W)` | HP-1 = SlDDB1 (perte de fonction) | Cultivé (mutant spontané, 1917) | RÉCESSIF | n.d. |
| `hp-2 (hp-2J, hp-2DG = dg)` | HP-2 = SlDET1 (perte de fonction) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `Ip` | Non cloné (amplification du signal phytochrome) | Cultivé (mutant) | DOMINANT | n.d. |
| `atv` | SlMYB-ATV, R3-MYB répresseur (Solyc07g052490) ; insertion de 4 pb | S. cheesmaniae / S. galapagense | RÉCESSIF | 7 |
| `Aft` | AN2-like / SlAN2, R2R3-MYB fonctionnel | S. chilense (introgressé) ; nouveaux allèles chez S. galapagense LA1141 | DOMINANT | 10 |
| `abg` | Allèle Abg de AN2-like + MYB113, de S. lycopersicoides | S. lycopersicoides | RÉCESSIF | 10 |

</details>

## 5. Fleur, autogamie & nouaison

*Le verrou d'autogamie (Style2.1) et la stérilité positionnelle.* — **5 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `Style2.1 (se2.1)` | Exserted / inserted style | 2 | 🔵 RÉCESSIF | Pistil INSÉRÉ dans le cône d'anthères → autogamie stricte. L'allèle sauvage (style exserté de ~3 mm) favorise l'allogamie et les hybridations | VERROU D'AUTOGAMIE : indispensable pour fixer une variété pure. Attention : un style exserté (sauvage, ou induit par le froid/canicule) ouvre la porte aux pollens voisins → isoler les fleurs. |
| `SE3.1` | Stigma insertion 3.1 | n.d. | 🔵 RÉCESSIF | Deuxième étape du décalage du stigmate : de « flush » à « inséré » ; module avec Style2.1 | Style2.1 gère l'étape 1, SE3.1 l'étape 2 : les deux cumulés = autogamie parfaite. |
| `SlSE2.2` | Stigma exsertion 2.2 | 2 | 🔵 RÉCESSIF | Degré d'exsertion du stigmate : le KO allonge anthères et style (stérilité positionnelle, sans émasculer) | Outil pour la production d'hybrides : stérilité positionnelle = pas d'émasculation manuelle. module IAA/ETH/JA/ABA. |
| `SlLst` | Long styles | 12 | ⚪ MIXTE / SELON FOND | Allongement du style et exsertion du stigmate SOUS CHALEUR (> 27 °C) : perte d'autogamie à la canicule | ⚠ Explique les fruits « mal fécondés » et l'allogamie accrue en été : la pureté variétale dépend aussi du climat. |
| `pat / pat-2` | Parthenocarpic | n.d. | 🔵 RÉCESSIF | Nouaison sans pollinisation → fruits sans pépins (souvent plus petits, moins de loges) | Récessif : à fixer. SlIAA9 (e) et les mutants de gibbérellines donnent des effets comparables. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (5 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `Style2.1 (se2.1)` | Style2.1 (Solyc02g087860), polypeptide à motif HLH contrôlant l'expansion cellulaire du style ; chez le cultivé = délétions StyleD1 (450 pb) + StyleD2 (750 pb) dans le promoteur | Ancêtre sauvage → fixé à la domestication | RÉCESSIF | 2 |
| `SE3.1` | Locus du chr 3, facteurs de transcription (SlbHLH005, AGL6, AGL15/SlMBP11 dans l'intervalle) | Cultivé moderne | RÉCESSIF | n.d. |
| `SlSE2.2` | SlSE2.2 (Solyc02g087270), protéine F-box ; délétion de 11 pb dans l'exon 1 | Cultivé (accession J59, 2025) | RÉCESSIF | 2 |
| `SlLst` | Récepteur d'éthylène de type EIN4 (Solyc12g027610) | Cultivé | MIXTE / SELON FOND | 12 |
| `pat / pat-2` | Locus classique, voie GA/auxine (non cloné pour pat-2) | Cultivé (mutant) | RÉCESSIF | n.d. |

</details>

## 6. Fruit — forme, loges & poids

*Deux axes indépendants (longueur × loges) plus les trois loci clonés du poids.* — **16 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `SUN (sun)` | Sun / fruit elongation | 7 (copie dupliquée ; gène d'origine IQD12 sur chr 10) | 🟡 SEMI-DOMINANT | Fruit très allongé, fuselé, en pointe (type Cornue des Andes). Redistribue la masse : plus de divisions longitudinales, moins de transversales, APRÈS fécondation | DOMINANCE DE DOSAGE : F1 intermédiaire (d/a ≈ −0,39, l'allèle rond est partiellement dominant). Présent chez 88 % des tomates longues et 83 % des cœurs de bœuf. Épistasie : SUN ≻ LC pour la longueur. |
| `OVATE (o)` | Ovate | 2 | 🔵 → 🟡 RÉCESSIF → SEMI-DOMINANT | Fruit ovale, en poire ou piriforme (Yellow Pear, Mountain Vineyard) | RÉCESSIF chez S. pimpinellifolium (rond dominant) mais ADDITIF dans l'IL2-5 de S. pennellii : la dominance dépend du fond. ovate seul ne suffit pas toujours (modificateurs). |
| `SOV1 / SlOFP20` | Square ovate | 2 | 🔵 RÉCESSIF | Nécessaire avec ovate pour l'obovoïde franc ; délétion régulatrice → sous-expression | Effet ADDITIF avec ovate ; une mutation de SlTRM5 restaure la forme ronde chez le double ovate/sov1. |
| `FS8.1` | Fruit shape 8.1 | 8 | ⚪ MIXTE / SELON FOND | Fruit carré / rectangulaire / « blocky » de la Roma de conserve, résistant à l'écrasement ; jusqu'à 27,4 % de la variance de l'indice de forme | PERTE DE FONCTION mais DOMINANCE PARTIELLE : d/a = −0,47 pour la forme (rond partiellement dominant), d/a = +1,14 pour le poids (sur-dominant). |
| `PT (POINTED TIP)` | Pointed tip | n.d. | 🔵 RÉCESSIF (LOF) | Fruit à pointe / téton distal net. L'allèle sauvage PT^H réprime FUL2 et SUPPRIME la pointe | Le caractère « pointe » est donc récessif ; bk (beaked, chr 2) et n (nipple, chr 5) sont des loci classiques indépendants. |
| `LC (locule number)` | Locule number | 2 | 🟣 QTL / ADDITIF | Passe de 2 loges (sauvage) à 3–4 loges : fruit plus gros et plus aplati | Essentiellement ADDITIF (d/a ≈ 0) mais décrit partiellement récessif selon les fonds. En fond LA1589, lc seul a PEU D'EFFET sans fas. |
| `FAS (fasciated)` | Fasciated | 11 | 🔵 RÉCESSIF | 6–10+ loges : fruits côtelés, aplatis, géants (Beefsteak, Cœur de bœuf) ; jusqu'à +37 % de poids | QUASI COMPLÈTEMENT RÉCESSIF : d/a = −0,88 pour le nombre de loges. ⚠ FAS n'est PAS SlYABBY2b (hypothèse de 2008 abandonnée). |
| `ENO (SlENO)` | Excessive number of floral organs | 3 | 🔵 RÉCESSIF | Plus de loges, fruits plus gros ; synergie avec lc et fas | Les fruits modernes à ≥ 8 loges cumulent lc + fas + eno. |
| `globe` | Globe | 12 | 🔵 RÉCESSIF | Distingue fruit APLATI (allèle mutant) de fruit GLOBE (rond) ; additif pour le poids | Ségrégation 3:1 « flat » : globe → l'allèle « flat » domine pour la forme, mais reste additif sur le poids. |
| `SlIQD21 / SlMAP70` | Élongation polaire | n.d. | ⚪ MIXTE / SELON FOND | Coordonne l'élongation polaire du fruit (interaction calmoduline / microtubules) | Nouveau maillon de l'axe proximo-distal, à exploiter en édition. |
| `tri2.1 / dblk2.1` | Distal blooming | 2 | 🟣 QTL / ADDITIF | QTL de l'extrémité distale (bec / pointe) | Utile en complément de PT et bk. |
| `ld6 / ld8 / ld11` | Lobulation | 6 / 8 / 11 | 🟣 QTL / ADDITIF | Degré de lobulation (bosses du fruit) | Trois loci indépendants : les bosses ne suivent pas fas/lc. |
| `FAB / CLV1, FIN, SlTPL3, SlKNUCKLES` | Modulateurs CLV–WUS | 4 / 11 / n.d. | 🟣 QTL / ADDITIF | Loges et taille du fruit (fond génétique de la voie CLV3–WUS) | Expliquent une partie du « bruit » autour de fas et lc. |
| `fw2.2` | Fruit weight 2.2 | 2 | 🟡 SEMI-DOMINANT | Masse du fruit : l'allèle CULTIVÉ (gros) augmente le poids de 30 à 50 % ; ~30 % de la différence sauvage/cultivé | L'ALLÈLE SAUVAGE « petit fruit » est SEMI-DOMINANT → le gros fruit est partiellement récessif. Piège classique du croisement avec une sauvage à fruits minuscules. |
| `fw3.2 / SlKLUH` | Fruit weight 3.2 | 3 | 🟣 QTL / ADDITIF | Poids du fruit (prolonge la durée de division cellulaire), ~19 % de la variance ; retarde aussi la maturation et augmente la ramification | Action ADDITIVE à additivo-dominante. Pléiotropie à surveiller (maturation). |
| `fw11.3 / CSR` | Fruit weight 11.3 | 11 | 🟢 DOMINANT (partiel) | Taille des CELLULES du mésocarpe ; ~8 % de la variance mais le plus fort effet sur le gradient de domestication | L'un des RARES loci de poids dominants. ⚠ fw11.3 est un locus DISTINCT de fas, situé 45 kb en aval — à ne pas confondre. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (16 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `SUN (sun)` | Duplication de 24,7 kb médiée par le rétrotransposon Rider → IQD12 (Solyc10g079240) surexprimé = gain de fonction ; BZR1.7 (voie BR) active sa transcription | Cultivé (allèle domestiqué) | SEMI-DOMINANT | 7 (copie dupliquée ; gène d'origine IQD12 sur chr 10) |
| `OVATE (o)` | Codon stop prématuré (SNP G→T) = allèle nul de la famille OFP ; l'OVATE fonctionnel est un RÉGULATEUR NÉGATIF de l'élongation | Cultivé + S. pimpinellifolium | RÉCESSIF → SEMI-DOMINANT | 2 |
| `SOV1 / SlOFP20` | SlOFP20, module OFP × TRM (TONNEAU1 Recruiting Motif) | Cultivé | RÉCESSIF | 2 |
| `FS8.1` | SNP A857T → arrêt prématuré = perte de fonction du facteur Trihelix GT-2 non canonique ; le gène fonctionnel active SlKRP2 (inhibiteur du cycle cellulaire) | Cultivé (tomate industrielle) | MIXTE / SELON FOND | 8 |
| `PT (POINTED TIP)` | SNP His→Arg : 2 domaines C2H2 au lieu de 3 (perte de fonction partielle) | Cultivé (2022) | RÉCESSIF (LOF) | n.d. |
| `LC (locule number)` | SlWUS (Solyc02g083950), orthologue WUSCHEL ; 2 SNP dans une boîte CArG = GAIN de fonction (élargissement du domaine d'expression) | Cultivé + S. pimpinellifolium | QTL / ADDITIF | 2 |
| `FAS (fasciated)` | SlCLV3 (Solyc11g071380) : inversion de ~294 kb dont un point de cassure à 1 kb en amont = perte de fonction partielle du promoteur | Cultivé | RÉCESSIF | 11 |
| `ENO (SlENO)` | Facteur AP2/ERF (Solyc03g117230) ; indel de 85 pb dans le promoteur → sous-expression (le gène réprime normalement SlWUS) | Cultivé | RÉCESSIF | 3 |
| `globe` | Solyc12g006860 = brassinostéroïde hydroxylase (P450) ; insertion d'1 pb = knock-out | Cultivé (apparu très tard dans la domestication) | RÉCESSIF | 12 |
| `SlIQD21 / SlMAP70` | SlIQD21 – SlMAP70 (2023) | Cultivé | MIXTE / SELON FOND | n.d. |
| `tri2.1 / dblk2.1` | Non cloné | Cultivé | QTL / ADDITIF | 2 |
| `ld6 / ld8 / ld11` | QTL non clonés, indépendants de FAS et LC | Cultivé + sauvage | QTL / ADDITIF | 6 / 8 / 11 |
| `FAB / CLV1, FIN, SlTPL3, SlKNUCKLES` | CLV1 (Solyc04g081590) ; FIN = arabinosyltransférase (Solyc11g064850) ; corépresseur TPL3 ; KNUCKLES | Cultivé | QTL / ADDITIF | 4 / 11 / n.d. |
| `fw2.2` | CNR = Cell Number Regulator, régulateur NÉGATIF de la division cellulaire du péricarpe ; changement d'expression (élément régulateur) | Allèle gros fruit : S. lycopersicum ; petit fruit : S. pimpinellifolium | SEMI-DOMINANT | 2 |
| `fw3.2 / SlKLUH` | SlKLUH = P450 CYP78A ; SNP dans le PROMOTEUR (expression accrue) ; les deux allèles sont fonctionnels | S. pennellii (IL3-2) | QTL / ADDITIF | 3 |
| `fw11.3 / CSR` | CSR = Cell Size Regulator (Solyc11g071940) ; délétion de 1,4 kb → troncation de 194 aa = gain de fonction (validé en complémentation transgénique) | S. pennellii (IL11-3) / cultivé | DOMINANT (partiel) | 11 |

</details>

## 7. Fruit — couleur (peau × chair)

*Modèle bi-couche : caroténoïdes de la chair, flavonoïdes de la peau, chlorophylle.* — **12 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `Y (SlMYB12)` | Yellow skin / flavonols | 1 | 🟢 DOMINANT | Peau JAUNE : accumulation de chalcone de naringénine dans la cuticule. y/y = peau INCOLORE (transparente « comme du verre ») | ⚠ ERRATUM : Y est sur le chr 1 (pas le chr 6 comme indiqué dans certaines fiches). C'est LE lien couleur ↔ nutrition : le fruit rose y/y est aussi privé de flavonols (rutine). Surexpression de SlMYB12 : rutine ×11 à ×19. |
| `r (PSY1)` | Yellow flesh | 3 | 🔵 RÉCESSIF | Chair JAUNE (caroténoïdes quasi nuls), floraison et pigmentation plus précoces | Effet de dosage : UN SEUL allèle fonctionnel suffit → le rouge est dominant. Ségrégation 3:1. |
| `t (tangerine / CRTISO)` | Tangerine | 10 | 🔵 RÉCESSIF | ORANGE lumineux par accumulation de PROLYCOPÈNE (cis-lycopène), biodisponible à cru ; ⚠ pas de β-carotène | ÉPISTATIQUE sur l'allèle r^2997 de PSY1 (les cis-caroténoïdes restaurent partiellement la transcription de PSY1) ; mais d'autres allèles de r (r^3756) sont épistatiques sur t. |
| `B (CYC-B, Beta)` | High-beta | 6 | 🟢 DOMINANT | ORANGE dense : le lycopène est converti en β-CAROTÈNE (> 80 % des caroténoïdes) = PROVITAMINE A | Gène dominant classique. VOS S. cheesmaniae et galapagense le portent TOUS → votre F1 avec une rouge sera ORANGE. |
| `og / og-c (old gold crimson)` | Old gold | 6 | 🔵 RÉCESSIF | ROUGE CRAMOISI intense (lycopène suraccumulé, 0 β-carotène), fleurs orange chamois | ⚠ B et og sont ALLÉLIQUES : on ne peut pas cumuler l'allèle nul et l'allèle surexprimé au même locus. |
| `Del (LCY-e)` | Delta | n.d. | 🟢 DOMINANT | ORANGE par accumulation de δ-carotène au détriment du lycopène | Dominant : s'exprime dès la F1. |
| `hp-3 (ZEP)` | High pigment-3 | n.d. | 🔵 RÉCESSIF | Rouge intense, plastes plus nombreux, lycopène ↑ | Rouge intense via déficience en ABA : ⚠ feuilles qui flétrissent et graines dormantes, comme chez `not`/`fl`/`sit`. |
| `u (uniform ripening)` | Uniform ripening | 10 | 🔵 RÉCESSIF | Fruit immature VERT CLAIR UNIFORME (suppression de l'épaule verte) — allèle fixé dans presque toutes les variétés modernes | ⚠ COÛT NUTRITIONNEL : −10 à −20 % de sucres et de caroténoïdes. Le « joli » fruit uniforme est génétiquement moins savoureux. |
| `ug (uniform gray-green)` | Uniform gray-green | n.d. | 🔵 RÉCESSIF | Absence d'épaule verte : phénocopie de u, par un autre gène | Utile pour distinguer deux origines d'un même look. |
| `gf (green flesh)` | Green-flesh | 8 | 🔵 RÉCESSIF | RÉTENTION de la chlorophylle à maturité → chair brun-verte (Noire de Crimée, Green Zebra) | Récessif (homozygotie requise). gf + r/r = chair VERT franc ; gf + Y = brun/noir, gf + y = pourpre-brun (Cherokee Purple). |
| `gs (green stripe)` | Green stripe | n.d. | 🔵 RÉCESSIF | Rayures vertes sur fruit immature (visibles à maturité si gf) | Récessif ; les rayures ne restent visibles à maturité QUE si `gf/gf` est présent — sinon elles disparaissent au rougissement. |
| `Gr / Nr-2` | Green-ripe | 1 | 🟢 DOMINANT | Le fruit NE MÛRIT PAS : reste vert avec un cœur rouge/orangé | Dominant : bloque la dégradation de la chlorophylle et la maturation. Gr et Nr-2 sont alléliques. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (12 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `Y (SlMYB12)` | SlMYB12, R2R3-MYB qui active toute la voie des flavonols (PAL, CHS, FLS) ; y = expression abolie (promoteur) ou protéine tronquée (allèle nul Δy) | Cultivé (Y) / rose (y) | DOMINANT | 1 |
| `r (PSY1)` | PSY1 = phytoène synthase 1 ; pertes de fonction multiples (transcrits aberrants, insertions) | Cultivé (allèle récessif r) | RÉCESSIF | 3 |
| `t (tangerine / CRTISO)` | CRTISO = caroténoïde isomérase (perte de fonction) | Cultivé (mutant) | RÉCESSIF | 10 |
| `B (CYC-B, Beta)` | CYC-B = lycopène β-cyclase plastidiale, SUREXPRIMÉE par variation du promoteur (haplotypes sauvages) = gain de fonction | S. cheesmaniae, S. galapagense, S. habrochaites LA0316, S. pennellii | DOMINANT | 6 |
| `og / og-c (old gold crimson)` | Allèles NULS (frameshift / codon stop) du MÊME gène CYC-B | Cultivé (mutant) | RÉCESSIF | 6 |
| `Del (LCY-e)` | Lycopène ε-cyclase (CrtL-e) à expression/activité accrue | S. pennellii / S. l. var. cerasiforme | DOMINANT | n.d. |
| `hp-3 (ZEP)` | Zeaxanthine époxydase (nul → déficience en ABA) | Cultivé (mutant) | RÉCESSIF | n.d. |
| `u (uniform ripening)` | SlGLK2 = GOLDEN2-LIKE (Solyc10g008160) ; mutation non-sens par insertion d'1 pb | S. cheesmaniae LA0428 / S. galapagense LA1141 / sélection interne | RÉCESSIF | 10 |
| `ug (uniform gray-green)` | TKN4 (KNOX de classe I), perte de fonction | Cultivé (mutant) | RÉCESSIF | n.d. |
| `gf (green flesh)` | SGR1 = STAY-GREEN (Solyc08g080090) ; substitution Arg143→Ser + ≥5 allèles nuls indépendants | Cultivé (mutant) | RÉCESSIF | 8 |
| `gs (green stripe)` | Non cloné | Cultivé (Green Zebra…) | RÉCESSIF | n.d. |
| `Gr / Nr-2` | GR, homologue de RTE1 (gain de fonction) ; délétion de 334 pb en 5′ → expression ectopique | Cultivé (mutant dominant) | DOMINANT | 1 |

</details>

> 🎨 Voir aussi [Prédire la couleur du fruit](#prédire-la-couleur-du-fruit) pour les combinaisons peau × chair, et n'oubliez pas que `B` et `og` sont **alléliques** (même gène `CYC-B`) : on ne les cumule pas.

## 8. Fruit — maturation & conservation

*rin, nor, alc, Cnr, Nr : le compromis conservation / arôme.* — **5 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `rin (ripening-inhibitor)` | Ripening inhibitor | 5 | 🔵 RÉCESSIF | Blocage de la maturation : fruit vert/pâle, jamais rouge, pas d'éthylène | Utilisé EN HÉTÉROZYGOZITÉ (rin/+) pour la longue conservation. ⚠ rin/nor détruisent aussi l'arôme (ils régulent TomLoxC, ADH2, HPL…). |
| `nor (non-ripening)` | Non-ripening | 10 | 🔵 RÉCESSIF | Maturation retardée, faible éthylène, longue conservation | Les hétérozygotes nor/+ sont la base industrielle du shelf-life. |
| `alc (alcobaca)` | Alcobaca | 10 | 🔵 RÉCESSIF | Même phénotype que nor mais PLUS FAIBLE : maturation lente, conservation longue (tomates « de colgar » / Penjar) | ⚠ alc n'est PAS un gène séparé : c'est un allèle de NOR. Idem nor/alc = hétérozygotes largement utilisés. |
| `Cnr (Colorless non-ripening)` | Colorless non-ripening | 4 | 🟢 + ⚫ DOMINANT + ÉPIGÉNÉTIQUE | Fruit incolore, péricarpe farineux, perte d'adhérence cellulaire | DOMINANT (contrairement à rin/nor) et ÉPISTATIQUE sur rin et nor. Incomplètement dominant à récessif pour la pigmentation et les volatils. ⚠ Les marqueurs ADN classiques peuvent échouer : c'est un épi-allèle. |
| `Nr` | Never ripe | n.d. | 🟢 DOMINANT | Maturation bloquée, sénescence et abscission retardées | Dominant négatif. À manier avec précaution en F1 : s'exprime dès la première génération. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (5 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `rin (ripening-inhibitor)` | SOLYC05G038930 MADS-RIN ; délétion → protéine de fusion, qui agit aussi en répresseur dominant négatif au niveau moléculaire | Cultivé (mutant) | RÉCESSIF | 5 |
| `nor (non-ripening)` | NAC-NOR (Solyc10g051480) ; délétion de 2 pb → protéine tronquée NOR186 | Cultivé (mutant) | RÉCESSIF | 10 |
| `alc (alcobaca)` | Allèle du MÊME gène NAC-NOR : substitution Val→Asp (V317D) | Cultivé | RÉCESSIF | 10 |
| `Cnr (Colorless non-ripening)` | SPL-CNR : ÉPIMUTATION = hyperméthylation du promoteur, AUCUN changement de séquence | Cultivé (mutant épigénétique) | DOMINANT + ÉPIGÉNÉTIQUE | 4 |
| `Nr` | SlETR3 (récepteur d'éthylène), mutation du domaine senseur = gain de fonction | Cultivé (mutant dominant) | DOMINANT | n.d. |

</details>

## 9. Saveur — sucres & solides solubles

*Brix : les gisements sauvages et le « frein à sucre » levé en 2024.* — **13 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `LIN5 (Brix9-2-5)` | Lin5 / invertase apoplasmique | 9 | 🟡 SEMI-DOMINANT | Double quasi le ratio fructose/glucose : attaque sucrée immédiate. +11 à +25 % de solides solubles SANS perte de rendement | PARTIELLEMENT DOMINANT : « the partially dominant nature of the S. pennellii allele » ; une seule copie de l'Asn366Asp suffit → utilisable dès la F1. Silençage : −30 % glucose, −17 à −26 % fructose. |
| `SlCDPK27 (SSC11.1)` | Frein à sucre | 11 | 🔵 RÉCESSIF | KO : +16 % de solubles ; double KO avec SlCDPK26 : +30 % de glucose+fructose, SANS pénalité de poids ni de rendement (graines plus petites) | PERTE DE FONCTION = RÉCESSIF, à fixer à l'homozygotie. ⚠ L'allèle a été PERDU à la domestication car lié au locus de poids fw11.3 (co-sélection gros fruit = peu sucré). Voie la plus rapide = CRISPR. |
| `SlCDPK26` | Paralogue de CDPK27 | n.d. | 🔵 RÉCESSIF | Effet uniquement en double KO avec SlCDPK27 (redondance) | Redondance fonctionnelle ⇒ il faut les DEUX pertes de fonction. |
| `SlSPS1 (qSSC7.1)` | Sucrose-phosphate synthase | 7 | 🟣 QTL / ADDITIF | Sucres en hausse SANS AUCUN effet sur le poids du fruit | Caractère quantitatif : l'allèle AG a décliné à la domestication, partiellement récupéré dans les programmes qualité. |
| `STP1 (qSSC2.1)` | Transporteur de monosaccharides | 2 | 🟣 QTL / ADDITIF | QTL de solubles solubles ; le KO fait baisser le Brix | ⚠ Ici le « bon » allèle est DÉJÀ dans le cultivé : pas besoin d'aller chercher le sauvage. |
| `SlSUS3` | Sucrose synthase | n.d. | 🟢 DOMINANT (transgène) | ↑ sucres sans effet sur le poids du fruit | Gain de fonction → effet de dosage, dominant à l'échelle du transgène. |
| `SlINVINH1 / SlVPE5` | Inhibiteur d'invertase / protéase | n.d. | 🔵 RÉCESSIF | ↑ solubles solubles, glucose et fructose | La perte de fonction des DEUX gènes est nécessaire pour l'effet maximal. |
| `SlVIF` | Inhibiteur d'invertase vacuolaire | n.d. | 🟣 QTL / ADDITIF | Régulation négative : modélise la force du « puits » à sucres | Surexpression ↓ hexoses, suppression ↑ hexoses. |
| `SlVI / Sucr` | Invertase vacuolaire | 3 | 🔵 RÉCESSIF | ↑ saccharose et solubles solubles | Le gène Sucr classique (chr 3). |
| `SlTST1 / SlTST2` | Transporteurs tonoplastiques | n.d. | 🔵 RÉCESSIF | Double mutant : −40 % glucose, −50 % fructose+saccharose, −40 % de Brix | Sens inverse : ce sont des gènes NÉCESSAIRES au sucre du fruit. |
| `SlSWEET7a / SlSWEET14` | Transporteurs d'efflux | n.d. | 🔵 RÉCESSIF | Silençage → ↑ sucres du fruit mûr | Perte de fonction souhaitable. |
| `SlbZIP1, SlNAP2, SlARF10, SlFgr, AGPase, SUT2, TIV1, RIN` | Régulateurs du Brix | divers | 🟣 QTL / ADDITIF | Chacun apporte 1 à 15 % de la variance ; RIN agit via SlVI/SlVIF | Dominance NON ÉTABLIE (régulateurs). L'ensemble des QTL connus couvre > 50 % de l'héritabilité du Brix ; un QTL majeur peut atteindre ~30 %. |
| `Segment « chm » (S. chmielewskii)` | Hauts solides historiques | n.d. | 🟢 DOMINANT (action génique dominante) | +13 % de Brix à l'homozygotie, +12 % à l'hétérozygote, +6 % avec une seule dose. Sans effet négatif cohérent sur rendement, poids ou pH | Le vieux gisement des années 1980–90 reste directement utilisable. ⚠ Ne pas confondre : les hauts solides de Rick (1974) viennent de chmielewskii, PAS de cheesmaniae. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (13 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `LIN5 (Brix9-2-5)` | Invertase de paroi (Solyc09g010080) ; QTN = SNP Asn366Asp près du site catalytique (activité enzymatique accrue, PAS de différence de transcription) | S. pennellii LA0716 → lignée IL9-2-5 (fond M82) | SEMI-DOMINANT | 9 |
| `SlCDPK27 (SSC11.1)` | Insertion de 12 pb dans le PROMOTEUR de l'allèle « haut sucre » → sous-expression (perte de fonction). Les kinases freinent la sucrose synthase SlSUS3 (phosphorylation → dégradation) | Prévalent chez S. pimpinellifolium et S. l. cerasiforme ; quasi absent des variétés modernes à gros fruit (97 % portent l'allèle bas-sucre) | RÉCESSIF | 11 |
| `SlCDPK26` | Paralogue de la même voie | Sauvages | RÉCESSIF | n.d. |
| `SlSPS1 (qSSC7.1)` | InDel de 1 pb (AG/A) à −2355 pb du promoteur ; l'allèle AG = plus d'expression | S. pimpinellifolium LA1924 (stable sur 3 ans et 3 environnements) | QTL / ADDITIF | 7 |
| `STP1 (qSSC2.1)` | InDel de 21 pb dans le PROMOTEUR, sélectionné pendant l'amélioration | Lignées cultivées élites | QTL / ADDITIF | 2 |
| `SlSUS3` | Surexpression (échappe à la dégradation par les CDPK) | Ingénierie | DOMINANT (transgène) | n.d. |
| `SlINVINH1 / SlVPE5` | KO simple ou double (CRISPR) | Ingénierie | RÉCESSIF | n.d. |
| `SlVIF` | — | Cultivé | QTL / ADDITIF | n.d. |
| `SlVI / Sucr` | KO | Cultivé | RÉCESSIF | 3 |
| `SlTST1 / SlTST2` | — | Cultivé | RÉCESSIF | n.d. |
| `SlSWEET7a / SlSWEET14` | — | Cultivé | RÉCESSIF | n.d. |
| `SlbZIP1, SlNAP2, SlARF10, SlFgr, AGPase, SUT2, TIV1, RIN` | Facteurs de transcription et enzymes ; édition de régions inhibitrices | Cultivé + sauvages | QTL / ADDITIF | divers |
| `Segment « chm » (S. chmielewskii)` | Plusieurs QTL (RFLP historique) | S. chmielewskii LA1028 (≈10 % SS contre ≈5 % chez VF36) ; lignées LA1563 (BC5S5) et VF145B-7879 | DOMINANT (action génique dominante) | n.d. |

</details>

## 10. Saveur — acidité, umami & GABA

*Malate, citrate, glutamate libre et le cas d'école SlGAD.* — **8 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `SlALMT9 (TFM6)` | Transporteur vacuolaire de malate | 6 | 🟡 SEMI-DOMINANT | Acidité malique vive et fraîche (pomme verte), équilibre le sucre. Malate + citrate = > 90 % des acides organiques | Mutation régulatrice : une seule copie semble suffire (modèle Ma1 du pommier). Marqueur très simple à génotyper (InDel 3 pb). |
| `SlWRKY42` | Répresseur d'ALMT9 | n.d. | ⚪ MIXTE / SELON FOND | ↓ malate par répression transcriptionnelle | Gain de fonction = acide réduit. À surveiller si vous cherchez de l'acidité. |
| `Loci du citrate (11 loci)` | Acidité titrable & pH | plusieurs | 🟣 QTL / ADDITIF | pH et acidité titrable : caractères très polygéniques, forte variabilité saisonnière | ⚠ LE CITRATE influence davantage la préférence du consommateur que le malate — et il n'a pas de gène majeur exploitable. |
| `GTF (glycosyltransférase groupe 1)` | Malate & citrate | 2 | 🟣 QTL / ADDITIF | Associé aux DEUX acides simultanément | Dominance non déterminée. |
| `SlGAD2 / SlGAD3` | GABA : la dominance la mieux documentée | 1 et 11 | 🟢 DOMINANT (partielle) | GABA multiplié par 7 à 15 (jusqu'à 125 mg/100 g frais) sans effet sur le rendement | LE GÈNE EST HAPLO-SUFFISANT : l'hétérozygote suffit → allèle directement exploitable en F1, en T0 et même en hémizygotie. Premier aliment CRISPR commercialisé au monde. |
| `SlGABA-T1` | Catabolisme du GABA | n.d. | 🔵 RÉCESSIF | GABA ×2,95 au stade rouge (73,8 mg/100 g) | Récessif. |
| `SlGABA-T1/2/3 + SlSSADH` | Multiplex GABA | n.d. | 🔵 RÉCESSIF | GABA ×19 MAIS nanisme sévère, malformations, quasi-stérilité | Pléiotropie forte ⇒ à ÉVITER en sélection classique. |
| `Pool de glutamate (umami)` | Umami | divers | 🟣 QTL / ADDITIF | Le L-glutamate est l'acide aminé libre dominant du fruit rouge ; aucun locus « umami » cloné à ce jour | HÉRITABILITÉ QUANTITATIVE, non mendélienne. Les 5'-ribonucléotides (IMP/GMP) sont quasi absents chez la tomate : l'umami explose dans les plats cuisinés, par synergie avec les nucléotides des autres ingrédients. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (8 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `SlALMT9 (TFM6)` | Solyc06g072910 ; InDel de 3 pb dans une BOÎTE W du promoteur (allèle « haut malate », sélectionné à la domestication) ; KO CRISPR → malate réduit | Cultivé (variation naturelle) | SEMI-DOMINANT | 6 |
| `SlWRKY42` | Facteur de transcription liant la 8e boîte W du promoteur de SlALMT9 | Cultivé | MIXTE / SELON FOND | n.d. |
| `Loci du citrate (11 loci)` | InDels et variants structuraux, QTL mineurs (GWAS 2023) | Cultivé + sauvages | QTL / ADDITIF | plusieurs |
| `GTF (glycosyltransférase groupe 1)` | Méta-GWAS | Cultivé | QTL / ADDITIF | 2 |
| `SlGAD2 / SlGAD3` | Troncation du domaine auto-inhibiteur C-terminal (CaMBD, liaison calmoduline) | Édition CRISPR (Sicilian Rouge High GABA, Japon 2021) | DOMINANT (partielle) | 1 et 11 |
| `SlGABA-T1` | KO CRISPR | Édition | RÉCESSIF | n.d. |
| `SlGABA-T1/2/3 + SlSSADH` | KO simultanés | Édition | RÉCESSIF | n.d. |
| `Pool de glutamate (umami)` | Peptidases, γ-glutamyl-transpeptidase, GDH et GABA-T (les deux dernières augmentent fortement à la maturation) | Cultivé | QTL / ADDITIF | divers |

</details>

## 11. Saveur — volatils & arôme

*Le registre complet des gènes clonés de l'arôme.* — **17 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `TomLoxC` | 13-lipoxygénase : longueur en bouche | 1 | 🟠 SURDOMINANCE | Arôme « tomate » (notes vertes et florales d'antan), longueur en bouche de 2 à 5 min : C5/C6 — (Z)-3-hexénal, hexanal, hexanol — + apocaroténoïdes | SURDOMINANCE / HÉTÉROSIS : les HÉTÉROZYGTES (rare + commun) expriment PLUS que les deux homozygotes → argument fort pour évaluer les F1 sur l'arôme, et pour ne PAS fixer l'allèle à l'homozygotie. Actif dès la F1. Allèle contre-sélectionné à la domestication, en résurgence aujourd'hui. |
| `DXR (promoteur)` | Précurseur des apocaroténoïdes | n.d. | 🟣 QTL / ADDITIF | β-ionone, géranylacétone, 6-méthyl-5-heptén-2-one : notes florales et fruitées | Sélection NÉGATIVE pendant la domestication. Effet d'expression, donc additif/quantitatif. |
| `SlHPL` | Arôme C6 | n.d. | 🟢 DOMINANT | Hexénal, hexanol : « odeur de tomate coupée » | L'allèle fonctionnel est NÉCESSAIRE (dominant pour l'arôme C6). |
| `SlADH2` | Ratio aldéhyde / alcool | 6 | 🟣 QTL / ADDITIF (dosage) | Notes « fruit mûr » plus intenses en surexpression ; l'antisens altère le ratio aldéhyde/alcool | Effet de dosage. Attention : dépend du statut en RIN. |
| `SlCXE1` | Balance des esters | 1 | 🟣 QTL / ADDITIF | Libère les alcools à partir des esters : notes tropicales (mangue, ananas, bonbon) | Avec AAT1, fixe l'équilibre esters/acides : la signature de Sungold. |
| `AAT1` | Alcool acyltransférase | 2 | 🟣 QTL / ADDITIF | Synthèse des ESTERS fruités (fermentation de l'arôme) | QTL additif — la paire AAT1/CXE1 est le « volume » des notes tropicales. |
| `SlCCD1A / SlCCD1B` | Apocaroténoïdes | n.d. | 🔵 RÉCESSIF (bénéfique) | Arôme amélioré (β-ionone…) au prix des pigments | ⚠ COMPROMIS : dégrader plus de caroténoïdes = moins de couleur, plus d'arôme. |
| `AADC1A / AADC1B / AADC2` | QTL « malodorous » | 8 | 🟣 QTL / ADDITIF (fort) | Phénylacétaldéhyde, 2-phényléthanol, 1-nitro-2-phényléthane | Allèle à forte activité, effet marqué non strictement additif. ⚠ Effet AMBIVALENT : perçu « malodorant » dans certains fonds → à valider en panel sensoriel avant d'introgresser. |
| `SlPAR1 / SlPAR2` | Phénylacétaldéhyde réductase | n.d. | 🟣 QTL / ADDITIF (dosage) | Dernière étape de la voie : convertit le phénylacétaldéhyde en 2-phényléthanol (note miel / rose, aussi majeure du parfum de la rose) | La biochimie est solidement établie, la génétique du fruit beaucoup moins : des lignées tomates à expression `LePAR` réduite **n'ont pas** perdu de 2-phényléthanol (redondance, voie déjà limitée par l'amont). À traiter en **effet de dosage**, pas en locus à fixer ; toute prédiction de croisement ici reste une [extrapolation]. |
| `FLORAL4` | Arôme floral | 4 | 🔵 RÉCESSIF (LOF pénalisante) | 2-phényléthanol (rose/thé), phénylacétaldéhyde, 1-nitro-2-phényléthane | L'allèle FONCTIONNEL est nécessaire : l'édition (mutations délétères) effondre les PHEV. Une NIL contrastante est réellement DIFFÉRENCIÉE à la dégustation. |
| `SlSAMT` | Salicylate de méthyle | n.d. | ⚪ MIXTE / SELON FOND | Note mentholée | Fonction enzymatique validée. |
| `SlEGS1` | Eugénol | n.d. | 🟣 QTL / ADDITIF | Note clou de girofle | QTL, dominance non déterminée. |
| `GT1 / UGT` | Volatils glycosylés | n.d. | 🟣 QTL / ADDITIF | Réservoirs d'arôme (les précurseurs glycosylés se libèrent à la dégustation et à la transformation) | Effets quantitatifs ; explique pourquoi un jus cuit sent plus fort qu'un fruit cru. |
| `LIP1 / LIP2` | Lipases | 12 | 🟣 QTL / ADDITIF (additif) | (Z)-4-décénal et plusieurs C5–C10 corrélés au PLAISIR du consommateur | UN SEUL SEGMENT CHROMOSOMIQUE augmente de nombreux volatils positifs → meilleure introgression « rendement aromatique/prix » du lot. |
| `SlYTH2` | Lecteur m6A : le multiplicateur d'arôme | n.d. | 🔵 RÉCESSIF (bénéfique) | +1,5× de volatils TOTAUX, sans altérer la couleur ni la fermeté ; 71 % des dégustateurs préfèrent le fruit édité | LE GÈNE FONCTIONNEL EST UN RÉPRESSEUR ⇒ la perte de fonction est RÉCESSIVE et BÉNÉFIQUE. À fixer à l'homozygotie (ou en hémizygotie T0). |
| `NSGT1` | Arôme « fumé » (gaïacol) | 9 | ⚪ MIXTE / SELON FOND | La forme FONCTIONNELLE empêche la libération de gaïacol (fumé), de salicylate de méthyle et d'eugénol → arôme « propre » | ⚠ CAS INVERSE : les haplotypes NON fonctionnels sont les plus fréquents chez les heirlooms et le cultivé moderne. Sélectionner NSGT1 FONCTIONNEL = assainir l'arôme moderne. |
| `RIN / NOR / FUL1-2` | Chefs d'orchestre de l'arôme | 5 / 10 / n.d. | 🟣 QTL / ADDITIF | Lient directement les promoteurs de TomLoxC, ADH2, HPL, CCD… | Effets PLÉIOTROPES : les mutants rin/nor bloquent la maturation ET détruisent l'arôme. Ne jamais sacrifier l'arôme pour la conservation sans le savoir. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (17 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `TomLoxC` | Allèle rare du PROMOTEUR (variant structural d'~4 kb) + duplication du locus ; Solyc01g006540 | S. pimpinellifolium : présent chez 91 % des tomates groseille, contre 2 % des heirlooms à gros fruit | SURDOMINANCE | 1 |
| `DXR (promoteur)` | Variant sauvage du promoteur → expression accrue du gène en aval | S. pimpinellifolium (58 % des accessions), 5 % chez cerasiforme, 2 % chez les heirlooms | QTL / ADDITIF | n.d. |
| `SlHPL` | 13-hydroperoxyde lyase ; cible de la régulation traductionnelle par SlYTH2 | Cultivé | DOMINANT | n.d. |
| `SlADH2` | Solyc06g059740, alcool déshydrogénase ; régulé par RIN | Cultivé + sauvages | QTL / ADDITIF (dosage) | 6 |
| `SlCXE1` | Carboxyestérase, identifiée par QTL | Cultivé + sauvages | QTL / ADDITIF | 1 |
| `AAT1` | Alcohol acyltransferase | Cultivé | QTL / ADDITIF | 2 |
| `SlCCD1A / SlCCD1B` | Caroténoïde cleavage dioxygenases ; SlCCD1B est traduit plus vite quand SlYTH2 est KO | Cultivé | RÉCESSIF (bénéfique) | n.d. |
| `AADC1A / AADC1B / AADC2` | Décarboxylases d'acides aminés aromatiques | S. pennellii LA0716 via la lignée IL8-2 (fond M82) | QTL / ADDITIF (fort) | 8 |
| `SlPAR1 / SlPAR2` | LePAR1 / LePAR2, réductases à cofacteur NADPH (famille short-chain dehydrogenase/reductase) ; expression maximale dans les boutons floraux, en baisse pendant la maturation ; conversion validée in vivo par surexpression chez le pétunia | Tieman et al. 2007 (Phytochemistry 68:1-11) | QTL / ADDITIF (dosage) | n.d. |
| `FLORAL4` | Solyc04g063350 ; QTL finement cartographié (10 gènes) | Cultivé + sauvages | RÉCESSIF (LOF pénalisante) | 4 |
| `SlSAMT` | Salicylate O-méthyltransférase | Cultivé | MIXTE / SELON FOND | n.d. |
| `SlEGS1` | Eugénol synthase | Cultivé | QTL / ADDITIF | n.d. |
| `GT1 / UGT` | Glycosyltransférases | Cultivé | QTL / ADDITIF | n.d. |
| `LIP1 / LIP2` | Lipases ; allèle SpLIP1 | S. pennellii LA0716, via la lignée IL12-3 | QTL / ADDITIF (additif) | 12 |
| `SlYTH2` | Lecteur de m6A qui RÉPRIME la traduction de SlHPL et SlCCD1B | Édition | RÉCESSIF (bénéfique) | n.d. |
| `NSGT1` | NON-SMOKY GLYCOSYLTRANSFERASE1 : convertit les précurseurs en triglycosides non clivables ; 5 haplotypes décrits (les IV et V sont non fonctionnels, avec délétions emportant aussi E8) | Trait « fumé » décrit chez S. pimpinellifolium et S. l. cerasiforme | MIXTE / SELON FOND | 9 |
| `RIN / NOR / FUL1-2` | Facteurs MADS (RIN, FUL) et NAC (NOR) | Cultivé | QTL / ADDITIF | 5 / 10 / n.d. |

</details>

## 12. Nutrition & innocuité

*Vitamines C / B9 / E, polyphénols, glycoalcaloïdes (amertume), minéraux.* — **17 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `SlGGP1 (uORF)` | Vitamine C | 6 | 🟢 DOMINANT (pratique) | Ascorbate jusqu'à ×5 | Régulation POST-TRANSCRIPTIONNELLE : effet important même avec un seul allèle modifié. ⚠ Compromis : les lignées ×5 présentent stérilité pollinique et fruits sans pépins. |
| `TFA9 / SlbHLH59` | Vitamine C naturelle | 9 | 🟣 QTL / ADDITIF | Le SNP le plus associé explique 15,9 % de la variance en ascorbate | ⚠ LE SEUL levier naturel marqué pour la vitamine C : marqueur direct disponible. |
| `SlGME1 / SlGME2` | É pimérase GDP-mannose | n.d. | 🟣 QTL / ADDITIF | Ascorbate ↑ + tolérance au froid, au sel et au paraquat | Redondance fonctionnelle ⇒ effets additifs, pas de dominance nette. Cible secondaire. |
| `SlNFYA10` | Répresseur de l'ascorbate | n.d. | ⚪ MIXTE / SELON FOND | Le knockdown fait monter l'AsA (> ×2 en feuille, ×1,3 en fruit) | Régulateur NÉGATIF : gain de fonction néfaste, perte de fonction souhaitable. |
| `GCHI + ADCS` | Folates (vitamine B9) | n.d. | 🟢 DOMINANT (tout ou rien) | Folates ×25 (840 µg/100 g) : le fruit ingénieré couvre à lui seul l'apport journalier recommandé d'une femme enceinte | EFFET COOPÉRATIF : il faut les DEUX, l'un seul ne suffit pas. |
| `GGH` | Rétention des folates | n.d. | 🔵 RÉCESSIF | Variété PKM-1 naturellement riche en folates | Seul levier NATUREL identifié. Retard de maturation associé. ⚠ La diversité des folates est très faible (391 accessions, peu de SNPs) et la teneur chute à la maturation. |
| `VTE3(1) / mQTL9-2-6` | Vitamine E (tocophérols) | 9 | ⚫ ÉPIGÉNÉTIQUE | ~50 % de la variation de vitamine E entre les deux parents | ⚠ ICI LA DOMINANCE MENDÉLIENNE NE S'APPLIQUE PAS : hérédité épigénétique. Un marqueur ADN classique peut échouer → prévoir des épi-marqueurs. |
| `VTE1 / VTE2 / VTE4 / VTE5 / HPPD` | Vitamine E, voie complète | 6, 7, 8, 9 | 🟣 QTL / ADDITIF | Héritabilité faible du caractère ; γ- vs α-tocophérol selon VTE4 ; surexpression HPT/TC/γ-TMT jusqu'à ×10 de tocochromanols (jusqu'à la transformation du plastome) | Caractère quantitatif additif. L'azote/potassium du sol module autant que le génotype. |
| `SlMYB12 (= Y/y)` | Flavonols (rutine) | 1 | 🟢 / 🔵 DOMINANT / RÉCESSIF | Le fruit ROSE (y/y) est doublement appauvri : peau transparente + flavonols effondrés. Surexpression : rutine ×11 à ×19 | Le lien direct COULEUR ↔ NUTRITION. Si vous cherchez la santé : évitez les roses. |
| `HQT` | Acide chlorogénique | n.d. | 🟣 QTL / ADDITIF (dosage) | Surexpression : +85 % de CGA ; silençage : −98 % | Effet quasi purement dosique, très reproductible. |
| `SlHY5` | Nutrition ↔ défense | n.d. | ⚪ MIXTE / SELON FOND | Régulateur positif des flavonols ET des glycoalcaloïdes | ILLUSTRE LE COMPROMIS nutrition ↔ défense : monter l'un monte l'autre (dont l'amertume). |
| `GORKY` | Amertume du fruit mûr | n.d. | 🔵 RÉCESSIF | La DÉLÉTION de ce transporteur laisse l'α-tomatine dans la vacuole du fruit mûr : fruit AMER et toxique | CARACTÈRE MONOGÉNIQUE RÉCESSIF explicitement documenté : il faut gorky/gorky pour que le fruit reste amer. GORKY fonctionnel (dominant) = fruit non amer. À vérifier avant tout croisement avec du sauvage. |
| `GAME5 / GAME31 / GAME36 / GAME40` | Détoxification des SGA | 8 (GAME5) | 🔵 RÉCESSIF | Dernière étape α-tomatine → esculéoside A (non amer, non toxique) ; hydroxylation / acétylation / glycosylation | Le silençage de GAME5 fait remonter l'α-tomatine. |
| `GAME9 / GE1` | Sélection anti-amertume | 7 | ⚪ MIXTE / SELON FOND | Les allèles « faibles » (modernes) réduisent les glycoalcaloïdes ; l'allèle sauvage « fort » de GAME9 active GAME7/GAME17 | ⚠ GE1 faible et GAME9 faible = principales causes de la baisse volontaire des SGA. La perturbation de GE1 donne des fruits à surface ridée (accumulation de γ-tomatine). |
| `DML2` | Épigénétique de la détox | n.d. | ⚫ ÉPIGÉNÉTIQUE | Assure la détoxification du fruit à la maturation ; le variant DML2^13D a basculé à la domestication | Hérédité épigénétique/pléiotrope : pas de dominance mendélienne simple. |
| `SlHMA3 / SlNRAMP6 / SlPCR2` | Cadmium (innocuité) | n.d. | 🟣 QTL / ADDITIF | Séquestrent le Cd dans la vacuole → réduction du Cd des organes comestibles | Caractère quantitatif ; introgression d'allèles « séquestrants » = piste de sécurité alimentaire. |
| `TOMLHA1 / FRO1 / NRAMP2 / FER / MYB72` | Fer & zinc du fruit | divers | 🟣 QTL / ADDITIF | AUCUN gène majeur de Fe/Zn du fruit n'est cloné à ce jour ; QTL via porte-greffes et populations RIL | Polygénique, additif, héritabilité faible ⇒ la biofortification AGRONOMIQUE (fumure foliaire) reste plus efficace et plus rapide que la génétique. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (17 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `SlGGP1 (uORF)` | uORF en 5′ qui freine la traduction de GDP-L-galactose phosphorylase (Solyc06g073320) ; le casser (CRISPR) ou surexprimer lève le frein | Cultivé + mutant EMS « haut ascorbate » cartographié dans l'uORF | DOMINANT (pratique) | 6 |
| `TFA9 / SlbHLH59` | InDel de 8 pb dans le promoteur (motif Py-rich de la 5'UTR) d'un facteur bHLH | Cultivé (sélectionné à la domestication) | QTL / ADDITIF | 9 |
| `SlGME1 / SlGME2` | Surexpression ; le silençage d'un seul gène est COMPENSÉ par l'autre | Cultivé | QTL / ADDITIF | n.d. |
| `SlNFYA10` | Facteur CCAAT qui réprime SlGME1/SlGGP1 | Cultivé | MIXTE / SELON FOND | n.d. |
| `GCHI + ADCS` | Deux branches limitantes (ptéridine et PABA) ; GCHI seul ne donne que ×2–4 | Ingénierie | DOMINANT (tout ou rien) | n.d. |
| `GGH` | Activité γ-glutamyl hydrolase réduite → meilleure rétention des folates polyglutamylés | Cultivé (PKM-1) | RÉCESSIF | n.d. |
| `VTE3(1) / mQTL9-2-6` | Le polymorphisme causal n'est PAS dans la séquence codante mais dans la MÉTHYLATION DU PROMOTEUR (épiallèles naturels) | IL de S. pennellii | ÉPIGÉNÉTIQUE | 9 |
| `VTE1 / VTE2 / VTE4 / VTE5 / HPPD` | QTL confirmés + 16 loci candidats | Cultivé + sauvages | QTL / ADDITIF | 6, 7, 8, 9 |
| `SlMYB12 (= Y/y)` | R2R3-MYB activateur de PAL/CHS/FLS ; corrélation expression ↔ flavonols R² ≈ 0,92 | Cultivé | DOMINANT / RÉCESSIF | 1 |
| `HQT` | Hydroxycinnamoyl-CoA quinate transférase | Cultivé | QTL / ADDITIF (dosage) | n.d. |
| `SlHY5` | Lie les boîtes G des promoteurs des deux voies ; la perte de fonction fait chuter les deux et rend sensible aux champignons | Cultivé | MIXTE / SELON FOND | n.d. |
| `GORKY` | Transporteur NPF du tonoplaste | Landraces péruviennes « high tomatine », sauvages | RÉCESSIF | n.d. |
| `GAME5 / GAME31 / GAME36 / GAME40` | Solyc08g006410 (UDP-glycosyltransférase) ; allèles nuls (codon stop) décrits | Cultivé + sauvages | RÉCESSIF | 8 (GAME5) |
| `GAME9 / GE1` | GAME9 = AP2/ERF à faible capacité de liaison à l'ADN ; GE1 = enhancer distal qui recrute le complexe MYC2–GAME9 et forme des boucles chromatine sur le cluster GAME (chr 7) | Fixés à la domestication | MIXTE / SELON FOND | 7 |
| `DML2` | Déméthylase d'ADN (DEMETER-LIKE 2), avec RIN, NOR, FUL1 et MYC2 sur le réseau GAME | Cultivé | ÉPIGÉNÉTIQUE | n.d. |
| `SlHMA3 / SlNRAMP6 / SlPCR2` | ATPase P1B du tonoplaste + NRAMP + PCR2 | Cultivé + sauvages | QTL / ADDITIF | n.d. |
| `TOMLHA1 / FRO1 / NRAMP2 / FER / MYB72` | Familles NRAMP / ZIP / YSL / NAS / ferritines | Cultivé + sauvages | QTL / ADDITIF | divers |

</details>

## 13. Résistances biotiques

*Maladies et ravageurs : gènes majeurs, QTL, dominance et contournements.* — **27 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `I` | Fusarium race 1 | 11 | 🟢 DOMINANT | Résistance à Fusarium oxysporum f. sp. lycopersici race 1 | Premier gène de résistance déployé en tomate (1939). Contourné par la race 2 → à pyramider avec I-2 / I-3. |
| `I-2` | Fusarium races 1 et 2 | 11 | 🟢 DOMINANT | Résistance aux races 1 ET 2 | Très utilisé commercialement, souvent pyramidé avec I-3 (qui vient de S. pennellii). |
| `Ve (Ve1)` | Verticilliose race 1 | 9 | 🟢 DOMINANT | Résistance à Verticillium dahliae et V. albo-atrum race 1 | Présent dans la majorité des cultivars. ⚠ Race 2 de Verticillium le contourne. |
| `Pto / Prf` | Moucheture bactérienne | 5 | 🟢 DOMINANT | Résistance à Pseudomonas syringae pv. tomato race 0 | Efficace des décennies contre la race 0, CONTOURNÉ par la race 1. La seule résistance Pto sans Prf ne donne rien. |
| `qRpp (LA1589)` | Résistance quantitative à Pst race 1 | 5, 6, 8 | 🟣 QTL / ADDITIF | Résistance SANS réponse hypersensible, là où Pto est contourné | Le complément quantitatif indispensable aux gènes majeurs usés. |
| `FLS3` | Perception de la flagelline | n.d. | 🟢 DOMINANT | PRR de surface : reconnaît la flgII-28 de Pseudomonas et amplifie l'immunité basale | Beaucoup de cultivars modernes ont PERDU FLS3 : le réintroduire est un levier d'immunité large. |
| `Cf-2.1 / Cf-2.2` | Cladosporiose (Avr2) | 1 | 🟢 DOMINANT | Résistance à Passalora (Cladosporium) fulvum races portant Avr2 | Le locus Cf-2 est le plus variable des populations naturelles : à génotyper finement. |
| `Cf-4` | Cladosporiose (Avr4) | 1 | 🟢 DOMINANT | Résistance | Dispersion du gène dans les populations sauvages documentée (Thomas 2000). |
| `Cf-5, Cf-8, Cf-9, Cf-13` | Cladosporiose | 1 | 🟢 DOMINANT | Résistance à plusieurs races (Avr5, Avr9…) | Cf-9/Cf-4 = locus Milky Way. Pyramidages classiques en serre. |
| `Cf-ECP1/2/4/5` | Reconnaissance d'effecteurs apoplastiques | 1 et 6 | 🟢 DOMINANT | Résistance via les récepteurs d'éliciteurs apoplastiques | Nouveaux loci : utiles contre les races échappant aux Cf classiques. |
| `Ph-1` | Mildiou | 7 | 🟢 DOMINANT | Résistance à Phytophthora infestans race T0 UNIQUEMENT — contourné par la race T1 aujourd'hui dominante | Ne compte plus guère seule : c'est Ph-2 + Ph-3 qu'il faut cumuler (les cultivars « DuR » combinent Ph-1/2/3). |
| `Ph-2` | Mildiou | 10 | 🟡 SEMI-DOMINANT | Freine la progression du mildiou | INCOMPLÈTEMENT DOMINANT : l'hétérozygote résiste moins. Résistance « fonctionnelle » à l'anglaise. |
| `Ph-3` | Mildiou | 9 | 🟡 SEMI-DOMINANT | Hypersensibilité cellulaire ciblée, résistance la plus forte des trois | Ph-2 + Ph-3 pyramidés = protection quasi totale contre les souches agressives, à l'état homozygote. |
| `Xv3 / Rx-4` | Tache bactérienne race T3 | 11 | 🟡 SEMI-DOMINANT | Résistance à Xanthomonas perforans race T3 | DOMINANCE INCOMPLÈTE. La race T2/T1 contournante est répandue : à associer aux rx récessifs. |
| `rx-1, rx-2 (chr 1) / rx-3 (chr 5)` | Tache bactérienne race T1 | 1 et 5 | 🔵 RÉCESSIF | Résistance aux Xanthomonas race T1 | RÉCESSIFS : nécessitent l'homozygotie, donc sélection par marqueurs et fixation. |
| `Ol-1, Ol-3, Ol-5` | Oïdium | 6 | 🟢 DOMINANT | Résistance majeure à Oidium neolycopersici (cluster Ol à 34 Mb) | Dominants et durables. En pratique, Ol-1 + Ol-5 se cumulent. |
| `On-9-l_che` | Oïdium (QTL des Galápagos) | 9 | 🟡 SEMI-DOMINANT | Résistance partielle à l'oïdium : explique 14,6 % de la variance (40 % de l'écart entre parents) | DOMINANCE PARTIELLE (pas dominante stricte, contrairement à certaines fiches). Faible linkage drag : idéal pour introduire chez les tomates cerises. |
| `ol-2 (Slmlo1)` | Oïdium, résistance durable | 4 | 🔵 RÉCESSIF | Résistance à LARGE SPECTRE et présumée durable (pas de contournement connu) | ⚠ ATTRIBUTION CORROMPUE : ol-2 ne vient PAS de S. habrochaites. Seul gène d'oïdium cloné, récessif → homozygotie obligatoire. |
| `Ty-2 (TYNBS1)` | TYLCV (enroulement jaune) | 11 | 🟢 DOMINANT | Résistance complète aux begomovirus (TYLCV) | DOMINANT COMPLET (efficace en hétérozygote), déployé dans le monde entier. ⚠ L'introgression porte une INVERSION de ~300 kb qui bloque la recombinaison (gros linkage drag) ; spectre étroit (inefficace sur TYLCSV, BCTV) → pyramider avec Ty-1/3 (S. chilense) ou ty-5 (S. peruvianum, récessif). |
| `Tm-1` | ToMV / ToMV-like, composante ToBRFV | 2 | 🟡 SEMI-DOMINANT | Inhibition de la réplicase virale ; contribue à la résistance au ToBRFV en combinaison | SEMI-DOMINANT (effet dose). Actuel : Tm-1 (chr 2) + un locus RÉCESSIF de tolérance sur le chr 11 = résistance au ToBRFV ; le tm-1 récessif + chr 11 = tolérance. |
| `ToBRFV-R (chr 11)` | Fruit rugueux brun | 11 | 🔵 RÉCESSIF | Tolérance (faible accumulation virale, symptômes réduits) | RÉSISTANCE = au moins 2 gènes (Tm-1 dominant + locus chr 11) ; TOLÉRANCE = gène récessif unique. F1 sensible si le donneur est homozygote récessif croisé avec un cultivar → trier en F2. Tm-2² est contourné par le virus. |
| `Wf-1` | Mouches blanches, pucerons, thrips, acariens, Tuta | 2 | 🟡 SEMI-DOMINANT | Barrière physique + chimique : active les trichomes type IV et jusqu'à 76 acylsucres ; explique ~54 % de la survie des adultes d'aleurodes et ~81 % de la densité de trichomes IV | PARTIELLEMENT DOMINANT à additif fort. Wf-2 (chr 9) en complément. Le phénotype se lit à la loupe (face inférieure, feuilles collantes). |
| `ShTPS / zFPS + ShZIS (locus Sst)` | Répulsif olfactif des ravageurs | 8 | 🟣 QTL / ADDITIF (codominant) | Zingibérène et 7-épi-zingibérène (sesquiterpène des trichomes VI) : répulsion et toxicité sur Bemisia, Tetranychus, Tuta absoluta, Diabrotica + activité antimicrobienne | Introgressions réussies (lignées à haut ZGB). Les gènes de la voie sont utilisables comme MARQUEURS moléculaires. |
| `MKS1 × MKS2` | Insecticide naturel (2-tridécanone) | 8 | ⚪ MIXTE / SELON FOND | 2-tridécanone et méthylcétones des trichomes VI : toxicité larvaire (Manduca, Tuta, mineuses, doryphore) | ÉPITASIE COMPLEXE : un seul des deux allèles ne donne rien. À pyramider obligatoirement. |
| `QTL psylle` | Résistance au psylle des solanées + Liberibacter | 1, 3, 5, 6, 8 | 🟣 QTL / ADDITIF | Mortalité adulte et baisse de fécondité de Bactericera cockerelli, donc moins de zèbre | Polygénique : sélection génomique ou phénotypique en conditions d'infestation. |
| `Rcm 2.0 / Rcm 5.1` | Chancre bactérien | 2 et 5 | 🟣 QTL / ADDITIF | Résistance quantitative à Clavibacter michiganensis (agirait sur la morphologie vasculaire) | Aucun gène majeur disponible : la prévention (semences saines, hygiène) reste primordiale. |
| `Sw-5 / Mi-1 / Ty-1, Ty-3, Ty-4 / ty-5` | À NE PAS CHERCHER chez vous | — | 🟢 / 🔵 DOMINANT / RÉCESSIF | TSWV (Sw-5), nématodes + pucerons (Mi-1), TYLCV (Ty-1/3/4, ty-5) | ⚠ Ces gènes ne sont PAS dans votre germoplasme (pimpinellifolium, cheesmaniae, habrochaites, galapagense) : il faut les acquérir par accession TGRC ou les acheter en variété. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (27 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `I` | LRR-RLP (Solyc11g011180), reconnaît l'effecteur Avr1/Six4 | S. pimpinellifolium (PI 79532 « Missouri 160 ») | DOMINANT | 11 |
| `I-2` | CC-NB-LRR (Solyc11g071430), reconnaît Avr2/Six3 (+ SIX5) | Hybride naturel S. pimpinellifolium × S. lycopersicum (PI 126915) | DOMINANT | 11 |
| `Ve (Ve1)` | RLP à LRR extracellulaires reconnaissant l'effecteur Ave1 | « Peru Wild » (S. pimpinellifolium), années 1930 | DOMINANT | 9 |
| `Pto / Prf` | Kinase sérine/thréonine Pto + NLR Prf (cluster) | S. pimpinellifolium | DOMINANT | 5 |
| `qRpp (LA1589)` | 3 QTL + 5 gènes candidats | S. pimpinellifolium LA1589 | QTL / ADDITIF | 5, 6, 8 |
| `FLS3` | LRR-RLK | S. pimpinellifolium (Hind et al. 2016) | DOMINANT | n.d. |
| `Cf-2.1 / Cf-2.2` | Deux LRR-RLP en tandem, tous deux fonctionnels ; locus très polymorphe (≥26 homologues « Hcr2p ») | S. pimpinellifolium | DOMINANT | 1 |
| `Cf-4` | LRR-RLP, locus « Milky Way » | Attribué historiquement à L. hirsutum = S. habrochaites (attribution débattue) | DOMINANT | 1 |
| `Cf-5, Cf-8, Cf-9, Cf-13` | LRR-RLP | S. pimpinellifolium (Cf-9, Cf-5, Cf-8 PI 124161, Cf-13 PI 211839) | DOMINANT | 1 |
| `Cf-ECP1/2/4/5` | LRR-RLP ; Cf-ECP1/4 colocalisent avec Cf-9/Cf-4 au locus Milky Way | S. pimpinellifolium | DOMINANT | 1 et 6 |
| `Ph-1` | Rick 1955 / Gallegly & Marvel ; gène majeur cloné non publié | S. pimpinellifolium (West Virginia 19 et 731) | DOMINANT | 7 |
| `Ph-2` | LRR-RLP | S. pimpinellifolium | SEMI-DOMINANT | 10 |
| `Ph-3` | CC-NB-LRR (cluster) ; marqueur co-dominant Ph-3-GLR/S | S. pimpinellifolium (accession L3708 / LA1269) | SEMI-DOMINANT | 9 |
| `Xv3 / Rx-4` | NB-LRR reconnaissant AvrXv3 | S. pimpinellifolium (PI 128216, lignée H7981) | SEMI-DOMINANT | 11 |
| `rx-1, rx-2 (chr 1) / rx-3 (chr 5)` | Gènes récessifs (perte de fonction / reconnaissance alternative) | Lignée H7998, origine historique S. habrochaites (PI 126445) | RÉCESSIF | 1 et 5 |
| `Ol-1, Ol-3, Ol-5` | Gènes R (Ol-5 = HR lente) | S. habrochaites : G1.1560 (Ol-1), G1.1290 (Ol-3), PI 247087 (Ol-5, var. glabratum) | DOMINANT | 6 |
| `On-9-l_che` | QTL entre 46,5 et 50,5 cM du chr 9, pic à 48 cM, cartographié par QTL-seq | S. cheesmaniae | SEMI-DOMINANT | 9 |
| `ol-2 (Slmlo1)` | Perte de fonction d'un gène MLO (susceptibilité) : le pathogène a besoin de l'hôte | S. l. var. cerasiforme LA1230 | RÉCESSIF | 4 |
| `Ty-2 (TYNBS1)` | NLR ; l'effecteur viral est la protéine Rep/C1 | S. habrochaites f. glabratum B6013, via la lignée H24 | DOMINANT | 11 |
| `Tm-1` | Protéine p80 inhibitrice (mécanisme antiviral inhabituel, pas un NLR ; région sous sélection positive chez S. habrochaites) | S. habrochaites PI 126445 (Pelham 1966) ; allèles de S. pennellii également efficaces | SEMI-DOMINANT | 2 |
| `ToBRFV-R (chr 11)` | Locus à ~46,84 Mb du chr 11 (intervalle de 22 kb) ; candidats Solyc11g062150 (TIR-NBS-LRR) et Solyc11g062180 (RLP) | S. pimpinellifolium USVL332 (PI 390717) ; locus aussi décrit chez S. pennellii | RÉCESSIF | 11 |
| `Wf-1` | QTL majeur de bout de chromosome 2, co-localisé avec densité de trichomes IV et métabolites (famille ASAT, locus AT2) | S. galapagense (LA1401 etc.) ; acylsucres aussi chez S. habrochaites et S. pimpinellifolium | SEMI-DOMINANT | 2 |
| `ShTPS / zFPS + ShZIS (locus Sst)` | Cluster biosynthétique zFPS + ShZIS (chr 8, LA1777) ; ShZO = ShCYP71D184 (P450, chr 1) oxyde le composé en dérivés plus toxiques | S. habrochaites var. hirsutum PI 127826, LA1777, PI134418 | QTL / ADDITIF (codominant) | 8 |
| `MKS1 × MKS2` | Gènes de la voie ShMKS1/ShMKS2 ; l'effet exige les deux allèles sauvages | S. habrochaites var. glabratum PI 134417 | MIXTE / SELON FOND | 8 |
| `QTL psylle` | Pas de gène cloné | S. habrochaites LA1777 | QTL / ADDITIF | 1, 3, 5, 6, 8 |
| `Rcm 2.0 / Rcm 5.1` | QTL (Rcm2.0 chr 2, Rcm5.1 chr 5) | S. habrochaites LA407 ; QTL aussi chez S. pimpinellifolium GI 1554 (chr 1, 2, 7, 8, 12) | QTL / ADDITIF | 2 et 5 |
| `Sw-5 / Mi-1 / Ty-1, Ty-3, Ty-4 / ty-5` | Gènes majeurs dominants, sauf ty-5 récessif | S. peruvianum (Sw-5, Mi-1, ty-5) et S. chilense (Ty-1/3/4) | DOMINANT / RÉCESSIF | — |

</details>

## 14. Tolérances abiotiques & racines

*Sel, sécheresse, froid, chaleur — presque tout est additif.* — **11 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `HKT1;1 / HKT1;2` | Homéostasie Na+/K+ (sel) | 7 | 🟣 QTL / ADDITIF (additif) | Protège fleurs et fruits du stress salin et thermique ; le QTL majeur explique > 40 % de la variance [Na+]/[K+]. ScHKT1;2 exclut efficacement le Na+ du xylème vers les tiges ; ScHKT1;1 est hyperactif dans les feuilles et les racines | Effet ADDITIF, co-introgression des deux loci recommandée. Stratégies d'inclusion (cheesmaniae) et d'exclusion (galapagense) COMPLÉMENTAIRES et cumulables. |
| `HKT2;1` | Récupération du Na+ du xylème | n.d. | 🟣 QTL / ADDITIF | Redistribue le Na+ via le phloème | Complément des HKT1 ; quantitatif. |
| `lnc1.1 (candidat NHX3)` | Concentration foliaire en Na+ | 1 | 🟣 QTL / ADDITIF | Compartimente le Na+ dans la vacuole foliaire (stratégie « incluseuse ») | Gènes SOS1/SOS2/SOS3/NHX1 cartographiés comme candidats de la voie SOS : utiles en marquage. |
| `SpiI3PS` | Tolérance au sel (myo-inositol) | n.d. | 🟣 QTL / ADDITIF | Copies additionnelles de l'inositol-3-phosphate synthase → meilleure osmoprotection | Le génome LA0480 est ENRICHI en gènes de réponse aux stress (biotiques et abiotiques). |
| `DREB1A / VP1.1` | haplotypes de tolérance au sel | n.d. | 🟣 QTL / ADDITIF | Variations alléliques associées à la tolérance (17–26 % de la variance en panel d'association) | Haplotypes, pas un gène unique : à génotyper en population. |
| `QTL rendement sous sel` | ~15 QTL | 1, 3, 7, 8, 11 | 🟣 QTL / ADDITIF | Poids et nombre de fruits, floraison sous salinité ; effets moyens de 8,5 à 16 % | Les allèles favorables sont généralement SAUVAGES. Attention au drag (petits fruits) : rétrocroisements assistés. |
| `Effet porte-greffe` | Rendement du greffon sous sel | divers | 🟣 QTL / ADDITIF | ≥ 8 QTL racinaires ; jusqu'à 65 % des lignées porte-greffe améliorent l'hybride commercial sous salinité | LE LEVIER LE PLUS COURT : greffer cette saison plutôt qu'introgresser pendant 5 ans. |
| `stm9` | Mise en réserve des glucides / turgescence | 9 | 🟣 QTL / ADDITIF | Maintien de la turgescence stomatique à 6 °C aux racines et sous sécheresse estivale ; 33 % de la variance expliquée | Un des rares QTL abiotiques à aussi fort effet ; MAS possible. |
| `DRO1 & architecture racinaire` | Enracinement profond | 9 | 🟣 QTL / ADDITIF | Racines longues et conductivité hydraulique élevée : exploration des couches profondes moins salines | Combine avec HKT : exclusion racinaire + racines profondes. |
| `QTL turgescence / température du couvert` | Déficit hydrique | 1, 5, 6, 7 | 🟣 QTL / ADDITIF | qtur/qtem sur chr 5 et 7 (6,8–9,1 % de variance) ; qtem sur chr 1 distal et 6 | Polygénique à petits effets : la sélection génomique + l'imagerie thermique battent le MAS simple. |
| `QTL chaleur (chr 9)` | Tolérance à la chaleur reproductive | 9 | 🟣 QTL / ADDITIF | Maintien du nombre de graines sous stress thermique (transporteurs ABC candidats) | ⚠ LA1589 elle-même est SENSIBLE à la chaleur : les tolérances peuvent être cryptiques et ne se révéler qu'en fond cultivé. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (11 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `HKT1;1 / HKT1;2` | Transporteurs Na+ de classe I ; le cultivé a PERDU l'expression de HKT1;1 et fixé un HKT1;2 différent | S. cheesmaniae (inclusion) + S. galapagense (exclusion, IL SG18_197 LA1141 × OH8245) | QTL / ADDITIF (additif) | 7 |
| `HKT2;1` | Transporteur K+-Na+ | S. cheesmaniae | QTL / ADDITIF | n.d. |
| `lnc1.1 (candidat NHX3)` | QTL, candidat NHX3 | S. cheesmaniae | QTL / ADDITIF | 1 |
| `SpiI3PS` | Variation en nombre de copies | S. pimpinellifolium LA0480 | QTL / ADDITIF | n.d. |
| `DREB1A / VP1.1` | Facteur DREB + promoteur VP1 | S. pimpinellifolium | QTL / ADDITIF | n.d. |
| `QTL rendement sous sel` | Population F7 « P » (pimpinellifolium) et « C » (cheesmaniae) ; un QTL ÉPISTATIQUE DOMINANT sur le chr 3 | S. pimpinellifolium, S. cheesmaniae | QTL / ADDITIF | 1, 3, 7, 8, 11 |
| `Effet porte-greffe` | h² ≈ 0,3, allèles favorables sauvages | S. pimpinellifolium, S. cheesmaniae | QTL / ADDITIF | divers |
| `stm9` | QTL majeur additif | S. habrochaites | QTL / ADDITIF | 9 |
| `DRO1 & architecture racinaire` | QTL + criblages LA1400/LA1401 | S. galapagense | QTL / ADDITIF | 9 |
| `QTL turgescence / température du couvert` | Population BC2S3 LA1141 × OH8245 ; sélection phénotypique (imagerie thermique) vs génomique | S. galapagense | QTL / ADDITIF | 1, 5, 6, 7 |
| `QTL chaleur (chr 9)` | Introgression 65,5–66,3 Mb, lignées BIL LA1589 | S. pimpinellifolium | QTL / ADDITIF | 9 |

</details>

## 15. Sources alléliques : votre germoplasme

*Espèce par espèce : ce que vous avez, à quelle probabilité, et comment le vérifier.* — **7 loci**

> 🍅 **À quel niveau de ploïdie travailler ?** Le TGRC maintient des **autotétraploïdes** (2-095 San Marzano 4x, 2-483 Red Cherry 4x, LA2335 *S. pimpinellifolium* 4x fertile) dont le comportement en croisement n'a rien de commun avec les lignes ci-dessus : voir l'annexe [TETRAPLOIDIE.md](TETRAPLOIDIE.md), sections 3 et 9.

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `S. pimpinellifolium` | La meilleure de vos 4 espèces | — | ▫️ — | Sucre + arôme + vitamine C + résistances (Ph-1/2/3, Cf, I/I-2, Pto, Xv3, FLS3). Croisement DIRECT sans barrière, autogame → lignées faciles à fixer | Vérifier SANS NUMÉRO D'ACCESSION = raisonner en probabilités : la variabilité intra-espèce dépasse souvent la variabilité inter-espèces. |
| `S. cheesmaniae` | Usine à provitamine A + sel | — | ▫️ — | Locus B (β-carotène) chez TOUTES les accessions ; tolérance à ~200 mM NaCl (stratégie inclusive) ; j-2 (récolte sans calice) ; u, ag2 ; solubles solubles élevés | ⚠ PAS de trichomes type IV → pas de résistance aux aleurodes. ⚠ N'est PAS source de résistance au TYLCV (0 accession asymptomatique sur 9 testées). |
| `S. galapagense` | Le meilleur contre les aleurodes | — | ▫️ — | Wf-1 (chr 2) + Wf-2 (chr 9) = trichomes IV + 76 acylsucres ; tolérance au sel (exclusion + racines) et à la sécheresse ; nouveaux allèles Aft/atv (fruit pourpre) ; B (β-carotène) | ⚠ Inversions de 18–21 Mb (chr 5), 7,4 Mb (chr 8) et 16–17 Mb (chr 11) → linkage drag structurel. Feuillage collant : pénible en serre, précieux en lutte intégrée. Graines dormantes : trempage 24 h, voire scarification. |
| `S. habrochaites` | Le réservoir de résistance n°1 | — | ▫️ — | Ty-2 (TYLCV), Tm-1, Ol-1/3/5, Rcm 2.0/5.1, rx-1/2/3, zingibérène (ZGB), MKS1/2 (2-tridécanone), 30 QTL de volatils, ascorbate (bin 8-B), tolérance froid/sécheresse, vigueur racinaire (porte-greffe) | ⚠ Auto-INCOMPATIBLE (allogame) : impossible de fixer par autofécondation, maintenez des familles. Fruit VERT non consommable, arômes « sauvages », éthylène très élevé. À utiliser en PARENT MÂLE : en sens inverse, l'incompatibilité unilatérale fait rejeter le pollen du cultivé. |
| `S. pennellii LA0716` | Le donateur des QTL | — | ▫️ — | LIN5 (Brix9-2-5), IL8-2 (AADC, « malodorous »), IL12-3 (LIP1/LIP2), fw3.2, fw11.3, Del, allèles Tm-1 de type pennellii, I-3 | La référence mondiale pour la génétique QUANTITATIVE de la tomate. Tous les segments sont déjà isolés en lignées : à demander, pas à créer. |
| `S. chmielewskii LA1028` | Le vieux gisement de Brix | — | ▫️ — | ≈10 % de solubles solubles (contre ≈5 % chez le cultivar VF36), +13 % à l'homozygote et +12 % à l'hétérozygote | ⚠ Fruits VERTS et pH élevé : l'introgression traîne des défauts à casser par rétrocroisements. |
| `S. chilense / lycopersicoides / peruvianum` | Pas chez vous, mais utiles | — | ▫️ — | Ty-1/3/4 + Aft (chilense), Abg + Del + LA2951 (lycopersicoides), Mi-1 + Sw-5 + ty-5 (peruvianum) | Barrières d'hybridabilité plus fortes : rétrocroisements longs, ovules immatures in vitro souvent nécessaires. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (7 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `S. pimpinellifolium` | Allèle rare de TomLoxC chez 91 % des accessions ; SlCDPK27 haut-sucre prévalent ; SlSPS1 AG (LA1924) ; variant DXR chez 58 % ; lycopène jusqu'à 390 µg/g (LA2093) | Accessions : LA0480, LA1589, LA1924, LA2093, TO-937, USVL332 (PI 390717), L3708, PI 126915, PI 128216 | — | — |
| `S. cheesmaniae` | B (Cyc-B) dominant ; j-2 récessif (LA0166) ; HKT1;1/HKT1;2 chr 7 ; ~15 QTL rendement sous sel | LA0166, LA0422, LA0428, LA1039 (génome), USVL | — | — |
| `S. galapagense` | Firdaus 2013 (Wf) ; Yu 2022 (génome de référence du super-pangénome) ; LA1141 (Aft, atv, u, QTL sel/sécheresse) | LA1141, LA1400, LA1401 (les IL de pennellii sont LA0716, autre espèce) | — | — |
| `S. habrochaites` | LA1353 = 265 NLR intacts, le plus grand répertoire immunitaire connu du genre ; voie zingibérène zFPS+ShZIS (chr 8) et ShCYP71D184 (chr 1) ; 30 QTL de volatils cartographiés | PI 126445, PI 127826, PI 134417, PI 247087, B6013, LA1777, LA0407, CGN15391, LA2167 | — | — |
| `S. pennellii LA0716` | Bibliothèque d'IL (Eshed & Zamir) : 75 lignes couvrant ~98 % du génome donneur, fond M82 | TGRC / Cornell | — | — |
| `S. chmielewskii LA1028` | Lignées LA1563 (BC5S5, 7–8 % SS) et segments VF145B-7879 | *S. chmielewskii* LA1028 (Casinchichua, Apurimac, Pérou) — accession TGRC ; dérivés LA1563 et VF145B-7879 | — | — |
| `S. chilense / lycopersicoides / peruvianum` | Bibliothèques d'IL publiées | *S. chilense* (Ty-1/3, Aft), *S. lycopersicoides* LA2951, *S. peruvianum* (Mi-1, Sw-5, ty-5) — toutes via le TGRC | — | — |

</details>

> ⚠️ Sans numéro d'accession, on raisonne en **probabilités** : la variabilité *à l'intérieur* d'une espèce dépasse souvent la variabilité *entre* espèces. Les tests de vérification sont dans le [protocole](#protocole-de-programme).

## 16. Combinaisons & épistasies

*Ce qui se cumule, ce qui s'écrase, ce qui vous tue la plante.* — **16 loci**

| Symbole | Nom / locus | Chr. | Dominance | Effet, phénotype | Ce que ça change en sélection |
|:--|:--|:--:|:--|:--|:--|
| `c + gob` | Double récessif potato leaf × goblet | — | ▫️ — | Feuilles presque TOTALEMENT simples (synergie) | Phénotype additif prévisible : utile pour « simplifier » un feuillage. |
| `e + La` | Double entire × Lanceolate | — | ▫️ — | Simplification renforcée (feuille simple franche) | e La-2/+ : feuille simple à limbe unique. |
| `tf + Me/+ ; tf + clau ; tf + bip` | Épistasie de trifoliate | — | ▫️ — | Le patron trifolié de base est CONSERVÉ ; seule la découpure de chaque foliole change (parfois plus extrême que chez le sauvage) | Règle : un gène de module différent se combine de façon prévisible ; un gène du MÊME module sature. |
| `35S:Kn1 + c / tf / e` | Kn1 ne ramifie qu'un plan préexistant | — | ▫️ — | Kn1 produit 700–2000 folioles par feuille chez le sauvage et augmente la ramification chez Pts — mais ÉCHOUÉ à restaurer la feuille composée chez potato-leaf, trifoliate et probablement entire | La hiérarchie du patron de base : La > tf > KNOX/GOB > e. |
| `La + tout` | Lanceolate est épistasique | — | ▫️ — | « La is epistatic to all known leaf shape mutations » : tout double La + gène de complexité donne une feuille simple ; La/La ne forme même pas de méristème caulinaire | La/La létal embryonnaire : ne jamais chercher à l'homozygoter. |
| `miR319 / miR164` | Fenêtre morphogénétique × découpage | — | ▫️ — | Surexprimer miR319 → feuilles « super-composées » à marges indifférenciées, largement SUPPRIMÉES par miR164 ou gob-3 ; surexprimer miR164 supprime le phénotype la-6 | Le cadre conceptuel le plus rentable pour prédire un double mutant de feuille. |
| `SlMP (SlARF5) + Gob-4d` | Additivité auxine × CUC | — | ▫️ — | Moins de folioles primaires, pétioles plus longs, sinus plus nombreux et profonds que chaque simple mutant | Les gènes de modules différents s'additionnent : ce sont les combinaisons qui marchent. |
| `j + s` | Jointless masque compound | — | ▫️ — | j supprime la ramification extrême de l'inflorescence de s | À savoir si vous voulez des grappes ramifiées ET sans pédoncule : ce n'est pas cumulable tel quel. |
| `sp + sft` | Port semi-déterminé | — | ▫️ — | sft/sft en fond SP = arrêté ; SFT/sft en fond sp = SEMI-DÉTERMINÉ (architecture intermédiaire très utilisée en sélection) | Le « semi-déterminé » commercial = sp + hétérozygotie sft, pas un gène nouveau. |
| `d + sp (+ mnt)` | Micro-Tom | — | ▫️ — | Nain ET déterminé (et mnt = micro-nain) | Le port déterminé et la taille sont GÉNÉTIQUEMENT INDÉPENDANTS : on peut être grand et déterminé, ou nain et indéterminé. |
| `clau + lyr` | Complexité renforcée | — | ▫️ — | Phénotype renforcé (les deux voies convergent vers GOB) | — |
| `SUN + LC + FAS` | Le cœur de bœuf | — | ▫️ — | SUN ≻ LC pour la forme globale (fruit long même avec lc) ; mais l'ajout de FAS RE-ARRONDIT et donne la forme oxheart « cœur de bœuf » | La forme d'un fruit = la somme pondérée des deux axes : ne jamais raisonner sur un seul gène. |
| `t + r` | Épistasie couleur | — | ▫️ — | t (tangerine) est épistatique sur r^2997 (les cis-caroténoïdes restaurent PSY1) ; d'autres allèles de r (r^3756) sont épistatiques sur t | Le génotype de l'allèle r précis compte : un marqueur « r » générique peut mentir. |
| `Cnr + rin/nor` | Blocage de blocage | — | ▫️ — | Cnr est ÉPISTATIQUE sur rin et nor | Un seul Cnr suffit à écraser le reste du programme de maturation. |
| `Aft/Abg + atv` | Anthocyanes intenses | — | ▫️ — | Seul : coloration végétative modérée. En combinaison : peau violette franche (Indigo Rose, Sun Black) | Le programme « bleue » exige 1 copie de Aft ET l'homozygotie atv/atv. |
| `Cu × c / tf / e / rg` | Croisements NON publiés à tester | — | ▫️ — | Cu × c : pompon conservé, folioles simplifiées. Cu × tf : on attend l'épistasie de tf. Cu × e : pompons à limbe continu. Cu × rg : additifs → pompon gaufré. Cu × Me : quasi impossible (loci liés) | À confirmer expérimentalement. Marquer explicitement comme hypothèse dans votre carnet. |

<details>
<summary>🔬 Biochimie, nature de la mutation, origine de l'allèle (16 loci)</summary>

| Symbole | Nature de la mutation / fonction moléculaire | Origine de l'allèle | Dominance | Chr. |
|:--|:--|:--|:--:|:--:|
| `c + gob` | C (MYB BL) et GOB (NAC) agissent dans des voies partiellement INDÉPENDANTES | Berger et al. 2009 (publié) | — | — |
| `e + La` | E (auxine) et LA (TCP/GA) agissent en voies parallèles | Publié (Shleizer-Burko/Ori 2012) | — | — |
| `tf + Me/+ ; tf + clau ; tf + bip` | Tf est NÉCESSAIRE à l'activité de KNOX-I : l'expression aberrante de LeT6/TKn2 ne suffit pas à créer des folioles dans la partie basale | Naz et al. 2013 (PNAS) | — | — |
| `35S:Kn1 + c / tf / e` | Démonstration que KNOX = ramification, et non établissement du patron | Hareven et al. 1996 (Cell) | — | — |
| `La + tout` | La bloque l'activité méristématique de tous les méristèmes aériens | Hareven et al. 1996 | — | — |
| `miR319 / miR164` | GOB agit À L'INTÉRIEUR de la fenêtre ouverte par LA/TCP4 : la fenêtre ouvre/ferme, GOB découpe | Ori 2007 ; Israeli 2021 | — | — |
| `SlMP (SlARF5) + Gob-4d` | SlARF5/SlMP promeut la foliole ; effet partiellement ADDITIF avec GOB | Israeli et al. 2021 | — | — |
| `j + s` | Épistasie de j (MADS-box) sur s (WOX) | Publié | — | — |
| `sp + sft` | Effet de dosage du florigène (SFT) contre l'antiflorigène (SP) | Kimura/Pnueli | — | — |
| `d + sp (+ mnt)` | Combinaison de trois récessifs indépendants | Cultivé (Micro-Tom) | — | — |
| `clau + lyr` | Voies différentes, convergence | Publié | — | — |
| `SUN + LC + FAS` | Trois loci, deux axes (proximo-distal × médio-latéral) | Rodríguez 2011 ; van der Knaap | — | — |
| `t + r` | Kachanovsky 2012 | Publié | — | — |
| `Cnr + rin/nor` | Épimutation dominante vs récessifs | Wang 2020 / Manning 2006 | — | — |
| `Aft/Abg + atv` | Aft/Abg dominants + atv récessif | Fenstemaker et al. 2022 (Plant Direct) | — | — |
| `Cu × c / tf / e / rg` | [extrapolation] — aucune publication sur Cu en double mutant | Vos notes Cu/Stick | — | — |

</details>

> **Règle de combinaison.** Les gènes d'un *même module* ne s'additionnent pas (`Cu`, `Me`, `Pts`, `bip`, `clau`, *35S:Kn1* passent tous par KNOX : les doubler sature le module). Les gènes de *modules différents* se combinent de façon prévisible et additive (`slmp Gob-4d/+`, `e La-2`, `tf + Me/+`). Hiérarchie du patron de base : **`La` > `tf` > KNOX / GOB > `e`**.

## Prédire la couleur du fruit

| Couleur finale du fruit | Génome chair | Génome peau | Variétés de référence |
|:--|:--:|:--:|:--|
| **Rouge vif classique** | `R_` | `Y_` | Saint-Pierre, Mountain Vineyard |
| **Rose** | `R_` | `yy` | Rose de Berne, Brandywine |
| **Orange mandarine** | `tt` | `Y_` | Tangerine, Sungold |
| **Orange pastel / saumon** | `tt` | `yy` | Orange Fleshed Purple Smudge |
| **Jaune doré** | `rr` | `Y_` | Yellow Pear, Taxi |
| **Blanc / ivoire** | `rr` | `yy` | Great White, Blanche de Prusse |
| **Brun chocolat / noir** | `R_` + `gf/gf` | `Y_` | Noire de Crimée, Black Cherry |
| **Pourpre / violet sombre** | `R_` + `gf/gf` | `yy` | Cherokee Purple |
| **Vert à maturité** | `rr` + `gf/gf` | `Y_` ou `yy` | Green Zebra, Aunt Ruby's Green Drago |
| **Bleu indigo profond** | `Aft_` + `atv/atv` | variable | Indigo Rose, Black Beauty |

En combinant `PSY1` + `SGR1` + `SlMYB12`, on prédit **8 phénotypes** distincts : chaque locus ségrége en 1:2:1 et n'agit qu'à l'homozygotie pour son allèle mutant ([Baek et al. 2025](https://www.kspbtjpb.org/journal/view.html?doi=10.5010%2FJPB.2025.52.019.163)).

## Calculer la taille de sa descendance

Pour combiner **k gènes récessifs indépendants** avec 95 % de certitude :

```
N ≥ ln(0,05) / ln(1 − 0,25^k)
```

| k | Probabilité par plant en F2 | Plants pour 95 % | Plants pour 99 % | Objectif typique |
|:--:|:--:|:--:|:--:|:--|
| **1** | 0,25^1 = 25,0 % | **11** | 17 | port déterminé (`sp/sp`) ou nain (`d/d`) |
| **2** | 0,25^2 = 6,25 % | **47** | 72 | `br` + `style2.1` · `d` + `sp` (Micro-Tom) |
| **3** | 0,25^3 = 1,562 % | **191** | 293 | nain + déterminé + sans pédoncule (`d sp j-2`) |
| **4** | 0,25^4 = 0,391 % | **766** | 1177 | + potato leaf (`c`) ou + `gf` |
| **5** | 0,25^5 = 0,098 % | **3067** | 4714 | « cerise naine déterminée rose sans calice » |
| **6** | 0,25^6 = 0,024 % | **12270** | 18861 | programme long terme : à diviser en deux lignées |

En dessous de cet effectif, vous ne *cherchez* pas le génotype : vous le laissez passer. Astuce : 4 récessifs = 766 plants en vrac, mais **deux lignées à 2 récessifs (47 + 47) croisées entre elles** puis une F2 triée à nouveau coûtent dix fois moins cher en place et en temps.

## Les 10 règles d'or

- **1. Un caractère DOMINANT s'exprime dès la F1** — `SUN` (allongé), `Y` (peau jaune), `R`/`PSY1` (chair rouge), `B` (β-carotène), `Aft` (anthocyanes), `Ip`, `Del`, `Nr`, `Gr`, `Cnr`, `fw11.3`, `Wf-1` (trichomes IV), `Ty-2`, `Ol-1`, `I`, `I-2`, `Ve`, `Pto`, `Mi-1`. **Un seul parent donneur suffit**, et l'hybride F1 est déjà commercialisable pour ce caractère.
- **2. Un caractère RÉCESSIF exige deux copies** — `d`, `br`, `sp`, `mnt`, `Style2.1` (pistil inclus), `j-2`, `ovate`, `fas`, `fs8.1`, `globe`, `eno`, `y` (rose), `r` (jaune), `t` (orange), `og`, `gf`, `u`, `gs`, `rin`, `nor`, `alc`, `c` (potato leaf), `e`, `gob`, `tf`, `bip`, `hp-1/hp-2`, `rx-1/2/3`, `ol-2`, `gorky`, `SlCDPK27` (haut sucre). Il **disparaît en F1** et **réapparaît chez 25 % des plants en F2** (par caractère).
- **3. Semi-dominants : l'hétérozygote a un prix** — `La` (létal à l'homozygotie), `erl`, `sft` (port semi-déterminé), `Nr`, `Tm-1`, `B/Cyc-B`, `Ph-2`, `Ph-3`, `Xv3`, `LIN5`, `On-9^l_che`, `SUN`, `lc`, `fw2.2`. Pour eux, le **niveau** de résistance, de compacité ou de sucre diffère entre la F1 et la lignée fixée : mesurez vos deux états, ne supposez jamais.
- **4. Surdominance : gardez l'hétérozygote** — `TomLoxC` (arôme) — l'hétérozygote (allèle rare + allèle commun) **exprime plus que les deux homozygotes** : ici fixer à l'homozygotie serait une erreur. Cas analogue, en négatif : les hétérozygotes `rin/+`, `nor/+`, `alc/+` donnent la conservation sans casser le fruit.
- **5. Épistasie : certains gènes écrasent les autres** — `j` ≻ `s` ; `La` ≻ toutes les mutations de forme foliaire ; `tf` ≻ `clau`/`bip`/`Me` ; `SUN` ≻ `LC` (mais `SUN`+`LC`+`FAS` = cœur de bœuf) ; `Cnr` ≻ `rin` ≈ `nor` ; `t` ≻ `r^2997` ; `j-2` × `ej2` = épistasie négative. **Un gène du même module ne s'additionne pas** (Cu+Me+bip+clau = saturation, souvent invivable) ; **les gènes de modules différents se combinent de façon prévisible.**
- **6. Le piège du rétrocroisement** — Ne rétrocroisez JAMAIS vers un parent sauvage après avoir introduit des gènes domestiques récessifs (`br`, `Style2.1`, `j-2`, `gf`, `u`…) : vous les écrasez à chaque BC. Procédez par **autofécondation en F2 avec tri généalogique**, ou par **rétrocroisement assisté par marqueurs (MABC)** en génotypant aussi les loci récessifs à conserver — pas seulement le gène cible.
- **7. Le linkage drag est la vraie difficulté** — `Ty-2` traîne une inversion de ~300 kb (chr 11) ; les Galápagos traînent des inversions de 18–21 Mb (chr 5), 7,4 Mb (chr 8), 16–17 Mb (chr 11) ; l'allèle haut-sucre de `SlCDPK27` a été perdu car lié au locus de poids `fw11.3`. **Prévoyez des populations fines et des marqueurs denses** pour casser ces liaisons : 2 à 4 générations.
- **8. Pensez d/a, pas « dominant »** — Pour tout caractère quantitatif, calculez **d/a = (2·F1 − P1 − P2) / (P1 − P2)**. 0 = additif, ±1 = dominance complète, |d/a| > 1 = surdominance. ⚠ **d/a n'est pas une constante du locus** : il change avec le couple de parents ET avec le caractère mesuré (`fs8.1` : −0,47 pour la forme, +1,14 pour le poids).
- **9. Le phénotype n'est pas que le génotype** — Hétéroblastie : le même plant change de feuille le long de la tige (miR156/SPL → miR319/TCP → CUC). Comparez toujours **le même rang de feuille** (ex. n° 6–8), au même stade, dans les mêmes conditions. De même, le Brix dépend de l'irrigation, du potassium, de l'éclairement et du stade de récolte : un °Brix de catalogue n'est pas un génotype.
- **10. Les défauts sont dans le paquet** — `u` = −10 à −20 % de sucres et de caroténoïdes ; `Cnr` = péricarpe farineux ; `Ip` = fruit plus petit ; `fw3.2` = maturation retardée ; `rin`/`nor` = arôme détruit ; vitamine C ×5 = stérilité pollinique ; GABA multiplex = nanisme et quasi-stérilité. **Cherchez toujours le coût physiologique avant d'écrire « variété ».**

Trois réflexes résument toute la fiche. **(1)** Regardez d'abord la **nature de la mutation** : une perte de fonction (codon stop, délétion, frameshift) sera récessive, un gain de fonction (duplication, promoteur, surexpression) sera dominant ou semi-dominant — cette règle prédit le mode de dominance mieux que n'importe quel tableau. **(2)** Comptez les **récessifs** de votre objectif : c'est ce nombre, et lui seul, qui décide de la surface que vous devez semer. **(3)** Ne cherchez jamais un allèle sauvage **sans son ticket de sortie** : chaque introgression arrive avec son segment voisin (inversions, `fw11.3`, petits fruits), et la seule monnaie qui paie ce nettoyage, ce sont les marqueurs.

## Marqueurs et génotypage

| Locus | Type de marqueur | Ce qu'il révèle |
|:--|:--|:--|
| `SlMYB12` (`y`) | Marqueur CAPS / InDel | rose (yy) vs rouge (Y_) + flavonols — 1:2:1 |
| `SGR1` (`gf`) | Marqueur basé gène | brun/vert à maturité — homozygotie requise |
| `PSY1` (`r`) | Marqueur basé gène | chair jaune vs rouge |
| `SlGLK2` (`u`) | InDel / CAPS | mûrissement uniforme + coût en sucres |
| `LC`, `FAS` | Marqueurs liés aux inversion/SNP | nombre de loges, aplatissement, poids |
| `B`/`og` (CYC-B) | Haplotypes du promoteur | β-carotène vs lycopène (même locus !) |
| `OVATE` | CAPS (codon stop) | forme poire/ovale |
| `Lin5` (Brix9-2-5) | SNP Asn366Asp | Brix — une copie suffit |
| `SlCDPK27` | PCR de l'insertion de 12 pb | haut sucre (récessif, chr 11) |
| `SlSPS1` | InDel 1 pb AG/A du promoteur | Brix sans pénalité de calibre |
| `STP1` | InDel 21 pb du promoteur | Brix (allèle déjà dans le cultivé) |
| `SlALMT9` | InDel 3 pb (boîte W) | acidité malique |
| `TFA9`/`SlbHLH59` | InDel 8 pb | vitamine C (15,9 % de la variance) |
| `TomLoxC` | Marqueur du variant structural | arôme — viser l'HÉTÉROZYGOTE |
| `GORKY` | Délétion | amertume / α-tomatine du fruit mûr |
| `GAME9`, `GE1` | Haplotypes | teneur en glycoalcaloïdes |
| `VTE3(1)` | **épi-marqueur** (méthylation) | vitamine E — l'ADN ne suffit pas |
| `Ph-3` | Marqueur co-dominant Ph-3-GLR/S | mildiou |
| `Ty-2` | Marqueur spécifique (2020) | TYLCV |
| `j-2` | Marqueurs (SlMBP21) | pédoncule sans coude |
| `br`, `sp`, `d` | Marqueurs MAS publiés | port compact / déterminé / nain |
| Trichomes type IV | **Phénotypage à la loupe** | résistance aleurodes (Wf-1) — pas de marqueur grand public |

Tous sont des PCR sur amplicon court (30–400 pb) depuis une disquette ou un fragment de feuille de 2 cm ; pour les InDel, un gel suffit, sans séquenceur.

## Pièges et corrections apportées

### 13 confusions classiques

- **`Cu` (Curl, dominant)** n'a rien à voir avec **`cu-3` (curl-3, récessif, récepteur des brassinostéroïdes)** ni avec `cu`/`cu-2` (curled) ni avec le virus « leaf curl » (TYLCV, gènes `Ty`).
- **`c`** = *potato leaf* (récessif) ; **`C`** = l'allèle sauvage dominant (regular leaf). Le même lettre, deux sens opposés.
- **`e` (entire)** est RÉCESSIF (perte de fonction de *SlIAA9*) malgré son nom qui évoque un dominant.
- **`FAS` n'est pas `SlYABBY2b`** (hypothèse de 2008) mais **`SlCLV3`** (inversion de 294 kb). Et `fw11.3` (`CSR`) est un locus **distinct, 45 kb en aval** : les confondre fait perdre des saisons.
- **`B` et `og`/`og^c` sont ALLÉLIQUES** (même gène `CYC-B`) : on ne cumule pas un allèle nul et un allèle surexprimé.
- **`alc` est un allèle de `NAC-NOR`**, pas un gène séparé. `nor` et `alc` s'utilisent en hétérozygotes.
- **`Ip` n'est pas un `hp`** : `Ip` est dominant, `hp-1`/`hp-2`/`dg` sont récessifs.
- **`ol-2` (`Slmlo1`, chr 4)** ne vient pas de *S. habrochaites* mais de *S. lycopersicum* var. *cerasiforme* LA1230.
- **Le port (`sp`) et la taille (`d`, `br`, `mnt`) sont indépendants** : on peut être déterminé et grand, ou nain et indéterminé.
- **`sft` n'est pas un monogénique simple 3:1** pour l'architecture : l'hétérozygote a un phénotype mesurable (dosage).
- **`j` (chr 11) et `j-2` (chr 12) ne sont PAS alléliques** : le phénotype « sans coude » peut venir de l'un ou de l'autre, et seul `j` casse la ramification de la grappe (épistasie sur `s`) et traîne un excès de feuillage — d'où la préférence pour `j-2` en sélection.
- **`style2.1`/`se2.1` (chr 2) n'est pas le seul verrou** : `SE3.1` (chr 3) et `SlSE2.2` (chr 2) modulent le degré d'exsertion, et `SlLst` (chr 12) fait déborder le style au-dessus de 27 °C. La pureté variétale est donc aussi climatique.
- **`gob` vs `Gob-4d`** : le premier est récessif (moins de folioles), le second est semi-dominant (lobes plus profonds) : même gène, effets opposés selon l'allèle.

### Corrections apportées aux synthèses antérieures

Ces affirmations ont été re-vérifiées ; les tableaux ci-dessus portent la valeur corrigée.

| Point | Souvent indiqué | État vérifié | Source |
|:--|:--|:--|:--|
| `Y` (*SlMYB12*, peau jaune / fruit rose) | chromosome 6 | **chromosome 1** | Clonage et cartographie : Ballester et al. 2010 ; le locus `y` est sur le chr 1 des cartes classiques. |
| Résistance au **ToBRFV** | « gène récessif de *S. pimpinellifolium*, chr 11 » | **Tm-1 (chr 2, semi-dominant) + locus récessif de tolérance chr 11** ; la résistance franche demande ≥ 2 gènes | Zinger et al. 2025 (PLOS Genet.) ; Jaiswal et al. 2025 (TAG 138:190) — QTL majeur chr 11 à ~46,84 Mb chez *S. pimpinellifolium* USVL332 (PI 390717), candidats Solyc11g062150 / Solyc11g062180 ; Zois et al. 2025 (allèle de *S. pennellii*). |
| **`On-9`** (oïdium, *S. cheesmaniae*) | « DOMINANT » | **dominance partielle (QTL)** | RechercheSquare 2026 : `On-9^l_che`, chr 9, 46,5–50,5 cM, pic à 48 cM, 14,6 % de la variance, ~40 % de l'écart entre parents. |
| **`Ph-1`** | chromosome 4 | **chromosome 7** ; résistance à la race T0 seulement | Gallegly & Marvel 1955 ; Peirce 1971 ; rappelé dans Wang et al. 2016 (Plant Breeding) et Springer 2025. |
| `SUN` | « DOMINANT (gain de fonction) » | **semi-dominant / dosage** (F1 intermédiaire, d/a ≈ −0,39) | Xiao et al. 2008 (Science) ; Clevenger et al. 2011. C'est une mutation RÉGULATRICE, donc dosée, pas un dominant franc. |
| **`style2.1`** | « pistil inséré = récessif » (sans précision) | confirmé : `se2.1` récessif, gène **Style2.1 = Solyc02g087860** (motif HLH), délétions promotrices StyleD1/StyleD2 | Chen et al. 2007 ; Riccini et al. 2025 (BMC Plant Biol.) — l'allèle est fixé chez le cultivé. |

**Statut des clones récents.** `FS8.1` (2023), `globe` (2021), `ENO` (2020), `PT` (2022), `SlOFP20` (2018), `SlSE2.2` (2025) : la dominance y est estimée sur peu de fonds génétiques. À confirmer sur votre population.

## Protocole de programme

**Étape 0 — Définir la cible et son mode de dominance**  
Écrivez le génotype visé en symboles (ex. `d/d sp/sp Y/y gf/gf Style2.1/Style2.1`). Comptez les récessifs : c'est le nombre **k** qui fixe la taille de votre descendance, pas l'ambition du projet.

**Étape 1 — Dimensionner la F2**  
Appliquez la formule N ≥ ln(0,05)/ln(1 − 0,25^k). 2 récessifs = **47 plants**, 3 = **191**, 4 = **766**. En dessous, vous ne « cherchez » pas le génotype, vous le laissez passer.

**Étape 2 — Choisir le sens du croisement**  
Avec *S. habrochaites*, *S. pennellii* ou *S. chilense*, utilisez-les en **parent MÂLE** : en sens inverse, l'incompatibilité unilatérale fait rejeter le pollen du cultivé. Avec *S. pimpinellifolium*, *cheesmaniae*, *galapagense* : les deux sens marchent.

**Étape 3 — Isoler, vraiment**  
L'autogamie n'est fiable que si le style est inclus (`Style2.1/Style2.1`). Sous canicule (> 27 °C, gène `SlLst`) ou avec du sauvage à style exserté, le taux d'hybridation monte : poches organza, isolateur, distance, ou émasculation + pollen contrôlé.

**Étape 4 — Marquer plutôt que d'attendre**  
Pour les récessifs masqués en hétérozygote (`fas`, `gf`, `y`, `ovate`, `SlCDPK27`, `ol-2`, `rx`, `u`), un marqueur sur semis (AMP / leaf punch) remplace 2 ans de phénotypage. Les locus à InDel court (3–21 pb) se génotypent en PCR simple, sans séquenceur.

**Étape 5 — Casser le drag, puis fixer**  
2 à 4 rétrocroisements assistés si vous venez du sauvage (sélectionnez le gène cible ET le fond cultivé aux loci utiles). Puis autofécondation jusqu'à F5–F6 avec tri généalogique pour fixer.

**Étape 6 — Valider en dégustation, pas au réfractomètre seul**  
Certains volatils augmentent la DOUCEUR PERÇUE sans changer le Brix : le sucre mesuré ≠ le sucre goûté. Panel à l'aveugle, 5–10 fruits par descendance, au même stade de maturité.

## Reproductibilité du dépôt

Ce dépôt est **volontairement plat** : sept fichiers, pas de dossier de données, pas de script. Les tableaux du présent fichier sont **la source de vérité** ; `README.en.md` en est le reflet anglais et `index.html` le pendant interactif. Rien n'est régénéré : une correction s'écrit à la main dans le fichier concerné et se propage dans les deux autres dès qu'elle touche au `Symbole`, au `Chr.` ou à la `Dominance` — les trois colonnes qui engagent une affirmation génétique.

```
tomato-genetics-cheatsheet/
├── README.md          ← cette fiche : LA référence (216 loci, 16 chapitres + bloc moléculaire dépliable)
├── README.en.md       ← édition anglaise : mêmes loci, mêmes chr., mêmes dominance, sans la couche moléculaire
├── SOURCES.md         ← bibliographie commune aux deux langues (228 entrées, liens, niveau de vérification)
├── TETRAPLOIDIE.md    ← annexe ploïdie (40 sources, niveau de preuve et limites affichés) — rédigée en français
├── index.html         ← version interactive autonome : recherche, filtres, calculateur F2, impression A4 paysage
├── CONTRIBUTING.md    ← format d'une ligne, règles de parité FR ↔ EN, critères d'acceptation
└── LICENSE            ← MIT (texte et données)
```

### Qui doit bouger ensemble

| Fichier | Contenu par locus | Règle de propagation |
|:--|:--|:--|
| `README.md` | tableau principal (6 colonnes) **et** bloc `<details>` : nature de la mutation, origine de l'allèle, dominance, chr. | c'est ici que l'affirmation est écrite en entier |
| `README.en.md` | tableau principal seul (6 colonnes) | la traduction ne touche que le texte ; `Symbole`, `Chr.` et `Dominance` se recopient à l'identique |
| `index.html` | une ligne `<tr data-dom="…" data-t="…">` par locus, 8 colonnes | mêmes chromosomes et mêmes codes que le FR ; `data-t` porte le texte indexé, en minuscules |

Un locus = **une ligne par fichier**, jamais une ligne par variété. Une ligne descriptive (QTL non cloné, germoplasme, épistasie) garde une dominance `—` : elle n'est pas mendélienne.

### Contrôler la cohérence en trois commandes

Rien à installer : `grep`, `awk` et `python3` du système suffisent, lancés à la racine du dépôt.
Le contrôle n° 3 passe en revue **tous** les fichiers markdown, annexe de la ploïdie comprise.

```bash
# 1. le compte annoncé par chapitre doit sommer à 216 dans les deux langues
for f in README.md README.en.md; do
  printf '%s : ' "$f"
  grep -oE '\*\*[0-9]+ loci\*\*' "$f" | tr -dc '0-9\n' | awk '{s+=$1} END {print s}'
done

# 2. le site interactif doit porter le même nombre de loci
grep -o '<tr data-dom=' index.html | wc -l  # → 216 lignes de loci (une ligne HTML en porte beaucoup)

# 3. plus aucune référence à un fichier ou à une ancre inexistante
python3 - <<'PY'
import re, os, glob
for fn in sorted(glob.glob("*.md")):          # tous les markdown, annexe comprise
    s = open(fn, encoding="utf-8").read()
    heads = {re.sub(r'[^\w \-]', '', h.lower().replace('&amp;', '&')).replace(' ', '-')
             for h in re.findall(r'^#{2,4}\s+(.*)$', s, re.M)}
    dead  = sorted({l for l in re.findall(r'\]\(#([^)]+)\)', s) if l not in heads})
    files = sorted({l for l in re.findall(r'\]\((?!#|https?:|mailto:)([^)]+)\)', s)})
    miss  = [f for f in files if not os.path.exists(f.split('#')[0].replace('%20', ' '))]
    print(fn, "->", len(heads), "titres ; ancres cassées :", dead or "aucune",
          "; fichiers absents :", miss or "aucun")
PY
```

Tout doit converger : **216 · 216 · 216**, puis `aucune` et `aucun`. Un chapitre modifié en FR sans l'être en EN fait échouer la commande 1 ; une ligne ajoutée au FR sans son reflet dans `index.html` fait échouer la commande 2.

### Publier la version interactive (2 minutes)

`index.html` est à la racine : **Settings → Pages → Source : Deploy from a branch**, branche `main`, dossier **`/` (racine)**. Le site répond alors sur `https://<utilisateur>.github.io/<nom-du-depot>/` — une page unique, sans build, sans dépendance réseau, qui garde la recherche, les filtres et l'impression A4 paysage. Aucun `.nojekyll` n'est nécessaire : il n'y a à la racine ni fichier ni dossier commençant par `_`.

### Le jour où vous voudrez industrialiser

Si la fiche dépasse ce qu'on relit à l'œil (plus de loci, exports CSV/XLSX, traductions tenues par un tiers), reprenez l'ordre inverse : extrayez les tableaux de `README.md` vers un fichier de données (TSV, un champ par colonne), générez le README et le HTML depuis ce fichier, et faites échouer le build dès qu'un chromosome ou une dominance diverge entre les deux langues. Le format s'y prête déjà : chaque ligne est autonome et les trois colonnes génétiques sont les mêmes dans les trois fichiers.

## Sources, licence et citation

- **Bibliographie** : [SOURCES.md](SOURCES.md) — 228 références par thème avec liens et niveau de vérification, plus les ressources de matériel végétal (TGRC, SGN, TOMATOMA, bibliothèques d'IL).
- **Annexe** : [TETRAPLOIDIE.md](TETRAPLOIDIE.md) — tétraploïdisation, dosage tétrasomique des loci et voie « sans pépins » ; sans équivalent anglais, comme la bibliographie.
- **Traçabilité** : la colonne *Origine de l'allèle* de chaque chapitre (bloc dépliable) indique l'espèce, l'accession ou le mutant d'origine ; les références complètes sont dans [SOURCES.md](SOURCES.md) ; ce qui n'est pas publié est marqué **[extrapolation]**.
- **Licence** : [MIT](LICENSE) — réutilisez, adaptez, redistribuez, y compris commercialement, en conservant la mention de copyright.
- **Citation** : pas de `CITATION.cff` dans ce dépôt. Citez *Fiche génétique de la tomate*, Tivaphe/tomato-genetics-cheatsheet, édition du 15/10/2026, avec l'URL ; si vous voulez une référence stable, créez un DOI Zenodo et ajoutez-y le fichier.

<sub>Fiche consolidée le 15/10/2026 à partir de huit dossiers de recherche documentaire. Ce dépôt est un outil de travail, pas une autorité : en sélection, la seule autorité reste votre F2.</sub>
