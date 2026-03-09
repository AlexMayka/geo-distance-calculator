<div align="center">

# 🌍 Geo Distance Calculator

**Data pipeline for calculating distances from addresses to geographic boundaries**

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)](https://selenium.dev)

<br>

<table>
<tr>
<td align="center"><h3>📍 4 stages</h3><sub>complete pipeline</sub></td>
<td align="center"><h3>🆓 Zero cost</h3><sub>no paid APIs</sub></td>
<td align="center"><h3>🎯 Accurate</h3><sub>within normal margin</sub></td>
<td align="center"><h3>📊 Visual</h3><sub>maps & charts</sub></td>
</tr>
</table>

</div>

---

## 💡 What It Does

Takes a list of **addresses** (city + full address) and calculates the **distance to the nearest geographic boundary** — all without paid geocoding APIs.

**Use cases:**
- Logistics planning — estimate delivery distances to border regions
- Risk assessment — proximity analysis for insurance or compliance
- Geospatial analytics — bulk distance calculations at scale

---

## 🔄 Pipeline

The process is split into **4 Jupyter notebooks**, each handling one stage:

| # | Stage | Notebook | Description |
|---|-------|----------|-------------|
| 1 | 🗺 **Boundary extraction** | `Finding_boundary_coordinates.ipynb` | Extract boundary coordinates from map data |
| 2 | 🧹 **Data preprocessing** | `Processing_of_input_data.ipynb` | Clean and normalize input addresses |
| 3 | 📍 **Geocoding** | `selenium/main.py` | Convert addresses to coordinates via Selenium |
| 4 | 📏 **Distance calculation** | `Calculation_of_distance.ipynb` | Haversine formula for geographic distances |

### Input

Excel file (`.xlsx`) with two columns:
- Column A: **City**
- Column B: **Full address**

### Output

DataFrame with:
- `address` — original address
- `coord` — geocoded coordinates (lat, lon)
- `dist_to_border` — distance to nearest boundary (km)

---

## 🛠 Tech Stack

| | Technology | Purpose |
|-|------------|---------|
| 🐍 | **Python** | Core language |
| 📓 | **Jupyter Notebook** | Interactive pipeline |
| 🌐 | **Selenium** | Browser-based geocoding (free) |
| 📊 | **Pandas** | Data manipulation |
| 🗺 | **GeoPy** | Geographic calculations |
| 📈 | **Matplotlib** | Visualization |

---

## 🚀 Quick Start

```bash
git clone https://github.com/AlexMayka/geo-distance-calculator.git
cd geo-distance-calculator
pip install -r requirements.txt
```

Then run notebooks sequentially: `1 → 2 → 3 → 4`

---

## 📁 Structure

```
├── Finding_boundary_coordinates.ipynb    # Stage 1: boundary coords
├── Processing_of_input_data.ipynb        # Stage 2: data cleaning
├── Calculation_of_distance.ipynb         # Stage 3: distance calc
├── selenium/main.py                      # Geocoding via Selenium
├── data/                                 # Input/output datasets
├── photo/                                # Pipeline visualizations
└── requirements.txt                      # Dependencies
```

## License

MIT
