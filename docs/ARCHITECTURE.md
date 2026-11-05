# Arquitetura — Little Dash Adventure
## Decisão
Aplicação 100% Web/PWA, hospedada como site estático. Não utiliza Kotlin, APK, Capacitor ou wrapper nativo.

## Componentes
- Interface sem framework: HTML semântico e CSS responsivo.
- Motor: Canvas 2D e requestAnimationFrame; física leve executada no cliente.
- Conteúdo: configuração declarativa dos mundos, fases, paletas e temas musicais.
- Persistência: localStorage para progresso e IndexedDB para preferências e foto familiar.
- Offline: Service Worker + Cache API, cache versionado e same-origin.
- Áudio: Web Audio API com motivos melódicos procedurais originais, ativados após interação do usuário.

## Dados locais
O progresso guarda versão do schema, estrelas, fases concluídas/desbloqueadas e personagem selecionado. A foto opcional é importada manualmente pelo responsável, recortada no navegador e armazenada como imagem local no IndexedDB. Não há upload, sincronização, telemetria ou reconhecimento facial.

## Loop do jogo
Avanço automático; toque para saltar; coleta de estrelas; obstáculos com recuperação assistida; efeitos de partículas; vitória e recompensa. O jogo não pune erros com perda de vida ou reinício obrigatório.

## Performance
Canvas dimensionado com pixel ratio máximo 2; requestAnimationFrame; cache estático; animação reduzida respeitando prefers-reduced-motion no CSS. O próximo ciclo deve implementar timestep fixo e profiling em aparelhos de entrada.

## Distribuição
GitHub Pages. CI valida JavaScript e smoke tests em PR; deploy só após validação na branch principal.

## Evolução
Avaliar Phaser ou PixiJS somente se benchmark demonstrar benefício claro. Separar cada fase em dados próprios, adicionar testes automatizados de colisão e acessibilidade, e profissionalizar pipeline de arte/áudio.
