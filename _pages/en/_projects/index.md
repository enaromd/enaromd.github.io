---
layout: page
title: "Projects"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/
lang: en

splash_title: "Projects"
splash_text: "Effective healthcare analytics requires understanding both the patient at the bedside and the algorithm in the pipeline. \n\nHere, you will find applied research projects ranging from cardiometabolic risk stratification in national surveys to customized triage indices for humanitarian medical missions."
splash_image: "/assets/images/splash-projects.jpg"

sections:
  - heading: "Database structures and Analytical Pipelines"
    description: "Designing third normal form (3NF) and Snowflake relational schema, stored procedures, and automated Python scripts to clean, process, and analyze clinical datasets without compromising diagnostic context."

    cards:
      - title: Medication intensity and Valvular Heart Disease
        image: "/assets/images/cover_project_mbi.png"
        description: "Classifies 25.7% of high-acuity patients into high-benefit intervention zones under severe field constraints."
        details_url: "mbi/"
        github_url: "https://github.com/enaromd/Cardio-MBI-Triage-Engine"
      - title: Clinical Obesity and NHANES 2021-2023
        image: "/assets/images/cover_project_nhanes-obesity.png"
        description: "Uncovers a 3.6x risk surge in normal-BMI adults with peripheral obesity missed by standard screening."
        details_url: "nhanes_obesity/"
        github_url: "https://github.com/enaromd/clinical-obesity"
      - title: Relational Database and MySQL-Python integration
        image: "/assets/images/cover_project_database.png"
        description: "100% transaction integrity and elimination of data redundancy through stored procedures."
        details_url: "little-lemon/"
        github_url: "https://github.com/enaromd/db-capstone-project"

  - heading: "Evidence Synthesis and Methodological Mentorship"
    description: "Guiding clinical teams through systematic bias evaluation, trial interpretation, and localized workflow adaptations to ensure evidence-based standardization in acute care."

    cards:
      - title: Diastolic Dysfunction in Maintenance Hemodialysis
        image: "/assets/images/cover_project_lvdd.png"
        description: "Identifies chronic Hypertension (PR: 2.22) as the strongest driver of heart failure in hemodialysis."
        details_url: "lvdd/"
      - title: Septic Shock Clinical Evidence Operationalization
        image: "/assets/images/cover_project_presention_sepsis.png"
        description: "Reduction of clinical variability through standardized, data-driven critical care consensus frameworks."
        details_url: "septic-shock/"
      - title: "Award-Winning Visual Strategy: Pharmacovigilance"
        image: "/assets/images/presentation_pharmacovigilance_05.jpg"
        description: "First Place at the XV Scientific Conference for disrupting traditional clinical reporting."
        details_url: "pharmacovigilance/"

cta:
  heading: "Bridge Frontline Clinical Reality with Technical Execution"
  description: "Effective healthcare analytics starts with knowing how data is born at the bedside—including the hectic workflows and human factors that warp raw records. If your team needs someone who combines frontline clinical perspective with Python, SQL, and biostatistics, let’s connect."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Get in touch"
    url: "contact/"
---

{% include splash.html%}

{% for section in page.sections %}
  <section class="section milestones-cards-section">
    <div class="container">
      <!-- Section Header -->
      {% if section.heading %}
        <div class="has-text-centered mb-5">
          <h2 class="title is-3 mb-4 milestones-heading">{{ section.heading }}</h2>
          {% if section.description %}
            <p class="subtitle is-5">{{ section.description }}</p>
          {% endif %}
        </div>
      {% endif %}
      <!-- Cards Grid -->
      <div class="columns is-multiline is-desktop">
        {% for card in section.cards %}
          {% include milestones-cards.html card=card %}
        {% endfor %}
      </div>
    </div>
  </section>
{% endfor %}

{% include cta.html %}