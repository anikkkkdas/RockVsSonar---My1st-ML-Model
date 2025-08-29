# Sonar Rock vs Mine Classification  

This project uses a **Logistic Regression** model to classify sonar signals as either **Rock** or **Mine**. The dataset is the classic **Sonar dataset**, where 60 numeric features represent energy values of sonar signals bounced off surfaces.  

## Project Workflow  

1. **Import Dependencies**  
   - NumPy, Pandas  
   - Scikit-learn (`train_test_split`, `LogisticRegression`, `accuracy_score`)  

2. **Load Dataset**  
   - Load `sonar data.csv` (no header).  
   - Inspect with `.head()`, `.shape()`, `.describe()`.  

3. **Preprocess Data**  
   - Separate features (X) and labels (y).  
   - Convert categorical target values into binary labels.  

4. **Train-Test Split**  
   - Split into training (90%) and test (10%).  
   - Used `stratify=y` to preserve class distribution.  
   - Set `random_state=42` for reproducibility.  

5. **Model Training**  
   - Logistic Regression model initialized.  
   - Fit on training data:  
     ```python
     LRmodel = LogisticRegression()
     LRmodel.fit(x_train, y_train)
     ```  

6. **Evaluation**  
   - Predictions made on test data.  
   - Accuracy calculated with `accuracy_score`.  

7. **Result**  
   - Model achieves good accuracy for a baseline Logistic Regression approach.  
   - Can be extended with other algorithms (SVM, Random Forest, etc.).  

## How to Run  

1. Clone this repository  
2. Install requirements:  
   ```bash
   pip install numpy pandas scikit-learn
   ```  
3. Place `sonar data.csv` in the project folder.  
4. Open and run `11_Sonar RockVsMine.ipynb` in Jupyter Notebook or VS Code.  

## Dataset  

- **Source**: UCI Machine Learning Repository  
- **Classes**:  
  - `R` → Rock  
  - `M` → Mine  
