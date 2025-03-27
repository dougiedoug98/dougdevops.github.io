---
layout: default
title: Play Doom
---

# Play Doom

Relive the classic game right in your browser! Use the controls below to start playing.

<div id="jsdos-container" style="width: 800px; height: 600px; margin: 0 auto; border: 2px solid #00ff00;"></div>

<script src="https://js-dos.com/6.22/current/js-dos.js"></script>
<script>
  document.addEventListener('DOMContentLoaded', () => {
    const container = document.getElementById('jsdos-container');
    Dos(container).run("https://js-dos.com/DOOM/doom.jsdos"); // Use external URL
  });
</script>

<p style="text-align: center;">Note: This game is embedded directly into the page. Performance may vary depending on your browser.</p>
