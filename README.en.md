# Tomato genetics sheet 🍅

![🇬🇧 English — this edition](https://img.shields.io/badge/%F0%9F%87%AC%F0%9F%87%A7_English-this_edition-64748b?style=for-the-badge)  [![🇫🇷 Français — → read the reference edition (French)](https://img.shields.io/badge/%F0%9F%87%AB%F0%9F%87%B7_Fran%C3%A7ais-%E2%86%92_read_the_reference_edition_%28French%29-0b6e4f?style=for-the-badge)](README.md)

**216 loci documented — plant architecture, foliage, fruit, flavour, nutrition and resistance genes, each with its mode of dominance and what it changes in a cross.**

[![loci](https://img.shields.io/badge/loci-216-0b6e4f?style=flat-square)](data/genes_tomate.csv) [![chapters](https://img.shields.io/badge/chapters-16-1d4ed8?style=flat-square)](#table-of-contents) [![interactive version](https://img.shields.io/badge/interactive%20version-docs%2Findex.html-6d28d9?style=flat-square)](docs/index.html) [![licence](https://img.shields.io/badge/licence-CC%20BY%204.0-f59e0b?style=flat-square)](LICENSE) [![updated](https://img.shields.io/badge/updated-15%2F10%202026-64748b?style=flat-square)](CHANGELOG.md)

> **Two editions, one genetics.** The button above opens the [French edition](README.md) — the reference one: same loci, same chromosomes, same dominance codes (the build fails if the two ever diverge). The molecular layer, the accessions and the filterable exports live there and in `data/`.

> **Who is this for?** Advanced amateur breeders, market gardeners, students and plant-breeding researchers. Every row answers three questions: *which gene, on which chromosome, dominant or recessive* — and therefore: *do I see it in the F1, or do I have to sow 200 plants*.

`216 loci` · `16 chapters` · literature checked through 2026 · claims that are not published are explicitly marked **[extrapolation]**.

## The essentials in 12 points

1. The **wild** tomato phenotype is round, red, yellow-matte skinned, indeterminate, with compound leaves and normal vigour: almost every mutant allele used by breeders is therefore **recessive** (loss of function).
2. **The best predictor of dominance is not the phenotype but the nature of the mutation**: gain of function (duplication, promoter, overexpression) ⇒ dominant or semi-dominant; loss of function (stop codon, deletion, frameshift) ⇒ recessive.
3. **Determinate habit is recessive** (`sp/sp`): contrary to a widespread belief, indeterminacy dominates, because `SP` is an antiflorigene and one functional copy is enough.
4. Fruit shape is read on **two independent axes** (length: `SUN`, `OVATE`, `FS8.1`, `PT`; locules/flattening: `LC`, `FAS`, `ENO`, `globe`) plus a third one for mass (`fw2.2`, `fw3.2`, `fw11.3`).
5. Colour = **three stackable layers**: flesh carotenoids (`r`, `t`, `B`, `og`) × skin flavonols (`Y`/`y`) × residual chlorophyll (`gf`, `u`). Three genes in homozygosity are enough to get an entirely green fruit.
6. **Pink is not a flesh colour**: it is a red fruit `R_` seen through skin **devoid of flavonols** (`y/y`, *SlMYB12*, chr 1) — and therefore also stripped of part of its nutritional value.
7. **Flavour is a five-piece puzzle** (sugars, acids, ~15 key volatiles, free amino acids including glutamate, bitterness): selecting on °Brix alone is not enough, because some volatiles raise *perceived* sweetness without changing measured sugar.
8. **`TomLoxC` is over-dominant**: the heterozygote expresses more aroma than either homozygote. That is the strong genetic argument for evaluating — and sometimes selling — **F1s** rather than pure lines for this trait.
9. **Keeping quality and aroma are controlled by the same regulators** (`RIN`, `NOR`, `FUL1/2`): blocking ripening (`rin`, `nor`, `Cnr`) destroys the perfume as well. The trade-off is genetic, not bad luck.
10. Almost every allele of taste or nutritional interest was **lost during domestication** (rare `TomLoxC`, high-sugar `SlCDPK27`, strong `DXR` alleles, `GAME9`/`GE1`): recovering them takes introgression from wild relatives or targeted editing (CRISPR).
11. In the **Galápagos** species (*cheesmaniae*, *galapagense*) and in *habrochaites*, introgressions have to cross **chromosomal inversions** (up to 18–21 Mb): recombination is blocked there, linkage drag is structural — plan fine mapping populations.
12. Dominance **is not a constant of the locus**: `d/a` changes with the parent pair and with the trait measured (`fs8.1`: −0.47 for shape, +1.14 for weight). Every value in this repository is an *informed guess to check on your own population*, never a law.

## How to read this sheet

One row = one locus. The **Dominance** column is the piece of information that decides the whole crossing protocol:

| | Mode of dominance | Meaning | Practical consequence |
|:--|:--|:--|:--|
| 🟢 | **DOMINANT** | Expressed in the F1: one donor parent is enough. | One donor parent is enough: the trait is already there in the F1, so it pays off in a hybrid too. |
| 🟡 | **SEMI-DOMINANT** | Heterozygote is intermediate: a dosage effect. | The heterozygote is intermediate: a marker (or an F2 measurement) is the only way to know what you actually have. |
| 🔵 | **RECESSIVE** | Two copies needed: fix it homozygous (25% in the F2). | Screen the F2 (25% per trait) or co-dominant-marker seedlings; fix the line before judging the fruit. |
| 🟣 | **QTL / ADDITIVE** | Quantitative trait: marker-assisted or genomic selection. | No single-gene screening possible: gain ground by stacking QTL, repeated phenotyping across years and sites, or genomic selection. |
| 🟠 | **OVER-DOMINANCE** | The heterozygote outperforms both homozygotes (heterosis). | Do NOT fix it: the optimum state is the heterozygote. Evaluate your F1s, not your inbreds. |
| ⚫ | **EPIGENETIC** | DNA methylation: outside Mendelian dominance, the sequence does not tell all. | The DNA genotype can lie: plan direct phenotyping or an epimarker (methylation). |
| ⚪ | **MIXED / BACKGROUND** | Dominance changes with the genetic background or the trait measured. | Measure dominance in YOUR population: a published value belongs to somebody else's background. |

**Notation.** `R_` = at least one *R* allele (dominant expressed) · `yy` and `gf/gf` = recessive homozygote · `Sp/sp` = heterozygote — with semi-dominants, that is where the *level* of expression (habit, resistance, Brix) is decided. `n.d.` = the locus is not finely mapped in the sources compiled here: **do not invent it**. `Chr.` = chromosome of the SL4.0 (ITAG 4.0) map. `—` in the Dominance column marks a germplasm row or an epistatic combination, not a Mendelian locus; a qualified label (`Q (additive)`, `RECESSIVE → SEMI-DOMINANT`) carries over the precision written in the input file.

The loci are arranged in **16 chapters**: plant (habit, foliage, trichomes, pigmentation, flower), fruit (shape, colour, ripening), flavour (sugars, acids, volatiles), nutrition, biotic resistance, abiotic tolerance, allelic sources and epistasis. This edition keeps the breeder-facing columns; the molecular layer (mutation nature, allele origin, accessions) and the filterable exports live in [`data/genes_tomate.csv`](data/genes_tomate.csv) and in the French edition [`README.md`](README.md). [`docs/index.html`](docs/index.html) is a self-contained searchable page (no network dependency) with full-text search, dominance filters, an F2 population calculator and A4 landscape print style.

## Table of contents

- [1. Plant architecture & inflorescence](#1-plant-architecture--inflorescence) — *29 loci*
- [2. Foliage — leaf shape](#2-foliage--leaf-shape) — *15 loci*
- [3. Trichomes & pubescence](#3-trichomes--pubescence) — *6 loci*
- [4. Foliage — colour & pigmentation](#4-foliage--colour--pigmentation) — *12 loci*
- [5. Flower, selfing & fruit set](#5-flower-selfing--fruit-set) — *5 loci*
- [6. Fruit shape, locule number & weight](#6-fruit-shape-locule-number--weight) — *16 loci*
- [7. Fruit colour (skin × flesh)](#predicting-fruit-colour) — *12 loci*
- [8. Fruit ripening & storage](#8-fruit-ripening--storage) — *5 loci*
- [9. Flavour — sugars & soluble solids](#9-flavour--sugars--soluble-solids) — *13 loci*
- [10. Flavour — acidity, umami & GABA](#10-flavour--acidity-umami--gaba) — *8 loci*
- [11. Flavour — volatiles & aroma](#11-flavour--volatiles--aroma) — *17 loci*
- [12. Nutrition & safety](#12-nutrition--safety) — *17 loci*
- [13. Biotic resistances](#13-biotic-resistances) — *27 loci*
- [14. Abiotic tolerances & roots](#14-abiotic-tolerances--roots) — *11 loci*
- [15. Allele sources: your germplasm](#sources-licence-and-citation) — *7 loci*
- [16. Combinations & epistasis](#16-combinations--epistasis) — *16 loci*
- [Predicting fruit colour](#predicting-fruit-colour)
- [Sizing your progeny](#sizing-your-progeny)
- [The 10 golden rules](#the-10-golden-rules)
- [Markers and genotyping](#markers-and-genotyping)
- [Pitfalls and corrections](#pitfalls-and-corrections)
- [Programme protocol](#programme-protocol)
- [Reproducibility](#reproducibility)
- [Sources, licence and citation](#sources-licence-and-citation)
- [SOURCES.md](SOURCES.md) — full bibliography (references are language-neutral) · [CONTRIBUTING.md](CONTRIBUTING.md) · [CITATION.cff](CITATION.cff) · [LICENSE](LICENSE)

---

## 1. Plant architecture & inflorescence

*Determination, branching, size, truss organogenesis — the SP/SFT switch* — **29 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `sp` | Self-pruning (SP) | 6 | 🔵 RECESSIVE | Determinate habit: shoot ends after 1–2 inflorescences, synchronous ripening | F1 SP/sp stays indeterminate; 25% determinate in F2. Keep SP for a plant that keeps growing. |
| `sft` | Single flower truss | n.d. | 🟡 SEMI-DOMINANT | Trusses of 1–3 flowers, leaves in the inflorescence, early shoot termination | Recessive but DOSE-SENSITIVE: sft/+ gives a semi-determinate plant — never treat it as a plain 3:1. |
| `sp5G` | Self-pruning 5G | n.d. | 🔵 RECESSIVE | Loss of long-day sensitivity → early flowering, more compact plant | Combine earliness with indeterminate growth. Popular in processing tomatoes. |
| `uf` | Uniflora | n.d. | 🔵 RECESSIVE | Elongated sympodia, late flowering, single-stem plant | Lab reference allele, rarely used commercially; useful to read an odd architecture. |
| `s` | Compound inflorescence | 2 | 🔵 RECESSIVE | Highly branched trusses, up to ~200 flowers ("multiflora" clusters) | `j` is epistatic to `s`: jointless removes the branching. |
| `an` | Anantha | n.d. | 🔵 RECESSIVE | Endlessly branched inflorescences, poorly differentiated flowers | Sterility costs — a genetics tool, not a breeding target. |
| `fa` | Falsiflora | n.d. | 🔵 RECESSIVE | Leafy inflorescences, flowers converted into shoots | Useful to diagnose a "leafy truss"; no commercial value. |
| `j` | Jointless | 11 | 🔵 RECESSIVE | Abscission zone absent from the pedicel; suppresses `s`; vegetative reversion of the truss | Breaks cluster branching and adds excess foliage — prefer j-2. |
| `j-2` | Jointless-2 | 12 | 🔵 RECESSIVE | Short, straight pedicel with no knuckle: fruit picks off cleanly, no calice, no wound | From S. cheesmaniae LA0166 (SlMBP21). Nearly universal in processing tomato. Negative epistasis with ej2 (chr 3). |
| `mc` | Macrocalyx | n.d. | 🔵 RECESSIVE | Enlarged calyx, modified inflorescence | MADS-box; floral genetics tool only. |
| `to` | Torosa | n.d. | 🔵 RECESSIVE | Corkscrew flowers and ovaries, erratic fruit set | Cull it in selection, never introduce it. |
| `bif` | Bifurcate flower truss | n.d. | 🔵 RECESSIVE | Branched trusses (like `s`), worsened by cold | Watch out in field programs in cool climates — easily mistaken for `s`. |
| `Nr` | Never ripe | n.d. | 🟢 DOMINANT | Delayed senescence and abscission of leaves, flowers and fruit; fruit does not ripen | SlETR3 ethylene receptor, dominant-negative: shows up in the F1. See also the ripening chapter. |
| `ls` | Lateral suppressor | n.d. | 🔵 RECESSIVE | No axillary buds: unbranched plant; sometimes fewer leaflets | No suckers at all, but early yield suffers; never adopted commercially. |
| `bl` | Blind | n.d. | 🔵 RECESSIVE | Strongly reduced branching, missing or stunted axillary buds | R2R3-MYB, same module family that dissects the leaf. |
| `slbrc1 / slbrc2` | Blind-like / BRC-like | n.d. | 🔵 RECESSIVE | Controls axillary bud dormancy (interacts with WO) | Branching genetics target; no commercial variety described as carrying it. |
| `d (dx, d-im)` | Dwarf | 2 | 🔵 RECESSIVE | Compact dwarf: short internodes, thick stem, rugose dark-green leaves | Brassinosteroid CYP85A1. Base of dwarf varieties; F1 always tall; d/d reappears in 25% of F2. Micro-Tom = d + sp (+ mnt). |
| `br` | Brachytic | 1 | 🔵 RECESSIVE | Very short internodes, sturdy stem, strong lateral branching, clustered fruit | Ideal for big fruit on a compact plant: does NOT change fruit size. MAS markers published. |
| `mnt` | Miniature | n.d. | 🔵 RECESSIVE | Extreme micro-dwarf (15–20 cm), insensitive to gibberellin | Combine with d and sp. Not cloned. |
| `dpy` | Dumpy | n.d. | 🔵 RECESSIVE | Dwarf, reduced branching, altered leaves; rescued by brassinolide spray | Diagnostic tool for the BR pathway (separates d from cu-3). |
| `cu-3` | Curl-3 | 4 | 🔵 RECESSIVE | Extreme dwarf, curled dark-green leaves, BR-insensitive | SlBRI1 receptor. ⚠ Not to be confused with Cu (Curl, dominant) or cu/cu-2. |
| `dgt` | Diageotropica | n.d. | 🔵 RECESSIVE | Diageotropic (horizontal) growth, hyponastic leaves, abnormal roots | Auxin-signalling cyclophilin; penalising in culture, useful for root genetics. |
| `pro` | Procera | n.d. | 🔵 RECESSIVE | Taller plant, elongated internodes, thin less-lobed leaves, constitutive GA response | DELLA (LeGAI). The GA-pathway counter-test: fragile stems, not a breeding target. |
| `gib-1` | Gibberellin deficient-1 | n.d. | 🔵 RECESSIVE | Dwarf, GA-dependent germination, smaller dark-green leaves | CPS. GA-responsive dwarf. |
| `gib-2` | Gibberellin deficient-2 | n.d. | 🔵 RECESSIVE | Severe dwarf | Test: a gib mutant greets and elongates after GA drench, a d plant does not. |
| `gib-3` | Gibberellin deficient-3 | n.d. | 🔵 RECESSIVE | Severe dwarf | KS step; same diagnostic logic as gib-2, versus GA insensitivity (cu-3). |
| `epi` | Epinastic | n.d. | 🔵 RECESSIVE | Strongly epinastic leaves (bent downward), thickened stems | ⚠ Do not mistake it for water stress, herbicide damage or a virus: genetic, recessive, visible from the seedling. |
| `not / fl / sit` | Notabilis / Flacca / Sitiens | n.d. | 🔵 RECESSIVE | Rolled leaves and wilting (ABA-deficient) | Water-stress mimics, stomata permanently open; avoid in breeding, use as a probe. |
| `erl` | Erectoid leaf | 10 | 🟡 SEMI-DOMINANT | Erect leaves: reduced insertion angle, upright canopy | SlTAC1-like loss of function; semi-dominant, so one copy is enough to see it. |

## 2. Foliage — leaf shape

*Regular / potato / carrot leaf: the four layers of compound-leaf control* — **15 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `c (c-2, clt, bli2)` | Cutleaf / potato leaf | 6 | 🔵 RECESSIVE | Simple leaf: continuous lamina, smooth margins, darker green | C_ = regular leaf (dominant). Potato × regular → regular F1; c/c reappears in 25% of F2. ~5% of old varieties (Brandywine…). |
| `e` | Entire | n.d. | 🔵 RECESSIVE | Leaflets with entire margins, less dissected leaf, ectopic lamina growth between leaflets | SlIAA9 loss of function — recessive despite the name. Same gene as the parthenocarpic Sliaa9 lines. |
| `La (La-2)` | Lanceolate | n.d. | 🟡 SEMI-DOMINANT | Small, simple, narrow leaves; earlier maturity | LA/TCP4 miR319-binding site mutated. EPISTATIC to every other leaf-shape mutation. La/La is embryo-lethal: never aim for the homozygote. |
| `gob (Gob-4d)` | Goblet | 7 | 🔵 RECESSIVE | Fewer leaflets, smooth margins; the Gob-4d allele (semi-dominant) does the opposite, with very deep lobes | NAC/CUC2 boundary gene, miR164 target. It is the "scissors" inside the window opened by LA. |
| `tf` | Trifoliate | 5 | 🔵 RECESSIVE | Only ~3 leaflets, fewer axillary buds | R2R3-MYB. Epistatic to clau, bip and Me/+: the trifoliate plan is kept, only the dissection of each leaflet changes. |
| `lyr` | Lyrate | 5 | 🔵 RECESSIVE | Reduced lamina growth and leaflet initiation, floral anomalies | JAGGED orthologue; lab mutant with pleiotropic floral costs. |
| `wi, wi3, wi4, wi6 (+wl)` | Wiry ("shoestring leaves") | n.d. | 🔵 RECESSIVE | Thread-like leaves without lamina, loss of dorsiventality, early flowering, extra branching | ta-siRNA pathway (RDR6, SGS3, AGO7, DCL4). Four complementation groups; not a breeding target. |
| `Me` | Mouse ear | n.d. | 🟢 DOMINANT | Heavily dissected leaves, extra leaflets and teeth, hyperactive meristems, abnormal inflorescences | TKN2/LeT6 (KNOX-I) mis-expression (PFP–TKN2 fusion). Tightly linked to Cu — never separated. |
| `Cu` | Curl | n.d. | 🟢 DOMINANT | Pom-pom foliage, "stick" stems, almost no suckers, greener fruit (more chloroplasts) | TKN2 overexpression, gain of function. ⚠ Not cu-3, not curled (cu), not Tomato leaf curl virus. |
| `Pts` | Petroselinum | n.d. | 🟡 SEMI-DOMINANT | Hyper-complex parsley-like leaves, supernumerary primary and secondary leaflets | 1-bp promoter deletion in PTS/TKD1 (atypical KNOX). Reported dominant or semi-dominant depending on the source. |
| `bip` | Bipinnata | 2 | 🔵 RECESSIVE | Bipinnate, finely divided "carrot leaf", narrow leaflets | BEL-like BIP loss of function → TKN1 overexpression. In amateur crosses: regular ≻ carrot ≻ potato (F2 ≈ 56/19/19/6). |
| `clau` | Clausa | n.d. | 🔵 RECESSIVE | Extremely compound leaves (up to ~11× wild type), continuous morphogenesis, ectopic meristems | MYB that dampens cytokinin signalling; floral and ovule defects → avoid in backcrossing. |
| `rg` | Rugose | n.d. | 🟢 DOMINANT | Rugose, crisped dark-green leaves (the "dwarf" look) | Dominant; combined with Cu it is expected to add up (pom-pom + rugose) — [extrapolation], unpublished. |
| `cu / cu-2` | Curled | n.d. | 🔵 RECESSIVE | Curled or wavy leaf blade | Curl series; no dwarfism here, unlike cu-3. |
| `clf-2` | Curly leaf-2 | n.d. | 🔵 RECESSIVE | Curled leaves, altered flowering | Polycomb (CLF-type); epigenetics tool, not a breeding character. |

## 3. Trichomes & pubescence

*Glandular hairs = defence, aroma and sticky glue for whiteflies; the WO + H module* — **6 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `wo` | Woolly | n.d. | 🔵 RECESSIVE | Dense hairs on stems and leaves (type I), branching affected, embryonic defects | HD-ZIP IV master regulator of trichome types I, III, V, VI, VII. |
| `h` | Hair | n.d. | 🔵 RECESSIVE | Sparse or abnormal trichomes | C2H2 zinc finger, WO partner. Fewer glandular hairs = less insect glue — watch whitefly susceptibility. |
| `hl` | Hairless | n.d. | 🔵 RECESSIVE | Deformed trichomes, "bald" stems | Same practical reading as h; shiny leaves more prone to sunscald. |
| `hl-2` | Hairless-2 | n.d. | 🔵 RECESSIVE | Severe deformation of every trichome type | NAP1 (SCAR/WAVE subunit); runty plant, not usable commercially. |
| `sh` | Sparse hair | n.d. | 🔵 RECESSIVE | Rare hairs | C2H2 partner of WO. Pubescence is the first anti-herbivore barrier, not an ornament. |
| `glandless` | Glandless | 9 | 🔵 RECESSIVE | Type VI glandular trichomes present but without gland: terpenes lost | SlHDZ38 (HD-ZIP IV). Type I/IV acylsugar exudate is a separate trait. |

## 4. Foliage — colour & pigmentation

*High pigment, chlorophyll and vegetative anthocyanins* — **12 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `au` | Aurea | n.d. | 🔵 RECESSIVE | Yellow-green seedlings (phytochrome chromophore deficit) | Do not mistake it for nitrogen deficiency: the defect is in the photoreceptor pigment. |
| `v` | Virescent | n.d. | 🔵 RECESSIVE | Whitish young leaves, progressively greening | Classic trap when seedlings are raised under weak light — it is genotype, not fertilisation. |
| `yv` | Yellow virescent | n.d. | 🔵 RECESSIVE | Like v but stronger, worse at low temperature | Same caution as v. |
| `xan` | Xantha | n.d. | 🔵 RECESSIVE | Yellow leaves throughout (reduced chlorophyll) | Unlike v, never fully greens up; fragile plant, no commercial interest. |
| `ch` | Chloronerva | n.d. | 🔵 RECESSIVE | Interveinal chlorosis that MIMICS iron deficiency | Iron in the soil is sufficient: transport is broken. Test before fertilising. |
| `gh` | Ghost | n.d. | 🔵 RECESSIVE | Pale foliage, altered plastids | Distinguish from a mosaic virus: the lamina is not deformed. |
| `hp-1 (hp-1W)` | High pigment-1 | n.d. | 🔵 RECESSIVE | Very dark green foliage, thicker leaves, exaggerated light response; more vitamin C and anthocyanins | SlDDB1 loss of function. Recessive. A spontaneous 1917 mutant of the crop, not a wild allele. |
| `hp-2 (hp-2J, hp-2DG = dg)` | High pigment-2 / Dark green | n.d. | 🔵 RECESSIVE | Dark-green immature fruit, lycopene ×1.5–2, β-carotene ×3 | SlDET1. Dark, thick foliage but compact growth and slower development: the "beautiful leaf" has a vegetative cost. |
| `Ip` | Intense pigmentation | n.d. | 🟢 DOMINANT | Intense pigmentation, exaggerated light response; dark-green immature fruit, +34–38% soluble solids, +62% carotenoids | One of the FEW dominant "high pigment" genes, without the hp defects. Smaller fruit (pleiotropy). |
| `atv` | Atroviolacea | 7 | 🔵 RECESSIVE | More anthocyanins (violet shades), mostly vegetative | R3-MYB repressor truncated (S. cheesmaniae / S. galapagense). Mild alone; with Aft or Abg: strong purple skin (Indigo Rose, Sun Black). |
| `Aft` | Anthocyanin fruit | 10 | 🟢 DOMINANT | Purple-bronzed skin, light-dependent; violet stems and leaves | AN2-like R2R3-MYB, functional allele introgressed from S. chilense (new alleles in S. galapagense LA1141). Monogenic dominant: visible in the F1. |
| `abg` | Aubergine | 10 | 🔵 RECESSIVE | Anthocyanin pigmentation with a different cellular distribution from Aft | Same AN2-like gene (allele Abg) + MYB113, from S. lycopersicoides. Historically described as recessive. |

## 5. Flower, selfing & fruit set

*The selfing lock (Style2.1) and positional male sterility* — **5 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `Style2.1 (se2.1)` | Exserted / inserted style | 2 | 🔵 RECESSIVE | Pistil INSERTED inside the anther cone → strict self-pollination. The wild allele (style exserted ~3 mm) favours outcrossing | Solyc02g087860, HLH motif, style cell expansion; cultivar allele carries StyleD1 (450 bp) + StyleD2 (750 bp) promoter deletions. THE SELFING LOCK: keep style2.1/style2.1 to fix a variety, and isolate flowers whenever the style exserts. |
| `SE3.1` | Stigma insertion 3.1 | n.d. | 🔵 RECESSIVE | Second step of the stigma shift, from flush to inserted; works with Style2.1 | Chr 3 locus (SlbHLH005, AGL6, AGL15/SlMBP11 in the interval) · Both loci together give full selfing: Style2.1 acts first, SE3.1 second. Modern varieties fixed for both. |
| `SlSE2.2` | Stigma exsertion 2.2 | 2 | 🔵 RECESSIVE | Degree of exsertion: knocking it out lengthens anthers and style (positional sterility, no emasculation needed) | Solyc02g087270, F-box protein; 11-bp exon-1 deletion (accession J59) · Tool for hybrid seed production: male sterility without hand emasculation. Modulates IAA/ETH/JA/ABA. |
| `SlLst` | Long styles | 12 | ⚪ MIXED / BACKGROUND | Style elongation and stigma exsertion UNDER HEAT (above ~27 °C): selfing breaks down in a heatwave | EIN4-like ethylene receptor (Solyc12g027610) · ⚠ Explains poor fruit set and unwanted hybrids in hot summers: varietal purity is also a climate question. |
| `pat / pat-2` | Parthenocarpic | n.d. | 🔵 RECESSIVE | Fruit set without pollination → seedless fruit (usually smaller, fewer locules) | Classical locus, GA/auxin pathway (pat-2 not cloned) · Recessive: must be fixed. SlIAA9 (e) and GA-deficient mutants phenocopy it. |

## 6. Fruit shape, locule number & weight

*Two independent axes (length × locules) plus the three cloned weight loci* — **16 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `SUN (sun)` | Sun / fruit elongation | 7 (duplication; IQD12 origin on chr 10) | 🟡 SEMI-DOMINANT | Very elongated, fusiform, pointed fruit (Cornue des Andes, Roma-type). Redistributes mass after fertilisation: more longitudinal, fewer transverse divisions | Rider retrotransposon 24.7-kb duplication → IQD12 overexpression (gain of function); BZR1.7 (BR) drives its transcription · DOSAGE-DEPENDENT: F1 intermediate (d/a ≈ −0.39). Found in 88% of long and 83% of oxheart fruit. SUN ≻ LC for length. |
| `OVATE (o)` | Ovate | 2 | 🔵 → 🟡 RECESSIVE → SEMI-DOMINANT | Oval, pear or pyriform fruit (Yellow Pear, Mountain Vineyard) | G→T premature stop = null allele of the OFP family; functional OVATE is a NEGATIVE regulator of elongation · Recessive in S. pimpinellifolium (round dominant) but additive in the S. pennellii IL2-5: dominance depends on background. ovate alone is not always enough. |
| `SOV1 / SlOFP20` | Square ovate | 2 | 🔵 RECESSIVE | Needed together with ovate for a true pyriform shape; regulatory deletion → under-expression | SlOFP20, OFP × TRM module · Additive with ovate; a SlTRM5 mutation restores roundness in the ovate/sov1 double. |
| `FS8.1` | Fruit shape 8.1 | 8 | ⚪ MIXED / BACKGROUND | Rectangular, blocky processing fruit, resistant to crushing; up to 27.4% of shape-index variance | A857T → premature stop, loss of a non-canonical GT-2 trihelix; the functional gene activates the cell-cycle inhibitor SlKRP2 · Loss of function but PARTIALLY DOMINANT: d/a = −0.47 for shape, +1.14 for weight. |
| `PT (POINTED TIP)` | Pointed tip | n.d. | 🔵 RECESSIVE (LOF) | Pointed/shouldered fruit tip. The wild allele PT^H represses FUL2 and SUPPRESSES the tip | His→Arg: 2 instead of 3 C2H2 domains (partial loss of function) · The tip is therefore recessive; classic bk (chr 2) and n (chr 5) are independent loci. |
| `LC (locule number)` | Locule number | 2 | 🟣 QTL / ADDITIVE | From 2 locules (wild) to 3–4: bigger, flatter fruit | SlWUS gain of function via 2 SNPs in a CArG box · Essentially additive (d/a ≈ 0), sometimes described as partially recessive. In an LA1589 background lc alone barely works without fas. |
| `FAS (fasciated)` | Fasciated | 11 | 🔵 RECESSIVE | 6–10+ locules: flattened, ribbed, giant fruit (Beefsteak, oxheart); up to +37% weight | SlCLV3 ~294-kb inversion with a break point 1 kb upstream = partial promoter loss of function · NEARLY COMPLETELY RECESSIVE (d/a = −0.88 for locule number). ⚠ FAS is SlCLV3, not SlYABBY2b. |
| `ENO (SlENO)` | Excessive number of floral organs | 3 | 🔵 RECESSIVE | More locules and bigger fruit; synergistic with lc and fas | AP2/ERF transcription factor; 85-bp promoter indel → under-expression (it normally represses SlWUS) · Modern fruit with ≥8 locules stack lc + fas + eno. |
| `globe` | Globe | 12 | 🔵 RECESSIVE | Separates FLATTENED fruit (mutant allele) from GLOBE fruit; additive for weight | Brassinosteroid hydroxylase (P450), 1-bp insertion = knock-out · Mutant "flat" allele appeared very late in domestication; 3:1 flat:globe for shape but additive for weight. |
| `SlIQD21 / SlMAP70` | Polar elongation | n.d. | ⚪ MIXED / BACKGROUND | Coordinates polar fruit elongation (calmodulin / microtubule interaction) | Described 2023 · New link of the proximo-distal axis; an editing target rather than a natural allele. |
| `tri2.1 / dblk2.1` | Distal blooming | 2 | 🟣 QTL / ADDITIVE | QTL acting on the distal end (tip/beak) | Not cloned · Complements PT and bk. |
| `ld6 / ld8 / ld11` | Lobulation | 6 / 8 / 11 | 🟣 QTL / ADDITIVE | Degree of lobing (shoulders) | Uncloned QTL, independent of FAS and LC · Three independent loci: ribs do not follow fas/lc. |
| `FAB / CLV1, FIN, SlTPL3, SlKNUCKLES` | CLV–WUS modulators | 4 / 11 / n.d. | 🟣 QTL / ADDITIVE | Fine-tune locule number and fruit size in the CLV3–WUS pathway | CLV1 (Solyc04g081590); FIN arabinosyltransferase (Solyc11g064850); TPL3 co-repressor; KNUCKLES · Explains part of the "noise" around fas and lc. |
| `fw2.2` | Fruit weight 2.2 | 2 | 🟡 SEMI-DOMINANT | Fruit weight: the CULTIVATED (big-fruit) allele adds 30–50%; ~30% of the wild/cultivated difference | CNR = Cell Number Regulator, negative regulator of pericarp cell division; expression change · The WILD small-fruit allele is SEMI-DOMINANT → big fruit is partially recessive. Classic trap when crossing with a tiny-fruit wild accession. |
| `fw3.2 / SlKLUH` | Fruit weight 3.2 | 3 | 🟣 QTL / ADDITIVE | Weight by prolonging cell division, ~19% of variance; also delays ripening and increases branching | SlKLUH P450 (CYP78A), promoter SNP raising expression; both alleles functional · Additive to additive-dominant. Watch the pleiotropy (ripening). |
| `fw11.3 / CSR` | Fruit weight 11.3 | 11 | 🟢 DOMINANT (partial) | SIZE of mesocarp cells; ~8% of variance but the strongest single effect along the domestication gradient | CSR (Solyc11g071940), 1.4-kb deletion → 194-aa truncation = gain of function (proved in transgenic complementation) · One of the few DOMINANT weight loci. ⚠ Distinct locus from fas, 45 kb downstream. |

## 7. Fruit colour (skin × flesh)

*Bi-layer model: carotenoids in the flesh, flavonoids in the skin, residual chlorophyll* — **12 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `Y (SlMYB12)` | Yellow skin / flavonols | 1 | 🟢 DOMINANT | YELLOW skin: naringenin chalcone in the cuticle. y/y = transparent skin | SlMYB12 R2R3-MYB activating the whole flavonol pathway; y = silenced promoter or truncated protein (null Δy) · ⚠ ERRATUM: Y sits on chr 1, not 6 as some fiches state. Monogenic 3:1. THE colour↔nutrition link: a pink fruit (y/y) has lost its flavonols too. SlMYB12 overexpression: rutin ×11–19. |
| `r (PSY1)` | Yellow flesh | 3 | 🔵 RECESSIVE | YELLOW flesh (almost no carotenoids), earlier flowering and pigmentation | PSY1 loss-of-function alleles (aberrant transcripts, insertions) · Dosage effect: ONE functional copy suffices, so red is dominant. Classic 3:1. |
| `t (tangerine / CRTISO)` | Tangerine | 10 | 🔵 RECESSIVE | Bright ORANGE from PROLYCOPENE (cis-lycopene), bioavailable raw — note: no β-carotene | CRTISO carotenoid isomerase loss of function · Epistatic over the r^2997 allele (cis-carotenoids partly restore PSY1 transcription), while r^3756 is epistatic over t: which r allele you carry matters. |
| `B (CYC-B, Beta)` | High-beta | 6 | 🟢 DOMINANT | Dense ORANGE: lycopene converted into β-CAROTENE (>80% of carotenoids) = PROVITAMIN A | CYC-B lycopene β-cyclase strongly over-expressed by promoter variation (gain of function) · All S. cheesmaniae and S. galapagense accessions carry a B allele → your F1 with a red tomato will be ORANGE. Effect is dose-modulated (bb < Bb < BB). |
| `og / og-c (old gold crimson)` | Old gold | 6 | 🔵 RECESSIVE | Deep CRIMSON red (lycopene over-accumulated, zero β-carotene), ochre-orange flowers | NULL alleles (frameshift / stop) of the SAME CYC-B gene · ⚠ B and og are ALLELIC: you cannot stack a null and an over-expressed allele at one locus. |
| `Del (LCY-e)` | Delta | n.d. | 🟢 DOMINANT | ORANGE from δ-carotene at the expense of lycopene | Lycopene ε-cyclase with higher expression/activity · Dominant: shows in the F1. |
| `hp-3 (ZEP)` | High pigment-3 | n.d. | 🔵 RECESSIVE | Deep red, more plastids, higher lycopene | Zeaxanthin epoxidase null → ABA deficiency · ABA deficit brings wilted leaves and dormant seeds, as in not/fl/sit. |
| `u (uniform ripening)` | Uniform ripening | 10 | 🔵 RECESSIVE | Uniformly light-green immature fruit (green shoulder removed); allele fixed in almost all modern varieties | SlGLK2 (Solyc10g008160) nonsense mutation by a 1-bp insertion · ⚠ COST: −10 to −20% sugars and carotenoids. The "pretty" uniform ripener is genetically less tasty. |
| `ug (uniform gray-green)` | Uniform gray-green | n.d. | 🔵 RECESSIVE | No green shoulder: a phenocopy of u through another gene | TKN4 (class I KNOX) loss of function · Lets you tell two looks with different genetic origins apart. |
| `gf (green flesh)` | Green-flesh | 8 | 🔵 RECESSIVE | Chlorophyll RETAINED at maturity → brown-green flesh (Black Crimean, Green Zebra) | SGR1 (Solyc08g080090) Arg143→Ser plus ≥5 independent null alleles · Recessive (homozygous). gf + r/r = true green flesh; gf + Y = brown/black; gf + y = purple-brown (Cherokee Purple). |
| `gs (green stripe)` | Green stripe | n.d. | 🔵 RECESSIVE | Green stripes on the immature fruit | Not cloned · Stripes stay visible at maturity only if gf/gf is present too. |
| `Gr / Nr-2` | Green-ripe | 1 | 🟢 DOMINANT | Fruit DOES NOT RIPEN: green with an orange-red core | GR, RTE1 homologue; 334-bp 5′ deletion → ectopic expression (gain of function) · Dominant, blocks chlorophyll degradation and ripening; Gr and Nr-2 are allelic. |

> 🎨 See also [Predicting fruit colour](#predicting-fruit-colour) for skin × flesh combinations, and remember that `B` and `og` are **allelic** (same gene, `CYC-B`): they do not stack.

## 8. Fruit ripening & storage

*rin, nor, alc, Cnr, Nr: the storage/aroma trade-off* — **5 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `rin (ripening-inhibitor)` | Ripening inhibitor | 5 | 🔵 RECESSIVE | Ripening blocked: pale green fruit that never reddens, no ethylene peak | MADS-RIN deletion → fusion protein, also a dominant-negative repressor at the molecular level · Used in HETEROZYGOSIS (rin/+) for shelf life. ⚠ rin/nor also destroy aroma: they regulate TomLoxC, ADH2, HPL. |
| `nor (non-ripening)` | Non-ripening | 10 | 🔵 RECESSIVE | Delayed ripening, low ethylene, long storage | NAC-NOR, 2-bp deletion → truncated NOR186 · nor/+ hybrids are an industry standard for shelf life. |
| `alc (alcobaca)` | Alcobaca | 10 | 🔵 RECESSIVE | Same as nor but WEAKER: slow ripening, long keeping (hanging "Penjar" tomatoes) | Allele of the SAME NAC-NOR gene, Val→Asp (V317D) · ⚠ Not a separate gene. nor and alc are both used as heterozygotes. |
| `Cnr (Colorless non-ripening)` | Colorless non-ripening | 4 | 🟢 + ⚫ DOMINANT + EPIGENETIC | Colourless fruit, floury pericarp, loss of cell adhesion | SPL-CNR promoter HYPERMETHYLATION (epimutation), no sequence change · DOMINANT (unlike rin/nor) and EPISTATIC over rin and nor. ⚠ An epiallele: DNA markers can fail to predict the phenotype. |
| `Nr` | Never ripe | n.d. | 🟢 DOMINANT | Ripening blocked, delayed senescence and abscission | SlETR3 ethylene receptor, sensor-domain mutation (gain of function) · Dominant-negative: shows in the F1, handle with care in hybrid programmes. |

## 9. Flavour — sugars & soluble solids

*Brix: the wild gene pools and the "sugar brake" released in 2024* — **13 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `LIN5 (Brix9-2-5)` | Lin5 / cell-wall invertase | 9 | 🟡 SEMI-DOMINANT | Roughly doubles the fructose:glucose ratio — an immediate sweet hit. +11 to +25% soluble solids with no yield loss | Solyc09g010080; causal variant is the Asn366Asp SNP near the catalytic site (higher activity, no expression difference) · PARTIALLY DOMINANT: one copy of the S. pennellii allele suffices → usable in the F1. Silencing it costs −30% glucose, −17 to −26% fructose. |
| `SlCDPK27 (SSC11.1)` | Sugar brake | 11 | 🔵 RECESSIVE | KO: +16% soluble solids; double KO with SlCDPK26: +30% glucose+fructose with NO penalty on fruit size or yield | 12-bp promoter insertion in the high-sugar allele → under-expression (loss of function); the kinases brake the sucrose synthase SlSUS3 · Recessive, fix it. ⚠ Lost during domestication because it is linked to the weight locus fw11.3 (big fruit ↔ dilute juice). Fastest route: CRISPR. |
| `SlCDPK26` | Paralogue of CDPK27 | n.d. | 🔵 RECESSIVE | Only shows up in the double knockout with SlCDPK27 | Same pathway · Functional redundancy: you need BOTH losses. |
| `SlSPS1 (qSSC7.1)` | Sucrose-phosphate synthase | 7 | 🟣 QTL / ADDITIVE | Higher sugars with NO effect at all on fruit weight | 1-bp promoter indel (AG/A) at −2355 bp; the AG allele is more expressed · From S. pimpinellifolium LA1924, stable over 3 years and 3 sites. The AG allele declined during domestication, partly recovered in quality programmes. |
| `STP1 (qSSC2.1)` | Monosaccharide transporter | 2 | 🟣 QTL / ADDITIVE | Soluble-solids QTL; knocking it out lowers Brix | 21-bp promoter indel selected during improvement · ⚠ Here the good allele is ALREADY in the elite germplasm: no wild introgression needed. |
| `SlSUS3` | Sucrose synthase | n.d. | 🟢 DOMINANT (transgene) | More sugars without changing fruit weight | Overexpression escaping degradation · Gain of function: dosage effect at transgene scale. |
| `SlINVINH1 / SlVPE5` | Invertase inhibitor / protease | n.d. | 🔵 RECESSIVE | Higher soluble solids, glucose and fructose | Single or double CRISPR knockouts · Maximal effect needs both genes knocked out. |
| `SlVIF` | Vacuolar invertase inhibitor | n.d. | 🟣 QTL / ADDITIVE | Fine control of the sugar "sink" strength | — · Editing target only; no exploitable natural allele described in breeding material. |
| `SlVI / Sucr` | Vacuolar invertase | 3 | 🔵 RECESSIVE | Higher sucrose and soluble solids | Knockout · The classical Sucr locus on chr 3. |
| `SlTST1 / SlTST2` | Tonoplast sugar transporters | n.d. | 🔵 RECESSIVE | Double mutant collapses quality: −40% glucose, −50% fructose+sucrose, −40% soluble solids | — · Opposite direction: these losses RUIN Brix. Protect them, do not mutate them. |
| `SlSWEET7a / SlSWEET14` | Efflux transporters | n.d. | 🔵 RECESSIVE | Silencing raises sugars in ripe fruit | — · Editing targets; no marked natural allele; field effect modest. |
| `SlbZIP1, SlNAP2, SlARF10, SlFgr, AGPase, SUT2, TIV1, RIN` | Brix regulators | divers | 🟣 QTL / ADDITIVE | Each brick contributes 1–15% of the variance; RIN acts through SlVI/SlVIF | Transcription factors and enzymes · Dominance not established. Known QTLs cover >50% of Brix heritability; a single major QTL reaches ~30%. |
| `Segment "chm" (S. chmielewskii)` | Historic high-solids pool | n.d. | 🟢 DOMINANT (dominant gene action) | +13% Brix at homozygosity, +12% in the heterozygote, +6% with one dose; no consistent penalty on yield, fruit weight or pH | Several QTL (classic RFLP mapping) · S. chmielewskii LA1028 (~10% SS vs ~5% in VF36); lines LA1563 (BC5S5) and VF145B-7879 · The 1980s–90s gene pool is still directly usable. ⚠ Rick's high-solids source was chmielewskii, NOT cheesmaniae. |

## 10. Flavour — acidity, umami & GABA

*Malate, citrate, free glutamate and the SlGAD case study* — **8 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `SlALMT9 (TFM6)` | Vacuolar malate transporter | 6 | 🟡 SEMI-DOMINANT | Bright malic acidity (green apple) balancing the sugar. Malate + citrate = >90% of total acids | Solyc06g072910; 3-bp indel in a W-box of the promoter (high-malate allele, selected at domestication); CRISPR KO lowers malate · Regulatory allele: one copy seems sufficient (apple Ma1 model). The 3-bp indel is an easy marker. |
| `SlWRKY42` | ALMT9 repressor | n.d. | ⚪ MIXED / BACKGROUND | Lowers malate by transcriptional repression | Binds the 8th W-box of the SlALMT9 promoter · Gain of function = less acid. Watch it out if you breed for tartness. |
| `Citrate loci (11 loci)` | Titratable acidity & pH | several | 🟣 QTL / ADDITIVE | pH and acidity are highly polygenic, with strong seasonal variation | Indels and structural variants; minor QTL (GWAS 2023) · ⚠ CITRATE matters more to consumer preference than malate — and has no major exploitable gene. |
| `GTF (glycosyltransferase family 1)` | Malate & citrate | 2 | 🟣 QTL / ADDITIVE | Associated with BOTH acids | Meta-GWAS · Dominance not determined. |
| `SlGAD2 / SlGAD3` | GABA: the best-documented dominance case in this file | 1 and 11 | 🟢 DOMINANT (partial) | GABA ×7 to ×15 (up to 125 mg/100 g fresh weight) with no yield effect | Truncation of the C-terminal auto-inhibitory domain (CaMBD, calmodulin binding) · The gene is HAPLO-SUFFICIENT: the heterozygote is enough, so the allele works directly in F1 hybrids and even in T0/hemizygous lines. Basis of Sicilian Rouge High GABA, the first CRISPR food on the market (Japan, 2021). |
| `SlGABA-T1` | GABA catabolism | n.d. | 🔵 RECESSIVE | GABA ×2.95 at red stage | CRISPR knockout · Recessive. |
| `SlGABA-T1/2/3 + SlSSADH` | Multiplex GABA | n.d. | 🔵 RECESSIVE | GABA ×19 BUT severe dwarfing, malformations, near sterility | Simultaneous knockouts · Strong pleiotropy → avoid outside controlled experiments. |
| `Free glutamate pool (umami)` | Umami | divers | 🟣 QTL / ADDITIVE | L-glutamate is the dominant free amino acid of red fruit; no "umami locus" cloned | Peptidases, γ-glutamyl transpeptidase, GDH and GABA-T (the last two surge at ripening) · Quantitative, non-Mendelian. IMP/GMP nucleotides are near absent in tomato: the umami bomb comes from synergy with other ingredients in a cooked dish. |

## 11. Flavour — volatiles & aroma

*The full catalogue of cloned aroma genes* — **17 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `TomLoxC` | 13-lipoxygenase: aroma persistence | 1 | 🟠 OVER-DOMINANCE | "Tomato" aroma, green/floweral notes, 2–5 min of length on the palate: C5/C6 volatiles ((Z)-3-hexenal, hexanal, hexanols) plus apocarotenoids | Rare PROMOTER allele (~4-kb structural variant) and locus duplication; Solyc01g006540 · SUPER-DOMINANCE: heterozygotes (rare + common allele) express MORE than both homozygotes → evaluate F1s, and do NOT fix this allele. Present in 91% of S. pimpinellifolium but only 2% of big-fruit heirlooms; currently coming back in modern varieties. |
| `DXR (promoter)` | Apocarotenoid precursor | n.d. | 🟣 QTL / ADDITIVE | β-ionone, geranylacetone, 6-methyl-5-hepten-2-one: floral and fruity notes | Wild promoter variant → higher downstream expression · Found in 58% of S. pimpinellifolium accessions vs 2% of heirlooms; selected AGAINST during domestication. Quantitative. |
| `SlHPL` | C6 aroma | n.d. | 🟢 DOMINANT | Hexenal and hexenol — "cut tomato" smell | 13-hydroperoxide lyase; translationally controlled by SlYTH2 · The functional allele is REQUIRED (dominant for C6 aroma). |
| `SlADH2` | Aldehyde/alcohol ratio | 6 | 🟣 QTL / ADDITIVE (dosage) | Stronger "ripe fruit" notes when over-expressed; antisense shifts the aldehyde/alcohol balance | Solyc06g059740; regulated by RIN · Dosage effect, and dependent on RIN status. |
| `SlCXE1` | Ester balance | 1 | 🟣 QTL / ADDITIVE | Releases alcohols from esters: tropical notes (mango, pineapple, candy) | Carboxylesterase found by QTL · With AAT1 it sets the volume of the tropical notes — the Sungold signature. |
| `AAT1` | Alcohol acyltransferase | 2 | 🟣 QTL / ADDITIVE | Fruit ESTER synthesis | — · Additive QTL. |
| `SlCCD1A / SlCCD1B` | Apocarotenoids | n.d. | 🔵 RECESSIVE (beneficial) | Better aroma (β-ionone…) at the expense of pigments | Carotenoid cleavage dioxygenases; SlCCD1B translates faster when SlYTH2 is knocked out · ⚠ TRADE-OFF: degrading more carotenoids = less colour, more aroma. |
| `AADC1A / AADC1B / AADC2` | "Malodorous" QTL | 8 | 🟣 QTL / ADDITIVE (strong) | Phenylacetaldehyde, 2-phenylethanol, 1-nitro-2-phenylethane | Aromatic amino-acid decarboxylases · From S. pennellii LA0716 through the IL8-2 line. High-activity allele, but AMBIVALENT: perceived as malodorous in some backgrounds → sensory panel before any introgression. |
| `SlPAR1 / SlPAR2` | Phenylacetaldehyde reductase | n.d. | 🟣 QTL / ADDITIVE (dosage) | Last step of the pathway: converts phenylacetaldehyde into 2-phenylethanol (honey / rose note, also the main scent compound of rose) | Tieman et al. 2007 (Phytochemistry 68) — the biochemistry is solid: NADPH-dependent reductases, conversion shown in vivo by overexpression in petunia. The fruit genetics much less so: tomato lines with reduced `LePAR` did NOT lose 2-phenylethanol (redundancy, pathway limited upstream). Treat as a **dosage** effect, not a locus to fix; any cross prediction here is [extrapolation]. |
| `FLORAL4` | Floral aroma | 4 | 🔵 RECESSIVE (loss is penalising) | 2-phenylethanol (rose/tea), phenylacetaldehyde, 1-nitro-2-phenylethane | Solyc04g063350; QTL fine-mapped to 10 genes · The functional allele is required: deleterious edits collapse PHEV. A contrasting NIL is actually DIFFERENTIATED by tasters. |
| `SlSAMT` | Methyl salicylate | n.d. | ⚪ MIXED / BACKGROUND | Menthol note | Salicylate carboxymethyltransferase · Validated enzyme function. |
| `SlEGS1` | Eugenol | n.d. | 🟣 QTL / ADDITIVE | Clove note | Eugenol synthase · QTL, dominance not determined. |
| `GT1 / UGT` | Glycosylated volatiles | n.d. | 🟣 QTL / ADDITIVE | Aroma reservoirs: glycosylated precursors release during eating and processing | Glycosyltransferases · Quantitative; explains why cooked juice smells stronger than raw fruit. |
| `LIP1 / LIP2` | Lipases | 12 | 🟣 QTL / ADDITIVE (additive) | (Z)-4-decenal and several C5–C10 correlated with consumer liking | Lipases; SpLIP1 allele · From S. pennellii IL12-3: ONE chromosomal segment lifts many positive volatiles at once — the best aroma gain per unit of linkage drag in the whole set. |
| `SlYTH2` | m6A reader: the aroma multiplier | n.d. | 🔵 RECESSIVE (beneficial) | Volatiles ×1.5 overall, with no change in colour or firmness; 71% of tasters preferred the edited fruit | m6A reader repressing translation of SlHPL and SlCCD1B · The functional gene is a REPRESSOR → the beneficial change is a recessive loss of function. Fix it, or evaluate hemizygous T0 lines. |
| `NSGT1` | "Smoky" note (guaiacol) | 9 | ⚪ MIXED / BACKGROUND | The FUNCTIONAL form prevents release of guaiacol (smoke), methyl salicylate and eugenol → cleaner aroma | Non-smoky glycosyltransferase; 5 haplotypes, the non-functional ones (IV, V) carry deletions also removing E8 · Trait described in S. pimpinellifolium and cerasiforme. ⚠ INVERSE CASE: the non-functional haplotypes are the common ones in heirlooms and modern cultivars — selecting functional NSGT1 cleans modern aroma. |
| `RIN / NOR / FUL1-2` | Orchestrators of aroma | 5 / 10 / n.d. | 🟣 QTL / ADDITIVE | Bind the promoters of TomLoxC, ADH2, HPL, CCD… | MADS (RIN, FUL) and NAC (NOR) transcription factors · Pleiotropic: rin/nor block ripening AND destroy aroma. Never trade aroma for shelf life unknowingly. |

## 12. Nutrition & safety

*Vitamins C / B9 / E, polyphenols, glycoalkaloids, minerals* — **17 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `SlGGP1 (uORF)` | Vitamin C | 6 | 🟢 DOMINANT (practical) | Ascorbate up to ×5 | 5′ uORF throttling translation of GDP-L-galactose phosphorylase (Solyc06g073320); breaking it (CRISPR) or over-expressing lifts the brake · POST-TRANSCRIPTIONAL control: strong effect with a single modified allele. ⚠ The ×5 lines show pollen sterility and seedless fruit. |
| `TFA9 / SlbHLH59` | Natural vitamin C | 9 | 🟣 QTL / ADDITIVE | The top SNP explains 15.9% of ascorbate variance | 8-bp promoter indel (Py-rich motif of the 5′UTR) of a bHLH factor · The only marked natural lever for vitamin C, with a direct marker; selected during domestication. |
| `SlGME1 / SlGME2` | GDP-mannose-3',5'-epimerase | n.d. | 🟣 QTL / ADDITIVE | Ascorbate up, plus tolerance to cold, salt and paraquat | Overexpression; silencing one is compensated by the other · Functional redundancy: additive, no clear dominance. Secondary target. |
| `SlNFYA10` | Ascorbate repressor | n.d. | ⚪ MIXED / BACKGROUND | Knockdown raises ascorbate (>×2 in leaf, ×1.3 in fruit) | CCAAT factor repressing SlGME1/SlGGP1 · Negative regulator: gain of function is harmful, loss is desirable. |
| `GCHI + ADCS` | Folates (vitamin B9) | n.d. | 🟢 DOMINANT (all-or-none) | Folates ×25 (840 µg/100 g): the engineered fruit alone covers the RDA of a pregnant woman | Two limiting branches (pteridine and PABA); GCHI alone gives only ×2–4 · Cooperative effect: you need BOTH. |
| `GGH` | Folate retention | n.d. | 🔵 RECESSIVE | The PKM-1 variety is naturally folate-rich | Reduced γ-glutamyl hydrolase activity retains polyglutamylated folates · The only natural lever identified; accompanied by slower ripening. ⚠ Folates vary little (few SNPs over 391 accessions) and decline during ripening. |
| `VTE3(1) / mQTL9-2-6` | Vitamin E (tocopherols) | 9 | ⚫ EPIGENETIC | ~50% of the variation between the two parents | The causal polymorphism is not in the coding sequence but in promoter METHYLATION (natural epialleles) · ⚠ MENDELIAN DOMINANCE DOES NOT APPLY here. A DNA marker may fail to predict the phenotype: use an epi-marker or measure. |
| `VTE1 / VTE2 / VTE4 / VTE5 / HPPD` | Vitamin E pathway | 6, 7, 8, 9 | 🟣 QTL / ADDITIVE | Weak heritability; γ- vs α-tocopherol set by VTE4; up to ×10 tocochromanols when over-expressing HPT/TC/γ-TMT | Confirmed QTL, 16 candidate loci · Additive quantitative. Soil nitrogen and potassium matter as much as genotype. |
| `SlMYB12 (= Y/y)` | Flavonols (rutin) | 1 | 🟢 / 🔵 DOMINANT / RECESSIVE | Pink fruit (y/y) is doubly depleted: transparent skin plus collapsed flavonols. Overexpression: rutin ×11–19 | R2R3-MYB activating PAL/CHS/FLS; expression↔flavonol correlation R² ≈ 0.92 · THE direct colour↔nutrition link. If you breed for nutrition, avoid pinks. |
| `HQT` | Chlorogenic acid | n.d. | 🟣 QTL / ADDITIVE (dosage) | +85% CGA when over-expressed; −98% when silenced | Hydroxycinnamoyl-CoA quinate transferase · Almost pure dosage, very reproducible. |
| `SlHY5` | Nutrition ↔ defence | n.d. | ⚪ MIXED / BACKGROUND | Positive regulator of flavonols AND of steroidal glycoalkaloids | Binds G-boxes of both pathways; losing it collapses both and increases fungal susceptibility · Illustrates the nutrition/defence trade-off: raising one raises the other (bitterness included). |
| `GORKY` | Bitterness of ripe fruit | n.d. | 🔵 RECESSIVE | Deletion keeps α-tomatine trapped in the ripe-fruit vacuole: bitter and toxic fruit | NPF tonoplast transporter · EXPLICITLY monogenic recessive: only gorky/gorky fruits stay bitter. The functional (dominant) allele is what makes a ripe tomato safe. Screen before any wild cross. |
| `GAME5 / GAME31 / GAME36 / GAME40` | Glycoalkaloid detoxification | 8 (GAME5) | 🔵 RECESSIVE | Last step α-tomatine → esculéoside A (non-bitter, non-toxic); hydroxylation/acetylation/glycosylation | Solyc08g006410 UDP-glycosyltransferase; non-functional (stop) alleles exist · Silencing GAME5 brings α-tomatine back up. |
| `GAME9 / GE1` | The anti-bitterness domestication sweep | 7 | ⚪ MIXED / BACKGROUND | Weak (modern) alleles lower glycoalkaloids; the strong wild GAME9 allele activates GAME7/GAME17 | GAME9 = AP2/ERF with weak DNA binding; GE1 = distal enhancer recruiting the MYC2–GAME9 complex on the chr 7 GAME cluster · ⚠ GE1-weak and GAME9-weak are the main causes of the deliberate drop of SGA during domestication. Disrupting GE1 gives wrinkled fruit surfaces (γ-tomatine). |
| `DML2` | Epigenetics of detoxification | n.d. | ⚫ EPIGENETIC | Ensures fruit detoxification at ripening; the DML2^13D variant shifted in frequency at domestication | DNA demethylase (DEMETER-LIKE 2), with RIN, NOR, FUL1 and MYC2 on the GAME network · Epi-genetic/pleiotropic: no simple Mendelian dominance. |
| `SlHMA3 / SlNRAMP6 / SlPCR2` | Cadmium (food safety) | n.d. | 🟣 QTL / ADDITIVE | Sequester Cd in the vacuole, lowering Cd in edible organs | Tonoplast P1B-ATPase, NRAMP and PCR2 · Quantitative; introgressing "sequestering" alleles is a food-safety route. |
| `TOMLHA1 / FRO1 / NRAMP2 / FER / MYB72` | Fruit iron & zinc | divers | 🟣 QTL / ADDITIVE | No major Fe/Zn fruit gene cloned to date; QTL and candidate genes | NRAMP / ZIP / YSL / NAS / ferritin families · Polygenic, additive, weakly heritable: agronomic biofortification (foliar feeding) still beats genetics in speed and efficiency. |

## 13. Biotic resistances

*Major genes, QTL, dominance and known breakdowns* — **27 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `I` | Fusarium race 1 | 11 | 🟢 DOMINANT | Resistance to Fusarium oxysporum f. sp. lycopersici race 1 | LRR-RLP (Solyc11g011180) recognising Avr1/Six4, from S. pimpinellifolium PI 79532 · First resistance gene deployed in tomato (1939). Overcome by race 2 → pyramid with I-2 / I-3. |
| `I-2` | Fusarium races 1 and 2 | 11 | 🟢 DOMINANT | Resistance to races 1 AND 2 | CC-NB-LRR (Solyc11g071430) recognising Avr2/Six3 (+SIX5), from a natural S. pimpinellifolium × S. lycopersicum hybrid (PI 126915) · Widely used commercially, often stacked with I-3 (from S. pennellii). |
| `Ve (Ve1)` | Verticillium race 1 | 9 | 🟢 DOMINANT | Resistance to V. dahliae and V. albo-atrum race 1 | RLP with extracellular LRRs recognising the Ave1 effector; from "Peru Wild" (S. pimpinellifolium) in the 1930s · Present in most cultivars. ⚠ Race 2 breaks it. |
| `Pto / Prf` | Bacterial speck | 5 | 🟢 DOMINANT | Resistance to Pseudomonas syringae pv. tomato race 0 | Ser/Thr kinase Pto + NLR Prf, introgressed cluster from S. pimpinellifolium · Effective for decades against race 0, overcome by race 1. Pto without PrF gives nothing. |
| `qRpp (LA1589)` | Quantitative resistance to Pst race 1 | 5, 6, 8 | 🟣 QTL / ADDITIVE | Resistance WITHOUT hypersensitive response, where Pto is broken | 3 QTL + 5 candidate genes, S. pimpinellifolium LA1589 · The quantitative complement to worn-out major genes. |
| `FLS3` | Flagellin perception | n.d. | 🟢 DOMINANT | Surface PRR recognising flgII-28, amplifying basal immunity | LRR-RLK, functional allele from S. pimpinellifolium · Many modern cultivars have LOST FLS3: reintroducing it is a broad-spectrum lever. |
| `Cf-2.1 / Cf-2.2` | Leaf mould (Avr2) | 1 | 🟢 DOMINANT | Resistance to Passalora (Cladosporium) fulvum races carrying Avr2 | Two tandem functional LRR-RLP; the locus is hypervariable (≥26 Hcr2p homologues) · Documented diversity in natural populations: genotype carefully. |
| `Cf-4` | Leaf mould (Avr4) | 1 | 🟢 DOMINANT | Resistance | LRR-RLP of the "Milky Way" locus; from "L. hirsutum" = S. habrochaites (attribution debated) · Dispersion of Cf-4 in wild populations documented (Thomas 2000). |
| `Cf-5, Cf-8, Cf-9, Cf-13` | Leaf mould | 1 | 🟢 DOMINANT | Resistance to several races (Avr5, Avr9…) | LRR-RLP from S. pimpinellifolium (Cf-8 PI 124161, Cf-13 PI 211839) · Cf-4/Cf-9 share the Milky Way locus. Standard stacking in greenhouse varieties. |
| `Cf-ECP1/2/4/5` | Apoplastic effector recognition | 1 & 6 | 🟢 DOMINANT | Resistance through apoplastic elicitor receptors | Cf-ECP1/4 co-locate with Cf-9/Cf-4 · Newer loci, useful against races escaping the classical Cf genes. |
| `Ph-1` | Late blight | 7 | 🟢 DOMINANT | Resistance to Phytophthora infestans race T0 ONLY — broken by race T1, now dominant | Major gene, not cloned; from S. pimpinellifolium West Virginia 19 and 731 · Barely useful alone today; "DuR" material stacks Ph-1/2/3. |
| `Ph-2` | Late blight | 10 | 🟡 SEMI-DOMINANT | Slows late blight progress | LRR-RLP from S. pimpinellifolium · INCOMPLETELY DOMINANT: heterozygotes resist less. The classic British "field tolerance". |
| `Ph-3` | Late blight | 9 | 🟡 SEMI-DOMINANT | Targeted cellular hypersensitivity, the strongest of the three | CC-NB-LRR cluster (accession L3708); co-dominant marker Ph-3-GLR/S · Ph-2 + Ph-3 stacked gives near-complete protection against aggressive isolates, at homozygosity. |
| `Xv3 / Rx-4` | Bacterial spot race T3 | 11 | 🟡 SEMI-DOMINANT | Resistance to Xanthomonas perforans race T3 | NB-LRR recognising AvrXv3; PI 128216 / line H7981 · INCOMPLETE dominance. T1/T2 races are widespread: combine with the rx recessives. |
| `rx-1, rx-2 (chr 1) / rx-3 (chr 5)` | Bacterial spot race T1 | 1 & 5 | 🔵 RECESSIVE | Resistance to Xanthomonas race T1 | Recessive genes; line H7998, historically from S. habrochaites (PI 126445) · Recessive: homozygous fixation and marker assistance required. |
| `Ol-1, Ol-3, Ol-5` | Powdery mildew | 6 | 🟢 DOMINANT | Major resistance to Oidium neolycopersici (Ol cluster at ~34 Mb) | R genes from S. habrochaites G1.1560 (Ol-1), G1.1290 (Ol-3), PI 247087 (Ol-5, var. glabratum) · Dominant and durable; Ol-1 + Ol-5 are commonly combined. |
| `On-9-l_che` | Powdery mildew (Galápagos QTL) | 9 | 🟡 SEMI-DOMINANT | Partial resistance; 14.6% of variance (~40% of the parental difference) | QTL between 46.5 and 50.5 cM of chr 9, peak at 48 cM, mapped by QTL-seq; from S. cheesmaniae · PARTIAL dominance (not a dominant gene as some fiches state). Low linkage drag: suitable for cherry breeding. |
| `ol-2 (Slmlo1)` | Powdery mildew, durable | 4 | 🔵 RECESSIVE | BROAD-SPECTRUM resistance presumed durable (no breakdown reported) | Loss of function of an MLO susceptibility gene the pathogen needs from the host · ⚠ ATTRIBUTION FIX: from S. lycopersicum var. cerasiforme LA1230, NOT from S. habrochaites. The only cloned mildew gene; recessive. |
| `Ty-2 (TYNBS1)` | TYLCV (yellow leaf curl) | 11 | 🟢 DOMINANT | Complete resistance to begomoviruses (TYLCV) | NLR; the viral elicitor is the Rep/C1 protein. From S. habrochaites f. glabratum B6013 via line H24 · Fully dominant (works in the heterozygote), deployed worldwide. ⚠ The introgression carries a ~300-kb inversion blocking recombination (big linkage drag); narrow spectrum (not TYLCSV, BCTV) → pyramid with Ty-1/3 or ty-5. |
| `Tm-1` | ToMV, and a ToBRFV component | 2 | 🟡 SEMI-DOMINANT | Inhibits viral replication; contributes to ToBRFV resistance in combination | p80 protein (an unusual antiviral mechanism, not an NLR); S. habrochaites PI 126445; S. pennellii alleles also effective · SEMI-DOMINANT (dose effect). Current model: Tm-1 (chr 2) + a recessive tolerance locus on chr 11 = ToBRFV resistance; tm-1 + chr 11 = tolerance. |
| `ToBRFV-R (chr 11)` | Tomato brown rugose fruit virus | 11 | 🔵 RECESSIVE | Tolerance: low virus accumulation, reduced symptoms | Locus near 46.84 Mb on chr 11 (22-kb interval); candidates Solyc11g062150 (TIR-NBS-LRR) and Solyc11g062180 (RLP) · TRUE resistance needs ≥2 genes (Tm-1 dominant + this locus); tolerance alone is a single recessive gene → the F1 of a homozygous donor × cultivar is susceptible. Tm-2² is broken by the virus. |
| `Wf-1` | Whiteflies, aphids, thrips, mites, Tuta | 2 | 🟡 SEMI-DOMINANT | Physical plus chemical barrier: activates type IV trichomes and up to 76 acylsugars; ~54% of adult whitefly survival and ~81% of type-IV density | Major terminal chr 2 QTL, co-located with trichome density and metabolites (ASAT family, AT2 locus); from S. galapagense · PARTIALLY dominant / strong additive. Add Wf-2 (chr 9). Read it with a hand lens (type IV glands, sticky leaves). |
| `ShTPS / zFPS + ShZIS (locus Sst)` | Repellent volatiles of the foliage | 8 | 🟣 QTL / ADDITIVE (codominant) | Zingiberene and 7-epi-zingiberene (type VI sesquiterpene): repellent and toxic to Bemisia, Tetranychus, Tuta absoluta, Diabrotica, plus antimicrobial activity | Biosynthetic cluster zFPS + ShZIS (chr 8, LA1777); ShZO = ShCYP71D184 (P450, chr 1) makes more toxic derivatives · From S. habrochaites var. hirsutum (PI 127826, LA1777). High-ZGB lines are available; the pathway genes work as markers. |
| `MKS1 × MKS2` | Natural insecticide (2-tridecanone) | 8 | ⚪ MIXED / BACKGROUND | 2-tridecanone and methyl ketones in type VI trichomes: larval toxicity (Manduca, Tuta, leafminers, beetle) | ShMKS1/ShMKS2 pathway genes; the effect requires BOTH wild alleles · From S. habrochaites var. glabratum PI 134417. COMPLEX EPISTASIS: one allele alone gives nothing — mandatory stacking. |
| `QTL psyllid` | Resistance to the tamarix/psyllid and Liberibacter | 1, 3, 5, 6, 8 | 🟣 QTL / ADDITIVE | Adult mortality and reduced fecundity of Bactericera cockerelli, thus less "psyllid yellowing" and less Liberibacter transmission | No gene cloned; from S. habrochaites LA1777 · Polygenic: genomic or phenotypic selection under infestation. |
| `Rcm 2.0 / Rcm 5.1` | Bacterial canker | 2 & 5 | 🟣 QTL / ADDITIVE | Quantitative resistance to Clavibacter michiganensis (acts on vascular morphology) | QTL from S. habrochaites LA407; more loci in S. pimpinellifolium GI 1554 (chr 1, 2, 7, 8, 12) · No major gene available: hygiene and clean seed remain the primary defence. |
| `Sw-5 / Mi-1 / Ty-1, Ty-3, Ty-4 / ty-5` | Not in your gene pool | — | 🟢 / 🔵 DOMINANT / RECESSIVE | TSWV (Sw-5), nematodes + aphids (Mi-1), TYLCV (Ty-1/3/4, ty-5) | Major dominant genes, except recessive ty-5 · From S. peruvianum (Sw-5, Mi-1, ty-5) and S. chilense (Ty-1/3/4). Not in pimpinellifolium, cheesmaniae, habrochaites or galapagense: buy them in varieties or request the accessions. |

## 14. Abiotic tolerances & roots

*Salt, drought, cold, heat — almost everything is additive* — **11 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `HKT1;1 / HKT1;2` | Na+/K+ homeostasis (salt) | 7 | 🟣 QTL / ADDITIVE (additive) | Protects flowers and fruit from salt and heat stress; the major QTL explains >40% of the [Na+]/[K+] variance. ScHKT1;2 excludes Na+ from the xylem efficiently; ScHKT1;1 is hyperactive in leaf and root | Class I Na+ transporters; the crop LOST HKT1;1 expression and fixed a different HKT1;2 · From S. cheesmaniae (inclusion) and S. galapagense (exclusion, IL SG18_197). Additive; co-introgression of both loci recommended — the two strategies are complementary. |
| `HKT2;1` | Na+ retrieval from the xylem | n.d. | 🟣 QTL / ADDITIVE | Retrieves Na+ from the xylem and redistributes it through the phloem | K+-Na+ transporter, from S. cheesmaniae · Completes the HKT1 set; quantitative. |
| `lnc1.1 (candidate NHX3)` | Leaf Na+ concentration | 1 | 🟣 QTL / ADDITIVE | Compartmentalises Na+ in the leaf vacuole (the "includer" strategy) | QTL with NHX3 as candidate, S. cheesmaniae · SOS1/SOS2/SOS3/NHX1 mapped as pathway candidates: useful as markers. |
| `SpiI3PS` | Salt tolerance (myo-inositol) | n.d. | 🟣 QTL / ADDITIVE | Extra copies of inositol-3-phosphate synthase improve osmotic adjustment | Copy-number variation · Enriched in the S. pimpinellifolium LA0480 genome, which is also loaded with stress-response genes. |
| `DREB1A / VP1.1` | Salt-tolerance haplotypes | n.d. | 🟣 QTL / ADDITIVE | Allelic variants associated with tolerance (17–26% of variance in association panels) | DREB transcription factor plus VP1 promoter · Haplotypes rather than one gene: genotype a population. |
| `QTL yield under salt` | ~15 QTL | 1, 3, 7, 8, 11 | 🟣 QTL / ADDITIVE | Fruit number and weight, flowering under salinity; medium effects of 8.5–16% | F7 populations "P" (pimpinellifolium) and "C" (cheesmaniae), plus a DOMINANT EPISTATIC QTL on chr 3 · Favourable alleles are usually wild. Watch the drag (small fruit): marker-assisted backcrossing. |
| `Rootstock effect` | Scion yield under salt | divers | 🟣 QTL / ADDITIVE | ≥8 rootstock QTL; up to 65% of rootstock lines improved a commercial hybrid under salinity | h² ≈ 0.3, favourable alleles from the wild species · THE SHORTEST LEVER: graft this season instead of introgressing for five years. |
| `stm9` | Starch reserves & turgor | 9 | 🟣 QTL / ADDITIVE | Maintains stomatal turgor at 6 °C root temperature and under summer drought; 33% of variance explained | Major additive QTL from S. habrochaites · One of the few abiotic QTL with such a large effect; MAS feasible. |
| `DRO1 & root architecture` | Deep rooting | 9 | 🟣 QTL / ADDITIVE | Long specific root length and high hydraulic conductivity: exploration of deeper, less saline layers | QTL plus screens of LA1400/LA1401, from S. galapagense · Combine with HKT: root exclusion plus deep roots. |
| `QTL turgor / canopy temperature` | Water deficit | 1, 5, 6, 7 | 🟣 QTL / ADDITIVE | qtur/qtem on chr 5 and 7 (6.8–9.1% of variance); qtem on distal chr 1 and chr 6 | BC2S3 population LA1141 × OH8245; thermal imaging · Polygenic small effects: genomic selection plus canopy-temperature imaging beat single-locus MAS. |
| `QTL heat (chr 9)` | Reproductive heat tolerance | 9 | 🟣 QTL / ADDITIVE | Maintains seed number under heat stress (ABC transporters as candidates) | Introgression at 65.5–66.3 Mb, BIL lines of LA1589 · ⚠ LA1589 itself is heat-SENSIBLE: tolerances can be cryptic and only show in a cultivated background. |

## 15. Allele sources: your germplasm

*Species by species: what you likely have, at what probability, and how to check it* — **7 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `S. pimpinellifolium` | The best of your four species | — | ▫️ — | Sugar, aroma, vitamin C plus resistances (Ph-1/2/3, Cf, I/I-2, Pto, Xv3, FLS3). Crosses with the crop with no barrier; selfing → easy-to-fix lines | Rare TomLoxC allele in 91% of accessions; SlCDPK27 high-sugar allele prevalent; SlSPS1 AG (LA1924); DXR promoter variant in 58%; lycopene up to 390 µg/g (LA2093) · Accessions LA0480, LA1589, LA1924, LA2093, TO-937, USVL332 (PI 390717), L3708, PI 126915, PI 128216 · Without an accession number you reason in PROBABILITIES: within-species variation often exceeds between-species variation. Same biological species as the crop: it crosses spontaneously. |
| `S. cheesmaniae` | Provitamin A plus salt factory | — | ▫️ — | Locus B (β-carotene) in ALL accessions; tolerance to ~200 mM NaCl (inclusion strategy); j-2 for machine/hand harvest without a calyx; u, ag2; sweet small fruit | B (Cyc-B) dominant; j-2 recessive (LA0166); HKT1;1/HKT1;2 on chr 7; ~15 yield-under-salt QTL · LA0166, LA0422, LA0428, LA1039 (genome), USVL lines · ⚠ No type IV trichomes → no whitefly resistance. ⚠ NOT a TYLCV resistance source (0 of 9 screened accessions asymptomatic). |
| `S. galapagense` | Your best whitefly barrier | — | ▫️ — | Wf-1 (chr 2) + Wf-2 (chr 9): type IV trichomes + 76 acylsugars; salt tolerance (exclusion plus roots) and drought; new Aft/atv alleles (purple fruit); locus B | Firdaus 2013 (Wf); Yu 2022 (genome anchoring the super-pangenome); LA1141 (Aft, atv, u, salt/drought QTL) · LA1141, LA1400, LA1401 · ⚠ Inversions of 18–21 Mb (chr 5), 7.4 Mb (chr 8) and 16–17 Mb (chr 11) → structural linkage drag. Sticky foliage is a nuisance in the greenhouse but a treasure for biocontrol. Dormant seed: soak 24 h, maybe scarify. |
| `S. habrochaites` | Resistance gene pool nº1 | — | ▫️ — | Ty-2 (TYLCV), Tm-1, Ol-1/3/5, Rcm 2.0/5.1, rx-1/2/3, zingiberene, MKS1/2 (2-tridecanone), 30 volatile QTL, ascorbate (bin 8-B), cold/drought tolerance, root vigour for grafting | LA1353 holds 265 intact NLRs, the largest immune repertoire known in the genus · PI 126445, PI 127826, PI 134417, PI 247087, B6013, LA1777, LA0407, CGN15391, LA2167 · ⚠ Self-INCOMPATIBLE (allogamous): you cannot fix it by selfing, maintain families. Green unripe fruit, wild flavours, very high ethylene. Use it as the POLLEN parent: in the reciprocal direction unilateral incompatibility rejects crop pollen. |
| `S. pennellii LA0716` | The quantitative donor | — | ▫️ — | LIN5 (Brix9-2-5), IL8-2 (AADC, "malodorous"), IL12-3 (LIP1/LIP2), fw3.2, fw11.3, Del, Tm-1-type alleles, I-3 | IL library (Eshed & Zamir): 75 lines covering ~98% of the donor genome, M82 background · Via TGRC / Cornell (C. M. Rick collection) · The world reference for QUANTITATIVE tomato genetics. All segments are already isolated as lines: request them, do not rebuild them. |
| `S. chmielewskii LA1028` | The old high-Brix pool | — | ▫️ — | ≈10% soluble solids (vs ≈5% in cultivar VF36), +13% at homozygosity and +12% in the heterozygote | Lines LA1563 (BC5S5, 7–8% SS) and segments VF145B-7879 · S. chmielewskii LA1028 (Casinchichua, Apurimac, Peru) — TGRC; derivatives LA1563 and VF145B-7879 · ⚠ GREEN fruit and high pH: the introgression drags faults to be broken by backcrossing. |
| `S. chilense / lycopersicoides / peruvianum` | Not yours, but useful | — | ▫️ — | Ty-1/3/4 + Aft (chilense), Abg + Del + LA2951 (lycopersicoides), Mi-1 + Sw-5 + ty-5 (peruvianum) | Published IL libraries · S. chilense (Ty-1/3, Aft), S. lycopersicoides LA2951, S. peruvianum (Mi-1, Sw-5, ty-5) — all via TGRC · Stronger hybridisation barriers: long backcrossing, often in-vitro ovule rescue. |

> ⚠️ Without an accession number you reason in **probabilities**: variation *within* a species often exceeds variation *between* species. The verification tests are in the [protocol](#programme-protocol).

## 16. Combinations & epistasis

*What stacks, what cancels, what kills the plant* — **16 loci** · raw filterable data: [`data/genes_tomate.csv`](data/genes_tomate.csv) (EN export: [`data_en/genes_tomate_en.csv`](data_en/genes_tomate_en.csv))

| Symbol | Name / locus | Chr. | Dominance | Effect, phenotype | What it changes in selection |
|:--|:--|:--:|:--|:--|:--|
| `c + gob` | Double recessive potato leaf × goblet | — | ▫️ — | Leaves almost TOTALLY simple (synergy) | C (MYB BL class) and GOB (NAC) act in partially INDEPENDENT pathways · Berger et al. 2009 · Predictably additive: useful to simplify a leaf look. |
| `e + La` | Double entire × Lanceolate | — | ▫️ — | Reinforced simplification (frank simple leaf) | E (auxin) and LA (TCP/GA) act in parallel pathways · Shleizer-Burko & Ori 2012 · e La-2/+ gives a single-lamina simple leaf. |
| `tf + Me/+ ; tf + clau ; tf + bip` | Trifoliate epistasis | — | ▫️ — | The basic trifoliate plan is KEPT; only the dissection of each leaflet changes, sometimes more extremely than in the wild type | Tf is REQUIRED for KNOX-I activity: mis-expression of LeT6/TKn2 cannot create leaflets in the basal part of a tf leaf · Naz et al. 2013 (PNAS) · Rule: genes of a different module stack predictably; genes of the SAME module saturate. |
| `35S:Kn1 + c / tf / e` | Kn1 only branches a pre-existing plan | — | ▫️ — | Kn1 yields 700–2000 leaflets per leaf in the wild type and adds branching in Pts, but FAILS to restore compound leaves in potato-leaf, trifoliate and probably entire | The clearest proof that KNOX = branching, not pattern establishment · Hareven et al. 1996 (Cell) · Pattern hierarchy: La > tf > KNOX/GOB > e. |
| `La + everything` | Lanceolate is epistatic | — | ▫️ — | "La is epistatic to all known leaf shape mutations": any La + complexity double gives a simple leaf; La/La forms no shoot meristem at all | La blocks meristematic activity of every shoot meristem · Hareven et al. 1996 · La/La is embryo-lethal: never try to fix it. |
| `miR319 / miR164` | Morphogenetic window × cutting | — | ▫️ — | Over-expressing miR319 gives "super-compound" leaves with undifferentiated margins, largely SUPPRESSED by miR164 or gob-3; over-expressing miR164 suppresses the la-6 phenotype | GOB acts INSIDE the window opened by LA/TCP4: the window opens and closes, GOB cuts · Ori 2007; Israeli 2021 · The most profitable conceptual frame for predicting a leaf double mutant. |
| `SlMP (SlARF5) + Gob-4d` | Auxin × CUC additivity | — | ▫️ — | Fewer primary leaflets, longer petioles, more and deeper sinuses than either single mutant | SlARF5/SlMP promotes leaflets; effect partially ADDITIVE with GOB · Israeli et al. 2021 · Genes of different modules add up: these are the combinations that work. |
| `j + s` | Jointless masks compound | — | ▫️ — | j suppresses the extreme truss branching of s | Epistasis of j (MADS-box) over s (WOX) · Published · Wanted: a branched truss AND a handle-free pedicel? Not compatible as they stand. |
| `sp + sft` | Semi-determinate habit | — | ▫️ — | sft/sft in a SP background = determinate-ish arrest; SFT/sft in a sp background = SEMI-DETERMINATE (the intermediate architecture used commercially) | Dosage of florigen (SFT) against antiflorigen (SP) · Kimura/Pnueli · Commercial "semi-determinate" = sp plus sft heterozygosity, not a new gene. |
| `d + sp (+ mnt)` | Micro-Tom | — | ▫️ — | Dwarf AND determinate (mnt adds micro-dwarfism) | Three independent recessives combined · Cultivar (Micro-Tom) · Architecture and size are genetically INDEPENDENT: you can be tall and determinate, or dwarf and indeterminate. |
| `clau + lyr` | Complexity reinforced | — | ▫️ — | Stronger phenotype (the two pathways converge on GOB) | Different pathways, convergence · Published · — |
| `SUN + LC + FAS` | The oxheart | — | ▫️ — | SUN ≻ LC for overall shape (long fruit even with lc), but adding FAS RE-ROUNDS it into the oxheart (French "cœur de bœuf") | Three loci, two axes (proximo-distal × medio-lateral) · Rodríguez 2011; van der Knaap · Fruit shape is the weighted sum of two axes: never reason on a single gene. |
| `t + r` | Colour epistasis | — | ▫️ — | t (tangerine) is epistatic over r^2997 (cis-carotenoids restore PSY1), while other r alleles (r^3756) are epistatic over t | Kachanovsky 2012 · Published · The exact r allele matters: a generic "r" marker can lie. |
| `Cnr + rin/nor` | Ripening block over block | — | ▫️ — | Cnr is EPISTATIC over rin and nor | Dominant epimutation over recessives · Wang 2020 / Manning 2006 · One Cnr copy overrides the rest of the ripening programme. |
| `Aft/Abg + atv` | Intense anthocyanins | — | ▫️ — | Alone: modest vegetative flushing. In combination: frank purple skin (Indigo Rose, Sun Black) | Aft/Abg dominant plus recessive atv · Fenstemaker et al. 2022 (Plant Direct) · The "blue" programme needs one Aft copy AND atv/atv homozygosity. |
| `Cu × c / tf / e / rg` | Unpublished crosses to test | — | ▫️ — | Cu × c: pom-pom architecture kept, leaflets simpler and fused. Cu × tf: tf epistasis expected → 3 leaflets. Cu × e: pom-pom with continuous margin. Cu × rg: expected additive, "rugose pom-pom". Cu × Me: nearly impossible (linked loci) | [extrapolation] — no publication exists on Cu in a double mutant · Your Cu/Stick notes · Confirm experimentally. Keep them marked as hypotheses in your notebook. |

> **Combination rule.** Genes of the *same module* do not add up (`Cu`, `Me`, `Pts`, `bip`, `clau`, *35S:Kn1* all go through KNOX: doubling them saturates the module). Genes of *different modules* combine predictably and additively (`slmp Gob-4d/+`, `e La-2`, `tf + Me/+`). Hierarchy of the base pattern: **`La` > `tf` > KNOX / GOB > `e`**.

## Predicting fruit colour

| Final fruit colour | Flesh genotype | Skin genotype | Reference varieties |
|:--|:--:|:--:|:--|
| **Classic bright red** | `R_` | `Y_` | Saint-Pierre, Mountain Vineyard |
| **Pink** | `R_` | `yy` | Rose de Berne, Brandywine |
| **Tangerine orange** | `tt` | `Y_` | Tangerine, Sungold |
| **Pastel orange / salmon** | `tt` | `yy` | Orange Fleshed Purple Smudge |
| **Golden yellow** | `rr` | `Y_` | Yellow Pear, Taxi |
| **White / ivory** | `rr` | `yy` | Great White, Princess Borghese (Blanche de Prusse) |
| **Chocolate brown / black** | `R_` + `gf/gf` | `Y_` | Black Russian, Black Cherry |
| **Dark purple** | `R_` + `gf/gf` | `yy` | Cherokee Purple |
| **Green at ripeness** | `rr` + `gf/gf` | `Y_` or `yy` | Green Zebra, Aunt Ruby's Green Drago |
| **Deep indigo** | `Aft_` + `atv/atv` | variable | Indigo Rose, Black Beauty |

Combining `PSY1` + `SGR1` + `SlMYB12` predicts **8 distinct phenotypes**: each locus segregates 1:2:1 and each mutant allele only acts at homozygosity ([Baek et al. 2025](https://www.kspbtjpb.org/journal/view.html?doi=10.5010%2FJPB.2025.52.019.163)).

## Sizing your progeny

To combine **k independent recessive genes** with 95% certainty:

```
N ≥ ln(0.05) / ln(1 − 0.25^k)
```

| k | Probability per F2 plant | Plants for 95% | Plants for 99% | Typical goal |
|:--:|:--:|:--:|:--:|:--|
| **1** | 0.25^1 = 25.0 % | **11** | 17 | determinate habit (`sp/sp`) or dwarf (`d/d`) |
| **2** | 0.25^2 = 6.25 % | **47** | 72 | `br` + `style2.1` · `d` + `sp` (Micro-Tom) |
| **3** | 0.25^3 = 1.562 % | **191** | 293 | dwarf + determinate + jointless (`d sp j-2`) |
| **4** | 0.25^4 = 0.391 % | **766** | 1177 | plus potato leaf (`c`) or plus `gf` |
| **5** | 0.25^5 = 0.098 % | **3067** | 4714 | "dwarf determinate pink cherry with no calyx" |
| **6** | 0.25^6 = 0.024 % | **12270** | 18861 | long-term programme: better split into two lines |

Below that number you are not *looking for* the genotype, you are letting it pass. Trick: 4 recessives = 766 plants in bulk, but **two lines with 2 recessives each (47 + 47) crossed together**, then one more sorted F2, costs ten times less space and time.

## The 10 golden rules

- **1. A DOMINANT trait shows up in the F1** — `SUN` (elongated), `Y` (yellow skin), `R`/`PSY1` (red flesh), `B` (β-carotene), `Aft` (anthocyanins), `Ip`, `Del`, `Nr`, `Gr`, `Cnr`, `fw11.3`, `Wf-1` (IV trichomes), `Ty-2`, `Ol-1`, `I`, `I-2`, `Ve`, `Pto`, `Mi-1`. **One donor parent is enough**, and the F1 hybrid is already saleable for that trait.
- **2. A RECESSIVE trait requires both copies** — `d`, `br`, `sp`, `mnt`, `Style2.1` (inserted stigma), `j-2`, `ovate`, `fas`, `fs8.1`, `globe`, `eno`, `y` (pink), `r` (yellow), `t` (orange), `og`, `gf`, `u`, `gs`, `rin`, `nor`, `alc`, `c` (potato leaf), `e`, `gob`, `tf`, `bip`, `hp-1`/`hp-2`, `rx-1/2/3`, `ol-2`, `gorky`, `SlCDPK27` (high sugar). It **disappears in the F1** and **reappears in 25% of the F2 plants** (per trait).
- **3. Semi-dominant: the heterozygote has a price** — `La` (lethal at homozygosity), `erl`, `sft` (semi-determinate), `Nr`, `Tm-1`, `B/Cyc-B`, `Ph-2`, `Ph-3`, `Xv3`, `LIN5`, `On-9^l_che`, `SUN`, `lc`, `fw2.2`. For these, the **level** of resistance, compactness or sugar differs between the F1 and the fixed line: measure both states, never assume.
- **4. Over-dominance: keep the heterozygote** — `TomLoxC` (aroma) — the heterozygote (rare allele + common allele) **expresses more than both homozygotes**: fixing it would be a mistake. A mirror image, this time negative: `rin/+`, `nor/+`, `alc/+` heterozygotes give shelf life without ruining the fruit.
- **5. Epistasis: some genes erase the others** — `j` ≻ `s`; `La` ≻ every leaf-shape mutation; `tf` ≻ `clau`/`bip`/`Me`; `SUN` ≻ `LC` (but `SUN`+`LC`+`FAS` = oxheart); `Cnr` ≻ `rin` ≈ `nor`; `t` ≻ `r^2997`; `j-2` × `ej2` = negative epistasis. **Genes of the same module do not add up** (Cu+Me+bip+clau saturates the module, often with an unviable plant); **genes of different modules combine predictably.**
- **6. The backcross trap** — Never backcross **towards** a wild parent after introducing recessive domestication genes (`br`, `Style2.1`, `j-2`, `gf`, `u`…): you erase them at every BC. Work by **selfing in the F2 with pedigree selection**, or by **marker-assisted backcrossing (MABC)** genotyping the recessive loci you want to keep — not only the target gene.
- **7. Linkage drag is the real difficulty** — `Ty-2` drags a ~300 kb inversion (chr 11); the Galápagos accessions carry inversions of 18–21 Mb (chr 5), 7.4 Mb (chr 8), 16–17 Mb (chr 11); the high-sugar allele of `SlCDPK27` was lost because it is linked to the `fw11.3` weight locus. **Plan fine populations and dense markers** to break these links: 2 to 4 generations.
- **8. Think d/a, not "dominant"** — For any quantitative trait, compute **d/a = (2·F1 − P1 − P2) / (P1 − P2)**: 0 = additive, ±1 = complete dominance, |d/a| > 1 = over-dominance. ⚠ **d/a is not a constant of the locus**: it moves with the parent pair and with the measured trait (`fs8.1`: −0.47 for shape, +1.14 for weight).
- **9. The phenotype is not only the genotype** — Heteroblasty: the same plant changes its leaves along the stem (miR156/SPL → miR319/TCP → CUC). Always compare **the same leaf rank** (e.g. n° 6–8), at the same stage, under the same conditions. Likewise °Brix depends on irrigation, potassium, light and harvest stage: a catalogue Brix is not a genotype.
- **10. The flaws come in the same packet** — `u` = −10 to −20% sugars and carotenoids; `Cnr` = gritty pericarp; `Ip` = smaller fruit; `fw3.2` = slower ripening; `rin`/`nor` = aroma destroyed; ×5 vitamin C = pollen sterility; multiplex GABA = dwarfism and near-sterility. **Always look for the physiological cost before you write "variety".**

Three reflexes sum up this whole sheet. **(1)** Look first at the **nature of the mutation**: a loss of function (stop codon, deletion, frameshift) will be recessive, a gain of function (duplication, promoter, overexpression) will be dominant or semi-dominant — this rule predicts the mode of dominance better than any table. **(2)** Count the **recessives** in your objective: that number, and only that number, decides how much you have to sow. **(3)** Never chase a wild allele **without its exit ticket**: every introgression arrives with the neighbouring segment (inversions, `fw11.3`, small fruit), and markers are the only currency that pays for cleaning it up.

## Markers and genotyping

| Locus | Marker type | What it reveals |
|:--|:--|:--|
| `SlMYB12` (`y`) | CAPS / InDel marker | pink (yy) vs red (Y_) plus flavonols — 1:2:1 |
| `SGR1` (`gf`) | gene-based marker | brown/green at ripeness — homozygosity required |
| `PSY1` (`r`) | gene-based marker | yellow vs red flesh |
| `SlGLK2` (`u`) | InDel / CAPS | uniform ripening plus its sugar cost |
| `LC`, `FAS` | markers linked to the inversion/SNP | locule number, flattening, weight |
| `B`/`og` (CYC-B) | promoter haplotypes | β-carotene vs lycopene (same locus!) |
| `OVATE` | CAPS (stop codon) | pear / oval shape |
| `Lin5` (Brix9-2-5) | SNP Asn366Asp | Brix — one copy is enough |
| `SlCDPK27` | PCR of the 12 bp insertion | high sugar (recessive, chr 11) |
| `SlSPS1` | 1 bp promoter InDel AG/A | Brix without a size penalty |
| `STP1` | 21 bp promoter InDel | Brix (allele already present in the crop) |
| `SlALMT9` | 3 bp InDel (W box) | malic acidity |
| `TFA9`/`SlbHLH59` | 8 bp InDel | vitamin C (15.9% of the variance) |
| `TomLoxC` | structural-variant marker | aroma — aim for the HETEROZYGOTE |
| `GORKY` | deletion | bitterness / α-tomatine of the ripe fruit |
| `GAME9`, `GE1` | haplotypes | glycoalkaloid content |
| `VTE3(1)` | **epimarker** (methylation) | vitamin E — DNA alone is not enough |
| `Ph-3` | co-dominant marker Ph-3-GLR/S | late blight |
| `Ty-2` | specific marker (2020) | TYLCV |
| `j-2` | markers (SlMBP21) | jointless pedicel |
| `br`, `sp`, `d` | published MAS markers | compact / determinate / dwarf habit |
| Type IV trichomes | **hand-lens phenotyping** | whitefly resistance (Wf-1) — no public marker |

All of them are short-amplicon PCRs (30–400 bp) from a leaf disc or a 2 cm leaf fragment; for InDels a gel is enough, no sequencer required.

## Pitfalls and corrections

### 13 classic confusions

- **`Cu` (Curl, dominant)** has nothing to do with **`cu-3` (curl-3, recessive, brassinosteroid receptor)**, nor with `cu`/`cu-2` (curled), nor with the leaf curl virus (TYLCV, `Ty` genes).
- **`c`** = *potato leaf* (recessive); **`C`** = the dominant wild-type allele (regular leaf). Same letter, opposite meaning.
- **`e` (entire) is RECESSIVE** (loss of function of *SlIAA9*) despite a name that suggests dominance.
- **`FAS` is not `SlYABBY2b`** (2008 hypothesis) but **`SlCLV3`** (294 kb inversion). And `fw11.3` (`CSR`) is a **distinct locus, 45 kb downstream**: confusing them costs whole seasons.
- **`B` and `og`/`og^c` are ALLELIC** (same gene, `CYC-B`): you do not stack a null allele with an overexpressed one.
- **`alc` is an allele of `NAC-NOR`**, not a separate gene. `nor` and `alc` are used as heterozygotes.
- **`Ip` is not an `hp`**: `Ip` is dominant, `hp-1`/`hp-2`/`dg` are recessive.
- **`ol-2` (`Slmlo1`, chr 4)** does not come from *S. habrochaites* but from *S. lycopersicum* var. *cerasiforme* LA1230.
- **Habit (`sp`) and size (`d`, `br`, `mnt`) are independent**: you can be determinate and tall, or dwarf and indeterminate.
- **`sft` is not a simple monogenic 3:1** for architecture: the heterozygote has a measurable phenotype (dosage).
- **`j` (chr 11) and `j-2` (chr 12) are NOT allelic**: the jointless phenotype can come from either, but only `j` breaks the truss branching (epistatic over `s`) and drags excess foliage — hence the breeder's preference for `j-2`.
- **`style2.1`/`se2.1` (chr 2) is not the only lock**: `SE3.1` (chr 3) and `SlSE2.2` (chr 2) set the degree of exsertion, and `SlLst` (chr 12) makes the style overflow above 27 °C. Varietal purity is therefore also a matter of climate.
- **`gob` vs `Gob-4d`**: the first is recessive (fewer leaflets), the second semi-dominant (deeper lobes): same gene, opposite effect depending on the allele.

### Corrections brought to earlier syntheses

These statements were re-checked; the tables above carry the corrected value.

| Point | Often stated | Verified status | Source |
|:--|:--|:--|:--|
| `Y` (*SlMYB12*, yellow skin / pink fruit) | chromosome 6 | **chromosome 1** | Cloning and mapping: Ballester et al. 2010; the `y` locus sits on chr 1 of the classical maps. |
| **ToBRFV** resistance | "a recessive gene from *S. pimpinellifolium*, chr 11" | **Tm-1 (chr 2, semi-dominant) + a recessive tolerance locus on chr 11**; real resistance needs ≥ 2 genes | Zinger et al. 2025 (PLOS Genet.); Jaiswal et al. 2025 (TAG 138:190) — major QTL on chr 11 at ~46.84 Mb in *S. pimpinellifolium* USVL332 (PI 390717), candidates Solyc11g062150 / Solyc11g062180; Zois et al. 2025 (*S. pennellii* allele). |
| **`On-9`** (powdery mildew, *S. cheesmaniae*) | "DOMINANT" | **partial dominance (QTL)** | ResearchSquare 2026: `On-9^l_che`, chr 9, 46.5–50.5 cM, peak at 48 cM, 14.6% of the variance, ~40% of the difference between the parents. |
| **`Ph-1`** | chromosome 4 | **chromosome 7**; effective against race T0 only | Gallegly & Marvel 1955; Peirce 1971; recalled in Wang et al. 2016 (Plant Breeding) and Springer 2025. |
| `SUN` | "DOMINANT (gain of function)" | **semi-dominant / dosage** (intermediate F1, d/a ≈ −0.39) | Xiao et al. 2008 (Science); Clevenger et al. 2011. It is a REGULATORY mutation, so it is dosed, not a clean dominant. |
| **`style2.1`** | "inserted stigma = recessive" (no further detail) | confirmed: `se2.1` recessive, gene **Style2.1 = Solyc02g087860** (HLH motif), promoter deletions StyleD1/StyleD2 | Chen et al. 2007; Riccini et al. 2025 (BMC Plant Biol.) — the allele is fixed in the crop. |

**Status of recent clones.** `FS8.1` (2023), `globe` (2021), `ENO` (2020), `PT` (2022), `SlOFP20` (2018), `SlSE2.2` (2025): dominance is estimated on few genetic backgrounds. Confirm it on your own population.

## Programme protocol

**Step 0 — Define the target and its mode of dominance**  
Write the genotype you want in symbols (e.g. `d/d sp/sp Y/y gf/gf Style2.1/Style2.1`). Count the recessives: that is the number **k** that fixes the size of your progeny, not the ambition of the project.

**Step 1 — Size the F2**  
Apply N ≥ ln(0.05)/ln(1 − 0.25^k). 2 recessives = **47 plants**, 3 = **191**, 4 = **766**. Below that you are not *hunting* the genotype, you are letting it walk past you.

**Step 2 — Choose the direction of the cross**  
With *S. habrochaites*, *S. pennellii* or *S. chilense*, use them as the **MALE** parent: in the reverse direction unidirectional incompatibility rejects the cultivated pollen. With *S. pimpinellifolium*, *cheesmaniae*, *galapagense*: both directions work.

**Step 3 — Isolation, for real**  
Selfing is only reliable when the stigma is inserted (`Style2.1/Style2.1`). Under a heat wave (> 27 °C, gene `SlLst`) or with a wild relative whose style is exserted, the outcrossing rate climbs: organza bags, an isolation cage, distance, or emasculation plus controlled pollen.

**Step 4 — Mark instead of waiting**  
For recessives hidden in the heterozygote (`fas`, `gf`, `y`, `ovate`, `SlCDPK27`, `ol-2`, `rx`, `u`), a seedling marker (AMP / leaf punch) saves two years of phenotyping. Short-InDel loci (3–21 bp) are genotyped by plain PCR, no sequencer needed.

**Step 5 — Break the drag, then fix**  
2 to 4 marker-assisted backcrosses if you come from a wild relative (select the target gene AND the cultivated background at the useful loci). Then self to F5–F6 with pedigree selection to fix.

**Step 6 — Validate by tasting, not by refractometer alone**  
Some volatiles raise PERCEIVED sweetness without changing the Brix: measured sugar ≠ tasted sugar. Blind panel, 5–10 fruit per progeny, at the same ripening stage.

## Reproducibility

This README, the site and the exports are **generated** from table files (TSV) — nothing is copied by hand. The French edition is built from `data/` (8 fields: locus, molecular basis, allele origin, selection note), the English edition from `data_en/` (6 fields: the selection columns only).

```
tomate-genetique/
├── README.md                  ← French edition (the reference one — generated)
├── README.en.md               ← this file, generated from data_en/
├── SOURCES.md                 ← bibliography: references, links and verification level (language-neutral)
├── CITATION.cff               ← how to cite the repository
├── CONTRIBUTING.md            ← format expected for an addition or a correction
├── LICENSE                    ← CC BY 4.0 (data and text)
├── data/                      ← SOURCE OF TRUTH, 8 fields per line
│   ├── 01_plante.tsv … 04_resistances.tsv
│   ├── genes_tomate.csv       ← all loci flat (export)
│   └── genes_tomate.xlsx      ← filterable workbook (one sheet per chapter)
├── data_en/                   ← English edition, 6 fields per line
│   ├── 01_plante.tsv … 04_resistances.tsv
│   └── genes_tomate_en.csv    ← flat English export
├── docs/index.html            ← static searchable site (French labels, same data)
└── scripts/build_fiche.py     ← regenerates README.md, README.en.md, docs and exports
```

```bash
python3 scripts/build_fiche.py   # regenerates README.md, README.en.md, docs/index.html and the exports
```

Every build runs a **FR ↔ EN consistency check**: same sections, same number of rows, same chromosomes and same dominance codes. Only the wording may differ. The column dictionary is in [`data/README.md`](data/README.md).

## Sources, licence and citation

- **Bibliography**: [SOURCES.md](SOURCES.md) — references by theme with links, plus the germplasm resources (TGRC, SGN, TOMATOMA, IL libraries). Written in French, but every reference is citable as is.
- **Traceability**: the *allele origin* of each locus (accession, mutant, species) is in the French README and in the CSV; anything unpublished here is marked **[extrapolation]**.
- **Licence**: [CC BY 4.0](LICENSE) — reuse, adapt, redistribute, with attribution.
- **Citation**: [CITATION.cff](CITATION.cff) (add your Zenodo DOI once minted).

<sub>Sheet consolidated on 15/10/2026 from eight literature-research dossiers. This repository is a working tool, not an authority: in breeding, the only authority left is your own F2.</sub>
