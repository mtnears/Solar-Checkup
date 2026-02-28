# ☀️ Solar Checkup

**Free, open-source tool to analyze your Enphase solar panels for underperformance, degradation, and failing microinverters.**

🔗 **[Run Solar Checkup](https://mtnears.github.io/Solar-Checkup/)** — no install required

---

## What It Does

Solar Checkup analyzes per-panel production data from your Enphase IQ Gateway to identify:

- **Underperforming panels** — panels producing significantly below their peers
- **Failing microinverters** — hardware issues that reduce individual panel output  
- **Degradation issues** — panels aging faster than manufacturer specifications
- **Array spread** — how evenly your panels are performing as a group

Most residential solar owners have no idea when individual panels start failing. Installers typically only monitor at the system level, and by the time you notice a drop on your electric bill, you could have been losing energy (and money) for months. This tool catches those issues early.

## How It Works

1. You open your Enphase gateway's local API in a browser tab
2. Copy the JSON data it shows (per-panel production numbers)
3. Paste it into Solar Checkup
4. Enter your panel specs (model, wattage, install date)
5. Get an instant health report with recommendations

**That's it.** No software to install, no accounts to create, no data collected.

## Privacy & Security

- **100% client-side** — all analysis runs in your browser
- **No data transmitted** — nothing is sent to any server, ever
- **No cookies, no tracking, no analytics** — zero data collection
- **Open source** — read every line of code right here in this repo
- **The only data involved** is microinverter serial numbers and wattage readings — no personal information

## What You Need

- An **Enphase IQ Gateway** on your local network (IQ Combiner or standalone)
- A **web browser** on the same network
- An **Enphase auth token** (if your gateway runs firmware 7.x+)

The tool works with any Enphase system using IQ microinverters (IQ7, IQ7+, IQ8, IQ8M, IQ8+, IQ8H, IQ8A, etc).

## The Report

Solar Checkup generates a detailed report including:

- **Overall health verdict** — green/yellow/red system status
- **Per-panel performance bars** — visual comparison of every panel
- **Health classification** — each panel rated as Excellent, Good, Fair, Watch, or Alert
- **Degradation analysis** — actual output vs expected for panel age (when specs provided)
- **Recommendations** — plain-English guidance on what to do next
- **Installer summary** — a copy-paste-ready text block with serial numbers and evidence for your solar company

## Demo Mode

Want to see the report without connecting to a gateway? Add `?demo` to the URL:

**[Try the demo](https://mtnears.github.io/Solar-Checkup/?demo)**

This loads simulated data for 16 panels with two underperformers so you can explore the full report.

## Deployment

This is a static site — just HTML, CSS, and JavaScript in a single file. It's hosted on GitHub Pages directly from this repo.

To host your own copy:

1. Fork this repo
2. Go to Settings → Pages
3. Set source to "Deploy from a branch" → `main` → `/ (root)`
4. Your copy will be live at `https://yourusername.github.io/Solar-Checkup/`

## Contributing

Found a bug? Have an idea? [Open an issue](https://github.com/mtnears/Solar-Checkup/issues) or submit a PR.

Some areas that could use help:
- Testing with different Enphase gateway firmware versions
- Adding support for additional data endpoints (production.json, inventory)
- Improving health classification thresholds based on real-world data
- SolarEdge support (future — their local API is more limited)
- Translations

## Background

This tool was born out of a real experience catching failing SolarEdge optimizers through panel-level data analysis. After going through the warranty claim process and realizing how invisible these issues are to most solar owners, we built Solar Checkup to make this kind of analysis accessible to anyone with an Enphase system.

Part of the [FranklinWH-Automation](https://github.com/mtnears/FranklinWH-Automation) project — open-source tools for solar energy management.

## License

MIT — use it however you want.
