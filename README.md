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
   - **Equation:**  
   \[
   X_{adv} = X + \epsilon \cdot \text{sign}(\nabla_X J(\theta, X, y))
   \]  
   where \(X\) is the original input, \(\epsilon\) is the attack strength, \(J\) is the loss function, and \(\theta\) are the model parameters.

2. **Basic Iterative Method (BIM)**  
   - **Description:** An iterative version of FGSM that applies small perturbations multiple times to increase the attack’s effectiveness.  
   - **Equation:**  
   \[
   X_0^{adv} = X, \quad X_{n+1}^{adv} = \text{Clip}_{X,\epsilon} \{ X_n^{adv} + \alpha \cdot \text{sign}(\nabla_X J(\theta, X_n^{adv}, y)) \}
   \]  
   where \(\alpha\) is the step size per iteration and \(\text{Clip}\) keeps the perturbation within \(\epsilon\).

3. **Scaling-based False Data Injection (FDI)**  
   - **Description:** A data manipulation attack that scales certain input values by a factor to inject false readings into the dataset.  
   - **Equation:**  
   \[
   X_{attacked} = X \cdot \text{scale\_factor}
   \]  
   where \(\text{scale\_factor}\) controls the intensity of the attack.




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
