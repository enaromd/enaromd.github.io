---
layout: page
title: "Disfunción Diastólica en Hemodiálisis"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/lvdd/
lang: es

page_components:
  - type: "header"
    title: "Triage Cardiorrenal: Cuantificando Razones de Prevalencia Robustas bajo Sesgo de Supervivencia"
  
    bottom_line:
      label: "En Resumen"
      text: "Al implementar un modelo de regresión de Poisson robusto para ajustar por las limitaciones muestrales de un solo centro, este análisis aisló la <span class='highlight-metric'>Hipertensión Crónica (RP ajustada: 2.22)</span> y el <span class='highlight-metric'>control glucémico (RP ajustada: 1.16)</span> como los principales factores independientes de insuficiencia cardíaca en hemodiálisis de mantenimiento, precisando la magnitud del riesgo."

    tech_stack:
      label: "Estrategias Clave"
      items:
        - "Mitigación de sesgos"
        - "Modelado de regresión robusta"
        - "Control multivariado de confusión"
  
  - type: "section"
    title: "El Desafío: Mortalidad Cardiovascular Silenciosa"
    content: "En pacientes en hemodiálisis de mantenimiento por Enfermedad Renal Crónica (ERC) avanzada en Estadio G5, <strong>la enfermedad cardiovascular es la principal causa de mortalidad</strong>. La Disfunción Diastólica del Ventrículo Izquierdo (DDVI) representa un marcador temprano y silencioso de esta crisis cardiorrenal."

  - type: "section"
    title: "Un Sesgo que Sobrevive"
    content: 'Los conjuntos de datos transversales en salas de diálisis activas sufren inherentemente del <strong>sesgo de Neyman (sesgo de supervivencia)</strong>. Debido a que los pacientes cardiorrenales de mayor gravedad suelen fallecer o requerir hospitalización de emergencia antes de que se capturen sus datos, los modelos estadísticos estándar terminan analizando <strong>una cohorte de sobrevivientes de estabilidad "no natural".</strong>'

  - type: "skills"
    skills_heading: "Elevando los Protocolos Clínicos a través de la Mentoría Estadística"
    skills_description: "Rescatar un protocolo de investigación institucional requiere ir más allá de la recolección de datos basales. Mi enfoque de asesoría se centró en orientar a los investigadores clínicos para que miraran más allá de los valores p y auditaran visualmente las distribuciones subyacentes de su cohorte."
    skills:
      - title: Visualización de la Varianza Oculta
        icon: "assets/images/icons/statistic.png"
        one: "Guié al equipo en la implementación de <b>visualizaciones de distribución</b> para desenmascarar un patrón crítico que ninguna tabla descriptiva podía revelar: varianza severa con asimetría a la derecha y múltiples valores atípicos no controlados que alcanzaban hasta un 10% de HbA1c."

      - title: Redirección Analítica
        icon: "assets/images/icons/selection.png"
        one: "Orienté al equipo de investigación hacia un <b>modelo de Regresión de Poisson con varianza robusta</b>, lo que les permitió calcular Razones de Prevalencia (RP) no infladas que traducen con mayor precisión la magnitud clínica del riesgo."

      - title: Regresiones Secuenciales
        icon: "assets/images/icons/timeline.png"
        one: "Estructuré una <b>matriz de regresión multivariada en tres fases</b>: modelos ajustados por demografía basal (edad/sexo), ruido nutricional/metabólico (IMC/Albúmina) y una fase final de integración multisistémica."

  - type: "showcase"
    heading: "Desenmascarando la Magnitud del Riesgo"
    description: "El protocolo auditado reveló que un alarmante 72.5% de la cohorte en hemodiálisis padecía activamente de DDVI. Al superar las limitaciones de una muestra pequeña de un solo centro mediante un modelado robusto, mi mentoría bioestadística orientó al equipo a extraer tamaños de efecto no inflados."
    image: "/assets/images/cover_project_lvdd.png"
    alt: "Forest plot de comparación de modelos para DDVI que muestra las RP y los valores p para los Modelos 1, 2 y 3"
    caption: "Figura 1: Regresiones de Poisson Multivariadas Estratificadas. Al reemplazar los odds ratio logísticos inestables por estimadores de covarianza de sándwich robustos, el marco controla con éxito las severas limitaciones muestrales (N = 51) sin sobresaturar los parámetros."
    metrics:
      - value: "72.5%"
        label: "Prevalencia de DDVI en la Cohorte"
        detail: "Carga basal desenmascarada en la cohorte activa en hemodiálisis."

      - value: "2.22"
        unit: "RPa"
        label: "para Hipertensión Crónica"
        detail: "Razón de prevalencia ajustada<br>(p < 0.001, IC 95%: 1.48–3.35)."

      - value: "+16%"
        unit: "por Unidad de HbA1c"
        label: "Riesgo por Incremento Glucémico"
        detail: "Aumento de riesgo por cada 1% de elevación de HbA1c<br>(p < 0.001)."

  - type: "quote"
    text: "La verdadera mentoría bioestadística no se trata de perseguir valores p; se trata de capacitar a un equipo clínico para reconocer dónde termina el ruido biológico y dónde comienza el riesgo real."
    background_image: "/assets/images/cta-bg.jpg"

  - type: "reflections"
    heading: "Reflexiones: La Metodología Dicta la Interpretación"
    description: "Guiar la capa bioestadística de este protocolo cardiorrenal consolidó un hecho en el análisis de salud: <b>el modelado matemático a ciegas falla cuando se desconecta de la fisiopatología clínica</b>. Rescatar este análisis requirió instruir al equipo de investigación para ir más allá de los resultados brutos del software estadístico y evaluar críticamente las implicaciones biológicas dentro de su arquitectura de datos."
    cards:
      - title: "El Efecto Techo"
        lead: "La patología universal destruye la varianza estadística. "
        body: "Factores de riesgo clásicos como la anemia severa no alcanzaron significancia debido a su omnipresencia en la ERC en Estadio G5. Asesoré al equipo para enfocarse en factores volátiles y de alto impacto, como las alteraciones metabólicas."

      - title: "El Compromiso de la Vida Media"
        lead: "La mecánica biológica distorsiona los desenlaces brutos. "
        body: "La hemodiálisis destruye mecánicamente los glóbulos rojos, reduciendo de forma artificial los valores brutos de HbA1c. Le advertí al equipo que el incremento de riesgo del 16% identificado por cada punto de HbA1c es un efecto sumamente conservador."

      - title: "Optimización Futura"
        lead: "Superar el sesgo de supervivencia requiere un seguimiento longitudinal. "
        body: "Aunque nuestro modelo robusto de Poisson logró estabilizar esta foto transversal, el sesgo de Neyman sigue siendo una amenaza inherente. Por lo tanto, recomiendo implementar un registro longitudinal que siga a las cohortes desde el primer día."

cta:
  heading: "Conecta la realidad clínica de primera línea con la ejecución técnica"
  description: "La analítica efectiva en salud comienza por comprender cómo nacen los datos junto a la cama del paciente, incluyendo los caóticos flujos de trabajo y factores humanos que distorsionan los registros. Si tu equipo necesita a alguien que combine la perspectiva clínica con Python, SQL y bioestadística, pongámonos en contacto."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Contáctame"
    url: "contact/"
---

<style>
.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}
</style>

{% for component in page.page_components %}
  {% if component.type == "section" %}
    {% include project-section.html data=component %}
  {% elsif component.type == "header" %}
    {% include project-header.html data=component %}
  {% elsif component.type == "skills" %}
    {% include skill-cards.html data=component %}
  {% elsif component.type == "reflections" %}
    {% include project-reflection-cards.html data=component %}
  {% elsif component.type == "figure" %}
    {% include project-chart.html data=component %}
  {% elsif component.type == "showcase" %}
    {% include project-chart-impact.html data=component %}
  {% elsif component.type == "quote" %}
    {% include project-quote.html data=component %}
  {% endif %}
{% endfor %}

{% include cta.html %}