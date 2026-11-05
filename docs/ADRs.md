# ADRs — Little Dash Adventure
Decisões aprovadas em 05/11/2026.

## ADR-001 — Web/PWA exclusivamente
HTML/CSS/JavaScript no navegador, instalável como PWA. Sem Kotlin, APK, Capacitor ou wrapper nativo. Hospedagem estática via GitHub Pages.

## ADR-002 — Motor Canvas 2D inicial
Vertical slice em Canvas 2D com JavaScript, dados de fase separados do motor. Reavaliar Phaser ou PixiJS após benchmark e protótipo. Alternativas: Phaser (motor completo), PixiJS (renderização acelerada), Canvas (mínimas dependências).

## ADR-003 — Offline-first
Service Worker + Cache API para shell e assets; IndexedDB para dados estruturados e foto opcional; localStorage apenas para progresso simples não sensível. Cache versionado.

## ADR-004 — Gameplay não punitivo
Sem Game Over, vidas ou perda de progresso. Colisões acionam recuperação assistida e invulnerabilidade breve. A dificuldade deve adaptar-se ao jogador.

## ADR-005 — IP e assets originais
Personagens, cenários, fases, UI, músicas e efeitos originais ou licenciados. Proibido extrair ou reproduzir assets e músicas de Geometry Dash. Manter inventário de origem, autor, licença e atribuição.

## ADR-006 — Recompensas sem monetização
Cosméticos conquistados jogando. Sem IAP, loot boxes pagas, anúncios ou rankings públicos.

## ADR-007 — Privacidade infantil
Sem contas obrigatórias, rastreadores, analytics, publicidade, reconhecimento facial ou upload de dados pessoais. Responsáveis controlam e removem personalizações.

## ADR-008 — Surpresa opcional do Rafael
Importação manual da foto pelo responsável; processamento local; IndexedDB local; aparição aleatória em vitórias e garantida ao concluir 12 fases se habilitada. Sem arquivo de imagem no Git, CDN, analytics ou backend. Sem reconhecimento facial. Não sincroniza entre dispositivos.

## ADR-009 — Progresso local
Save local com versionamento de schema e migração defensiva. Sem sincronização na primeira versão.

## ADR-010 — Gate de qualidade
Aprovar um nível vertical slice no Reino dos Doces antes de replicar as outras 11 fases.

## ADR-011 — Áudio original
Trilhas originais por mundo e efeitos próprios; iniciar áudio após gesto do usuário e oferecer silêncio/volume.

## Referências
- PWA: https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps
- Service Worker: https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API
- IndexedDB: https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- Game Accessibility Guidelines: https://gameaccessibilityguidelines.com/
- Phaser: https://docs.phaser.io/
- PixiJS: https://pixijs.com/
