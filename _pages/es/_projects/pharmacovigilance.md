---
layout: page
title: "Farmacovigilancia en Hipertensión"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/pharmacovigilance/
lang: es

page_components:
  - type: "header"
    title: "La Economía de la Elección: Visualizando la Falla Terapéutica"
  
    bottom_line:
      label: "Conclusión Clave"
      text: "Conclusión Clave: En la XV Jornada Científica, 17 presentaciones clínicas mostraron datos estáticos. Este proyecto tomó un camino diferente. Fusionando algoritmos estrictos de causalidad de la OMS con reencuadre conductual del riesgo, expusimos cómo las llamadas <span class='highlight-metric'>reacciones secundarias 'leves'</span> impulsan en secreto una <span class='highlight-metric'>tasa de abandono del tratamiento del 50%.</span>"

    tech_stack:
      label: "Estrategias Clave"
      items:
        - " Causalidad Algorítmica"
        - "Storytelling Persuasivo"
        - "Jerarquía Visual"

  - type: "section"
    title: 'El Desafío: La Trampa Cognitiva de los Datos "Leves"'
    content: 'En farmacovigilancia, los datos a menudo se ignoran si carecen de una severidad catastrófica. Nuestro análisis de registro reveló que el <strong>57.1% de las reacciones adversas a medicamentos se clasificaron como "leves"</strong>. Para los clínicos de primera línea, esto desencadena una heurística cognitiva: leve significa inofensivo. Sin embargo, esta misma fricción "inofensiva" es <strong>responsable de una tasa de abandono terapéutico del 50%</strong> en pacientes hipertensos crónicos. El objetivo fue estructurar una presentación que rompiera este sesgo cognitivo.'

  - type: "skills"
    skills_heading: "De los Datos a la Estandarización Algorítmica"
    skills_description: "Aplicación del Algoritmo de Causalidad de la OMS para validar señales, evitando que los datos sean descartados como ruido clínico."
    skills:
      - title: Estandarización de Términos
        icon: "assets/images/icons/data_management.png"
        one: "Mapeo de problemas médicos activos mediante el índice CIE-10 y categorización de todos los medicamentos consumidos según el marco Anatómico, Terapéutico y Químico (ATC)."

      - title: Causalidad Algorítmica
        icon: "assets/images/icons/selection.png"
        one: "Procesamiento de datos sintomáticos crudos a través del Algoritmo de Evaluación de Causalidad de la OMS para verificar objetivamente la relación entre la exposición al fármaco y los eventos adversos."

      - title: Clasificación del Riesgo de Reacciones
        icon: "assets/images/icons/risk.png"
        one: "Aplicación del sistema de clasificación modificado de Rawlins y Thompson para diferenciar entre reacciones predecibles dependientes de la dosis y anomalías impredecibles."

  - type: "figure"
    heading: "El Factor Victoria: Destacar"
    description: "En un campo concurrido de 17 presentaciones científicas, esta jerarquía visual centrada en el comportamiento sacó a la luz que las reacciones adversas aparentemente menores desencadenan directamente el abandono terapéutico masivo."
    image: "/assets/images/cover_project_presention_pharmacovigilance.png"
    alt: "Gatillo Estratégico"
    caption: "Figura 1: Diseño orientado a destacar el vínculo directo entre las reacciones adversas a medicamentos (RAM) y la falla terapéutica en la farmacovigilancia activa."

  - type: "results"
    cards:
      - title: "El Umbral de Abandono"
        description_1: "Identificación de que el <span class='highlight-metric'>50% de los pacientes</span> que presentaron una reacción adversa a medicamentos antihipertensivos suspendieron por completo su consumo."

      - title: 'La Paradoja de lo "Leve"'
        description_1: "Descubrimiento de que el <span class='highlight-metric'>71.4% de las reacciones documentadas fueron Tipo A</span> según Rawlins y Thompson, demostrando que la gran mayoría de las fallas terapéuticas eran esperables y prevenibles."

      - title: "Alineación Estratificada"
        description_1: 'Verificación de una <span class="highlight-metric">tasa de causalidad "Posible" del 95.2%</span>, destacando que el <span class="highlight-metric">57.1% de las reacciones fueron clínicamente "Leves"</span>, aunque lo suficientemente disruptivas como para arruinar la adherencia al tratamiento.'

  - type: "quote"
    text: "No solo presento datos; los estructuro para asegurar que la evidencia supere las heurísticas conductuales establecidas."

  - type: "gallery"
    heading: "Evidencia Visual"
    description: "Una inmersión en la estrategia de comunicación que obtuvo el Primer Lugar en la XV Jornada Científica."
    items:
      - image: "/assets/images/xv-jornada-01.jpg"
        alt: "Resaltado de datos sobre hipertensión"
        caption: "Urgencia Clínica: Jerarquía visual diseñada para transformar cifras frías en un llamado a la acción con respecto a la alta morbimortalidad cardiovascular."

      - image: "/assets/images/xv-jornada-02.jpg"
        alt: "Desglose metodológico"
        caption: "Iconografía minimalista utilizada para guiar al jurado a través de las fases de identificación, prevalencia y severidad de las RAM."

      - image: "/assets/images/xv-jornada-03.jpg"
        alt: "Descripción de características demográficas"
        caption: "Segmentación demográfica que permite comprender el entorno socioeconómico donde se manifiestan las reacciones adversas."

      - image: "/assets/images/xv-jornada-04.jpg"
        alt: "Gráfico de barras de la frecuencia de reacciones adversas a medicamentos"
        caption: "Visualización de síntomas (n=13) que permite priorizar los eventos adversos con mayor impacto en la calidad de vida del paciente."

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