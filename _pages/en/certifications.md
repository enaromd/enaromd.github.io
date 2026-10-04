---
layout: page
title: "Certifications"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: certifications/
lang: en

splash_title: "Certifications"
splash_text: "Continuous professional development is fundamental to maintaining analytical rigor. \n\nHere is an overview of completed coursework and specializations across biostatistics, database optimization, and healthcare analytics."
splash_image: "/assets/images/splash-certifications.jpg"

sections:
  - heading: "Data Foundations"
    description: "Core competencies in extracting, modeling, and visualizing complex datasets without losing clinical context or structural integrity."

    cards:
      - title: "Google Data Analytics"
        issuer: "Google"
        image: "/assets/images/certification_data_analytics.png"
        description: "Data cleaning, Tableau visualization, and Python-driven exploratory analysis."
        credentials_url: "https://www.coursera.org/account/accomplishments/professional-cert/6WYNGZ2YUTNB"
      - title: "Meta Database Engineer"
        issuer: "Meta"
        image: "/assets/images/certification_database_engineer.jpg"
        description: "Relational schema design, advanced MySQL optimization, and ETL pipeline development."
        credentials_url: "https://www.coursera.org/account/accomplishments/professional-cert/TE1VSZSPDZ56"
      - title: "Statistics with Python"
        issuer: "University of Michigan"
        image: "/assets/images/certification_statistics-python.jpg"
        description: "Multilevel models, sampling weights, and logistic/linear regression adjustment."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/PJX2HNZZYYJD"
      - title: "Everyday Excel"
        issuer: "University of Colorado Boulder"
        image: "/assets/images/certification_excel.jpg"
        description: "Advanced logical functions, data validation, and pivot tables."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/SJXAGC3NQHCC"

  - heading: "Research and Public Health"
    description: "Methodological frameworks for evaluating observational cohorts, synthesizing clinical literature, and modeling population-level outcomes."

    cards:
      - title: "Biostatistics in Public Health"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_biostatistics.jpg"
        description: "Statistical inference, regression methods, and survival analysis."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/ZRXSQLDMFXPR"
      - title: "Introduction to Systematic Review and Meta-Analysis"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_meta-analysis.jpg"
        description: "Systematic reviews, meta-analysis, and bias assessment."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/PR8EM6PJTQ9F"
      - title: "Healthcare Management and Finance"
        issuer: "University of Michigan"
        image: "/assets/images/certification_healthcare-management.png"
        description: "Strategic planning and cost analysis for healthcare organizations."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/JAOGI855KZXS"

  - heading: "Strategic communication"
    description: "Translating complex clinical and statistical insights into structured visual slide architectures, persuasive narratives, and executive presentations."

    cards:
      - title: "Good with Words: Speaking and Presenting"
        issuer: "University of Michigan"
        image: "/assets/images/certification_speaking-presenting.jpg"
        description: "High-impact message architecture and delivery techniques for public speaking."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/GEANNPWG96DG"
      - title: "Presentation Skills: Designing Slides"
        issuer: "National Research Tomsk State University"
        image: "/assets/images/certification_slide-design.jpg"
        description: "Visual hierarchy and slide architecture for expert audiences."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/JWZG97JHLWCX"
      - title: "Presentation Skills: Speech Writing and Storytelling"
        issuer: "National Research Tomsk State University"
        image: "/assets/images/certification_storytelling.jpg"
        description: "Drafting persuasive narratives and impactful story architecture."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/24WLKLMUS3A7"
      - title: "First Place - XV Scientific Conference"
        issuer: "SILAIS Granada"
        image: "/assets/images/award_scientific-fair.jpg"
        description: "Drafting persuasive narratives and impactful story architecture."
        credentials_url: "https://drive.google.com/file/d/1nib_fIRz1-YxlaEv80VYZgGtqg_XQotb/view"
      - title: "C2 English Level"
        issuer: "EF Standard English Test"
        image: "/assets/images/efset_c2.jpg"
        description: "Advanced synthesis capability and fluent communication in complex environments."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/MV8WGWJ9SBPRs"

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