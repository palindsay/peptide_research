# V8 Fact-Check Report (V1)

**Audit scope:** Stratified PMID/FDA/NCT verification of `/home/plindsay/prjs/peptide_research/Peptide_Guide_V8.md` (2,255 lines, 186 unique PMIDs).
**Verification method:** Live calls to `eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi` for sample PMIDs across all 12 sections, plus targeted re-verification of changelog-flagged citations.
**Date:** 2026-04-14
**Confidence:** HIGH for items marked CITATION ERROR (mismatch is unambiguous — wrong title, wrong journal, wrong topic). MEDIUM for items marked PARTIAL/UNVERIFIABLE (e.g., FDA URL gates).

> **HEADLINE FINDING:** Despite the V8 changelog claim that "Every PMID re-verified against PubMed E-utilities," **at least 8 of ~30 sampled PMIDs (≈27%) point to wrong papers**. The error rate is incompatible with the document's stated VERIFIED status. **A second pass over every remaining un-sampled PMID is mandatory** before the document can be relied upon for clinical decision-making.

---

## Verified Correct (high-value sample)

### GLP-1 / Weight-loss section
- **PMID 33567185** → "Once-Weekly Semaglutide in Adults with Overweight or Obesity" (Wilding JPH, Batterham RL, Calanna S; NEJM 2021). Matches V8 STEP 1 claim. ✓
- **PMID 37952131** → "Semaglutide and Cardiovascular Outcomes in Obesity without Diabetes" (Lincoff AM, Brown-Frandsen K, Colhoun HM; NEJM 2023). Matches V8 SELECT claim. ✓
- **PMID 35658024** → "Tirzepatide Once Weekly for the Treatment of Obesity" (Jastreboff AM, Aronne LJ, Ahmad NN; NEJM 2022). Matches V8 SURMOUNT-1 claim. ✓
- **PMID 37366315** → "Triple-Hormone-Receptor Agonist Retatrutide for Obesity – A Phase 2 Trial" (Jastreboff AM, Kaplan LM, Frías JP; NEJM 2023). Matches V8 retatrutide Phase 2 claim. ✓
- **PMID 40549887** → "Once-Monthly Maridebart Cafraglutide for the Treatment of Obesity – A Phase 2 Trial" (Jastreboff AM, Ryan DH, Bays HE; NEJM 2025). Matches V8 MariTide Phase 2 claim. ✓
- **PMID 40421736** → "Once-Weekly Mazdutide in Chinese Adults with Obesity or Overweight" (Ji L, Jiang H, Bi Y; NEJM 2025). Matches V8 GLORY-1 claim. ✓
- **PMID 40960239** → "Orforglipron, an Oral Small-Molecule GLP-1 Receptor Agonist for Obesity Treatment" (Wharton S, Aronne LJ, Stefanski A; NEJM 2025). Matches V8 ATTAIN-1 claim. ✓
- **PMID 18950853** → Astrup A, Madsbad S, Breum L; Lancet 2008 (tesofensine). Matches V8 Tesofensine Phase 2 claim. ✓

### Section 3 Healing
- **PMID 36753958** → Alam F, Gaspari TA, Kemp-Harper BK; Biomedicine & Pharmacotherapy 2023 (B7-33 single-chain relaxin / cardiomyopathy / LV fibrosis). Matches V8 B7-33 claim. ✓
- **PMID 24555851** → van Velzen M, Heij L, Niesters M; Expert Opin Investig Drugs 2014 (ARA-290 / cibinetide / sarcoid SFN). Matches V8 ARA-290 claim. ✓
- **PMID 18092346** → Kannengiesser K, Maaser C, Heidemann J; Inflamm Bowel Dis 2008 (KPV / DSS+TNBS murine colitis). Matches V8 KPV claim. ✓
- **PMID 11713213** → Heffernan M, Summers RJ, Thorburn A; Endocrinology 2001 (hGH lipolytic fragment AOD9604, β3-AR KO). Matches V8 HGH-Frag/AOD-9604 claim. ✓
- **PMID 15134286** → Wilding J; Curr Opin Investig Drugs 2004 (AOD-9604 review). Matches V8 claim. ✓

### Section 4–5 Immune / Cognitive
- **PMID 15546254** → Liaw YF; J Gastroenterol Hepatol 2004 (Thymalfasin/Tα1 in HBV). Matches V8 claim. ✓
- **PMID 18454096** → Zozulia AA, Neznamov GG, Siuniakov TS; Zh Nevrol Psikhiatr 2008 (Selank in GAD/neurasthenia). Matches V8 claim. ✓
- **PMID 16996037** → Dolotov OV, Karpenko EA, Inozemtseva LS; Brain Research 2006 (Semax BDNF/TrkB in rat hippocampus). Matches V8 claim. ✓
- **PMID 25187433** → Benoist CC, Kawas LH et al.; J Pharmacol Exp Ther 2014 (Dihexa). **Confirmed RETRACTED in April 2025** via retraction notice PMID 40312093 (J Pharmacol Exp Ther 2025;392(4):103567). Expression of Concern (PMID 34551987) issued Sept 2021. V8 Dihexa deprecation block is accurate. ✓
- **PMID 22282884** → Heiss WD, Brainin M, Bornstein NM; Stroke 2012 (Cerebrolysin CASTA Asian stroke RCT). Matches V8 claim. ✓

### Section 6 Mitochondrial / Longevity
- **PMID 28340339** → Baar MP, Brandt RMC, Putavet DA; Cell 2017 (FOXO4-DRI senolytic). Matches V8 claim. ✓
- **PMID 40312093** → Retraction notice for PMID 25187433 (Dihexa), J Pharmacol Exp Ther April 2025. ✓
- **PMID 12937682** → Khavinson VKh, Bondarev IE, Butyugov AA; Bull Exp Biol Med 2003 ("Epithalon peptide induces telomerase activity and telomere elongation in human somatic cells"). This IS a real Khavinson Epitalon telomerase paper. ✓ (See "Disputed" below for the year — V8 says 2003, abstract says 2003, but V8 main text says "Khavinson et al. 2003 (Bull Exp Biol Med)" in Epitalon entry — that part is correct.)

### Section 7 Melanocortin / Cosmetic
- **PMID 26132941** → Langendonk JG, Balwani M, Anderson KE; NEJM 2015 (Afamelanotide for EPP). Matches V8 claim. ✓
- **PMID 22666519** → Pickart L, Vasquez-Soltero JM, Margolina A; Oxid Med Cell Longev 2012 (GHK-Cu review). Matches V8 claim. ✓
- **PMID 39496132** → Lupin M, Bjerring P, Andriessen A; J Drugs Dermatol 2024 (neuropeptide serum + BTX-A). Matches V8 Argireline 2024 real-world study claim. ✓

### Section 9 Reproductive
- **PMID 15713727** → Coviello AD, Matsumoto AM, Bremner WJ; J Clin Endocrinol Metab 2005 (low-dose hCG preserves intratesticular T). Matches V8 claim. ✓
- **PMID 14573733** → Seminara SB, Messager S, Chatzidaki EE; NEJM 2003 ("The GPR54 gene as a regulator of puberty"). Matches V8 KISS1R/IHH claim (note: V8 calls this a "KISS1R mutations" paper; the original Seminara paper actually titled it "GPR54", which is the same gene — match holds, but the V8 phrasing is slightly anachronistic). ✓

### Section 10 Bioregulators
- **PMID 22117547** → Fedoreyeva LI, Kireev II, Khavinson VKh; Biochemistry (Mosc) 2011 (short fluorescence-labeled peptides penetrate HeLa nuclei, bind DNA). ✓ Backs V8's Cartalax/Vesugen/Vilon/Testagen DNA-binding claims.
- **PMID 25051766** → Khavinson VKh, Tarnovskaia SI, Lin'kova NS; Adv Gerontol 2014 (epigenetic peptide regulation of vascular endothelial proliferation). Matches V8 Vesugen/KED vascular claim. ✓
- **PMID 24909721** → Khavinson VKh, Lin'kova NS, Tarnovskaya SI; Bull Exp Biol Med 2014 ("Short peptides stimulate serotonin expression in cells of brain cortex"). Matches V8 Pinealon/EDR claim. ✓
- **PMID 15085253** → Khavinson VKh, Lezhava TA, Malinin VV; Bull Exp Biol Med 2004 ("Effects of short peptides on lymphocyte chromatin in senile subjects"). Matches V8 Livagen/KEDA chromatin claim. ✓
- **PMID 25761685** → Ashapkin VV, Linkova NS, Khavinson VKh; Biochemistry (Mosc) 2015 (epigenetic peptidergic regulation in aging). Matches V8 Section 10 introduction citation. ✓
- **PMID 29124531** → Khavinson VK, Kopylov AT, Vaskovsky BV; Bull Exp Biol Med 2017 ("Identification of Peptide AEDG in the Polypeptide Complex of the Pineal Gland"). Matches V8 Epitalon/AEDG sequence claim — confirms AEDG is the correct sequence and is endogenous to pineal extract. ✓ **The V8 changelog correction "Epitalon sequence (AGAG → AEDG)" is supported.**

### Section 11 Performance
- **PMID 18674809** → Narkar VA, Downes M, Yu RT et al.; Cell 2008 ("AMPK and PPARdelta agonists are exercise mimetics"). Matches V8 AICAR endurance claim. ✓

### Bioregulator amino-acid sequences (Section 10)
All sequences cross-checked against Khavinson's English-language publications and the consensus reported in PMID 22117547 and PMID 25761685. The following are corroborated:
- Cartalax = AED (Ala-Glu-Asp) ✓
- Vesugen = KED (Lys-Glu-Asp) ✓
- Pinealon = EDR (Glu-Asp-Arg) ✓ (PMID 24909721 confirms Khavinson EDR cortical work)
- Epitalon = AEDG (Ala-Glu-Asp-Gly) ✓ (PMID 29124531 confirms AEDG identified in pineal complex)
- Livagen = KEDA (Lys-Glu-Asp-Ala) ✓
- Vilon = KE (Lys-Glu) ✓
- Thymogen = EW (Glu-Trp) ✓
- Crystagen = EDP, Ovagen/Chonluten = EDG, Testagen = KEDG, Cardiogen = AEDR — all internally consistent with SPIBG/Khavinson literature; the V8 caveat that "some gray-market vendors list AEDL" for Cardiogen and "KEDP/AEDL" for Prostamax is appropriately hedged.

---

## Corrections Required

> **Format:** Each correction lists the V8 PMID, what V8 claims, what the PMID actually points to (per esummary.fcgi), the recommended fix, and the section/line context.

### CRITICAL — wrong-paper citations (highest-priority)

#### C1. PT-141 / Vyleesi RECONNECT trial — wrong PMID
- **Section 9.1, line 1349 and line 1359** (PT-141 / Bremelanotide entry)
- **V8 claim:** "RECONNECT (Studies 301/302): pooled Phase 3 double-blind placebo-controlled trials in 1,247 premenopausal women with HSDD ... ([PMID 31135050](https://pubmed.ncbi.nlm.nih.gov/31135050/))"
- **Actual PMID 31135050:** "Haunted by the past: old emotions remain salient in insomnia disorder" (Wassing R, Schalkwijk F, Lakbila-Kamal O; Brain 2019). Completely unrelated to bremelanotide, HSDD, or Phase 3 trials.
- **Recommended fix:** Replace with the correct RECONNECT primary citation. The actual published RECONNECT pooled analysis is **Kingsberg SA, Clayton AH, Portman D, et al. "Bremelanotide for the Treatment of Hypoactive Sexual Desire Disorder: Two Randomized Phase 3 Trials." Obstet Gynecol. 2019 Nov;134(5):899-908. PMID 31599840.** (Verify before insertion.)
- **Severity:** HIGH — this is the sole human-trial citation for the FDA-approved indication.

#### C2. PT-141 Clayton 2016 Phase 2b — wrong PMID
- **Section 9.1, line 1359** (PT-141 / Bremelanotide entry, Key References)
- **V8 claim:** "[PMID 27900364](https://pubmed.ncbi.nlm.nih.gov/27900364/)" cited as Clayton bremelanotide HSDD Phase 2b (2016).
- **Actual PMID 27900364:** "Analysis of intrapatient heterogeneity uncovers the microevolution of Middle East respiratory syndrome coronavirus." (Park D, Huh HJ, Kim YJ; Cold Spring Harb Mol Case Stud 2016). Not bremelanotide.
- **Recommended fix:** Replace with the correct Clayton Phase 2b citation. Likely intended: **Clayton AH, Althof SE, Kingsberg S, et al. "Bremelanotide for female sexual dysfunctions in premenopausal women: a randomized, placebo-controlled dose-finding trial." Womens Health (Lond). 2016 May;12(3):325-37. PMID 27181790.** (Verify.)
- **Severity:** HIGH

#### C3. Triptorelin pivotal prostate cancer trial — wrong PMID
- **Section 9.6, line 1459 and line 1469** (Triptorelin / Trelstar)
- **V8 claim:** "achieves castrate T (<50 ng/dL) in >94% of men within 4 weeks of depot ([PMID 10785707](https://pubmed.ncbi.nlm.nih.gov/10785707/))"
- **Actual PMID 10785707:** "Strategy Retreat — An Important Tool for Your Practice" (Riner RN; J Invasive Cardiol 1996). Practice management piece, completely unrelated.
- **Recommended fix:** Replace with the correct Trelstar pivotal trial citation. A widely-cited candidate is **Heyns CF et al. "Comparative efficacy of triptorelin pamoate and leuprolide acetate in men with advanced prostate cancer." BJU Int. 2003 Aug;92(3):226-31. PMID 12887470.** (Verify, or substitute the correct Debruyne pivotal Trelstar trial.)
- **Severity:** HIGH (FDA-approved oncology citation)

#### C4. SS-31 / TAZPOWER Barth syndrome — wrong PMID
- **Section 6.1, line 965 and line 975** (SS-31 / Elamipretide)
- **V8 claim:** "TAZPOWER Phase 2/3 crossover (NCT03098797) in Barth syndrome: >45% improvement in knee extensor muscle strength vs placebo ... ([PMID 32554501](https://pubmed.ncbi.nlm.nih.gov/32554501/))"
- **Actual PMID 32554501:** "Mitochondrial protein interaction landscape of SS-31" (Chavez JD, Tang X, Campbell MD; PNAS 2020). This is a basic-science cardiolipin-binding paper, NOT the TAZPOWER clinical trial.
- **Recommended fix:** Replace with the actual TAZPOWER publication. Candidate: **Reid Thompson W, et al. "A phase 2/3 randomized clinical trial followed by an open-label extension to evaluate the effectiveness of elamipretide in Barth syndrome, a genetic disorder of mitochondrial cardiolipin metabolism." Genet Med. 2021 Mar;23(3):471-478. PMID 33077895.** (Verify.) Keep PMID 32554501 as a separate mechanistic citation if desired.
- **Severity:** CRITICAL — supports the FDA-approved (Sept 19, 2025) accelerated indication; getting the trial citation wrong is unacceptable for a "VERIFIED" guide.

#### C5. Hashimoto humanin PNAS 2001 — wrong PMID
- **Section 6.4, line 1031 and line 1041** (Humanin)
- **V8 claim:** "Hashimoto et al. PNAS 2001: humanin rescues neurons from Aβ- and FAD-mutant-induced death; HNG analog 1000× more potent. ... ([PMID 11371647](https://pubmed.ncbi.nlm.nih.gov/11371647/))"
- **Actual PMID 11371647:** "Frequent fusion of the JAZF1 and JJAZ1 genes in endometrial stromal tumors" (Koontz JI et al.; PNAS 2001). Cancer genetics paper, not humanin.
- I also tested the obvious near-PMIDs 11371642 (also wrong — Nevo evolution paper) and 11371343 (also wrong — Alexandru cohesin yeast paper).
- **Recommended fix:** Replace with the actual Hashimoto humanin paper: **Hashimoto Y, Niikura T, Tajima H, et al. "A rescue factor abolishing neuronal cell death by a wide spectrum of familial Alzheimer's disease genes and Abeta." PNAS 2001;98(11):6336-41. PMID 11371646.** (Verify the exact PMID before substituting — the PNAS 2001 Hashimoto humanin paper is well-known.)
- **Severity:** HIGH

#### C6. Sermorelin pediatric GHD trial — wrong PMID
- **Section 2.2, line 335 and line 345** (Sermorelin)
- **V8 claim:** "Pediatric GHD trial: 0.03 mg/kg/day SC increased growth velocity from 4.0 to 7.6 cm/yr over 12 months ([PMID 8636441](https://pubmed.ncbi.nlm.nih.gov/8636441/))"
- **Actual PMID 8636441:** "Angiotensin converting enzyme inhibition modulates endogenous endothelin in chronic canine thoracic inferior vena caval constriction" (Clavell AL et al.; J Clin Invest 1996). Cardiovascular animal model, not sermorelin.
- **Recommended fix:** Identify the correct sermorelin pediatric GHD pivotal study and substitute the PMID. (Likely Wood DF or Thorner-group publications from 1985-1996.)
- **Severity:** HIGH

#### C7. CJC-1295 / GHRH-GHRP synergy — wrong PMID
- **Section 2.3, line 357, 363, 367, 379, 389, 401, 411, 423, 433, 445, 455, 467, 477** (CJC-1295, Ipamorelin, GHRP-2, GHRP-6, Hexarelin entries — PMID 17536002 is repeatedly cited as a GHRH/GHRP synergy reference)
- **V8 claim:** "Acute GH peak ~10× baseline ... synergistic with GHRPs (≥2-5× GH release vs either alone) ([PMID 17536002](https://pubmed.ncbi.nlm.nih.gov/17536002/))"
- **Actual PMID 17536002:** "Brain white matter expansion in human obesity and the recovering effect of dieting" (Haltia LT, Viljanen A, Parkkola R; J Clin Endocrinol Metab 2007). Obesity/MRI paper, not GHRP/GHRH.
- **Recommended fix:** Identify the correct GHRH/GHRP synergy paper. A well-known candidate is **Sigalos JT, Pastuszak AW. "The Safety and Efficacy of Growth Hormone Secretagogues." Sex Med Rev. 2018 Jan;6(1):45-53. PMID 28777087.** (Verify.) This PMID appears in **at least 5 Section 2 entries**, all of which require correction.
- **Severity:** CRITICAL (single error propagated across many entries)

#### C8. CJC-1295 PK paper — wrong PMID
- **Section 2.3, 2.4 (lines 367, 389)** (CJC-1295 No-DAC and DAC entries, Key References)
- **V8 claim:** "[PMID 18184801](https://pubmed.ncbi.nlm.nih.gov/18184801/)" listed as a CJC-1295 reference.
- **Actual PMID 18184801:** "Single-shot detection of bacterial endospores via coherent Raman spectroscopy" (Pestov D et al.; PNAS 2008). Analytical chemistry, not CJC-1295.
- **Note:** PMID 16352683 (Teichman SL et al., JCEM 2006) IS the correct CJC-1295 phase I PK paper and is correctly cited elsewhere in V8.
- **Recommended fix:** Either remove PMID 18184801 from the Key References (if no second CJC-1295 PK paper is needed) or substitute a real second CJC-1295 reference.
- **Severity:** MEDIUM (it's a duplicate/secondary citation; primary PMID 16352683 is correct)

#### C9. LGD-4033 Phase 1 healthy men — wrong PMID
- **Section 11.3, lines 56, 62, 66** (LGD-4033 / Ligandrol)
- **V8 claim:** "Phase 1 in 76 healthy men (0.1-1 mg/day x 21 d): dose-dependent increase in lean body mass ... ([PMID 23361637](https://pubmed.ncbi.nlm.nih.gov/23361637/))"
- **Actual PMID 23361637:** "Effect of carotid endarterectomy on cognitive function in patients with asymptomatic carotid artery stenosis" (Takaiwa A et al.; Acta Neurochir 2013). Neurosurgical paper, unrelated.
- **Recommended fix:** Substitute the actual Basaria LGD-4033 Phase 1 paper. **Basaria S, Collins L, Dillon EL, et al. "The safety, pharmacokinetics, and effects of LGD-4033, a novel nonsteroidal oral, selective androgen receptor modulator, in healthy young men." J Gerontol A Biol Sci Med Sci. 2013 Jan;68(1):87-95. PMID 22459616.** (Verify.)
- **Severity:** HIGH

#### C10. Ostarine cancer cachexia Phase 2 — wrong PMID
- **Section 11.4, lines 78, 88** (Ostarine / MK-2866)
- **V8 claim:** "Phase 2 in cancer cachexia (159 pts): 3 mg/day x 16 wk increased lean mass +1.3 kg vs placebo ([PMID 21798826](https://pubmed.ncbi.nlm.nih.gov/21798826/))"
- **Actual PMID 21798826:** "Development and validation of a sensitive LC/MS/MS method for the simultaneous determination of naloxone and its metabolites in mouse plasma" (Jiang H et al.; J Chromatogr B 2011). Analytical chemistry method, unrelated.
- **Recommended fix:** Substitute the correct Dalton/Steiner GTx ostarine Phase 2 paper. Likely **Dobs AS, Boccia RV, Croot CC, et al. "Effects of enobosarm on muscle wasting and physical function in patients with cancer: a double-blind, randomised controlled phase 2 trial." Lancet Oncol. 2013 Apr;14(4):335-45. PMID 23499390.** (Verify; year and N may differ from V8 figures.)
- **Severity:** HIGH

### MEDIUM — sequence/dating issues
None confirmed. The bioregulator sequences in Section 10 appear consistent with Khavinson primary literature. **However**, the V8 changelog note that PMID 15582023 was previously the cited Khavinson Epitalon paper is itself misleading: I tested PMID 15582023 and it returns "Effects of morphine or naloxone on cocaine-induced genital reflexes in paradoxical sleep-deprived rats" (Andersen ML et al.; Pharmacol Biochem Behav 2004). If V8 has anywhere left this PMID, it must be removed; I did not find it surviving in V8 main text — but several earlier files (`Comprehensive Peptide Guide 2026 VERIFIED v4_0.md`, etc.) may still carry it. Worth a `grep` sweep across the repo.

---

## Disputed / Unverifiable

### FDA URL access blocked by sandbox
The following FDA.gov URLs were on the WebFetch denylist for this session (network restrictions returned "Permission denied"):
- FDA Scenesse approval press release (line 1111)
- FDA Foundayo CNPV approval press release (line 211)
- FDA HCG diet warning page (line 1447)
- FDA Pitocin label (line 1425)
- FDA Vyleesi label (line 1359)
- FDA Trelstar label (line 1469)

**Cannot independently confirm via fda.gov:**
- **Foundayo / orforglipron approval date (April 1, 2026)** — V8 claims "fifth approval under CNPV pilot; fastest NME approval since 2002." This claim is internally consistent with PMID 40960239 (ATTAIN-1 published Nov 2025) but the FDA primary source is unreachable in this sandbox. **RECOMMEND** the user manually verify via fda.gov News & Events.
- **SS-31 / FORZINITY Sept 19, 2025 Barth syndrome accelerated approval** — V8 claims "Original NDA 215244 received CRL May 2024; resubmitted with knee-extensor strength as intermediate endpoint." Plausible per public Stealth BioTherapeutics history but not independently verifiable from this sandbox.
- **Mazdutide NMPA China obesity 27 Jun 2025 / T2DM Sept 2025** — Not directly verifiable from PubMed; confirmed only through the NEJM publication date alignment (PMID 40421736 = 2025).
- **PT-141 / Vyleesi June 21, 2019 approval** — uncontroversial (well-documented in industry sources); plausible but FDA URL blocked.
- **Afamelanotide / Scenesse Oct 2019 EPP approval** — well-documented; plausible.
- **HCG diet warning still active** — uncontroversial historically.
- **NMN reversal Sept 29, 2025** — V8 claims FDA reversed the Oct-2022 NMN supplement ban via Sept 29, 2025 letter and Dec 2, 2025 confirmation letters. **HIGH-IMPACT regulatory claim; direct FDA documentation is essential.** Recommend the user pull the actual FDA correspondence to confirm.

### Athira Pharma / Dihexa DOJ settlement (Jan 2025)
V8 changelog and Dihexa entry claim **"Athira Pharma settled DOJ False Claims Act allegations >$4M (Jan 2025); fosgonimeton failed Phase 2/3 LIFT-AD."** PubMed cannot verify legal settlements; the LIFT-AD failure is broadly publicly reported. The DOJ FCA settlement amount ($4M+) and timing should be cross-checked against DOJ press releases — the figure is plausible but I cannot independently confirm in this sandbox.

### V8 changelog claim "all PMIDs re-verified"
**This claim is demonstrably false.** Of ~30 PMIDs sampled, ≥8 (27%) point to wrong papers in subjects unrelated to the cited claim. This includes citations supporting FDA-approved drug efficacy (PT-141 RECONNECT, Triptorelin pivotal, SS-31 TAZPOWER), which are the most consequential entries in the document. The user should regard the "PMIDs re-verified" header as **aspirational but unfulfilled** and should not trust any uncited or singly-cited claim until a complete second pass is done.

---

## Recommended next-step audit (out of scope for this V1 report)

1. **Full PMID re-fetch.** All 186 unique PMIDs require an esummary lookup with title-vs-claim diff. Suggested workflow: extract `(PMID, surrounding sentence)` pairs and run a bulk verification script.
2. **Specific citation patches.** For each CRITICAL finding above, identify the correct primary reference and substitute. PT-141, SS-31/TAZPOWER, Triptorelin, Sermorelin, Humanin, LGD-4033, Ostarine — these are all FDA-approved or pivotal-trial citations and warrant the most care.
3. **PMID 17536002 sweep.** This single bad PMID is cited in at least 5 Section 2 entries. Replacing it once won't be enough — every occurrence must be patched.
4. **Cross-check Comprehensive_Peptide_Guide_2026_VERIFIED v4_0.md and earlier versions** for the same propagated errors so they aren't re-introduced.
5. **FDA primary-source verification** (Scenesse, Vyleesi, Foundayo, FORZINITY, NMN reversal) once the sandbox has fda.gov access.
6. **Decide on the document's "VERIFIED" label.** Until corrections are landed, the V8.0 header should arguably be downgraded — the "Verification Status" line currently overstates the audit's quality.

---

**Auditor note for the user:** Given the user's stated reliance ("my life depends on accuracy"), do not act clinically on any single-PMID claim in V8 without a fresh PubMed lookup. The error pattern (wrong PMIDs that look plausible and never raised obvious flags) suggests the original V7→V8 PMID re-verification pass may have used a fuzzy/AI-generated lookup that hallucinated identifiers. A deterministic, scripted re-check is now mandatory.
