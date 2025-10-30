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

# Welcome to Media Literacy Planet 🌍🛰️

<div class="intro-text">
  <strong>Mission Log:</strong><br><br>
  You've entered the <strong>orbit of Media Literacy Planet</strong> — a critical stop in your journey to restore humanity’s understanding of truth. Across the galaxy, misinformation has clouded the minds of humans, blurring the lines between fact and fiction. Your mission is to recover media literacy and bring that knowledge back to Earth. <br><br>

  <strong>Why this matters:</strong><br>
  Media literacy is our first line of defense against deception. Every day, countless messages compete for our attention. Some media informs, others persuade, and many sell. Without the ability to recognize these differences, society risks confusion, bias, and manipulation.<br><br>

  <strong>Skills you will gain:</strong><br>
  On this planet, you will train to:
  <ul>
    <li>Differentiate between <strong>real</strong> and <strong>fake news</strong></li>
    <li>Identify the <strong>purpose</strong> behind different forms of media</li>
    <li>Recognize sources of bias in media and learn how to identify the truth</li>
    <li>Develop critical thinking and skepticism when encountering online content</li>
  </ul>

  <strong>Mission Objective:</strong><br>
  Alien invaders are attacking your spaceship with confusing news pieces! Sort each artifact by its purpose: <strong>Persuade</strong>, <strong>Inform</strong>, or <strong>Sell</strong>. Each correct classification strengthens your protective shield. Reach a score of <strong>7</strong> to complete the mission and proceed to your next mission: <strong>Media Bias</strong>.
</div>

<style>
body {
  min-height: 100vh;
  background: url('https://img.freepik.com/free-vector/space-ship-window-with-space-planets-stars-cartoon-vector-illustration_1284-16119.jpg') center center fixed;
  background-size: contain;
  background-color: black;
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
  overflow: hidden;
  position: relative;
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
  position: absolute;
  animation: flyIn 2s ease-out forwards;
}

@keyframes flyIn {
  0% { opacity: 0; transform: translateX(-100vw); }
  100% { opacity: 1; transform: translateX(0); }
}

.artifact.dragging {
  opacity: 0.7;
  transform: scale(0.95);
}

.controls {
  display: flex;
  justify-content: center;
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
  border: 6px solid rgba(0,204,255,0.6);
  box-shadow: 0 0 120px rgba(0,204,255,0.3), 0 0 250px rgba(0,204,255,0.2);
  transition: transform 0.3s ease;
  pointer-events: none;
  z-index: 999;
  opacity: 0.85;
  display: flex;
  align-items: center;
  justify-content: center;
}

.shield img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  filter: drop-shadow(0 0 10px #00ccff);
}

.alien {
  position: absolute;
  width: 100px;
  height: 100px;
  animation: alienFly 1.5s ease-in forwards;
  z-index: 999;
  pointer-events: none;
}

@keyframes alienFly {
  0% { opacity: 0; transform: translateY(-50px) scale(0.5); }
  50% { opacity: 1; transform: translateY(50px) scale(1); }
  100% { opacity: 0; transform: translateY(250px) scale(0.2); }
}

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

#next-submodule-btn {
  background: #00ccff;
  color: black;
  font-weight: 700;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.3s;
}

#next-submodule-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 0 10px rgba(0,204,255,0.6);
}
</style>

<div class="game-screen">
  <div class="game-header">
    <div class="info-pill" id="player-name">Player: Guest</div>
    <div class="info-pill" id="score">Score: 0</div>
  </div>

  <div class="bins-container">
    <div class="bin" data-bin="Persuade"><div class="bin-label">Persuade</div><div class="bin-content"></div></div>
    <div class="bin" data-bin="Inform"><div class="bin-label">Inform</div><div class="bin-content"></div></div>
    <div class="bin" data-bin="Sell"><div class="bin-label">Sell</div><div class="bin-content"></div></div>
  </div>

  <div class="artifacts-area" id="artifacts"></div>

  <div class="controls">
    <button class="btn btn-ghost" id="reset-btn">Reset</button>
    <button class="btn btn-ghost" id="autofill-btn">Autofill</button>
    <button class="btn btn-primary" id="next-submodule-btn" onclick="goToNextSubmodule()">Next Mission ➜</button>
  </div>

  <div class="shield" id="shield">
    <img src="https://i.ibb.co/m6YwkrW/security-shield.png" alt="Shield Icon">
  </div>
</div>

<div class="notification" id="notification">
  Congratulations. Shield Level 1 has been achieved.<br>
  Proceed to the next mission: <strong>Media Bias</strong>.
</div>

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
let placedArtifacts = new Set();
let shieldGrowing = false;

const artifactsArea = document.getElementById("artifacts");
const bins = document.querySelectorAll(".bin");
const shieldEl = document.getElementById("shield");
const notification = document.getElementById("notification");
const scoreDisplay = document.getElementById("score");

function updateDisplays() {
  scoreDisplay.textContent = `Score: ${score}`;
}

function createArtifactCard(artifact, index) {
  const div = document.createElement("div");
  div.className = "artifact";
  div.textContent = artifact.text;
  div.draggable = true;
  div.dataset.purpose = artifact.purpose;
  div.dataset.id = `artifact-${index}`;
  div.style.top = `${Math.random() * 150}px`;
  div.style.left = `${Math.random() > 0.5 ? "-200px" : "100%"}`;
  return div;
}

function spawnAlien() {
  const alien = document.createElement("img");
  alien.src = "https://i.ibb.co/pzDsc6P/alien-fly.png";
  alien.className = "alien";
  alien.style.left = `${Math.random() * 80 + 10}%`;
  alien.style.top = "0";
  artifactsArea.appendChild(alien);
  setTimeout(() => alien.remove(), 1500);
}

function initGame() {
  artifactsArea.innerHTML = "";
  placedArtifacts.clear();
  score = 0;
  shieldEl.style.transform = 'translate(-50%, -50%) scale(0)';
  notification.style.display = "none";
  shieldGrowing = false;
  updateDisplays();

  ARTIFACTS.sort(() => Math.random() - 0.5).forEach((artifact, i) => {
    artifactsArea.appendChild(createArtifactCard(artifact, i));
  });

  document.querySelectorAll(".artifact").forEach(div => {
    div.addEventListener("dragstart", e => {
      if (placedArtifacts.has(div.dataset.id)) { e.preventDefault(); return; }
      div.classList.add("dragging");
      e.dataTransfer.setData("text/plain", div.dataset.id);
    });
    div.addEventListener("dragend", () => div.classList.remove("dragging"));
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
      spawnAlien();
      artifact.animate([{ transform: "translateX(0)" }, { transform: "translateX(-5px)" }, { transform: "translateX(5px)" }, { transform: "translateX(0)" }], { duration: 300 });
    }
    updateDisplays();
  });
});

function showShieldEffect() {
  let currentScale = parseFloat(shieldEl.style.transform.match(/scale\\(([\d.]+)\\)/)?.[1]) || 0;
  shieldEl.style.transform = `translate(-50%, -50%) scale(${currentScale + 0.15})`;
}

function showShieldComplete() {
  shieldGrowing = true;
  let scale = parseFloat(shieldEl.style.transform.match(/scale\\(([\d.]+)\\)/)?.[1]) || 1;
  notification.style.display = "block";

  function grow() {
    scale += 0.05;
    shieldEl.style.transform = `translate(-50%, -50%) scale(${scale})`;
    if (scale < 15) requestAnimationFrame(grow);
    else {
      setTimeout(() => { shieldEl.style.display = "none"; }, 2000);
    }
  }
  grow();
}

document.getElementById("reset-btn").addEventListener("click", initGame);
document.getElementById("autofill-btn").addEventListener("click", () => {
  ARTIFACTS.forEach((a, i) => {
    const bin = Array.from(bins).find(b => b.dataset.bin === a.purpose);
    const artifact = document.querySelector(`[data-id="artifact-${i}"]`);
    bin.querySelector(".bin-content").appendChild(artifact);
    placedArtifacts.add(artifact.dataset.id);
    score++;
    showShieldEffect();
  });
  updateDisplays();
  if (score >= 7 && !shieldGrowing) showShieldComplete();
});

function goToNextSubmodule() {
  window.location.href = "{{ site.baseurl }}/digital-famine/media-lit/submodule_2/";
}

initGame();
</script>