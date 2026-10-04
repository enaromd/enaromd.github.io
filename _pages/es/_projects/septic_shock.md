---
layout: page
title: "Evidencia en Choque Séptico"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/septic-shock/
lang: es

page_components:
  - type: "header"
    title: "Sepsis: De la evidencia en ensayos hacia flujos de trabajo clínicos"
  
    bottom_line:
      label: "Conclusión Clave"
      text: "Conclusión Clave: La mejor evidencia científica es inútil si no puede ser adoptada en la primera línea. Esta síntesis tradujo rápidamente <span class='highlight-metric'>razones complejas</span> de los ensayos ANDROMEDA-SHOCK y CLOVERS <span class='highlight-metric'>en acuerdos operacionales inmediatos y estandarizados.</span>"

    tech_stack:
      label: "Estrategias Clave"
      items:
        - "Medicina Basada en Evidencia"
        - "Síntesis de Ensayos"
        - "Alineación de Flujos de Trabajo"

  - type: "section"
    title: "El Desafío: Brechas entre los Últimos Ensayos y la Práctica Clínica al Pie de la Cama"
    content: "En el entorno de alta presión de los cuidados intensivos, <strong>la brecha entre la publicación de un ensayo clave y la implementación de su flujo de trabajo puede costar vidas.</strong> Mi objetivo fue comprimir efectivamente este cronograma sintetizando los puntos de datos precisos necesarios para una adopción inmediata en el flujo de trabajo clínico."

  - type: "skills"
    skills_heading: "Traducción de Evidencia para Flujos de Trabajo Clínicos"
    skills_description: "Descomposición de datos de ensayos hito en cuidados intensivos para mapear gatillos clínicos accionables y de alta visibilidad."
    skills:
      - title: Curaduría de Ensayos Hito
        icon: "assets/images/icons/selection.png"
        one: "Sinteticé el diseño y los resultados de ensayos clínicos aleatorizados, extrayendo los desenlaces clínicos más importantes para su implementación al pie de la cama."

      - title: Alineación Operativa
        icon: "assets/images/icons/analysis.png"
        one: "Logré una rápida alineación clínica involucrando a los actores clave mediante jerarquías visuales claras e impulsadas por la evidencia que redujeron la carga cognitiva."

      - title: Restricciones por Comorbilidad
        icon: "assets/images/icons/effects.png"
        one: "Tomé en cuenta las restricciones fisiopatológicas superpuestas, aislando puntos de inflexión donde la titulación de fluidos debe pivotar para evitar la sobrecarga de volumen."

  - type: "figure"
    heading: "Operativización de la Evidencia de Ensayos Clínicos"
    description: "Contrastando la metodología de los ensayos con el contexto médico local para extraer hitos de decisión de alto rendimiento."
    image: "/assets/images/sepsis_evidence.jpg"
    alt: "Tabla de recomendación basada en la Campaña Sobrevivir a la Sepsis."
    caption: "Tabla 1: Tabla de recomendación basada en la Campaña Sobrevivir a la Sepsis para estandarizar el manejo dentro de la primera hora."

  - type: "results"
    cards:
      - title: "Alineación Estratificada"
        description_1: "<span class='highlight-metric'>Traducción de desenlaces de múltiples ensayos en señales clínicas</span>, conectando la fisiología fundamental para internos y la metodología avanzada de ensayos para subespecialistas durante una revisión institucional conjunta."

      - title: "Guías Clínicas de MBE"
        description_1: "<span class='highlight-metric'>Flujos de trabajo al pie de la cama específicos para el contexto</span> e impulsados por evidencia para la reanimación con fluidos guiada por llenado capilar y lactato, inicio temprano de vasopresores y uso estratégico de corticosteroides."

      - title: "El Valor del Analista"
        description_1: "Minimización de la varianza clínica y la latencia de implementación mediante la <span class='highlight-metric'>destilación de datos de ensayos de alta dimensión en marcos estructurados al pie de la cama</span> para una ejecución rápida y estandarizada."

  - type: "quote"
    text: "La generación de evidencia es solo la mitad de la batalla. El despliegue estratégico en los flujos de trabajo clínicos es lo que en última instancia salva vidas."

  - type: "gallery"
    heading: "Evidencia Visual"
    description: "Una síntesis de evidencia clínica para la estandarización del manejo de la Sepsis."
    items:
      - image: "/assets/images/sepsis_01.jpg"
        alt: "Resumen del Ensayo ANDROMEDA-SHOCK"
        caption: "Efecto de una Estrategia de Reanimación Guiada por el Estado de Perfusión Periférica vs. Niveles de Lactato Sérico."

      - image: "/assets/images/sepsis_02.jpg"
        alt: "Tabla de Resultados de ANDROMEDA-SHOCK"
        caption: "Resultados: Análisis de Hazard Ratios que respaldan la seguridad y eficacia de la reanimación guiada por perfusión periférica."

      - image: "/assets/images/sepsis_03.jpg"
        alt: "Cristaloides Balanceados vs. Solución Salina"
        caption: "Evaluación en el Ensayo SALT-ED de los resultados de cristaloides vs. solución salina en pacientes no críticos en urgencias."

      - image: "/assets/images/sepsis_04.jpg"
        alt: "Concentración de Electrólitos Séricos"
        caption: "Tendencias de concentración media de electrólitos séricos durante las primeras 72 horas de reanimación."

      - image: "/assets/images/sepsis_05.jpg"
        alt: "Heterogeneidad del Efecto del Tratamiento"
        caption: "Análisis de subgrupos y forest plot que demuestra los Odds Ratios para lesión renal aguda."

cta:
  heading: "Conecte la Realidad Clínica de Primera Línea con la Ejecución Técnica"
  description: "La analítica de salud efectiva comienza entendiendo cómo nacen los datos al pie de la cama del paciente, incluyendo los flujos de trabajo ajetreados y los factores humanos que distorsionan los registros crudos. Si su equipo necesita a alguien que combine la perspectiva clínica de primera línea con Python, SQL y bioestadística, conectemos."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Ponerse en contacto"
    url: "contact/"
---

<style>
.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}

.skill-cards-section {
  margin-top: 1rem;
}
</style>

{% for component in page.page_components %}
  {% if component.type == "section" %}
    {% include project-section.html data=component %}
  {% elsif component.type == "header" %}
    {% include project-header.html data=component %}
  {% elsif component.type == "button" %}
    {% include project-button.html data=component %}
  {% elsif component.type == "skills" %}
    {% include skill-cards.html data=component %}
  {% elsif component.type == "reflections" %}
    {% include project-reflection-cards.html data=component %}
  {% elsif component.type == "figure" %}
    {% include project-chart.html data=component %}
  {% elsif component.type == "results" %}
    {% include project-results.html data=component %}
  {% elsif component.type == "showcase" %}
    {% include project-chart-impact.html data=component %}
  {% elsif component.type == "quote" %}
    {% include project-quote.html data=component %}
  {% elsif component.type == "flexible_content" %}
    {% include project-flexible-content.html data=component %}
  {% elsif component.type == "gallery" %}
    {% include project-gallery.html data=component %}
  {% endif %}
{% endfor %}

{% include cta.html %}