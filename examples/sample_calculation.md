# Sample Calculation Example

## Scenario
User: Using ChatGPT-4 for 10 minutes in Atlanta, GA at 2:00 PM

## Calculation

**Step 1: Model Power**
- ChatGPT-4 on A100 GPU
- Power = 416W (from model_specs.json)

**Step 2: Energy**
- Time = 10 minutes = 10/60 hours = 0.167 hours
- Energy = 416W × 0.167h / 1000 = 0.0694 kWh

**Step 3: Carbon Intensity**
- Atlanta at 2 PM: 450 gCO2/kWh

**Step 4: Emissions**
- CO2 = 0.0694 kWh × 450 gCO2/kWh = **31.2 grams of CO2**

## Comparisons

**Time shifting:**
- Same usage at 3 AM (250 gCO2/kWh): 17.4 grams
- **Savings: 44%**

**Location:**
- Same usage in California (180 gCO2/kWh): 12.5 grams
- **Savings: 60%**

**Equivalents:**
- 31.2g CO2 = Charging 4 smartphones
- 31.2g CO2 = Driving 0.26 km in a car
- 31.2g CO2 = 0.0015 kg (need tree to offset for 26 days)
