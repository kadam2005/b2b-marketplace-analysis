# b2b-marketplace-analysis
 End-to-end B2B marketplace data pipeline — web crawler, ETL, and EDA on IndiaMART product listings across 6 categories with 8 charts and 10 business insights


## 📌 Project Overview
This project is an end-to-end data engineering and analysis
pipeline that collects B2B product listings from IndiaMART-style
marketplaces, cleans the data, and performs deep exploratory
data analysis (EDA) to uncover meaningful business insights.



## 🎯 Objectives
- Identify and target meaningful B2B product categories
- Build a robust web crawler with anti-blocking measures
- Generate clean structured data output (JSON + CSV)
- Perform EDA with visualizations and business insights



## 📁 Project Structure

b2b_project/

 📓 notebooks/
   b2b_marketplace_analysis.ipynb

 📂 data/
       b2b_products.csv
       b2b_products.json

 📊 charts/
    chart1_category.png
    chart2_price.png
    chart3_cities.png
    chart4_heatmap.png
    chart5_verified_rating.png
    chart6_pricebox.png
    chart7_experience.png
    chart8_insights.png

 📝 README.md




## 🗂️ Target Categories
| # | Category | Subcategories |
|---|----------|---------------|
| 1 | Industrial Machinery | CNC Machine, Hydraulic Press, Compressor |
| 2 | Electronics | PCB Board, LED Light, Sensor, Power Supply |
| 3 | Textiles | Cotton Fabric, Polyester Yarn, Denim, Silk |
| 4 | Agriculture | Spices, Pulses, Rice, Organic Products |
| 5 | Chemicals | Solvent, Fertilizer, Pigment, Adhesive |
| 6 | Packaging | Corrugated Box, PET Bottle, Bubble Wrap |



## 🕷️ Crawler Architecture

    
       B2B Marketplace Crawler      

 Phase 1: Live Scraping              
           ->Rotating User-Agents (4 agents) 
           ->Random Delays (2-5 seconds)     
           ->Retry Logic (3 retries)         
           ->403/429 Block Detection         
                                     
 Phase 2: Synthetic Fallback         
            ->Log-Normal Price Distribution   
            ->Real Indian City Data           
            ->Faker Library (company names)   
            ->480 Products × 15 Fields        
                                    
 Phase 3: Output                              
           ->b2b_products.json               
           ->b2b_products.csv                





## 📊 Dataset Description
| Field | Type | Description |
|-------|------|-------------|
| product_id | String | Unique product ID |
| name | String | Product name |
| category | String | Main category |
| subcategory | String | Sub category |
| price_inr | Float | Price in Indian Rupees |
| supplier_name | String | Supplier company name |
| supplier_city | String | Supplier city |
| supplier_state | String | Supplier state |
| supplier_country | String | Country (India) |
| verified_supplier | Boolean | Verification status |
| supplier_rating | Float | Rating (1.0 - 5.0) |
| supplier_reviews | Integer | Number of reviews |
| min_order_qty | Integer | Minimum order quantity |
| years_in_business | Integer | Years of experience |
| keywords | String | Product keywords |
| scraped_at | DateTime | Collection timestamp |
| data_source | String | live or synthetic |



## 🚀 How to Run

### ✅ Option 1 - Google Colab (Recommended)

1. Go to colab.research.google.com
2. Click File → Upload Notebook
3. Upload b2b_marketplace_analysis.ipynb
4. Click Runtime → Run All
5. All charts will appear automatically


### 💻 Option 2 - Run Locally

**Step 1: Install Python**
# Download Python 3.10+ from
https://www.python.org/downloads/

**Step 2: Install Required Libraries**
pip install requests beautifulsoup4 pandas matplotlib seaborn faker lxml jupyter


**Step 3: Launch Jupyter Notebook**
jupyter notebook


**Step 4: Open and Run**

# Open notebooks/b2b_marketplace_analysis.ipynb
# Click Kernel → Restart & Run All




## 📦 Requirements

requests==2.31.0
beautifulsoup4==4.12.0
pandas==2.0.0
matplotlib==3.7.0
seaborn==0.12.0
faker==19.0.0
lxml==4.9.0
jupyter==1.0.0
numpy==1.24.0



## 📈 EDA Charts
| Chart | Description |
|-------|-------------|
| Chart 1 | Products by Category |
| Chart 2 | Price Distribution (Normal + Log Scale) |
| Chart 3 | Top 10 Supplier Cities |
| Chart 4 | State × Category Heatmap |
| Chart 5 | Verified vs Unverified + Rating |
| Chart 6 | Price Range by Category (Boxplot) |
| Chart 7 | Supplier Experience Distribution |
| Chart 8 | Key Insights Dashboard |



## 🧠 Key Insights

1. Maharashtra & Gujarat dominate B2B supply (40%+ listings)
2. Prices follow log-normal distribution (₹200 to ₹50,00,000)
3. Verified suppliers have 15% higher ratings on average
4. Industrial Machinery has highest average transaction value
5. 62% supplier verification rate across all categories
6. Most suppliers have 3-8 years of business experience
7. Packaging category has highest minimum order quantities
8. Organic & eco-friendly keywords growing in Agriculture
9. Price outliers (~17%) represent bulk enterprise orders
10. Tier-2 cities emerging as new supplier hubs




## 🛡️ Anti-Blocking Measures

✅ User-Agent rotation (4 different browsers)
✅ Random delays between requests (2-5 seconds)
✅ Session reuse to mimic real browser
✅ HTTP 429 detection → 30 second wait
✅ HTTP 403 detection → skip and fallback
✅ Retry logic (3 attempts on timeout)
✅ Synthetic fallback when blocked



## 🔧 Tech Stack

Language  : Python 3.10+
Scraping  : requests, beautifulsoup4
Data      : pandas, numpy
Charts    : matplotlib, seaborn
Synthetic : faker
Platform  : Google Colab
Output    : JSON, CSV



## 👤 Author
- **Name** : Rutika Balaji Kadam
- **Email** : ritikakadam186@gmail.com 
- **GitHub** : github.com/kadam2005



