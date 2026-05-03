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

**My current research primarily focuses on:**

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

| Date | Update |
|:-----|:-------|
| **2026.05** | 🎉Two paper has been accepted to ICML 2026, including [*RMNP*](https://arxiv.org/abs/2603.20527) ! We will soon release two blog posts to discuss the rich intuitions behind RMNP.|
| **2026.03** | 🎉 Our paper about [*"Hessian Spectral Bifurcation"*](https://arxiv.org/abs/2602.00545) has been accepted to **ISIT 2026**.|
| **2026.03** | 📄 New preprint about Matrix-Based Optimization: [*RMNP: Row-Momentum Normalized Preconditioning for Scalable Matrix-Based Optimization*](https://arxiv.org/abs/2603.20527) |
| **2026.02** | 🏆 My first paper as first author, [*"Suspicious Alignment of SGD"*](https://arxiv.org/abs/2601.11789), received **Best Student Paper Award** at the 37th International Conference on Algorithmic Learning Theory (ALT) 2026! |
| **2026.02** | 🎙️ Giving a talk at Fields Institute on Feb 26th about our ALT paper ([Recording](https://www.youtube.com/watch?v=uRXzDT5L_Sk&t=2761s))|
| **2026.02** | 📄 New short paper preprint about Hessian: [*Depth, Not Data: An Analysis of Hessian Spectral Bifurcation*](https://arxiv.org/abs/2602.00545))|
| **2026.02** | 📝 Serving as a reviewer for **ICML 2026** |
| **2025.12** | 🎉 [*"Suspicious Alignment of SGD"*](https://arxiv.org/abs/2601.11789) has been accepted to **ALT 2026** .|
| **2025.12** | 💰 Honored to receive a $2,000 grant from **Lambda AI** |
| **2025.10** | 📝 Serving as a reviewer for **ICLR 2026** |
| **2025.10** | 👋 First post on this website - welcome! |

---

<span class='anchor' id='publications'></span>

## 📚 Selected Research

<p style="margin: 4px 0 12px 0; font-size: 0.95em; color: #555;"><sup>*</sup> indicates equal contribution.</p>

<div style="background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ec 100%); padding: 20px; border-radius: 12px; margin: 15px 0;">

<strong>Suspicious Alignment of SGD: A Fine-Grained Step Size Condition Analysis</strong><br>
<span style="color: #555;"><strong>Shenyang Deng</strong>, Boyao Liao, Zhuoli Ouyang, Tianyu Pang, Minhak Song, Yaoqing Yang</span><br>
<em>The 37th International Conference on Algorithmic Learning Theory (ALT)</em>, 2026<br>
🏆 <span style="color: #E74C3C; font-weight: bold;">Best Student Paper Award</span><br>
<a href="https://arxiv.org/abs/2601.11789">[arxiv]</a> <a href="https://drive.google.com/file/d/1VIR-OjXcosWFBDb9lUU_AEeEEqCc3xLu/view?usp=sharing">[download]</a>

</div>

<div style="display: flex; justify-content: center; margin: 18px 0 24px 0;">
  <div style="width: min(52%, 520px); height: 210px; display: flex; align-items: center; justify-content: center; padding: 12px; border: 1px solid rgba(0,0,0,0.08); border-radius: 12px; box-shadow: 0 3px 12px rgba(0,0,0,0.08); background: #fff; overflow: hidden;">
    <img src="/images/con_figure_3agx_2.png" alt="Suspicious Alignment of SGD" style="width: 100%; height: 100%; object-fit: contain; border-radius: 8px;">
  </div>
</div>

<div style="background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ec 100%); padding: 20px; border-radius: 12px; margin: 15px 0;">

<strong>RMNP: Row-Momentum Normalized Preconditioning for Scalable Matrix-Based Optimization</strong><br>
<span style="color: #555;"><strong>Shenyang Deng</strong><sup>*</sup>, Zhuoli Ouyang<sup>*</sup>, Tianyu Pang, Zihang Liu, Ruochen Jin, Shuhua Yu, Yaoqing Yang</span><br>
<em>The 43rd International Conference on Machine Learning (ICML 2026)</em><br>
<a href="https://arxiv.org/abs/2603.20527">[arxiv]</a>

</div>

<div style="display: flex; justify-content: center; margin: 18px 0 24px 0;">
  <div style="width: min(60%, 620px); height: 240px; display: flex; align-items: center; justify-content: center; padding: 12px; border: 1px solid rgba(0,0,0,0.08); border-radius: 12px; box-shadow: 0 3px 12px rgba(0,0,0,0.08); background: #fff; overflow: hidden;">
    <img src="/images/precc3_01.png" alt="RMNP" style="width: 100%; height: 100%; object-fit: contain; border-radius: 8px;">
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

<div style="margin: 10px 0 18px 0; font-size: 0.97em; line-height: 1.5;">
  <div style="display: grid; grid-template-columns: 105px 1fr; gap: 10px; padding: 8px 0; border-bottom: 1px solid rgba(0,0,0,0.08); align-items: start;">
    <strong>2025.11.27</strong>
    <span><strong>Suspicious Alignment of SGD</strong><br>Dartmouth--Berkeley--Rice AI Reading Group · <a href="https://drive.google.com/file/d/1ByfsVsaRM7DG_HPKRijWwpkVApFOgjHx/view?usp=sharing">Recording</a></span>
  </div>
  <div style="display: grid; grid-template-columns: 105px 1fr; gap: 10px; padding: 8px 0 0 0; align-items: start;">
    <strong>2026.02.26</strong>
    <span><strong>Suspicious Alignment of SGD</strong><br>The Fields Institute · <a href="https://www.youtube.com/watch?v=uRXzDT5L_Sk&t=2761s">Recording</a></span>
  </div>
</div>

---

## 🍽️ Miscellaneous

I am a food enthusiast who loves both eating and cooking. I enjoy preparing a hearty dinner after a busy work schedule and then rewarding myself with a game of **StarCraft II** 🎮. Here are some photos of the dishes I have made: [**See Gallery →**](/gallery/)
