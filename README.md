# CarbonLens 🌍

**Open-source framework for tracking AI inference carbon emissions**

[![Status](https://img.shields.io/badge/status-in%20development-yellow)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()

## Overview

CarbonLens addresses a critical gap in AI sustainability research: while most work focuses on training emissions, billions of daily AI inference queries generate ongoing carbon emissions that vary by time, location, and model architecture.

This tool provides a framework for:
- Calculating AI inference emissions based on real data
- Analyzing geographic and temporal variability
- Identifying opportunities for carbon reduction
- Providing methodology for researchers

## The Problem

- AI inference (using models) happens billions of times daily
- Emissions vary 40-60% based on time of day and location
- No existing tools track this systematically
- Individuals and organizations lack carbon accounting for AI usage

## The Solution

CarbonLens integrates:
- Real-time power grid carbon intensity data
- AI model specifications (parameters, hardware)
- Geographic and temporal analysis
- Research-grade methodology documentation

## Features (In Development)

- [x] Project structure
- [ ] Real-time carbon intensity integration
- [ ] AI model emission calculator
- [ ] Temporal variability analysis
- [ ] Geographic comparison tools
- [ ] Data export for researchers
- [ ] Interactive web interface
- [ ] Methodology documentation

## Current Status

**Version 0.1 - In Development**

Building core calculator and methodology. Expected completion: January 2026.

## Methodology

Full methodology documentation coming soon. Initial approach:

1. **Carbon Intensity:** Power grid data (gCO2/kWh) by region and time
2. **Model Power:** Estimated from architecture, parameters, hardware
3. **Usage Calculation:** Energy (kWh) = Power (W) × Time (h) / 1000
4. **Emissions:** CO2 (g) = Energy (kWh) × Carbon Intensity (gCO2/kWh)

## Data Sources

### Carbon Intensity
- **Electricity Maps** - Real-time grid carbon intensity (electricitymaps.com)
- **U.S. EPA eGRID** - Regional carbon intensity data (epa.gov/egrid)
- **WattTime API** - Marginal emissions data for California region

### AI Model Specifications
- Patterson, D., et al. (2021). "Carbon Emissions and Large Neural Network Training." arXiv:2104.10350
- Luccioni, A., et al. (2023). "Power Hungry Processing: Watts Driving the Cost of AI Deployment?" arXiv:2311.16863
- Strubell, E., et al. (2019). "Energy and Policy Considerations for Deep Learning in NLP." ACL Anthology
- NVIDIA Technical Specifications - Official GPU TDP values

### Methodology
- Standard electrical engineering calculations (P = E/t)
- Data center PUE estimates from cloud provider sustainability reports

## How to Cite
```
Vats, S. (2025). CarbonLens: Framework for AI Inference Carbon Tracking.
GitHub repository: https://github.com/sharanyavats/carbonlens
```

## Roadmap

**December 2024:**
- Build core calculator
- Establish methodology
- Create initial dataset

**January 2025:**
- Add real-time data integration
- Build web interface
- Complete documentation

**February 2025:**
- Launch public version
- Submit methodology paper
- Integrate with research projects

## Contributing

This is currently a solo research project. Suggestions and feedback welcome via Issues.

## License

MIT License - Open for research and educational use

## About

Created by Sharanya Vats as part of research on AI sustainability and computational environmental science.

**Connect:**
- Blog: https://sharanyavats.github.io/sharanyavats-blog
- GitHub: @sharanyavats(https://github.com/sharanyavats)
- Email: sharanyakvats@gmail.com

---

**Last Updated:** December 25, 2025
