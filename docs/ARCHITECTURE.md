# Arquitetura — Little Dash Adventure
A aplicação é uma PWA estática com HTML/CSS/JavaScript. index.html apresenta a interface, styles.css o layout responsivo, app.js navegação e gameplay Canvas 2D, manifest.json metadados de instalação e sw.js cache offline.

## Camadas
- Interface: telas home, mundos, fases, jogo e área dos responsáveis.
- Gameplay: loop requestAnimationFrame, simulação Canvas, salto por toque/teclado, coleta, obstáculos e recuperação assistida.
- Conteúdo: quatro mundos e três fases por mundo.
- Persistência: localStorage para progresso/estrelas; IndexedDB para a foto opcional importada pelo responsável.
- Offline: Service Worker com cache versionado do shell.

## Privacidade
A foto do Rafael é escolhida manualmente pelo responsável, processada localmente e salva no IndexedDB. Não incluir imagem no Git, assets públicos, telemetria ou backend. A primeira versão não possui conta ou sincronização.

## Distribuição
GitHub Pages. O workflow valida sintaxe JavaScript e publica os arquivos estáticos da raiz. Sem Capacitor, Kotlin ou APK.

## Próximas decisões técnicas
- Separar dados de fase do motor e usar timestep fixo.
- Avaliar Phaser/PixiJS após medir a vertical slice.
- Criar pipeline de assets licenciados, áudio original e inventário cosmético.
- Adicionar migração de schema para progresso e testes automatizados de gameplay.
