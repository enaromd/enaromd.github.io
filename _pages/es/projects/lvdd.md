---
layout: splash
title: "Disfunción diastólica en hemodiálisis"
permalink: portfolio/projects/lvdd/
lang: es
# Social previews
description: "Superando las limitaciones muestrales en la enfermedad renal crónica terminal."
header:
  teaser: "/assets/images/lvdd_plot_pr.png"
# This block communicates directly with the SEO plugin
seo:
  type: "article"
  title: "Disfunción diastólica en hemodiálisis" # Repeat title here
  image: "/assets/images/presentation_sepsis.png"
# Sections
approach:
  - title: "Elevando los protocolos clínicos a través del mentoreo estadístico"
  - excerpt: "Rescatar un protocolo de investigación institucional requiere ir más allá de la recopilación de datos basales. Mi enfoque de asesoría se centró en guiar a los investigadores clínicos para ver más allá de los valores p y auditar visualmente las distribuciones de su cohorte subyacente."
results:
  - title: "Desenmascarando la magnitud del riesgo"
  - excerpt: "El protocolo auditado reveló que un alarmante <span class='highlight-metric'>72.5% de la cohorte en hemodiálisis sufría activamente de DDVD</span>. Al superar las limitaciones de una muestra pequeña y monocéntrica mediante un modelado robusto, mi mentoreo bioestadístico guió al equipo a extraer tamaños de efecto sin inflación."
---
<style>
.feature-divider {
  margin-top: 5rem;
  margin-bottom: 2rem;
}

.cta {
  margin-top: 5rem !important;
}

.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}
</style>

<div class="headline">
    <h1>Triaje cardiorrenal: Cuantificando razones de prevalencia robustas bajo sesgo de supervivencia</h1>
    <p><strong>En síntesis:</strong> Mediante el despliegue de un modelo de regresión de Poisson robusto para ajustar las restricciones muestrales monocéntricas, este análisis aisló a la <span class="highlight-metric">hipertensión crónica (RP ajustada: 2.22) y al control glucémico (RP ajustada: 1.16)</span> como los impulsores independientes dominantes de la insuficiencia cardíaca en hemodiálisis de mantenimiento, blindando la magnitud del riesgo.</p>
</div>

<div class="skills-bar">
    <p><strong>Estrategias centrales:</strong> Mitigación de sesgos, modelado de regresión robusto, control de confusión multivariado</p>
</div>

<h2>El desafío: Mortalidad cardiovascular silenciosa</h2>
<p>En pacientes sometidos a hemodiálisis de mantenimiento por enfermedad renal crónica (ERC) avanzada en estadio G5, <strong>la enfermedad cardiovascular se alza como la principal causa de mortalidad</strong>. La disfunción diastólica del ventrículo izquierdo (DDVD) representa un marcador temprano y silencioso de esta crisis cardiorrenal.</p>

<h2>Un sesgo que sobrevive</h2>
<p>Los conjuntos de datos transversales en salas de diálisis activas sufren inherentemente de <strong>sesgo de Neyman (sesgo de supervivencia)</strong>. Debido a que los pacientes cardiorrenales de mayor gravedad suelen fallecer o enfrentarse a hospitalizaciones de emergencia antes de que se capturen sus datos, los modelos estadísticos estándar terminan analizando a <strong>una cohorte de supervivientes artificialmente "estable".</strong></p>

<hr class="feature-divider">

{% include feature_row id="approach" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <img src="/assets/images/statistic.png" alt="Ícono: Visualización" class="grid-icon">
    <h3>Visualizando la Varianza oculta</h3>
    <p>Guié al equipo para desplegar <strong>visualizaciones de distribución</strong> con el fin de desenmascarar un patrón crítico que ninguna tabla de resumen podría revelar: una severa varianza de cola sesgada a la derecha con múltiples valores atípicos no controlados que alcanzaban hasta el 10% de HbA1c.</p> 
  </div>
  <div class="grid-item">
    <img src="/assets/images/selection.png" alt="'Ícono: Análisis" class="grid-icon">
    <h3>Pivote Analítico</h3>
    <p>Guié al equipo de investigación hacia un <strong>modelo de regresión de Poisson con varianza robusta</strong>, lo que les permitió calcular razones de prevalencia (RP) sin inflación que traducen con mayor precisión la magnitud clínica del riesgo.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/timeline.png" alt="Ícono: Secuencia" class="grid-icon">
    <h3>Regresiones Secuenciales</h3>
    <p>Estructuré una <strong>matriz de regresión multivariada de tres fases</strong>: modelos ajustados por demografía basal (edad/sexo), ruido nutricional/metabólico (IMC/albúmina) y una fase final de integración multisistémica.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}`

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/lvdd_plot_pr.png" alt="LVDD regression models" style="width: 100%; max-width: 900px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    Figura 1: Regresiones de Poisson multivariadas. Al sustituir los odds ratios logísticas inestables por estimadores de covarianza robustos de tipo sándwich, la metodología controla con éxito las restricciones muestrales severas ($N = 51$) sin sobresaturar los parámetros.
  </p>
</div>

<div class="project-grid">
  <div class="card">
    <h3>El impacto de la hipertensión</h3>
    <p><strong>La hipertensión crónica fue el impulsor clínico más agresivo.</strong> El modelo robusto mentoreado cuantificó un tamaño de efecto independiente masivo, dando como resultado una razón de prevalencia (RP) ajustada de 2.22, lo que más que duplicó la probabilidad de remodelado cardíaco avanzado.</p>
  </div>
  <div class="card">
    <h3>El impacto metabólico</h3>
    <p><strong>La desestabilización glucémica planteó una amenaza compuesta.</strong> Dejando atrás las limitaciones de las tablas agregadas, el modelo de regresión determinó que cada incremento del 1% en la HbA1c conllevaba un aumento continuo del 16% en el riesgo de prevalencia de DDVD (RP ajustada: 1.16).</p>
  </div>
  <div class="card">
    <h3>Estabilidad del modelo</h3>
    <p><strong>La arquitectura multivariada logró una alta estabilidad matemática.</strong> Esto se validó mediante una significación de Chi-cuadrado de la razón de verosimilitud de $p = 0.037$, demostrando que los controles de confusión secuenciales explicaron con éxito la varianza basal.</p>
  </div>
</div>

<div class="pull-quote">
  "El verdadero mentoreo bioestadístico no se trata de perseguir valores p; se trata de coachear a un equipo clínico para que <strong>reconozca dónde termina el ruido biológico y dónde comienza el riesgo real.</strong>"
</div>

<h2>Reflexiones: La metodología dicta la interpretación</h2>
<p>Guiar la capa bioestadística de este protocolo cardiorrenal solidificó un hecho del análisis sanitario: <strong>el modelado matemático ciego fracasa cuando se desconecta de la fisiopatología clínica.</strong> Rescatar este análisis requirió mentorear al equipo de investigación para mirar más allá de los resultados brutos del software estadístico y evaluar críticamente los compromisos biológicos dentro de su arquitectura de datos.</p>

<div class="project-grid">
  <div class="card">
    <h3>El efecto techo</h3>
    <p><strong>La patología universal destruye la varianza estadística.</strong> Los factores de riesgo cardiorrenal clásicos, como la anemia profunda, no lograron alcanzar significación porque son omnipresentes en pacientes con ERC en estadio G5. Coacheé al equipo para enfocarse en su lugar en impulsores volátiles y de alto impacto, como los cambios metabólicos.</p>
  </div>
  <div class="card">
    <h3>El compromiso de la vida útil del eritrocito</h3>
    <p><strong>La mecánica biológica distorsiona los endpoints brutos.</strong> La hemodiálisis destruye mecánicamente los glóbulos rojos, reduciendo artificialmente los valores brutos de HbA1c. Advertí al equipo que el aumento del 16% en el riesgo que descubrimos por unidad de HbA1c es un efecto sumamente conservador.</p>
  </div>
  <div class="card">
    <h3>Optimización futura</h3>
    <p><strong>Vencer el sesgo de supervivencia requiere un seguimiento longitudinal.</strong> Aunque nuestro modelo robusto de Poisson estabilizó con éxito esta captura transversal, el sesgo de Neyman sigue siendo una amenaza inherente. Por lo tanto, recomiendo un registro longitudinal que siga a las cohortes desde el primer día.</p>
  </div>
</div>

<div class="cta">
  <div style="text-align: center;">
    <h3>Transformemos tus ideas en acción</h3>
    <p>
      Los grandes avances nacen de la colaboración. Debido a mi compromiso con la precisión técnica y la narrativa de impacto, acepto un número limitado de proyectos para asegurar el rigor que cada desafío merece.
    </p>
    <p><strong>Si buscas convertir evidencia compleja en decisiones estratégicas, hablemos.</strong></p>
    <a href="contact/" class="btn btn--primary">Ponte en contacto</a>
  </div>
</div>