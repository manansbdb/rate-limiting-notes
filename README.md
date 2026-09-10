<p align="center">
  <img src="docs/banner.svg" alt="Rate Limiting Notes banner" width="100%" />
</p>

<h1 align="center">rate-limiting-notes</h1>

<p align="center">
  <strong>EN</strong> API rate-limiting strategies & response headers<br/>
  <strong>PT</strong> Estratégias de rate limiting para APIs e headers de resposta
</p>

<p align="center">
  <a href="https://github.com/manansbdb/rate-limiting-notes/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge" alt="MIT" /></a>
  <img src="https://img.shields.io/badge/lang-EN%20%7C%20PT-3b82f6?style=for-the-badge" alt="EN PT" />
  <img src="https://img.shields.io/badge/topic-rate--limit-f43f5e?style=for-the-badge" alt="rate-limit" />
  <a href="#support--apoio"><img src="https://img.shields.io/badge/donate-BTC-f59e0b?style=for-the-badge" alt="Donate BTC" /></a>
</p>

---

## What it does / Para que serve

| English | Português |
|---------|-----------|
| Notes on **rate-limiting strategies** (fixed window, sliding, token bucket) and useful response headers. | Notas sobre **estratégias de rate limiting** (janela fixa, sliding, token bucket) e headers úteis. |
| Use when designing public API quotas and 429 responses. | Usa ao desenhar quotas de API pública e respostas 429. |

```mermaid
flowchart LR
  A["📥 Request"] --> B{"🧮 Quota?"}
  B -->|ok| C["✅ Handler"]
  B -->|exceeded| D["⛔ 429 + headers"]
  style A fill:#6366f1,stroke:#4338ca,color:#fff
  style B fill:#f97316,stroke:#c2410c,color:#fff
  style C fill:#14b8a6,stroke:#0f766e,color:#fff
  style D fill:#e11d48,stroke:#9f1239,color:#fff
```

---

## Install / Instalação

### 1) Clone / Clona

```bash
git clone https://github.com/manansbdb/rate-limiting-notes.git
cd rate-limiting-notes
```

### 2) Copy into docs / Copia para docs

```bash
mkdir -p docs/api
cp strategies.md docs/api/rate-limiting-strategies.md
cp headers.md docs/api/rate-limiting-headers.md
```

### Requirements / Requisitos

- `git`
- Optional: Redis or in-memory store for implementing limits

---

## Quick start / Início rápido

```bash
git clone https://github.com/manansbdb/rate-limiting-notes.git
# read strategies.md → pick algorithm → document headers from headers.md
```

---

## Contents / Conteúdos

| Path | Purpose / Função |
|------|------------------|
| `strategies.md` | Limiting algorithms |
| `headers.md` | `X-RateLimit-*` / `Retry-After` |
| `SUPPORT.md` | Donations / Doações |

---

## Project layout / Estrutura

```text
rate-limiting-notes/
├── docs/banner.svg
├── strategies.md
├── headers.md
├── SUPPORT.md
└── README.md
```

---

## Support / Apoio

Bitcoin donations welcome / Doações em Bitcoin bem-vindas:

```
bc1q0qfnlnxyum9u45stzxe0a7jnhtj4j0usfkqdjw
```

See [SUPPORT.md](./SUPPORT.md).

---

## License / Licença

[MIT](./LICENSE) © 2026 manansbdb
