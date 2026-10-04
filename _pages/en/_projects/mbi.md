---
layout: page
title: "Medication intensity and Heart Disease"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/mbi/
lang: en

page_components:
  - type: "header"
    title: "Hemodynamic Gap: Medication Intensity as a Surrogate for Cardiac Remodeling"
  
    bottom_line:
      label: "The Bottom Line"
      text: "The Medication Burden Index successfully <span class='highlight-metric'>stratified 25.7% of the high-volume clinical cohort into high-acuity risk zones</span>, identifying advanced hemodynamic complexity and critical pulmonary hypertension directly from pharmacological footprints."

    tech_stack:
      label: "Tech Stack"
      items:
        - "Object-oriented programming (OOP)"
        - "Pandas"
        - "NumPy"
        - "Statsmodels"
        - "Matplotlib" 
        - "Seaborn"

  - type: "section"
    title: "The Challenge: High volume in a compressed timeline"
    content: "During a high-stakes 10-day clinical sprint, field teams must rapidly triage an overwhelming influx of patients suffering from complex structural heart conditions. The immediate operational bottleneck lies in patient selection: clinicians must quickly <strong>identify which patients are actively transitioning into critical hemodynamic failure</strong> to fast-track them for resource-intensive Transesophageal Echocardiography (TEE) before their intervention window closes."

  - type: "section"
    title: "The Data Distortion: Missing Not At Random (MNAR) bias"
    content: "To survive the extreme pace of the medical mission, <strong>cardiologists maximize clinical throughput by documenting only critical pathology—leaving fields for healthy cardiac structures entirely blank</strong>. This clinical shorthand introduces a severe Missing Not At Random (MNAR) bias that aggressively skews the dataset, artificially inflates the cohort's apparent baseline severity, and completely breaks statistical models."

  - type: "skills"
    skills_heading: "Restoring Signal to the Cohort Baseline"
    skills_description: "To overcome clinician documentation shorthand, I engineered a clinical data pipeline that restores population variance and extracts hidden physiological indicators across three standalone engineering phases:"
    skills:
      - title: Bias Mitigation
        icon: "assets/images/icons/data_management.png"
        one: "I engineered a <b>Gaussian Imputation model</b> aligned with American Society of Echocardiography guidelines. By injecting controlled physiological noise centered on healthy reference parameters, the algorithm recovers the true population variance."

      - title: Index Engineering
        icon: "assets/images/icons/engineering.png"
        one: "I developed the <b>Medication Burden Index (MBI)</b>. This parameter normalizes complex polypharmacy arrays against therapeutic ceilings, converting fragmented medication registries into a single, standardized surrogate metric for cardiac remodeling."

      - title: Statistical Triage
        icon: "assets/images/icons/statistic.png"
        one: "I executed a <b>Receiver Operating Characteristic (ROC)</b> curve analysis to map the engineered MBI scores against objective clinical and hemodynamic indicators, establishing an empirical triage cutoff that fast-tracks high-acuity patients with high precision."

  - type: "flexible_content"
    heading: "Quantifying intensity: How the MBI works"
    blocks:
      - type: "paragraph"
        text: "Rather than a simple pill count, the Medication Burden Index evaluates the collective 'effort' a patient's cardiovascular system undergoes under active medical support. The engine calculates this by evaluating individual medication dosages relative to their globally recognized maximum therapeutic thresholds and applying class-specific clinical weights:"

      - type: "formula"
        equation: "MBI = \\sum_{i=1}^{n} \\left( \\text{Weight}_{\\text{class}_i} \\times \\frac{\\text{Total Daily Dose}_i}{\\text{Maximum Dose}_i} \\right)"

      - type: "paragraph"
        text: "To standardize this calculation, the pipeline processes two critical variables:"

      - type: "bullets"
        items:
          - "**Total Daily Dose:** The total milligrams consumed by the patient in 24 hours. For example, a patient on Furosemide 40mg every 12h has a $TDD = 80\\text{ mg}$."
          - "**Clinical Weights:** The code assigns higher weights (e.g., **3.0**) to loop diuretics and lower weights (**0.5**) to statins or maintenance drugs."

      - type: "paragraph"
        text: "By consolidating these complex polypharmacy arrays into a single, standardized continuous variable, the index unmasks advanced disease severity well before a patient ever reaches an echocardiograph station."

      - type: "paragraph"
        text: "The code assigns specific weights based on the severity of the condition being treated, prioritizing signals of cardiac remodeling:"

      - type: "table"
        headers:
          - "Weight"
          - "Priority"
          - "Medication Classes"
        rows:
          - ["3.0", "**Critical**", "Loop diuretics, Pulmonary vasodilators."]
          - ["2.0", "**High**", "RAAS inhibitors, Beta-blockers, SGLT2."]
          - ["1.0", "**Moderate**", "Anticoagulants, Calcium channel blockers."]
          - ["0.5", "**Maintenance**", "Statins, Metabolic drugs."]

  - type: "showcase"
    heading: "MBI-Driven Hemodynamic Triage"
    description: "The ultimate output of the data analysis is a non-linear classification framework that successfully stratified 25.7% of the patient cohort into high-acuity clinical risk zones. This allows the medical mission to isolate the high-benefit intervention candidates and maximize diagnostic utility under strict field resource constraints."
    image: "/assets/images/cover_project_mbi.png"
    alt: "MBI Distribution and Triage Zones"
    caption: "<b>Figure 1: Correlation between MBI and hemodynamic severity.</b> The three validated operative triage zones are shown."
    metrics:
      - value: "67%"
        label: "Cohort Rescue"
        detail: "Prevented patient cohort exclusion by diagnosing MNAR shorthand patterns and preserving baseline data."

      - value: "34.7%"
        label: "Pathology Inflation Corrected"
        detail: "Eliminated artificial elevation by lowering skewed average RVSP from 51.0 mmHg to 33.3 mmHg, reflecting a more accurate baseline."

      - value: "28.9%"
        label: "Clinical Discordance Unmasked"
        detail: "Identified hidden risk profiles in patients maintaining moderate pressures strictly through agressive medication."

  - type: "figure"
    heading: "Dashboard structure and visualizations"
    description: "Every visual component functions as an active interactive filter, allowing users to cross-examine sub-cohorts dynamically by simply clicking on specific data segments."
    dashboard_vertical: "/assets/images/mbi_dashboard.png"
    link: "https://public.tableau.com/app/profile/enyel.a.rodr.guez.g./viz/MBIstratification/MBIstratification"
    alt: "MBI Dashboard"

  - type: "results"
    cards:
      - title: "Cohort distribution"
        lead_1: "Age Distribution Registry: "
        description_1: "A continuous histogram detailing the age composition of the mission's cohort."
        lead_2: "Gender Split (Donut Chart): "
        description_2: "Enables rapid auditing of gender-based clinical variations across disease groups."

      - title: "Pathological Crossroads"
        lead_1: "Disease Prevalence Matrix: "
        description_1: "Maps diagnoses driving patient presentation, color-coded by MBI Triage Zones."
        lead_2: "Index Composition: "
        description_2: "Deconstructs Medication Burden across distinct pharmacological classes."

      - title: "Average KPI Cards"
        lead_1: "Operational Footprint: "
        description_1: "Provides an operational read on the polypharmacy footprint across selected fields."
        lead_2: "Hemodynamic Baseline (RVSP): "
        description_2: "Tracks RVSP in relation to the proposed triage thresholds."

  - type: "quote"
    text: "The MBI transforms a medication list into a severity metric, allowing the mission to operate more efficiently."

  - type: "flexible_content"
    heading: "Reflections: Context Dictates Structure"
    blocks:
      - type: "paragraph"
        text: "Building the Cardio-MBI-Triage-Engine solidified a fundamental truth of specialized health informatics: <strong>pure data analysis patterns fail if they are implemented without deep clinical domain literacy.</strong>"

      - type: "callout"
        lead: "Key Takeaway:"
        text: "An outside data team looking at this missing dataset blindly would have either dropped the incomplete rows entirely (destroying the cohort size) or applied standard, unweighted mean imputations that completely mask the real structural crisis of the field operation."

      - type: "paragraph"
        text: "By pairing an intimate understanding of cardiologist behavioral patterns in high-stress clinical environments with robust data structure, this pipeline successfully translated fragmented medication registries into high-fidelity diagnostic targets—maximizing the impact of the mission's absolute scarcest asset: the specialist's time."

  - type: "gallery"
    heading: "Data Analysis and Visualization"
    description: "From raw data processing to statistical validation: the end-to-end workflow for the 2025 ‘Project Health for Leon’ cardiology mission."
    items:
      - image: "/assets/images/mbi_code.png"
        alt: "Dictionary of medication doses"
        caption: "Implementation of the ClinicalConfig class to standardize medication weights and dosages into a reproducible Python pipeline."

      - image: "/assets/images/mbi_imputation.jpg"
        alt: "Sensitivity analysis"
        caption: "Utilizing Stochastic Gaussian Imputation to correct 'Informative Missingness' (MNAR) and restore the natural physiological distribution of RVSP"

      - image: "/assets/images/mbi_3nf.jpg"
        alt: "Database 3NF"
        caption: "The database layer implements a 5-table Snowflake Schema, enforcing Third Normal Form (3NF) compliance across core tables"

      - image: "/assets/images/mbi_roc_rvsp.jpg"
        alt: "ROC Curve for RVSP"
        caption: "ROC Curve analysis establishing the 5.25 MBI threshold as a high-precision marker for critical pulmonary hypertension."

      - image: "/assets/images/mbi_discordance.jpg"
        alt: "Residual analysis for MBI and RVSP"
        caption: "Identifying 'deceptively stable' patients who maintain moderate pressures only through aggressive pharmacological compensation."

      - image: "/assets/images/mbi_table.jpg"
        alt: "Table 1: Baseline characteristics"
        caption: "Defining the clinical 'Sweet Spot' to prioritize surgical interventions based on the intersection of MBI zones and hemodynamic severity."

  - type: "button"
    text: "Check README on GitHub"
    url: "https://github.com/enaromd/Cardio-MBI-Triage-Engine"
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