# Solace Agent Mesh - ROI Calculator

Interactive calculator for estimating the business value of Solace Agent Mesh relative to framework-only approaches (LangChain, OpenAI SDK, Bedrock, etc.).

**Live:** [solacese.github.io/sam-roi](https://solacese.github.io/sam-roi/)

## Features

- 6 value cards with live formulas
- Conservative / Base / Aggressive preset toggle
- Editable advanced assumptions
- Stack selector (adapts "Today:" text per competitor)
- Region presets for engineer cost
- Diminishing returns at scale (agents > 50)
- Export as PDF (single landscape page)
- Copy summary to clipboard
- Shareable URL (inputs encoded as query params)

## Assumptions and Sources

| Assumption | Base Value | Source |
|---|---|---|
| Effort reduction per new scenario | 40% | Field-observed across 5+ enterprise deployments |
| Token savings | 20% | BBVA production data (25% measured, 20% conservative) |
| Cost per system outage | $250K | Gartner avg downtime cost for enterprise SoR |
| Cost per additional jurisdiction | $90K | Platform team build cost (6 eng-months equivalent) |
| Pilot failure burn | 4 months x 3 engineers | Industry avg failed AI pilot duration |
| Time-to-production (today) | 16 weeks | Customer interviews, pre-SAM baseline |
| Time-to-production (SAM) | 6 weeks | Measured across early adopters |

**Validated proof points:**
- BBVA: 25% token savings, 400+ agents in production
- British Telecom: 1,000+ agents monitored

## How to Use in Customer Conversations

1. **Discovery call:** Open the calculator, plug in the prospect's numbers live. Start with Base preset.
2. **Follow-up email:** Use "Copy Summary" to paste into email with the shareable URL.
3. **Business case deck:** Export as PDF, include as an appendix.
4. **Technical deep-dive:** Open Advanced Assumptions, walk through each formula to build credibility.
5. **Executive sponsor:** Use Aggressive preset for upside scenario, Conservative for floor.

**Tips:**
- Always acknowledge these are estimates. Say "directional" not "guaranteed."
- Card 3 (systems of record) is risk-based. Frame it as insurance, not savings.
- The diminishing returns function prevents absurd numbers at scale. If a prospect has 500+ agents, the calculator stays credible.

## Development

Single HTML file, no build step. Open `index.html` in a browser.

```bash
# Serve locally
python3 -m http.server 8000
open http://localhost:8000
```

## Contributing

1. Edit `index.html` directly
2. Test all 6 cards with default and extreme inputs
3. Verify PDF export renders on one page
4. Push to `main` - GitHub Pages deploys automatically

## License

MIT
