---
layout: default
title: Retro Arcade
---

# Space Invaders

Take a break and defend Earth from the alien invasion! Click the button below to start playing.

<div id="game-selector" style="text-align: center; margin: 2rem auto; max-width: 900px;">
  <button onclick="loadGame()" class="game-btn" style="padding: 1rem 2rem; font-size: 1.2rem;">
    <span style="font-size: 2rem; display: block; margin-bottom: 0.5rem;">👾</span>
    Play Space Invaders
  </button>
</div>

<div id="game-container" style="width: 100%; max-width: 800px; height: 600px; margin: 2rem auto; border: 2px solid #00ff00; background: black; display: none;">
  <iframe id="game-frame" width="100%" height="100%" frameborder="0" style="display: block;"></iframe>
</div>

<div id="game-info" style="text-align: center; margin-top: 1rem; display: none;">
  <p style="color: #00ff00;"><strong>Controls:</strong> Arrow Keys = Move | Space = Fire</p>
  <button onclick="closeGame()" class="tech-button" style="margin-top: 1rem;">Close Game</button>
</div>

<style>
  .game-btn {
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    color: #00ff00;
    background: black;
    border: 2px solid #00ff00;
    border-radius: 5px;
    cursor: pointer;
    font-family: 'Courier New', Courier, monospace;
    transition: all 0.3s ease;
    box-shadow: 0 0 10px rgba(0, 255, 0, 0.3);
  }

  .game-btn:hover {
    background: #00ff00;
    color: black;
    box-shadow: 0 0 15px rgba(0, 255, 0, 0.6);
    transform: translateY(-2px);
  }
</style>

<script>
  let gameActive = false;

  function loadGame() {
    const gameFrame = document.getElementById('game-frame');
    const gameContainer = document.getElementById('game-container');
    const gameInfo = document.getElementById('game-info');
    const gameSelector = document.getElementById('game-selector');

    gameFrame.src = 'https://freeinvaders.org/';
    gameContainer.style.display = 'block';
    gameInfo.style.display = 'block';
    gameSelector.style.display = 'none';
    gameActive = true;

    // Scroll to game
    gameContainer.scrollIntoView({ behavior: 'smooth', block: 'center' });

    // Prevent arrow key scrolling when game is active
    enableArrowKeyBlock();
  }

  function closeGame() {
    const gameFrame = document.getElementById('game-frame');
    const gameContainer = document.getElementById('game-container');
    const gameInfo = document.getElementById('game-info');
    const gameSelector = document.getElementById('game-selector');

    gameFrame.src = '';
    gameContainer.style.display = 'none';
    gameInfo.style.display = 'none';
    gameSelector.style.display = 'block';
    gameActive = false;

    // Re-enable arrow key scrolling
    disableArrowKeyBlock();

    // Scroll back to game selector
    gameSelector.scrollIntoView({ behavior: 'smooth', block: 'start' });
  }

  // Prevent arrow keys from scrolling the page
  function preventArrowScroll(e) {
    if (gameActive && ['ArrowUp', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'Space'].includes(e.code)) {
      e.preventDefault();
    }
  }

  function enableArrowKeyBlock() {
    window.addEventListener('keydown', preventArrowScroll);
  }

  function disableArrowKeyBlock() {
    window.removeEventListener('keydown', preventArrowScroll);
  }
</script>

<p style="text-align: center; margin-top: 2rem; font-size: 0.9rem; color: #888;">
  The classic arcade game is embedded and runs directly on this page. Use arrow keys to move and space to fire!
</p>
