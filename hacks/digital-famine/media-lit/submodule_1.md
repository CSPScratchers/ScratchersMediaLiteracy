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
author: "Aashika Patel, Varada Vichare"
date: 2025-10-21
---

# Awareness: Media Purpose Training

<<<<<<< HEAD
<div class="intro-text">
Welcome to <strong>Media Literacy Planet</strong>! The alien invaders are hurling pieces of news at you in an attempt to scramble human understanding. Your mission: <strong>sort each artifact by its purpose: Persuade, Inform, or Sell</strong>. Every correct choice strengthens your protective shield. Reach a score of <strong>7</strong> to unlock <strong>Shield Level 1</strong> and advance to the next challenge in recovering from the digital famine. 
</div>

<style>
body {
  min-height: 100vh;
  background: url('https://img.freepik.com/free-vector/space-ship-window-with-space-planets-stars-cartoon-vector-illustration_1284-16119.jpg') no-repeat center center fixed;
  background-size: cover;
  font-family: system-ui, -apple-system, sans-serif;
  color: #ffffff;
  overflow-x: hidden;
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
  background: rgba(0,0,50,0.4);
  border: 2px dashed #00ccff;
  border-radius: 14px;
  padding: 12px;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: all 0.3s ease;
}

.bin.highlight {
  background: rgba(0,204,255,0.25);
  border-color: #00f;
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
  background: #00ccff;
  color: black;
}

.btn-ghost {
  background: rgba(255,255,255,0.2);
  color: white;
}

.btn:hover {
  transform: translateY(-1px);
  box-shadow: 0 2px 10px rgba(0,0,0,0.5);
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

.shield img {
  width: 100%;
  height: 100%;
  object-fit: contain;
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

/* On-screen center notification */
.notification {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #00ccff;
  color: black;
  padding: 25px 35px;
  border-radius: 12px;
  font-weight: 700;
  font-size: 1.3rem;
  z-index: 1000;
  box-shadow: 0 0 25px rgba(0,0,0,0.6);
  display: none;
  text-align: center;
}
</style>

<div class="game-screen">
  <div class="game-header">
    <div class="info-pill" id="player-name">Player: Guest</div>
    <div class="info-pill" id="score">Score: 0</div>
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
    <button class="btn btn-primary" id="submit-btn">Submit Score</button>
  </div>

  <div class="shield" id="shield">
    <img src="https://img.freepik.com/premium-vector/security_1162360-7974.jpg?semt=ais_hybrid&w=740&q=80" alt="Shield Icon">
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
</div>

<div class="notification" id="notification">Congratulations. Shield Level 1 has been achieved. Proceed to the next mission.</div>

<script>
const ARTIFACTS = [
  { text: "VOTE FOR A GREENER FUTURE!", purpose: "Persuade" },
  { text: "GLOBAL WARMING RISES 1.5°C BY 2030", purpose: "Inform" },
  { text: "BUY THE NEW GALAXY SMARTPHONE TODAY!", purpose: "Sell" },
  { text: "JOIN SOCIAL MOVEMENT FOR EDUCATION REFORM", purpose: "Persuade" },
  { text: "LOCAL ELECTION RESULTS ANNOUNCED", purpose: "Inform" },
  { text: "LIMITED EDITION SNEAKERS AVAILABLE ONLINE", purpose: "Sell" },
  { text: "SUPPORT ANIMAL WELFARE CAMPAIGNS", purpose: "Persuade" },
  { text: "NASA DISCOVERS NEW EXOPLANET", purpose: "Inform" }
];

let score = 0;
let currentPlayer = "Guest";
let placedArtifacts = new Set();
let shieldGrowing = false;

const scoreDisplay = document.getElementById("score");
const playerDisplay = document.getElementById("player-name");
const artifactsArea = document.getElementById("artifacts");
const bins = document.querySelectorAll(".bin");
const shieldEl = document.getElementById("shield");
const notification = document.getElementById("notification");

function updateDisplays() {
  scoreDisplay.textContent = `Score: ${score}`;
  playerDisplay.textContent = `Player: ${currentPlayer}`;
}

function createArtifactCard(artifact, index) {
  const div = document.createElement("div");
  div.className = "artifact";
  div.textContent = artifact.text;
  div.draggable = true;
  div.dataset.purpose = artifact.purpose;
  div.dataset.id = `artifact-${index}`;

  div.addEventListener("dragstart", (e) => {
    if (placedArtifacts.has(div.dataset.id)) { e.preventDefault(); return; }
    div.classList.add("dragging");
    e.dataTransfer.setData("text/plain", div.dataset.id);
  });

  div.addEventListener("dragend", () => div.classList.remove("dragging"));

  return div;
}

function initGame() {
  artifactsArea.innerHTML = '';
  document.querySelectorAll(".bin-content").forEach(b => b.innerHTML = '');
  placedArtifacts.clear();
  score = 0;
  shieldGrowing = false;
  shieldEl.style.transform = 'translate(-50%, -50%) scale(0)';
  notification.style.display = 'none';
  updateDisplays();

  ARTIFACTS.sort(() => Math.random() - 0.5).forEach((artifact, i) => {
    artifactsArea.appendChild(createArtifactCard(artifact, i));
  });
}

bins.forEach(bin => {
  bin.addEventListener("dragover", e => { e.preventDefault(); bin.classList.add("highlight"); });
  bin.addEventListener("dragleave", () => bin.classList.remove("highlight"));
  bin.addEventListener("drop", e => {
    e.preventDefault();
    bin.classList.remove("highlight");
    const id = e.dataTransfer.getData("text/plain");
    const artifact = document.querySelector(`[data-id="${id}"]`);
    if (!artifact || placedArtifacts.has(id)) return;

    if (artifact.dataset.purpose === bin.dataset.bin) {
      bin.querySelector(".bin-content").appendChild(artifact);
      placedArtifacts.add(id);
      score++;
      showShieldEffect();
      if (score >= 7 && !shieldGrowing) { showShieldComplete(); }
    } else {
      artifact.animate([{ transform: "translateX(0)" }, { transform: "translateX(-5px)" }, { transform: "translateX(5px)" }, { transform: "translateX(0)" }], { duration: 300 });
    }
    updateDisplays();
  });
});

function showShieldEffect() {
  let currentScale = parseFloat(shieldEl.style.transform.match(/scale\(([\d.]+)\)/)?.[1]) || 0;
  shieldEl.style.transform = `translate(-50%, -50%) scale(${currentScale + 0.15})`;
}

function showShieldComplete() {
  shieldGrowing = true;
  let scale = parseFloat(shieldEl.style.transform.match(/scale\(([\d.]+)\)/)?.[1]) || 1;
  shieldEl.style.display = 'flex';
  notification.style.display = 'block';
  
  function grow() {
    scale += 0.05;
    shieldEl.style.transform = `translate(-50%, -50%) scale(${scale})`;
    if (scale < 15) {
      requestAnimationFrame(grow);
    } else {
      // After 5 seconds, hide shield & notification
      setTimeout(() => {
        shieldEl.style.display = 'none';
        notification.style.display = 'none';
      }, 5000);
    }
  }
  grow();
}

function autofillArtifacts() {
  ARTIFACTS.forEach((a, i) => {
    const bin = Array.from(bins).find(b => b.dataset.bin === a.purpose);
    const artifact = document.querySelector(`[data-id="artifact-${i}"]`);
    bin.querySelector(".bin-content").appendChild(artifact);
    placedArtifacts.add(artifact.dataset.id);
    score++;
    showShieldEffect();
  });
  updateDisplays();
  if (score >= 7 && !shieldGrowing) { showShieldComplete(); }
}

document.getElementById("reset-btn").addEventListener("click", initGame);
document.getElementById("autofill-btn").addEventListener("click", autofillArtifacts);
document.getElementById("submit-btn").addEventListener("click", () => {
  alert(`Score submitted: ${score}`);
  initGame();
});

updateDisplays();
initGame();
</script>
=======
# Awareness: Your First Line of Defense in the Digital World 🛡️

Every day, we are surrounded by information. From social media feeds and news websites to YouTube videos, podcasts, and messages from friends or family, the amount of content we encounter is overwhelming. But here’s the truth: **not everything we see or read is accurate.** Some information is misleading, some is biased, and some is deliberately false.  

In today’s fast-paced digital world, being able to **analyze, question, and evaluate information**—a skill called media literacy—is not just helpful, it’s essential. Media literacy is your first line of defense against misinformation, disinformation, and manipulation. Without it, it’s easy to fall for content that looks true but is designed to deceive.  

---

## Types of Information 📰

To protect ourselves, we first need to understand the types of information we might encounter:

- **Accurate, fact-checked information ✅**  
  This comes from credible sources and is backed by verifiable evidence. It provides a complete picture, presents facts in context, and allows readers to form informed opinions. For example, an article from a reputable news outlet citing multiple experts is more reliable than a random post on social media.  

- **Misinformation ⚠️**  
  False or misleading information shared unintentionally. People often spread misinformation because they assume it’s true or they don’t check the facts. A common example is a viral post claiming a celebrity did something shocking, which turns out to be completely false.  

- **Disinformation ❌**  
  Deliberately false or misleading content created to deceive. Disinformation is designed to influence opinions, emotions, or behavior. For instance, political disinformation may present selective facts or fake polls to sway public perception, while health-related disinformation might promote unsafe remedies.  

---

## Propaganda and Manipulation Techniques 🎭

One of the most powerful forms of disinformation is **propaganda**. Propaganda is information that is often biased or misleading, designed to shape public opinion or behavior. Here are some common techniques:

- **Emotional appeals ❤️🔥**  
  Propaganda often targets our emotions rather than our reasoning. Posts may use fear, anger, or urgency to get us to act quickly without thinking critically. For example, a social media post claiming a food product is dangerous without evidence may make people panic and share it widely.  

- **Exaggeration 📢**  
  This involves stretching the truth or presenting extreme scenarios to grab attention. Headlines like “BREAKING: The world is ending tomorrow!” are designed to shock and go viral, even if the content is false.  

- **Selective reporting 🎯**  
  This technique shares only part of a story, leaving out critical facts. By presenting one side or omitting context, propaganda can make an issue seem more extreme or one-sided than it actually is.  

- **Fake visuals or deepfakes 🎥**  
  Videos and images can be manipulated to mislead viewers. For example, a video might be edited to show a public figure saying something they never actually said, creating a false impression. Technology has made it easier than ever to create realistic but fake visuals.  

- **Bandwagon and peer pressure 👫**  
  Content may suggest “everyone believes this” or “everyone is doing this,” pushing you to conform without evaluating the facts yourself. This technique relies on social proof rather than truth.  

---

## Why Awareness Matters 🤔

You might wonder, “Why should I care? Why not just scroll past?” The truth is, misinformation and propaganda have real-world consequences. False information can harm people’s health, spread fear, influence elections, and create distrust in institutions. Even one post shared without verification can ripple through social networks, misleading hundreds or thousands of people.  

Being aware protects not just yourself, but your community. A single critical thinker who pauses to fact-check can prevent false content from spreading further. Awareness allows you to think critically, ask questions, and make informed decisions instead of reacting impulsively.  

---

## How to Protect Yourself 🛡️

Developing awareness starts with simple, consistent habits:

1. **Question the source ❓**  
   Always ask: Who created this content? Is it a reputable organization, a verified journalist, or just a random social media page?  

2. **Check the evidence 📊**  
   Reliable information is usually supported by verifiable facts, studies, or multiple credible sources. Be skeptical of content that relies solely on opinions or unnamed sources.  

3. **Consider bias ⚖️**  
   Even accurate information can be framed in a way that promotes a specific agenda. Understanding bias allows you to think critically about the context and intent behind the content.  

4. **Pause before sharing ⏸️**  
   Many posts are designed to make you act quickly. Take a moment to think: “Am I reacting to facts, or to emotions?”  

5. **Encourage critical thinking in others ✅**  
   Share verified information and model media literacy for friends and family. Awareness spreads just like information, but in a positive way.  

---

## Real-World Examples 💡

- A viral post claiming a celebrity said something controversial—often false, spreads quickly because it’s sensational.  
- Health tips shared on social media without evidence—these can be dangerous if people follow unsafe advice.  
- Political posts highlighting only one side of a story—can influence opinions unfairly.  
- Deepfake videos that appear real, tricking viewers into believing events never happened.  

These examples show why it’s so important to be vigilant, think critically, and question everything you see online.  

---

## Final Thoughts 🌟

In today’s digital world, information spreads faster than ever. Awareness is no longer optional—it’s essential. It’s your responsibility, your shield, and your tool for navigating the online world safely. **Stay curious, stay critical, and stay informed.**  

By practicing media literacy, you strengthen your ability to separate fact from fiction, make informed choices, and protect not only yourself but also your community. Your **awareness is your first and most powerful line of defense.**  

Remember: in the digital age, thinking critically about what you see, hear, and share is not just smart—it’s essential.  

>>>>>>> ab0aab1e2 (script for video)
