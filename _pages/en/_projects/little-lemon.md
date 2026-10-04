---
layout: page
title: "Relational Database Engineering"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/little-lemon/
lang: en

page_components:
  - type: "header"
    title: "End-to-End MySQL Engineering: Synthetic Data to Validated Reporting"
  
    bottom_line:
      label: "The Bottom Line"
      text: "The Bottom Line: Before data can be safely analyzed, it must be relational. This project demonstrates the <span class='highlight-metric'>end-to-end engineering of a clean relational database</span>—from Faker-driven synthetic generation to strict 3NF normalization and programmatic Python ETL bridging."

    tech_stack:
      label: "Core Strategies"
      items:
        - 3NF Relational Modeling
        - MySQL
        - Stored Procedures
        - MySQL Connector/Python
        - Tableau
        - Faker

  - type: "section"
    title: "The Root Problem: Relational Fragmentation"
    content: "In transactional systems, <strong>poor table organization and a lack of explicit constraints introduce massive operational vulnerabilities.</strong> Relying on non-normalized structures creates an environment where a single update can trigger cascading data anomalies, destroying the database's reliability before any analytical tool can even connect to it."

  - type: "section"
    title: "The Structural Risk: Cascading Redundancy"
    content: "When database schema boundaries are blurred, duplication scales exponentially. <strong>Without server-side validation</strong> to block conflicting inputs or overlapping booking states, <strong>the underlying system quietly corrupts its own records.</strong> For any downstream business intelligence platform or dashboard, this is fatal: visualizing un-normalized tables results in flawed metrics and distorted operational logic."

  - type: "skills"
    skills_heading: "The Engineering Workflow"
    skills_description: "Decomposing operational models into specialized relational tables to guarantee transactional consistency."
    skills:
      - title: Schema Engineering
        icon: "assets/images/icons/data_schema.png"
        one: "Designing a <strong>Third Normal Form (3NF) relational model</strong> to mathematically eliminate data redundancy."

      - title: Probabilistic Generation
        icon: "assets/images/icons/data_population.png"
        one: "Deploying <strong>Python's Faker library to simulate</strong> production-ready datasets that mirror <strong>real-world variance.</strong>"

      - title: Transaction Security
        icon: "assets/images/icons/data_transaction.png"
        one: "Deploying <strong>Stored Procedures to</strong> automate logic checks and <strong>secure transactions</strong> against data corruption."

  - type: "figure"
    heading: "The Execution Factor: From Storage to Strategy"
    description: "The success of this structure lies in its ability to convert a static database into a dynamic operational asset. By bridging Python automation with SQL logic, I established a system where data is not just stored, but actively managed to ensure 100% transaction integrity"
    image: "/assets/images/project_lemon_database_schema.png"
    alt: "Recommendation table based on the Surviving Sepsis Campaign."
    caption: "Figure 1: Database schema that implements 3rd Normal Form (3NF)"

  - type: "results"
    cards:
      - title: "Zero Redundancy"
        description_1: "Validated a complete 3NF schema deployment, entirely removing update anomalies across all tables."

      - title: "Procedural Immunity"
        description_1: "Validated a complete 3NF schema deployment, entirely removing update anomalies across all tables."

      - title: "Intelligence translation"
        description_1: "Enforced ACID-compliant stored procedures, neutralizing simultaneous transaction conflicts at the server layer."

  - type: "quote"
    text: "A database is more than a container; it is the structural integrity that allows data to transition into actionable intelligence."

  - type: "flexible_content"
    heading: "Reflections: The Relational Imperative"
    blocks:
      - type: "paragraph"
        text: "While this project models commercial transactions, the technical execution directly maps to the rigorous standards required in health informatics and Real-World Evidence (RWE): <strong>data tables must remain structurally sound to prevent the upstream duplication errors that frequently compromise observational study cohorts.</strong>"

      - type: "callout"
        lead: "Key Takeaway:"
        text: "The exact same 3NF constraints implemented here to prevent a transactional double-booking are the operational mechanisms required to eliminate duplicate patient enrollment identifiers within clean analytical registries."

      - type: "paragraph"
        text: "Although relying on Python's Faker engine successfully provided high-volume inputs to stress-test these schema limits, synthetic distributions naturally lack the messy, erratic data anomalies common to organic entry. A valuable next iteration will intentionally inject edge-case malformations into the generation script to test the database's automated rejection mechanisms under hostile, unpredictable transactional loads."

  - type: "gallery"
    heading: "Visual Milestones"
    description: "A visual walk-through of the database lifecycle: from ERD schema design and Faker ingestion to the final Tableau reporting layer"
    items:
      - image: "/assets/images/meta_procedure.jpg"
        alt: "Stored procedure"
        caption: "Encapsulating complex business logic within the MySQL backend to automate routine management tasks."

      - image: "/assets/images/meta_connection.jpg"
        alt: "MYSQL-Python connection"
        caption: "Establishing a secure link between Python and MySQL using MySQL Connector/Python for programmatic backend management."

      - image: "/assets/images/meta_insertion.jpg"
        alt: "Data population with Faker library"
        caption: "Automated data population utilizing the Python Faker library to simulate production-ready datasets with probabilistic logic."

      - image: "/assets/images/meta_validation.jpg"
        alt: "Serum Electrolyte Concentration"
        caption: "Demonstrating the database’s self-correcting logic when faced with invalid or conflicting operational inputs."

      - image: "/assets/images/meta_execution.jpg"
        alt: "Execution through Jupyter notebook"
        caption: "Executing backend SQL logic through a Jupyter interface, demonstrating the full integration of the engineering stack."

  - type: "button"
    text: "Check README on GitHub"
    url: "https://github.com/enaromd/db-capstone-project"
    icon: "github"
    align: "center"

cta:
  heading: "Bridge Frontline Clinical Reality with Technical Execution"
  description: "Effective healthcare analytics starts with knowing how data is born at the bedside—including the hectic workflows and human factors that warp raw records. If your team needs someone who combines frontline clinical perspective with Python, SQL, and biostatistics, let’s connect."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Get in touch"
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