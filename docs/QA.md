# QA — Little Dash Adventure
## Testes automatizados no CI
- `node --check app.js`
- `node tests/smoke-check.mjs`: verifica referências DOM, quatro mundos/12 fases, fluxo de vitória, persistência local da foto, ausência de chamadas de rede no app, cache versionado e movimento reduzido.

## Checklist manual antes de release
- [ ] Android Chrome: instalação PWA, toque, áudio, rotação, pausa e retorno.
- [ ] iOS Safari: adicionar à tela inicial, toque, áudio e persistência.
- [ ] Desktop Chrome/Firefox/Safari: clique e teclado.
- [ ] Completar as 12 fases; verificar desbloqueios e estrelas após recarregar.
- [ ] Testar colisões e recuperação com diferentes tempos de salto.
- [ ] Verificar música, mute, pause e retomada.
- [ ] Importar foto, confirmar aparição aleatória e final, desativar e remover.
- [ ] Confirmar em DevTools que a imagem não é enviada por requisição.
- [ ] Primeira carga online e segunda carga em modo avião.
- [ ] Lighthouse: performance, acessibilidade, boas práticas e PWA.
- [ ] Validar redução de movimento e alvos de toque.
- [ ] Conferir que nenhum asset pessoal/licença duvidosa entrou no repositório.

## Limitações conhecidas
A arte atual é vetorial/Canvas com formas e emojis, não uma produção final de sprites ilustrados. Áudio é procedural simples, não trilha composta final. A dificuldade ainda usa parâmetros por fase e recuperação básica; não há sistema sofisticado de adaptação comportamental. Os testes automatizados atuais são smoke tests estáticos, não substituem QA de gameplay em aparelhos reais.
