# Dataset Documentation: World Bank Data360 – Digital

##  Describe the Dataset

### Title & Source  
**Title**: Digital Data (from Data360)  
**Source**: [World Bank Data360 – Digital](https://data360.worldbank.org/en/digital)  

### File Format(s)  
- Primary access via interactive web interface (Data360 platform).  
- Data can be exported in **CSV** and **Excel (XLSX)** formats.  
- API access may be available through the broader World Bank Open Data infrastructure, though not explicitly documented on the Data360 Digital page.

### Size  
As of October 2025, the dataset includes:
- **~200+ indicators** related to digital development (e.g., internet users, mobile subscriptions, broadband access, digital government services).
- **~200+ countries and economies**.
- Temporal coverage typically spans **2000–2023**, though availability varies by indicator.
- Approximate dimensions: **~200 indicators × ~200 countries × ~20 years** → potentially **800,000+ data points**, though sparse for some country-indicator-year combinations.

### Basic Statistics  
While exact statistics depend on the specific indicator, typical numeric columns exhibit:
- **Internet users (% of population)**:  
  - Min: ~0% (e.g., fragile states in early 2000s)  
  - Max: ~100% (e.g., high-income countries post-2020)  
  - Global average (2023): ~67%  
- **Mobile cellular subscriptions (per 100 people)**:  
  - Min: <1 (historical)  
  - Max: >150 (due to multiple SIM ownership)  
  - Average (2023): ~110  
- **Fixed broadband subscriptions (per 100 people)**:  
  - Min: ~0  
  - Max: ~50+ (e.g., South Korea, UAE)  
  - Global average (2023): ~15  

>  Note: These are illustrative ranges based on known World Bank indicators; exact values require downloading and analyzing the dataset.

### Geographic or Temporal Coverage  
- **Geographic**: Global coverage, including all World Bank member countries and some territories.  
- **Temporal**: Most indicators span **2000–2023**, with higher frequency and completeness post-2010. Some newer indicators (e.g., on digital ID or cybersecurity) may start only after 2015.

### License  
- **License Type**: **Open**  
- **Reuse Conditions**:  
  - Licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.  
  - Users must **credit the World Bank** as the source.  
  - Commercial and non-commercial reuse permitted with attribution.  
  - No additional restrictions for academic or public use.

---

##  Augment the Dataset

### Complementary Dataset  
**Dataset**: [ITU ICT Indicators (International Telecommunication Union)](https://www.itu.int/en/ITU-D/Statistics/Pages/stat/default.aspx)  
**Format**: CSV, Excel, and online database  
**License**: Open (CC BY-NC-SA 3.0 IGO, with attribution)

### How the Datasets Could Be Linked or Compared  
- Both datasets cover overlapping domains: internet access, mobile penetration, broadband, and digital infrastructure.  
- **Linking keys**: Country name (or ISO 3166-1 alpha-3 codes) and year.  
- ITU data often includes **more granular technical metrics** (e.g., download speeds, fiber coverage, household ICT access) not fully covered by World Bank.

### Potential Research Questions from Combination  
1. **How do national digital policies (proxied by World Bank governance indicators) correlate with actual infrastructure deployment (from ITU)?**  
2. **Does higher mobile penetration (World Bank) translate into higher e-government usage (ITU or UN E-Government Survey)?**  
3. **Are there discrepancies between World Bank and ITU estimates for the same metric (e.g., internet users), and what might explain them?**

### Next Steps to Merge  
1. **Standardize country codes** (e.g., map both to ISO3).  
2. **Harmonize indicator definitions** (e.g., “broadband” may differ slightly).  
3. **Handle missing data**: Impute or exclude based on coverage thresholds.  
4. **Align temporal granularity** (both annual, so straightforward).  
5. **Validate overlaps** to assess consistency between sources.

>  Alternative augmentation: Combine with the **UN E-Government Development Index (EGDI)** to link infrastructure (World Bank) with digital service outcomes.

---

##  Review the Dataset Using FAIR Principles

| FAIR Principle | Assessment |
|----------------|-----------|
| **Findable** |  **Good**<br>• Clearly indexed on World Bank’s Data360 platform.<br>• Metadata includes indicator definitions, source agencies (e.g., ITU, OECD), and update frequency.<br>• Searchable by topic, country, and indicator name. |
| **Accessible** |  **Good**<br>• No login or payment required.<br>• Direct download in CSV/XLSX.<br>• Persistent URLs for indicators (e.g., `https://data360.worldbank.org/indicator/123`).<br>• However, bulk API access is not prominently documented. |
| **Interoperable** |  **Moderate**<br>• Data is machine-readable (CSV/XLSX).<br>• Uses standard country names but **lacks consistent use of ISO codes** in exports (may require mapping).<br>• Indicator metadata includes methodology, but variable naming is not always aligned with international standards (e.g., SDG indicators). |
| **Reusable** |  **Good**<br>• Clear CC BY 4.0 license.<br>• Detailed documentation per indicator (definition, source, notes).<br>• Caveats on data limitations are provided.<br>• Suitable for academic, policy, and commercial reuse with attribution. |

### Overall FAIR Rating: **High**  
The dataset is well-suited for research and policy analysis, though minor improvements in standardization (e.g., ISO codes, API access) would enhance interoperability.