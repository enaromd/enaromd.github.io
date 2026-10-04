---
layout: page
title: "About me"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: about/
lang: en

about:
  title: "Grounding Health Data Integrity in Clinical Practice"
  p1: "My clinical work reinforces a simple truth: behind every protocol is a data trail, and behind every data point is a high-stress medical decision. Healthcare analytics suffers when code is written without understanding bedside care."
  p2: "I bridge that gap by combining frontline clinical experience with SQL database design and statistical modeling, converting raw health records into standardized, validated metrics that improve patient outcomes."
  image: "/assets/images/about_squared.jpg"

features:
  - heading: "The Art of Persuading with Evidence"
    p1: "Winning First Place at the XV SILAIS Granada Scientific Conference validated a core thesis of my work: rigorous methodology only succeeds when paired with clear communication."
    p2: "This award recognized the translation of  statistical analysis into a structured narrative that gave public health decision-makers clarity and actionable insights."
    image: "/assets/images/about_story-1.jpeg"
    alt: "Award ceremony at the SILAIS Granada Scientific Conference with healthcare professionals holding a first place certificate"
  - heading: "Field Demands Drive Structure"
    p1: "Operating within the high-pressure environment of the ‘Project Health for Leon’ cardiology brigade exposed a critical workflow vulnerability: how to safely triage an overwhelming patient volume under tight time constraints."
    p2: "This exact operational bottleneck drove me to develop the Medication Burden Index (MBI), converting raw medication registries into a surrogate metric for cardiac remodeling."
    image: "/assets/images/about_story-2.jpeg"
    alt: "Project Health for Leon medical brigade team in scrubs posing outside an operating room"
  - heading: "Translating Complexity into Strategy"
    p1: "Participating in the technical discussion session at the First Western Congress on Maternal and Neonatal Health highlighted the necessity of cross-functional dialogue."
    p2: "My role focused on navigating complex immunological frameworks during interdisciplinary panels to establish practical, purposeful clarity regarding Antiphospholipid Syndrome in Pregnancy."
    image: "/assets/images/about_story-3.jpeg"
    alt: "Medical speaker presenting at a podium on stage alongside a live virtual panelist displayed on a projected screen"
      
skills_heading: "Core Principles & Analytical Philosophy"
skills_description: "Combining direct medical practice with quantitative rigor to mitigate data distortion, reduce systematic bias, and improve real-world patient outcomes."
skills:
  - title: Evidence Over Dogma
    icon: "assets/images/icons/selection.png"
    one: "Clinical intuition creates hypotheses; empirical data establishes truth."
    two: "Decisions must rest on verifiable quantitative evidence rather than habit or hierarchy. This allows us to diagnose missingness mechanisms, audit workflows, and let data dictate the solution."
  - title: Persuasion Through Clarity
    icon: "assets/images/icons/event.png"
    one: "Complex biostatistical models are useless if stakeholders cannot interpret them."
    two: "True influence comes from translating complex concepts—like treatment effect heterogeneity—into transparent, decision-ready communication."
  - title: Cross-Disciplinary Synergy
    icon: "assets/images/icons/effects.png"
    one: "Controlling ego means recognizing the limits of clinical training alone"
    two: "Combining frontline clinical practice with database engineering and systems thinking creates pipelines that are technically sound and operationally realistic."

cta:
  heading: "Bridge Frontline Clinical Reality with Technical Execution"
  description: "Effective healthcare analytics starts with knowing how data is born at the bedside—including the hectic workflows and human factors that warp raw records. If your team needs someone who combines frontline clinical perspective with Python, SQL, and biostatistics, let’s connect."
  bg_image: "/assets/images/cta-background.jpg"
  button:
    text: "Get in touch"
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