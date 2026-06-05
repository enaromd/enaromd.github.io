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
approach:
  - title: "Estructura del proyecto"
  - excerpt: "El pipeline se divide en tres etapas modulares y listas para producción con el fin de preservar un estricto linaje de datos y reproducibilidad:"
results:
  - title: "El Factor Impacto: Precisión Predictiva"
  - excerpt: "El modelo validó que un MBI > 5.25 identifica hipertensión pulmonar crítica con un 85% de precisión. Esta herramienta permite un 'triaje de recepción', priorizando a los pacientes con mayor beneficio de intervención y optimizando el recurso más escaso de la misión: el tiempo de los especialistas."
dashboard:
  - title: Estructura del dashboard y visualizaciones
  - excerpt: "Cada componente visual funciona como un filtro interactivo activo, permitiendo a los usuarios realizar exámenes cruzados de subcohortes de forma dinámica con solo hacer clic en segmentos de datos específicos."
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
  - url: "/assets/images/mbi_decomposed.jpg"
    image_path: "/assets/images/mbi_decomposed.jpg"
    alt: "Deconstrucción del Índice"
    title: "Un desglose visual de cómo las diferentes clases farmacológicas contribuyen al puntaje total de MBI en toda la cohorte."
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
    <h1>Cuantificando las brechas clínicas: MBI como sucedáneo <br>de remodelado cardíaco</h1>
    <p>Análisis de datos aplicada a la brigada cardiológica 2025 en León, Nicaragua.</p>
</div>

<div class="skills-bar">
    <strong>Tech Stack:</strong> Object-Oriented Programming (OOP), <code>Pandas</code>, <code>NumPy</code>, <code>Statsmodels</code>, <code>Scikit-learn</code>, <code>Matplotlib/Seaborn</code>
</div>

<h2>El corazón del análisis: ¿Qué es el 'Medication Burden Index' (MBI)?</h2>
<p>
  El <strong>MBI</strong> es un índice ponderado que cuantifica la intensidad del tratamiento farmacológico de un paciente. En lugar de solo contar cuántas pastillas toma una persona, el MBI evalúa el "esfuerzo" que el sistema cardiovascular está realizando bajo soporte médico.
</p>

<div class="math-block">
  $$MBI = \sum \left( \text{Peso} \times \frac{\text{DTD}}{\text{Dosis Máxima}} \right)$$
</div>

<p>Para lograr este cálculo, el motor procesa dos variables críticas:</p>

<ul>
  <li><strong>Dosis Total Diaria (DTD):</strong> Es la sumatoria de miligramos que el paciente consume en 24 horas. Por ejemplo, un paciente con Furosemida 40mg cada 12h tiene un $DTD = 80mg$.</li>
  <li><strong>Pesos Clínicos:</strong> El código asigna pesos mayores (e.j. $3.0$) a diuréticos de asa y vasodilatadores pulmonares, y pesos menores ($0.5$) a estatinas o fármacos de mantenimiento.</li>
</ul>

<p>
  Esta arquitectura permite que el MBI actúe como un <strong>sucedáneo de severidad hemodinámica</strong>, capturando la señal de falla cardíaca antes de que el paciente llegue al ecocardiógrafo.
</p>

<h3>Lógica de Ponderación: Pesos clínicos</h3>
<p>
  No todos los fármacos indican la misma gravedad. El código asigna un peso específico basado en la severidad de la condición que tratan, priorizando señales de remodelación cardíaca:
</p>

<div class="table-container">
  <table class="mbi-table" style="width: 65%; border: 1px solid #ddd;">
    <thead>
      <tr style="background-color: #003152; color: white;">
        <th style="padding: 12px; border: 1px solid #ddd;">Peso</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Prioridad</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Clases de Medicación</th>
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
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Alta</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Inhibidores RAAS, Beta-bloqueadores, SGLT2.</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>1.0</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Moderada</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Anticoagulantes, Calcioantagonistas.</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;"><strong>0.5</strong></td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">Mantenimiento</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">Estatinas, Fármacos metabólicos.</td>
      </tr>
    </tbody>
  </table>
</div>

<h2>El Reto: El "Silencio de los Normales" (Sesgo MNAR)</h2>
<p>En misiones de alto volumen, los datos suelen ser incompletos: los cardiólogos enfocaron la velocidad de ejecución en la patología crítica, dejando los campos para estructuras sanas completamente en blanco. Esto genera un sesgo de <strong>Missing Not At Random (MNAR)</strong> que exhibe una media de $\text{RVSP}$ fuertemente distorsionada de $51.0\text{ mmHg}$, omitiendo por completo el espectro basal saludable.</p>

<hr class="feature-divider">

{% include feature_row id="approach" type="center" %}

<div class="grid-container">
  <div class="grid-item">
      <img src="/assets/images/data_management.png" alt="Icono: Procesamiento de Datos" class="grid-icon">
      <h3>Extracción & Mitigación de Sesgo</h3>
      <p>Construcción de un modelo de Imputación Gausiana de 'Normalidad Natural' basado en evidencia utilizando las pautas de la Sociedad Americana de Ecocardiografía para restaurar la verdadera varianza poblacional.</p>
  </div>
  <div class="grid-item">
      <img src="/assets/images/data_architecture.png" alt="Icono: Arquitectura Clínica" class="grid-icon">
      <h3>Ingeniería de Esquema 3NF</h3>
      <p>Diseño y despliegue de una estructura de base de datos MySQL robusta. Las matrices fragmentadas de polifarmacia se normalizaron en un modelo de base de datos estrictamente relacional.</p>
  </div>
  <div class="grid-item">
      <img src="/assets/images/statistic.png" alt="Icono: Validación Estadística" class="grid-icon">
      <h3>Mapeo de Residuos OLS</h3>
      <p>Cálculo de residuos de regresión por Mínimos Cuadrados Ordinarios (OLS) para aislar a los pacientes cuya patología subyacente grave está siendo enmascarada activamente por terapias intensivas.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/mbi_triage.png" alt="Distribución MBI y Zonas de Triaje" style="width: 100%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    Figura 1: Correlación entre el MBI y la severidad hemodinámica. Se aprecian las tres zonas operativas de triaje validadas.
  </p>
</div>

<div class="project-grid">
  <div class="card">
    <h3>La Zona clave</h3>
    <p>Identificación de la <strong>Zona 2 (MBI 4.0 - 5.5)</strong>: pacientes con patología mixta que obtienen el mayor beneficio del recambio valvular.</p>
  </div>
  <div class="card">
    <h3>Poder Predictivo</h3>
    <p>AUC de <strong>0.73/0.82</strong> para detectar compromiso hemodinámico. El MBI actúa como un "Ecocardiograma Químico" preliminar.</p>
  </div>
  <div class="card">
    <h3>Eficiencia Operativa</h3>
    <p>Reducción de la carga en estaciones de diagnóstico al priorizar pacientes en <strong>Agotamiento Farmacológico</strong> (MBI > 5.5).</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="dashboard" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/mbi_dashboard.png" alt="MBI Distribution and Triage Zones" style="width: 45%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
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