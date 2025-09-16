# 🌬️ Wind EPA Rating Calculator  

A lightweight, browser-based calculator for preliminary wind EPA (Effective Projected Area) checks of light poles, fixtures, and solar attachments. Built for solar designers, lighting specialists, and engineers who need quick, field-friendly verification against ASCE 7-22 design wind speeds.  

🚀 **[Try it live](https://floridawindcalcs.com/free-wind-calculators)**  

---

## 📌 Features  
- **Inputs:**  
  - Pole height (10–40 ft)  
  - Pole type/model (fiberglass, aluminum, steel, etc.)  
  - Manufacturer EPA rating capacity (ft² @ mph)  
  - Rated wind speed (mph)  
  - Attachment EPA (ft²)  
  - Mounting height (ft, default = pole top)  
  - Design wind speed (120–170 mph)  
  - Exposure category (B, C, D per ASCE 7-22)  

- **Backend Logic:**  
  - ASCE 7-22 simplified wind pressure:  
    ```
    q = 0.00256 * V^2 * Kz * G
    ```
    where `G = 0.85`, with `Kz` interpolated by exposure & height.  
  - Calculates demand vs. capacity → **Safety Factor (SF)**.  
  - Color-coded gauge:  
    - ✅ Safe (SF ≥ 1.5)  
    - ⚠️ Monitor (1.0 ≤ SF < 1.5)  
    - ❌ Fail (SF < 1.0)  

- **Outputs:**  
  - Summary tables with user inputs and results  
  - Allowable attachment EPA at design wind speed  
  - Safety Factor and recommendation  
  - Export results to PDF  

---

## 🖥️ Usage  
1. Clone or download this repository.  
2. Open `index.html` in your browser.  
3. Fill out the form and click **Calculate**.  
4. Review results in the output section.  
5. Use **Export to PDF** to save results.  

---

## 📷 Screenshots  
*(Add screenshots of the calculator interface and output results here)*  

---

## 📜 Disclaimer  
This calculator is for **preliminary analysis only**.  
- It does **not** replace full structural design.  
- Final design must comply with ASCE 7-22, local building codes (IBC/FBC), and manufacturer specifications.  
- Sealed calculations must be reviewed and approved by a licensed Professional Engineer.  

---

## 🔮 Roadmap  
- Add a library of manufacturer pole models with preloaded EPA values  
- Optional soil/embedment resistance check  
- Improved mobile optimization  
- API endpoint for external integration  

---

## 🤝 Contributing  
Contributions are welcome! Open a pull request or issue with suggestions, bug reports, or enhancements.  

---

## 📧 Contact  
Developed by **Oasis Engineering**  
🌐 [WindCalculations.com](https://windcalculations.com)  
📩 info@oasisengineering.com  
