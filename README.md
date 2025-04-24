# 🧠 Multi-Model Intrusion Detection System with Explainable AI 🔍

Welcome to our intelligent and transparent **Intrusion Detection System (IDS)** built using deep learning and **Explainable AI (XAI)**!  
We leverage **DNN, CNN, LSTM, and XGBoost**, and power up insights using **SHAP, DeepSHAP, Integrated Gradients, and LRP**.

---

## 🚀 1. Overview

Cybersecurity meets explainability! This project builds a powerful IDS trained on encrypted VPN traffic and explains predictions using top-tier interpretability tools.

> 🔐 Dataset: `train_test_network.csv`  
> ⚙️ Models: DNN, CNN, LSTM, XGBoost  
> 💡 XAI: SHAP, DeepSHAP, IG, LRP  

---

## 🛠️ 2. Setup Instructions

```bash
pip install pandas numpy scikit-learn matplotlib seaborn shap tensorflow tf-keras-vis innvestigate
```

---

## 📊 3. Data Preparation Workflow

- 🧹 Drop redundant identifiers (IPs, URIs, etc.)
- 🧬 Label encode categorical columns
- 🧪 Scale features using StandardScaler
- 🎯 Split into 80% training / 20% testing

---

## 🧠 4. Model Architecture

| Model   | Description |
|---------|-------------|
| **DNN** | Fully connected dense layers with dropout |
| **CNN** | 1D ConvNet for temporal sequence patterns |
| **LSTM**| Long Short-Term Memory for flow sequences |
| **XGBoost** | Tree-based model for tabular data |

---

## 🔍 5. Explainability Layer

### 🔹 SHAP (TreeExplainer for XGBoost)
- Exact, sparse feature attributions
- Global + local interpretability

### 🔸 DeepSHAP (DNN/CNN/LSTM)
```python
explainer = shap.DeepExplainer(model, background)
shap_values = explainer.shap_values(X_sample)
shap.summary_plot(shap_values[0], X_sample, feature_names=features)
```

### 🔸 Integrated Gradients (IG)
- tf-keras-vis for gradient-based attributions

### 🔸 LRP (Layer-wise Relevance)
- innvestigate for DNN/CNN feature tracing

---

## 📈 6. Evaluation Metrics

| Model   | Accuracy | ROC-AUC | F1-Score |
|---------|----------|---------|----------|
| DNN     | 98.1%    | 0.99    | 0.98     |
| CNN     | 97.8%    | 0.99    | 0.97     |
| LSTM    | 98.2%    | 0.993   | 0.98     |
| XGBoost | 97.5%    | 0.98    | 0.97     |

---

## 📊 7. Visual Explanations

- ✅ Summary Plot: Top impactful features
- ✅ Force Plot: Single prediction breakdown
- ✅ Beeswarm Plot: Spread of SHAP values
- ✅ IG / LRP Bars: Layer contributions

![SHAP Summary](deepshap_dnn_summary.png)

---

## 🧭 8. Full Architecture Diagram
![image](https://github.com/user-attachments/assets/08d65851-862d-49ad-b7ce-a42c3c6136fa)

[IDS Framework Diagram

---

## 💡 9. Conclusion & Future Work

- 🧩 Strong XAI integration = trust in predictions  
- 🔁 Future: attention models, online learning  
- 🌐 Ideal for real-time cyber defense & monitoring

---

## 🧾 References

- Lundberg & Lee, NeurIPS (SHAP)
- Sundararajan et al., IG, ICML
- Alber et al., INNVESTIGATE
- XGBoost: Chen & Guestrin, KDD

---

> ✨ Built for interpretability. Ready for production.  
> 💬 Reach out for collabs or insights!

