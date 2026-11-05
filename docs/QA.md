# QA — Geometry Dash

## Validação automatizada
```bash
node --check game.js
```
O workflow de CI executa essa verificação a cada push e pull request.

## Regressões tratadas nesta etapa
- [x] Timeout de morte não pode encerrar uma tentativa reiniciada.
- [x] Troca de fase cancela transição de morte pendente.
- [x] Resize recompõe geometria e atualiza a referência da fase ativa.
- [x] Obstáculos já acionados preservam estado durante resize.
- [x] Perda de foco libera input preso.
- [x] Aba oculta pausa a partida; retomada é manual.
- [x] Música para e volta com pausa manual.

## Testes manuais obrigatórios
| Área | Cenário | Resultado esperado |
|---|---|---|
| Menu | Play e selecionar cada fase | Fase correta inicia |
| Input | Espaço, clique e toque | Um salto por pressionamento |
| Morte | Colidir e reiniciar rapidamente | Nova tentativa permanece jogável |
| Morte | Colidir e aguardar 450 ms | Overlay de colisão aparece |
| Pause | P, clique para retomar | Estado e áudio retomam |
| Aba | Alternar para outra aba e voltar | Jogo permanece pausado |
| Resize | Redimensionar durante jogo | Chão, jogador e obstáculos alinhados |
| Fullscreen | Entrar/sair | Canvas e geometria se ajustam |
| Practice | Morrer após checkpoint | Retorna ao checkpoint |
| Persistência | Completar fase e recarregar | Melhor progresso permanece |
| Mobile | Android Chrome | Sem scroll ou zoom acidental |

## Critério de release
Validar as três fases em Chrome desktop e Android, incluindo pause/resume, resize, Practice Mode e persistência.
