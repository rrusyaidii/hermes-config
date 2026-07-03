# Hermes Config — @rrusyaidii

Full Hermes Agent configuration backup (config, memory, installed skills, SOUL).

> **Nak yang ringan?** Guna [hermes-memory](https://github.com/rrusyaidii/hermes-memory) — memory, SOUL, config je. Takde skill files, senang clone.

## Structure

```
hermes-config/
├── config/config.yaml       # Main Hermes configuration
├── memory/
│   ├── MEMORY.md            # Agent persistent notes (PC specs, guardrails)
│   └── USER.md              # User profile (Haziq Rusyaidi)
├── skills/                   # Installed skills (500+ files by category)
├── .env.example              # Template for secrets
├── .gitignore
├── SOUL.md                   # Agent identity definition
└── README.md
```

## Setup

```bash
git clone https://github.com/rrusyaidii/hermes-config.git
```

Kalau nak guna kat PC baru:
```bash
# Copy memory & config
cp hermes-config/memory/* ~/AppData/Local/hermes/memories/
cp hermes-config/SOUL.md ~/AppData/Local/hermes/
# Setup secrets
cp hermes-config/.env.example ~/AppData/Local/hermes/.env
# Edit .env dengan API keys korang
```

## Notes

- Secrets (API keys, tokens) are NOT committed — use `.env`.
- Skills included for full restore but Hermes bundles them already.
- For lightweight memory-only sync, use `hermes-memory`.
