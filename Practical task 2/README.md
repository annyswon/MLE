## MLE Advanced Machine Learning Topics

## Contents

### Lab 1 — Basic Python & Jupyter Setup (0 pts)
- Objective: Set up Python and Jupyter Notebook environment.  
- Key Steps:
  - Install Python 3.x and Jupyter Notebook
  - Practice basic Python operations (variables, loops, functions)
  - Install essential ML libraries: NumPy, Pandas, Matplotlib, Scikit-learn, PyTorch, Torchvision  
- Deliverable: Notebook with basic Python operations and short descriptions.

---

### Lab 2 — Ensemble Models (33.33 pts)
- **Dataset:** Breast Cancer (from Scikit-learn)  
- **Models Implemented:**
  - Random Forest (`RandomForestClassifier`)
  - XGBoost (`XGBClassifier`)  
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1 (via cross-validation)  

**Results Summary**  
- Random Forest: Accuracy = 96.5%, F1 = 0.9722 (stronger recall & sensitivity)  
- XGBoost: Accuracy = 95.6%, F1 = 0.9650 (balanced but slightly weaker)  

**Conclusion:**  
Both models performed well. Random Forest was slightly better overall, especially in recall, making it stronger for cancer detection. XGBoost is still a solid alternative, especially with further tuning.

---

### Lab 3 — Neural Networks with PyTorch (33.33 pts)
- **Task:** Build and train a LeNet-style CNN on CIFAR-10.  
- **Architecture:**  
  - Conv1: `nn.Conv2d(3, 6, 5)` → 456 params  
  - Conv2: `nn.Conv2d(6, 16, 5)` → 2,416 params  
  - FC1: `nn.Linear(400, 120)` → 48,120 params  
  - FC2: `nn.Linear(120, 84)` → 10,164 params  
  - FC3: `nn.Linear(84, 10)` → 850 params  
  - **Total Parameters:** 62,006  

- **Training Setup:**  
  - Loss: CrossEntropyLoss  
  - Optimizer: SGD, LR = 0.01  
  - Epochs = 10 (baseline)  
  - Batch Size = 128  

- **Results:**  
  - Accuracy: 63.57%  
  - Best F1 (~0.70–0.75): car, frog, ship  
  - Weakest performance: cat, bird  
  - Loss history: steady decline, no overfitting  

- **Limitations:**  
  - LeNet too simple for CIFAR-10  
  - Only 10 epochs  
  - No data augmentation  

- **Improvements:**  
  - Train longer  
  - Add augmentation (crop, flip)  
  - Use advanced CNNs (ResNet, VGG)  
  - LR scheduling  
  - Hyperparameter tuning  

---

## Summary
- Lab 1: Environment setup  
- Lab 2: Ensemble models → Random Forest slightly outperformed XGBoost  
- Lab 3: CNN baseline → LeNet achieved 63.57% accuracy on CIFAR-10  

This task demonstrated core ML workflows, model evaluation, and the impact of architecture and hyperparameters on performance.



