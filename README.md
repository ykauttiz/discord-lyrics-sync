<div align="center">

<br>

```
██╗   ██╗██╗  ██╗ █████╗ ██╗   ██╗████████╗████████╗██╗███████╗
╚██╗ ██╔╝██║ ██╔╝██╔══██╗██║   ██║╚══██╔══╝╚══██╔══╝██║╚════██║
 ╚████╔╝ █████╔╝ ███████║██║   ██║   ██║      ██║   ██║    ██╔╝
  ╚██╔╝  ██╔═██╗ ██╔══██║██║   ██║   ██║      ██║   ██║   ██╔╝
   ██║   ██║  ██╗██║  ██║╚██████╔╝   ██║      ██║   ██║   ██║
   ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝    ╚═╝      ╚═╝   ╚═╝   ╚═╝
```

<h2>🎵 discord lyrics sync</h2>
<p><strong>Sincronize letras em tempo real com seu status customizado do Discord</strong></p>

<br>

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Discord](https://img.shields.io/badge/Discord-Status_Bot-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com)
[![Windows](https://img.shields.io/badge/Windows-10%2F11-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![Linux](https://img.shields.io/badge/Linux%2FMac-Spotify_API-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://spotify.com)
[![Docker](https://img.shields.io/badge/Docker-Servidor-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com)
[![License](https://img.shields.io/badge/Licença-MIT-22c55e?style=for-the-badge)](LICENSE)

<br>

> Feito com 💙 por **[yKauttiz](https://github.com/yKauttiz)**

<br>

</div>

---

## 🖥️ Preview

```
╭─────────────────────────────────────────────────────────────────────╮
│  🎵 discord lyrics sync  ·  por yKauttiz          fonte: windows   │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│  Música    Bohemian Rhapsody                                        │
│  Artista   Queen                                                    │
│  Tempo     03:48                                                    │
│                                                                     │
│  🎵  Is this the real life?                                         │
│                                                                     │
│    ████████████████████░░░░░░░░░░░░░   58%                         │
│                                                                     │
│  › a seguir: Is this just fantasy?                                  │
│                                                                     │
├─────────────────────────────────────────────────────────────────────┤
│  Discord ● ativo     Sessão  00:24:15     🎵 7  ♪ 48  cache 91%    │
╰──────────────────────────────────────────────────── v2.0 · Ctrl+C ─╯
```

---

## ✨ Recursos

| Funcionalidade | Descrição |
|---|---|
| 🎵 **Letras em tempo real** | Atualiza seu status do Discord linha por linha enquanto a música toca |
| 📱 **Prévia da próxima linha** | Exibe no terminal a letra que vem a seguir |
| 📊 **Barra de progresso** | Progresso visual entre as linhas da letra |
| 💾 **Cache persistente** | Letras já buscadas são salvas — evita downloads repetidos |
| 🔁 **Rate limiting inteligente** | Retry automático e respeito ao limite da API do Discord |
| 🏠 **Windows WinRT** | Detecta qualquer player: Spotify, YouTube Music, Deezer... |
| 🌍 **Spotify Web API** | Funciona em Linux, Mac e servidores — qualquer sistema |
| 🐳 **Docker pronto** | Deploy em VPS em minutos com docker-compose |
| ⚙️ **Config flexível** | `.env`, `config.json` ou argumentos CLI — você escolhe |
| 📁 **Logs automáticos** | Arquivo `lyrics_sync.log` gerado automaticamente |
| 📈 **Estatísticas** | Faixas ouvidas, linhas sincronizadas, hits de cache na sessão |
| 🔕 **Modo headless** | Roda silenciosamente em servidores sem interface gráfica |

---

## 🗺️ Compatibilidade

| Ambiente | Método | Config necessária |
|---|---|---|
| 🪟 **Windows 10/11 (PC)** | Windows Media Controls (WinRT) | Só o token do Discord |
| 🍎 **Mac / 🐧 Linux (PC)** | Spotify Web API | Token Discord + credenciais Spotify |
| 🖥️ **Servidor VPS** | Spotify Web API + headless | Token Discord + credenciais Spotify + Docker |

---

## 🚀 Início rápido

### 1. Clone o repositório

```bash
git clone https://github.com/yKauttiz/discord-lyrics-sync.git
cd discord-lyrics-sync
```

### 2. Instale as dependências

```bash
pip install -r requirements.txt
```

**Se estiver no Windows**, instale também as dependências do WinRT:

```bash
pip install winrt-runtime winrt-Windows.Foundation winrt-Windows.Media.Control
```

### 3. Configure seu token do Discord

Crie o arquivo `.env` na pasta do projeto:

```bash
cp .env.example .env
```

Abra o `.env` e preencha:

```env
DISCORD_TOKEN=seu_token_aqui
```

### 4. Execute

```bash
python main.py
```

---

## 🔑 Como obter o token do Discord

> ⚠️ **Usar tokens de usuário pode violar os Termos de Serviço do Discord. Use por sua própria conta e risco.**

1. Abra o **Discord no navegador** em [discord.com/app](https://discord.com/app)
2. Pressione **`F12`** para abrir as Ferramentas de Desenvolvedor
3. Vá na aba **`Network`** (Rede)
4. Recarregue a página com **`F5`**
5. Na barra de busca das requisições, pesquise `science` ou clique em qualquer requisição para `discord.com`
6. Na seção **`Request Headers`**, copie o valor do campo **`authorization`**
7. Cole no seu arquivo `.env`:

```env
DISCORD_TOKEN=valor_copiado_aqui
```

> 💡 **Dica:** O token é uma string longa. Não inclua aspas ao colar.

---

## 🎧 Configuração do Spotify (para Linux / Mac / Servidor)

Se você não está no Windows, precisará da **Spotify Web API** para detectar a música tocando.

### Passo 1 — Criar um app no Spotify Developer

1. Acesse [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard)
2. Clique em **"Create app"**
3. Preencha:
   - **App name:** `discord-lyrics-sync` (ou qualquer nome)
   - **App description:** qualquer coisa
   - **Redirect URI:** `http://localhost:8888/callback`
   - Marque **"Web API"**
4. Clique em **"Save"**
5. Na página do app, clique em **"Settings"** e copie:
   - `Client ID`
   - `Client Secret`

### Passo 2 — Adicionar ao `.env`

```env
DISCORD_TOKEN=seu_token_discord
SPOTIFY_CLIENT_ID=seu_client_id
SPOTIFY_CLIENT_SECRET=seu_client_secret
```

### Passo 3 — Autenticar

```bash
python main.py --spotify-setup
```

Siga as instruções no terminal:
1. Acesse a URL exibida no navegador
2. Autorize o app
3. Copie a URL de redirecionamento completa e cole no terminal

Os tokens serão salvos em `.spotify_tokens.json` e renovados automaticamente.

### Passo 4 — Executar

```bash
python main.py
```

---

## 🐳 Deploy em Servidor com Docker

Ideal para rodar 24/7 em um VPS sem precisar deixar o PC ligado.

### Pré-requisitos

- Servidor com Docker e Docker Compose instalados
- Credenciais do Spotify configuradas (passo acima)

### Passo 1 — Configurar na sua máquina local primeiro

```bash
# Configure o .env com token do Discord e credenciais do Spotify
python main.py --spotify-setup
```

Isso cria o arquivo `.spotify_tokens.json` que você vai copiar pro servidor.

### Passo 2 — Enviar arquivos para o servidor

```bash
scp -r . usuario@seu-servidor:/opt/discord-lyrics-sync/
```

Ou use `rsync`:

```bash
rsync -avz . usuario@seu-servidor:/opt/discord-lyrics-sync/
```

### Passo 3 — Iniciar com Docker Compose

```bash
ssh usuario@seu-servidor
cd /opt/discord-lyrics-sync

docker compose up -d
```

### Comandos úteis

```bash
# Ver logs em tempo real
docker compose logs -f

# Reiniciar
docker compose restart

# Parar
docker compose down

# Ver status
docker compose ps
```

---

## ⚙️ Configuração avançada

Crie o arquivo `config.json` (copie de `config.example.json`):

```json
{
  "discord": {
    "token": "",
    "emoji": "🎵",
    "max_length": 100,
    "update_interval": 0.8,
    "clear_on_pause": true,
    "template": "{emoji} {lyric}"
  },
  "lyrics": {
    "max_length": 100,
    "cache_ttl_h": 168,
    "filter_noise": true
  },
  "media": {
    "source": "auto",
    "spotify_client_id": "",
    "spotify_client_secret": "",
    "poll_interval": 0.3
  },
  "display": {
    "headless": false,
    "show_next_lyric": true,
    "show_progress_bar": true,
    "show_stats": true
  },
  "logging": {
    "level": "INFO",
    "to_file": true
  }
}
```

### Referência das configurações

| Campo | Padrão | Descrição |
|---|---|---|
| `discord.emoji` | `🎵` | Emoji antes da letra no status |
| `discord.max_length` | `100` | Máximo de caracteres na letra |
| `discord.update_interval` | `0.8` | Mínimo de segundos entre atualizações |
| `discord.clear_on_pause` | `true` | Limpa status ao pausar |
| `discord.template` | `{emoji} {lyric}` | Template do status (use `{emoji}` e `{lyric}`) |
| `lyrics.cache_ttl_h` | `168` | Horas antes de re-buscar letras (7 dias) |
| `lyrics.filter_noise` | `true` | Filtra linhas com ruído/artefatos |
| `media.source` | `auto` | `auto`, `windows` ou `spotify` |
| `media.poll_interval` | `0.3` | Segundos entre verificações de mídia |
| `display.show_next_lyric` | `true` | Exibe prévia da próxima linha |
| `display.show_progress_bar` | `true` | Barra de progresso entre linhas |
| `display.show_stats` | `true` | Painel de estatísticas |
| `display.headless` | `false` | Sem UI — ideal para servidores |
| `logging.level` | `INFO` | `DEBUG`, `INFO`, `WARNING`, `ERROR` |

---

## 💻 Comandos CLI

```bash
# Modo padrão (detecção automática de fonte)
python main.py

# Forçar fonte de mídia
python main.py --source windows   # usa WinRT (Windows)
python main.py --source spotify   # usa Spotify API

# Modo servidor (sem UI gráfica)
python main.py --headless

# Configurar autenticação do Spotify
python main.py --spotify-setup

# Verificar se o token do Discord está válido
python main.py --validate-token

# Gerenciamento do cache
python main.py --cache-stats      # mostra informações do cache
python main.py --cache-clear      # apaga todo o cache

# Versão
python main.py --version
```

---

## 📁 Estrutura do projeto

```
discord-lyrics-sync/
│
├── main.py                   # script principal (tudo em um arquivo)
├── requirements.txt          # dependências Python
│
├── .env                      # suas credenciais (NÃO versionar!)
├── .env.example              # modelo do .env
│
├── config.json               # configuração avançada (opcional)
├── config.example.json       # modelo do config.json
│
├── Dockerfile                # imagem Docker para servidor
├── docker-compose.yml        # deploy com Docker Compose
│
├── .spotify_tokens.json      # tokens OAuth Spotify (auto-gerado)
├── .lyrics_cache.json        # cache de letras (auto-gerado)
├── lyrics_sync.log           # arquivo de log (auto-gerado)
│
└── README.md
```

> **⚠️ Importante:** Adicione ao seu `.gitignore`:
> ```
> .env
> .spotify_tokens.json
> .lyrics_cache.json
> lyrics_sync.log
> ```

---

## ❓ Perguntas frequentes

<details>
<summary><strong>O status não está atualizando no Discord — o que fazer?</strong></summary>

1. Verifique se o token está correto:
   ```bash
   python main.py --validate-token
   ```
2. Certifique-se de que a música está tocando (não pausada)
3. Verifique o arquivo `lyrics_sync.log` para erros

</details>

<details>
<summary><strong>A letra não aparece para algumas músicas</strong></summary>

Nem todas as músicas têm letra sincronizada disponível nas bases de dados (syncedlyrics, LRClib). Músicas muito novas, raras ou regionais podem não ter letra disponível.

O script tenta dois provedores em sequência:
1. **syncedlyrics** (LRClib, Netease, Musixmatch)
2. **LRClib API** (diretamente)

Se nenhum retornar, o status simplesmente não é atualizado para aquela faixa.

</details>

<details>
<summary><strong>Posso usar o Spotify no Windows em vez do WinRT?</strong></summary>

Sim! Use:
```bash
python main.py --source spotify
```

Isso pode ser útil se o WinRT não estiver funcionando corretamente.

</details>

<details>
<summary><strong>O script roda na inicialização do Windows?</strong></summary>

Sim. Crie um arquivo `.bat`:

```bat
@echo off
cd /d "C:\caminho\para\discord-lyrics-sync"
python main.py
```

Pressione `Win + R`, digite `shell:startup` e coloque o `.bat` na pasta que abrir.

</details>

<details>
<summary><strong>Meu servidor não tem interface gráfica — como configurar?</strong></summary>

1. Configure o Spotify localmente primeiro: `python main.py --spotify-setup`
2. Copie o arquivo `.spotify_tokens.json` para o servidor
3. Use Docker Compose (recomendado) ou rode com `--headless`

</details>

<details>
<summary><strong>Como limpar o cache se as letras estiverem erradas?</strong></summary>

```bash
python main.py --cache-clear
```

Ou delete manualmente o arquivo `.lyrics_cache.json`.

</details>

<details>
<summary><strong>O que é filtro de ruído (filter_noise)?</strong></summary>

O filtro remove linhas de letra problemáticas automaticamente:
- Linhas com camelCase colado (romaji sintetizado)
- Linhas muito longas ou com muitos caracteres especiais
- Símbolos musicais isolados (♪, ♫, ~)

Se quiser desativar, configure `lyrics.filter_noise: false` no `config.json`.

</details>

---

## 📦 Dependências

| Pacote | Versão | Para quê |
|---|---|---|
| `requests` | ≥ 2.31 | Chamadas HTTP (Discord, Spotify, LRClib) |
| `python-dotenv` | ≥ 1.0 | Suporte ao arquivo `.env` |
| `rich` | ≥ 13.7 | Interface do terminal (painéis, cores, live update) |
| `syncedlyrics` | ≥ 0.4 | Provedor primário de letras sincronizadas |
| `winrt-*` | qualquer | Detecção de mídia no Windows (opcional) |

---

## 🔒 Segurança

- **Nunca** suba seu `.env` ou `token.txt` para o GitHub
- **Nunca** compartilhe seu token do Discord — ele dá acesso total à sua conta
- Adicione ao `.gitignore`:
  ```
  .env
  token.txt
  .spotify_tokens.json
  .lyrics_cache.json
  ```
- Os tokens do Spotify são armazenados localmente em `.spotify_tokens.json` — proteja esse arquivo

---

## ⚠️ Aviso legal

> Este projeto utiliza o **token de usuário** do Discord para atualizar o status customizado. Isso pode violar os [Termos de Serviço do Discord](https://discord.com/terms). Use por sua própria conta e risco. O autor não se responsabiliza por banimentos ou penalidades.
>
> O projeto é para uso pessoal e fins educacionais.

---

## 📝 Créditos

**Desenvolvido por [yKauttiz](https://github.com/yKauttiz)**

Tecnologias utilizadas:
- [syncedlyrics](https://github.com/moehmeni/syncedlyrics) — letras sincronizadas
- [LRClib](https://lrclib.net) — banco de dados de letras gratuito
- [Rich](https://github.com/Textualize/rich) — interface do terminal
- [Spotify Web API](https://developer.spotify.com/documentation/web-api) — detecção de música
- [Discord API](https://discord.com/developers) — atualização de status

---

<div align="center">

**Se este projeto te ajudou, deixa uma ⭐ no repositório!**

<br>

Made with 💙 by **yKauttiz**

</div>
