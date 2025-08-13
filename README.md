# Secure-EVCS-demand-forecasting-under-adversarial-and-false-data-injection-attacks
The purpose of this repository is to provide code and data for forecasting electric vehicle (EV) charging demand, evaluating model performance under cyber-attacks (including FGSM, BIM, and scaling FDI), and implementing adversarial training to enhance resilience and accuracy. The manuscript titled "Secure Electric Vehicle Charging Station Demand Forecasting under Adversarial and False Data Injection Attacks," which is based on this project, is currently under review. Therefore, only the dataset and a few images are available at this time. **The code and trained models will be published once the paper has been accepted for publication.**


## **Dataset**  
 The data utilized in this research originates from Palo Alto, a city located in the United States of America (USA), [Available](https://github.com/Najmul1801098/Secure-EVCS-demand-forecasting-under-adversarial-and-false-data-injection-attacks/tree/b16f809997060d82e95bb57be0097cb357c1d8b9/Dataset)

  
<p align="center">
  <img src="Images/EVCS_station.png" width="400" alt="EVCS Charging Station">
</p>

## Attacks

This project considers three types of attacks on EVCS demand forecasting models:

1. **Fast Gradient Sign Method (FGSM)**  
   - **Description:** A gradient-based adversarial attack that perturbs input data in the direction of the gradient to maximize the model’s prediction error.  
   - **Equation:** `X_adv = X + epsilon * sign(∇_X J(theta, X, y))`  

2. **Basic Iterative Method (BIM)**  
   - **Description:** An iterative version of FGSM that applies small perturbations multiple times to increase the attack’s effectiveness.  
   - **Equation:** `X_0_adv = X; X_(n+1)_adv = Clip_X,epsilon{X_n_adv + alpha * sign(∇_X J(theta, X_n_adv, y))}`  

3. **Scaling-based False Data Injection (FDI)**  
   - **Description:** A data manipulation attack that scales certain input values by a factor to inject false readings into the dataset.  
   - **Equation:** `X_attacked = X * scale_factor`  





## **Installation**  

This code is compatible with Python 3.8+ and uses the following main dependencies:

- **Pandas** version 1.5.3  
- **NumPy** version 1.24.3  
- **Matplotlib** version 3.7.1  
- **Seaborn** version 0.12.2  
- **Scikit-learn** version 1.2.2  
- **CatBoost** version 1.2.4  
- **Keras** version 2.12.0  
- **TensorFlow** version 2.12.0 (for Keras backend)

The remainder of the dependencies are standard Python packages and may come pre-installed with distributions like Anaconda.



1. **Clone the Repository:**  
   
bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository in this add table of contents
