# Hermes Config — @rrusyaidii

Personal Hermes Agent configuration backup, including memory (user profile, persistent notes), installed skills, config, and SOUL definition.

## Structure

```
hermes-config/
├── config/
│   └── config.yaml          # Main Hermes configuration
├── memory/
│   ├── MEMORY.md            # Agent persistent notes (PC specs, guardrails)
│   └── USER.md              # User profile (Haziq Rusyaidi)
├── skills/                   # Installed skills (categories)
├── cron/                     # Cron job output
├── hooks/                    # Webhook configurations
├── .env.example              # Template for secrets (copy to ~/.hermes/.env)
├── .gitignore
├── SOUL.md                   # Agent identity definition
└── README.md
```

## Setup

```bash
# Clone
git clone https://github.com/rrusyaidii/hermes-config.git ~/hermes-config

# Copy config & memory to Hermes home
cp -r hermes-config/config/* ~/AppData/Local/hermes/
cp -r hermes-config/memory/* ~/AppData/Local/hermes/memories/
cp hermes-config/SOUL.md ~/AppData/Local/hermes/

# Set up secrets
cp hermes-config/.env.example ~/AppData/Local/hermes/.env
# Edit .env with your actual API keys
```

## Notes

- Secrets (API keys, tokens) are NOT committed — use `.env` for those.
- Memory files contain PC specs, user profile, and guardrails.
- Skills are bundled/categorized under `skills/`.
