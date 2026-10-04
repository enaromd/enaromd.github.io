---
layout: page
title: "Acerca de mi"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: about/
lang: es

about:
  title: "Fundamentando la integridad de los datos de salud en la práctica clínica"
  p1: "Mi trabajo clínico refuerza una verdad sencilla: detrás de cada protocolo hay un rastro de datos, y detrás de cada dato hay una decisión médica de alta exigencia. La analítica en salud sufre cuando el código se escribe sin comprender la atención al pie de la cama del paciente."
  p2: "Cierro esa brecha combinando la experiencia clínica de primera línea con el diseño de bases de datos SQL y el modelado estadístico, convirtiendo registros de salud en bruto en métricas estandarizadas y validadas que mejoran los resultados en los pacientes."
  image: "/assets/images/about_squared.jpg"

features:
  - heading: "El arte de persuadir con evidencia"
    p1: "Obtener el Primer Lugar en la XV Jornada Científica SILAIS Granada validó una tesis central de mi trabajo: la metodología rigurosa solo tiene éxito cuando se combina con una comunicación clara."
    p2: "Este premio reconoció la traducción del análisis estadístico en una narrativa estructurada que brindó claridad e información accionable a quienes toman decisiones en salud pública."
    image: "/assets/images/about_story-1.jpeg"
    alt: "Persona leyendo en un sofá cómodo"
  - heading: "Las exigencias del campo impulsan la estructura"
    p1: "Operar en el entorno de alta presión de la brigada de cardiología 'Project Health for León' expuso una vulnerabilidad crítica en el flujo de trabajo: cómo clasificar (triage) de forma segura un volumen abrumador de pacientes bajo estrictas restricciones de tiempo."
    p2: "Este cuello de botella operacional me impulsó a desarrollar el Índice de Carga Medicamentosa (MBI), convirtiendo registros de medicamentos en bruto en un indicador subrogado del remodelado cardíaco."
    image: "/assets/images/about_story-2.jpeg"
    alt: "Personas leyendo libros en una biblioteca"
  - heading: "Traduciendo la complejidad en estrategia"
    p1: "Participar en la sesión de discusión técnica del Primer Congreso Occidental de Salud Materna y Neonatal destacó la necesidad del diálogo interdisciplinario."
    p2: "Mi rol se enfocó en navegar marcos inmunológicos complejos durante paneles interdisciplinarios para establecer claridad práctica e intencionada sobre el Síndrome Antifosfolípido en el Embarazo."
    image: "/assets/images/about_story-3.jpeg"
    alt: "Personas leyendo libros en una biblioteca"
      
skills_heading: "Principios fundamentales y filosofía analítica"
skills_description: "Combinando la práctica médica directa con el rigor cuantitativo para mitigar la distorsión de datos, reducir el sesgo sistemático y mejorar los resultados reales en los pacientes."
skills:
  - title: Evidencia sobre dogma
    icon: "fa-solid fa-stethoscope"
    one: "La intuición clínica genera hipótesis; los datos empíricos establecen la verdad."
    two: "Las decisiones deben basarse en evidencia cuantitativa verificable en lugar de hábitos o jerarquías. Esto nos permite diagnosticar mecanismos de datos faltantes, auditar flujos de trabajo y dejar que los datos dicten la solución."
  - title: Persuasión a través de la claridad
    icon: "fa-solid fa-database"
    one: "Los modelos bioestadísticos complejos son inútiles si los actores clave no pueden interpretarlos."
    two: "La verdadera influencia proviene de traducir conceptos complejos —como la heterogeneidad del efecto del tratamiento— en una comunicación transparente y lista para la toma de decisiones."
  - title: Sinergia interdisciplinaria
    icon: "fa-solid fa-chart-column"
    one: "Controlar el ego significa reconocer los límites de la formación clínica por sí sola."
    two: "Combinar la práctica clínica de primera línea con la ingeniería de bases de datos y el pensamiento sistémico genera pipelines de datos técnicamente sólidas y operacionalmente realistas."

cta:
  heading: "Conecta la realidad clínica de primera línea con la ejecución técnica"
  description: "La analítica efectiva en salud comienza por comprender cómo nacen los datos junto a la cama del paciente, incluyendo los caóticos flujos de trabajo y factores humanos que distorsionan los registros. Si tu equipo necesita a alguien que combine la perspectiva clínica con Python, SQL y bioestadística, pongámonos en contacto."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Contáctame"
    url: "contact/"
---

<style>
  .skill-cards-section {
    padding-top: 0 !important;
    margin-top: 0rem;
}
</style>

{% include about.html %}

{% include features-list.html%}

{% include skill-cards.html %}

{% include cta.html %}