# Francis_Farm
Francis Farm: Cultivating Data, Growing Futures. Francis Farm began as a modest patch of land—just a few acres of seasonal crops and a dream. He started logging everything: rainfall patterns, crop yields, soil pH levels, labor . What began as a spreadsheet soon evolved into a full-fledged analytics dashboard powered by Python, SQL, and Power BI.

---

## 📘 Column Documentation

### 📐 Dim_Crop – Crop Metadata
| Column Name     | Description |
|-----------------|-------------|
| **Crop_ID**     | Unique identifier for each crop (e.g., C001) |
| **Crop_Name**   | Name of the crop (e.g., Tomato, Strawberry) |
| **Crop_Type**   | Category of crop (e.g., Vegetable, Fruit) |
| **Growth_Duration** | Estimated days from planting to harvest |
| **Season**      | Optimal growing season (Summer, Monsoon, Winter) |

---

### 🌳 Dim_Tree – Tree Metadata
| Column Name       | Description |
|-------------------|-------------|
| **Tree_ID**       | Unique identifier for each tree species (e.g., T001) |
| **Tree_Species**  | Tree species name (e.g., Teak, Mango, Rambutan) |
| **Planting_Year** | Year tree was planted |
| **Carbon_Absorption** | CO₂ absorbed per year (kg) |
| **Timber_Value**  | Estimated market value when mature (₹) |

---

### 📅 Dim_Date – Date Reference Table
| Column Name  | Description |
|--------------|-------------|
| **Date_ID**  | Unique date key in `YYYYMMDD` format (e.g., 20250908) |
| **Date**     | Actual calendar date |
| **Month**    | Full month name (e.g., September) |
| **Quarter**  | Fiscal quarter (e.g., Q3) |
| **Year**     | Calendar year (e.g., 2025) |

---

### 🌾 Fact_Crop_Yield – Crop Production Data
| Column Name      | Description |
|------------------|-------------|
| **Yield_ID**     | Unique identifier for each yield record |
| **Crop_ID**      | Foreign key → `Dim_Crop` |
| **Date_ID**      | Foreign key → `Dim_Date` |
| **Area_Hectares** | Land area cultivated (hectares) |
| **Yield_kg**     | Total crop yield (kg) |
| **Fertilizer_Used** | Fertilizer applied (kg) |
| **Rainfall_mm**  | Rainfall during crop cycle (mm) |

---

### 🌱 Fact_Tree_Investment – Tree Growth & Financials
| Column Name       | Description |
|-------------------|-------------|
| **Investment_ID** | Unique identifier for each tree investment record |
| **Tree_ID**       | Foreign key → `Dim_Tree` |
| **Date_ID**       | Foreign key → `Dim_Date` |
| **Maintenance_Cost** | Maintenance cost (₹) |
| **Growth_cm**     | Tree height growth (cm) |
| **Carbon_Credits** | Revenue from carbon offset programs (₹) |

---

## 🔎 Usage Ideas
- 📊 **Power BI / Tableau:** Build dashboards for crop yield analysis, tree investments, and carbon credits.  
- 🗄 **SQL / Data Warehousing:** Practice joins, aggregations, and time-series analysis.  
- 🌍 **Sustainability Analytics:** Track carbon absorption and financial impact of tree plantations.  

---

## 📂 Example Files
- `Dim_Crop.csv`
- `Dim_Tree.csv`
- `Dim_Date.csv`
- `Fact_Crop_Yield.csv`
- `Fact_Tree_Investment.csv`

---

💡 This dataset is **synthetic** and created for **educational & portfolio purposes**.  
You can use it in BI dashboards, academic projects, or GitHub portfolios.
