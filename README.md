# SOC-Automation-Lab

Final Year Project — BSc Cybercrime — SETU Carlow — Kacper Szkutnik (C00285636)

## What this is

An automated threat intelligence pipeline built entirely from open-source tools. The goal was to connect MISP, Cortex, TheHive and Maltego into a single workflow and test whether automation actually reduces investigation time compared to doing everything manually.

It does by an average of 78% across four incident scenario types tested over two weeks.

## Tools used

- **MISP** — threat intelligence collection and IOC sharing
- **Cortex** — automated enrichment via VirusTotal, AbuseIPDB and IPInfo
- **TheHive** — case management, dashboards and investigation workflows
- **Maltego** — visual threat correlation and infrastructure mapping

## What's in this repo

SOC-Automation-Lab/
├── README.md
├── configs/
│   ├── compose.yaml         
│   ├── thehive-application.conf
│   └── cortex-application.conf
├── templates/
│   └── thehive-case-templates.json
└── docs/
└── deployment-guide.md

## Key results

| Scenario | Manual | Automated | Reduction |
|---|---|---|---|
| Phishing | 3:05 | 0:35 | 81% |
| Malware | 2:52 | 0:45 | 74% |
| Network Activity | 3:10 | 0:42 | 78% |
| Account Compromise | 2:56 | 0:35 | 80% |
| **Average** | **3:01** | **0:39** | **~78%** |


## How to set it up

See [docs/deployment-guide.md] for full instructions.

The short version:
1. Deploy MISP VM from the official image
2. Deploy TheHive and Cortex using the StrangeBee pre-configured image
3. Apply the memory optimisations in compose.yaml before running
4. Connect the platforms using the API keys and URLs in the deployment guide
5. Import the case templates into TheHive

## Supervisor

Martin Tolan — SETU Carlow
