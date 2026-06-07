---
layout: splash
title: "Medication Burden Index (MBI)"
permalink: portfolio/projects/mbi/
lang: en
# Social previews
description: "Developing a Python-based clinical engine to quantify pharmacological intensity. Featuring ROC-validated triage thresholds for critical pulmonary hypertension."
header:
  teaser: "/assets/images/mbi_triage.png"
# This block communicates directly with the SEO plugin
seo:
  type: "article"
  title: "Medication Burden Index (MBI)" # Repeat title here
  image: "/assets/images/mbi_triage.png"
# Sections
solution:
  - title: "Restoring Signal to the Cohort Baseline"
  - excerpt: "To overcome clinician documentation shorthand, I engineered a clinical data pipeline that restores population variance and extracts hidden physiological indicators across three standalone engineering phases:"
results:
  - title: "MBI-Driven Hemodynamic Triage"
  - excerpt: "The ultimate output of the data analysis is a non-linear classification framework that successfully stratified <span class='highlight-metric'>25.7% of the patient cohort into high-acuity clinical risk zones</span>. This allows the medical mission to isolate the high-benefit intervention candidates and maximize diagnostic utility under strict field resource constraints."
dashboard:
  - title: Dashboard structure and visualizations
  - excerpt: "Every visual component functions as an active interactive filter, allowing users to cross-examine sub-cohorts dynamically by simply clicking on specific data segments."
highlights_title: 
  - title: "Data Analysis and Visualization"
  - excerpt: "From raw data processing to statistical validation: the end-to-end workflow for the 2025 'Project Health for Leon' cardiology mission."
highlights:
  - url: "/assets/images/mbi_code.png"
    image_path: "/assets/images/mbi_code.png"
    alt: "Architecting the MBI engine"
    title: "Implementation of the ClinicalConfig class to standardize medication weights and dosages into a reproducible Python pipeline."
  - url: "/assets/images/mbi_imputation.jpg"
    image_path: "/assets/images/mbi_imputation.jpg"
    alt: "Restoring Data Integrity"
    title: "Utilizing Stochastic Gaussian Imputation to correct 'Informative Missingness' (MNAR) and restore the natural physiological distribution of RVSP."
  - url: "/assets/images/mbi_3nf.jpg"
    image_path: "/assets/images/mbi_3nf.jpg"
    alt: "3NF schema"
    title: "The database layer implements a 5-table Snowflake Schema, enforcing Third Normal Form (3NF) compliance across core tables"
  - url: "/assets/images/mbi_roc_rvsp.jpg"
    image_path: "/assets/images/mbi_roc_rvsp.jpg"
    alt: "Statistical Validation"
    title: "ROC Curve analysis establishing the 5.25 MBI threshold as a high-precision marker for critical pulmonary hypertension."
  - url: "/assets/images/mbi_discordance.jpg"
    image_path: "/assets/images/mbi_discordance.jpg"
    alt: "Mapping the Care Gap"
    title: "Identifying 'deceptively stable' patients who maintain moderate pressures only through aggressive pharmacological compensation."
  - url: "/assets/images/mbi_table.jpg"
    image_path: "/assets/images/mbi_table.jpg"
    alt: "Strategic Triage Mapping"
    title: "Defining the clinical 'Sweet Spot' to prioritize surgical interventions based on the intersection of MBI zones and hemodynamic severity."
---

<style>
.feature-divider { 
    margin-top: 5rem; margin-bottom: 2rem; 
}

.cta {
    margin-top: 5rem !important;
}

.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}

.mbi-table {
    margin-left: auto !important;
    margin-right: auto !important;
    border-collapse: collapse !important;
    display: table !important;
}

.math-block {
    text-align: center;
    font-size: clamp(0.8rem, 4vw, 1.2rem); 
    overflow-x: auto;
    white-space: nowrap;
}
</style>

<div class="headline">
  <h1>Hemodynamic Gap: Medication Intensity as a Surrogate for Cardiac Remodeling</h1>
  <p><strong>The Bottom Line:</strong> The Medication Burden Index successfully stratified <span class="highlight-metric">25.7% of the high-volume clinical cohort into high-acuity risk zones</span>, identifying advanced hemodynamic complexity and critical pulmonary hypertension directly from pharmacological footprints.</p>
</div>

<div class="skills-bar">
  <strong>Tech Stack:</strong> Object-oriented programming (OOP), Pandas, NumPy, Statsmodels, Matplotlib, Seaborn
</div>

<h2>The Challenge: High volume in a compressed timeline</h2>
<p>During a high-stakes 10-day clinical sprint, field teams must rapidly triage an overwhelming influx of patients suffering from complex structural heart conditions. The immediate operational bottleneck lies in patient selection: clinicians must quickly <strong>identify which patients are actively transitioning into critical hemodynamic failure</strong> to fast-track them for resource-intensive Transesophageal Echocardiography (TEE) before their intervention window closes.</p>

<h2>The Data Distortion: Missing Not At Random (MNAR) bias</h2>
<p>To survive the extreme pace of the medical mission, <strong>cardiologists maximize clinical throughput by documenting only critical pathology—leaving fields for healthy cardiac structures entirely blank.</strong> This clinical shorthand introduces a severe Missing Not At Random (MNAR) bias that aggressively skews the dataset, artificially inflates the cohort's apparent baseline severity, and completely breaks statistical models.</p>

<hr class="feature-divider">

{% include feature_row id="solution" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <img src="/assets/images/data_management.png" alt="Icon: Data Processing" class="grid-icon">
    <h3>Bias Mitigation</h3>
    <p>I engineered a <strong>Gaussian Imputation model</strong> aligned with American Society of Echocardiography guidelines. By injecting controlled physiological noise centered on healthy reference parameters, the algorithm recovers the true population variance.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/engineering.png" alt="Icon: Data Processing" class="grid-icon">
    <h3>Feature Engineering</h3>
    <p>I developed the <strong>Medication Burden Index (MBI)</strong>. This parameter normalizes complex polypharmacy arrays against therapeutic ceilings, converting fragmented medication registries into a single, standardized surrogate metric for cardiac remodeling.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/statistic.png" alt="Icon: Data Processing" class="grid-icon">
    <h3>Statistical Triage</h3>
    <p>I executed a <strong>Receiver Operating Characteristic (ROC)</strong> curve analysis to map the engineered MBI scores against objective clinical and hemodynamic indicators, establishing an empirical triage cutoff that fast-tracks high-acuity patients with high precision.</p>
  </div>
</div>

<hr class="feature-divider">

<h2>Quantifying intensity: How the MBI works</h2>
<p>Rather than a simple pill count, the Medication Burden Index evaluates the collective "effort" a patient's cardiovascular system undergoes under active medical support. The engine calculates this by evaluating individual medication dosages relative to their globally recognized maximum therapeutic thresholds and applying class-specific clinical weights:</p>

<div class="math-block">
  $$MBI = \sum \left( \text{Weight} \times \frac{\text{TDD}}{\text{Maximum Dose}} \right)$$
</div>

<p>To standardize this calculation, the pipeline processes two critical variables:</p>

<ul>
  <li><strong>Total Daily Dose (TDD):</strong> The total milligrams consumed by the patient in 24 hours. For example, a patient on Furosemide 40mg every 12h has a $TDD = 80\text{ mg}$.</li>
  <li><strong>Clinical Weights:</strong> The code assigns higher weights (e.g., $3.0$) to loop diuretics and pulmonary vasodilators, and lower weights ($0.5$) to statins or maintenance drugs.</li>
</ul>

<p>By consolidating these complex polypharmacy arrays into a single, standardized continuous variable, the index unmasks advanced disease severity well before a patient ever reaches an echocardiograph station.</p>

<p>The code assigns specific weights based on the severity of the condition being treated, prioritizing signals of cardiac remodeling:</p>

<div class="table-container">
  <table class="mbi-table" style="width: 65%; border: 1px solid #ddd;">
    <thead>
      <tr style="background-color: #003152; color: white;">
        <th style="padding: 12px; border: 1px solid #ddd;">Weight</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Priority</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Medication Classes</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>3.0</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Critical</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Loop diuretics, Pulmonary vasodilators.</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>2.0</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">High</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">RAAS inhibitors, Beta-blockers, SGLT2.</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>1.0</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Moderate</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Anticoagulants, Calcium channel blockers.</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>0.5</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Maintenance</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Statins, Metabolic drugs.</td>
      </tr>
    </tbody>
  </table>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/mbi_triage.png" alt="MBI Distribution and Triage Zones" style="width: 100%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    Figure 1: Correlation between MBI and hemodynamic severity. The three validated operative triage zones are shown.
  </p>
</div>

<div class="project-grid">
  <div class="card">
    <h3>Cohort Rescue</h3>
    <p><strong>Prevented the clinical exclusion of 67% of the patient cohort</strong>. By diagnosing Missing Not At Random (MNAR) clinician shorthand entry patterns, the pipeline successfully preserved valuable population data that standard deletion models would have discarded.</p>
  </div>
  <div class="card">
    <h3>Correcting Overestimation</h3>
    <p><strong>Eliminated a 34.7% artificial inflation of cohort pathology.</strong> The  "Natural Normal" Imputation lowered the apparent average RVSP from a skewed 51.0 mmHg to a physiologically accurate 33.3 mmHg, stabilizing model assumptions.</p>
  </div>
  <div class="card">
    <h3>Unmasking Discordance</h3>
    <p><strong>Identified a 28.9% clinical discordance rate</strong> across complex profiles. The index pinpointed patients maintaining deceptively "moderate" pressures only through aggressive, unsustainable pharmacological compensation.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="dashboard" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <a href="https://public.tableau.com/app/profile/enyel.a.rodr.guez.g./viz/MBIstratification/MBIstratification" target="_blank">
    <img src="/assets/images/mbi_dashboard.png" alt="MBI Distribution and Triage Zones" style="width: 45%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  </a>
</div>

<div class="project-grid">
  <div class="card">
    <h3>Cohort Distribution</h3>
    <span><b>Age Distribution Registry:</b> A continuous histogram detailing the age composition.</span>
    <br>
    <span><b>Gender Split (Donut Chart):</b> Enables rapid auditing of gender-based clinical variations across disease groups.</span>
  </div>
  <div class="card">
    <h3>Pathological Crossroads</h3>
    <span><b>Disease Prevalence:</b> Maps the primary clinical indications driving patient presentation, fully color-coded by MBI Triage Zones.</span>
    <br>
    <span><b>Medication Burden Index Composition:</b> Deconstructs the MBI across distinct medication groups.</span>
  </div>
  <div class="card">
    <h3>Average KPI cards</h3>
    <span><b>Medication Burden Index:</b> Provides an instant read on the standard operational polypharmacy footprint.</span>
    <br>
    <span><b>Right Ventricular Systolic Pressure (RVSP):</b> Tracks the running baseline to provide an un-masked metric of global right-heart performance.</span>
  </div>
</div>

<div class="pull-quote">
  "The MBI transforms a medication list into a <strong>severity metric</strong>, allowing the mission to operate with statistical precision."
</div>

<h2>Reflections: Context Dictates Structure</h2>
<p>Building the <em>Cardio-MBI-Triage-Engine</em> solidified a fundamental truth of specialized health informatics: <strong>pure data analysis patterns fail if they are implemented without deep clinical domain literacy.</strong></p>

<blockquote>
  <strong>Key Takeaway:</strong> An outside data team looking at this missing dataset blindly would have either dropped the incomplete rows entirely (destroying the cohort size) or applied standard, unweighted mean imputations that completely mask the real structural crisis of the field operation.
</blockquote>

<p>By pairing an intimate understanding of cardiologist behavioral patterns in high-stress clinical environments with robust data structure, this pipeline successfully translated fragmented medication registries into high-fidelity diagnostic targets—maximizing the impact of the mission's absolute scarcest asset: the specialist's time.</p>

<hr class="feature-divider">

{% include feature_row id="highlights_title" type="center" %}

{% include gallery id="highlights" %}

<div class="see-more-button">
  <a href="https://github.com/enaromd/Cardio-MBI-Triage-Engine" class="btn btn--primary">View GitHub repository</a>
</div>

<div class="cta">
  <div style="text-align: center;">
    <h3>Leveraging Data for High-Impact Decisions</h3>
    <p>From data processing to predictive model validation, I transform complex variables into operational clarity. If you are looking for a data architect who understands the strategic value of technical precision, let's talk.</p>
    <a href="contact/" class="btn btn--primary">Get in Touch</a>
  </div>
</div>