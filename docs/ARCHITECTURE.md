# Arquitetura — Geometry Dash

Aplicação HTML5 Canvas com JavaScript vanilla. O código principal está em `game.js`; `index.html` é a entrada e `styles.css` controla o canvas. O estado inclui menu, playing, paused, dead e complete; as fases são listas de obstáculos em coordenadas de mundo. O progresso é salvo localmente em `localStorage` na chave `gd_save2`. A simulação e renderização ainda compartilham o mesmo loop e a física está ligada ao frame rate; a separação e timestep fixo são prioridades futuras.

A etapa atual corrige o timeout de morte, reconstrução da geometria no resize, pausa ao ocultar a aba e retomada do áudio. Preserve `render_game_to_text` e `advanceTime` usados no teste automatizado.