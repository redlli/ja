---
title: JA
layout: def
permalink: /
icon: /assets/img/icons/JA_logo.png
description: Home page for JA explore Apps, Games and many more.... 
keywords: JA, JA by redlii, JA home page, app, JA apps, JA games
---

<style>

  /* Projects Section */
  .section.projects {
    padding: 40px 20px;
    text-align: center;
  }
  .section.projects h2 {
    font-size: 2.5em;
    margin-bottom: 30px;
    color: white;
  }
  .project-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    width: 90%;
    max-width: 1200px;
    margin: 20px auto;
  }
  .card {
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    padding: 20px;
    text-align: center;
    transition: transform 0.2s ease-in-out;
  }
  .card:hover {
    transform: scale(1.05);
  }
  .card img {
    width: 150px;
    height: auto;
    margin-bottom: 15px;
  }
  .card h3 {
    color: #4CAF50;
    font-size: 1.5em;
    margin-bottom: 10px;
  }
  .card p {
    color: #666;
    margin-bottom: 15px;
  }
  .card a {
    display: inline-block;
    text-decoration: none;
    color: #007bff;
    font-weight: bold;
    padding: 10px 20px;
    border: 1px solid #007bff;
    border-radius: 5px;
    transition: background-color 0.3s ease, color 0.3s ease;
  }
  .card a:hover {
    background-color: #007bff;
    color: white;
  }

  /* Scrolling Ticker */
  .ticker-wrapper {
    overflow: hidden;
    background-color: #222;
    margin-top: 10px;
    width: 100%;
  }
  .ticker-content {
    display: inline-block;
    white-space: nowrap;
    animation: scrollTicker 15s linear infinite;
    color: white;
    font-size: 1.2em;
    font-weight: bold;
  }
  @keyframes scrollTicker {
    from { transform: translateX(100%); }
    to { transform: translateX(-100%); }
  }
</style>

<div class="section projects">
  <h2>Projects</h2>
  <div class="project-container">
    {% for project in site.pages %}
    {% if project.path contains "Projects/" %}
    <div class="card">
      <img src="{{ project.icon | default: '/assets/img/default-icon.png' }}" alt="{{ project.title }} Icon">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description | default: 'Check out this awesome project!' | truncatewords: 20 }}</p>
      <a href="{{ project.url }}">Learn More</a>
    </div>
    {% endif %}
    {% endfor %}
  </div>
</div>

<div class="ticker-wrapper">
  <div class="ticker-content">
    <p>New Projects adding soon. This website is still in devlopement phase. You might face bugs useing it. feel free to report it.</p>
  </div>
</div>

