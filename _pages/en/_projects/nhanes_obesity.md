---
layout: page
title: "Clinical Obesity in NHANES 2021-2023"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/nhanes_obesity/
lang: en

page_components:
  - type: "header"
    title: "When Weight Doesn’t Weigh the Same on Everyone: Applying The Lancet’s Clinical Obesity Framework"
  
    bottom_line:
      label: "The Bottom Line"
      text: "The Metabolic Score for Insulin Resistance <span class='highlight-metric'>(METS-IR) showed a robust independent effect for FibroScan-confirmed hepatic fibrosis (Adjusted RR = 2.9)</span> and the best overall model fit (QIC = 815.7) compared to other lipid and glycemic ratios in fully adjusted models."

    tech_stack:
      label: "Tech Stack"
      items:
        - " Python"
        - "PyReadStat"
        - "Pandas"
        - "NumPy"
        - "Matplotlib"
        - "Missingno"
        - "PyArrow"

  - type: "section"
    title: "The Challenge: The diagnostic gap of Body Mass Index (BMI)"
    content: "<strong>Clinicians almost universally rely on Body Mass Index (BMI ≥ 30 kg/m²) as the default diagnostic gatekeeper for obesity assessment</strong>. By relying solely on body weight and height ratios, standard screening protocols overlook significant subclinical cardiometabolic, hepatic, and renal involvement in metabolically unhealthy normal-weight individuals."

  - type: "section"
    title: "The Translation Gap: Anthropometric Ratios and Risk Indices"
    content: "Operationalizing The Lancet’s Clinical Obesity Framework requires moving beyond raw BMI by calculating specific anthropometric ratios—such as Waist-to-Height Ratio (WHtR)—to accurately define clinical obesity phenotypes.<br><br>Furthermore, raw NHANES data stores biomarkers as isolated laboratory parameters across complex survey subsamples. <strong>To systematically quantify cardiovascular, metabolic, and organ-specific risk, these individual inputs must be translated into validated clinical risk indices</strong> (e.g., METS-IR, FIB-4, FLI, and AHA PREVENT) to capture subclinical vulnerability prior to overt organ impairment."

  - type: "skills"
    skills_heading: "Cohort Filtration, Risk Engineering & GEE Modeling"
    skills_description: "Executing an end-to-end biostatistical pipeline—from structured cohort attrition (N = 1,816) to composite index calculation and survey-weighted Risk Ratio estimation."
    skills:
      - title: Sequential Cohort Attrition
        icon: "assets/images/icons/timeline.png"
        one: "I built an intentional filtration pipeline isolating working-age adults (ages 18 to 64) from the NHANES 2021–2023 cycle, <b>systematically controlling for pregnancy, unweighted records, and missing baseline parameters</b> (N = 11,933 → 1,816)."

      - title: Risk Indices Operationalization
        icon: "assets/images/icons/engineering.png"
        one: "I transformed <b>raw data into validated clinical risk indices</b>, including the Metabolic Score for Insulin Resistance (METS-IR), Fatty Liver Index (FLI), Fibrosis-4 Index (FIB-4), and AHA PREVENT cardiometabolic-renal risk scores."

      - title: Survey-Weighted Risk Ratios
        icon: "assets/images/icons/statistic.png"
        one: "I applied <b>Generalized Estimating Equations (GEE) with log link and Poisson family</b>, incorporating survey design parameters (primary sampling units SDMVPSU, strata SDMVSTRA, and fasting weights WTSAF2YR) to calculate population-adjusted Risk Ratios (RR)."

  - type: "figure"
    heading: "Cohort Selection & Systematic Attrition"
    description: "Executing a filtration pipeline to control for complex survey skips, fasting subsample weights, and phenotypic boundary criteria."
    dashboard_vertical: "/assets/images/nhanes_flowchart.svg"
    alt: "STROBE flowchart"
    caption: "<b>Figure 1. Cohort Attrition Pipeline.</b> Sequential filtration of the NHANES 2021–2023 master dataset (N = 11,933). Enforcing morning fasting protocol compliance (WTSAF2YR), working-age boundaries (18–64 years), and complete-case data hygiene isolated 1,816 fasting adults. Pruning 228 ambiguous unclassified records established a final phenotypically valid analysis cohort of N = 1,588 adults."

  - type: "flexible_content"
    heading: "Baseline Population Stratification (Table 1)"
    blocks:
      - type: "paragraph"
        text: "Evaluating survey-weighted demographic, examination, and biomarker gradients across Control, Peripheral, and Classic phenotype cohorts (N = 1,588)." 

      - type: "table"
        headers:
          - "Variable"
          - "Overall"
          - "Control"
          - "Peripheral"
          - "Classic"
        rows:
          - ["Age (years)", "40.92", "32.05", "45.55", "42.94"]
          - ["Systolic BP (mmHg)",	"117.21",	"112.75",	"118.29",	"119.31"]
          - ["Diastolic BP (mmHg)",	"74.59",	"68.59",	"74.11",	"78.64"]
          - ["Pulse rate (bpm)",	"70.88",	"69.30",	"70.41",	"72.06"]
          - ["Fasting Glucose (mg/dL)",	"105.06",	"98.72",	"103.94",	"111.31"]
          - ["Triglycerides (mg/dL)",	"108.60",	"74.17",	"117.46",	"124.36"]
          - ["HDL Cholesterol (mg/dL)",	"53.62",	"60.70",	"53.50",	"49.59"]
          - ["Liver Stiffness (kPa)",	"5.76",	"4.86",	"5.42",	"6.79"]
          - ["eGFR (mL/min/1.73m²)",	"102.51",	"108.14",	"99.57",	"101.41"]
          - ["Hepatic damage (%)",	"13.96",	"4.08",	"9.55",	"25.13"]
          - ["Metabolic damage (%)",	"6.42",	"0.09",	"7.90",	"9.82"]
          - ["Renal damage (%)",	"0.99",	"0.00",	"0.93",	"1.54"]

  - type: "figure"
    heading: "Phenotypic & Index-Adjusted Relative Risk"
    description: "Tracking hepatic fibrosis risk from unadjusted phenotype baselines (M1) through cross-spillover surrogates (M2) to fully integrated phenotype-index models (M3)."
    image: "/assets/images/nhanes_plot_indices_forest_coefficients.png"
    alt: "Forest Plot comparing Risk Ratios across indices"
    caption: "<b>Figure 2. Sequential Risk Attenuation in GEE Poisson Regression.</b> Comparing baseline structural phenotypes (M1) against integrated models (M3). Inclusion of the METS-IR diagnostic cutoff (RR = 2.87) attenuates the Classic Phenotype risk ratio from RR = 5.19 (95% CI: 2.94-9.17) down to RR = 2.44 (95% CI: 1.22-4.89), confirming metabolic dysfunction as a primary mediator of hepatic end-organ damage."

  - type: "results"
    cards:
      - title: "BMI & Unadjusted Hepatic Damage"
        description_1: "Unadjusted models show that the <span class='highlight-metric'>BMI-driven Classic Phenotype strongly tracks hepatic damage (RR = 5.19).</span>"
        description_2: "However, <span class='highlight-metric'>relying solely on BMI ignores 35.0% of adults</span> categorized as Peripheral, who still face elevated hepatic risk (RR = 1.95)."

      - title: "METS-IR as a Surrogate for Hepatic Damage Risk"
        description_1: "METS-IR functions as a <span class='highlight-metric'>robust independent driver of hepatic damage</span> across the integrated model <span class='highlight-metric'>(RR = 2.87).</span>"
        description_2: "Crucially, it detects marked damage risk surges in both the isolated classic (RR = 2.76) and isolated peripheral (RR = 3.60) cohorts."

      - title: "Phenotypes & Domain Risk Disparities"
        description_1: "Encompassing 45.8% of adults, the <span class='highlight-metric'>Classic Phenotype drives the bulk of multi-domain risk (28.3% overall).</span>"
        description_2: "As a result, it maintains higher risk of end-organ damage (RR = 2.44) than the Peripheral Phenotype (RR = 1.91), even after integrating METS-IR."

  - type: "showcase"
    heading: "From Clinical Phenotypes to Domain Risk and End-Organ Damage"
    description: "Mapping the survey-weighted cascade from baseline body composition through subclinical domain risk clusters into overt organ impairment."
    image: "/assets/images/cover_project_nhanes-obesity.png"
    alt: "Survey-weighted flow diagram mapping obesity phenotypes to domain damage risk"
    caption: "<b>Figure 3. Phenotypic Trajectories Across Domain Risk Clusters.</b> Survey-weighted flow diagram mapping obesity phenotypes to domain damage risk. Healthy controls flow exclusively to zero organ damage, whereas the Classic Phenotype acts as the primary origin for multi-domain dysfunction (≥2 organ systems), reinforcing the synergistic risk of hepatic and metabolic strain."
    metrics:
      - value: "45.8%"
        unit: "(69.48M)"
        label: "Classic Obesity Phenotype Prevalence"
        detail: "Dominant clinical phenotype driving the primary burden of downstream multi-domain subclinical risk."

      - value: "28.3%"
        unit: "(42.98M)"
        label: "Multi-Domain End-Organ Damage Risk"
        detail: "Risk across multiple domains, serving as the primary transition state toward overt end-organ damage."

      - value: "13.4%"
        unit: "(20.27M)"
        label: "Hepatic End-Organ Damage"
        detail: "Leading end-organ damage, far exceeding isolated metabolic (5.1%), renal (0.7%), or multi-organ strain (2.4%)."

  - type: "quote"
    text: "Reframing obesity from a static anthropometric number to a multi-system metabolic continuum is the essential first step toward true precision medicine—proving that body weight alone cannot dictate clinical vulnerability."

  - type: "flexible_content"
    heading: "Reflection: Redefining Obesity Beyond the Scale"
    blocks:
      - type: "paragraph"
        text: "Our findings challenge the long-standing reliance on BMI as a sole diagnostic gatekeeper: two individuals with similar anthropometric measurements can harbor radically different trajectories of subclinical organ strain."

      - type: "callout"
        lead: "Key Takeaway:"
        text: "Metabolic health cannot be inferred from body mass alone. Within normal-BMI adults classified into the Peripheral Obesity phenotype, <b>crossing the high METS-IR threshold triggers a 3.60-fold relative risk surge for FibroScan-confirmed hepatic fibrosis</b>, demonstrating that subclinical insulin resistance drives tissue damage long before overt clinical obesity manifests."

      - type: "paragraph"
        text: "Translating these biostatistical insights into real-world care requires embedding automation of risk indices—such as METS-IR, FIB-4, and FLI—directly into electronic health record (EHR) pipelines. Automating these calculations from routine laboratory panels creates a fundamental paradigm shift: moving healthcare away from reactive, late-stage disease management toward proactive, algorithmically guided subclinical intervention."

  - type: "gallery"
    heading: "Diagnostic Visuals & Phenotypic Trajectories"
    description: "Index formulas, survey-weighted ridgelines, GEE Poisson model comparisons, and multi-domain Sankey trajectory maps."
    items:
      - image: "/assets/images/obesity_indices_formulas.jpg"
        alt: "Operationalization of clinical indices"
        caption: "Mathematical formulations for composite risk indices, detailing METS-IR, CKD-EPI 2021 eGFR, and TyG Index equations."

      - image: "/assets/images/obesity_indices_ridgelines.jpg"
        alt: "Ridgeline plots of clinical indices"
        caption: "Survey-weighted ridgeline density plots illustrating population biomarker separation across Control, Peripheral, and Classic obesity phenotypes."

      - image: "/assets/images/obesity_indices_table.jpg"
        alt: "Table comparing clinical indices"
        caption: "Design-adjusted mean distribution table comparing Control, Peripheral, and Classic phenotypes across renal, hepatic, and cardiometabolic markers."

      - image: "/assets/images/obesity_indices_forest.jpg"
        alt: "Forest plot comparing clinical indices across regression models"
        caption: "GEE Poisson regression forest plot comparing unadjusted (M2) vs. fully adjusted (M3) Relative Risk (RR) models and QIC goodness-of-fit metrics."

      - image: "/assets/images/obesity_sankey_bmi.jpg"
        alt: "Sankey diagram: MBI to end-organ damage"
        caption: "Survey-weighted Sankey diagram mapping population flow from standard BMI categories through clinical phenotypes to multi-organ damage targets."

      - image: "/assets/images/obesity_sankey_mets-ir.jpg"
        alt: "Sankey diagram: METS-IR to end-organ damage"
        caption: "Survey-weighted flow diagram mapping BMI, clinical phenotypes, METS-IR risk thresholds, and hepatic damage outcomes."

  - type: "button"
    text: "Check README on GitHub"
    url: "https://github.com/enaromd/clinical-obesity"
    icon: "github"
    align: "center"

cta:
  heading: "Bridge Frontline Clinical Reality with Technical Execution"
  description: "Effective healthcare analytics starts with knowing how data is born at the bedside—including the hectic workflows and human factors that warp raw records. If your team needs someone who combines frontline clinical perspective with Python, SQL, and biostatistics, let’s connect."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Get in touch"
    url: "contact/"
---

<style>
.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}

.skill-cards-section {
  margin-top: 1rem;
}
</style>

{% for component in page.page_components %}
  {% if component.type == "section" %}
    {% include project-section.html data=component %}
  {% elsif component.type == "header" %}
    {% include project-header.html data=component %}
  {% elsif component.type == "button" %}
    {% include project-button.html data=component %}
  {% elsif component.type == "skills" %}
    {% include skill-cards.html data=component %}
  {% elsif component.type == "reflections" %}
    {% include project-reflection-cards.html data=component %}
  {% elsif component.type == "figure" %}
    {% include project-chart.html data=component %}
  {% elsif component.type == "results" %}
    {% include project-results.html data=component %}
  {% elsif component.type == "showcase" %}
    {% include project-chart-impact.html data=component %}
  {% elsif component.type == "quote" %}
    {% include project-quote.html data=component %}
  {% elsif component.type == "flexible_content" %}
    {% include project-flexible-content.html data=component %}
  {% elsif component.type == "gallery" %}
    {% include project-gallery.html data=component %}
  {% endif %}
{% endfor %}

{% include cta.html %}