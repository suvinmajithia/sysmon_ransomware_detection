Sysmon Ransomware Detection 🔍💣
Ransomware detection on Sysmon logs using the SILRAD dataset. I compare a simple rule‑based detector with an XGBoost model, handle class imbalance, map events to MITRE ATT&CK, and explain decisions with SHAP.
​

🔧 What I Did
Loaded 196k+ labeled Sysmon events (benign vs ransomware).
​
Built a z‑score rule‑based detector to flag unusual events.
​
Trained an XGBoost model with class imbalance handling.
​
Used SHAP for feature importance and explainability.
​
Linked Sysmon event.code values to MITRE ATT&CK techniques like T1082 and T1556.
​

📊 Key Findings
Dataset is heavily skewed: ~8.5× more benign than ransomware events.
​
Rules: only catch ~31% of ransomware and generate many false alarms.
​
XGBoost: reaches ~99%+ F1 on ransomware with very low false positives/negatives on the test set.
​
SHAP shows fields like Image, ImageLoaded, event.code, User, and TargetObject drive most decisions.
​

🧠 Why It Matters
Shows how ML can augment rule‑based detections instead of replacing them.
​
Keeps the model explainable (SHAP) and aligned with attacker behavior (MITRE mapping), which is critical for real security operations.
​
