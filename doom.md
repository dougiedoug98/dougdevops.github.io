---
layout: default
title: Retro Arcade
---

# Retro Arcade

Take a break and play some classic games right here on the page!

<div id="game-selector" style="text-align: center; margin: 2rem auto; max-width: 900px;">
  <h2 style="color: #00ff00; margin-bottom: 1rem;">Select a Game</h2>
  <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 0.75rem; margin-bottom: 2rem;">
    <button onclick="loadGame('tetris')" class="game-btn">
      <span style="font-size: 1.2rem;">🟦</span> Tetris
    </button>
    <button onclick="loadGame('snake')" class="game-btn">
      <span style="font-size: 1.2rem;">🐍</span> Snake
    </button>
    <button onclick="loadGame('breakout')" class="game-btn">
      <span style="font-size: 1.2rem;">🧱</span> Breakout
    </button>
    <button onclick="loadGame('pong')" class="game-btn">
      <span style="font-size: 1.2rem;">🏓</span> Pong
    </button>
    <button onclick="loadGame('spaceinvaders')" class="game-btn">
      <span style="font-size: 1.2rem;">👾</span> Space Invaders
    </button>
  </div>
</div>

<div id="game-container" style="width: 100%; max-width: 800px; height: 600px; margin: 0 auto; border: 2px solid #00ff00; background: black; display: none;">
  <iframe id="game-frame" width="100%" height="100%" frameborder="0" style="display: block;"></iframe>
</div>

<div id="game-info" style="text-align: center; margin-top: 1rem; display: none;">
  <p style="color: #00ff00;"><strong>Controls:</strong> <span id="controls-text">Use arrow keys</span></p>
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
  const games = {
    tetris: {
      url: 'https://www.google.com/logos/2020/july4th20/rc4/july4th20.html?hl=en',
      controls: 'Arrow Keys = Move/Rotate | Space = Drop'
    },
    snake: {
      url: 'https://www.google.com/fbx?fbx=snake_arcade',
      controls: 'Arrow Keys = Direction'
    },
    breakout: {
      url: 'https://elgoog.im/breakout/',
      controls: 'Mouse or Arrow Keys = Move Paddle'
    },
    pong: {
      url: 'https://www.ponggame.org/',
      controls: 'Mouse = Move Paddle'
    },
    spaceinvaders: {
      url: 'https://freeinvaders.org/',
      controls: 'Arrow Keys = Move | Space = Fire'
    }
  };

  function loadGame(gameId) {
    const game = games[gameId];
    const gameFrame = document.getElementById('game-frame');
    const gameContainer = document.getElementById('game-container');
    const gameInfo = document.getElementById('game-info');
    const controlsText = document.getElementById('controls-text');

    gameFrame.src = game.url;
    controlsText.textContent = game.controls;
    gameContainer.style.display = 'block';
    gameInfo.style.display = 'block';

    // Scroll to game
    gameContainer.scrollIntoView({ behavior: 'smooth', block: 'center' });
  }

  function closeGame() {
    const gameFrame = document.getElementById('game-frame');
    const gameContainer = document.getElementById('game-container');
    const gameInfo = document.getElementById('game-info');

    gameFrame.src = '';
    gameContainer.style.display = 'none';
    gameInfo.style.display = 'none';

    // Scroll back to game selector
    document.getElementById('game-selector').scrollIntoView({ behavior: 'smooth', block: 'start' });
  }
</script>

<p style="text-align: center; margin-top: 2rem; font-size: 0.9rem; color: #888;">
  Click a game above to start playing. All games are embedded and run directly on this page!
</p>
