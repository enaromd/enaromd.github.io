---
layout: splash
title: "Clinical Obesity in NHANES 2021-2023"
permalink: portfolio/projects/nhanes_obesity/
lang: en
description: "When Weight Doesn’t Weigh the Same on Everyone: Applying The Lancet’s Clinical Obesity Framework"
header:
  teaser: "/assets/images/plot_framework_sankey.png"
seo:
  type: "article"
  title: "Clinical Obesity framework (NHANES 2021–2023)"
  image: "/assets/images/obesity_teaser.png"
approach:
  - title: "Cohort Filtration, Risk Engineering & GEE Modeling"
  - excerpt: "Executing an end-to-end biostatistical pipeline—from structured cohort attrition (N = 1,816) to composite index calculation and survey-weighted Risk Ratio estimation."
flowchart:
  - title: "Cohort Selection & Systematic Attrition"
  - excerpt: "Executing a filtration pipeline to control for complex survey skips, fasting subsample weights, and phenotypic boundary criteria."
table1:
  - title: "Baseline Population Stratification (Table 1)"
  - excerpt: "Evaluating survey-weighted demographic, examination, and biomarker gradients across Control, Peripheral, and Classic phenotype cohorts (N = 1,588)."
results:
  - title: "Phenotypic Disparities & METS-IR Performance"
  - excerpt: "Uncovering subclinical metabolic dysregulation and end-organ damage obscured by standard anthropometric screening."
forest:
  - title: "Phenotypic & Index-Adjusted Relative Risk"
  - excerpt: "Tracking hepatic fibrosis risk from unadjusted phenotype baselines (M1) through cross-spillover surrogates (M2) to fully integrated phenotype-index models (M3)."
sankey:
  - title: "From Clinical Phenotypes to Domain Risk and End-Organ Damage"
  - excerpt: "Mapping the survey-weighted cascade from baseline body composition through subclinical domain risk clusters into overt organ impairment."
---
<style>
.feature-divider {
  margin-top: 5rem;
  margin-bottom: 2rem;
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

.highlight-metric {
  color: #b80f0a;
  font-weight: 600;
}
</style>

<div class="headline">
  <h1>When Weight Doesn’t Weigh the Same on Everyone: Applying The Lancet’s Clinical Obesity Framework</h1>
  <p><strong>The Bottom Line:</strong> The Metabolic Score for Insulin Resistance <span class="highlight-metric">(METS-IR) showed a robust independent effect for FibroScan-confirmed hepatic fibrosis (Adjusted RR = 2.9</span>) and the best overall model fit (QIC = 815.7) compared to other lipid and glycemic ratios in fully adjusted models.</p>
</div>

<div class="skills-bar">
  <p><strong>Tech Stack:</strong> Python, PyReadStat, Pandas, NumPy, Matplotlib, Missingno, PyArrow</p>
</div>

<h2>The Challenge: The diagnostic gap of Body Mass Index (BMI)</h2>
<p><strong>Clinicians almost universally rely on Body Mass Index (BMI ≥ 30 kg/m²) as the default diagnostic gatekeeper for obesity assessment</strong>. By relying solely on body weight and height ratios, standard screening protocols overlook significant subclinical cardiometabolic, hepatic, and renal involvement in metabolically unhealthy normal-weight individuals.</p>

<h2>The Translation Gap: Anthropometric Ratios and Risk Indices</h2>
<p>Operationalizing The Lancet’s Clinical Obesity Framework requires moving beyond raw BMI by calculating specific anthropometric ratios—such as Waist-to-Height Ratio (WHtR)—to accurately define clinical obesity phenotypes.</p>
<p>Furthermore, raw NHANES data stores biomarkers as isolated laboratory parameters across complex survey subsamples. <strong>To systematically quantify cardiovascular, metabolic, and organ-specific risk, these individual inputs must be translated into validated clinical risk indices</strong> (e.g., METS-IR, FIB-4, FLI, and AHA PREVENT) to capture subclinical vulnerability prior to overt organ impairment.</p>

<hr class="feature-divider">

{% include feature_row id="approach" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <img src="/assets/images/timeline.png" alt="Icon: Attrition" class="grid-icon">
    <h3>Cohort Attrition</h3>
    <p>I built an intentional filtration pipeline <strong>isolating working-age adults (ages 18 to 64)</strong> from the NHANES 2021–2023 cycle, systematically controlling for pregnancy, unweighted records, and missing baseline parameters (N = 11,933 $\to$ 1,816).</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/engineering.png" alt="Icon: Engineering" class="grid-icon">
    <h3>Risk Indices Engineering</h3>
    <p>I transformed <strong>raw data into validated clinical risk indices</strong>, including the Metabolic Score for Insulin Resistance (METS-IR), Fatty Liver Index (FLI), Fibrosis-4 Index (FIB-4), and AHA PREVENT cardiometabolic-renal risk scores.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/statistic.png" alt="Icon: Statistics" class="grid-icon">
    <h3>Survey-Weighted Risk Ratios</h3>
    <p>I applied <strong>Generalized Estimating Equations (GEE) with log link and Poisson family</strong>, incorporating survey design parameters (primary sampling units <code>SDMVPSU</code>, strata <code>SDMVSTRA</code>, and fasting weights <code>WTSAF2YR</code>) to calculate population-adjusted Risk Ratios (RR).</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="flowchart" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/final_flowchart.svg" alt="STROBE flowchart" style="width: 100%; max-width: 520px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    <strong>Figure 1. Cohort Attrition Pipeline.</strong> Sequential filtration of the NHANES 2021–2023 master dataset (N = 11,933). Enforcing morning fasting protocol compliance (<code>WTSAF2YR</code>), working-age boundaries (18–64 years), and complete-case data hygiene isolated 1,816 fasting adults. Pruning 228 ambiguous unclassified records established a final phenotypically valid analysis cohort of N = 1,588 adults.
  </p>
</div>

<hr class="feature-divider">

{% include feature_row id="table1" type="center" %}

<div class="table-container" style="overflow-x: auto; margin: 2rem 0;">
  <table class="mbi-table" style="width: 100%; max-width: 750px; border: 1px solid #ddd;">
    <thead>
      <tr style="background-color: #003152; color: white;">
        <th style="padding: 12px; border: 1px solid #ddd; text-align: left;">Variable</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">Overall</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">Control</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">Peripheral</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">Classic</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Age</strong> (years)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">40.92</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">32.05</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">45.55</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">42.94</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Systolic BP</strong> (mmHg)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">117.21</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">112.75</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">118.29</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">119.31</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Diastolic BP</strong> (mmHg)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">74.59</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">68.59</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">74.11</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">78.64</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Pulse rate</strong> (bpm)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">70.88</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">69.30</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">70.41</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">72.06</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Fasting Glucose</strong> (mg/dL)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">105.06</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">98.72</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">103.94</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">111.31</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Triglycerides</strong> (mg/dL)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">108.60</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">74.17</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">117.46</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">124.36</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>HDL Cholesterol</strong> (mg/dL)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">53.62</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">60.70</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">53.50</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">49.59</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Liver Stiffness</strong> (kPa)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">5.76</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">4.86</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">5.42</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">6.79</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>eGFR</strong> (mL/min/1.73m²)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">102.51</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">108.14</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">99.57</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">101.41</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Hepatic damage</strong> (%)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">13.96</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">4.08</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">9.55</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">25.13</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Metabolic damage</strong> (%)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">6.42</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.09</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">7.90</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">9.82</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Renal damage</strong> (%)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.99</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.00</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.93</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">1.54</td>
      </tr>
    </tbody>
  </table>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}

<div class="project-grid">
  <div class="card">
    <h3>BMI & Unadjusted Hepatic Damage</h3>
    <p>Unadjusted models show that the <strong>BMI-driven Classic Phenotype strongly tracks hepatic damage (RR = 5.19).</strong></p>
    <p>However, <strong>relying solely on BMI ignores 35.0% of adults</strong> categorized as Peripheral, who still face elevated hepatic risk (RR = 1.95).</p>
  </div>
  <div class="card">
    <h3>METS-IR as a Surrogate for Hepatic Damage Risk</h3>
    <p>METS-IR functions as a <strong>robust independent driver of hepatic damage</strong> across the integrated model <strong>(RR = 2.87).</strong></p>
    <p>Crucially, it detects marked damage risk surges in both the isolated classic (RR = 2.76) and isolated peripheral (RR = 3.60) cohorts.</p>
  </div>
  <div class="card">
    <h3>Phenotypes & Domain Risk Disparities</h3>
    <p>Encompassing 45.8% of adults, the <strong>Classic Phenotype drives the bulk of multi-domain risk (28.3% overall).</strong></p>
    <p>As a result, it <strong>maintains higher risk of end-organ damage (RR = 2.44)</strong> than the Peripheral Phenotype (RR = 1.91).</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="forest" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/plot_indices_forest_coefficients.png" alt="Forest Plot comparing Risk Ratios across indices" style="width: 100%; max-width: 850px; border-radius: 8px;">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    <strong>Figure 2. Sequential Risk Attenuation in GEE Poisson Regression.</strong> Comparing baseline structural phenotypes (M1) against integrated models (M3). Inclusion of the METS-IR diagnostic cutoff (RR = 2.87) attenuates the Classic Phenotype risk ratio from RR = 5.19 (95% CI: 2.94-9.17) down to RR = 2.44 (95% CI: 1.22-4.89), confirming metabolic dysfunction as a primary mediator of hepatic end-organ damage.
  </p>
</div>

<hr class="feature-divider">

{% include feature_row id="sankey" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/plot_framework_sankey.png" alt="Sankey Diagram from obesity phenotypes through risk domains towards end-organ damage" style="width: 100%; max-width: 850px; border-radius: 8px;">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    <strong>Figure 3. Phenotypic Trajectories Across Domain Risk Clusters.</strong> Survey-weighted flow diagram mapping obesity phenotypes to domain damage risk. Healthy controls flow exclusively to zero organ damage, whereas the Classic Phenotype acts as the primary origin for multi-domain dysfunction ($\ge 2$ organ systems), reinforcing the synergistic risk of hepatic and metabolic strain.
  </p>
</div>

<div class="pull-quote">
  "<strong>Reframing obesity</strong> from a static anthropometric number <strong>to a multi-system metabolic continuum</strong> is the essential first step toward true precision medicine—proving that body weight alone cannot dictate clinical vulnerability."
</div>

<h2>Reflection: Redefining Obesity Beyond the Scale</h2>

<p>Our findings challenge the long-standing reliance on BMI as a sole diagnostic gatekeeper: two individuals with similar anthropometric measurements can harbor radically different trajectories of subclinical organ strain.</p>

<blockquote>
    <strong>Key Takeaway:</strong> Metabolic health cannot be inferred from body mass alone. Within normal-BMI adults classified into the Peripheral Obesity phenotype, crossing the high METS-IR threshold triggers a <strong>3.60-fold relative risk surge</strong> for FibroScan-confirmed hepatic fibrosis, demonstrating that subclinical insulin resistance drives tissue damage long before overt clinical obesity manifests.
</blockquote>

<p>Translating these biostatistical insights into real-world care requires embedding automation of risk indices—such as METS-IR, FIB-4, and FLI—directly into electronic health record (EHR) pipelines. Automating these calculations from routine laboratory panels creates a fundamental paradigm shift: moving healthcare away from reactive, late-stage disease management toward proactive, algorithmically guided subclinical intervention.</p>

<div class="cta">
  <div style="text-align: center;">
    <h3>Leveraging Data for High-Impact Decisions</h3>
    <p>From data processing to predictive model validation, I transform complex variables into operational clarity. If you are looking for a data analyst who understands the strategic value of technical precision, let's talk.</p>
    <a href="contact/" class="btn btn--primary">Get in Touch</a>
  </div>
</div>