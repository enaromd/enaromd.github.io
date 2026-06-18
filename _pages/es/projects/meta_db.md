---
layout: splash
title: "Base de datos relacional e integración MySQL-Python"
permalink: portfolio/projects/little-lemon-db/
lang: es
# Social previews
description: "Ingeniería de una base de datos relacional 3NF e integración Python-SQL para la gestión operativa."
header:
  teaser: "/assets/images/database_schema.png"
# This block communicates directly with the SEO plugin
seo:
  type: "article"
  title: "Base de datos relacional e integración MySQL-Python" # Repeat title here
  image: "/assets/images/database_schema.png"
# Sections
approach:
  - title: "El flujo de trabajo de ingeniería"
  - excerpt: "Descomposición de modelos operativos en tablas relacionales especializadas para garantizar la consistencia transaccional."
results:
  - title: "El factor de ejecución: del almacenamiento a la estrategia"
  - excerpt: "El éxito de esta estructura radica en su capacidad para convertir una base de datos estática en un activo operativo dinámico. Al conectar la automatización de Python con la lógica de SQL, establecí un sistema donde los datos no solo se almacenan, sino que se gestionan activamente para garantizar un 100% de integridad transaccional."
highlights_title: 
  - title: "Hitos de ingeniería"
  - excerpt: "Un recorrido visual por el ciclo de vida de la base de datos: desde el diseño del esquema ERD y la ingesta con Faker hasta la capa final de reportes en Tableau."
highlights:
  - url: "/assets/images/meta_procedure.jpg"
    image_path: "/assets/images/meta_procedure.jpg"
    alt: "Stored procedures"
    title: "Encapsulación de lógica de negocio compleja dentro del backend de MySQL para automatizar tareas de gestión rutinarias."
  - url: "/assets/images/meta_connection.jpg"
    image_path: "/assets/images/meta_connection.jpg"
    alt: "Execution bridge"
    title: "Establecimiento de un enlace seguro entre Python y MySQL utilizando <code>MySQL Connector/Python</code> para la gestión programática del backend."
  - url: "/assets/images/meta_insertion.jpg"
    image_path: "/assets/images/meta_insertion.jpg"
    alt: "Ingestion engine"
    title: "Población automatizada de datos utilizando la librería <code>Faker</code> de Python para simular conjuntos de datos listos para producción con lógica probabilística."
  - url: "/assets/images/meta_validation.jpg"
    image_path: "/assets/images/meta_validation.jpg"
    alt: "Integrity guard"
    title: "Demostración de la lógica autocorrectiva de la base de datos al enfrentarse a entradas operativas inválidas o en conflicto."
  - url: "/assets/images/meta_execution.jpg"
    image_path: "/assets/images/meta_execution.jpg"
    alt: "The bridge in Action"
    title: "Ejecución de la lógica SQL del backend a través de una interfaz de Jupyter, demostrando la integración completa del stack de ingeniería."
  - url: "/assets/images/meta_dashboard.jpg"
    image_path: "/assets/images/meta_dashboard.jpg"
    alt: "Actionable analytics"
    title: "Conversión de registros de bases de datos sin procesar en insights estratégicos, permitiendo a los interesados visualizar el rendimiento operativo de un vistazo."
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

.highlight-metric {
    color: #b80f0a; /* Deep clinical red */
    font-weight: 600; /* Optional: gives the metric a tiny bit more structural weight */
}
</style>

<div class="headline">
    <h1>Ingeniería de MySQL de extremo a extremo: de datos sintéticos a reportes validados</h1>
    <p><strong>En Síntesis':</strong> Antes de que los datos puedan ser analizados de forma segura, deben ser relacionales. Este proyecto demuestra la <span class="highlight-metric">ingeniería de extremo a extremo de una base de datos relacional limpia</span>, desde la generación sintética impulsada por Faker hasta una estricta normalización 3NF y el puenteado ETL programático con Python.</p>
</div>

<div class="skills-bar">
    <p><strong>Stack tecnológico:</strong> Modelado relacional 3NF, MySQL, Procedimientos almacenados, MySQL Connector/Python, Tableau, Faker</p>
</div>

<h2>El problema de raíz: Fragmentación relacional</h2>
<p>En los sistemas transaccionales, <strong>una mala organización de las tablas y la falta de restricciones explícitas introducen vulnerabilidades operativas masivas</strong>. Depender de estructuras no normalizadas crea un entorno donde una sola actualización puede desencadenar anomalías de datos en cascada, destruyendo la confiabilidad de la base de datos antes de que cualquier herramienta analítica pueda siquiera conectarse a ella.</p>

<h2>El riesgo estructural: Redundancia en cascada</h2>
<p>Cuando los límites del esquema de la base de datos se desdibujan, la duplicación escala exponencialmente. <strong>Sin una validación en el lado del servidor</strong> que bloquee entradas en conflicto o estados de reserva superpuestos, <strong>el sistema subyacente corrompe silenciosamente sus propios registros</strong>. Para cualquier plataforma o dashboard de inteligencia de negocios downstream, esto es fatal: la visualización de tablas no normalizadas da como resultado métricas erróneas y una lógica operativa distorsionada.</p>

<hr class="feature-divider">

{% include feature_row id="approach" type="center" %}

<div class="grid-container">
  <div class="grid-item">
      <img src="/assets/images/data_schema.png" alt="Icon: Schema Design" class="grid-icon">
      <h3>Ingeniería de esquemas</h3>
      <p>Diseño de un <strong>modelo relacional de Tercera Forma Normal (3NF)</strong> para eliminar matemáticamente la redundancia de datos.</p>
  </div>
  <div class="grid-item">
      <img src="/assets/images/data_population.png" alt="Icon: Data Processing" class="grid-icon">
      <h3>Generación probabilística</h3>
      <p>Despliegue de la <strong>librería Faker de Python para simular</strong> conjuntos de datos listos para producción que reflejan la <strong>varianza del mundo real.</strong></p>
  </div>
  <div class="grid-item">
      <img src="/assets/images/data_transaction.png" alt="Icon: Transaction Security" class="grid-icon">
      <h3>Seguridad transaccional</h3>
      <p>Despliegue de <strong>procedimientos almacenados para</strong> automatizar las comprobaciones lógicas y <strong>asegurar las transacciones</strong> contra la corrupción de datos.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/database_schema.png" alt="Database schema in 3NF" style="width: 100%; max-width: 750px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    Figura 1: Esquema de base de datos que implementa la Tercera Forma Normal (3NF)
  </p>
</div>

<div class="project-grid">
  <div class="card">
    <h3>Cero redundancia</h3>
    <p>Validación de un <strong>despliegue completo de esquema 3NF</strong>, eliminando por completo las anomalías de actualización en todas las tablas.</p>
  </div>
  <div class="card">
    <h3>Inmunidad procedimental</h3>
    <p>Aplicación de <strong>procedimientos almacenados conformes con ACID</strong>, neutralizando los conflictos de transacciones simultáneas en la capa del servidor.</p>
  </div>
  <div class="card">
    <h3>Traducción analítica</h3>
    <p>Envío de salidas de consultas perfectamente limpias y <strong>normalizadas a Tableau</strong>, creando una fuente única de verdad precisa.</p>
  </div>
</div>

<div class="pull-quote">
  "Una base de datos es más que un contenedor; es la <strong>integridad estructural</strong> que permite que los datos se transformen en inteligencia accionable."
</div>

<h2>Reflexiones: El imperativo relacional</h2>
<p>Aunque este proyecto modela transacciones comerciales, la ejecución técnica se mapea directamente con los rigurosos estándares requeridos en la informática de la salud y la evidencia del mundo real (RWE): <strong>las tablas de datos deben permanecer estructuralmente sólidas para evitar los errores de duplicación upstream que frecuentemente comprometen las cohortes de estudios observacionales.</strong></p>

<blockquote>
  <strong>Conclusión clave:</strong> Las exactas mismas restricciones 3NF implementadas aquí para evitar una doble reserva transaccional son los mecanismos operativos requeridos para eliminar identificadores duplicados de inscripción de pacientes dentro de registros analíticos limpios.
</blockquote>

<p>Aunque depender del motor <code>Faker</code> de Python proporcionó con éxito entradas de gran volumen para poner a prueba los límites del esquema, las distribuciones sintéticas carecen naturalmente de las anomalías de datos desordenadas y erráticas comunes en la entrada orgánica. Una próxima iteración valiosa inyectará intencionalmente malformaciones de casos extremos en el script de generación para evaluar los mecanismos de rechazo automatizados de la base de datos bajo cargas transaccionales hostiles e impredecibles.</p>

<hr class="feature-divider">

{% include feature_row id="highlights_title" type="center" %}

{% include gallery id="highlights" %}

<div class="see-more-button">
  <a href="https://github.com/enrodri/db-capstone-project" class="btn btn--primary">Ver repositorio completo</a>
</div>

<div class="cta">
  <div style="text-align: center;">
    <h3>Construyamos los cimientos de tus datos</h3>
    <p>Ya sea investigación clínica u operaciones comerciales, un proyecto es solo tan fuerte como su base de datos. Me especializo en construir los puentes que mantienen tus datos limpios, rápidos y accesibles.</p>
    <a href="contact/" class="btn btn--primary">Ponte en contacto</a>
  </div>
</div>