---
layout: page
title: "Enyel Rodríguez"
logo: "/assets/images/logo.png" 
hide_hero: false
permalink: vcard/
lang: es

hero:
  bg_image: "/assets/images/hero-bg.png"
  title: "Más allá del estetoscopio:<br>Evidencia con Datos del Mundo Real"
  description: "Soy Enyel Rodríguez, Médico y Analista de Datos. Cierro la brecha crítica entre los flujos de trabajo clínicos de primera línea y la bioestadística rigurosa, construyendo índices clínicos validados en tuberías de Datos del Mundo Real para obtener resultados basados en evidencia."

  primary_cta:
    text: "WhatsApp"
    url: "contact/"
    icon: "fa-solid fa-mobile-screen"
  secondary_cta:
    text: "Ver proyectos"
    url: "projects/"
    icon: "fa-solid fa-folder-open" 
  
  image: "/assets/images/hero_squared.png"
  image_alt: "Dr. Enyel Rodríguez"

  languages:
    - flag_svg: "/assets/images/flags/en.svg"
      text: "EN (C2)"
    - flag_svg: "/assets/images/flags/es.svg"
      text: "ES (Nativo)"

  badges_heading: "INSIGNIAS DE CERTIFICACIÓN"
  badges:
    - image: "/assets/images/badge-meta-database-engineer.png"
      url: "https://www.credly.com/badges/b87a61e6-0b8d-41ff-b8a5-f52833fca99f"
      alt: "Meta Database Engineer Certificate"
      tooltip: "Verificar certificación de Meta"
    - image: "/assets/images/badge-google-analytics.png"
      url: "https://www.credly.com/badges/5d5f46ce-cd86-4966-9dc2-115d5568d9b1"
      alt: "Google Data Analytics Certificate"
      tooltip: "Verificar certificación de Google"

see_more_milestones:
  text: "Ver todas las certificaciones"
  url: "certifications/"

sections:
  - heading: "Certificaciones destacadas"
    description: "Credenciales que conectan la medicina clínica con la ingeniería cuantitativa, abarcando inferencia estadística, creación de tuberías ETL y evaluación de ensayos clínicos."

    cards:
      - title: "Biostatistics in Public Health"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_biostatistics.jpg"
        description: "Inferencia estadística, métodos de regresión y análisis de supervivencia."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/ZRXSQLDMFXPR"
      - title: "Statistics with Python"
        issuer: "University of Michigan"
        image: "/assets/images/certification_statistics-python.jpg"
        description: "Modelos multinivel, pesos de muestreo y ajuste de regresión logística/lineal."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/PJX2HNZZYYJD"
      - title: "Introduction to Systematic Review and Meta-Analysis"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_meta-analysis.jpg"
        description: "Revisiones sistemáticas, meta-análisis y evaluación de sesgos."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/PR8EM6PJTQ9F"

highlighted_projects_heading: "Proyectos destacados"
highlighted_projects_description: "Transformando registros de expedientes clínicos electrónicos y encuestas nacionales de salud en flujos de trabajo clínicos accionables."
see_more_projects:
  text: "Ver todos los proyectos"
  url: "projects/" 

highlighted_projects:
  - title: Intensidad farmacológica y enfermedad cardíaca valvular
    image: "/assets/images/cover_project_mbi.png"
    description: "Clasifica el 25.7% de los pacientes de alta agudeza en zonas de intervención de alto beneficio bajo severas restricciones de campo."
    details_url: "/projects/mbi/"
    github_url: "https://github.com/enaromd/Cardio-MBI-Triage-Engine"
  - title: Obesidad clínica y NHANES 2021-2023
    image: "/assets/images/cover_project_nhanes-obesity.png"
    description: "Revela un incremento del riesgo de 3.6x en adultos con IMC normal pero con obesidad periférica no detectada en tamizajes estándar."
    details_url: "/projects/mbi/"
    github_url: "https://github.com/enaromd/clinical-obesity"
  - title: Disfunción diastólica en hemodiálisis de mantenimiento
    image: "/assets/images/cover_project_lvdd.png"
    description: "Identifica la hipertensión crónica (RP: 2.22) como el principal factor impulsor de la insuficiencia cardíaca en hemodiálisis."
    details_url: "/projects/mbi/"

connect:
    title: "Conéctate conmigo"
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