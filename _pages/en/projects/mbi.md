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
approach:
  - title: "Project structure"
  - excerpt: "The pipeline is split into three modular, production-ready stages to preserve strict data lineage and reproducibility:"
results:
  - title: "The Impact Factor: Predictive Precision"
  - excerpt: "The model validated that an MBI > 5.25 identifies critical pulmonary hypertension with 85% accuracy. This tool enables 'intake triage,' prioritizing patients who would benefit most from intervention and optimizing the mission's scarcest resource: the specialists' time."
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
  - url: "/assets/images/mbi_decomposed.jpg"
    image_path: "/assets/images/mbi_decomposed.jpg"
    alt: "Deconstructing the Index"
    title: "A visual breakdown of how different pharmacological classes contribute to the total MBI score across the cohort."
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
    <h1>Quantifying Clinical Gaps: MBI as a Surrogate for Cardiac Remodeling</h1>
    <p>Data Analysis applied to the 2025 Cardiology Mission in León, Nicaragua.</p>
</div>

<div class="skills-bar">
    <strong>Tech Stack:</strong> Object-Oriented Programming (OOP), <code>Pandas</code>, <code>NumPy</code>, <code>Statsmodels</code>, <code>Scikit-learn</code>, <code>Matplotlib/Seaborn</code>
</div>

<h2>The Core of the Analysis: What is the 'Medication Burden Index' (MBI)?</h2>
<p>
  The <strong>MBI</strong> is a weighted index that quantifies the intensity of a patient's pharmacological treatment. Rather than simply counting pills, the MBI evaluates the "effort" the cardiovascular system is making under medical support.
</p>

<div class="math-block">
  $$MBI = \sum \left( \text{Weight} \times \frac{\text{TDD}}{\text{Maximum Dose}} \right)$$
</div>

<p>To achieve this, the engine processes two critical variables:</p>

<ul>
  <li><strong>Total Daily Dose (TDD):</strong> The total milligrams consumed by the patient in 24 hours. For example, a patient on Furosemide 40mg every 12h has a $TDD = 80mg$.</li>
  <li><strong>Clinical Weights:</strong> The code assigns higher weights (e.g., $3.0$) to loop diuretics and pulmonary vasodilators, and lower weights ($0.5$) to statins or maintenance drugs.</li>
</ul>

<p>
  This architecture allows the MBI to act as a <strong>surrogate for hemodynamic severity</strong>, capturing signs of heart failure well before the patient even reaches the echocardiograph.
</p>

<h3>Weighting Logic: Clinical Weights</h3>
<p>
  The code assigns specific weights based on the severity of the condition being treated, prioritizing signals of cardiac remodeling:
</p>

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

<h2>The Challenge: The "Silence of the Normals" (MNAR Bias)</h2>
<p>In high-volume missions, data is often incomplete: cardiologists focused execution speed on critical pathology, leaving fields for healthy structures entirely blank. This creates a <strong>Missing Not At Random (MNAR)</strong> bias that exhibits a heavily distorted mean $\text{RVSP}$ of $51.0\text{ mmHg}$, omitting the healthy baseline spectrum completely.</p>

<hr class="feature-divider">

{% include feature_row id="approach" type="center" %}

<div class="grid-container">
  <div class="grid-item">
      <img src="/assets/images/data_management.png" alt="Icon: Data Processing" class="grid-icon">
      <h3>Extraction & Bias Mitigation</h3>
      <p>Built an evidence-based Gaussian 'Natural Normal' Imputation model using American Society of Echocardiography guidelines to restore true population variance.</p>
  </div>
  <div class="grid-item">
      <img src="/assets/images/data_architecture.png" alt="Icon: Clinical Architecture" class="grid-icon">
      <h3>3NF Schema Engineering</h3>
      <p>Engineered and deployed a robust MySQL database structure. Fragmented polypharmacy arrays were normalized into a strict, relational database model.</p>
  </div>
  <div class="grid-item">
      <img src="/assets/images/statistic.png" alt="Icon: Statistical Validation" class="grid-icon">
      <h3>OLS residual mapping</h3>
      <p>Calculated Ordinary Least Squares (OLS) regression residuals to isolate patients whose severe underlying disease is actively masked by intensive therapies.</p>
  </div>
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
    <h3>The Key Zone</h3>
    <p>Identification of <strong>Zone 2 (MBI 4.0 - 5.5)</strong>: patients with mixed pathology who gain the most benefit from valve replacement.</p>
  </div>
  <div class="card">
    <h3>Predictive Power</h3>
    <p>AUC of <strong>0.73/0.82</strong> for detecting hemodynamic compromise. The MBI acts as a preliminary "Chemical Echocardiogram."</p>
  </div>
  <div class="card">
    <h3>Operational Efficiency</h3>
    <p>Relieves pressure on diagnostic stations by prioritizing patients in <strong>Pharmacological Exhaustion</strong> (MBI > 5.5).</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="dashboard" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/mbi_dashboard.png" alt="MBI Distribution and Triage Zones" style="width: 45%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
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