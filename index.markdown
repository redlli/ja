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
    padding: 60px 20px;
    text-align: center;
    background-color: #0b0b0b; /* Deep black section background */
  }
  .section.projects h2 {
    font-size: 2.8em;
    margin-bottom: 40px;
    color: #ffffff;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 2px;
  }
  .project-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 35px;
    width: 90%;
    max-width: 1200px;
    margin: 20px auto;
  }
  .card {
    background-color: #1e1e1e; /* Sleek dark card */
    border: 1px solid #2a2a2a;
    border-radius: 16px; /* Smooth rounded corners */
    padding: 25px;
    text-align: center;
    box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.5);
    transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.3s ease, border-color 0.3s ease;
  }
  .card:hover {
    transform: translateY(-10px) scale(1.02); /* Pop-up lift effect */
    border-color: #ff2a2a; /* Red border on hover */
    box-shadow: 0px 15px 35px rgba(255, 42, 42, 0.25); /* Gaming neon red glow */
  }
  .card img {
    width: 120px;
    height: 120px;
    object-fit: cover;
    margin: 0 auto 20px auto;
    border: 3px solid #111111; /* Sharp black border */
    border-radius: 22px;       /* App-style squircle corners */
    display: block;
    box-shadow: 0 4px 10px rgba(0,0,0,0.4);
    background-color: #151515;
  }
  .card h3 {
    color: #ff2a2a; /* Tech red title */
    font-size: 1.6em;
    margin-bottom: 12px;
    font-weight: 700;
  }
  .card p {
    color: #b3b3b3; /* Highly readable secondary text */
    font-size: 0.95em;
    line-height: 1.5;
    margin-bottom: 25px;
  }
  .card a {
    display: inline-block;
    text-decoration: none;
    color: #ffffff;
    font-weight: 600;
    padding: 10px 24px;
    background: #007bff;
    border-radius: 8px;
    transition: background 0.2s ease, transform 0.2s ease, box-shadow 0.2s ease;
    box-shadow: 0 4px 15px rgba(0, 123, 255, 0.3);
  }
  .card a:hover {
    background: #0069d9;
    box-shadow: 0 6px 20px rgba(0, 123, 255, 0.5);
  }

  /* Scrolling Ticker */
  .ticker-wrapper {
    overflow: hidden;
    background-color: #111;
    border-top: 1px solid #222;
    border-bottom: 1px solid #222;
    padding: 10px 0;
    width: 100%;
  }
  .ticker-content {
    display: inline-block;
    white-space: nowrap;
    animation: scrollTicker 20s linear infinite;
    color: #888;
    font-size: 1em;
  }
  .ticker-content p {
    margin: 0;
  }
  @keyframes scrollTicker {
    from { transform: translateX(100%); }
    to { transform: translateX(-100%); }
  }
</style>

<div class="section projects">
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
    <p>New Projects adding soon. This website is still in development phase. You might face bugs using it. Feel free to report it.</p>
  </div>
</div>
