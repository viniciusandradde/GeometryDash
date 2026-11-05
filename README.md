# Little Dash Adventure 🌈
**Jogo infantil original | Web/PWA | pt-BR**

Little Dash Adventure é uma experiência de plataforma acolhedora para crianças: o personagem avança automaticamente, a criança toca para saltar, coleta estrelas e explora quatro mundos. Não existe Game Over, perda de vidas, anúncios ou compras internas.

## Acessos
- **Jogar (GitHub Pages):** https://viniciusandradde.github.io/GeometryDash/
- **Repositório:** https://github.com/viniciusandradde/GeometryDash
- **Pull Request de desenvolvimento:** https://github.com/viniciusandradde/GeometryDash/pull/2
- **Releases:** https://github.com/viniciusandradde/GeometryDash/releases
- **Actions/CI:** https://github.com/viniciusandradde/GeometryDash/actions

A URL de Pages só refletirá esta versão depois que as alterações forem integradas à main e o workflow de publicação terminar com sucesso.

## Conteúdo — 4 mundos / 12 fases
| Mundo | Fases |
|---|---|
| 🍭 Reino dos Doces | Bosque de Balas · Ponte de Biscoito · Castelo de Chocolate |
| 🦕 Ilha dos Dinossauros | Vale das Pegadas · Vulcão Dorminhoco · Festa dos Dinossauros |
| 🐠 Fundo do Mar | Jardim de Corais · Caverna das Pérolas · Baile das Sereias |
| 🚀 Aventura Espacial | Lua de Queijo · Anéis de Saturno · Grande Cometa |

## Como jogar
- Toque/clique na tela ou use Espaço / Seta para cima para saltar.
- O botão II pausa; música pode ser silenciada.
- Obstáculos geram recuperação assistida; não há tela de derrota.
- Ganhe estrelas para desbloquear personagens na coleção.
- Fases são liberadas progressivamente.

## Personalização familiar opcional
Na Área dos Responsáveis, a família pode importar uma foto do Rafael. O navegador cria um recorte circular e grava no IndexedDB local. A imagem aparece aleatoriamente em algumas vitórias e sempre ao concluir as 12 fases, se a opção estiver ativa. Pode ser desativada ou removida a qualquer momento.
**A foto não é incluída no repositório, não é enviada por rede, não é processada por reconhecimento facial e não é usada em analytics.** Para adicionar, importar a foto neste dispositivo depois de abrir o jogo.

## Arquitetura e execução
- `index.html`: telas e acessibilidade.
- `styles.css`: interface responsiva e preferência de movimento reduzido.
- `app.js`: motor Canvas 2D, física simples, conteúdo, progressão, áudio sintetizado e persistência.
- `manifest.json`, `sw.js`: instalação PWA e cache offline.
- `assets/icon.svg`: ícone original.
- `docs/`: PRD, ADRs, arquitetura, QA e roadmap.
- `tests/smoke-check.mjs`: validações estáticas.

Para executar localmente: `python3 -m http.server 8000` e acesse `http://localhost:8000`. Não abra o HTML via `file://`, pois Service Worker e IndexedDB dependem de contexto HTTP seguro/local.

## Desenvolvimento e release
1. Alterações em branch.
2. CI verifica sintaxe e smoke tests em Pull Requests.
3. Merge na main aciona GitHub Pages.
4. Criar tag/release SemVer (`vMAJOR.MINOR.PATCH`) após smoke tests manuais em Android Chrome, iOS Safari e desktop.
5. Validar instalação, offline, som, progresso e exclusão de foto antes de anunciar a versão.

## Escopo e limitações desta entrega
A base implementa a navegação, 12 fases parametrizadas, gameplay Canvas, progressão, personagens desbloqueáveis, efeitos visuais básicos, áudio procedural original, save local, PWA e controles parentais da foto. Ainda requer rodada de QA em dispositivos físicos e refinamento de arte, animações, desenho de fases, trilhas compostas e acessibilidade antes de ser tratada como versão final de produção.

## Referências técnicas
- PWA: https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps
- Service Worker: https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API
- Cache API: https://developer.mozilla.org/en-US/docs/Web/API/Cache
- IndexedDB: https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API
- Web Audio API: https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- Game Accessibility Guidelines: https://gameaccessibilityguidelines.com/
- Phaser: https://docs.phaser.io/
- PixiJS: https://pixijs.com/
- Kenney (confirmar licença de cada pacote): https://kenney.nl/assets
- OpenGameArt (confirmar licença por recurso): https://opengameart.org/
