# PRD — Little Dash Adventure
Versão 1.0 | 05/11/2026 | pt-BR

## Visão
Jogo original de plataforma, acolhedor e acessível, para crianças a partir de aproximadamente 4 anos. O personagem avança automaticamente; a criança toca para saltar, coleta estrelas e explora pequenos mundos. A experiência prioriza diversão, descoberta e reforço positivo.

## Princípios obrigatórios
- 100% Web/PWA. Sem Kotlin, APK, Capacitor ou wrapper nativo.
- Sem Game Over, vidas, perda de progresso, publicidade, compras internas, loot boxes ou competição pública.
- Recuperação assistida, saltos tolerantes e dificuldade adaptativa.
- Botões grandes, textos curtos, controle por toque e feedback positivo.
- Offline-first e privacidade infantil por padrão.
- Identidade, personagens, fases, música e efeitos originais ou devidamente licenciados.

## Conteúdo
1. Reino dos Doces: Bosque de Balas; Ponte de Biscoito; Castelo de Chocolate.
2. Ilha dos Dinossauros: Vale das Pegadas; Vulcão Dorminhoco; Festa dos Dinossauros.
3. Fundo do Mar: Jardim de Corais; Caverna das Pérolas; Baile das Sereias.
4. Aventura Espacial: Lua de Queijo; Anéis de Saturno; Grande Cometa.

## Loop
Avanço automático, toque para saltar, coleta generosa de estrelas, recuperação automática após colisões, celebração ao concluir fase e mundo. As 12 fases têm uma celebração final.

## Foto opcional do Rafael
Apenas a foto importada manualmente pelo responsável. O navegador processa um recorte circular e armazena no IndexedDB local. Aparição surpresa em cerca de 22% das vitórias e garantida na conclusão final se habilitada. Nunca entra no repositório, bundle, CDN, analytics ou backend. Sem reconhecimento facial ou embeddings. O responsável pode desativar e excluir.

## Requisitos não funcionais
- Responsivo para celular, tablet e desktop; sem bloquear orientação.
- Alvos de toque amplos, contraste adequado, opção de silenciar.
- Limitar pixel ratio e efeitos para aparelhos modestos.
- Sem trackers, analytics, anúncios ou coleta de dados infantis.
- Progresso local versionado; falhas de armazenamento não podem bloquear o jogo.

## Histórias e aceite
1. Criança inicia jogo em até dois passos.
2. Toque, clique e Espaço/Seta para cima saltam.
3. Colisões recuperam automaticamente; nunca há tela de derrota.
4. Quatro mundos e 12 fases navegáveis.
5. Responsável silencia e controla a personalização.
6. Foto é importada no cliente, removível e não transmitida.
7. Depois da primeira visita, shell do jogo abre offline.
8. Conclusão exibe celebração positiva.

## Fora de escopo
Aplicativo nativo, multiplayer, chat, ranking público, monetização, publicidade, login obrigatório, sincronização em nuvem e reconhecimento facial.

## Plano
1. Fundamentos PWA e navegação.
2. Vertical slice de qualidade no Reino dos Doces.
3. Motor de conteúdo e 12 fases.
4. Persistência, acessibilidade, dificuldade adaptativa e recompensas.
5. Área dos responsáveis e surpresa local opcional.
6. Testes em aparelhos, auditoria de privacidade e publicação.

## Referências
- PWA: https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps
- Service Worker: https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API
- Cache API: https://developer.mozilla.org/en-US/docs/Web/API/Cache
- IndexedDB: https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API
- Web Audio: https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- Game Accessibility Guidelines: https://gameaccessibilityguidelines.com/
- Phaser: https://docs.phaser.io/
- PixiJS: https://pixijs.com/
- Kenney (verificar licença do pacote): https://kenney.nl/assets
- OpenGameArt (verificar licença por asset): https://opengameart.org/
- Pixabay (verificar licença por recurso): https://pixabay.com/
