# Dew Protocols: The Autonomous "Just In" Intelligence

<div align="center">
  <img src="logo.png" alt="Dew Protocols Logo" width="200">
  <br>
  <b>Real-Time Crypto Intelligence | Whale Tracking | Gen-Z Analyst Persona</b>
</div>

---

![Status](https://img.shields.io/badge/Status-Operating-success)
![Python](https://img.shields.io/badge/Python-3.12-blue)
![AI](https://img.shields.io/badge/AI-Groq%20%7C%20Llama3-orange)
![Infrastructure](https://img.shields.io/badge/Infra-Ubuntu%20%7C%20Nextcloud-purple)

## 🌐 What is Dew Protocols?

**Dew Protocols** is not just a bot; it's an **Autonomous Agentic Organization** designed to dominate the crypto news cycle. It operates as a 24/7 "Just In" news aggregator and on-chain analyst, delivering high-speed, high-signal customized content to X (Twitter) and Threads.

Unlike generic alert bots, Dew Protocols adopts a **"Jaksel" Gen-Z persona**—blending financial sophistication with slang/meme culture (e.g., "Mega Whale Alert", "Cukong Masuk"). It doesn't just repost data; it interprets market regimes, visualizes whale movements, and engages with the community using AI-generated visuals and witty commentary.

## 🚀 Key Features

### 1- 🐋 Giant Hunter (Hyperliquid Whale Watcher)
Directly taps into the **Hyperliquid** L2 data stream to detect massive capital flows.
- **Real-Time Detection**: Monitors "Mega Whales" ($100k+) and "Krakens" ($1M+) opening/closing positions.
- **PnL Tracking**: Tracks the profitability of these whales over time (e.g., "Whale who bought bottoms is now taking profit").
- **Visuals**: Auto-generates cyberpunk-style images of whales based on position side (Bullish/Bearish).

### 2- ⚡ "Just In" News Agreggator
A multi-vector scraping engine that beats mainstream media to the punch.
- **Sources**: Watcher Guru, Cointelegraph, SUI Ecosystem, and direct RSS feeds (SEC, PRNewswire).
- **Speed**: Scrapes every 3-5 minutes, filters for "High Priority" keywords, and broadcasts immediately.
- **Zero-Hallucination**: Uses rigorous content validation to ensure news is factual before AI rephrasing.

### 3- 🧠 Regime & Price Monitor
An internal "Regime Engine" that understands market context.
- **Trend Detection**: Identifies Pump, Dump, ATH (All-Time High), and Correction phases.
- **Context Awareness**: Won't post low-priority news during a "Panic Sell" event.
- **Sentiment Alpha**: Tracks Long/Short ratios and funding rates to provide "Counter-Trade" signals.

### 4- 🖼️ Cognitive Brand Backend
A sophisticated content pipeline that ensures brand consistency.
- **Persona Engine**: Enforces strict character limits (350 chars for Threads, 150 for X) and tone.
- **Image Gen**: Integrated with Pollinations AI to create dynamic headers and thumbnails.
- **Cross-Posting**: Smartly formats content for X (Hashtags, Cashtags) vs Threads (Visual-first, longer form).

---

## 🏗️ System Architecture

Dew Protocols follows a **Data-Driven Event-Loop Architecture**.

```mermaid
graph TD
    subgraph Data_Layer ["📡 Data Ingestion"]
        HL[Hyperliquid Engine] -->|Trades & Open Interest| GH[Giant Hunter]
        W[Watcher Guru Scraper] -->|Breaking News| NA[News Aggregator]
        RSS[RSS Feeds] -->|Corporate Actions| NA
        Price[Price Monitor] -->|Volatility & ATH| RE[Regime Engine]
    end

    subgraph Logic_Layer ["🧠 The Brain (Core Logic)"]
        GH & NA --> PE[Priority Engine]
        RE --> PE
        PE -->|High Signal Event| LLM[LLM Client (Groq/Llama3)]
        LLM -->|Draft Content| VAL[Content Validator]
        VAL -->|Approved| IG[Image Generator]
    end

    subgraph Storage_Layer ["� State & Logging"]
        States[JSON State Files] <-->|Sync| NC[Nextcloud Cloud Storage]
        Logs[Activity Logs] -->|Backup| SB[Supabase DB]
    end

    subgraph Action_Layer ["� Broadcaster"]
        IG --> Poster[Smart Broadcaster]
        Poster -->|API/Browser| Twitter[X (Twitter) Bot]
        Poster -->|API| Threads[Threads Bot]
        Poster -->|Notify| TG[Telegram Admin Ops]
    end

    %% formatting
    classDef source fill:#e1f5fe,stroke:#01579b,stroke-width:2px;
    classDef logic fill:#fff3e0,stroke:#ff6f00,stroke-width:2px;
    classDef storage fill:#f3e5f5,stroke:#4a148c,stroke-width:2px;
    classDef action fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px;

    class HL,W,RSS,Price source;
    class GH,NA,RE,PE,LLM,VAL,IG logic;
    class States,Logs,NC,SB storage;
    class Poster,Twitter,Threads,TG action;
```

---

## 🛠️ Technology Stack

### Core Logic
- **Language**: Python 3.12 (Typed, AsyncIO)
- **AI/LLM**: Groq API (Llama-3-70b-Versatile) for speed and intelligence.
- **Image Gen**: Pollinations AI (Flux) for instant visual assets.

### Backend Infrastructure
- **Server**: Ubuntu 22.04 LTS (Hetzner/DigitalOcean).
- **Process Management**: `Systemd` services + `PM2` for monitoring.
- **Storage**: **Nextcloud** (WebDAV) for decentralized state management and log syncing.
- **Database**: **Supabase** (PostgreSQL) for long-term historical analysis.

### Data & Connectivity
- **APIs**: Hyperliquid (Direct API), CoinGecko (Market Data).
- **Scraping**: `Playwright` & `BeautifulSoup4` with **Rotating Proxies** (`verified_proxies.json`) to bypass WAFs.
- **Networking**: Cloudflare WARP (1.1.1.1) for secure, high-speed upstream connectivity.

### "Banned" / Resilient Tech
- **Browser Fingerprinting**: Uses Stealth Puppeteer/Playwright techniques to mimic human users.
- **Cookie Management**: Persistent session handling to avoid repeated logins/captchas.
- **Rate Limit Evasion**: Jittered scheduling and smart backoff algorithms.

---

## � Project Structure

```bash
X Automation/
├── src/
│   ├── generators/       # AI Content prompts & templates
│   ├── utils/            # Helper functions (text, formatting)
│   ├── giant_hunter_flow.py # Hyperliquid Whale Logic
│   ├── content_generator.py # Central AI Drafts
│   ├── llm_client.py     # Groq Interface
│   └── nextcloud_logger.py # Cloud Sync
├── data/                 # JSON State files (Synced to Nextcloud)
├── scripts/              # Verify & Maintenance scripts
└── deploy.py             # Auto-deployment to Production
```

---

> ⚠️ **Disclaimer**: This is a private autonomous agent. Use at your own risk.
