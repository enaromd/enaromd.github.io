---
layout: splash
title: "Projects"
permalink: portfolio/projects/
lang: en
# Social previews
description: "My projects are more than just a summary of my work; they are a testament to my dedication to achieving high-impact results."
# Header 
header:
  overlay_filter: rgba(0, 19, 32, 0.8)
  overlay_image: /assets/images/splash-projects.jpg
  teaser: "/assets/images/splash-projects.jpg"
excerpt: 'My projects are more than just a summary of my work; they are a testament to my dedication to achieving high-impact results. <br>Through every analysis, my goal is to ensure that data is not only correct but tells a compelling story backed by evidence, capable of inspiring action and innovation.'  
seo:
  type: "article"
  title: "Projects" # Repeat title here
  image: "/assets/images/splash-projects.jpg"
presentations:
  - title: "Presentations and mentorship"
data:
  - title: "Data and Databases"
---

<style>
.feature-divider {
  margin-top: 5rem;
  margin-bottom: 2rem;
}

.cta {
  margin-top: 5rem !important;
}
</style>

{% include feature_row id="data" type="center" %}
<div class="grid-container">
  <div class="grid-item">
    <a href="mbi/">
      <img src="/assets/images/mbi_triage.png" alt="Project: Cardio-MBI-Triage-Engine">
      <h3>Medication Burden Index (MBI)</h3>
      <p>Engineering a clinical data pipeline with 3NF/Snowflake schemas and 'natural normal' imputation to overcome structural missingness in a 10-day cardiology mission.</p>
      <p><strong>Impact:</strong> Classifies 25.7% of high-acuity patients into high-benefit intervention zones under severe field constraints.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="little-lemon-db/">
      <img src="/assets/images/database_schema.png" alt="Project: Little Lemon">
      <h3>Relational Database and MySQL-Python integration</h3>
      <p>Engineering a 3NF ecosystem and a programmatic bridge to automate complex restaurant operations.</p>
      <p><strong>Impact:</strong> 100% transaction integrity and elimination of data redundancy through stored procedures.</p>
    </a>
  </div>
</div>

{% include feature_row id="presentations" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <a href="lvdd/">
      <img src="/assets/images/lvdd_plot_pr.png" alt="Project: LVDD in Hemodialysis">
      <h3>Diastolic Dysfunction in Maintenance Hemodialysis</h3>
      <p>Deploying multivariate Poisson regression with robust sandwich covariance estimators to neutralize sample limits.</p>
      <p><strong>Impact:</strong> Identification of chronic Hypertension (PR: 2.22) as the strongest driver of heart failure in hemodialysis.</p>
    </a>
  </div>
  <div class="grid-item">
  <a href="sepsis/">
    <img src="/assets/images/presentation_sepsis.png" alt="Project: Sepsis Adaptation">
    <h3>Septic Shock Clinical Evidence Operationalization</h3>
    <p>Deconstructing high-dimensional trial data (ANDROMEDA-SHOCK, CLOVERS, SMART) into actionable, localized bedside workflows.</p>
    <p><strong>Impact:</strong> Reduction of clinical variability through standardized, data-driven critical care consensus frameworks.</p>
  </a>
  </div>
  <div class="grid-item">
  <a href="pharmacovigilance/">
    <img src="/assets/images/project_pharmacovigilance.png" alt="Project: XV Scientific Conference">
    <h3>Pharmacovigilance and Clinical Narrative</h3>
    <p>Characterization of adverse drug reactions (ADR) using WHO causality algorithms and visual narrative design.</p>
    <p><strong>Impact:</strong> First place SILAIS 2023 for excellence in high-impact scientific communication.</p>
  </a>
  </div>
</div>


<div class="cta">
  <div>
    <h3>Let's Transform Your Ideas into Action</h3>
    <p>
      I firmly believe that <strong>great discoveries are born from collaboration and shared vision</strong>. 
      Due to my commitment to technical precision, I accept a limited number of challenges concurrently, 
      ensuring that each project receives the rigor and depth it deserves.
    </p>
    <p>
      <strong>If you are ready to turn data into action, I would love to hear your proposal.</strong>
    </p>
    <a href="contact/" class="btn btn--primary">Get in Touch</a>
  </div>
</div>