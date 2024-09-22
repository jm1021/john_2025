---
layout: base
title: RPG
permalink: /rpg/
---

<canvas id='gameCanvas'></canvas>

<script type="module">
    import GameControl from '{{site.baseurl}}/assets/js/rpg/GameControl.js';

    // Background data
    const background_src = "{{site.baseurl}}/images/rpg/water.png";
    const background_data = {
        pixels: {height: 580, width: 1038}
    };
    const background = {src: background_src, data: background_data};

    // Sprite data
    const sprite_src = "{{site.baseurl}}/images/rpg/turtle.png";
    const sprite_data = {
        pixels: {height: 280, width: 256},
        orientation: {rows: 4, columns: 3 },
        front: {row: 0, start: 0, images: 3 },
        left: {row: 1, start: 0, images: 3 },
        right: {row: 2, start: 0, images: 3 },
        back: {row: 3, start: 0, images: 3 },
    };
    const sprite = {src: sprite_src, data: sprite_data};

    // Assets for game
    const assets = {background: background, sprite: sprite}

    // Start game engine
    GameControl.start(assets);
</script>