---
layout: default
title: Play Doom
---

# Play Doom

Relive the classic game right in your browser! Use the controls below to start playing.

<div id="jsdos-container" style="width: 100%; max-width: 800px; height: 600px; margin: 2rem auto; border: 2px solid #00ff00; background: black; position: relative;"></div>

<script src="https://js-dos.com/6.22/current/js-dos.js"></script>
<script>
  document.addEventListener('DOMContentLoaded', () => {
    const container = document.getElementById('jsdos-container');
    if (container && typeof Dos !== 'undefined') {
      // Try to load Doom from js-dos CDN
      Dos(container, {
        wdosboxUrl: "https://js-dos.com/6.22/current/wdosbox.js",
      }).run("https://js-dos.com/6.22/demos/doom.jsdos").catch((error) => {
        console.error('Doom loading error:', error);
        // Fallback message
        container.innerHTML = '<div style="color: #ff0000; text-align: center; padding: 2rem;"><p>Unable to load Doom at this time.</p><p style="font-size: 0.9rem; margin-top: 1rem;">The game server may be temporarily unavailable. Please try again later.</p></div>';
      });
    } else {
      container.innerHTML = '<p style="color: #ff0000; text-align: center; padding: 2rem;">Doom emulator failed to initialize. Please refresh the page.</p>';
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
