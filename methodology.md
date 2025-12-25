# CarbonLens Methodology

**Version 0.1 - Draft**

## Overview

This document explains the methodology for calculating AI inference carbon emissions in CarbonLens.

## Calculation Framework

### Step 1: Determine Model Power Consumption

**Formula:**
```
Power (W) = GPU_Power × Utilization × Efficiency_Factor
```

**Variables:**
- GPU_Power: Thermal Design Power of GPU (e.g., NVIDIA A100 = 400W)
- Utilization: Percentage of GPU used (typically 70-90% during inference)
- Efficiency_Factor: Accounts for cooling, power supply losses (typically 1.2-1.5)

**Example:**
- ChatGPT-4 inference on A100 GPU
- GPU_Power = 400W
- Utilization = 80% = 0.8
- Efficiency_Factor = 1.3 (includes data center overhead)
- Power = 400 × 0.8 × 1.3 = 416W

### Step 2: Calculate Energy Consumption

**Formula:**
```
Energy (kWh) = Power (W) × Time (hours) / 1000
```

**Example:**
- Power = 416W
- Time = 1 minute = 1/60 hour
- Energy = 416 × (1/60) / 1000 = 0.00693 kWh

### Step 3: Get Carbon Intensity

**Source:** Real-time power grid data

**Units:** gCO2/kWh (grams of CO2 per kilowatt-hour)

**Variation:**
- Time of day: 200-600 gCO2/kWh (peak vs off-peak)
- Location: 50-1000 gCO2/kWh (clean vs coal grids)
- Season: Varies by heating/cooling demand

**Example:**
- Atlanta, GA at 2:00 PM: 450 gCO2/kWh
- Atlanta, GA at 3:00 AM: 250 gCO2/kWh
- California at 2:00 PM: 180 gCO2/kWh

### Step 4: Calculate Emissions

**Formula:**
```
CO2 (g) = Energy (kWh) × Carbon_Intensity (gCO2/kWh)
```

**Example:**
- Energy = 0.00693 kWh
- Carbon_Intensity = 450 gCO2/kWh
- CO2 = 0.00693 × 450 = 3.12 grams

## Model Specifications

### Current Estimates

| Model | Parameters | GPU | Power (W) | Tokens/sec |
|-------|-----------|-----|-----------|------------|
| GPT-4 | 1.76T | A100 | 400 | 50 |
| GPT-3.5 | 175B | V100 | 300 | 100 |
| Claude-3 | ~500B | A100 | 400 | 60 |
| Gemini Pro | ~500B | TPUv5 | 350 | 70 |

*Note: These are estimates based on publicly available information and may not reflect exact specifications.*

## Limitations

1. **Model specifications:** Many AI companies don't publish exact specs
2. **Data center efficiency:** Varies by facility (PUE 1.1-2.0)
3. **Carbon intensity:** Real-time data not available for all regions
4. **Utilization:** Actual GPU usage varies by query complexity
5. **Batching:** Companies may batch requests, affecting per-query cost

## Future Improvements

- [ ] More accurate model specifications from research
- [ ] Real-time carbon intensity integration
- [ ] Per-token rather than per-minute calculations
- [ ] Accounting for model optimization techniques
- [ ] Validation against published company data

## References

1. Patterson et al. (2021). "Carbon Emissions and Large Neural Network Training"
2. Wu et al. (2022). "Sustainable AI: Environmental Implications, Challenges and Opportunities"
3. Strubell et al. (2019). "Energy and Policy Considerations for Deep Learning in NLP"

## Changelog

- **2025-12-25:** Initial methodology draft
