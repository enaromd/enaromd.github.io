---
layout: splash
title: "Obesidad Clínica en NHANES 2021-2023"
permalink: portfolio/projects/nhanes_obesity/
lang: es
description: "Cuando el peso no pesa lo mismo en todos: Aplicando el marco de Obesidad Clínica de The Lancet"
header:
  teaser: "/assets/images/plot_framework_sankey.png"
seo:
  type: "article"
  title: "Marco de Obesidad Clínica (NHANES 2021–2023)"
  image: "/assets/images/obesity_teaser.png"
approach:
  - title: "Filtrado de Cohorte, Ingeniería de Riesgo y Modelado GEE"
  - excerpt: "Ejecución de un flujo bioestadístico de extremo a extremo: desde el filtrado estructurado de la cohorte (N = 1,816) hasta el cálculo de índices compuestos y la estimación de Razones de Riesgo ponderadas por encuesta."
flowchart:
  - title: "Selección de Cohorte y Atrición Sistemática"
  - excerpt: "Ejecución de un flujo de filtración para controlar saltos en encuestas complejas, pesos de submuestras en ayunas y criterios de límites fenotípicos."
table1:
  - title: "Estratificación Inicial de la Población (Tabla 1)"
  - excerpt: "Evaluación de gradientes demográficos, de examen y biomarcadores ponderados por encuesta en cohortes de fenotipos Control, Periférico y Clásico (N = 1,588)."
results:
  - title: "Disparidades Fenotípicas y Rendimiento de METS-IR"
  - excerpt: "Revelando la desregulación metabólica subclínica y el daño a órganos diana ocultos por el tamizaje antropométrico estándar."
forest:
  - title: "Riesgo Relativo Fenotípico y Ajustado por Índices"
  - excerpt: "Rastreo del riesgo de fibrosis hepática desde líneas base fenotípicas no ajustadas (M1), pasando por sucedáneos de desbordamiento cruzado (M2), hasta modelos fenotipo-índice totalmente integrados (M3)."
sankey:
  - title: "De Fenotipos Clínicos a Riesgo por Dominio y Daño a Órganos Diana"
  - excerpt: "Mapeo de la cascada ponderada por encuesta desde la composición corporal inicial, a través de cúmulos de riesgo subclínico por dominio, hasta el deterioro orgánico manifiesto."
---
<style>
.feature-divider {
  margin-top: 5rem;
  margin-bottom: 2rem;
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

.highlight-metric {
  color: #b80f0a;
  font-weight: 600;
}
</style>

<div class="headline">
  <h1>Cuando el peso no pesa lo mismo en todos: Aplicando el marco de Obesidad Clínica de The Lancet</h1>
  <p><strong>Punto Clave:</strong> El Puntaje Metabólico para Resistencia a la Insulina <span class="highlight-metric">(METS-IR) mostró un efecto independiente y robusto para la fibrosis hepática confirmada por FibroScan (RR ajustado = 2.9</span>) y el mejor ajuste general del modelo (QIC = 815.7) en comparación con otras razones lipídicas y glucémicas en modelos totalmente ajustados.</p>
</div>

<div class="skills-bar">
  <p><strong>Stack Tecnológico:</strong> Python, PyReadStat, Pandas, NumPy, Matplotlib, Missingno, PyArrow</p>
</div>

<h2>El Desafío: La brecha diagnóstica del Índice de Masa Corporal (IMC)</h2>
<p><strong>Los clínicos confían casi universalmente en el Índice de Masa Corporal (IMC ≥ 30 kg/m²) como el filtro diagnóstico por defecto para evaluar la obesidad</strong>. Al basarse únicamente en proporciones de peso y talla, los protocolos estándar de tamizaje pasan por alto un compromiso subclínico cardiometabólico, hepático y renal significativo en individuos con peso normal pero metabólicamente no saludables.</p>

<h2>La Brecha de Traducción: Razones Antropométricas e Índices de Riesgo</h2>
<p>Operacionalizar el Marco de Obesidad Clínica de The Lancet requiere ir más allá del IMC bruto mediante el cálculo de razones antropométricas específicas —como la Razón Cintura-Estatura— para definir con precisión los fenotipos de obesidad clínica.</p>
<p>Además, los datos brutos de NHANES almacenan biomarcadores como parámetros de laboratorio aislados a través de submuestras complejas de encuestas. <strong>Para cuantificar de manera sistemática el riesgo cardiovascular, metabólico y de órganos específicos, estas variables individuales deben traducirse en índices de riesgo clínico validados</strong> (ej. METS-IR, FIB-4, FLI y AHA PREVENT) para capturar la vulnerabilidad subclínica antes del deterioro orgánico manifiesto.</p>

<hr class="feature-divider">

{% include feature_row id="approach" type="center" %}

<div class="grid-container">
  <div class="grid-item">
    <img src="/assets/images/timeline.png" alt="Ícono: Atrición" class="grid-icon">
    <h3>Atrición de la Cohorte</h3>
    <p>Construí un flujo de filtración <strong>aislando a adultos en edad laboral (18 a 64 años)</strong> del ciclo NHANES 2021–2023, controlando sistemáticamente el embarazo, los registros sin ponderar y los parámetros iniciales faltantes (N = 11,933 $\to$ 1,816).</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/engineering.png" alt="Ícono: Ingeniería de Riesgo" class="grid-icon">
    <h3>Ingeniería de Índices de Riesgo</h3>
    <p>Transformé <strong>datos brutos en índices de riesgo clínico validados</strong>, incluyendo el Score Metabólico para Resistencia a la Insulina (METS-IR), Índice de Hígado Graso (FLI), Índice de Fibrosis-4 (FIB-4) y los puntajes de riesgo cardiometabólico-renal AHA PREVENT.</p>
  </div>
  <div class="grid-item">
    <img src="/assets/images/statistic.png" alt="Ícono: Estadística" class="grid-icon">
    <h3>Razones de Riesgo Ponderadas por Encuesta</h3>
    <p>Apliqué <strong>Ecuaciones de Estimación Generalizadas (GEE) con familia Poisson</strong>, incorporando parámetros del diseño de la encuesta (grupos, estratos y pesos de ayuno) para calcular Razones de Riesgo (RR) ajustadas a la población.</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="flowchart" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/final_flowchart.svg" alt="Diagrama de flujo STROBE" style="width: 100%; max-width: 520px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    <strong>Figura 1. Flujo de Atrición de Cohorte.</strong> Filtración secuencial del conjunto de datos maestro NHANES 2021–2023 (N = 11,933). Hacer cumplir la conformidad con el protocolo de ayuno matutino (<code>WTSAF2YR</code>), los límites de edad laboral (18–64 años) y la higiene de datos de casos completos aisló a 1,816 adultos en ayunas. La depuración de 228 registros ambiguos no clasificados estableció una cohorte final de análisis fenotípicamente válida de N = 1,588 adultos.
  </p>
</div>

<hr class="feature-divider">

{% include feature_row id="table1" type="center" %}

<div class="table-container" style="overflow-x: auto; margin: 2.5rem 0;">
  <table class="mbi-table" style="width: 100%; max-width: 800px; border: 1px solid #ddd; border-collapse: collapse; font-size: 0.9rem;">
    <thead>
      <tr style="background-color: #003152; color: white;">
        <th style="padding: 12px; border: 1px solid #ddd; text-align: left;">Variable</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">General</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">Control</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">Periférico</th>
        <th style="padding: 12px; border: 1px solid #ddd; text-align: right;">Clásico</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Edad</strong> (años)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">40.92</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">32.05</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">45.55</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">42.94</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>PA Sistólica</strong> (mmHg)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">117.21</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">112.75</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">118.29</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">119.31</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>PA Diastólica</strong> (mmHg)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">74.59</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">68.59</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">74.11</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">78.64</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Frecuencia cardíaca</strong> (ppm)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">70.88</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">69.30</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">70.41</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">72.06</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Glucosa en Ayunas</strong> (mg/dL)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">105.06</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">98.72</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">103.94</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">111.31</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Triglicéridos</strong> (mg/dL)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">108.60</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">74.17</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">117.46</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">124.36</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Colesterol HDL</strong> (mg/dL)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">53.62</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">60.70</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">53.50</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">49.59</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Rigidez Hepática</strong> (kPa)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">5.76</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">4.86</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">5.42</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">6.79</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>TFGe</strong> (mL/min/1.73m²)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">102.51</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">108.14</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">99.57</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">101.41</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Daño hepático</strong> (%)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">13.96</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">4.08</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">9.55</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">25.13</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Daño metabólico</strong> (%)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">6.42</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.09</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">7.90</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">9.82</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;"><strong>Daño renal</strong> (%)</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.99</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.00</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">0.93</td>
        <td style="padding: 10px; border: 1px solid #ddd; text-align: right;">1.54</td>
      </tr>
    </tbody>
  </table>
</div>

<hr class="feature-divider">

{% include feature_row id="results" type="center" %}

<div class="project-grid">
  <div class="card">
    <h3>IMC y Daño Hepático No Ajustado</h3>
    <p>Los modelos no ajustados muestran que el <strong>Fenotipo Clásico guiado por el IMC rastrea fuertemente el daño hepático (RR = 5.19).</strong></p>
    <p>Sin embargo, <strong>confiar únicamente en el IMC ignora al 35.0% de los adultos</strong> categorizados como Periféricos, quienes aun así enfrentan un riesgo hepático elevado (RR = 1.95).</p>
  </div>
  <div class="card">
    <h3>METS-IR como Sucedáneo para el Riesgo de Daño Hepático</h3>
    <p>El METS-IR funciona como un <strong>impulsor independiente y robusto de daño hepático</strong> a lo largo del modelo integrado <strong>(RR = 2.87).</strong></p>
    <p>De manera crucial, detecta incrementos marcados en el riesgo de daño tanto en las cohortes aisladas clásica (RR = 2.76) como periférica (RR = 3.60).</p>
  </div>
  <div class="card">
    <h3>Fenotipos y Disparidades de Riesgo por Dominio</h3>
    <p>Abarcando el 45.8% de los adultos, el <strong>Fenotipo Clásico impulsa la mayor parte del riesgo multidominio (28.3% global).</strong></p>
    <p>Como resultado, <strong>mantiene un mayor riesgo de daño a órgano diana (RR = 2.44)</strong> que el Fenotipo Periférico (RR = 1.91).</p>
  </div>
</div>

<hr class="feature-divider">

{% include feature_row id="forest" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/plot_indices_forest_coefficients.png" alt="Gráfico de bosque (Forest Plot) comparando Razones de Riesgo a través de índices" style="width: 100%; max-width: 850px; border-radius: 8px;">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    <strong>Figura 2. Atenuación Secuencial del Riesgo en Regresión de Poisson con GEE.</strong> Comparación de los fenotipos estructurales iniciales (M1) frente a modelos integrados (M3). La inclusión del punto de corte diagnóstico de METS-IR (RR = 2.87) atenúa la razón de riesgo del Fenotipo Clásico de RR = 5.19 (IC del 95%: 2.94-9.17) a RR = 2.44 (IC del 95%: 1.22-4.89), confirmando la disfunción metabólica como un mediador primario del daño hepático a órgano diana.
  </p>
</div>

<hr class="feature-divider">

{% include feature_row id="sankey" type="center" %}

<div class="mbi-main-plot" style="margin: 3rem 0; text-align: center;">
  <img src="/assets/images/plot_framework_sankey.png" alt="Diagrama de Sankey desde fenotipos de obesidad a través de dominios de riesgo hacia daño a órganos diana" style="width: 100%; max-width: 850px; border-radius: 8px;">
  <p style="font-style: italic; color: #666; margin-top: 1rem; font-size: 0.9rem;">
    <strong>Figura 3. Trayectorias Fenotípicas a través de Cúmulos de Riesgo por Dominio.</strong> Diagrama de flujo ponderado por encuesta que mapea los fenotipos de obesidad hacia el riesgo de daño por dominio. Los controles sanos fluyen exclusivamente hacia cero daño orgánico, mientras que el Fenotipo Clásico actúa como el origen principal de la disfunción multidominio ($\ge 2$ sistemas orgánicos), reforzando el riesgo sinérgico de la sobrecarga hepática y metabólica.
  </p>
</div>

<hr class="feature-divider">

<div class="pull-quote">
  "<strong>Reenmarcar la obesidad</strong> desde un número antropométrico estático <strong>hacia un continuo metabólico multisistémico</strong> es el primer paso esencial hacia una verdadera medicina de precisión, demostrando que el peso corporal por sí solo no puede dictar la vulnerabilidad clínica."
</div>

<h2>Reflexión: Redefiniendo la Obesidad Más Allá de la Báscula</h2>

<p>Nuestros hallazgos desafían la dependencia histórica del IMC como único filtro diagnóstico: dos individuos con mediciones antropométricas similares pueden albergar trayectorias radicalmente diferentes de sobrecarga orgánica subclínica.</p>

<blockquote>
    <strong>Punto Clave:</strong> La salud metabólica no se puede inferir solo a partir de la masa corporal. En adultos con IMC normal clasificados en el fenotipo de Obesidad Periférica, cruzar el umbral elevado de METS-IR desencadena un <strong>incremento de 3.60 veces en el riesgo relativo</strong> de fibrosis hepática confirmada por FibroScan, lo que demuestra que la resistencia a la insulina subclínica impulsa el daño tisular mucho antes de que se manifieste la obesidad clínica evidente.
</blockquote>

<p>Traducir estas percepciones bioestadísticas a la atención del mundo real requiere integrar la automatización de índices de riesgo —como METS-IR, FIB-4 y FLI— directamente en los flujos de trabajo del expediente clínico electrónico (EHR). Automatizar estos cálculos a partir de paneles de laboratorio de rutina crea un cambio de paradigma fundamental: alejar la atención médica de la gestión reactiva de enfermedades en etapas tardías hacia una intervención subclínica proactiva y guiada por algoritmos.</p>

<div class="cta">
  <div style="text-align: center;">
    <h3>Aprovechando Datos para Decisiones de Alto Impacto</h3>
    <p>Desde el procesamiento de datos hasta la validación de modelos predictivos, transformo variables complejas en claridad operacional. Si busca un analista de datos que entienda el valor estratégico de la precisión técnica, hablemos.</p>
    <a href="/contact/" class="btn btn--primary">Ponerse en Contacto</a>
  </div>
</div>