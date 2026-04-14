# V8 Safety Audit (V2)

**Auditor:** Claude (Opus 4.6, 1M context)
**Audited file:** `/home/plindsay/prjs/peptide_research/Peptide_Guide_V8.md` (2,255 lines)
**Date:** 2026-04-14
**Methodology:** Direct file read for all flagged compounds + cross-check against PubMed primary literature, FDA labels, WADA 2026 Prohibited List, and current case-report literature (2024-2025) via WebSearch.

---

## High-Confidence Safety Issues Found

### 1. Section 11.1 — IGF-1 LR3: Cancer language too soft
**Issue:** Layman Risks calls cancer promotion "theoretical." This understates the evidence. UK Biobank (~400,000 participants), EPIC-Heidelberg, and multiple prospective cohorts have established a *causal-direction* (pre-diagnostic IGF-1 levels predicting subsequent diagnosis) link between elevated circulating IGF-1 and breast, prostate, colorectal, and thyroid cancers (HR ~1.25-1.31 per SD; ~4.5x highest vs lowest quartile in prostate). LR3 is engineered to escape IGFBP buffering, producing *supraphysiological* free IGF-1 exposure.

**Recommended replacement Layman Risks language:**
> Severe hypoglycemia (can cause loss of consciousness, seizures, death — has happened in bodybuilder users), organomegaly with chronic use, cardiac hypertrophy, increased risk of breast/prostate/colorectal/thyroid cancer (multiple large cohort studies link elevated IGF-1 to these malignancies; LR3 produces sustained supraphysiological exposure), acromegalic facial/jaw/foot growth, retinal edema, injection-site lipomas. Absolute contraindication if you have, or have a strong family history of, hormone-sensitive cancer.

**Also add to Side Effects:** seizures (documented in PED-user case literature), cardiac hypertrophy.

---

### 2. Section 11.2/11.3/11.4 — SARMs DILI: Frequency understated
**Issue:** All three SARM entries describe DILI as "reported" or "case reports." LiverTox (NCBI Bookshelf, updated 2025) catalogs **15 published DILI cases** as of 2025 (8 LGD-4033, 6 RAD-140, 3 ostarine, plus newer 2024-2025 reports — Labban *Cureus* 2024, Habeb *Cureus* 2025, Perananthan *Aust Prescr* 2024). Pattern is consistently **cholestatic with jaundice, bilirubin >15 mg/dL, weeks-to-months duration**, with one case requiring hospital admission at bilirubin 708 µmol/L (≈41 mg/dL). JAMA 2024 (Hahamyan & Basaria) called SARMs "heralds of the next drug epidemic." V8 cites only PMID 32979861, 30057765, 32047400 — all 2018-2020 — and doesn't reflect the 2024-2025 case explosion.

**Recommended Layman Risks addition (all three):**
> Cholestatic drug-induced liver injury (DILI) with severe jaundice — published cases now exceed 15 across the SARM class, with multiple 2024-2025 reports requiring hospitalization; bilirubin can rise to 20-40+ mg/dL and remain elevated for months after stopping. Also: HPG suppression that may not fully recover, cardiovascular events (myocarditis, rhabdomyolysis case reports), and contamination of supplement-marketed SARMs with anabolic steroids and unrelated drugs.

**Add references:** PMC11485217 (Labban 2024), PMC12230875 (Habeb 2025), Perananthan & George *Aust Prescr* 2024, JAMA 2024;331:1359-1360 (Hahamyan/Basaria), LiverTox NBK619971 (2025 update).

---

### 3. Section 11.4 — Ostarine Safety Rating too generous
**Current:** ★★★ ("mildest of the SARMs but still HPG-suppressive")
**Recommend:** ★★☆☆☆ (2/5)
**Rationale:** Even though Phase 2 cachexia data exists, the *underground* doses (10-25 mg/day, 3-8x trial dose) are what users actually take, and ostarine is the **#1 cause of doping violations 2015-2022** AND is implicated in DILI cases (PMID 32047400 plus newer reports). The "mildest" framing leads users to underestimate. Recommend aligning at 2/5 with the other SARMs and explicitly noting "trial dose 1-3 mg vs underground 10-25 mg" risk gradient.

---

### 4. Section 7.2 — Melanotan 2: PRES citation missing
**Issue:** Layman Risks mentions "PRES (case reports)" in Side Effects but doesn't cite the primary case report in Key References. The landmark Kaski et al. *Ann Intern Med* 2013;158:707-708 (PMID 23648955, also indexed under 23648958) is the first published PRES case after MT-2 use (20-year-old woman, generalized tonic-clonic seizure, postcentral gyrus hyperintensity).

**Recommended fix:** Add Kaski citation to Key References and strengthen Layman Risks to:
> Eruptive atypical moles and *multiple published melanoma cases* (≥6 in dermatology literature: Hjuler 2014, Ong 2012, Paurobally 2011, Cardones 2009 etc.); priapism requiring ER intervention; **posterior reversible encephalopathy syndrome with seizures** (Kaski 2013); rhabdomyolysis; renal infarct; severe nausea/flushing; uncontrolled gray-market product purity. Avoid in anyone with history of atypical nevi, melanoma, or untreated hypertension.

The current ★☆☆☆☆ rating is appropriate.

---

### 5. Section 2.9 — MK-677: CHF risk needs to specify population
**Issue:** Current language "worsens heart failure (trial increased CHF events)" is correct but vague. The Adunsky 2011 hip-fracture trial showed **4/62 (6.5%) CHF in MK-677 vs 1/61 (1.7%) placebo over 24 weeks**, and notably the **trial was terminated early** for safety. FDA explicitly lists ibutamoren as posing "significant safety risks due to the potential for congestive heart failure in certain patients" (Pharmacy Compounding Advisory Committee 2023 briefing).

**Recommended Layman Risks addition:**
> ⚠️ A randomized trial in elderly hip-fracture patients was *stopped early for safety* after CHF rates were 6.5% on MK-677 vs 1.7% placebo (Adunsky 2011, PMID 21067829); FDA cites "significant safety risk" for CHF; raises fasting glucose and HbA1c in ALL studied populations (not just diabetics); causes water retention, gynecomastia, lethargy/sedation, intracranial hypertension signal, increased appetite. Avoid in anyone with cardiovascular disease, prediabetes/diabetes, or sleep apnea.

**Safety Rating ★★☆☆☆ is appropriate** — keep as-is.

---

### 6. Section 5.6 — Cerebrolysin: Cochrane finding understated
**Issue:** Current Layman Risks says "Cochrane flags possible increase in non-fatal SAEs." The actual Cochrane 2023 finding is stronger: **RR 2.39 (95% CI 1.10-5.23) for non-fatal SAEs at full dose; RR 2.87 (1.24-6.69) at 30 mL × 10 days dose** (moderate-certainty evidence). The authors explicitly state "no further trials should be conducted" because it would be **unethical to enroll patients in a trial offering no benefit but possible harm**. Cochrane also flagged related-compound Cortexin caused deaths in mild-stroke arm vs zero placebo deaths.

**Recommended Layman Risks language:**
> Cochrane 2023 (Ziganshina) found *more than double the rate of non-fatal serious adverse events* in patients receiving Cerebrolysin (RR 2.39, CI 1.10-5.23; RR 2.87 at 300 mL cumulative dose) with no mortality benefit; review concluded further trials would be unethical. Porcine-derived (anaphylaxis/CJD-class theoretical risk); related compound Cortexin caused deaths in stroke trials. Most positive efficacy trials are manufacturer-funded and from regions with weaker trial-quality oversight.

**Safety Rating 3/5 is borderline-generous** — consider ★★☆☆☆ given Cochrane's stance. At minimum keep 3/5 but make the harm signal explicit in the rating note.

---

### 7. Section 1.11 — Tesofensine: Psychiatric signal too soft + COFEPRIS status outdated framing
**Issue:** "Possible mood/psychiatric effects" understates the trial data: 6% depressed mood in 0.5/1.0 mg arms, **2% major depression at 1 mg**, plus increased anger/hostility/confusion. The Lancet 2008 commentary warned that the trial *excluded* psychiatric patients, so real-world use will likely show higher rates. 17% Phase 2 discontinuation due to AEs (mainly cardiovascular and psychiatric).

The "stimulant-like" framing is correct but should be more explicit about controlled-substance similarity — phenyltropane class shares the cocaine/methamphetamine pharmacophore, which is why FDA scheduling concerns blocked development.

**Recommended Layman Risks addition:**
> Documented psychiatric adverse events at therapeutic doses: ~6% depressed mood, 2% major depression at 1 mg, increased anger/hostility/confusion, agitation, anxiety, panic attacks, insomnia (Astrup 2008 Lancet trial *excluded* patients with psychiatric history, so real-world rates likely higher). 17% Phase 2 discontinuation rate. Phenyltropane class shares cocaine/methamphetamine pharmacophore — abuse-liability and CV risk concerns have blocked US approval. Raises HR by ~7 bpm and BP at higher doses. **Not approved anywhere as of April 2026** — Mexico COFEPRIS resubmission still pending (analyst expectation 2025 not realized at time of audit).

---

### 8. Section 12.3 — Adipotide DEPRECATED banner: HUMAN trial outcome should be cited
**Issue:** The banner cites primate data (PMID 22089374) but doesn't reflect that the **Phase 1 in humans (NCT01655823) was discontinued specifically due to nephrotoxicity in humans**, with researchers reporting the therapeutic window was "too narrow for acceptable clinical use." Currently V8 says "results not published in high-impact journals; development halted" — softer than reality. Development was *permanently discontinued in 2019* per follow-on Kolonin lab disclosures.

**Recommended banner addition:**
> The Phase 1 trial (NCT01655823) in castrate-resistant prostate cancer patients was **terminated early due to dose-limiting nephrotoxicity in humans** (the therapeutic window between fat-loss efficacy and renal tubular injury was unacceptably narrow). Development was **permanently discontinued in 2019**. No peer-reviewed human trial data has ever been published.

Banner is otherwise visible and well-positioned. Safety Rating 1/5 is correct.

---

### 9. Section 12.5 — GW-0742 DEPRECATED banner: missing primary carcinogenicity citations
**Issue:** Banner cites a class review (PMID 19285093) but the actual pivotal evidence is the **two GSK Society of Toxicology 2009 abstracts**: Geiger LE et al. (rat 2-year bioassay, PS 895) and Newsholme SJ et al. (mouse, PS 896) showing **multi-organ tumors at 5 and 40 mg/kg/day**. The Wikipedia GW501516 entry is a more comprehensive lay reference. WADA prohibited the entire PPAR-delta class in 2009 specifically because of this finding.

**Recommended additions to banner:**
> The defining 2-year rat bioassay (Geiger LE et al., *Toxicol Sci* 2009 PS 895) showed dose-dependent tumors in liver, urinary bladder, stomach, skin, tongue, thyroid, and testes at 5-40 mg/kg/day; the parallel mouse bioassay (Newsholme et al.) confirmed multi-tissue carcinogenicity. GSK terminated GW-501516 development in 2007. WADA prohibited the entire PPAR-delta agonist class in 2009. Mechanism likely involves COX-2/VEGF upregulation, anti-apoptotic signaling, and "dark side of PPAR-delta" fueling cancer cell fatty-acid metabolism. The TGA (Australia) Schedule 10'd cardarine in 2018 — the strictest possible classification.

Banner visibility is appropriate; ★☆☆☆☆ rating correct.

---

### 10. Section 5.9 — Dihexa: Banner thorough but Layman Risks could be sharper
**Issue:** Banner is excellent. However, the Layman Risks field still says "vendors still selling as 'cognitive peptide' are trading on fraudulent science" — accurate but doesn't warn about the **HGF/c-Met oncogenic mechanism** if it ever does work. HGF is a validated oncogenic driver in many cancers (NSCLC, gastric, hepatocellular). Even if the synaptogenesis claims were never replicable, off-target chronic c-Met agonism is a real cancer concern.

Banner mentions this briefly. Recommend a single sentence emphasizing it: "If the c-Met activation claims *were* true, chronic dosing would carry meaningful tumor-promotion risk — c-Met is a validated oncogenic driver in lung, gastric, and liver cancers."

Banner is otherwise comprehensive and 0/5 stars is appropriate.

---

### 11. Section 9.1 — PT-141: BP magnitude understated for repeat-dose ambulatory
**Issue:** Current language "transient BP spikes (~6 mm Hg systolic)" is the FDA-label single-dose number. The **ambulatory BP monitoring Phase 3 study (Clayton et al., parallel-arm, 397 women)** showed peak SBP increases of 3.0-3.2 mm Hg with multiple doses, but importantly: the Vyleesi label has a hard contraindication for **uncontrolled hypertension OR known cardiovascular disease**, and warns to seek emergency care if SBP ≥180 or DBP ≥120. The original *intranasal* program was **halted by FDA clinical hold in 2007 specifically due to BP**.

**Recommended Layman Risks addition:**
> Vyleesi label *contraindicates* use in known cardiovascular disease or uncontrolled hypertension; warns to seek immediate medical care if SBP ≥180 or DBP ≥120. The original intranasal formulation was halted by FDA clinical hold (2007) specifically due to blood pressure spikes — subcutaneous version was developed to narrow exposure. Maximum 8 doses/month, never more than once per 24 h. Focal hyperpigmentation can become permanent with repeated use; melanoma history is a relative contraindication.

**Safety Rating ★★★★☆ acceptable for FDA-approved on-label use** but should arguably be ★★★☆☆ for off-label "research use" / male use without monitoring.

---

### 12. Section 9.6 — Triptorelin flare protection: Add explicit antiandrogen pre-treatment timing
**Issue:** Current language "Initial testosterone 'flare' can worsen prostate-cancer symptoms in first 1-2 weeks (co-administer antiandrogen)" is correct but doesn't specify pre-treatment timing. Standard of care is **antiandrogen started BEFORE or same-day as triptorelin and continued ≥7 days** (some guidelines say start antiandrogen 7 days before for high-volume metastatic disease to prevent spinal cord compression).

**Recommended Layman Risks addition:**
> ⚠️ The first-week testosterone flare can be **life-threatening** in men with metastatic prostate cancer (spinal cord compression, ureteral obstruction). Standard-of-care: nonsteroidal antiandrogen (bicalutamide 50 mg, flutamide 250 mg tid, or cyproterone 100 mg bid) started at minimum same-day, ideally 7 days before triptorelin in high-risk patients, continued ≥7 days post-injection. GnRH antagonists (degarelix, relugolix) avoid the flare entirely and are preferred when flare risk is high.

Safety Rating ★★★★☆ acceptable for oncology use; flag that PCT/HPG-restart "microdose" use is off-label without RCT.

---

## Safety Rating Adjustments Recommended

| Section | Compound | Current | Recommended | Reason |
|---|---|---|---|---|
| 11.4 | Ostarine | ★★★ | ★★☆☆☆ | DILI cases plus #1 doping violation; "mildest SARM" framing misleads users about underground 10-25 mg dosing |
| 5.6 | Cerebrolysin | ★★★ | ★★☆☆☆ | Cochrane 2023 found RR 2.39 for non-fatal SAEs and concluded further trials unethical |
| 6.4 | Humanin | ★★ | ★★ (keep) | Adequate — preclinical-only flag is accurate |
| 9.1 | PT-141 | ★★★★ | ★★★★ for FDA on-label / ★★★ for off-label male/research use | BP contraindication is hard, not soft |
| 11.2 | RAD-140 | ★★ | ★★ (keep) | Adequate, but Layman Risks needs DILI severity language |
| 11.3 | LGD-4033 | ★★ | ★★ (keep) | Adequate, same caveat |

All other ratings reviewed are within reasonable bounds.

---

## Dosing Range Issues

1. **Section 11.4 Ostarine "Typical Dosing"**: V8 lists "Trial: 1-3 mg/day oral. Underground: 10-25 mg/day x 8-12 wk." Good — explicitly distinguishes. **Keep this format as model for other compounds.**

2. **Section 11.1 IGF-1 LR3 "Typical Dosing"**: V8 says "20-50 mcg/day." Search results show some bodybuilder communities go to 80-120 mcg with documented hypoglycemia at those doses. Should add: "Doses >50 mcg/day substantially increase hypoglycemia risk; some user surveys report 50-75 mcg medians with 9-week median duration."

3. **Section 2.9 MK-677**: V8 lists "10-25 mg PO once daily." This matches the trial range, but should note that the **CHF safety signal emerged at 25 mg/day in elderly population** — i.e., the upper end of the listed dose range is the dose that caused trial termination. Add: "Note: 25 mg/day was the dose that produced 6.5% CHF in the Adunsky elderly trial; lower doses (10-15 mg) carry less data but smaller IGF-1 elevation."

4. **Section 9.1 PT-141**: V8 says "Research-grade: 1-2 mg SC on demand." The FDA label is **1.75 mg** with explicit "do not exceed 1 dose per 24 hours, max 8 doses/month." Research-grade 2 mg exceeds label. Acceptable to mention but should flag: "2 mg slightly exceeds FDA label maximum single dose."

5. **Section 12.3 Adipotide "Typical Dosing"**: V8 says "Historic trial: 0.43 mg/kg/day subQ × 4 weeks. Do not use." Good. **Adequate.**

6. **Section 12.5 GW-0742 "Typical Dosing"**: V8 says "Do not use. Preclinical: 1-10 mg/kg in rodents." Good.

7. **Sections 1.1 / 1.2 (Semaglutide / Tirzepatide)**: Dosing matches FDA labels. **Adequate.**

8. **Section 1.11 Tesofensine**: V8 lists "Phase 3 doses: 0.25 mg or 0.5 mg. 1.0 mg associated with more BP/HR effects." Good — 1 mg is the dose that produced the depression signal, so this is appropriately cautious.

---

## Confirmed Adequate (No changes recommended)

- **Section 1.1 Semaglutide** — Layman Risks correctly notes pancreatitis, gallbladder, and boxed-warning thyroid C-cell risk. Matches FDA Wegovy label.
- **Section 1.2 Tirzepatide** — Boxed warning mentioned; SURMOUNT-OSA approval reflected; AE rates accurate.
- **Section 1.3 Retatrutide** — Dysesthesia signal at 12 mg properly highlighted (~21% AE rate disclosed).
- **Section 3.2 TB-500** — WADA S2 status confirmed (verified against 2026 list).
- **Section 3.3 HGH Frag 176-191** — WADA S2.2 confirmed; lipolytic mechanism accurately differentiated from full GH.
- **Section 3.4 AOD-9604** — Phase IIb obesity failure properly disclosed; WADA S2.2 confirmed.
- **Section 5.9 Dihexa** — DEPRECATED banner is excellent; retraction (PMID 40312093), Athira DOJ settlement, fosgonimeton LIFT-AD failure all correctly cited. Best deprecation banner in the document.
- **Section 6.2 MOTS-c** — WADA S4.4 (2024) confirmed; "exercise in a vial" hype caveat appropriate.
- **Section 6.3 NMN/NR** — Cancer caveat appropriately framed as "theoretical concern: avoid in active malignancy"; long-term mouse data (lifespan extension without tumor increase) is favorable; FDA Sept 2025 reversal correctly cited.
- **Section 6.5 FOXO4-DRI** — ★☆☆☆☆ rating with explicit "no human data, vendor authenticity concerns" is excellent.
- **Section 6.6 Epitalon** — Telomerase-cancer concern correctly flagged; single-lab evidence base properly questioned.
- **Section 7.1 Melanotan 1 (Afamelanotide)** — FDA-approved status, EPP indication, melanoma caveat all accurate.
- **Section 9.5 HCG** — "HCG diet debunked" with FDA warning citation is appropriately direct.
- **Section 11.5 ACE-031** — Vascular AE program-halt properly disclosed.
- **Section 11.6 Follistatin-344** — Product authenticity skepticism (recombinant glycoprotein impossible from bacterial expression) is technically excellent.
- **Section 11.9 AICAR** — WADA S4.4 since 2009 confirmed; hyperuricemia/gout flare and hypoglycemia warnings appropriate.

---

## Cross-Cutting Observations

1. **WADA citations are accurate.** All compounds flagged as WADA-prohibited (TB-500, AOD-9604, HGH Frag, AICAR, MOTS-c, IGF-1 LR3, SARMs, MK-677, GW-0742) match the 2026 Prohibited List I verified.

2. **DEPRECATED banner format is consistent and visible** — the ⚠️ emoji, bold "DEPRECATED" label, and bold "Do not use" closer all align across 5.9, 12.3, and 12.5. Good.

3. **The PT-141 contraindication is the single most important "soft" warning in the document** — Vyleesi has a HARD contraindication for CV disease, not a "use with caution." Strengthen.

4. **The IGF-1 LR3 cancer language is the most important "soft" warning for chronic-use compounds** — UK Biobank epidemiology has moved this from "theoretical" to "established association" since the V7 cycle.

5. **No deprecated compound is missing a banner**; no compound has a misleading "research-grade safe" framing.

6. **Citation freshness**: SARMs section needs 2024-2025 case-report citations added (PMC11485217, PMC12230875, JAMA 2024;331:1359). Otherwise citations look current.

7. **No safety rating exceeds ★★★★ for a non-FDA-approved compound** — appropriately conservative.

---

## Summary Severity Triage

| Severity | Section | Single-line summary |
|---|---|---|
| 🔴 High | 11.1 IGF-1 LR3 | Cancer language must move from "theoretical" to "established epidemiologic association" |
| 🔴 High | 11.2/11.3/11.4 SARMs | Add 2024-2025 DILI literature; emphasize cholestatic severity (bilirubin 20-40 mg/dL) |
| 🔴 High | 9.1 PT-141 | Explicit contraindication wording matching Vyleesi label, not soft "avoid in" |
| 🟡 Med | 2.9 MK-677 | Quantify CHF rate (6.5% vs 1.7%) and trial-termination fact |
| 🟡 Med | 5.6 Cerebrolysin | Cochrane RR 2.39 should be quantitative in Layman Risks; consider rating drop to ★★ |
| 🟡 Med | 7.2 Melanotan 2 | Add Kaski 2013 PRES citation; expand melanoma case count |
| 🟡 Med | 1.11 Tesofensine | Quantify psychiatric signal (6% depressed mood, 2% major depression) |
| 🟢 Low | 9.6 Triptorelin | Add explicit antiandrogen pre-treatment timing protocol |
| 🟢 Low | 11.4 Ostarine rating | Drop ★★★ → ★★ for consistency with class hazard |
| 🟢 Low | 12.3 Adipotide banner | Add "human Phase 1 terminated for nephrotoxicity in humans" detail |
| 🟢 Low | 12.5 GW-0742 banner | Add Geiger/Newsholme primary 2-year bioassay citations |

No compound was found where the safety rating was *too harsh* relative to the literature.

---

## Sources Consulted (key)

- LiverTox: SARMs (NCBI Bookshelf NBK619971, 2025 update)
- Labban et al. *Cureus* 2024;16:e69601 (PMC11485217) — LGD-4033 DILI
- Habeb et al. *Cureus* 2025;17:e85500 (PMC12230875) — RAD-140 DILI
- Perananthan & George *Aust Prescr* 2024;47(1):26-28 — RAD-140 severe liver injury
- Hahamyan & Basaria *JAMA* 2024;331:1359-1360 — SARM commentary
- Kaski et al. *Ann Intern Med* 2013;158:707-708 (PMID 23648955) — Melanotan-2 PRES
- Adunsky et al. *Arch Gerontol Geriatr* 2011;53:183-189 (PMID 21067829) — MK-677 CHF
- Ziganshina et al. *Cochrane* 2023, CD007026.pub7 (PMID 37818733) — Cerebrolysin SAE
- Geiger et al. (rat) and Newsholme et al. (mouse), *Toxicol Sci* 2009 — GW501516 carcinogenicity
- Vyleesi FDA label (NDA 210557, accessdata.fda.gov)
- FDA Warrior Labz SARMS warning letter (June 2023, #655280)
- WADA 2026 Prohibited List (effective 1 January 2026)
- UK Biobank IGF-1 cancer analysis (Oxford CEU, ~400,000 participants)
- EPIC-Heidelberg IGF-1 cancer/mortality cohort (PMC10505533)
- Athira Pharma LIFT-AD topline (3 Sept 2024) — fosgonimeton failure
- Saniona Q4 2024 update (March 2025) — tesofensine COFEPRIS status
