---
layout: splash
title: "Índice de carga farmacológica"
permalink: portfolio/projects/mbi/
lang: es
# Social previews
description: "Desarrollo de un motor clínico en Python para cuantificar la intensidad farmacológica. Incluye umbrales de triaje validados mediante curvas ROC para hipertensión pulmonar crítica."
header:
  teaser: "/assets/images/mbi_triage.png"
# This block communicates directly with the SEO plugin
seo:
  type: "article"
  title: "Índice de carga farmacológica" # Repeat title here
  image: "/assets/images/mbi_triage.png"
# Sections
solution:
  - title: "Restaurando la Señal en la Línea Base de la Cohorte"
  - excerpt: "Para superar las anotaciones abreviadas de los médicos, diseñé un pipeline de datos clínicos que restaura la varianza de la población y extrae indicadores fisiológicos ocultos a través de tres fases independientes de ingeniería:"
results:
  - title: "Triaje Hemodinámico Guiado por MBI"
  - excerpt: "El resultado definitivo del análisis de datos es un marco de clasificación no lineal que estratificó exitosamente al <span class='highlight-metric'>25.7% de la cohorte de pacientes en zonas de riesgo clínico de alta agudeza</span>. Esto permite a la misión médica aislar a los candidatos con mayor beneficio de intervención y maximizar la utilidad diagnóstica bajo estrictas limitaciones de recursos en el trabajo de campo."
dashboard:
  - title: Estructura del dashboard y visualizaciones
  - excerpt: "Cada componente visual funciona como un filtro interactivo activo, lo que permite a los usuarios examinar subcohortes de forma dinámica con solo hacer clic en segmentos de datos específicos."
highlights_title: 
  - title: "Análisis de Datos y Visualización"
  - excerpt: "Del procesamiento de crudos a la validación estadística: el proceso completo de la brigada de cardiología 'Project Health for Leon' 2025."
highlights:
  - url: "/assets/images/mbi_code.png"
    image_path: "/assets/images/mbi_code.png"
    alt: "Arquitectura del Motor MBI"
    title: "Implementación de la clase ClinicalConfig para estandarizar pesos y dosis de medicamentos en un pipeline de Python reproducible."
  - url: "/assets/images/mbi_imputation.jpg"
    image_path: "/assets/images/mbi_imputation.jpg"
    alt: "Restauración de la Integridad de Datos"
    title: "Uso de Imputación Estocástica Gaussiana para corregir el sesgo de datos faltantes (MNAR) y restaurar la distribución fisiológica natural de la PSAP."
  - url: "/assets/images/mbi_3nf.jpg"
    image_path: "/assets/images/mbi_3nf.jpg"
    alt: "Esquema 3NF"
    title: "La capa de base de datos implementa un Esquema Copo de Nieve (Snowflake Schema) de 5 tablas, garantizando el cumplimiento de la Tercera Forma Normal (3NF) en las tablas principales."
  - url: "/assets/images/mbi_roc_rvsp.jpg"
    image_path: "/assets/images/mbi_roc_rvsp.jpg"
    alt: "Validación Estadística"
    title: "Análisis de curva ROC que establece el umbral de 5.25 MBI como un marcador de alta precisión para la hipertensión pulmonar crítica."
  - url: "/assets/images/mbi_discordance.jpg"
    image_path: "/assets/images/mbi_discordance.jpg"
    alt: "Mapeo de la Brecha de Tratamiento"
    title: "Identificación de pacientes 'engañosamente estables' que mantienen presiones moderadas solo mediante una compensación farmacológica agresiva."
  - url: "/assets/images/mbi_table.jpg"
    image_path: "/assets/images/mbi_table.jpg"
    alt: "Mapeo de Triaje Estratégico"
    title: "Definición del 'Punto Óptimo' clínico para priorizar intervenciones quirúrgicas basadas en la intersección de las zonas MBI y la severidad hemodinámica."
---

<style>
.feature-divider { 
    margin-top: 5rem; margin-bottom: 2rem; 
}

.cta {
    margin-top: 5rem !important;
}

.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}

.mbi-table {
    margin-left: auto !important;
    margin-right: auto !important;
    border-collapse: collapse !important;
    display: table !important;
}

.math-block {
    text-align: center;
    font-size: clamp(0.8rem, 4vw, 1.2rem); 
    overflow-x: auto;
    white-space: nowrap;
}
</style>

<div class="headline">
  <h1>Brecha Hemodinámica: La Intensidad de la Medicación como sucedáneo del Remodelado Cardíaco</h1>
  <p><strong>En Síntesis:</strong> El Índice de carga farmacológica estratificó con éxito al <span class="highlight-metric">25.7% de la cohorte clínica de alto volumen en zonas de riesgo de alta agudeza</span>, identificando la complejidad hemodinámica avanzada y la hipertensión pulmonar crítica directamente a partir de las huellas farmacológicas.</p>
</div>

<div class="skills-bar">
    <strong>Tech Stack:</strong> Object-Oriented Programming (OOP), <code>Pandas</code>, <code>NumPy</code>, <code>Statsmodels</code>, <code>Scikit-learn</code>, <code>Matplotlib/Seaborn</code>
</div>

<h2>El Desafío: Alto volumen en un cronograma comprimido</h2>
<p>Durante un sprint clínico de alta exigencia de 10 días, los equipos de campo deben clasificar rápidamente a una afluencia abrumadora de pacientes que padecen afecciones cardíacas estructurales complejas. El cuello de botella operacional inmediato radica en la selección de pacientes: los médicos deben <strong>identificar rápidamente qué pacientes están en transición activa hacia una insuficiencia hemodinámica crítica</strong> para agilizarlos hacia una Ecocardiografía Transesofágica (ETE) antes de que se cierre su ventana de intervención.</p>

<h2>La Distorsión de los Datos: Sesgo de datos faltantes informativos (MNAR)</h2>
<p>Para sobrevivir al ritmo extremo de la misión médica, <strong>los cardiólogos maximizan el rendimiento clínico documentando únicamente la patología crítica, dejando completamente en blanco los campos para las estructuras cardíacas sanas.</strong> Esta simplificación clínica introduce un grave sesgo de datos faltantes informativos (MNAR, Missing Not At Random) que desvía agresivamente el conjunto de datos, infla artificialmente la gravedad de la línea base de la cohorte y rompe por completo los modelos estadísticos.</p>

<hr class="feature-divider">

{% include feature_row id="solution" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <img src="/assets/images/data_management.png" alt="Icon: Data Processing" class="grid-icon">
    <h3>Mitigación del Sesgo</h3>
    <p>Diseñé un <strong>modelo de Imputación Gausiana</strong> alineado con las directrices de la Sociedad Americana de Ecocardiografía. Al inyectar ruido fisiológico controlado centrado en parámetros de referencia saludables, el algoritmo recupera la verdadera varianza de la población.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/engineering.png" alt="Icon: Data Processing" class="grid-icon">
    <h3>Ingeniería de Características</h3>
    <p>Desarrollé el <strong>Medication Burden Index (MBI)</strong>. Este parámetro normaliza arreglos complejos de polifarmacia frente a los límites terapéuticos máximos, transformando registros de medicación fragmentados en una métrica subrogada única y estandarizada para el remodelado cardíaco.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/statistic.png" alt="Icon: Data Processing" class="grid-icon">
    <h3>Triaje Estadístico</h3>
    <p>Ejecuté un análisis de curva <strong>Característica Operativa del Receptor (ROC)</strong> para mapear las puntuaciones de MBI calculadas frente a indicadores clínicos y hemodinámicos objetivos, estableciendo un punto de corte empírico de triaje que prioriza con alta precisión a los pacientes de alta agudeza.</p>
  </div>
</div>

<hr class="feature-divider">

<h2>Cuantificación de la intensidad: Cómo funciona el MBI</h2>
<p>Más que un simple conteo de píldoras, el Medication Burden Index evalúa el "esfuerzo" colectivo que experimenta el sistema cardiovascular de un paciente bajo soporte médico activo. El motor calcula esto evaluando las dosis de medicamentos individuales en relación con sus umbrales terapéuticos máximos reconocidos mundialmente y aplicando pesos clínicos específicos por clase:</p>

<div class="math-block">
  $$MBI = \sum \left( \text{Peso} \times \frac{\text{DDT}}{\text{Dosis Máxima}} \right)$$
</div>

<p>Para estandarizar este cálculo, el pipeline procesa dos variables críticas:</p>

<ul>
  <li><strong>Dosis Diaria Total (DDT):</strong> Los miligramos totales consumidos por el paciente en 24 horas. Por ejemplo, un paciente que toma Furosemida 40 mg cada 12 horas tiene una $DDT = 80\text{ mg}$.</li>
  <li><strong>Pesos Clínicos:</strong> El código asigna pesos más altos (por ejemplo, $3.0$) a los diuréticos de asa y vasodilatadores pulmonares, y pesos más bajos ($0.5$) a las estatinas o fármacos de mantenimiento.</li>
</ul>

<p>Al consolidar estos complejos arreglos de polifarmacia en una sola variable continua estandarizada, el índice desenmascara la gravedad avanzada de la enfermedad mucho antes de que el paciente llegue a la estación de ecocardiografía.</p>

<p>El código asigna pesos específicos basados en la gravedad de la patología tratada, priorizando las señales de remodelado cardíaco:</p>

<div class="table-container">
  <table class="mbi-table" style="width: 65%; border: 1px solid #ddd;">
    <thead>
      <tr style="background-color: #003152; color: white;">
        <th style="padding: 12px; border: 1px solid #ddd;">Peso</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Prioridad</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Clases de Medicamentos</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>3.0</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Crítico</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Diuréticos de asa, Vasodilatadores pulmonares.</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>2.0</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Alto</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Inhibidores del SRAA, Betabloqueadores, SGLT2.</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>1.0</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Moderado</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Anticoagulantes, Antagonistas de los canales de calcio.</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>0.5</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Mantenimiento</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Estatinas, Fármacos metabólicos.</td>
      </tr>
    </tbody>
  </table>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/mbi_triage.png" alt="Distribución de MBI y Zonas de Triaje" style="width: 100%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    Figura 1: Correlación entre el MBI y la gravedad hemodinámica. Se muestran las tres zonas operativas de triaje validadas.
  </p>
</div>

<div class="project-grid">
  <div class="card">
    <h3>Rescate de la Cohorte</h3>
    <p><strong>Evitó la exclusión clínica del 67% de la cohorte de pacientes</strong>. Al diagnosticar los patrones de abreviación (MNAR) de los médicos en el ingreso de datos, el pipeline preservó con éxito información valiosa de la población que los modelos estándar de eliminación habrían descartado.</p>
  </div>
  <div class="card">
    <h3>Corrección de Sobreestimación</h3>
    <p><strong>Eliminó una inflación artificial del 34.7% en la patología de la cohorte.</strong> La imputación "Natural Normal" redujo el promedio aparente de la PSVD de un valor sesgado de 51.0 mmHg a un valor fisiológicamente preciso de 33.3 mmHg, estabilizando los supuestos del modelo.</p>
  </div>
  <div class="card">
    <h3>Desenmascarando la Discordancia</h3>
    <p><strong>Identificó una tasa de discordancia clínica del 28.9%</strong> en perfiles complejos. El índice detectó con precisión a pacientes que mantenían presiones engañosamente "moderadas" solo mediante una compensación farmacológica agresiva e insostenible.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="dashboard" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <a href="https://public.tableau.com/app/profile/enyel.a.rodr.guez.g./viz/MBIstratification/MBIstratification" target="_blank">
    <img src="/assets/images/mbi_dashboard.png" alt="MBI Distribution and Triage Zones" style="width: 45%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  </a>
</div>

<div class="project-grid">
  <div class="card">
    <h3>Distribución de la Cohorte</h3>
    <span><b>Registro de Distribución de Edad:</b> Un histograma continuo que detalla la composición por edad.</span>
    <br>
    <span><b>División por Género (Gráfico de Dona):</b> Permite una auditoría rápida de las variaciones clínicas basadas en el género a través de los grupos de enfermedades.</span>
  </div>
  <div class="card">
    <h3>Encrucijada Patológica</h3>
    <span><b>Prevalencia de Enfermedades:</b> Mapea las indicaciones clínicas primarias que impulsan la presentación del paciente, completamente codificadas por colores según las Zonas de Triaje de MBI.</span>
    <br>
    <span><b>Composición del Índice de Carga de Medicamentos:</b> Deconstruye el MBI a través de distintos grupos de medicamentos.</span>
  </div>
  <div class="card">
    <h3>Tarjetas de KPI de Promedio</h3>
    <span><b>Índice de Carga de Medicamentos:</b> Proporciona una lectura instantánea de la huella operativa estándar de polifarmacia.</span>
    <br>
    <span><b>Presión Sistólica del Ventrículo Derecho (RVSP):</b> Rastrea la línea de base móvil para proporcionar una métrica sin máscara del rendimiento global del corazón derecho.</span>
  </div>
</div>

<div class="pull-quote">
  "El MBI transforma una lista de medicamentos en una <strong>métrica de severidad</strong>, permitiendo que la brigada opere con precisión estadística."
</div>

<h2>Reflexiones: El Contexto Dicta la Estructura</h2>
<p>El desarrollo de <em>Cardio-MBI-Triage-Engine</em> consolidó una verdad fundamental de la informática médica especializada: <strong>los patrones puros de ingeniería de datos fracasan si se implementan sin un profundo conocimiento del dominio clínico.</strong></p>

<blockquote>
  <strong>Conclusión Clave:</strong> Un equipo de datos externo que analizara este conjunto de datos a ciegas habría descartado por completo las filas incompletas (destruyendo el tamaño de la cohorte) o habría aplicado imputaciones medias estándar no ponderadas que ocultarían por completo la verdadera crisis estructural de la operación en el terreno.
</blockquote>

<p>Al combinar una comprensión íntima de los patrones de comportamiento de los cardiólogos en entornos clínicos de alto estrés con una estructura de datos sólida, este pipeline tradujo con éxito registros de medicación fragmentados en objetivos diagnósticos de alta fidelidad, maximizando el impacto del activo más escaso de la misión: el tiempo del especialista.</p>

<hr class="feature-divider">

{% include feature_row id="highlights_title" type="center" %}

{% include gallery id="highlights" %}

<div class="see-more-button">
  <a href="https://github.com/enaromd/Cardio-MBI-Triage-Engine" class="btn btn--primary">Ver repository en GitHub</a>
</div>

<div class="cta">
  <div style="text-align: center;">
    <h3>Potenciando decisiones de alto impacto mediante datos</h3>
    <p>Desde el procesamiento de datos hasta la validación de modelos predictivos, transformo variables complejas en claridad operativa. Si buscas un arquitecto de datos que entienda el valor estratégico de la precisión técnica, hablemos.</p>
    <a href="/es/contact/" class="btn btn--primary">Contáctame</a>
  </div>
</div>