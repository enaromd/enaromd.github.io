---
layout: page
title: "Obesidad Clínica en NHANES 2021-2023"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/nhanes_obesity/
lang: es

page_components:
  - type: "header"
    title: "Cuando el Peso No Pesa Igual en Todos: Aplicando el Marco de Obesidad Clínica de The Lancet"
  
    bottom_line:
      label: "Conclusión Clave"
      text: "El Puntaje Metabólico para Resistencia a la Insulina <span class='highlight-metric'>(METS-IR) mostró un sólido efecto independiente para fibrosis hepática confirmada por FibroScan (RR Ajustado = 2.9)</span> y el mejor ajuste global del modelo (QIC = 815.7) en comparación con otras razones lipídicas y glucémicas en modelos totalmente ajustados."

    tech_stack:
      label: "Stack Tecnológico"
      items:
        - " Python"
        - "PyReadStat"
        - "Pandas"
        - "NumPy"
        - "Matplotlib"
        - "Missingno"
        - "PyArrow"

  - type: "section"
    title: "El Desafío: La brecha diagnóstica del Índice de Masa Corporal (IMC)"
    content: "<strong>Los clínicos confían de manera casi universal en el Índice de Masa Corporal (IMC ≥ 30 kg/m²) como el filtro diagnóstico predeterminado para evaluar la obesidad</strong>. Al depender exclusivamente de las proporciones entre peso y talla, los protocolos de cribado estándar pasan por alto un compromiso cardiometabólico, hepático y renal subclínico significativo en individuos con peso normal pero metabólicamente no saludables."

  - type: "section"
    title: "La Brecha de Traducción: Razones Antropométricas e Índices de Riesgo"
    content: "Operativizar el Marco de Obesidad Clínica de The Lancet requiere ir más allá del IMC crudo mediante el cálculo de razones antropométricas específicas—como la Razón Cintura-Estatura (RCEst)—para definir con precisión los fenotipos de obesidad clínica.<br><br>Además, los datos crudos de NHANES almacenan biomarcadores como parámetros de laboratorio aislados a través de submuestras complejas de la encuesta. <strong>Para cuantificar sistemáticamente el riesgo cardiovascular, metabólico y de órgano blanco, estos insumos individuales deben traducirse en índices de riesgo clínico validados</strong> (por ejemplo, METS-IR, FIB-4, FLI y AHA PREVENT) para capturar la vulnerabilidad subclínica antes de un daño orgánico manifiesto."

  - type: "skills"
    skills_heading: "Filtración de Cohorte, Ingeniería de Riesgo y Modelado GEE"
    skills_description: "Ejecución de un pipeline bioestadístico end-to-end: desde la atrición estructurada de la cohorte (N = 1,816) hasta el cálculo de índices compuestos y la estimación de Razones de Riesgo ponderadas por diseño muestral."
    skills:
      - title: Atrición Secuencial de la Cohorte
        icon: "assets/images/icons/timeline.png"
        one: "Construí un pipeline de filtración intencional aislando a adultos en edad laboral (18 a 64 años) del ciclo NHANES 2021–2023, <b>controlando sistemáticamente el embarazo, registros no ponderados y parámetros basales faltantes</b> (N = 11,933 → 1,816)."

      - title: Operativización de Índices de Riesgo
        icon: "assets/images/icons/engineering.png"
        one: "Transformé <b>datos crudos en índices de riesgo clínico validados</b>, incluyendo el Puntaje Metabólico para Resistencia a la Insulina (METS-IR), el Índice de Hígado Graso (FLI), el Índice Fibrosis-4 (FIB-4) y los puntajes de riesgo cardiometabólico-renal AHA PREVENT."

      - title: Razones de Riesgo Ponderadas por Encuesta
        icon: "assets/images/icons/statistic.png"
        one: "Apliqué <b>Ecuaciones de Estimación Generalizadas (GEE) con enlace logarítmico y familia Poisson</b>, incorporando parámetros de diseño muestral (unidades primarias de muestreo SDMVPSU, estratos SDMVSTRA y pesos de ayuno WTSAF2YR) para calcular Razones de Riesgo (RR) ajustadas a la población."

  - type: "figure"
    heading: "Selección de Cohorte y Atrición Sistemática"
    description: "Ejecución de un pipeline de filtración para controlar saltos complejos de la encuesta, pesos de submuestras de ayuno y criterios limítrofes fenotípicos."
    dashboard_vertical: "/assets/images/nhanes_flowchart.svg"
    alt: "Diagrama de flujo STROBE"
    caption: "<b>Figura 1. Pipeline de Atrición de la Cohorte.</b> Filtración secuencial del conjunto de datos maestro de NHANES 2021–2023 (N = 11,933). El cumplimiento del protocolo de ayuno matutino (WTSAF2YR), los límites de edad laboral (18–64 años) y la higiene de datos de casos completos aislaron a 1,816 adultos en ayunas. La depuración de 228 registros ambiguos no clasificados estableció una cohorte final fenotípicamente válida de N = 1,588 adultos."

  - type: "flexible_content"
    heading: "Estratificación de la Población Basal (Tabla 1)"
    blocks:
      - type: "paragraph"
        text: "Evaluación de gradientes demográficos, de examen y biomarcadores ponderados por encuesta en las cohortes de fenotipos Control, Periférico y Clásico (N = 1,588)." 

      - type: "table"
        headers:
          - "Variable"
          - "Global"
          - "Control"
          - "Periférico"
          - "Clásico"
        rows:
          - ["Edad (años)", "40.92", "32.05", "45.55", "42.94"]
          - ["PA Sistólica (mmHg)", "117.21", "112.75", "118.29", "119.31"]
          - ["PA Diastólica (mmHg)", "74.59", "68.59", "74.11", "78.64"]
          - ["Frecuencia cardíaca (lpm)", "70.88", "69.30", "70.41", "72.06"]
          - ["Glucosa en ayunas (mg/dL)", "105.06", "98.72", "103.94", "111.31"]
          - ["Triglicéridos (mg/dL)", "108.60", "74.17", "117.46", "124.36"]
          - ["Colesterol HDL (mg/dL)", "53.62", "60.70", "53.50", "49.59"]
          - ["Rigidez Hepática (kPa)", "5.76", "4.86", "5.42", "6.79"]
          - ["TFGe (mL/min/1.73m²)", "102.51", "108.14", "99.57", "101.41"]
          - ["Daño hepático (%)", "13.96", "4.08", "9.55", "25.13"]
          - ["Daño metabólico (%)", "6.42", "0.09", "7.90", "9.82"]
          - ["Daño renal (%)", "0.99", "0.00", "0.93", "1.54"]

  - type: "figure"
    heading: "Riesgo Relativo Fenotípico e Ajustado por Índice"
    description: "Rastreo del riesgo de fibrosis hepática desde líneas base fenotípicas no ajustadas (M1) a través de subrogados cruzados (M2) hasta modelos fenotipo-índice totalmente integrados (M3)."
    image: "/assets/images/nhanes_plot_indices_forest_coefficients.png"
    alt: "Gráfico de Bosque (Forest Plot) comparando Razones de Riesgo entre índices"
    caption: "<b>Figura 2. Atenuación Secuencial del Riesgo en Regresión de Poisson con GEE.</b> Comparación de fenotipos estructurales basales (M1) frente a modelos integrados (M3). La inclusión del punto de corte diagnóstico de METS-IR (RR = 2.87) atenúa la razón de riesgo del Fenotipo Clásico de RR = 5.19 (IC 95%: 2.94-9.17) a RR = 2.44 (IC 95%: 1.22-4.89), confirmando la disfunción metabólica como un mediador primario del daño hepático a órgano blanco."

  - type: "results"
    cards:
      - title: "IMC y Daño Hepático No Ajustado"
        description_1: "Los modelos no ajustados muestran que el <span class='highlight-metric'>Fenotipo Clásico impulsado por el IMC rastrea fuertemente el daño hepático (RR = 5.19).</span>"
        description_2: "Sin embargo, <span class='highlight-metric'>depender únicamente del IMC ignora al 35.0% de los adultos</span> categorizados como Periféricos, quienes aún enfrentan un riesgo hepático elevado (RR = 1.95)."

      - title: "METS-IR como Subrogado del Riesgo de Daño Hepático"
        description_1: "METS-IR funciona como un <span class='highlight-metric'>sólido factor independiente del daño hepático</span> en todo el modelo integrado <span class='highlight-metric'>(RR = 2.87).</span>"
        description_2: "Crucialmente, detecta picos marcados de riesgo de daño tanto en la cohorte clásica aislada (RR = 2.76) como en la periférica aislada (RR = 3.60)."

      - title: "Fenotipos y Disparidades de Riesgo por Dominio"
        description_1: "Al abarcar el 45.8% de los adultos, el <span class='highlight-metric'>Fenotipo Clásico impulsa la mayor parte del riesgo multidominio (28.3% global).</span>"
        description_2: "Como resultado, mantiene un mayor riesgo de daño a órgano blanco (RR = 2.44) que el Fenotipo Periférico (RR = 1.91), incluso tras integrar METS-IR."

  - type: "showcase"
    heading: "De Fenotipos Clínicos a Riesgo por Dominio y Daño a Órgano Blanco"
    description: "Mapeo de la cascada ponderada por encuesta desde la composición corporal basal hasta la afectación orgánica manifiesta a través de clústeres subclínicos."
    image: "/assets/images/cover_project_nhanes-obesity.png"
    alt: "Diagrama de flujo ponderado por encuesta que mapea fenotipos de obesidad hacia el riesgo de daño orgánico"
    caption: "<b>Figura 3. Trayectorias Fenotípicas a través de Clústeres de Riesgo por Dominio.</b> Diagrama de flujo ponderado por encuesta que mapea los fenotipos de obesidad hacia el riesgo de daño orgánico. Los controles saludables fluyen exclusivamente hacia cero daño orgánico, mientras que el Fenotipo Clásico actúa como el origen principal de disfunción multidominio (≥2 sistemas orgánicos), reforzando el riesgo sinérgico del esfuerzo hepático y metabólico."
    metrics:
      - value: "45.8%"
        unit: "(69.48M)"
        label: "Prevalencia del Fenotipo de Obesidad Clásica"
        detail: "Fenotipo clínico dominante que impulsa la carga principal de riesgo subclínico multidominio descendente."

      - value: "28.3%"
        unit: "(42.98M)"
        label: "Riesgo de Daño a Órgano Blanco Multidominio"
        detail: "Riesgo en múltiples dominios, sirviendo como el estado de transición primario hacia el daño orgánico manifiesto."

      - value: "13.4%"
        unit: "(20.27M)"
        label: "Daño Hepático a Órgano Blanco"
        detail: "Daño orgánico principal, superando con creces la sobrecarga aislada metabólica (5.1%), renal (0.7%) o multiorgánica (2.4%)."

  - type: "quote"
    text: "Redefinir la obesidad pasando de un número antropométrico estático a un continuo metabólico multisistémico es el primer paso esencial hacia una verdadera medicina de precisión, demostrando que el peso corporal por sí solo no puede dictar la vulnerabilidad clínica."

  - type: "flexible_content"
    heading: "Reflexión: Redefiniendo la Obesidad Más Allá de la Báscula"
    blocks:
      - type: "paragraph"
        text: "Nuestros hallazgos desafían la tradicional dependencia del IMC como único filtro diagnóstico: dos individuos con mediciones antropométricas similares pueden albergar trayectorias radicalmente diferentes de sobrecarga orgánica subclínica."

      - type: "callout"
        lead: "Conclusión Clave:"
        text: "La salud metabólica no se puede inferir solo a partir de la masa corporal. En adultos con IMC normal clasificados en el fenotipo de Obesidad Periférica, <b>cruzar el umbral elevado de METS-IR desencadena un aumento de 3.60 veces en el riesgo relativo de fibrosis hepática confirmada por FibroScan</b>, lo que demuestra que la resistencia subclínica a la insulina impulsa el daño tisular mucho antes de que se manifieste la obesidad clínica evidente."

      - type: "paragraph"
        text: "Traducir estos conocimientos bioestadísticos a la atención del mundo real requiere integrar la automatización de índices de riesgo—como METS-IR, FIB-4 y FLI—directamente en los flujos de trabajo de los expedientes clínicos electrónicos (EHR). Automatizar estos cálculos a partir de paneles de laboratorio de rutina crea un cambio de paradigma fundamental: alejar la atención médica de la gestión reactiva de enfermedades en etapas tardías y orientarla hacia una intervención subclínica proactiva y guiada por algoritmos."

  - type: "gallery"
    heading: "Visuales Diagnósticos y Trayectorias Fenotípicas"
    description: "Fórmulas de índices, gráficos ridgeline ponderados por encuesta, comparaciones de modelos de Poisson con GEE y mapas Sankey de trayectorias multidominio."
    items:
      - image: "/assets/images/obesity_indices_formulas.jpg"
        alt: "Operativización de índices clínicos"
        caption: "Formulaciones matemáticas para índices compuestos de riesgo, detallando las ecuaciones de METS-IR, eTFG CKD-EPI 2021 e Índice TyG."

      - image: "/assets/images/obesity_indices_ridgelines.jpg"
        alt: "Gráficos ridgeline de índices clínicos"
        caption: "Gráficos de densidad ridgeline ponderados por encuesta que ilustran la separación de biomarcadores en la población a través de los fenotipos Control, Periférico y Clásico."

      - image: "/assets/images/obesity_indices_table.jpg"
        alt: "Tabla comparativa de índices clínicos"
        caption: "Tabla de distribución de medias ajustadas por diseño que compara fenotipos Control, Periférico y Clásico en marcadores renales, hepáticos y cardiometabólicos."

      - image: "/assets/images/obesity_indices_forest.jpg"
        alt: "Forest plot comparando índices clínicos entre modelos de regresión"
        caption: "Forest plot de regresión de Poisson con GEE comparando modelos de Riesgo Relativo (RR) no ajustados (M2) vs. totalmente ajustados (M3) y métricas de ajuste QIC."

      - image: "/assets/images/obesity_sankey_bmi.jpg"
        alt: "Diagrama de Sankey: IMC a daño orgánico"
        caption: "Diagrama de Sankey ponderado por encuesta que mapea el flujo poblacional desde categorías de IMC estándar hasta fenotipos clínicos y daño a órgano blanco."

      - image: "/assets/images/obesity_sankey_mets-ir.jpg"
        alt: "Diagrama de Sankey: METS-IR a daño orgánico"
        caption: "Diagrama de flujo ponderado por encuesta que mapea IMC, fenotipos clínicos, umbrales de riesgo METS-IR y resultados de daño hepático."

  - type: "button"
    text: "Ver README en GitHub"
    url: "https://github.com/enaromd/clinical-obesity"
    icon: "github"
    align: "center"

cta:
  heading: "Conecte la Realidad Clínica de Primera Línea con la Ejecución Técnica"
  description: "La analítica de salud efectiva comienza entendiendo cómo nacen los datos al pie de la cama del paciente, incluyendo los flujos de trabajo ajetreados y los factores humanos que distorsionan los registros crudos. Si su equipo necesita a alguien que combine la perspectiva clínica de primera línea con Python, SQL y bioestadística, conectemos."
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