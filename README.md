# 🏗️ AI DDR Generator

An AI-powered system that automatically generates **Detailed Defect Reports (DDR)** from inspection PDF documents using Large Language Models.

---

## 🌐 Live Demo
👉 [https://ai_ddr-generator.streamlit.app
](https://ai-ddr-generator-6s9qu5jztvybzu5y2qggmh.streamlit.app/)
---

## 📌 Features

- 📄 Extracts data from inspection PDFs using pdfplumber  
- 🤖 Generates structured engineering reports using LLM (Groq API)  
- 📊 Includes:
  - Defect Identification  
  - Risk Assessment  
  - Recommendations  
- 📈 AI Confidence Score based on input data  
- 🌐 Interactive web app using Streamlit  

---

## 🛠️ Tech Stack

- Python  
- Streamlit  
- Groq API (LLM)  
- pdfplumber  

---

## ⚙️ How It Works

1. Upload inspection PDF  
2. (Optional) Upload thermal PDF  
3. Extract text from documents  
4. Process data using AI model  
5. Generate structured DDR report  

---

## 🧪 How to Use

1. Open the Live Demo  
2. Upload inspection PDF  
3. Upload thermal PDF (optional)  
4. Click **Generate DDR Report**  
5. Download the result  

---

## 📄 Sample Input Files

To test the application:

- Inspection → `sample_inputs/sample_inspection.pdf`  
- Thermal → `sample_inputs/sample_thermal.pdf`  

👉 Upload these in the app to generate DDR.

---

## ▶️ Run Locally

```bash
pip install -r requirements.txt
streamlit run app.py
