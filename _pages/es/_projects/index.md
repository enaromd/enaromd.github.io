---
layout: page
title: "Proyectos"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/
lang: es

splash_title: "Proyectos"
splash_text: "La analítica efectiva en salud requiere comprender tanto al paciente junto a la cama como al algoritmo en la tubería de datos. \n\nAquí encontrarás proyectos de investigación aplicada que van desde la estratificación del riesgo cardiometabólico en encuestas nacionales hasta índices de triage personalizados para misiones médicas humanitarias."
splash_image: "/assets/images/splash-projects.jpg"

sections:
  - heading: "Estructuras de bases de datos y pipelines analíticas"
    description: "Diseño de esquemas relacionales en Tercera Forma Normal (3NF) y Copo de Nieve (Snowflake), procedimientos almacenados y scripts automatizados en Python para limpiar, procesar y analizar conjuntos de datos clínicos sin comprometer el contexto diagnóstico."

    cards:
      - title: Intensidad farmacológica y enfermedad cardíaca valvular
        image: "/assets/images/cover_project_mbi.png"
        description: "Clasifica el 25.7% de los pacientes de alta agudeza en zonas de intervención de alto beneficio bajo severas restricciones de campo."
        details_url: "/projects/mbi/"
        github_url: "https://github.com/enaromd/Cardio-MBI-Triage-Engine/blob/main/README.es.md"
      - title: Obesidad clínica y NHANES 2021-2023
        image: "/assets/images/cover_project_nhanes-obesity.png"
        description: "Revela un incremento del riesgo de 3.6x en adultos con IMC normal pero con obesidad periférica no detectada en tamizajes estándar."
        details_url: "nhanes_obesity/"
        github_url: "https://github.com/enaromd/clinical-obesity/blob/main/README.es.md"
      - title: Base de datos relacional e integración MySQL-Python
        image: "/assets/images/cover_project_database.png"
        description: "100% de integridad transaccional y eliminación de redundancia de datos mediante procedimientos almacenados."
        details_url: "little-lemon/"
        github_url: "https://github.com/enaromd/db-capstone-project"

  - heading: "Síntesis de evidencia y mentoría metodológica"
    description: "Guiando a equipos clínicos a través de la evaluación sistemática de sesgos, interpretación de ensayos clínicos y adaptación local de flujos de trabajo para asegurar la estandarización basada en evidencia en la atención médica aguda."

    cards:
      - title: Disfunción diastólica en hemodiálisis de mantenimiento
        image: "/assets/images/cover_project_lvdd.png"
        description: "Identifica la hipertensión crónica (RP: 2.22) como el principal factor impulsor de la insuficiencia cardíaca en hemodiálisis."
        details_url: "lvdd/"
      - title: Operacionalización de la evidencia clínica en choque séptico
        image: "/assets/images/cover_project_presention_sepsis.png"
        description: "Reducción de la variabilidad clínica mediante marcos de consenso estandarizados e impulsados por datos en cuidados intensivos."
        details_url: "septic-shock/"
      - title: "Estrategia visual galardonada: Farmacovigilancia"
        image: "/assets/images/cover_project_presention_pharmacovigilance.png"
        description: "Primer Lugar en la XV Jornada Científica por transformar el reporte clínico tradicional."
        details_url: "pharmacovigilance/"

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