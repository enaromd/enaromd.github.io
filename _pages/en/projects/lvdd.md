---
layout: splash
title: "Diastolic dysfunction in Hemodialysis"
permalink: portfolio/projects/lvdd/
lang: en
# Social previews
description: "Overcoming sample constraints in End-Stage Renal disease."
header:
  teaser: "/assets/images/lvdd_plot_pr.png"
# This block communicates directly with the SEO plugin
seo:
  type: "article"
  title: "Diastolic dysfunction in Hemodialysis" # Repeat title here
  image: "/assets/images/presentation_sepsis.png"
# Sections
approach:
  - title: "Elevating Clinical Protocols Through Statistical Mentorship"
  - excerpt: "Rescuing an institutional research protocol requires moving past baseline data collection. My advisory approach focused on mentoring clinical investigators to look beyond p-values and visually audit their underlying cohort distributions."
results:
  - title: "Unmasking the Risk Magnitude"
  - excerpt: "The audited protocol revealed that an alarming <span class='highlight-metric'>72.5% of the hemodialysis cohort was actively suffering from LVDD</span>. By overcoming the limitations of a small, single-center sample through robust modeling, my biostatistical mentorship guided the team to extract uninflated effect sizes."
---
<style>
.feature-divider {
  margin-top: 5rem;
  margin-bottom: 2rem;
}

.cta {
  margin-top: 5rem !important;
}

.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}
</style>

<div class="headline">
    <h1>Cardiorenal Triage: Quantifying Robust Prevalence Ratios Under Survival Bias</h1>
    <p><strong>The Bottom Line:</strong> By deploying a robust Poisson regression model to adjust for single-center sample constraints, this analysis isolated <span class="highlight-metric">chronic Hypertension (Adjusted PR: 2.22) and glycemic control (Adjusted PR: 1.16)</span> as the dominant independent drivers of heart failure in maintenance hemodialysis, locking down the risk magnitude.</p>
</div>

<div class="skills-bar">
    <p><strong>Core Strategies:</strong> Bias mitigation, robust regression modeling, multi-variate confounding control</p>
</div>

<h2>The Challenge: Silent Cardiovascular Mortality</h2>
<p>In patients undergoing maintenance hemodialysis for advanced Stage G5 Chronic Kidney Disease (CKD), <strong>cardiovascular disease stands as the leading cause of mortality</strong>. Left Ventricular Diastolic Dysfunction (LVDD) represents an early, silent marker of this cardiorenal crisis.</p>

<h2>A Bias That Survives</h2>
<p>Cross-sectional datasets in active dialysis wards suffer inherently from <strong>Neyman Bias (survival bias)</strong>. Because the highest-acuity cardiorenal patients often pass away or face emergency hospitalization before data is even captured, standard statistical models end up analyzing <strong>an unnaturally "stable" survivor cohort.</strong></p>

<hr class="feature-divider">

{% include feature_row id="approach" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <img src="/assets/images/statistic.png" alt="Icon: Visualization" class="grid-icon">
    <h3>Visualizing Hidden Variance</h3>
    <p>I coached the team to deploy <strong>distribution visualizations</strong> to unmask a critical pattern that no summary table could reveal: severe right-skewed tail variance with multiple uncontrolled outliers stretching up to 10% HbA1c. </p> 
  </div>
  <div class="grid-item">
    <img src="/assets/images/selection.png" alt="Icon: Analysis" class="grid-icon">
    <h3>Analytical Pivot</h3>
    <p>I guided the investigative team toward a <strong>Poisson Regression model with robust variance</strong>, which allowed them to calculate uninflated Prevalence Ratios (PR) that more accurately translate the clinical magnitude of the risk.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/timeline.png" alt="Icon: Sequence" class="grid-icon">
    <h3>Sequential Regressions</h3>
    <p>I structured a <strong>three-phase multi-variate regression matrix</strong>: models adjusted for baseline demographics (age/sex), nutritional/metabolic noise (BMI/Albumin), and a final multi-system integration phase.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/lvdd_plot_pr.png" alt="LVDD regression models" style="width: 100%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    Figure 1: Stratified Multivariate Poisson Regressions. By replacing unstable logistic odds with robust sandwich covariance estimators, the framework successfully controls for severe sample constraints ($N = 51$) without over-saturating the parameters.
  </p>
</div>

<div class="project-grid">
  <div class="card">
    <h3>The Toll of Hypertension</h3>
    <p><strong>Chronic Hypertension was the most aggressive clinical driver.</strong> The mentored robust model quantified a massive independent effect size, yielding an adjusted Prevalence Ratio (PR) of 2.22 that more than doubled the probability of advanced cardiac remodeling.</p>
  </div>
  <div class="card">
    <h3>The Metabolic Toll</h3>
    <p><strong>Glycemic destabilization posed a compounding threat.</strong> Moving past aggregate table limitations, the regression model determined that each single 1% HbA1c increment incurred a continuous 16% increase in LVDD prevalence risk (Adjusted PR: 1.16).</p>
  </div>
  <div class="card">
    <h3>Model Stability</h3>
    <p><strong>The multi-variate architecture achieved high mathematical stability.</strong> This was validated by a Likelihood Ratio Chi-Square significance of $p = 0.037$, proving the sequential confounding controls successfully accounted for baseline variance.</p>
  </div>
</div>

<div class="pull-quote">
  "True biostatistical mentorship isn’t about chasing <i>p-values</i>; it’s about coaching a clinical team to <strong>recognize where biological noise ends and true risk begins.</strong>"
</div>

<h2>Reflections: Methodology Dictates Interpretation</h2>
<p>Guiding the biostatistical layer of this cardiorenal protocol solidified a fact of healthcare analysis: <strong>blind mathematical modeling fails when disconnected from clinical pathophysiology.</strong> Rescuing this analysis required mentoring the investigative team to look past raw statistical software outputs and critically evaluate the biological trade-offs within their data architecture.</p>

<div class="project-grid">
  <div class="card">
    <h3>The Ceiling Effect</h3>
    <p><strong>Universal pathology destroys statistical variance.</strong> Classic risk factors like profound anemia failed to reach significance because they are omnipresent in Stage G5 CKD. I coached the team to focus on volatile, high-impact drivers like metabolic shifts instead.</p>
  </div>
  <div class="card">
    <h3>The Lifespan Trade-off</h3>
    <p><strong>Biological mechanics distort raw endpoints.</strong> Hemodialysis mechanically destroys red blood cells, artificially lowering raw HbA1c values. I advised the team that our uncovered 16% risk surge per HbA1c point is a highly conservative effect; the real-world toll is likely much higher.</p>
  </div>
  <div class="card">
    <h3>Future Optimization</h3>
    <p><strong>Conquering survival bias requires longitudinal tracking.</strong> While our robust Poisson model successfully stabilized this cross-sectional snapshot, Neyman Bias remains an inherent threat. Therefore I recommend a longitudinal registry following cohorts from day one.</p>
  </div>
</div>

<div class="cta">
  <div style="text-align: center;">
    <h3>Let’s Turn Your Ideas into Action</h3>
    <p>
      Great breakthroughs are born from collaboration. Due to my commitment to technical precision and impactful storytelling, I accept a limited number of projects to ensure the rigor each challenge deserves.
    </p>
    <p><strong>If you are looking to convert complex evidence into strategic decisions, let's talk.</strong></p>
    <a href="contact/" class="btn btn--primary">Get in Touch</a>
  </div>
</div>