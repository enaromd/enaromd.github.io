---
layout: splash
title: Enyel Rodríguez
permalink: /
lang: en
author_profile: false
# Social previews
description: "I help transform clinical complexity into explanatory and predictive models that contribute to making strategic decisions."
header:
  teaser: "/assets/images/hero_preview.png"
# This block communicates directly with the SEO plugin
seo:
  type: "article"
  title: "Enyel Rodríguez" # Repeat title here
  image: "/assets/images/hero_preview.png"    
# Certifications section
certifications: 
  - title: "Certifications"
  - excerpt: "My certifications are not just credentials; they are proof of an unwavering commitment to excellence. From statistical analysis to effective communication, each skill is a key piece in ensuring our projects are technically sound, well-communicated, and high-impact."
# Projects section
projects: 
  - title: "Projects"
  - excerpt: "My projects are not just a summary of my work; they are a testament to my dedication to achieving high-impact results. Through every analysis, my goal is to ensure that data is not only correct but tells a compelling story backed by evidence, capable of inspiring action and innovation."  
---
<div class="custom-splash-hero">
  <div class="hero-main-layout">
    <img src="/assets/images/web_hero_eng.png" alt="Profile picture" class="hero-img">
    <div class="hero-text-content">
      <h1>Beyond the stethoscope: <br>Evidence with health statistics</h1>
      <p>I am Enyel Rodríguez, MD and Clinical Data Analyst. I bridge the critical gap between front-line clinical workflows and rigorous biostatistics. By engineering validated clinical indices into Real-World Data (RWD) pipelines, I help research teams build explanatory models that translate directly into safer, evidence-based patient outcomes.</p>

      <a href="contact/" class="btn btn--primary">Get in touch</a>
    </div>
  </div>
  <div class="trust-bar-glass">
    <div class="trust-content">
      <span class="trust-label">Certification badges</span>
      <div class="badge-flex-container">
        <a href="https://www.credly.com/badges/b87a61e6-0b8d-41ff-b8a5-f52833fca99f" target="_blank">
          <img src="/assets/images/badge-meta-database-engineer.png" alt="Meta Database Engineer" class="cert-badge">
        </a>
        <!-- <a href="https://www.credly.com/badges/b87a61e6-0b8d-41ff-b8a5-f52833fca99f" target="_blank">
          <img src="/assets/images/badge-tableau-analytics.png" alt="Tableau Data Analyst" class="cert-badge">
        </a>
        <a href="https://www.credly.com/badges/b87a61e6-0b8d-41ff-b8a5-f52833fca99f" target="_blank">
          <img src="/assets/images/badge-google-analytics.png" alt="Google Data Analyst" class="cert-badge">
        </a> -->
      </div>
    </div>
  </div>
</div>

<div class="hero_problem">
  <div class="hero__image-wrapper" data-image-src="/assets/images/hero_problem.png"></div>
  <div>
    <h1>The Cost of Distorted Data</h1>
    <p>In clinical trials and observational studies, evidence is only as reliable as its source. But clinical databases are notoriously messy, fraught with systematic biases and missing parameters.</p>
    <p>When patient data is parsed without a deep, front-line understanding of clinical workflows, critical variables are misclassified, cohort selections become biased, and biostatistical models fail to reflect true patient outcomes.</p>
    <p>For research organizations and healthcare systems, clinical data misinterpretation is more than a technical error—it is a direct threat to patient safety and therapeutic efficacy.</p>
  </div>
</div>

<hr class="feature-divider">

<div class="hero_solution">
  <div class="hero__image-wrapper" data-image-src="/assets/images/hero_solution.png"></div>
  <div>
    <h1>Success: When evidence guides you</h1>
    <p>Imagine a scenario where your data gives you the answers you need, when you need them.</p>
    <p>Success is having a clear understanding of the information you already have, discovering perspectives you didn't even know existed. It's moving from uncertainty to certainty.</p>
    <p>This translates into smart strategic decisions that drive efficiency, optimize clinical operations and, most importantly, improve patient outcomes.</p>
    <p>With a solid foundation of evidence, your decisions will not only be correct, but will also inspire confidence and leadership.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="certifications" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <a href="https://www.coursera.org/account/accomplishments/professional-cert/TE1VSZSPDZ56">
      <img src="/assets/images/certification_database_engineer.jpg" alt="Certification: Meta Database Engineer">
      <h3>Meta Database Engineer</h3>
      <p>Meta</p>
      <p>Relational schema design, advanced MySQL optimization, and Python-driven ETL pipeline development.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="https://www.coursera.org/account/accomplishments/specialization/ZRXSQLDMFXPR">
      <img src="/assets/images/certification_biostatistics.jpg" alt="Certification: Biostatistics in Public Health">
      <h3>Biostatistics in Public Health</h3>
      <p>Johns Hopkins University</p>
      <p>Statistical inference, regression methods, and survival analysis.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="https://www.coursera.org/account/accomplishments/specialization/PJX2HNZZYYJD">
      <img src="/assets/images/certification_statistics-python.jpg" alt="Certification: Statistics with Python">
      <h3>Statistics with Python</h3>
      <p>University of Michigan</p>
      <p>Multilevel models, sampling weights, and logistic/linear regression adjustment.</p>
    </a>
  </div>
</div>

<div class="see-more-button">
  <a href="portfolio/certifications/" class="btn btn--primary">See more certifications</a>
</div>

<hr class="feature-divider">

{% include feature_row id="projects" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <a href="portfolio/projects/mbi/">
      <img src="/assets/images/mbi_triage.png" alt="Project: Cardio-MBI-Triage-Engine">
      <h3>Medication Burden Index (MBI)</h3>
      <p>Engineering a clinical data pipeline with 3NF/Snowflake schemas and 'natural normal' imputation to overcome structural missingness in a 10-day cardiology mission.</p>
      <p><strong>Impact:</strong> Classifies 25.7% of high-acuity patients into high-benefit intervention zones under severe field constraints.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="portfolio/projects/lvdd/">
      <img src="/assets/images/lvdd_plot_pr.png" alt="Project: LVDD in Hemodialysis">
      <h3>Diastolic Dysfunction in Maintenance Hemodialysis</h3>
      <p>Deploying multivariate Poisson regression with robust sandwich covariance estimators to neutralize sample limits.</p>
      <p><strong>Impact:</strong> Identification of chronic Hypertension (PR: 2.22) as the strongest driver of heart failure in hemodialysis.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="portfolio/projects/sepsis/">
      <img src="/assets/images/presentation_sepsis.png" alt="Project: Sepsis Adaptation">
      <h3>Septic Shock Clinical Evidence Operationalization</h3>
      <p>Deconstructing high-dimensional trial data (ANDROMEDA-SHOCK, CLOVERS, SMART) into actionable, localized bedside workflows.</p>
      <p><strong>Impact:</strong> Reduction of clinical variability through standardized, data-driven critical care consensus frameworks.</p>
    </a>
  </div>
</div>

<div class="see-more-button">
  <a href="portfolio/projects/" class="btn btn--primary">See more projects</a>
</div>

<hr class="feature-divider">

<div class="about-hero">
  <img src="/assets/images/web_hero-about.png" alt="About me">
  <div>
    <h1>About Me</h1>
    <p>As a practicing physician, I have spent years listening to hearts, stabilizing critical patients under acute stress, and running municipal emergency departments. But I realized that the greatest barrier to modern patient care isn’t clinical capacity—it is the integrity of the data that shapes clinical protocols.</p>
    <p>This realization transformed me into a dual-force: an active MD who is also a certified database engineer and biostatistician. I do not just analyze rows in a database; I understand the human workflow that generated them, the clinical indices required to normalize them, and the biostatistical outcomes we must strive for.</p>
  </div>
</div>

<div class="cta">
  <div>
    <h3>Let's transform your ideas into actions</h3>
    <p>
      I firmly believe that <strong>great discoveries are born from collaboration and shared vision</strong>. 
      Due to my commitment to technical precision, I accept a limited number of challenges in parallel, 
      ensuring that each project receives the rigor and depth it deserves.
    </p>
    <p>
      <strong>If you are ready to turn data into actions, I would love to hear your proposal.</strong>
    </p>
    <a href="contact/" class="btn btn--primary">Get in touch</a>
  </div>
</div>