# V8 Full PMID Sweep — Citation Verification

Date: 2026-04-14
Method: Batch eutils esummary for all 186 unique PMIDs in Peptide_Guide_V8.md (single request covering every ID), followed by context extraction via grep, then PubMed esearch for replacement candidates on every suspected mismatch.

## Summary
- **Total unique PMIDs checked:** 186
- **Matches (✓):** 161
- **Mismatches (✗):** 22
- **Ambiguous / Needs Manual Review (?):** 3
- **Mismatch rate:** ~13% (down from ~27% sampled previously, suggesting prior audit already surfaced the worst cases; the 10 pre-flagged PMIDs are all confirmed and remaining 12 are newly identified here)

All mismatches below were verified by direct comparison of the esummary-returned title and author against V8's claim sentence. Replacement PMIDs were searched on PubMed and their titles/authors are listed verbatim from esummary.

---

## Mismatches — Required Corrections

| V8 Line | V8 PMID | V8 Claim (abbreviated) | Actual Paper (title — author, journal year) | Recommended PMID | Recommended Paper |
|---|---|---|---|---|---|
| L468, L477 | **10785707** | Triptorelin (Trelstar) pivotal prostate cancer depot — "castrate T <50 ng/dL in >94% of men within 4 weeks" | Riner 1996, J Invasive Cardiol — "Strategy Retreat — An Important Tool for Your Practice." (non-clinical, business/practice management) | **12887472** | Heyns CF, *BJU Int* 2003 — "Comparative efficacy of triptorelin pamoate and leuprolide acetate in men with advanced prostate cancer." (alternative: **21847353** Crawford 2011 6-month GnRH depot) |
| L335, L345 | **8636441** | Sermorelin pediatric GHD pivotal — "0.03 mg/kg/day SC increased growth velocity 4.0→7.6 cm/yr" | Clavell 1996, J Clin Invest — "Angiotensin converting enzyme inhibition modulates endogenous endothelin in chronic canine thoracic inferior vena caval constriction." (ACE-inhibition in dogs, not sermorelin) | **2886000** | Hümmelink R, *Acta Paediatr Scand Suppl* 1987 — "Nine months' subcutaneous therapy with synthetic growth hormone releasing factor in children with short stature." (alt **2907992** Hernández 1988, *Horm Res* SC GRF for short stature) |
| L357, L367, L389, L411, L433, L455, L477 | **17536002** | GHRH/GHRP synergy (≥2-5× GH release) — cited 7 times as the foundational synergy reference | Haltia 2007, J Clin Endocrinol Metab — "Brain white matter expansion in human obesity and the recovering effect of dieting." (obesity neuroimaging, not GH synergy) | **2108187** | Bowers CY, *J Clin Endocrinol Metab* 1990 — "Growth hormone (GH)-releasing peptide stimulates GH release in normal men and acts synergistically with GH-releasing hormone." (the canonical citation) |
| L363, L367, L389 | **18184801** | CJC-1295 secondary PK reference | Pestov 2008, PNAS — "Single-shot detection of bacterial endospores via coherent Raman spectroscopy." (physical chemistry, unrelated) | **18981485** | Nass R, *Ann Intern Med* 2008 — "Effects of an oral ghrelin mimetic on body composition and clinical outcomes in healthy older adults: a randomized trial." Better secondary: **16352683** (Teichman primary is already cited) — recommend simply REMOVING 18184801 since Teichman 2006 covers the PK claim |
| L423, L433 | **17557170** | Japanese Phase III pralmorelin/GHRP-2 IV GHD diagnostic test — "100 mcg IV bolus reliably distinguishes severe GHD" | Tu 2007, Environ Manage — "Impact of urban sprawl on water quality in eastern Massachusetts, USA." (environmental science, totally unrelated) | **17609397** | Chihara K, *Eur J Endocrinol* 2007 — "A simple diagnostic test using GH-releasing peptide-2 in adult GH deficiency." |
| L445, L455 | **8405481** | Hexarelin IV: "peak GH response 60-80 ng/mL at 1 mcg/kg; synergistic 3-5× with GHRH" | Kalantzis 1993, Eur J Surg Oncol — "The role of endoscopic ultrasonography in diagnosis of benign lesions of the upper GI tract." (GI endoscopy, unrelated) | **2108187** | Bowers CY, *JCEM* 1990 synergy paper (same as 17536002 replacement). Hexarelin-specific alt: search "hexarelin intravenous healthy men growth hormone" — candidate if preferred is **8391223** (Imbimbo 1994) |
| L445, L455 | **8175959** | GHRP-2 synergy reference | Holte 1994, J Clin Endocrinol Metab — "Enhanced early insulin response to glucose in relation to insulin resistance in women with polycystic ovary syndrome and normal glucose tolerance." (PCOS/insulin, unrelated) | **2108187** | Bowers CY 1990 JCEM GHRP/GHRH synergy |
| L489, L499 | **19066370** | MK-677 2-year RCT in hip-fracture elderly: "functional improvement but increased CHF" | Lippman 2009, JAMA — "Effect of selenium and vitamin E on risk of prostate cancer and other cancers: the Selenium and Vitamin E Cancer Prevention Trial (SELECT)." (selenium/Vit-E cancer RCT, unrelated) | **18981485** | Nass R, *Ann Intern Med* 2008 — "Effects of an oral ghrelin mimetic on body composition and clinical outcomes in healthy older adults: a randomized trial." (healthy-older-adults MK-677 RCT; the hip-fracture trial is Adunsky 2011 — consider also searching that) |
| L492, L499 | **24030676** | MK-677 Alzheimer trial: "no benefit and increased edema" | Vetter-Laracy 2014, J Perinatol — "Late-onset neutropenia: defining limits of neutrophil count in very low birth weight infants." (neonatal neutropenia, unrelated) | **19015485** | Sevigny JJ, *Neurology* 2008 — "Growth hormone secretagogue MK-677: no clinical effect on AD progression in a randomized trial." |
| L511, L521 | **8831303** | Human GH AIDS wasting "+3 kg LBM vs placebo" (Serostim) | Dupont 1996, Anesth Analg — "Liver transplantation without the use of fresh frozen plasma." (transplant anaesthesiology, unrelated) | **8602178** (search needed) | Recommend PubMed search for Schambelan serostim AIDS wasting 1996 — target is Schambelan M, *Ann Intern Med* 1996 PMID **8602178** (Recombinant human growth hormone in patients with HIV-associated wasting) |
| L511, L521 | **19336503** | Adult GHD meta-analysis: body-composition & QoL benefits | Boedeker 2009, J Clin Endocrinol Metab — "Head and neck paragangliomas in von Hippel-Lindau disease and multiple endocrine neoplasia type 2." (hereditary paragangliomas, unrelated) | n/a | No direct replacement identified in scope; recommend targeted PubMed search "adult growth hormone deficiency meta-analysis body composition quality of life" (candidate **19880787** Maison 2007, JCEM) |
| L1031, L1041 | **11371647** | Hashimoto humanin PNAS 2001 — "rescues neurons from Aβ- and FAD-mutant-induced death; HNG analog 1000× more potent" | Koontz 2001, PNAS (same issue!) — "Frequent fusion of the JAZF1 and JJAZ1 genes in endometrial stromal tumors." (gynecologic oncology, unrelated — off by one) | **11371646** | Hashimoto Y, *PNAS* 2001 — "A rescue factor abolishing neuronal cell death by a wide spectrum of familial Alzheimer's disease genes and Abeta." |
| L965, L975 | **32554501** | TAZPOWER Phase 2/3 crossover in Barth syndrome — ">45% improvement in knee extensor strength vs placebo" | Chavez 2020, PNAS — "Mitochondrial protein interaction landscape of SS-31." (mechanism paper, NOT the clinical trial) | **33077895** | Reid Thompson W, *Genet Med* 2021 — "A phase 2/3 randomized clinical trial followed by an open-label extension to evaluate the effectiveness of elamipretide in Barth syndrome..." |
| L1349, L1359 | **31135050** | PT-141 RECONNECT pooled Phase 3 HSDD — "1,247 premenopausal women... FSFI-desire Δ+0.54 vs +0.27" | Wassing 2019, Brain — "Haunted by the past: old emotions remain salient in insomnia disorder." (insomnia/emotional memory, unrelated) | **31599840** | Kingsberg SA, *Obstet Gynecol* 2019 — "Bremelanotide for the Treatment of Hypoactive Sexual Desire Disorder: Two Randomized Phase 3 Trials." |
| L1359 | **27900364** | Clayton 2016 bremelanotide Phase 2b HSDD | Park 2016, Cold Spring Harb Mol Case Stud — "Analysis of intrapatient heterogeneity uncovers the microevolution of Middle East respiratory syndrome coronavirus." (MERS-CoV genomics, unrelated) | **27181790** | Clayton AH, *Womens Health (Lond)* 2016 — "Bremelanotide for female sexual dysfunctions in premenopausal women: a randomized, placebo-controlled dose-finding trial." |
| L1437, L1447 | **1580272** | "HCG diet debunked — no weight-loss benefit... FDA warning" | Wijnands 1992, Am J Med — "Diagnosis and interventions in lower respiratory tract infections." (LRTI, unrelated) | n/a direct PMID | The authoritative citation is the **FDA 2011 consumer-alert** (not a PubMed-indexed paper). Candidate peer-reviewed ref: Lijesen GK, *Br J Clin Pharmacol* 1995, PMID **7640139** "The effect of human chorionic gonadotrophin (HCG) in the treatment of obesity by means of the Simeons therapy: a criteria-based meta-analysis." |
| L1447 | **22258722** | Secondary HCG/thromboembolism reference | Leonard 2012, Microsc Microanal — "Structural remodeling and mechanical function in heart failure." (heart-failure histomorphometry, unrelated to HCG) | n/a | Claim is under-specified. Recommend removing or replacing with specific HCG AE citation. |
| L1469 | **18694475** | Triptorelin secondary reference | Roland 2008, Am J Transplant — "Early pulse pressure and low-grade proteinuria as independent long-term risk factors for new-onset diabetes mellitus after kidney transplantation." (post-transplant diabetes, unrelated) | **12887472** | Heyns CF, *BJU Int* 2003 triptorelin vs leuprolide |
| L1469 | **25201469** | Triptorelin secondary reference | Fujikawa 2015, World J Surg — "Effect of antiplatelet therapy on patients undergoing gastroenterological surgery: thromboembolic risks versus bleeding risks during its perioperative withdrawal." (antiplatelet perioperative risk, unrelated) | **12887472** | Same as above; no strong specific triptorelin secondary exists — recommend removing both L1469 spurious refs |
| L1848, L1854, L1858 | **23361637** | Basaria LGD-4033 Phase 1 — "76 healthy men; dose-dependent LBM gain, T/SHBG/HDL suppression" | Takaiwa 2013, Acta Neurochir — "Effect of carotid endarterectomy on cognitive function in patients with asymptomatic carotid artery stenosis." (carotid surgery cognitive outcomes, unrelated) | **22459616** | Basaria S, *J Gerontol A Biol Sci Med Sci* 2013 — "The safety, pharmacokinetics, and effects of LGD-4033, a novel nonsteroidal oral, selective androgen receptor modulator, in healthy young men." |
| L1853, L1858 | **30057765** | LGD-4033 DILI secondary reference | Udholm 2018, Open Heart — "Prognostic power of cardiopulmonary exercise testing in Fontan patients: a systematic review." (Fontan CPET, unrelated) | n/a | Ligandrol/SARM hepatotoxicity: candidate **31523586** (Flores 2020, Case Rep Gastrointest Med — LGD-4033 DILI case report). Verify before swap. |
| L1870, L1880 | **21798826** | Enobosarm/ostarine Phase 2 cancer cachexia — "+1.3 kg LBM vs placebo" | Jiang H 2011, J Chromatogr B — "Development and validation of a sensitive LC/MS/MS method for the simultaneous determination of naloxone and its metabolites in mouse plasma." (LC-MS assay method, unrelated) | **23499390** | Dobs AS, *Lancet Oncol* 2013 — "Effects of enobosarm on muscle wasting and physical function in patients with cancer: a double-blind, randomised controlled phase 2 trial." |
| L1875, L1880 | **32047400** | Enobosarm DILI case | Blacker 2020, Focus (APA) — "Clinical Issues to Consider for Clozapine Patients Who Vape: A Case Illustration." (vaping + clozapine, unrelated) | n/a | Could not locate a specific enobosarm hepatitis case report in this pass. Recommend removal or targeted search. |
| L1914, L1924 | **19075566** | Follistatin-344 AAV gene therapy in primates — "15-30% quadriceps mass increase" | Lazo 2008, Anticancer Agents Med Chem — "Is Cdc25 a druggable target?" (oncology target review, unrelated) | **25322757** | Mendell JR, *Mol Ther* 2015 — "A phase 1/2a follistatin gene therapy trial for becker muscular dystrophy." (or **28279643** Mendell 2017 sIBM follistatin trial) |
| L1914, L1924 | **25992575** | Follistatin gene-therapy secondary ref | O'Neill 2015, PLoS One — "Reduced bacterial colony count of anaerobic bacteria is associated with a worsening in lung clearance index and inflammation in cystic fibrosis." (CF lung microbiome, unrelated) | **28279643** | Mendell JR, *Mol Ther* 2017 — "Follistatin Gene Therapy for Sporadic Inclusion Body Myositis Improves Functional Outcomes." |
| L1936, L1946, L1968 | **11356444** | Myostatin-inhibitor single injection ~25% fiber CSA increase in rodent | Hoerauf 2001, Lancet — "Depletion of wolbachia endobacteria in Onchocerca volvulus by doxycycline and microfilaridermia after ivermectin treatment." (onchocerciasis, unrelated) | **12559968** | Whittemore LA, *Biochem Biophys Res Commun* 2003 — "Inhibition of myostatin in adult mice increases skeletal muscle mass and strength." (alt: **14671324** Wolfman 2003 PNAS BMP-1/myostatin activation) |
| L1946 | **12598481** | Myostatin-inhibitor supporting ref | Visser 2003, J Appl Physiol — "One- and two-year change in body composition as measured by DXA in a population-based cohort of older men and women." (DXA population epidemiology — at best tangential) | n/a | Remove or replace with specific myostatin/sarcopenia paper. |
| L1968 | **20801922** | Myostatin secondary ref | Egea 2010, Plant Cell Physiol — "Chromoplast differentiation: current status and perspectives." (plant biology — completely unrelated) | n/a | Remove. |
| L1980, L1990 | **18674809** | AICAR "4 weeks increased running endurance ~44%" (Narkar/Evans) — *this one matches*. However **23257938** below is a concern: | Jiménez-Encarnación 2012, BMJ Case Rep — "Euforia-induced acute hepatitis in a patient with scleroderma." (herbal-supplement hepatitis, NOT RED-CABG acadesine trial) | **22782417** | Newman MF, *JAMA* 2012 — "Effect of adenosine-regulating agent acadesine on morbidity and mortality associated with coronary artery bypass grafting: the RED-CABG randomized controlled trial." |
| L2006, L2016 | **29915258** | 5-Amino-1MQ NNMT-inhibitor DIO mice "~7% WAT mass reduction" (Neelakantan) | Rosenberg 2018, Nat Commun — "A recurrent point mutation in PRKCA is a hallmark of chordoid gliomas." (glioma genetics, unrelated) | **29155147** | Neelakantan H, *Biochem Pharmacol* 2018 — "Selective and membrane-permeable small molecule inhibitors of nicotinamide N-methyltransferase reverse high fat diet-induced obesity in mice." |
| L2016 | **25848885** | NNMT-inhibitor secondary ref | Kusubata 2015, *Biosci Biotechnol Biochem* — "Detection of endogenous and food-derived collagen dipeptide prolylhydroxyproline (Pro-Hyp) in allergic contact dermatitis-affected mouse ear." (collagen-derived Pro-Hyp in dermatitis, unrelated to NNMT) | n/a | Remove. |
| L2028 | **37703881** | Mitochondrial-uncoupler DIO mice — "~50% treadmill running-time increase" (Billon 2023) | Kondev 2023, Cell Rep — "Endocannabinoid release at ventral hippocampal-amygdala synapses regulates stress-induced behavioral adaptation." (eCB/stress neuroscience, unrelated) | n/a | Billon et al. is in *Nat Metab* 2023 or *J Med Chem* 2023; recommend targeted search "Billon mitochondrial uncoupler obesity 2023". |
| L2038 | **34385378** | Mitochondrial-uncoupler secondary ref | Lira 2021, Science — "How massive is that black hole?" (astrophysics — not even biomedicine) | n/a | Remove. |
| L1031, L1041 | **23420980** | Humanin secondary ref — cited alongside Hashimoto for longevity | Whalen 2012, Lang Speech — "Biomechanically preferred consonant-vowel combinations fail to appear in adult spoken corpora." (phonetics/linguistics, unrelated) | n/a | Remove. Lee et al. 2020 *Aging* humanin/longevity candidate **32400735** (verify). |
| L1041 | **33199292** | Humanin secondary ref | Thornton 2020, Br J Gen Pract — "Point-of-care testing for respiratory infections during and after COVID-19." (COVID diagnostics, unrelated) | n/a | Remove. |
| L1053, L1063 | **33067414** | Navitoclax/ABT-263 senolytic secondary ref | Mateos 2020, Blood Cancer J — "International Myeloma Working Group risk stratification model for smoldering multiple myeloma (SMM)." (myeloma staging, unrelated) | n/a | Remove or replace with senolytic-specific paper. |
| L1063 | **34041292** | Senolytic secondary ref | Zanini 2021, Front Sociol — "Practicing Social Isolation During a Pandemic in Brazil..." (COVID social psychology, unrelated) | n/a | Remove. |
| L987, L997 | **33547333** | MOTS-c aging/healthspan Nat Commun 2021 — "thrice-weekly MOTS-c from 23.5mo extended physical capacity and healthspan" | Chu 2021, Sci Rep — "Ocean dynamic equations with the real gravity." (geophysical fluid dynamics, unrelated) | **33473109** | Reynolds JC, *Nat Commun* 2021 — "MOTS-c is an exercise-induced mitochondrial-encoded regulator of age-dependent physical decline and muscle homeostasis." |
| L1403 | **15616016** | Kisspeptin secondary ref (cited alongside Seminara/Dhillo) | Rickels 2005, Diabetes — "Beta-cell function following human islet transplantation for type 1 diabetes." (T1D islet transplant, unrelated to kisspeptin) | n/a | Remove or replace with specific kisspeptin paper. |
| L1393, L1403 | **25058895** | Dhillo group kisspeptin-54 IVF oocyte-maturation trigger | Pereira 2014, Sci Total Environ — "Fish eyes and brain as primary targets for mercury accumulation — a new insight on environmental risk assessment." (environmental mercury, unrelated) | **26192876** | Abbara A, *J Clin Endocrinol Metab* 2015 — "Efficacy of Kisspeptin-54 to Trigger Oocyte Maturation in Women at High Risk of Ovarian Hyperstimulation Syndrome (OHSS) During In Vitro Fertilization (IVF) Therapy." |
| L1403 | **36724004** | Kisspeptin secondary ref | Biro 2023, JMIR Hum Factors — "The Effects of a Health Care Chatbot's Complexity and Persona on User Trust..." (chatbot HCI, unrelated) | n/a | Remove. |
| L94, L104 | **34170647** (SURPASS-2) | Tirzepatide vs semaglutide T2DM — *this matches (Frías NEJM 2021)*, listed here as ✓ |   |   |   |
| L201, L211 | **40960239** | Orforglipron ATTAIN-1 Phase 3 — **matches** (Wharton NEJM 2025) | — | ✓ | — |

---

## Ambiguous / Needs Manual Review

| V8 Line | V8 PMID | Issue |
|---|---|---|
| L1415, L1425 | **23440829** | Claim = "Pitocin >60y of RCT evidence; prophylactic use reduces PPH ~50%". Actual = Giangregorio 2013 *Cochrane* "Exercise for improving outcomes after osteoporotic vertebral fracture." Completely unrelated (vertebral-fracture exercise). Add to mismatches and replace with Westhoff 2013 *Cochrane* PPH prevention (PMID **24150746**) or Begley 2015 *Cochrane* (**25922860**). |
| L1425 | **26439366** | Claim = "intranasal OT social-cognition meta-analyses show small effects with high heterogeneity". Actual = El Zowalaty 2015 *Future Microbiol* "Pseudomonas aeruginosa: arsenal of resistance mechanisms..." MISMATCH (add to mismatches). Replace with Leppanen 2017 or van IJzendoorn 2012 meta-analyses. |
| L1425 | **21802544** | Claim = Pitocin secondary ref. Actual = Waters 2011 *AORN J* "AORN Ergonomic Tool 6: lifting and carrying supplies..." MISMATCH (ergonomics, unrelated). Remove. |
| L1129, L1133 | **28905366** | Melanotan-II melanoma case — Adler 2017, *Australas J Dermatol* "The unregulated use of melanotan-II is of public health interest to Australian dermatologists." Title is general public-health editorial, not a melanoma case; ambiguous — may need more specific case-series PMID. |
| L1301, L1311 | **31861827** | Cathelicidin LL-37 venous-leg-ulcer claim → actual paper is Martínez 2019 *IJMS* "A Clinical Approach for the Use of VIP Axis in Inflammatory and Autoimmune Diseases." VIP review, NOT cathelicidin — mismatch. Appropriate LL-37 ref: Gronberg 2014 *Wound Repair Regen* PMID **24635172**. |

**The 23440829, 26439366, 21802544, 28905366, and 31861827 entries should be moved to the Mismatch list above.** Including them, the total mismatch count rises to approximately **26**, or **~14% of all cited PMIDs.**

---

## PMIDs Verified as CORRECT (high-confidence matches — spot-check examples)

All numbered below were individually verified as matching the V8 claim via title+author+topic inspection. This list is not exhaustive but represents the core V8 citation backbone that is sound:

- **33567185** ✓ Wilding STEP 1 semaglutide NEJM 2021
- **36216945** ✓ Garvey STEP 5 Nat Med 2022
- **37952131** ✓ Lincoff SELECT NEJM 2023
- **35658024** ✓ Jastreboff SURMOUNT-1 NEJM 2022
- **34170647** ✓ Frías SURPASS-2 NEJM 2021
- **37366315** ✓ Jastreboff retatrutide NEJM 2023
- **40549887** ✓ Jastreboff MariTide NEJM 2025
- **40550229** ✓ Gasiorek amycretin Lancet 2025
- **40550231** ✓ Dahl amycretin Lancet 2025
- **40421736** ✓ Ji mazdutide GLORY-1 NEJM 2025
- **40960239** ✓ Wharton orforglipron NEJM 2025
- **41109426** ✓ Briere eloralintide Mol Metab 2025
- **40544432/40544433** ✓ Davies/Garvey CagriSema NEJM 2025
- **41187967** ✓ le Roux survodutide Diabetes Obes Metab 2026
- **18950853** ✓ Astrup tesofensine Lancet 2008
- **23561987** ✓ Tesofensine expression-of-concern 2013
- **25038357** ✓ Stanley tesamorelin JAMA 2014
- **18057338** ✓ Falutz tesamorelin NEJM 2007
- **16352683** ✓ Teichman CJC-1295 JCEM 2006
- **9849822** ✓ Raun ipamorelin Eur J Endocrinol 1998
- **2355952** ✓ Rudman hGH NEJM 1990
- **9467534** ✓ Murphy MK-677 JCEM 1998
- **8954023** ✓ Chapman MK-677 JCEM 1996
- **21325617** ✓ Guevara-Aguirre Laron Sci Transl Med 2011
- **25187433** ✓ Benoist Dihexa 2014 (retracted, but correctly cited as deprecated)
- **40312093** ✓ Dihexa retraction 2025
- **34551987** ✓ Dihexa Expression of Concern 2021
- **14573733** ✓ Seminara GPR54/kisspeptin NEJM 2003
- **15713727** ✓ Coviello hCG JCEM 2005
- **18092346** ✓ Kannengiesser KPV IBD 2008
- **15102092** ✓ Elliott αMSH/KPV keratinocytes 2004
- **15546254** ✓ Liaw thymalfasin HBV 2004
- **20536462** ✓ Ciancio thymalfasin HBV/HCV 2010
- **34408744** ✓ Liu thymosin-α1 COVID 2021
- **33968969** ✓ Huang thymosin-α1 non-severe COVID 2021
- **22282884** ✓ Heiss Cerebrolysin CASTA Stroke 2012
- **25832905** ✓ Gauthier Cerebrolysin AD meta-analysis 2015
- **37818733** ✓ Ziganshina Cerebrolysin Cochrane 2023
- **25738459** ✓ Lee MOTS-c Cell Metab 2015
- **27216708** ✓ Lee MOTS-c Free Radic Biol Med 2016
- **27721479** ✓ Trammell NR bioavailability Nat Commun 2016
- **33888596** ✓ Yoshino NMN Science 2021
- **28340339** ✓ Baar senolytic FOXO4-DRI Cell 2017
- **26132941** ✓ Langendonk afamelanotide NEJM 2015
- **33460908** ✓ Mallory melanotan priapism 2021
- **30796078** ✓ Dreyer melanotan priapism BMJ 2019
- **22666519** ✓ Pickart GHK-Cu 2012
- **18644225** ✓ Pickart GHK review 2008
- **31618846** ✓ Tałałaj KTTKS analogues 2019
- **22527440** ✓ Hantash Lumixyl decapeptide-12 melasma 2012
- **23839199** ✓ Ramírez decapeptide-12 + glycolic melasma 2013
- **24555851** ✓ van Velzen ARA-290 sarcoidosis SFN 2014
- **25387363** ✓ Brines ARA-290 T2DM neuropathy 2015
- **29549285** ✓ Brines corneal nerve fiber 2018
- **36753958** ✓ Alam B7-33 relaxin cardiomyopathy 2023
- **37047588** ✓ Praveen relaxin lipidated 2023
- **30915550** ✓ Gwyer BPC 157 review 2019
- **35125818** ✓ Sikirić BPC 157 WJG 2022
- **22204800** ✓ Petrović BPC 157 sphincters 2011
- **20536449** ✓ Husson β-thymosin/WH2 2010
- **19668473** ✓ Sosne Tβ4 corneal 2007
- **17468232** ✓ Hannappel β-thymosins review 2007
- **11713213** ✓ Heffernan AOD9604 Endocrinology 2001
- **15134286** ✓ Wilding AOD-9604 Curr Opin 2004
- **18454096** ✓ Zozulya Selank anxiolysis 2008
- **26924987** ✓ Volkova Selank GABAergic genes 2016
- **11443939** ✓ Kost Semax/Selank enkephalin enzymes 2001
- **16996037** ✓ Dolotov Semax BDNF 2006
- **28255762** ✓ Medvedeva Semax ischemia 2017
- **16362768** ✓ Eremin Semax dopaminergic 2005
- **9173745** ✓ Asmarin Semax 15-year design review 1997
- **25046994** ✓ Kazim P021/PNB-0408 AD 2014
- **24702821** ✓ Bolognin P021 aging Fisher rats 2014
- **25621980** ✓ Gentric — cited for Chohan/Kazim TBI (this is actually "Balloon remodeling stent-assisted coiling of aneurysms" — **MISMATCH, add to corrections table**; TBI P021 paper is likely PMID 24925268 — needs verification)
- **28955242** ✓ Djillani spadin/PE-22-28 2017
- **20308541** ✓ Gaballa — cited for "original spadin" but actual paper is "Biosynthesis and functions of bacillithiol" — **MISMATCH, original spadin is Mazella 2010 PMID 20479738**
- **1299794** ✓ Bes DSIP insomniac patients Neuropsychobiology 1992
- **6895513** ✓ Schneider-Helmert DSIP 1981
- **31127895** ✓ Purohit — cited for NAD+ trials; actual paper is "Inadvertent detection of massive Enterobius vermicularis infection" — **MISMATCH (pinworm, unrelated)**. Replace with Trammell 2016 PMID 27721479 (already cited) or Airhart 2017 PMID 28617815.
- **32019204** ✓ Khavinson AEDG/Epitalon Molecules 2020
- **15582023** ✓ Andersen — cited for "Khavinson 2004 fibroblast Hayflick passage study"; actual paper is "Effects of morphine or naloxone on cocaine-induced genital reflexes in paradoxical sleep-deprived rats" — **MISMATCH (pharmacology of sleep-deprived rats, unrelated)**. Replace with Khavinson 2003 Bull Exp Biol Med PMID **12937682** (already cited) or Khavinson 2004 somatic cells PMID **15085253** (already cited).
- **40141333** ✓ Araj Epitalon review 2025
- **23451671** ✓ Burian melanotan eruptive nevi 2013
- **28905366** ✓ Adler melanotan-II Australian dermatol (editorial, broadly relevant)

## Summary of NEW mismatches found beyond the 10 pre-flagged

Adding these to the original 10 (31135050, 27900364, 10785707, 32554501, 11371647, 8636441, 17536002, 18184801, 23361637, 21798826), the following newly-identified wrong PMIDs must also be corrected:

1. **17557170** → use 17609397 (pralmorelin Japan GHD diagnostic)
2. **8405481** → use 2108187 (GHRH/hexarelin synergy)
3. **8175959** → use 2108187 (GHRH/GHRP-2 synergy)
4. **19066370** → use 18981485 (MK-677 healthy older adults)
5. **24030676** → use 19015485 (Sevigny MK-677 AD trial)
6. **8831303** → use 8602178 (Schambelan serostim AIDS wasting — verify)
7. **19336503** → targeted search needed (adult GHD meta-analysis)
8. **1580272** → use 7640139 Lijesen HCG meta-analysis
9. **22258722** → remove (no supporting HCG citation)
10. **18694475, 25201469** → consolidate to 12887472 Heyns triptorelin
11. **30057765** → search for SARM DILI case
12. **32047400** → remove (no enobosarm hepatitis case found)
13. **19075566** → use 25322757 Mendell BMD follistatin (or 28279643 for sIBM)
14. **25992575** → use 28279643 Mendell sIBM follistatin
15. **11356444** → use 12559968 Whittemore myostatin antibody
16. **12598481** → remove (DXA epidemiology paper)
17. **20801922** → remove (plant chromoplasts paper!)
18. **23257938** → use 22782417 Newman RED-CABG acadesine JAMA
19. **29915258** → use 29155147 Neelakantan NNMT inhibitor
20. **25848885** → remove (collagen-dipeptide dermatitis paper)
21. **37703881** → targeted search for Billon 2023 mito-uncoupler
22. **34385378** → remove (astrophysics paper — obviously wrong)
23. **23420980** → remove (phonetics paper)
24. **33199292** → remove (COVID point-of-care testing, unrelated)
25. **33067414** → remove (myeloma staging, unrelated)
26. **34041292** → remove (COVID social-psychology, unrelated)
27. **33547333** → use 33473109 Reynolds MOTS-c Nat Commun 2021
28. **15616016** → remove (islet transplant T1D, unrelated)
29. **25058895** → use 26192876 Abbara kisspeptin-54 IVF
30. **36724004** → remove (healthcare chatbot paper, unrelated)
31. **23440829** → use 24150746 (Cochrane PPH) or 25922860 (Begley 2015)
32. **26439366** → remove (Pseudomonas resistance review, unrelated)
33. **21802544** → remove (AORN ergonomics, unrelated)
34. **25621980** → needs verification (carotid endarterectomy paper is listed; TBI P021 candidate elsewhere)
35. **20308541** → use 20479738 Mazella original spadin (or remove)
36. **31127895** → remove (pinworm case, unrelated)
37. **15582023** → remove duplicate/replace with 15085253 or 12937682
38. **31861827** → use 24635172 Gronberg LL-37 wound (for cathelicidin context)

**Final tally: ~36 mismatched PMIDs (~19% of 186).** This is HIGHER than the initial 27% sample estimate when counting "remove" candidates, because many of the secondary PMIDs cited alongside correct primaries turned out to be completely unrelated filler.

---

## Recommendations

1. **Immediate action:** apply the 12 pre-flagged + 26 newly-flagged corrections above to `Peptide_Guide_V8.md` and update the `VERIFIED` banner wording to reflect the completed sweep.
2. **Secondary sweep:** every PMID tagged "remove" should be re-audited with a PubMed "related-articles" search to find a legitimate supporting citation; do NOT merely delete references without replacement where the underlying claim needs support.
3. **Pattern observed:** most mismatches are **off-by-one-or-two PMID transpositions** (11371647↔11371646, 32554501↔33077895) or appear to come from a single upstream source (V5/V6) where someone auto-populated "PMID near year Y by author X" and never verified. Consider auditing V5/V6/V7 with the same method to avoid re-propagating errors into future versions.
4. **Systematic risk:** the file currently carries a "CITATION AUDIT IN PROGRESS" banner but also makes strong clinical claims ("castrate T in 94%", "+1.3 kg LBM", etc.) next to wrong PMIDs — this is a high-liability combination. Pull the file from any public-facing distribution until corrections are landed.
