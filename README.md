# Meeting Ingestion

Unified skill for ingesting meeting transcripts from Google Drive and orchestrating the processing pipeline (recap, blocks). Replaces legacy MG-1 through MG-6 agent sequence.

## Installation

```bash
cd /home/workspace/Skills
git clone https://github.com/vrijenattawar/zo-meeting-ingestion.git meeting-ingestion
python3 meeting-ingestion/bootloader.py
```

The bootloader will:
1. Survey your environment
2. Detect potential conflicts
3. Propose an installation plan
4. Execute only with your approval

## Required Secrets

Set these in **Zo Settings > Developers**:

- `ZO_CLIENT_IDENTITY_TOKEN`

## Required Integrations

Connect these in **Zo Settings > Integrations**:

- Google Drive
- Google Calendar
- Gmail

## Webhook Ingestion

This skill supports receiving data via webhooks.

```bash
python3 scripts/webhook_setup.py --register
```

## Configuration

```bash
cp config/settings.yaml.example config/settings.yaml
```

## License

MIT

---

Built for [Zo Computer](https://zo.computer).