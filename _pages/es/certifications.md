---
layout: page
title: "Certificaciones"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: certifications/
lang: es

splash_title: "Certificaciones"
splash_text: "El desarrollo profesional continuo es fundamental para mantener el rigor analítico. \n\nAquí se presenta una visión general de los cursos y especializaciones completados en bioestadística, optimización de bases de datos y analítica en salud."
splash_image: "/assets/images/splash-certifications.jpg"

sections:
  - heading: "Fundamentos de Datos"
    description: "Competencias clave en la extracción, modelado y visualización de conjuntos de datos complejos sin perder el contexto clínico ni la integridad estructural."

    cards:
      - title: "Google Data Analytics"
        issuer: "Google"
        image: "/assets/images/certification_data_analytics.png"
        description: "Limpieza de datos, visualización en Tableau y análisis exploratorio impulsado por Python."
        credentials_url: "https://www.coursera.org/account/accomplishments/professional-cert/6WYNGZ2YUTNB"
      - title: "Meta Database Engineer"
        issuer: "Meta"
        image: "/assets/images/certification_database_engineer.jpg"
        description: "Diseño de esquemas relacionales, optimización avanzada en MySQL y desarrollo de ETL pipelines."
        credentials_url: "https://www.coursera.org/account/accomplishments/professional-cert/TE1VSZSPDZ56"
      - title: "Statistics with Python"
        issuer: "University of Michigan"
        image: "/assets/images/certification_statistics-python.jpg"
        description: "Modelos multinivel, pesos de muestreo y ajuste de regresión logística y lineal."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/PJX2HNZZYYJD"
      - title: "Everyday Excel"
        issuer: "University of Colorado Boulder"
        image: "/assets/images/certification_excel.jpg"
        description: "Funciones lógicas avanzadas, validación de datos y tablas dinámicas."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/SJXAGC3NQHCC"

  - heading: "Investigación y Salud Pública"
    description: "Marcos metodológicos para evaluar cohortes observacionales, sintetizar literatura clínica y modelar resultados a nivel poblacional."

    cards:
      - title: "Biostatistics in Public Health"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_biostatistics.jpg"
        description: "Inferencia estadística, métodos de regresión y análisis de supervivencia."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/ZRXSQLDMFXPR"
      - title: "Introduction to Systematic Review and Meta-Analysis"
        issuer: "Johns Hopkins University"
        image: "/assets/images/certification_meta-analysis.jpg"
        description: "Revisiones sistemáticas, meta-análisis y evaluación de sesgos."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/PR8EM6PJTQ9F"
      - title: "Healthcare Management and Finance"
        issuer: "University of Michigan"
        image: "/assets/images/certification_healthcare-management.png"
        description: "Planificación estratégica y análisis de costos para organizaciones de salud."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/JAOGI855KZXS"

  - heading: "Comunicación Estratégica"
    description: "Traducción de hallazgos clínicos y estadísticos complejos en arquitecturas visuales de diapositivas, narrativas persuasivas y presentaciones ejecutivas."

    cards:
      - title: "Good with Words: Speaking and Presenting"
        issuer: "University of Michigan"
        image: "/assets/images/certification_speaking-presenting.jpg"
        description: "Estructura de mensajes de alto impacto y técnicas de oratoria para hablar en público."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/GEANNPWG96DG"
      - title: "Presentation Skills: Designing Slides"
        issuer: "National Research Tomsk State University"
        image: "/assets/images/certification_slide-design.jpg"
        description: "Jerarquía visual y arquitectura de diapositivas para audiencias especializadas."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/JWZG97JHLWCX"
      - title: "Presentation Skills: Speech Writing and Storytelling"
        issuer: "National Research Tomsk State University"
        image: "/assets/images/certification_storytelling.jpg"
        description: "Redacción de narrativas persuasivas y estructura narrativa de alto impacto."
        credentials_url: "https://www.coursera.org/account/accomplishments/verify/24WLKLMUS3A7"
      - title: "Primer Lugar - XV Jornada Científica"
        issuer: "SILAIS Granada"
        image: "/assets/images/award_scientific-fair.jpg"
        description: "Redacción de narrativas persuasivas y estructura narrativa de alto impacto."
        credentials_url: "https://drive.google.com/file/d/1nib_fIRz1-YxlaEv80VYZgGtqg_XQotb/view"
      - title: "Nivel de Inglés C2"
        issuer: "EF Standard English Test"
        image: "/assets/images/efset_c2.jpg"
        description: "Capacidad avanzada de síntesis y comunicación fluida en entornos complejos."
        credentials_url: "https://www.coursera.org/account/accomplishments/specialization/MV8WGWJ9SBPRs"

cta:
  heading: "Conecta la realidad clínica de primera línea con la ejecución técnica"
  description: "La analítica efectiva en salud comienza por comprender cómo nacen los datos junto a la cama del paciente, incluyendo los caóticos flujos de trabajo y factores humanos que distorsionan los registros. Si tu equipo necesita a alguien que combine la perspectiva clínica con Python, SQL y bioestadística, pongámonos en contacto."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Contáctame"
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