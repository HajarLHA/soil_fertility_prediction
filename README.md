# 🌱 Soil-Fer — Soil Fertility, Crop & Fertilizer Recommendation App

A **web-based application** that analyzes soil parameters using **machine learning** to:
- Predict **soil fertility**,
- Recommend suitable **crops**,
- Suggest appropriate **fertilizers**.

This project aims to support **data-driven and sustainable agriculture**.

> ⚡ **Note:** This is a **group project** developed collaboratively. We also applied the **Design Thinking process** to empathize with users, define challenges, ideate solutions, prototype models, and test results.

---

## 📦 Repository Structure
```
soil-fer/
├── app.py                              # Main Flask app (serves web UI & predictions)
├── requirements.txt                    # Python dependencies
├── templates/                          # HTML templates for the UI
├── static/                             # CSS/JS/images assets
├── crop_recommendation_model.pkl       # Trained crop recommendation model
├── fertility_model.pkl                 # Trained soil fertility model
├── fertilizer_recommendation_model.pkl # Trained fertilizer recommendation model
├── scaler.pkl                          # Feature scaler used during training/inference
└── docs/                               # Documentation folder
    └── Design_Thinking.pdf            # Presentation of Design Thinking process
```
---

## 🛠️ Tech Stack
- **Python**, **Flask** (web framework)  
- **scikit-learn**, **NumPy**, **pandas** (ML & data processing)  
- **HTML/CSS/JavaScript** for the frontend  
- Pretrained models serialized as **.pkl**  

---

## ⚙️ Installation
1) **Clone the repository**
```bash
git clone https://github.com/HajarLHA/soil_fertility_prediction.git
cd soil_fertility_prediction
```

2) **Create & activate a virtual environment**
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

3) **Install dependencies**
```bash
pip install -r requirements.txt
```

> If installation fails on a package, upgrade pip:
```bash
python -m pip install --upgrade pip setuptools wheel
```

---

## ▶️ Run the App
```bash
python app.py
```
Open your browser at:
```
http://127.0.0.1:5000/
```

---

## 🧪 Usage

1. Open the web app in your browser.  
2. Use the appropriate form:

- **Fertility Prediction:** enter `clay`, `sand`, `CEC`, `CaCO3`, `Fe`  
- **Crop Recommendation:** enter `humidity`, `potassium (K)`, `rainfall`, `phosphorous (P)`, `temperature`  
- **Fertilizer Suggestion:** enter `phosphorous (P)`, `nitrogen (N)`, `potassium (K)`

3. Submit the form to get:
   - Fertility status (`Fertile` / `Non Fertile`)  
   - Recommended crop(s)  
   - Suggested fertilizer(s)
 
> Inputs are scaled automatically using `scaler.pkl`.

---

## 📈 Models

Pre-trained models used:
- `fertility_model.pkl` – predicts soil fertility  
- `crop_recommendation_model.pkl` – recommends the most suitable crops  
- `fertilizer_recommendation_model.pkl` – suggests fertilizer type

---

## 🎨 Design Thinking Process

1. **Problem Background** – Describe the main problem your project addresses (soil fertility, crop selection, fertilizer recommendation).  
2. **Inspiration** – Gather insights from research, datasets, or user needs that motivated the project.  
3. **Ideation** – Brainstorm possible solutions and modeling approaches.  
4. **Implementation** – Develop the app: ML models, Flask web app, frontend & backend workflow.

For a detailed presentation of our Design Thinking process, see the included PDF: [Design Thinking Presentation](docs/design_thinking.pdf)

---

## 👥 Team Members
- **AARAB Ilham** 
- **LHAMYANI Hajar** 
- **COLERE Pierjos** 
- **OUHSSAIN Asmae** 
---

## 🧰 Configuration

Adjust as needed:
- Feature order & preprocessing in `app.py`  
- HTML templates in `templates/`  
- CSS/JS in `static/`  

---

## ✅ Health Check
- Ensure model files exist in the root and paths are correct.  
- Verify feature names/order match the scaler and models.  
- Check Python/package versions against `requirements.txt`.  

---

## 🗺️ Roadmap

Future improvements and features for the app may include:  
- Exporting predictions as **CSV or PDF**  
- Supporting **regional recommendations** based on climate or soil zones  
- **Dockerizing** the app for easy deployment  
- Deploying the app to **Render, Heroku, Fly.io**, or other hosting platforms

---

## 🤝 Contributing
1. Fork the repo  
2. Create a feature branch: `git checkout -b feature/my-feature`  
3. Commit: `git commit -m "feat: add my feature"`  
4. Push: `git push origin feature/my-feature`  
5. Open a Pull Request  

---


## 🙌 Acknowledgments
- Our course instructor, Mr.CHAOUKI, for guidance and support throughout the project  
- All team members for their contributions to this group project  
- Dataset providers and open-source communities supporting agri-tech innovation  
- Developers of Python, Flask, scikit-learn, pandas, and the broader Python ecosystem
