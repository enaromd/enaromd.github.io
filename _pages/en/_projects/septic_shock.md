---
layout: page
title: "Evidence in Septic Shock"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/septic-shock/
lang: en

page_components:
  - type: "header"
    title: "Sepsis: From evidence in trials towards clinical workflows"
  
    bottom_line:
      label: "The Bottom Line"
      text: "The Bottom Line: The best scientific evidence is useless if it cannot be adopted by the front line. This synthesis rapidly <span class='highlight-metric'>translated complex ratios</span> from ANDROMEDA-SHOCK and CLOVERS <span class='highlight-metric'>into immediate, standardized operational agreements.</span>"

    tech_stack:
      label: "Core Strategies"
      items:
        - "Evidence-Based Medicine"
        - "Trial Synthesis"
        - "Workflow aligment"

  - type: "section"
    title: "The Challenge: Gaps Between Latest Trials and Clinical Bedside"
    content: "In the high-pressure environment of critical care, <strong>the gap between the publication of a major trial and its workflow implementation can cost lives.</strong> My objective was to effectively compress this timeline by synthesizing the precise data points needed for immediate clinical workflow adoption."

  - type: "skills"
    skills_heading: "Evidence Translation for Clinical Workflows"
    skills_description: "Deconstructing data from landmark critical care trials to map out actionable, high-visibility clinical triggers."
    skills:
      - title: Landmark Trials Curation
        icon: "assets/images/icons/selection.png"
        one: "I synthesized the design and results of randomized clinical trials, extracting the most important clinical endpoints for bedside implementation."

      - title: Operational Alignment
        icon: "assets/images/icons/analysis.png"
        one: "I achieved swift clinical alignment by engaging stakeholders with clear, evidence-driven visual hierarchies that reduced cognitive load."

      - title: Comorbidity-Driven Constraints
        icon: "assets/images/icons/effects.png"
        one: "I accounted for overlapping pathophysiological constraints, isolating inflection points where fluid titration must pivot to avoid volume overload."

  - type: "figure"
    heading: "Operationalizing Clinical Trial Evidence"
    description: "Contrasting trial methodology with localized medical context to extract high-yield decision milestones."
    image: "/assets/images/sepsis_evidence.jpg"
    alt: "Recommendation table based on the Surviving Sepsis Campaign."
    caption: "Table 1: Recommendation table based on the Surviving Sepsis Campaign for standardizing management within the first hour."

  - type: "results"
    cards:
      - title: "Stratified Alignment"
        description_1: "<span class='highlight-metric'>Translated multi-trial endpoints into clinical signals</span>, bridging foundational physiology for interns and advanced trial methodology for subspecialists during a joint institutional review."

      - title: "EBM Clinical Guidelines"
        description_1: "Evidence-driven, <span class='highlight-metric'>context-specific bedside workflows</span> for fluid resuscitation guidance by capillary refill and lactate, early initiation of vasopressors, and strategic use of corticosteroids."

      - title: "The Analyst’s Value"
        description_1: "Minimizing clinical variance and implementation latency by <span class='highlight-metric'>distilling high-dimensional trial data into structured bedside frameworks</span> for rapid, standardized execution."

  - type: "quote"
    text: "Evidence generation is only half the battle. Strategic deployment into clinical workflows is what ultimately saves lives."

  - type: "gallery"
    heading: "Visual Evidence"
    description: "A synthesis of clinical evidence for the standardization of Sepsis management."
    items:
      - image: "/assets/images/sepsis_01.jpg"
        alt: "ANDROMEDA-SHOCK Trial Summary"
        caption: "Effect of a Resuscitation Strategy Targeting Peripheral Perfusion Status vs Serum Lactate Levels."

      - image: "/assets/images/sepsis_02.jpg"
        alt: "ANDROMEDA-SHOCK Outcomes Table"
        caption: "Outcomes: Analysis of Hazard Ratios supporting the safety and efficacy of peripheral perfusion-guided resuscitation."

      - image: "/assets/images/sepsis_03.jpg"
        alt: "Balanced Crystalloids vs Saline"
        caption: "SALT-ED Trial evaluation of crystalloid vs saline outcomes in non-critically ill emergency patients."

      - image: "/assets/images/sepsis_04.jpg"
        alt: "Serum Electrolyte Concentration"
        caption: "Mean concentration trends of serum electrolytes across the initial 72 hours of resuscitation."

      - image: "/assets/images/sepsis_05.jpg"
        alt: "Heterogeneity of Treatment Effect"
        caption: "Subgroup analysis and forest plot demonstrating odds ratios for acute kidney injury."

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