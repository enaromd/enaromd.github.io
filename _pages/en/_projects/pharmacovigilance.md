---
layout: page
title: "Pharmacovigilance in Hypertension"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/pharmacovigilance/
lang: en

page_components:
  - type: "header"
    title: "The Economics of Choice: Visualizing Therapeutic Failure"
  
    bottom_line:
      label: "The Bottom Line"
      text: "The Bottom Line: At the XV Scientific Fair, 17 clinical presentations delivered static data. This project took a different path. By fusing strict WHO causality algorithms with behavioral risk-reframing, we exposed how so-called <span class='highlight-metric'>translated complex ratios</span> from ANDROMEDA-SHOCK and CLOVERS <span class='highlight-metric'>'mild' side effects secretly drive a 50% treatment dropout rate.</span>"

    tech_stack:
      label: "Core Strategies"
      items:
        - " Algorithmic Causality"
        - "Persuasive Storytelling"
        - "Visual Hierarchy"

  - type: "section"
    title: 'The Challenge: The Cognitive Trap of "Mild" Data"'
    content: 'In pharmacovigilance, data is often ignored if it lacks catastrophic severity. Our registry analysis revealed that <strong>57.1% of adverse drug reactions were classified as "mild"</strong>. For front-line clinicians, this triggers a cognitive heuristic: mild means harmless. However, this exact "harmless" friction is <strong>responsible for a 50% therapeutic dropout rate</strong> in chronic hypertensive patients. The objective was to structure a presentation that shattered this cognitive bias.'

  - type: "skills"
    skills_heading: "From Data to Algorithmic Standarization"
    skills_description: "Applying the WHO Causality Algorithm to validate signals, preventing data from being dismissed as clinical noise."
    skills:
      - title: Terms Standarization
        icon: "assets/images/icons/data_management.png"
        one: "Mapped active medical problems using the CIE-10 index and categorized all consumed medications according to the Anatomical Therapeutical Chemistry (ATC) framework."

      - title: Algorithmic Causality
        icon: "assets/images/icons/selection.png"
        one: "Processed raw symptom data through the WHO Causality Assessment Algorithm to objectively verify the relationship between drug exposure and adverse events."

      - title: Drug Reaction Risk Classification
        icon: "assets/images/icons/risk.png"
        one: "Applied the modified Rawlins & Thompson classification system to differentiate between predictable, dose-dependent reactions and unpredictable anomalies."

  - type: "figure"
    heading: "The Victory Factor: Standing Out"
    description: "In a crowded field of 17 scientific presentations, this behavioral-first visual hierarchy brought to light that seemingly minor adverse reactions directly trigger massive therapeutic abandonment."
    image: "/assets/images/cover_project_presention_pharmacovigilance.png"
    alt: "Strategic Trigger"
    caption: "Figure 1: Design oriented to highlight the direct link between adverse drug reactions (ADR) and therapeutic failure in active pharmacovigilance."

  - type: "results"
    cards:
      - title: "The Abandonment Threshold"
        description_1: "Identified that <span class='highlight-metric'>50% of patients</span> who presented an adverse reaction to antihypertensive medications entirely suspended their consumption."

      - title: 'The "Mild" Paradox'
        description_1: "Discovered that <span class='highlight-metric'>71.4% of documented reactions were Type A</span> according to Rawlins & Thompson, proving the vast majority of therapeutic failures were expected and preventable."

      - title: "Stratified Alignment"
        description_1: 'Verified a <span class="highlight-metric">95.2% "Possible" causality rate</span>, while highlighting that <span class="highlight-metric">57.1% of reactions were clinically "Mild"</span>—yet still disruptive enough to ruin treatment adherence.'

  - type: "quote"
    text: "I don't just present data; I structure it to ensure evidence overcomes established behavioral heuristics."

  - type: "gallery"
    heading: "Visual Evidence"
    description: "An immersion into the communication strategy that earned First Place at the XV Scientific Conference."
    items:
      - image: "/assets/images/xv-jornada-01.jpg"
        alt: "Hypertension data highlight"
        caption: "Clinical Urgency: Visual hierarchy designed to transform cold figures into a call to action regarding high cardiovascular morbidity and mortality."

      - image: "/assets/images/xv-jornada-02.jpg"
        alt: "Methodological Breakdown"
        caption: "Minimalist iconography used to guide the jury through the identification, prevalence, and severity phases of ADRs."

      - image: "/assets/images/xv-jornada-03.jpg"
        alt: "Description of demographic characteristics"
        caption: "Demographic segmentation allowing for an understanding of the socioeconomic environment where adverse reactions manifest."

      - image: "/assets/images/xv-jornada-04.jpg"
        alt: "Bar chart of adverse drug reactions' frequency"
        caption: "Visualization of symptoms (n=13) allowing for the prioritization of adverse events with the highest impact on patient quality of life."

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