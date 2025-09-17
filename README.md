# 🌍 Iran & Regional Economy Dashboard – Power BI (2000–2024)

## 📖 Overview

This Power BI project visualizes and analyzes **Iran’s macroeconomic performance** in comparison with its neighbors and regional blocs (CIS, GCC, OPEC).
The dashboard is built using **IMF World Economic Outlook (WEO), April 2025 release**, covering the period **2000–2024**.

The analysis focuses on:

* **Nominal GDP (NGDPD)** – size of the economy in USD
* **Purchasing Power Parity GDP (PPPGDP)** – comparative living standards and consumption capacity
* **Volatility vs. Growth Analysis** – risk/reward patterns of economies
* **Country Profiles** – structured insights on each neighbor (economic structure, tiers, memberships)
* **Dynamic Flags Integration** – ISO2-driven flag rendering via Flagpedia API

---

## 🛠 Features

✅ Trend analysis of **NGDPD & PPPGDP (2000–2024)**
✅ **Bubble chart** with quadrants (Growth vs. Volatility vs. Market Size)
✅ **Tooltip pages** with detailed country insights
✅ **Dynamic flags** using ISO2 codes and external image URLs
✅ **Ranking measures** for Iran among neighbors
✅ **Custom chart titles** with indicator names + units
✅ **CAGR & Volatility measures** for quadrant classification

---

## 📂 Data Sources

* **IMF World Economic Outlook (WEO), April 2025**
* **Flagpedia API** (for flags)
* Custom contextual annotations (sanctions, JCPOA, oil price shocks)

---

## 🗂 Data Model

The dashboard follows a **star schema** with one **fact table** (`WEO`) and multiple **dimension tables**, ensuring optimized performance and analytical flexibility.

### **Fact Table**

* **`WEO`** → Core IMF dataset (Nominal GDP, PPP GDP, indicators, values by year and country).

### **Dimension Tables**

* **`DimCountry`** → Country attributes (Category, CIS/GCC membership, structure summaries).
* **`DimIndicator`** → Economic indicators (NGDPD, PPPGDP, inflation, etc.).
* **`DimUnits`** → Measurement units (Billions of USD, Index, Percent, etc.).
* **`DimYear`** → Calendar years (2000–2024).
* **`Population`** → Country population (for per capita calculations).
* **`DimCountryColor`** → Custom HEX colors for consistent visualization.
* **`ChartType`** → Controls toggle between column/line chart in visuals.
* **`Country A` / `Country B`** → Used for country comparison visuals with flags.
* **`GeoPeriods`** → Defines custom periods for geopolitical/economic analysis.
* **`IranEvents`** → Timeline of key Iran-specific events (sanctions, JCPOA, oil shocks).
* **`Oil Price`** → Historical oil prices linked to year dimension for contextual analysis.

### **Relationships**

* `WEO` links to **DimCountry, DimIndicator, DimUnits, DimYear**.
* `Population` links to **DimCountry** for per capita metrics.
* `GeoPeriods`, `IranEvents`, and `Oil Price` link to **DimYear** for contextual overlays.
* **Single-direction relationships** maintain clarity and prevent ambiguity in filters.

🔑 **Why this structure?**

* **Scalability** → Add new indicators or countries easily.
* **Performance** → Star schema ensures faster queries in Power BI.
* **Flexibility** → Enables advanced DAX measures (CAGR, volatility, quadrant analysis).

---

## 📊 Key Insights

* **Iran**: high growth potential but very volatile → “opportunity with risk”
* **Türkiye**: diversified, strong growth with moderate volatility → regional benchmark
* **GCC economies**: oil & gas dependent but fiscally strong, lower volatility
* **CIS (Russia, Kazakhstan)**: large scale, trade corridor opportunities for Iran
* **Pakistan**: catching up in NGDPD terms, stable but lower growth

---

## 🖼️ Visualizations & Design

* **16:9 canvas layout** (1280×720) → presentation-friendly
* **Consistent typography** (Calibri: titles 14pt bold, body 11–12pt)
* **Clean design** with \~20% white space for clarity
* **Quadrant labeling** in bubble chart for intuitive storytelling
* **Interactive slicers** (Year, Indicator, Country tiers)

---

## 📂 Repository Structure

```
├── IranNeighbors_EconomicTrends.pbix   # Power BI dashboard
├── README.md                           # Project documentation
├── WEOApr2025all.xlsx                  # IMF WEO dataset
├── weopub-dsd-apr2025.xlsx             # IMF metadata (indicators, definitions)
├── screenshots/                        # Dashboard preview images
│   ├── GDP_of_IR.png
│   ├── GDP_vs._PPP_of_IR.png
│   ├── Interactive_Comparison.png
│   └── Volatility_of_GDP.png
```

---

## 🚀 How to Use

1. Clone this repository:

   ```bash
   git clone https://github.com/FatiMollaei/PowerBI-Economic-Dashboard
   ```
2. Open the `.pbix` file in **Power BI Desktop (latest version)**.
3. Use slicers to explore indicators, countries, and years.
4. Hover over bubbles for quadrant insights (CAGR, Volatility, Base Value).

---

## 🎯 Skills Demonstrated

* **Power BI development** (multi-page design, tooltips, quadrant analysis)
* **DAX programming** (CAGR, volatility, quadrant classification, dynamic titles)
* **Data modeling** with star schema (fact/dim tables + contextual overlays)
* **Economic analysis & storytelling** blending data with context
* **GitHub portfolio building** (README, versioning, documentation)

---

## 📄 License

MIT License – free to use with attribution.

---

## 👤 Author

**Fatemeh Mollaei**
📧 Email: [fatimollaei@gmail.com](mailto:fatimollaei@gmail.com)
🌍 Iran, Zanjan
🎓 MBA (Master’s)
💼 IELTS Instructor | Former Strategic Planning Expert

---



