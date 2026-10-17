# AEGIS Cloud Defense

An AWS security dashboard for the Amazon Developers Hackathon. AEGIS shows what needs fixing in a cloud account, lets a three-model AI council explain it, and proves the risk by attacking itself.

## Features

- **Threat radar** with a live sweep. Every finding is a clickable dot.
- **Red team simulation**: AEGIS plays the attacker against your findings. Fix one link, run it again, and the attack is blocked.
- **AI council**: Sentinel (detection), Oracle (strategy and breach cost) and Forge (exact fixes), plus a consensus answer.
- **Review-first remediation**: see the exact command and its effect, then approve. Nothing runs on its own.
- Breach cost estimate, 30-day score trend, shield rank and badges
- Findings with search and filters, asset inventory, compliance coverage (CIS, SOC 2, ISO 27001, PCI DSS)
- Command palette (Ctrl or Cmd + K), simulated scan, live threat feed, CSV export
- Responsive layout

## AI modes

- **Simulated (default):** the council answers from rules over the live findings. No network calls.
- **Live AI (optional):** paste an Anthropic API key in the AI council tab. The key stays in your browser's localStorage and requests go straight from the browser to the Anthropic API. This is for demos only. Never ship a real key in a public page; a production version would call a backend.

## Run locally

No install or build step. Open `index.html` in a modern browser.

## Publish with GitHub Pages

1. Push this repository to GitHub.
2. Open **Settings, Pages**.
3. Choose **Deploy from a branch**, pick the default branch and the `/ (root)` folder, then save.

## Project structure

```text
.
├── index.html   (the whole app: HTML, CSS and JavaScript in one file)
├── README.md
├── LICENSE
└── .gitignore
```

## Demo scope

The account, findings, assets and scan results are illustrative sample data. AEGIS does not connect to or change any AWS account. A live version needs AWS onboarding and a backend that reads Security Hub, AWS Config and inventory. Any remediation must be separately permissioned, require explicit approval and write an audit record.

## License

MIT. See `LICENSE`. Replace `YOUR NAME` in that file with your own name.
