# ADRs — Little Dash Adventure
## ADR-001 — Web/PWA exclusivamente
HTML/CSS/JavaScript no navegador e GitHub Pages. Sem Kotlin, APK, Capacitor ou wrapper nativo. Consequência: distribuição instalável via navegador e atualizações web.

## ADR-002 — Canvas 2D para a primeira versão
Canvas 2D sem dependência de engine para validar o loop. Phaser e PixiJS ficam como alternativas se benchmark justificar. Consequência: dependência pequena, mas o motor e colisões são responsabilidade do projeto.

## ADR-003 — Offline-first
Service Worker e Cache API para shell; IndexedDB para foto/preferências; localStorage para progresso. Cache versionado e limpeza de versões antigas.

## ADR-004 — Gameplay não punitivo
Sem Game Over, vidas ou perda de progresso. Colisões dão impulso de recuperação e o progresso só avança. A adaptação avançada será refinada por playtesting.

## ADR-005 — Propriedade intelectual
Música, personagens, cenários e UI devem ser originais ou licenciados. Não copiar faixas, sprites, nomes, fases ou identidade visual de Geometry Dash. Manter registro de autor, origem e licença por asset.

## ADR-006 — Recompensas sem monetização
Estrelas e personagens desbloqueáveis por jogo. Sem compras internas, loot boxes pagas, anúncios ou ranking público.

## ADR-007 — Privacidade infantil
Sem conta obrigatória, analytics, trackers, publicidade ou comunicação social. Sem reconhecimento facial. Preferências e progresso ficam no dispositivo.

## ADR-008 — Foto opcional do Rafael
Importação manual pelo responsável, processamento local e armazenamento IndexedDB. Aparição em parte das vitórias e garantida ao concluir as 12 fases, se ativa. Nunca versionar, enviar ou sincronizar a imagem. Possibilidade de desativar e excluir.

## ADR-009 — Save local
Progresso versionado e armazenado localmente. Sincronização em nuvem fica fora do primeiro release.

## ADR-010 — Gate de qualidade
A base funcional não é considerada produto final até passar QA físico e gates de arte, áudio, acessibilidade e playtesting.

## ADR-011 — Áudio original procedural
Web Audio API gera motivos melódicos originais sem carregar faixas de terceiros. A primeira versão é provisória; trilhas compostas finais exigem produção e licença documentadas.

## ADR-012 — CI antes do deploy
Pull Requests executam verificação de sintaxe e smoke tests. Deploy do Pages ocorre após validação na branch main.
