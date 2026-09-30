# Awesome-Container-Tracking

## Top Container Tracking Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Ocean Freight Visibility, Container Milestone Tracking, Port Congestion & Demurrage Management*

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Container Tracking**. These tools help shippers, freight forwarders, and logistics teams monitor container movements, receive milestone alerts, predict ETAs, and manage demurrage and detention risk.



**Examples** include Vizion, project44, Terminal49, GoComet, SeaRates, ShipsGo, CargoSmart, Ocean Insights, Portcast, and Descartes (the category leaders).



**Open-source emphasis**: Container tracking has a **vibrant open-source foundation** built around **AIS (Automatic Identification System) data** and **DCSA standards**. **aisdecode** provides AIS decoding and web-based vessel tracking from serial or UDP sources . **AIS-catcher** is a mature AIS receiver for SDR dongles with 460+ stars . **AISight** delivers a full-stack vessel tracking platform with TimescaleDB, Redis, and React . **Container Tracking MCP** exposes 225 carriers to AI assistants via DCSA-normalized events . **ICD TZ** provides inland container depot management with gate operations, automated billing, and container location tracking . This section documents these production-grade solutions.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Vizion](https://www.vizionapi.com/)**  

  Container tracking API connecting to 100+ ocean carriers. Provides real-time milestone events, ETA predictions, and demurrage/detention alerts via normalized API.



- **[project44](https://www.project44.com/)**  

  Comprehensive supply chain visibility platform covering ocean, air, rail, and road. Provides container tracking, port congestion insights, and predictive ETAs across carriers.



- **[Terminal49](https://terminal49.com/)**  

  Container tracking and terminal visibility platform. Provides real-time container status, port congestion data, and demurrage risk alerts for US and global ports.



- **[GoComet](https://www.gocomet.com/)**  

  Logistics visibility platform with container tracking, freight procurement, and shipment management. Covers ocean, air, and land transportation.



- **[SeaRates](https://www.searates.com/)**  

  Logistics platform with container tracking, freight rate comparison, and shipment management tools.



- **[ShipsGo](https://shipsgo.com/)**  

  Container tracking and supply chain visibility platform. Provides real-time tracking across 200+ carriers with milestone alerts and ETA predictions.



- **[CargoSmart](https://www.cargosmart.com/)**  

  Ocean shipping visibility and collaboration platform. Provides container tracking, port congestion data, and supply chain disruption alerts.



- **[Ocean Insights](https://www.ocean-insights.com/)**  

  Ocean freight visibility platform (now part of project44). Provides container tracking, port congestion analytics, and carrier performance data.



- **[Portcast](https://www.portcast.io/)**  

  Predictive supply chain visibility platform. Provides container ETA predictions, port congestion forecasts, and risk alerts using machine learning.



- **[Descartes](https://www.descartes.com/)**  

  Logistics technology platform with container tracking, customs compliance, and global trade intelligence.



## Open-Source GitHub Projects



### AIS Decoding & Vessel Tracking



- **[aisdecode](https://github.com/madpsy/aisdecode)**  

  **AIS Decoder and Web-based Tracker for serial AIS hardware and generic UDP network data sources.** Tested with SevenStar 2rxPro and various SDR-based decoders . **Features**: Accepts NMEA 0183 data via UDP port 8101 or serial device; web interface at port 8100 showing live vessels; admin panel for station configuration; aggregator mode to push data to public aggregation servers; deduplication window (default 1s); vessel data expiration (default 24h); external lookup endpoint for vessels missing names; state persistence and logging options . **Go-based**. Designed for AIS receiver operators wanting self-hosted vessel tracking.



- **[AIS-catcher](https://github.com/jvde-github/AIS-catcher)**  

  **AIS receiver for RTL SDR dongles, Airspy R2/Mini/HF+, HackRF, SDRplay, and SoapySDR.** **460 GitHub stars, 76 forks** . C++-based, actively maintained. Provides raw AIS reception for vessel tracking pipelines. Foundation for building custom container tracking systems.



- **[AISight](https://github.com/snekkenull/AISight)**  

  **Full-stack real-time vessel tracking platform with live AIS data streaming and interactive maps** . **Tech stack**: Node.js 18+, PostgreSQL 14+ with TimescaleDB extension, Redis 7+, React frontend with Mapbox integration. **Features**: Live AIS data streaming from AISStream API, interactive map visualization, vessel search and filtering, position history tracking, REST API endpoints for vessels and tracks . Requires AISStream API key (free tier available).



### Container Tracking MCP & AI Integration



- **[Container Tracking MCP](https://github.com/lxxmng/container-tracking-mcp)**  

  **Ocean-freight MCP server for tracking containers across 200+ shipping lines (225 carriers) from Claude, ChatGPT, Cursor, or any MCP client.** Every carrier is normalized to **DCSA ocean-tracking event standard** so milestones look the same regardless of line . **Track by**: container number, bill of lading, or booking number. **Returns**: live milestone events, vessel name + IMO, live AIS vessel position, ETA with confidence percentage, demurrage & detention free-time countdown, and port congestion signals . **Tools**: getShipmentSummary, getContainerDetail, getVesselPosition, getDemurrageReport, getPortCongestion, addContainer . Hosted remote server with token-metered pricing (€49 for 3,000 tokens). Registry ID: `io.github.lxxmng/container-tracking`.



- **[marine-traffic-mcp](https://github.com/salmangada/marine-traffic-mcp)**  

  **Model Context Protocol (MCP) server for accessing Marine Traffic vessel tracking data** . **Tools**: vessel details by MMSI/IMO/ship ID, port calls history, port details, port search . **Architecture**: clean layered design with Configuration Layer, Client Layer (Marine Traffic API client), Server Layer (MCP protocol handlers), and Main Entry Point . Go-based. Enables AI assistants to query vessel positions, port calls, and port intelligence.



### Inland Container Depot & Terminal Management



- **[ICD TZ](https://github.com/navariltd/icd_tz)**  

  **Comprehensive Inland Container Depot (ICD) Management Application tailored for Tanzania operations.** Built on **Frappe framework** . **Key features**: Manifest & Bill of Lading management (MBL/HBL hierarchies, Excel import, stakeholder linking); Container reception with gate-in process and seal verification; **Advanced container tracking** with real-time status (In Yard, At Booking, At Inspection, At Payments, Delivered) and precise yard location tracking . **Yard operations**: in-yard booking, stripping, loose cargo tracking, inspections, customs verification movements, service orders linked to Sales Orders/Invoices. **Automated billing**: tariff rules by container dimensions (20ft, 40ft, 45ft, High Cube), dynamic storage periods (single/double charge), automated day limits . **Gate-out payment security**: mathematically blocks container exit if unpaid invoices exist . **Open source**.



### Container Tracking Libraries & SDKs



- **[container-tracker (@ph-itdev)](https://www.npmjs.com/package/@ph-itdev/container-tracker)**  

  **NPM package for tracking shipping containers across ports and vessels.** **Features**: register containers with vessel/origin/destination/carrier; update status (IN_TRANSIT, etc.) and ETA; get container details, filter by status or carrier; get timeline and transit duration; get milestone alerts; overall statistics; search across all fields . **MIT License**. Simple API for building container tracking into Node.js applications .



- **[AISdb](https://github.com/AISViz/AISdb)**  

  **Python package for smart AIS data storage and interaction** . Provides database utilities for storing and querying AIS vessel tracking data. Foundation for building custom analytics on AIS data streams.



### Additional Strong Open-Source Options



- **AIS Reception**: **AIS-catcher** (SDR-based, 460+ stars), **aisdecode** (serial/UDP, web tracker) .

- **Vessel Tracking Platforms**: **AISight** (full-stack, TimescaleDB + React), **Maritime Vessel Tracking** (Django + React with AISStream) .

- **Container Tracking MCP**: **Container Tracking MCP** (225 carriers, DCSA-normalized), **marine-traffic-mcp** (Marine Traffic API) .

- **Depot Management**: **ICD TZ** (Frappe-based, automated billing, gate-out security) .

- **Libraries**: **container-tracker** (NPM, MIT), **AISdb** (Python AIS storage) .



**Frameworks for building custom systems**: Combine **AIS-catcher** or **aisdecode** for AIS data reception, **AISight** for vessel tracking visualization, **Container Tracking MCP** for carrier milestone data via AI assistants, and **ICD TZ** for depot/terminal container lifecycle management. Add **PostgreSQL + TimescaleDB** for time-series vessel data and **Docker** for deployment.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Container tracking platforms handle sensitive shipment and logistics data; ensure compliance with contractual requirements and data protection regulations.

- **Open-source reality**: The open-source ecosystem for container tracking is **strong at the AIS data reception and vessel tracking layers** (**AIS-catcher**, **aisdecode**, **AISight**) and **emerging at the carrier milestone integration layer** (**Container Tracking MCP**, **marine-traffic-mcp**) . **ICD TZ** provides production-grade inland depot management with automated billing and gate-out security . However, **commercial platforms** (Vizion, project44, Terminal49) provide **direct carrier API integrations, normalized milestone events across 100+ carriers, and enterprise-grade SLAs** that open-source alternatives cannot match without significant carrier partnership and engineering investment. The open-source path is most viable for **AIS-based vessel tracking**, **AI-assisted container queries**, or **depot/terminal operations** rather than full commercial container visibility.



---



**Made for logistics engineers, freight forwarders, supply chain visibility teams, and port operations managers.**

Let's make container tracking more open, transparent, and AI-accessible.
