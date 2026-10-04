---
layout: page
title: "Ingeniería de Bases de Datos Relacionales"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/little-lemon/
lang: es

page_components:
  - type: "header"
    title: "Ingeniería End-to-End en MySQL: De Datos Sintéticos a Reportes Validados"
  
    bottom_line:
      label: "Conclusión Clave"
      text: "Conclusión Clave: Antes de que los datos puedan analizarse de forma segura, deben ser relacionales. Este proyecto demuestra la <span class='highlight-metric'>ingeniería end-to-end de una base de datos relacional limpia</span>, desde la generación sintética impulsada por Faker hasta la normalización estricta en 3NF y el puente programático ETL con Python."

    tech_stack:
      label: "Estrategias Clave"
      items:
        - Modelado Relacional 3NF
        - MySQL
        - Procedimientos Almacenados
        - MySQL Connector/Python
        - Tableau
        - Faker

  - type: "section"
    title: "El Problema de Raíz: Fragmentación Relacional"
    content: "En los sistemas transaccionales, <strong>la deficiente organización de las tablas y la falta de restricciones explícitas introducen vulnerabilidades operativas masivas.</strong> Depender de estructuras no normalizadas crea un entorno donde una sola actualización puede desencadenar anomalías de datos en cascada, destruyendo la confiabilidad de la base de datos antes de que cualquier herramienta analítica pueda siquiera conectarse a ella."

  - type: "section"
    title: "El Riesgo Estructural: Redundancia en Cascada"
    content: "Cuando los límites del esquema de la base de datos se desdibujan, la duplicación se escala exponencialmente. <strong>Sin una validación del lado del servidor</strong> para bloquear entradas conflictivas o estados de reserva superpuestos, <strong>el sistema subyacente corrompe silenciosamente sus propios registros.</strong> Para cualquier plataforma o panel de inteligencia de negocios descendente, esto es fatal: visualizar tablas no normalizadas resulta en métricas defectuosas y una lógica operativa distorsionada."

  - type: "skills"
    skills_heading: "El Flujo de Trabajo de Ingeniería"
    skills_description: "Descomposición de modelos operativos en tablas relacionales especializadas para garantizar la consistencia transaccional."
    skills:
      - title: Ingeniería de Esquema
        icon: "assets/images/icons/data_schema.png"
        one: "Diseño de un <strong>modelo relacional en Tercera Forma Normal (3NF)</strong> para eliminar matemáticamente la redundancia de datos."

      - title: Generación Probabilística
        icon: "assets/images/icons/data_population.png"
        one: "Uso de la <strong>librería Faker de Python para simular</strong> conjuntos de datos listos para producción que reflejan la <strong>varianza del mundo real.</strong>"

      - title: Seguridad Transaccional
        icon: "assets/images/icons/data_transaction.png"
        one: "Implementación de <strong>Procedimientos Almacenados para</strong> automatizar verificaciones lógicas y <strong>proteger las transacciones</strong> contra la corrupción de datos."

  - type: "figure"
    heading: "El Factor de Ejecución: Del Almacenamiento a la Estrategia"
    description: "El éxito de esta estructura radica en su capacidad para convertir una base de datos estática en un activo operativo dinámico. Al conectar la automatización en Python con la lógica SQL, establecí un sistema donde los datos no solo se almacenan, sino que se gestionan activamente para garantizar un 100% de integridad transaccional."
    image: "/assets/images/project_lemon_database_schema.png"
    alt: "Tabla de recomendación basada en la Campaña Sobrevivir a la Sepsis."
    caption: "Figura 1: Esquema de base de datos que implementa la Tercera Forma Normal (3NF)"

  - type: "results"
    cards:
      - title: "Redundancia Cero"
        description_1: "Validación de un despliegue completo del esquema 3NF, eliminando totalmente las anomalías de actualización en todas las tablas."

      - title: "Inmunidad Procedimental"
        description_1: "Aplicación de procedimientos almacenados compatibles con ACID, neutralizando conflictos de transacciones simultáneas en la capa del servidor."

      - title: "Traducción de Inteligencia"
        description_1: "Conversión de datos relacionales validados en tableros interactivos de Tableau para reportes analíticos precisos."

  - type: "quote"
    text: "Una base de datos es más que un contenedor; es la integridad estructural que permite que los datos se transformen en inteligencia accionable."

  - type: "flexible_content"
    heading: "Reflexiones: El Imperativo Relacional"
    blocks:
      - type: "paragraph"
        text: "Aunque este proyecto modela transacciones comerciales, la ejecución técnica se mapea directamente a los rigurosos estándares requeridos en la informática de la salud y la Evidencia en el Mundo Real (RWE): <strong>las tablas de datos deben mantenerse estructuralmente sólidas para prevenir los errores de duplicación ascendentes que frecuentemente comprometen las cohortes de estudios observacionales.</strong>"

      - type: "callout"
        lead: "Conclusión Clave:"
        text: "Las mismas restricciones 3NF implementadas aquí para evitar una doble reserva transaccional son los mecanismos operativos necesarios para eliminar identificadores duplicados de inscripción de pacientes en registros analíticos limpios."

      - type: "paragraph"
        text: "Aunque confiar en el motor Faker de Python proporcionó con éxito un alto volumen de entradas para probar los límites del esquema, las distribuciones sintéticas carecen naturalmente de las anomalías de datos caóticas e impredecibles comunes en la entrada orgánica. Una valiosa iteración futura consistirá en inyectar intencionalmente malformaciones de casos límite en el script de generación para probar los mecanismos de rechazo automatizados de la base de datos bajo cargas transaccionales hostiles e impredecibles."

  - type: "gallery"
    heading: "Hitos Visuales"
    description: "Un recorrido visual por el ciclo de vida de la base de datos: desde el diseño del esquema ERD y la ingesta con Faker hasta la capa final de reportes en Tableau"
    items:
      - image: "/assets/images/meta_procedure.jpg"
        alt: "Procedimiento almacenado"
        caption: "Encapsulamiento de lógica de negocios compleja en el backend de MySQL para automatizar tareas de gestión rutinarias."

      - image: "/assets/images/meta_connection.jpg"
        alt: "Conexión MySQL-Python"
        caption: "Establecimiento de un enlace seguro entre Python y MySQL utilizando MySQL Connector/Python para la gestión programática del backend."

      - image: "/assets/images/meta_insertion.jpg"
        alt: "Población de datos con la librería Faker"
        caption: "Población automatizada de datos utilizando la librería Faker de Python para simular conjuntos de datos listos para producción con lógica probabilística."

      - image: "/assets/images/meta_validation.jpg"
        alt: "Concentración de Electrólitos Séricos"
        caption: "Demostración de la lógica de autocorrección de la base de datos al enfrentarse a entradas operativas inválidas o conflictivas."

      - image: "/assets/images/meta_execution.jpg"
        alt: "Ejecución a través de Jupyter notebook"
        caption: "Ejecución de la lógica SQL del backend a través de una interfaz de Jupyter, demostrando la integración completa del stack de ingeniería."

  - type: "button"
    text: "Ver README en GitHub"
    url: "https://github.com/enaromd/db-capstone-project"
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