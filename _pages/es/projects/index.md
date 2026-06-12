---
layout: splash
title: "Proyectos"
permalink: portfolio/projects/
lang: es
# Social previews
description: "Mis proyectos no son solo un resumen de mi trabajo; son un testimonio de mi dedicación para lograr resultados de alto impacto."
# Header 
header:
  overlay_filter: rgba(0, 19, 32, 0.8)
  overlay_image: /assets/images/splash-projects.jpg
  teaser: "/assets/images/splash-projects.jpg"
excerpt: 'Mis proyectos no son solo un resumen de mi trabajo; son un testimonio de mi dedicación para lograr resultados de alto impacto. <br>A través de cada análisis, mi objetivo es asegurar que los datos no solo sean correctos, sino que cuenten una historia convincente y respaldada por evidencia, capaz de inspirar la acción y la innovación'  
seo:
  type: "article"
  title: "Projects" # Repeat title here
  image: "/assets/images/splash-projects.jpg"
presentations:
  - title: "Presentaciones y mentoría"
data:
  - title: "Datos y bases de datos"
---

<!-- Adds top margin to the feature divider -->
<style>
.feature-divider {
  margin-top: 5rem;
  margin-bottom: 2rem;
}

.cta {
  margin-top: 5rem !important;
}
</style>

{% include feature_row id="data" type="center" %}
<!-- Projects columns -->
<div class="grid-container">
  <div class="grid-item">
    <a href="mbi/">
      <img src="/assets/images/mbi_triage.png" alt="Proyecto: Cardio-MBI-Triage-Engine">
      <h3>Índice de Carga Farmacológica (MBI)</h3>
      <p>Diseño de un pipeline de datos clínicos con esquemas 3NF/Snowflake e imputación 'natural normal' para superar la pérdida estructural de datos en una brigada cardiológica de 10 días.</p>
      <p><strong>Impacto:</strong> Clasifica al 25.7% de los pacientes de alta agudeza en zonas de intervención de alto beneficio bajo severas restricciones de campo.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="little-lemon-db/">
      <img src="/assets/images/database_schema.png" alt="Proyecto: Little Lemon DB">
      <h3>Base de Datos Relacional e Integración Python-SQL</h3>
      <p>Ingeniería de un ecosistema 3NF y un puente programático para automatizar operaciones de restaurante complejas.</p>
      <p><strong>Impacto:</strong> 100% de integridad transaccional y eliminación de redundancia mediante procedimientos almacenados.</p>
    </a>
  </div>
</div>

{% include feature_row id="presentations" type="center" %}

<!-- Projects columns -->
<div class="grid-container">
  <div class="grid-item">
    <a href="lvdd/">
      <img src="/assets/images/lvdd_plot_pr.png" alt="Proyecto: DDVI en Hemodiálisis">
      <h3>Disfunción Diastólica en Hemodiálisis de Mantenimiento</h3>
      <p>Aplcación de regresiones de Poisson multivariadas con estimadores de covarianza robustos de tipo sándwich para neutralizar las limitaciones muestrales.</p>
      <p><strong>Impacto:</strong> Identificación de la hipertensión arterial crónica (PR: 2.22) como el principal factor impulsor de la falla cardíaca en hemodiálisis.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="sepsis/">
      <img src="/assets/images/presentation_sepsis.png" alt="Proyecto: Adaptación en Sepsis">
      <h3>Operacionalización de Evidencia Clínica en Choque Séptico</h3>
      <p>Desfragmentando datos complejos de ensayos clínicos (ANDROMEDA-SHOCK, CLOVERS, SMART) en flujos de trabajo locales a la cabecera del paciente para minimizar la latencia terapéutica.</p>
      <p><strong>Impacto:</strong> Reducción de la variabilidad clínica mediante marcos estandarizados de consenso basados en datos para cuidados críticos.</p>
    </a>
  </div>
  <div class="grid-item">
    <a href="pharmacovigilance/">
      <img src="/assets/images/project_pharmacovigilance.png" alt="Proyecto: XV Jornada Científica">
      <h3>Farmacovigilancia y narrativa clínica</h3>
      <p>Caracterización de reacciones adversas (RAM) mediante algoritmos de causalidad de la OMS y diseño de narrativa visual.</p>
      <p><strong>Impacto:</strong> Primer lugar SILAIS 2023 por excelencia en comunicación científica de alto impacto.</p>
    </a>
  </div>
</div>


<!-- CTA section -->
<div class="cta">
  <div>
    <h3>Transformemos tus ideas en acciones</h3>
    <p>
      Creo firmemente que <strong>los grandes descubrimientos nacen de la colaboración y la visión compartida</strong>. 
      Debido a mi compromiso con la precisión técnica, acepto un número limitado de desafíos en paralelo, 
      asegurando que cada proyecto reciba el rigor y la profundidad que merece.
    </p>
    <p>
      <strong>Si estás listo para convertir datos en acciones, me encantaría escuchar tu propuesta.</strong>
    </p>
    <a href="/es/contact/" class="btn btn--primary">Contáctame</a>
  </div>
</div>