# REACT: risk of REcurrent Atherosclerotic Cardiovascular evenTs

REACT estimates the five-year risk of a major adverse coronary or cerebrovascular event (MACE) for patients at their first presentation with atherosclerotic cardiovascular disease (ASCVD).

**Calculator:** https://react-ascvd.web.app


---

## Intended use

REACT is intended for clinicians assessing patients aged 18 to 85 years at their first presentation with ASCVD. It is designed to support decisions on secondary prevention. It is not a substitute for clinical judgement, and it has not been evaluated or registered as a medical device.

## The study

> **Predicting risk of REcurrent Atherosclerotic Cardiovascular evenTs using routinely collected health characteristics in patients with established disease: derivation and external validation of the REACT score**
>
> Daniel King<sup>1,\*</sup>, Daniel E. Harris<sup>1,2,3,\*</sup>, Ashley Akbari<sup>1</sup>, Mathew Lawrence<sup>2</sup>, Clive Weston<sup>4</sup>, Chris Hopkins<sup>2</sup>, Leighton Phillips<sup>2</sup>, Christopher Ll Morgan<sup>5</sup>, Craig J. Currie<sup>5</sup>, Julian Halcox<sup>1,6,†</sup>, Mike B. Gravenor<sup>1,†</sup>
>
> <sup>1</sup> Swansea University Medical School, Swansea University &nbsp;·&nbsp; <sup>2</sup> Tritech Institute, Hywel Dda University Health Board &nbsp;·&nbsp; <sup>3</sup> Pharmacy Department, Hywel Dda University Health Board &nbsp;·&nbsp; <sup>4</sup> Cardiology Department, Hywel Dda University Health Board &nbsp;·&nbsp; <sup>5</sup> Human Data Sciences, Cardiff &nbsp;·&nbsp; <sup>6</sup> Department of Cardiology, Swansea Bay University Health Board
>
> <sup>\*</sup> Joint first authors &nbsp;&nbsp; <sup>†</sup> Joint senior authors
>
> *Manuscript in preparation. The full reference will be added here on publication.*

REACT was developed using linked, routinely collected, individual-level primary and secondary care records for patients presenting with ASCVD in Wales, held in the Secure Anonymised Information Linkage (SAIL) Databank. The model was externally validated in English primary care records from the Clinical Practice Research Datalink (CPRD) Aurum, linked to hospital and mortality data.

## Inputs

| Input | Definition |
|---|---|
| Age | Years at first presentation (18 to 85), grouped as under 50, 50–59, 60–69, 70–79 and 80–85 |
| Sex | Male or female |
| Deprivation | Area deprivation quintile, from a postcode or entered directly: Welsh Index of Multiple Deprivation in Wales, English Index of Multiple Deprivation in England. Quintile 1 is the most deprived. Postcodes are accepted for Wales and England only |
| Diagnosis type | Stable diagnosis or MACE diagnosis, as above |
| Vascular territory | Coronary, cerebrovascular or peripheral arterial disease, at first presentation |
| Smoking status | Non-smoker, ex-smoker or current smoker |
| Comorbidities | Diabetes, dementia, liver disease, hypertension and heart failure, recorded before first presentation |
| Non-HDL cholesterol | Most recent measurement (mmol/L), grouped as ≤4.3 or >4.3 |
| eGFR | Most recent measurement (mL/min/1.73m²), grouped as >60, 30–60 or <30 |

## Outputs

- **Five-year risk of a major adverse event.** For a stable diagnosis, this is the probability of a first MACE within five years. For a MACE diagnosis, it is the probability of a further MACE. Events followed by death within the five years are counted.
- **Distribution at five years.** Among 100 patients with the same characteristics, the expected numbers who remain event-free, experience one MACE, experience two or more MACE, or die.


## Lipid-lowering adjustment

The calculator offers an optional, illustrative adjustment showing the expected effect of lowering low-density lipoprotein cholesterol (LDL-C). It is applied to the REACT estimates and does not change the REACT model itself.

**1. LDL-C reduction.** The user enters the current LDL-C and chooses either:
- initiation of a PCSK9 inhibitor, taken as a **60% reduction** in LDL-C, as observed in the FOURIER trial;<sup>1</sup> or
- a percentage reduction of their own choosing.

The absolute reduction is the current LDL-C multiplied by the percentage reduction. The calculator also shows the resulting LDL-C.

**2. Rate ratios.** The rate ratios per 1 mmol/L lower LDL-C come from the Cholesterol Treatment Trialists' (CTT) Collaboration meta-analysis of individual data from 174,000 participants in 27 statin trials, by sex:<sup>2</sup>

| | Men | Women |
|---|---|---|
| Major vascular events | 0.78 | 0.84 |
| All-cause death | 0.90 | 0.91 |

The rate ratio is compounded over the absolute reduction, so a reduction of *d* mmol/L multiplies the risk by RR<sup>*d*</sup>.

**3. Applying the ratios.** The rate ratio for major vascular events is applied to the five-year risk of a major adverse event and to the expected numbers with one or with two or more MACE. The rate ratio for death is applied to the expected number of deaths. Patients no longer expected to have an event or to die are added to the number who remain event-free.

**Worked example.** A man with a five-year risk of 20% and a current LDL-C of 4.0 mmol/L starts a PCSK9 inhibitor:
- LDL-C falls by 60%, from 4.0 to 1.6 mmol/L, an absolute reduction of 2.4 mmol/L.
- His risk of a major adverse event is multiplied by 0.78<sup>2.4</sup> = 0.55, giving **11%**.
- His expected deaths are multiplied by 0.90<sup>2.4</sup> = 0.78.
- For a woman with the same profile, the factors are 0.84<sup>2.4</sup> = 0.66 (risk 13%) and 0.91<sup>2.4</sup> = 0.80.

**Limitations of the adjustment**
- It assumes the proportional benefit per mmol/L observed in statin trials applies to the entered reduction, whichever drug achieves it, and from the start of treatment. In the trials, benefit was smaller in the first year.
- The development cohort included patients already taking lipid-lowering therapy. The adjusted figures therefore indicate the likely direction and approximate size of the benefit; they are not a validated prediction.

## Privacy

The calculator does not store any inputs. Risks are computed on request and only rounded percentages are returned. If a postcode is entered, it is sent to [postcodes.io](https://postcodes.io) to identify the area, and the deprivation quintile is then looked up within the page.

## References

1. Sabatine MS, Giugliano RP, Keech AC, Honarpour N, Wiviott SD, Murphy SA, et al. Evolocumab and clinical outcomes in patients with cardiovascular disease. N Engl J Med 2017;376:1713-1722. doi: https://doi.org/10.1056/NEJMoa1615664
2. Cholesterol Treatment Trialists' (CTT) Collaboration. Efficacy and safety of LDL-lowering therapy among men and women: meta-analysis of individual data from 174 000 participants in 27 randomised trials. Lancet 2015;385:1397-1405. doi: https://doi.org/10.1016/S0140-6736(14)61368-4

## Funding and contact

This study was funded by an unrestricted research grant from Amgen.

For questions about REACT, contact Daniel King, Swansea University Medical School (d.t.king@swansea.ac.uk).

© 2025–2026 Daniel King. All rights reserved.
