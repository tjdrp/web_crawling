# Used iPhone Market Analysis 📱💰

This project analyzes second-hand iPhone prices from Bunjang, a South Korean marketplace.  
By scraping and visualizing market data, we help users find fair prices for used iPhones.

---

## 📌 Project Overview
- **Data Source**: Bunjang (Korean second-hand marketplace)
- **Goal**: Analyze price trends of used iPhones based on model and storage capacity.
- **Technology Stack**:
  - Web scraping: `Selenium`
  - Data processing: `Pandas`
  - Visualization: `Matplotlib`

---

## 📊 Data Collection & Processing
- **Scraping Method**: Used `Selenium` (asynchronous `requests` was not possible due to JavaScript-rendered pages).
- **Extracted Information**:
  - `Title`: Product title (e.g., "iPhone 12 Pro 256GB")
  - `Price`: Listed price in KRW
  - `Link`: Product page URL

### 🔹 Challenges
1. **Crawling Speed Issue**  
   - Initially attempted `requests` but switched to `Selenium` due to JavaScript rendering.  
   - `headless` mode was used to improve efficiency, but speed is still a limitation.  

2. **Missing Product Details**  
   - Only basic details (title, price, link) are scraped because scraping additional details (e.g., product condition) would significantly increase execution time.

---

## 📈 Price Distribution
![Price Distribution](./images/price_distribution.png)

- Prices below **200,000 KRW** and above **2,000,000 KRW** were filtered out.
- Most used iPhone listings fall between **500,000 KRW** and **1,500,000 KRW**.
