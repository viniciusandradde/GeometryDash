# Geometry Dash — VSA Tecnologia

Jogo de plataforma rítmico em HTML5 Canvas e JavaScript puro, executado diretamente no navegador. Este projeto é independente e não é afiliado à RobTop Games.

## Estado do projeto
**Base jogável existente; etapa atual: estabilidade de gameplay e engenharia.** O jogo possui três fases, modos Cube/Ship, obstáculos, pads, orbs, portais de velocidade, Practice Mode, checkpoints, efeitos, áudio sintetizado e progresso local.

Esta entrega corrige transições de morte, reconstrução de geometria ao redimensionar a janela e pausa ao alternar de aba. Ainda são necessários testes reais em navegadores e dispositivos.

## Executar
Não há etapa de build nem dependências externas. Na raiz do repositório:

```bash
python3 -m http.server 8000
```

Acesse http://localhost:8000.

## Controles
| Ação | Teclado | Mouse / toque |
|---|---|---|
| Pular / voar | Espaço, ↑ ou W | Clique / toque |
| Pausar / retomar | P | Toque durante pausa |
| Reiniciar após colisão | Espaço / Enter | Toque |
| Silenciar | M | Botão de áudio |
| Menu | Esc | Botão de retorno |
| Tela cheia | F | — |

## Recursos atuais
- Três fases: Neon Pulse, Rebound e Spectral Drift.
- Modos Cube e Ship.
- Espinhos, blocos, plataformas, gaps, movers, pads, orbs e portais.
- Velocidades slow, normal, fast e very fast.
- Practice Mode e checkpoints.
- Progresso e tentativas salvos em localStorage.
- Efeitos visuais e áudio sintetizado via Web Audio API.

## Estrutura
- `index.html`: entrada.
- `game.js`: lógica, física, fases, renderização e áudio.
- `styles.css`: layout.
- `actions.json`: sequência de ações para teste/playback.
- `docs/`: arquitetura, QA e roadmap.

## Qualidade
```bash
node --check game.js
```

- [Arquitetura](docs/ARCHITECTURE.md)
- [QA](docs/QA.md)
- [Roadmap](docs/ROADMAP.md)

## Persistência e privacidade
O progresso é armazenado localmente no navegador pela chave `gd_save2`. Não há conta, backend ou telemetria implementados nesta base. Limpar os dados do navegador pode apagar o progresso.

## Licença e propriedade intelectual
O arquivo LICENSE existente declara MIT e atribui copyright a Anay Goenka. Preserve esse aviso e os termos da licença ao redistribuir. Geometry Dash e suas marcas/ativos oficiais pertencem aos respectivos titulares. Use somente identidade visual, músicas, sprites e fases originais ou devidamente licenciados; não utilize assets extraídos do jogo comercial.
