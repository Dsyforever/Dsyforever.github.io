---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

# About Me

I am currently a second-year PhD student at Dartmouth College. I am honored to be advised by Prof. [Yaoqing Yang](https://sites.google.com/site/yangyaoqingcmu/). Prior to this, I earned my Bachelor's degree in Mathematics and Applied Mathematics from South China University of Technology in 2024. My primary research interests lie in **learning theory** 📊 and **optimization** 📈.

---

<span class='anchor' id='research'></span>

## ✨ Research Interests

I am interested in both classical learning theory problems (Rademacher Complexity, Covering Number, PAC-Bayesian, etc.) and recently emerging theory problems (primarily focusing on the statistical and optimization properties of large-scale deep neural networks). If you have any interesting related problems, feel free to discuss with me anytime! I am very open to cooperation.


- Analyze the optimization properties (Non-Smoothness, Hessian, River-Valley, etc.) of large-scale neural networks, the behavior of optimization algorithms under specific loss landscapes, and develop scalable optimization algorithms based on these optimization properties and algorithms' behavior.
- Investigate **non-vacuous** and theoretically interpretable metrics for data/model statistical complexity in neural networks training, and determine how the interplay between data complexity and model complexity can lead to improved generalization and robustness performance.


---

<span class='anchor' id='xl'></span>

## 📖 Education

<table style="width: 100%; border-collapse: collapse; margin: 8px 0 2px 0; font-size: 0.97em; line-height: 1.35;">
  <tr style="border-bottom: 1px solid rgba(0,0,0,0.08);">
    <td style="width: 140px; padding: 6px 10px 6px 0; vertical-align: top;"><strong>2024.9 - Present</strong></td>
    <td style="padding: 6px 0; vertical-align: top;"><strong>Ph.D in Computer Science</strong><br>Dartmouth College</td>
  </tr>
  <tr>
    <td style="width: 140px; padding: 6px 10px 0 0; vertical-align: top;"><strong>2020.9 - 2024.6</strong></td>
    <td style="padding: 6px 0 0 0; vertical-align: top;"><strong>B.S. in Mathematics and Applied Mathematics</strong><br>South China University of Technology</td>
  </tr>
</table>

## 🏆 Selected Awards

<div style="margin: 8px 0 2px 0; font-size: 0.97em; line-height: 1.35;">
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2026</strong>
    <span>ICML 2026 Golden Reviewer.</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2026</strong>
    <span><strong style="color: #C0392B;">Best Student Paper Award</strong>, The 37th International Conference on Algorithmic Learning Theory.</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2024</strong>
    <span>Outstanding Graduation Thesis Award.</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2023</strong>
    <span>Yingli Scholarship (2/68).</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2023</strong>
    <span>Hong Ping Evergreen Fund (Outstanding Research Potential).</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2022</strong>
    <span>Mathematical Contest in Modeling: Finalist (0.2% of participants).</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0 0 0; align-items: start;">
    <strong>2022</strong>
    <span>First-class scholarship: top 2% of grade (2/68).</span>
  </div>
</div>

---

<span class='anchor' id='news'></span>

## 📢 News

<style>
  .news-table {
    width: 100%;
    border-collapse: collapse;
    margin: 8px 0 2px 0;
    font-size: 0.97em;
    line-height: 1.4;
  }

  .news-table th,
  .news-table td {
    padding: 8px 10px;
    vertical-align: top;
    border-bottom: 1px solid rgba(0, 0, 0, 0.08);
  }

  .news-table th {
    text-align: left;
    font-weight: 700;
  }

  .news-table td:first-child,
  .news-table th:first-child {
    width: 110px;
    white-space: nowrap;
  }

  .news-table tr:last-child td {
    border-bottom: none;
  }

  .news-details {
    position: relative;
    margin-top: -4px;
  }

  .news-details summary {
    list-style: none;
    cursor: pointer;
    height: 92px;
    display: flex;
    align-items: flex-end;
    justify-content: center;
    padding: 0 0 12px 0;
    background: linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(250, 251, 252, 0.88) 56%, #ffffff 100%);
  }

  .news-details summary::-webkit-details-marker {
    display: none;
  }

  .news-details[open] summary {
    display: none;
  }

  .news-summary-button {
    display: inline-block;
    padding: 8px 16px;
    border-radius: 999px;
    border: 1px solid rgba(71, 85, 105, 0.18);
    background: rgba(248, 250, 252, 0.96);
    color: #334155;
    font-size: 0.93em;
    font-weight: 600;
    box-shadow: 0 8px 18px rgba(15, 23, 42, 0.08);
    transition: transform 0.18s ease, box-shadow 0.18s ease, background 0.18s ease, border-color 0.18s ease;
  }

  .news-details summary:hover .news-summary-button,
  .news-details summary:focus .news-summary-button {
    transform: translateY(-1px);
    box-shadow: 0 12px 24px rgba(15, 23, 42, 0.12);
    background: #ffffff;
    border-color: rgba(71, 85, 105, 0.28);
  }

  .news-collapse-row {
    display: flex;
    justify-content: center;
    margin-top: 14px;
  }

  .news-collapse-button {
    border: 1px solid rgba(71, 85, 105, 0.16);
    padding: 8px 16px;
    border-radius: 999px;
    background: #f8fafc;
    color: #475569;
    font-size: 0.92em;
    font-weight: 600;
    cursor: pointer;
    box-shadow: 0 4px 10px rgba(15, 23, 42, 0.05);
    transition: background 0.18s ease, transform 0.18s ease, border-color 0.18s ease;
  }

  .news-collapse-button:hover {
    background: #ffffff;
    border-color: rgba(71, 85, 105, 0.24);
    transform: translateY(-1px);
  }

  @media (max-width: 640px) {
    .news-table td:first-child,
    .news-table th:first-child {
      width: 86px;
    }
  }
</style>

<table class="news-table">
  <thead>
    <tr>
      <th>Date</th>
      <th>Update</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>2026.06</strong></td>
      <td>💰 Honored to receive the <strong>ISIT 2026 Travel Grant Award</strong>.</td>
    </tr>
    <tr>
      <td><strong>2026.06</strong></td>
      <td>🎉 Our paper, <a href="https://openreview.net/pdf?id=U812abpXRD"><em>How Does Orthogonalization Adapt to the Neural-Network Hessian Structure? A Gradient Self Outer-Product Analysis at Initialization</em></a>, has been accepted to the <strong>ICML 2026 HILD Workshop</strong>.</td>
    </tr>
    <tr>
      <td><strong>2026.05</strong></td>
      <td>🎙️ Gave a talk about <a href="https://arxiv.org/abs/2603.20527"><em>RMNP</em></a> at Dartmouth--Berkeley--Rice AI Reading Group (<a href="https://drive.google.com/file/d/1DpE-PhpCtNHCZuI5oIdvQutLnOOL2yUS/view?usp=drive_link">Recording</a>).</td>
    </tr>
    <tr>
      <td><strong>2026.05</strong></td>
      <td>✨ <a href="/blog/dsyblog/"><em>New blog: A Proof of Orthogonalized and Row-Normalized Descent Directions</em></a> is now online.</td>
    </tr>
    <tr>
      <td><strong>2026.05</strong></td>
      <td>🎉 Honored to be recognized as an ICML 2026 Golden Reviewer. Grateful for the recognition from the community.</td>
    </tr>
    <tr>
      <td><strong>2026.05</strong></td>
      <td>✨ <a href="/blog/">New blog</a> in understanding Row normalization and orthogonalization for NN online. Welcome to discuss!</td>
    </tr>
    <tr>
      <td><strong>2026.05</strong></td>
      <td>🎉Two paper has been accepted to ICML 2026, including <a href="https://arxiv.org/abs/2603.20527"><em>RMNP</em></a>! We will soon release two blog posts to discuss the rich intuitions behind RMNP.</td>
    </tr>
    <tr>
      <td><strong>2026.03</strong></td>
      <td>🎉 Our paper about <a href="https://arxiv.org/abs/2602.00545"><em>Hessian Spectral Bifurcation</em></a> has been accepted to <strong>ISIT 2026</strong>.</td>
    </tr>
  </tbody>
</table>

<details class="news-details">
  <summary>
    <span class="news-summary-button">More news</span>
  </summary>

  <table class="news-table">
    <tbody>
      <tr>
        <td><strong>2026.03</strong></td>
        <td>📄 New preprint about Matrix-Based Optimization: <a href="https://arxiv.org/abs/2603.20527"><em>RMNP: Row-Momentum Normalized Preconditioning for Scalable Matrix-Based Optimization</em></a></td>
      </tr>
      <tr>
        <td><strong>2026.02</strong></td>
        <td>🏆 My first paper as first author, <a href="https://arxiv.org/abs/2601.11789"><em>Suspicious Alignment of SGD</em></a>, received <strong>Best Student Paper Award</strong> at the 37th International Conference on Algorithmic Learning Theory (ALT) 2026!</td>
      </tr>
      <tr>
        <td><strong>2026.02</strong></td>
        <td>🎙️ Giving a talk at Fields Institute on Feb 26th about our ALT paper (<a href="https://www.youtube.com/watch?v=uRXzDT5L_Sk&t=2761s">Recording</a>)</td>
      </tr>
      <tr>
        <td><strong>2026.02</strong></td>
        <td>📄 New short paper preprint about Hessian: <a href="https://arxiv.org/abs/2602.00545"><em>Depth, Not Data: An Analysis of Hessian Spectral Bifurcation</em></a></td>
      </tr>
      <tr>
        <td><strong>2026.02</strong></td>
        <td>📝 Serving as a reviewer for <strong>ICML 2026</strong></td>
      </tr>
      <tr>
        <td><strong>2025.12</strong></td>
        <td>🎉 <a href="https://arxiv.org/abs/2601.11789"><em>Suspicious Alignment of SGD</em></a> has been accepted to <strong>ALT 2026</strong>.</td>
      </tr>
      <tr>
        <td><strong>2025.12</strong></td>
        <td>💰 Honored to receive a $2,000 grant from <strong>Lambda AI</strong></td>
      </tr>
      <tr>
        <td><strong>2025.10</strong></td>
        <td>📝 Serving as a reviewer for <strong>ICLR 2026</strong></td>
      </tr>
      <tr>
        <td><strong>2025.10</strong></td>
        <td>👋 First post on this website - welcome!</td>
      </tr>
    </tbody>
  </table>

  <div class="news-collapse-row">
    <button type="button" class="news-collapse-button" onclick="this.closest('details').open=false;">Show less</button>
  </div>
</details>

---

<span class='anchor' id='publications'></span>

## 📚 Selected Research

<p style="margin: 4px 0 12px 0; font-size: 0.95em; color: #555;"><sup>*</sup> indicates equal contribution.</p>

<div style="background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ec 100%); padding: 20px; border-radius: 12px; margin: 15px 0;">

<strong>How Does Orthogonalization Adapt to the Neural-Network Hessian Structure? A Gradient Self Outer-Product Analysis at Initialization</strong><br>
<span style="color: #555;"><strong>Shenyang Deng</strong>, Shuhua Yu, Yaoqing Yang</span><br>
<em>ICML 2026 Workshop on High-dimensional Learning Dynamics</em><br>
<a href="https://openreview.net/pdf?id=U812abpXRD">[OpenReview]</a>

</div>

<div style="display: flex; justify-content: center; margin: 18px 0 24px 0;">
  <div style="width: min(60%, 620px); height: 240px; display: flex; align-items: center; justify-content: center; padding: 12px; border: 1px solid rgba(0,0,0,0.08); border-radius: 12px; box-shadow: 0 3px 12px rgba(0,0,0,0.08); background: #fff; overflow: hidden;">
    <img src="/images/HILD_img.png" alt="How Does Orthogonalization Adapt to the Neural-Network Hessian Structure?" style="width: 100%; height: 100%; object-fit: contain; border-radius: 8px;">
  </div>
</div>

<div style="background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ec 100%); padding: 20px; border-radius: 12px; margin: 15px 0;">

<strong>RMNP: Row-Momentum Normalized Preconditioning for Scalable Matrix-Based Optimization</strong><br>
<span style="color: #555;"><strong>Shenyang Deng</strong><sup>*</sup>, Zhuoli Ouyang<sup>*</sup>, Tianyu Pang, Zihang Liu, Ruochen Jin, Shuhua Yu, Yaoqing Yang</span><br>
<em>The 43rd International Conference on Machine Learning (ICML 2026)</em><br>
<a href="https://arxiv.org/abs/2603.20527">[arxiv]</a> <a href="https://dsyforever.github.io/blog/normalization-orthogonalization/">[Additional Asymptotic Theory on NNs]</a>

</div>

<div style="display: flex; justify-content: center; margin: 18px 0 24px 0;">
  <div style="width: min(60%, 620px); height: 240px; display: flex; align-items: center; justify-content: center; padding: 12px; border: 1px solid rgba(0,0,0,0.08); border-radius: 12px; box-shadow: 0 3px 12px rgba(0,0,0,0.08); background: #fff; overflow: hidden;">
    <img src="/images/precc3_01.png" alt="RMNP" style="width: 100%; height: 100%; object-fit: contain; border-radius: 8px;">
  </div>
</div>

<div style="background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ec 100%); padding: 20px; border-radius: 12px; margin: 15px 0;">

<strong>Suspicious Alignment of SGD: A Fine-Grained Step Size Condition Analysis</strong><br>
<span style="color: #555;"><strong>Shenyang Deng</strong>, Boyao Liao, Zhuoli Ouyang, Tianyu Pang, Minhak Song, Yaoqing Yang</span><br>
<em>The 37th International Conference on Algorithmic Learning Theory (ALT 2026)</em><br>
🏆 <span style="color: #E74C3C; font-weight: bold;">Best Student Paper Award</span><br>
<a href="https://arxiv.org/abs/2601.11789">[arxiv]</a> <a href="https://drive.google.com/file/d/1VIR-OjXcosWFBDb9lUU_AEeEEqCc3xLu/view?usp=sharing">[download]</a>

</div>

<div style="display: flex; justify-content: center; margin: 18px 0 24px 0;">
  <div style="width: min(52%, 520px); height: 210px; display: flex; align-items: center; justify-content: center; padding: 12px; border: 1px solid rgba(0,0,0,0.08); border-radius: 12px; box-shadow: 0 3px 12px rgba(0,0,0,0.08); background: #fff; overflow: hidden;">
    <img src="/images/con_figure_3agx_2.png" alt="Suspicious Alignment of SGD" style="width: 100%; height: 100%; object-fit: contain; border-radius: 8px;">
  </div>
</div>

<div style="background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ec 100%); padding: 20px; border-radius: 12px; margin: 15px 0;">

<strong>Depth, Not Data: An Analysis of Hessian Spectral Bifurcation</strong><br>
<span style="color: #555;"><strong>Shenyang Deng</strong><sup>*</sup>, Boyao Liao<sup>*</sup>, Zhuoli Ouyang<sup>*</sup>, Tianyu Pang, Yaoqing Yang</span><br>
<em>IEEE International Symposium on Information Theory (ISIT 2026)</em> <strong>(Extended version in preparation for IEEE Transactions on Information Theory)</strong><br>
<a href="https://arxiv.org/abs/2602.00545">[arxiv]</a>

</div>

<div style="display: flex; justify-content: center; margin: 18px 0 24px 0;">
  <div style="width: min(60%, 620px); height: 240px; display: flex; align-items: center; justify-content: center; padding: 12px; border: 1px solid rgba(0,0,0,0.08); border-radius: 12px; box-shadow: 0 3px 12px rgba(0,0,0,0.08); background: #fff; overflow: hidden;">
    <img src="/images/combined_3panels.png" alt="Depth, Not Data: An Analysis of Hessian Spectral Bifurcation" style="width: 100%; height: 100%; object-fit: contain; border-radius: 8px;">
  </div>
</div>

<p style="text-align: center; margin: 6px 0 18px 0;">
  <a href="/publications/" style="display: inline-block; padding: 10px 18px; border-radius: 999px; background: #1f2937; color: #fff; text-decoration: none; font-weight: 600;">See Full Publication List →</a>
</p>

<p style="text-align: center;">
  📎 Check out more of my work on <a href="https://scholar.google.com/citations?user=TvUZLD8AAAAJ&hl=en"><strong>Google Scholar</strong></a>
</p>

---

<span class='anchor' id='talks'></span>

## 🎙️ Recent Talks
<div style="margin: 8px 0 2px 0; font-size: 0.94em; line-height: 1.35;">
  <div style="display: grid; grid-template-columns: 92px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2026.05.05</strong>
    <span><strong>RMNP</strong><br>Dartmouth--Berkeley--Rice AI Reading Group. <a href="https://drive.google.com/file/d/1DpE-PhpCtNHCZuI5oIdvQutLnOOL2yUS/view?usp=drive_link">Recording</a></span>
  </div>
  <div style="display: grid; grid-template-columns: 92px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2026.02.26</strong>
    <span><strong>Suspicious Alignment of SGD</strong><br>Fields Institute. <a href="https://www.youtube.com/watch?v=uRXzDT5L_Sk&t=2761s">Recording</a></span>
  </div>
  <div style="display: grid; grid-template-columns: 92px 1fr; gap: 8px; padding: 6px 0 0 0; align-items: start;">
    <strong>2025.11.27</strong>
    <span><strong>Suspicious Alignment of SGD</strong><br>Dartmouth--Berkeley--Rice AI Reading Group. <a href="https://drive.google.com/file/d/1ByfsVsaRM7DG_HPKRijWwpkVApFOgjHx/view?usp=sharing">Recording</a></span>
  </div>
</div>

---

<span class='anchor' id='service'></span>

## 📝 Academic Service

<div style="margin: 8px 0 2px 0; font-size: 0.94em; line-height: 1.35;">
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>Journal</strong>
    <span>Reviewer for TPAMI</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2026</strong>
    <span>Reviewer for ICML 2026</span>
  </div>
  <div style="display: grid; grid-template-columns: 72px 1fr; gap: 8px; padding: 6px 0 0 0; align-items: start;">
    <strong>2025</strong>
    <span>Reviewer for ICLR 2026</span>
  </div>
</div>

---

## 🍽️ Miscellaneous

I am a food enthusiast who loves both eating and cooking. I enjoy preparing a hearty dinner after a busy work schedule and then rewarding myself with a game of **StarCraft II** 🎮. Here are some photos of the dishes I have made: [**See Gallery →**](/gallery/)
