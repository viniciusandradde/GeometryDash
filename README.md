# Little Dash Adventure 🌈
Uma aventura colorida, acolhedora e positiva para crianças.

## Links
- Jogar: https://viniciusandradde.github.io/GeometryDash/
- Código: https://github.com/viniciusandradde/GeometryDash
- Versões: https://github.com/viniciusandradde/GeometryDash/releases
- Publicação e CI: https://github.com/viniciusandradde/GeometryDash/actions

A URL pública muda somente depois que a branch main receber a implementação e o workflow de Pages concluir com sucesso.

## Mundos
1. Reino dos Doces — Bosque de Balas, Ponte de Biscoito, Castelo de Chocolate.
2. Ilha dos Dinossauros — Vale das Pegadas, Vulcão Dorminhoco, Festa dos Dinossauros.
3. Fundo do Mar — Jardim de Corais, Caverna das Pérolas, Baile das Sereias.
4. Aventura Espacial — Lua de Queijo, Anéis de Saturno, Grande Cometa.

## Executar localmente
Execute python3 -m http.server 8000 e abra http://localhost:8000. Em navegador compatível, use Instalar aplicativo ou Adicionar à tela inicial.

## Controles
Toque/clique ou Espaço/Seta para cima para saltar. Botão de pausa interrompe a partida. Sem Game Over ou perda de progresso.

## Foto opcional do Rafael
A área dos responsáveis permite importar uma foto do dispositivo para uma comemoração surpresa. A imagem é redimensionada e armazenada no IndexedDB local. Não faz parte do repositório, não é enviada a servidores e pode ser removida/desativada. Não há reconhecimento facial.

## Arquitetura
- index.html: interface e estrutura.
- styles.css: identidade visual e layout responsivo.
- app.js: navegação, Canvas, fases, progresso e personalização.
- manifest.json: metadados PWA.
- sw.js: cache offline.
- docs/PRD-LITTLE-DASH-ADVENTURE.md: requisitos e referências.
- docs/ADRs.md: decisões arquiteturais.

## Estado atual
Esta é uma primeira base funcional com menus, 12 fases configuradas, gameplay Canvas simples, estrelas, recuperação assistida, salvamento local, PWA e personalização opcional. Arte final, trilhas originais completas, inventário cosmético, dificuldade adaptativa refinada, ícones PWA e testes em aparelhos reais ainda são etapas de produção.

## Versionamento
SemVer MAJOR.MINOR.PATCH. Cada release deve validar navegação, gameplay, vitória, persistência, offline e exclusão da foto. Nunca publicar imagens pessoais ou assets sem licença comprovada.
