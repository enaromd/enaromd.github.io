---
layout: page
title: "Enyel Rodríguez"
logo: "/assets/images/logo.png" 
hide_hero: false
permalink: vcard/
lang: en

hero:
  bg_image: "/assets/images/hero-bg.png"
  title: "Beyond the stethoscope:<br>Evidence with Real-World Data"
  description: "I am Enyel Rodríguez, MD and Data Analyst. I bridge the critical gap between front-line clinical workflows and rigorous biostatistics, engineering validated clinical indices into Real-World Data pipelines for evidence-based outcomes."

  primary_cta:
    text: "WhatsApp"
    url: "contact/"
    icon: "fa-solid fa-mobile-screen"
  secondary_cta:
    text: "View Projects"
    url: "projects/"
    icon: "fa-solid fa-folder-open" 
  
  image: "/assets/images/hero_squared.png"
  image_alt: "Dr. Enyel Rodríguez"

  languages:
    - flag_svg: "/assets/images/flags/en.svg"
      text: "EN (C2)"
    - flag_svg: "/assets/images/flags/es.svg"
      text: "ES (Native)"

  badges_heading: "CERTIFICATION BADGES"
  badges:
    - image: "/assets/images/badge-meta-database-engineer.png"
      url: "https://www.credly.com/badges/b87a61e6-0b8d-41ff-b8a5-f52833fca99f"
      alt: "Meta Database Engineer Certificate"
      tooltip: "Verify Meta Certification"
    - image: "/assets/images/badge-google-analytics.png"
      url: "https://www.credly.com/badges/5d5f46ce-cd86-4966-9dc2-115d5568d9b1"
      alt: "Google Data Analytics Certificate"
      tooltip: "Verify Google Certification"

see_more_milestones:
  text: "See all certifications"
  url: "certifications/"

sections:
  - heading: "Featured Certifications"
    description: "Credentials bridging clinical medicine with quantitative engineering—spanning statistical inference, ETL pipeline creation, and clinical trial evaluation."

    cards:
      - title: "Biostatistics in Public Health"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_biostatistics.jpg"
        description: "Statistical inference, regression methods, and survival analysis."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/ZRXSQLDMFXPR"
      - title: "Statistics with Python"
        issuer: "University of Michigan"
        image: "/assets/images/certification_statistics-python.jpg"
        description: "Multilevel models, sampling weights, and logistic/linear regression adjustment."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/PJX2HNZZYYJD"
      - title: "Introduction to Systematic Review and Meta-Analysis"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_meta-analysis.jpg"
        description: "Systematic reviews, meta-analysis, and bias assessment."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/PR8EM6PJTQ9F"

highlighted_projects_heading: "Featured projects"
highlighted_projects_description: "Transforming raw EHR records and national health surveys into actionable clinical workflows."
see_more_projects:
  text: "See all projects"
  url: "projects/" 

highlighted_projects:
  - title: Medication intensity and Valvular Heart Disease
    image: "/assets/images/cover_project_mbi.png"
    description: "Classifies 25.7% of high-acuity patients into high-benefit intervention zones under severe field constraints."
    details_url: "/projects/mbi/"
    github_url: "https://github.com/enaromd/Cardio-MBI-Triage-Engine"
  - title: Clinical Obesity and NHANES 2021-2023
    image: "/assets/images/cover_project_nhanes-obesity.png"
    description: "Uncovers a 3.6x risk surge in normal-BMI adults with peripheral obesity missed by standard screening."
    details_url: "/projects/mbi/"
    github_url: "https://github.com/enaromd/clinical-obesity"
  - title: Diastolic Dysfunction in Maintenance Hemodialysis
    image: "/assets/images/cover_project_lvdd.png"
    description: "Identifies chronic Hypertension (PR: 2.22) as the strongest driver of heart failure in hemodialysis."
    details_url: "/projects/mbi/"

connect:
    title: "Connect with Me"
    links:
      - name: "LinkedIn"
        handle: "Enyel Rodríguez"
        url: "https://www.linkedin.com/in/enaromd/"
        icon: "fab fa-linkedin"

      - name: "GitHub"
        handle: "enaromd"
        url: "https://github.com/enaromd"
        icon: "fab fa-github"

      - name: "Threads"
        handle: "enaromd"
        url: "https://threads.net/@enaromd"
        icon: "fab fa-threads"

      - name: "X"
        handle: "enaromd"
        url: "https://x.com/enaromd"
        icon: "fab fa-x-twitter"
---

<style>
.about-hero-style {
    margin-top: 1rem;
    margin-bottom: 1rem;
}

.milestones-cards-section {
    padding: 6rem 1.5rem;
}

.highlighted-projects-cards-section {
    margin-top: 5rem !important;
}

@media screen and (max-width: 640px) {
    .hero {
        padding-top: 6rem;
    }

    .highlighted-projects-cards-section {
        margin-bottom: 1rem !important;
    }
}
</style>

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
      <!-- See More Certifications Action -->
      {% if page.see_more_milestones %}
        <div class="has-text-centered">
          <a href="{{ page.see_more_milestones.url | relative_url }}" class="see-more-milestones-link">
            <span>{{ page.see_more_milestones.text | default: "See all certifications" }}</span>
            <span class="icon is-small">
              <i class="fa-solid fa-arrow-right"></i>
            </span>
          </a>
        </div>
      {% endif %}
    </div>
  </section>
{% endfor %}

{% include highlighted-projects-cards.html %}

{% include social.html %}