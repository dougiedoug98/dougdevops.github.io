---
layout: default
title: Play Doom
---

# Play Doom

Relive the classic game right in your browser! Use the controls below to start playing.

<div id="jsdos-container" style="width: 100%; max-width: 800px; height: 600px; margin: 2rem auto; border: 2px solid #00ff00; background: black;"></div>

<script src="https://js-dos.com/6.22/current/js-dos.js"></script>
<script>
  document.addEventListener('DOMContentLoaded', () => {
    const container = document.getElementById('jsdos-container');
    if (container && typeof Dos !== 'undefined') {
      Dos(container).run("https://cdn.dos.zone/original/2X/e/e476457f5c2cc3adea37b0c40eb0264da9c8bbe8.jsdos").catch((error) => {
        container.innerHTML = '<p style="color: #ff0000; text-align: center; padding: 2rem;">Error loading Doom. Please check your internet connection.</p>';
        console.error('Doom loading error:', error);
      });
    }
  });
</script>

<p style="text-align: center; margin-top: 1rem;">Note: This game is embedded directly into the page. Performance may vary depending on your browser.</p>

<style>
  #jsdos-container canvas {
    width: 100% !important;
    height: 100% !important;
  }
</style>
