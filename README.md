# Geometry Dash — VSA Tecnologia

Jogo de plataforma rítmico em HTML5 Canvas e JavaScript puro, executado diretamente no navegador. Este projeto é independente e não é afiliado à RobTop Games.

## Estado do projeto
**Base jogável existente; etapa atual: estabilidade de gameplay e engenharia.** O jogo possui três fases, modos Cube/Ship, obstáculos, pads, orbs, portais de velocidade, Practice Mode, checkpoints, efeitos, áudio sintetizado e progresso local.

Esta entrega corrige transições de morte, reconstrução de geometria ao redimensionar a janela e pausa ao alternar de aba. Ainda são necessários testes reais em navegadores e dispositivos.

## Executar
Não há etapa de build nem dependências externas para executar a versão web. Na raiz do repositório:

```bash
python3 -m http.server 8000
```

Acesse http://localhost:8000.

## Aplicativo Android: arquitetura e tecnologia

O projeto também possui empacotamento para Android por meio do **Capacitor 7**.

**Importante: o jogo não foi desenvolvido integralmente em Kotlin.** A lógica principal, a física, as fases, a renderização e o áudio continuam implementados em JavaScript, HTML5 Canvas e CSS. No Android, essa aplicação web é executada dentro de uma WebView, empacotada como aplicativo Android pelo Capacitor.

| Camada | Tecnologia | Responsabilidade |
|---|---|---|
| Jogo e gameplay | JavaScript | Física, controles, colisões, fases, progresso e áudio |
| Interface e renderização | HTML5 Canvas e CSS | Tela do jogo, menus e apresentação visual |
| Integração Android | Capacitor 7 | Empacotamento da aplicação web e acesso às capacidades nativas quando necessário |
| Projeto nativo Android | Android / Gradle | Estrutura de compilação e geração do APK |

Configuração atual:
- **Application ID:** `com.vsa.technology.geometrydash`
- **Nome Android:** `Geometry Dash VSA`
- **Diretório web empacotado:** `www/`
- **APK gerado no CI:** variante debug (`app-debug.apk`).

O projeto Android é preparado durante o workflow de CI; portanto, a implementação atual não representa uma reescrita nativa do motor do jogo em Kotlin. Caso sejam adicionadas funcionalidades nativas específicas, elas poderão utilizar Kotlin no projeto Android.

### Gerar o APK localmente

Requisitos: Node.js 20 ou compatível, JDK 21, Android SDK e ferramentas do Gradle.

```bash
npm install
mkdir -p www
cp index.html game.js styles.css www/
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```

O APK de debug será gerado em:

```
android/app/build/outputs/apk/debug/app-debug.apk
```

Para atualizar os arquivos web depois de alterações no jogo:

```bash
mkdir -p www
cp index.html game.js styles.css www/
npx cap sync android
```

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
- `package.json` e `capacitor.config.json`: dependências e configuração do empacotamento Android.
- `.github/workflows/`: automação de validação, publicação web e geração do APK.

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
