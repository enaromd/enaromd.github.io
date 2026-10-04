---
layout: page
title: "Intensidad Medicamentosa y Enfermedad Cardíaca"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/mbi/
lang: es

page_components:
  - type: "header"
    title: "Brecha Hemodinámica: La Intensidad Medicamentosa como Indicador Subrogado de Remodelado Cardíaco"
  
    bottom_line:
      label: "Conclusión Clave"
      text: "El Índice de Carga Medicamentosa estratificó con éxito al <span class='highlight-metric'>25.7% de la cohorte clínica de alto volumen en zonas de riesgo de alta agudeza</span>, identificando complejidad hemodinámica avanzada e hipertensión pulmonar crítica directamente desde huellas farmacológicas."

    tech_stack:
      label: "Stack Tecnológico"
      items:
        - "Programación orientada a objetos (POO)"
        - "Pandas"
        - "NumPy"
        - "Statsmodels"
        - "Matplotlib" 
        - "Seaborn"

  - type: "section"
    title: "El Desafío: Alto volumen en un cronograma comprimido"
    content: "Durante un sprint clínico de alta exigencia de 10 días, los equipos de campo debieron triar rápidamente una afluencia abrumadora de pacientes con cardiopatías estructurales complejas. El cuello de botella operativo inmediato residía en la selección de pacientes: los clínicos debían <strong>identificar rápidamente qué pacientes estaban evolucionando activamente hacia una falla hemodinámica crítica</strong> para acelerar su acceso a Ecocardiografía Transesofágica (ETE) antes de que se cerrara su ventana de intervención."

  - type: "section"
    title: "La Distorsión de Datos: Sesgo de Ausencia No Aleatoria (MNAR)"
    content: "Para sobrevivir al ritmo extremo de la misión médica, <strong>los cardiólogos maximizan el rendimiento clínico documentando únicamente la patología crítica, dejando completamente en blanco los campos correspondientes a estructuras cardíacas sanas</strong>. Esta taquigrafía clínica introduce un sesgo severo de Ausencia No Aleatoria (MNAR) que distorsiona agresivamente el conjunto de datos, infla artificialmente la severidad basal aparente de la cohorte y rompe por completo los modelos estadísticos."

  - type: "skills"
    skills_heading: "Restaurando la Señal en la Línea Base de la Cohorte"
    skills_description: "Para superar la taquigrafía de documentación de los clínicos, diseñé un pipeline de datos clínicos que restaura la varianza poblacional y extrae indicadores fisiológicos ocultos a través de tres fases independientes de ingeniería:"
    skills:
      - title: Mitigación de Sesgo
        icon: "assets/images/icons/data_management.png"
        one: "Diseñé un <b>modelo de Imputación Gaussiana</b> alineado con las guías de la Sociedad Americana de Ecocardiografía. Al inyectar ruido fisiológico controlado centrado en parámetros de referencia saludables, el algoritmo recupera la verdadera varianza poblacional."

      - title: Ingeniería del Índice
        icon: "assets/images/icons/engineering.png"
        one: "Desarrollé el <b>Índice de Carga Medicamentosa (MBI)</b>. Este parámetro normaliza arreglos complejos de polifarmacia frente a techos terapéuticos, convirtiendo registros de medicamentos fragmentados en una métrica subrogada estandarizada de remodelado cardíaco."

      - title: Triage Estadístico
        icon: "assets/images/icons/statistic.png"
        one: "Ejecuté un análisis de curva <b>Característica Operativa del Receptor (ROC)</b> para mapear los puntajes MBI frente a indicadores clínicos y hemodinámicos objetivos, estableciendo un punto de corte empírico de triage que prioriza a pacientes de alta agudeza con alta precisión."

  - type: "flexible_content"
    heading: "Cuantificando la intensidad: Cómo funciona el MBI"
    blocks:
      - type: "paragraph"
        text: "En lugar de un simple conteo de pastillas, el Índice de Carga Medicamentosa evalúa el 'esfuerzo' colectivo al que se somete el sistema cardiovascular de un paciente bajo soporte médico activo. El motor calcula esto evaluando las dosis individuales de medicamentos en relación con sus umbrales terapéuticos máximos reconocidos mundialmente y aplicando pesos clínicos específicos por clase:"

      - type: "formula"
        equation: "MBI = \\sum_{i=1}^{n} \\left( \\text{Peso}_{\\text{clase}_i} \\times \\frac{\\text{Dosis Diaria Total}_i}{\\text{Dosis Máxima}_i} \\right)"

      - type: "paragraph"
        text: "Para estandarizar este cálculo, el pipeline procesa dos variables críticas:"

      - type: "bullets"
        items:
          - "**Dosis Diaria Total:** Los miligramos totales consumidos por el paciente en 24 horas. Por ejemplo, un paciente con Furosemida 40 mg cada 12 h tiene una $DDT = 80\\text{ mg}$."
          - "**Pesos Clínicos:** El código asigna pesos más altos (ej. **3.0**) a diuréticos de asa y pesos más bajos (**0.5**) a estatinas o medicamentos de mantenimiento."

      - type: "paragraph"
        text: "Al consolidar estos arreglos complejos de polifarmacia en una sola variable continua estandarizada, el índice desenmascara la severidad avanzada de la enfermedad mucho antes de que el paciente llegue a la estación de ecocardiografía."

      - type: "paragraph"
        text: "El código asigna pesos específicos basados en la severidad de la condición tratada, priorizando las señales de remodelado cardíaco:"

      - type: "table"
        headers:
          - "Peso"
          - "Prioridad"
          - "Clases de Medicamentos"
        rows:
          - ["3.0", "**Crítica**", "Diuréticos de asa, Vasodilatadores pulmonares."]
          - ["2.0", "**Alta**", "Inhibidores del SRAA, Betabloqueadores, SGLT2."]
          - ["1.0", "**Moderada**", "Anticoagulantes, Antagonistas de canales de calcio."]
          - ["0.5", "**Mantenimiento**", "Estatinas, Fármacos metabólicos."]

  - type: "showcase"
    heading: "Triage Hemodinámico Impulsado por MBI"
    description: "El resultado final del análisis de datos es un marco de clasificación no lineal que estratificó con éxito al 25.7% de la cohorte de pacientes en zonas de riesgo clínico de alta agudeza. Esto permite a la misión médica aislar a los candidatos de mayor beneficio para intervención y maximizar la utilidad diagnóstica bajo estrictas restricciones de recursos en el campo."
    image: "/assets/images/cover_project_mbi.png"
    alt: "Distribución de MBI y Zonas de Triage"
    caption: "<b>Figura 1: Correlación entre MBI y severidad hemodinámica.</b> Se muestran las tres zonas de triage operativo validadas."
    metrics:
      - value: "67%"
        label: "Rescate de Cohorte"
        detail: "Evitó la exclusión de la cohorte de pacientes al diagnosticar patrones de taquigrafía MNAR y preservar los datos basales."

      - value: "34.7%"
        label: "Inflación de Patología Corregida"
        detail: "Eliminó la elevación artificial al reducir la PSVD promedio sesgada de 51.0 mmHg a 33.3 mmHg, reflejando una línea base más precisa."

      - value: "28.9%"
        label: "Discordancia Clínica Desenmascarada"
        detail: "Identificó perfiles de riesgo ocultos en pacientes que mantenían presiones moderadas únicamente a través de medicación agresiva."

  - type: "figure"
    heading: "Estructura del Dashboard y Visualizaciones"
    description: "Cada componente visual funciona como un filtro interactivo activo, permitiendo a los usuarios examinar subcohortes dinámicamente con solo hacer clic en segmentos específicos de datos."
    dashboard_vertical: "/assets/images/mbi_dashboard.png"
    link: "https://public.tableau.com/app/profile/enyel.a.rodr.guez.g./viz/MBIstratification/MBIstratification"
    alt: "Dashboard de MBI"

  - type: "results"
    cards:
      - title: "Distribución de la Cohorte"
        lead_1: "Registro de Distribución por Edad: "
        description_1: "Un histograma continuo que detalla la composición por edad de la cohorte de la misión."
        lead_2: "Desglose por Género (Gráfico de Dona): "
        description_2: "Permite una auditoría rápida de las variaciones clínicas según el género en los diferentes grupos de patologías."

      - title: "Encrucijada Patológica"
        lead_1: "Matriz de Prevalencia de Enfermedades: "
        description_1: "Mapea los diagnósticos que motivan la consulta del paciente, codificados por colores según las Zonas de Triage de MBI."
        lead_2: "Composición del Índice: "
        description_2: "Descompone la Carga Medicamentosa en distintas clases farmacológicas."

      - title: "Tarjetas de KPI Promedio"
        lead_1: "Huella Operativa: "
        description_1: "Ofrece una lectura operativa de la huella de polifarmacia en los campos seleccionados."
        lead_2: "Línea Base Hemodinámica (PSVD): "
        description_2: "Rastrea la PSVD en relación con los umbrales de triage propuestos."

  - type: "quote"
    text: "El MBI transforma una lista de medicamentos en una métrica de severidad, permitiendo que la misión opere con mayor eficiencia."

  - type: "flexible_content"
    heading: "Reflexiones: El Contexto Dicta la Estructura"
    blocks:
      - type: "paragraph"
        text: "El desarrollo del motor Cardio-MBI-Triage consolidó una verdad fundamental de la informática médica especializada: <strong>los patrones puros de análisis de datos fallan si se implementan sin un profundo dominio del contexto clínico.</strong>"

      - type: "callout"
        lead: "Conclusión Clave:"
        text: "Un equipo externo de datos que examinara este conjunto de datos incompletos a ciegas habría descartado por completo las filas incompletas (destruyendo el tamaño de la cohorte) o habría aplicado imputaciones promedio estándar sin ponderar, enmascarando por completo la crisis estructural real de la operación de campo."

      - type: "paragraph"
        text: "Al combinar una comprensión íntima de los patrones de comportamiento de los cardiólogos en entornos clínicos de alto estrés con una estructura de datos robusta, este pipeline tradujo con éxito registros de medicamentos fragmentados en objetivos diagnósticos de alta fidelidad, maximizando el impacto del recurso más escaso de la misión: el tiempo del especialista."

  - type: "gallery"
    heading: "Análisis de Datos y Visualización"
    description: "Desde el procesamiento de datos crudos hasta la validación estadística: el flujo de trabajo end-to-end para la misión cardiológica 'Project Health for Leon' 2025."
    items:
      - image: "/assets/images/mbi_code.png"
        alt: "Diccionario de dosis de medicamentos"
        caption: "Implementación de la clase ClinicalConfig para estandarizar los pesos y dosis de medicamentos en un pipeline ejecutable en Python."

      - image: "/assets/images/mbi_imputation.jpg"
        alt: "Análisis de sensibilidad"
        caption: "Uso de Imputación Gaussiana Estocástica para corregir la 'Ausencia Informativa' (MNAR) y restaurar la distribución fisiológica natural de la PSVD."

      - image: "/assets/images/mbi_3nf.jpg"
        alt: "Base de datos en 3NF"
        caption: "La capa de base de datos implementa un Esquema en Copo de Nieve de 5 tablas, aplicando el cumplimiento de Tercera Forma Normal (3NF) en las tablas principales."

      - image: "/assets/images/mbi_roc_rvsp.jpg"
        alt: "Curva ROC para PSVD"
        caption: "Análisis de Curva ROC que establece el umbral de 5.25 en MBI como un marcador de alta precisión para hipertensión pulmonar crítica."

      - image: "/assets/images/mbi_discordance.jpg"
        alt: "Análisis de residuos para MBI y PSVD"
        caption: "Identificación de pacientes 'engañosamente estables' que mantienen presiones moderadas únicamente a través de compensación farmacológica agresiva."

      - image: "/assets/images/mbi_table.jpg"
        alt: "Tabla 1: Características basales"
        caption: "Definición del 'Punto Óptimo' clínico para priorizar intervenciones quirúrgicas basadas en la intersección de zonas de MBI y severidad hemodinámica."

  - type: "button"
    text: "Ver README en GitHub"
    url: "https://github.com/enaromd/Cardio-MBI-Triage-Engine"
    icon: "github"
    align: "center"

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