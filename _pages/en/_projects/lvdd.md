---
layout: page
title: "Diastolic Dysfunction in Hemodialysis"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: projects/lvdd/
lang: en

page_components:
  - type: "header"
    title: "Cardiorenal Triage: Quantifying Robust Prevalence Ratios Under Survival Bias"
  
    bottom_line:
      label: "The Bottom Line"
      text: "By deploying a robust Poisson regression model to adjust for single-center sample constraints, this analysis isolated <span class='highlight-metric'>chronic Hypertension (Adjusted PR: 2.22)</span> and <span class='highlight-metric'>glycemic control (Adjusted PR: 1.16)</span> as the dominant independent drivers of heart failure in maintenance hemodialysis, locking down the risk magnitude."

    tech_stack:
      label: "Core Strategies"
      items:
        - "Bias mitigation"
        - "Robust regression modeling"
        - "Multi-variate confounding control"
  
  - type: "section"
    title: "The Challenge: Silent Cardiovascular Mortality"
    content: "In patients undergoing maintenance hemodialysis for advanced Stage G5 Chronic Kidney Disease (CKD), <strong>cardiovascular disease stands as the leading cause of mortality</strong>. Left Ventricular Diastolic Dysfunction (LVDD) represents an early, silent marker of this cardiorenal crisis."

  - type: "section"
    title: "A Bias That Survives"
    content: 'Cross-sectional datasets in active dialysis wards suffer inherently from <strong>Neyman Bias (survival bias)</strong>. Because the highest-acuity cardiorenal patients often pass away or face emergency hospitalization before data is even captured, standard statistical models end up analyzing <strong>an unnaturally "stable" survivor cohort.</strong>'

  - type: "skills"
    skills_heading: "Elevating Clinical Protocols Through Statistical Mentorship"
    skills_description: "Rescuing an institutional research protocol requires moving past baseline data collection. My advisory approach focused on mentoring clinical investigators to look beyond p-values and visually audit their underlying cohort distributions."
    skills:
      - title: Visualizing Hidden Variance
        icon: "assets/images/icons/statistic.png"
        one: "I coached the team to deploy <b>distribution visualizations</b> to unmask a critical pattern that no summary table could reveal: severe right-skewed tail variance with multiple uncontrolled outliers stretching up to 10% HbA1c."

      - title: Analytical redirection
        icon: "assets/images/icons/selection.png"
        one: "I guided the investigative team toward a <b>Poisson Regression model with robust variance</b>, which allowed them to calculate uninflated Prevalence Ratios (PR) that more accurately translate the clinical magnitude of the risk."

      - title: Sequential Regressions
        icon: "assets/images/icons/timeline.png"
        one: "I structured a <b>three-phase multi-variate regression matrix</b>: models adjusted for baseline demographics (age/sex), nutritional/metabolic noise (BMI/Albumin), and a final multi-system integration phase."

  - type: "showcase"
    heading: "Unmasking the Risk Magnitude"
    description: "The audited protocol revealed that an alarming 72.5% of the hemodialysis cohort was actively suffering from LVDD. By overcoming the limitations of a small, single-center sample through robust modeling, my biostatistical mentorship guided the team to extract uninflated effect sizes."
    image: "/assets/images/cover_project_lvdd.png"
    alt: "LVDD model comparison forest plot showing PR and p-values for Model 1, 2, and 3"
    caption: "<b>Figure 1: Stratified Multivariate Poisson Regressions.</b> By replacing unstable logistic odds with robust sandwich covariance estimators, the framework successfully controls for severe sample constraints (N = 51) without over-saturating the parameters."
    metrics:
      - value: "72.5%"
        label: "Cohort LVDD Prevalence"
        detail: "Unmasked baseline burden across active hemodialysis cohort."

      - value: "2.22"
        unit: "aPR"
        label: "for Chronic Hypertension"
        detail: "Adjusted prevalence ratio<br>(p < 0.001, 95% CI: 1.48–3.35)."

      - value: "+16%"
        unit: "per HbA1c Unit"
        label: "Risk due to Glycemic Surge"
        detail: "Risk increase per 1% HbA1c elevation<br>(p < 0.001)."

  - type: "quote"
    text: "True biostatistical mentorship isn’t about chasing p-values; it’s about coaching a clinical team to recognize where biological noise ends and true risk begins."

  - type: "reflections"
    heading: "Reflections: Methodology Dictates Interpretation"
    description: "Guiding the biostatistical layer of this cardiorenal protocol solidified a fact of healthcare analysis: <b>blind mathematical modeling fails when disconnected from clinical pathophysiology</b>. Rescuing this analysis required mentoring the investigative team to look past raw statistical software outputs and critically evaluate the biological trade-offs within their data architecture."
    cards:
      - title: "The Ceiling Effect"
        lead: "Universal pathology destroys statistical variance. "
        body: "Classic risk factors like profound anemia failed to reach significance due to their omnipresence in Stage G5 CKD. I coached the team to focus on volatile, high-impact drivers like metabolic shifts instead."

      - title: "The Lifespan Trade-off"
        lead: "Biological mechanics distort raw endpoints. "
        body: "Hemodialysis mechanically destroys red blood cells, artificially lowering raw HbA1c values. I advised the team that our uncovered 16% risk surge per HbA1c point is a highly conservative effect."

      - title: "Future Optimization"
        lead: "Conquering survival bias requires longitudinal tracking. "
        body: "While our robust Poisson model successfully stabilized this cross-sectional snapshot, Neyman Bias remains an inherent threat. Therefore I recommend a longitudinal registry following cohorts from day one."

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
  {% endif %}
{% endfor %}

{% include cta.html %}