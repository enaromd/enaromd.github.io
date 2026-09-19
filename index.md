---
layout: page
title: "Enyel Rodríguez"
hide_hero: true

hero:
  bg_image: "/assets/images/hero-bg.png"
  title: "Beyond the stethoscope:<br>Evidence with data"
  description: "I am Enyel Rodríguez, MD and Clinical Data Analyst. I bridge the critical gap between front-line clinical workflows and rigorous biostatistics, engineering validated clinical indices into Real-World Data pipelines for evidence-based outcomes."

  primary_cta:
    text: "Get in touch"
    url: "#contact"
  secondary_cta:
    text: "View Projects"
    url: "#projects"
  
  image: "/assets/images/hero_squared.png"
  image_alt: "Dr. Enyel Rodríguez"

  languages:
    - flag_svg: "/assets/images/flags/us.svg"
      text: "EN (C2)"
    - flag_svg: "/assets/images/flags/es.svg"
      text: "ES (Native)"

  badges_heading: "CERTIFICATION BADGES"
  badges:
    - image: "/assets/images/badge-meta-database-engineer.png"
      url: "https://www.credly.com/badges/b87a61e6-0b8d-41ff-b8a5-f52833fca99f"
      alt: "Meta Database Engineer Certificate"
    - image: "/assets/images/badge-google-analytics.png"
      url: "https://www.credly.com/badges/5d5f46ce-cd86-4966-9dc2-115d5568d9b1"
      alt: "Google Data Analytics Certificate"

skills_heading: "Core Competencies"
skills_description: "Bridging clinical medicine with biostatistics and data engineering to build actionable health insights."
skills:
  - title: Clinical Domain Knowledge
    icon: "fa-solid fa-stethoscope"
    one: "<b>Clinical Knowledge & Strategy:</b> Internal Medicine, Cardiorenal & Metabolic Pathology."
    two: "<b>Evidence Synthesis:</b> Systematic reviews, meta-analysis, and systematic bias assessment."
    three: "<b>Scientific Communication:</b> High-impact message structure and expert presentation design."
  - title: Database Engineering
    icon: "fa-solid fa-database"
    one: "<b>Relational Database Design:</b> 3NF & Snowflake schema and MySQL optimization."
    two: "<b>SQL Development:</b> Advanced joins, subqueries, aggregations, and stored procedures."
    three: "<b>ETL & Data Quality Control (DQC):</b> Building data validation pipelines and audit trails."
  - title: Biostatistics and Visual Insights
    icon: "fa-solid fa-chart-column"
    one: "<b>Python Analytical Stack:</b> Pandas, NumPy, SciPy, Statsmodels, and Seaborn."
    two: "<b>Interactive BI Dashboards:</b> Executive and operational data storytelling in Tableau."
    three: "<b>Survey-Weighted Modeling:</b> Complex sampling adjustments, GEE Poisson models, and sandwich estimators."

highlighted_projects_heading: "Featured Projects"
highlighted_projects_description: "My projects are a testament to my dedication to achieving high-impact results."
highlighted_projects:
  - title: Medication intensity and Valvular Heart Disease
    image: "/assets/images/cover_project_mbi.png"
    description: "Classifies 25.7% of high-acuity patients into high-benefit intervention zones under severe field constraints."
    details_url: "/projects/mbi/"
    github_url: "https://github.com/username/project-mbi"
  - title: Clinical Obesity and NHANES 2021-2023
    image: "/assets/images/cover_project_nhanes-obesity.png"
    description: "Uncovers a 3.6x risk surge in normal-BMI adults with peripheral obesity missed by standard screening."
    details_url: "/projects/mbi/"
    github_url: "https://github.com/username/project-mbi"
  - title: Diastolic Dysfunction in Maintenance Hemodialysis
    image: "/assets/images/cover_project_lvdd.png"
    description: "Identifies chronic Hypertension (PR: 2.22) as the strongest driver of heart failure in hemodialysis."
    details_url: "/projects/mbi/"
    github_url: "https://github.com/username/project-mbi"

sections:
  - heading: "Certifications"
    description: "My certifications are not just credentials; they are proof of an unwavering commitment to excellence. From statistical analysis to effective communication, each skill is a key piece in ensuring our projects are technically sound, well-communicated, and high-impact."
    cards:
      - title: "Google Data Analytics"
        issuer: "Google"
        image: "/assets/images/certification_data_analytics.png"
        description: "Data cleaning, Tableau visualization, and Python-driven exploratory analysis."
        details_url: "/credentials/google-data-analytics/"
      - title: "Google Data Analytics"
        issuer: "Google"
        image: "/assets/images/certification_data_analytics.png"
        description: "Data cleaning, Tableau visualization, and Python-driven exploratory analysis."
        details_url: "/credentials/google-data-analytics/"
      - title: "Google Data Analytics"
        issuer: "Google"
        image: "/assets/images/certification_data_analytics.png"
        description: "Data cleaning, Tableau visualization, and Python-driven exploratory analysis."
        details_url: "/credentials/google-data-analytics/"
---

{% include hero.html %}

{% include skill-cards.html %}

{% include highlighted-projects-cards.html %}

{% for section in page.sections %}
  <section class="section milestones-cards-section">
    <div class="container">
      <!-- Section Header -->
      {% if section.heading %}
        <div class="has-text-centered mb-6">
          <h2 class="title is-2 mb-4 milestones-heading">{{ section.heading }}</h2>
          {% if section.description %}
            <p class="subtitle is-5">{{ section.description }}</p>
          {% endif %}
        </div>
      {% endif %}
      <!-- Cards Grid -->
      <div class="columns is-multiline is-desktop">
        {% for card in section.cards %}
          {% include credentials-cards.html card=card %}
        {% endfor %}
      </div>
    </div>
  </section>
{% endfor %}