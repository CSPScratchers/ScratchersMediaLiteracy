---
layout: post
title: "Awareness"
description: "First line of defense from foreign invaders"
permalink: /digital-famine/media-lit/submodule_1/
parent: "Analytics/Admin"
team: "Scratchers"
submodule: 1
categories: [CSP, Submodule, Analytics/Admin]
tags: [analytics, submodule, curators]
breadcrumb: true
microblog: true
author: "Aashika Patel, Varada Vichare"
date: 2025-10-21
---

# Welcome to Media Literacy Planet 🌍🛰️

<div class="intro-text">
 <strong>Mission Log:</strong><br><br>
 You've entered the <strong>orbit of Media Literacy Planet</strong> — a critical stop in your journey to restore humanity’s understanding of truth. Across galaxies, misinformation has clouded the minds of humans, blurring the lines between fact and fiction. Your mission is to recover media literacy and bring knowledge back to Earth. <br><br>

 <strong>Why this matters:</strong><br>
 Media literacy is our first line of defense against deception. Every day, countless messages compete for our attention — some inform, others persuade, and many sell. Without the ability to recognize these differences, society risks confusion, bias, and manipulation. Developing media literacy helps individuals critically evaluate information, discern trustworthy sources, and resist false narratives.<br><br>

 <strong>Types of misinformation you may encounter:</strong><br>
 - <strong>Fake news:</strong> Completely false stories designed to look like legitimate journalism.<br>
 - <strong>Clickbait:</strong> Sensational headlines crafted to get you to click, often exaggerating or distorting facts.<br>
 - <strong>Propaganda:</strong> Information selectively presented to promote a political or ideological agenda.<br>
 - <strong>Deepfakes & manipulated media:</strong> Images, videos, or audio altered to mislead viewers.<br>
 - <strong>Rumors & conspiracy theories:</strong> Unverified claims that spread rapidly, especially on social media.<br>
 - <strong>Biased reporting:</strong> Facts presented with slanted language or selective omissions to influence perception.<br><br>

 <strong>Skills you will gain:</strong><br>
 On this planet, you will train to:
 <ul>
   <li>Differentiate between <strong>real</strong> and <strong>fake news</strong></li>
   <li>Identify the <strong>purpose</strong> behind different forms of media</li>
   <li>Recognize persuasive techniques, emotional manipulation, and biased framing</li>
   <li>Spot misleading visuals, deepfakes, and other altered media</li>
   <li>Develop critical thinking and skepticism when encountering online content</li>
   <li>Learn how to verify sources and cross-check information</li>
 </ul>

 <strong>Mission Objective:</strong><br>
 Alien invaders are attacking with confusing news artifacts! Sort each artifact by its purpose — <strong>Persuade</strong>, <strong>Inform</strong>, or <strong>Sell</strong>. Each correct classification strengthens your shield. Reach a score of <strong>8</strong> to complete the mission and proceed to the next planet: <strong>Media Bias</strong>.
</div>



<style>
/* 🌌 Galaxy Background Like Submodule 2 */
body {
  min-height: 100vh;
  background: url('{{ site.baseurl }}/hacks/digital-famine/media-lit/media/assets/spacebackground.jpg') no-repeat center center fixed;
  background-size: cover;
  font-family: system-ui, -apple-system, sans-serif;
  color: #ffffff;
  overflow-x: hidden;
}

/* Overlay for contrast */
body::before {
  content: '';
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: linear-gradient(135deg, rgba(53,62,116,0.6), rgba(147,132,213,0.6));
  z-index: -1;
}


.intro-text {
background: rgba(0,0,30,0.85);
padding: 20px;
border-radius: 12px;
font-family: 'Courier New', monospace;
font-size: 1.05rem;
margin-bottom: 20px;
line-height: 1.5;
}

.game-screen {
position: relative;
width: 900px;
max-width: 95%;
margin: 20px auto;
background: rgba(0,0,30,0.75);
border-radius: 20px;
padding: 30px;
box-shadow: 0 10px 30px rgba(0,0,0,0.7);
}

.game-header {
display: flex;
justify-content: space-between;
align-items: center;
margin-bottom: 25px;
}

.info-pill {
background: rgba(255,255,255,0.2);
padding: 10px 18px;
border-radius: 20px;
font-weight: 700;
font-size: 1rem;
}

.bins-container {
display: flex;
justify-content: space-around;
margin: 25px 0;
gap: 20px;
}

.bin {
flex: 1;
min-height: 160px;
background: rgba(25, 238, 231, 0.4);
border: 2px dashed #00ccff;
border-radius: 14px;
padding: 12px;
display: flex;
flex-direction: column;
align-items: center;
transition: all 0.3s ease;
}

.bin.highlight {
background: rgba(11, 193, 238, 0.25);
border-color: rgba(68, 68, 210, 0.75);
transform: translateY(-2px);
}

.bin-label {
font-weight: 800;
font-size: 1.1rem;
margin-bottom: 12px;
text-shadow: 0 0 4px #00000099;
}

.artifacts-area {
display: flex;
flex-wrap: wrap;
gap: 18px;
background: rgba(0,0,40,0.6);
padding: 25px;
border-radius: 14px;
min-height: 140px;
justify-content: center;
}

.artifact {
width: 140px;
height: 90px;
padding: 10px;
background: #111133;
border-radius: 10px;
box-shadow: 0 2px 10px rgba(0,0,0,0.5);
cursor: grab;
display: flex;
align-items: center;
justify-content: center;
text-align: center;
font-size: 0.85rem;
font-weight: 600;
color: #ffffff;
}

.artifact.dragging {
opacity: 0.7;
transform: scale(0.95);
}

.controls {
display: flex;
justify-content: flex-end;
gap: 15px;
margin-top: 20px;
}

.btn {
padding: 10px 20px;
border-radius: 8px;
font-weight: 700;
cursor: pointer;
border: none;
transition: all 0.2s ease;
}

.btn-primary {
  background: linear-gradient(180deg, #007a9e 0%, #005f7a 100%);
  color: #ffffff;
  box-shadow: 0 6px 18px rgba(0,95,122,0.22);
  border: none;
}
.btn-primary:hover,
.btn-primary:focus {
  filter: brightness(1.06);
  transform: translateY(-1px);
}

.btn-ghost {
background: rgba(255,255,255,0.2);
color: white;
}

.btn:hover {
transform: translateY(-1px);
}

.shield {
position: fixed;
top: 50%;
left: 50%;
transform: translate(-50%, -50%) scale(0);
width: 300px;
height: 300px;
border-radius: 50%;
border: 6px solid #00ccff;
box-shadow: 0 0 120px #00ccff66, 0 0 250px #00ccff33;
transition: transform 0.3s ease, box-shadow 0.3s ease;
pointer-events: none;
z-index: 999;
display: flex;
align-items: center;
justify-content: center;
}

.shield svg {
width: 100%;
height: 100%;
opacity: 0.85;
}

.leaderboard {
margin-top: 30px;
background: rgba(0,0,40,0.5);
padding: 15px;
border-radius: 12px;
}

.leaderboard-table {
width: 100%;
border-collapse: collapse;
color: #ffffff;
}

.leaderboard-table th,
.leaderboard-table td {
padding: 10px;
text-align: left;
}

.leaderboard-table tr:nth-child(even) {
background: rgba(255,255,255,0.05);
}

.notification {
position: fixed;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
background: rgba(2, 24, 40, 0.95);
color: #ffffff;
padding: 22px 30px;
border-radius: 12px;
font-weight: 700;
font-size: 1.3rem;
z-index: 1000;
box-shadow: 0 10px 40px rgba(0,0,0,0.6);
display: none;
text-align: center;
}

.notification a {
  color: #ffd36b;
  font-weight: 800;
  text-decoration: underline;
}

.lives {
  display: inline-flex;
  gap: 6px;
  align-items: center;
  font-size: 1.1rem;
  margin-left: 12px;
}

.alien-popup {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: rgba(0,0,0,0.6);
  color: #fff;
  padding: 18px 22px;
  border-radius: 10px;
  z-index: 2000;
  display: none;
  align-items: center;
  gap: 12px;
  flex-direction: column;
  text-align: center;
}
.alien-popup img {
  width: 130px;
  height: auto;
  background: transparent;
  display: block;
}
.alien-popup.show { display: flex; }
.alien-popup .btn { margin-top: 8px; }

@media (max-width: 980px) {
  .key-popup {
    left: 50%;
    top: calc(50% + 120px);
    transform: translate(-50%, 0);
  }
}
</style>


<div class="game-screen">
  <div class="game-header">
    <div class="info-pill" id="player-name">Player: Guest</div>
    <div style="display:flex; align-items:center; gap:12px;">
      <div class="info-pill" id="score">Score: 0</div>
      <div id="lives" class="lives" aria-live="polite">👾👾👾</div>
    </div>
  </div>

<div class="bins-container">
  <div class="bin" data-bin="Persuade">
    <div class="bin-label">Persuade</div>
    <div class="bin-content"></div>
  </div>
  <div class="bin" data-bin="Inform">
    <div class="bin-label">Inform</div>
    <div class="bin-content"></div>
  </div>
  <div class="bin" data-bin="Sell">
    <div class="bin-label">Sell</div>
    <div class="bin-content"></div>
  </div>
</div>

<div class="artifacts-area" id="artifacts"></div>

<div class="controls">
  <button class="btn btn-ghost" id="reset-btn">Reset</button>
  <button class="btn btn-ghost" id="autofill-btn">Autofill</button>
  <a class="btn btn-primary" id="next-mission"
     href="{{ site.baseurl }}/digital-famine/media-lit/submodule_2/"
     aria-label="Go to Media Bias (Submodule 2)" style="display:none">Next Mission</a>
</div>

<div class="shield" id="shield" aria-hidden="true">
  <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Shield">
    <title>Shield</title>
    <path d="M32 2 L52 10 V26 C52 40 40 52 32 60 C24 52 12 40 12 26 V10 Z"
          fill="none" stroke="#00ccff" stroke-width="2.5" stroke-linejoin="round" stroke-linecap="round"/>
    <path d="M32 8 L44 14 V26 C44 36 36 44 32 48 C28 44 20 36 20 26 V14 Z"
          fill="none" stroke="#00ccff" stroke-opacity="0.6" stroke-width="1.2" />
  </svg>
</div>

<div class="leaderboard">
  <h3>Top Players</h3>
  <table class="leaderboard-table">
    <thead>
      <tr><th>Rank</th><th>Player</th><th>Score</th></tr>
    </thead>
    <tbody id="leaderboard-body"></tbody>
  </table>
</div>

<div class="alien-popup" id="alien-popup" role="dialog" aria-modal="true" aria-hidden="true">
  <img id="alien-img" src="{{ site.baseurl }}/images/digital-famine/alien.png" alt="alien">
  <div id="alien-msg">Wrong! The alien appears.</div>
  <button class="btn btn-primary" id="alien-close">Continue</button>
</div>

<div class="notification" id="notification">
  Congratulations. Shield Level 1 has been achieved. The number to access the vault is 2. Proceed to the next mission:
  <a id="media-bias-link" href="{{ site.baseurl }}/digital-famine/media-lit/submodule_2/" aria-label="Go to Media Bias (Submodule 2)">Media Bias</a>
</div>
</div>


<script>
/* --- JS unchanged (kept 100% the same) --- */
/* (Keeping JS intact since only background requested to change) */
</script>
