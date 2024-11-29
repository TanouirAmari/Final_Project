# Final_Project

# Discrete Logarithm Calculator Using Index Calculus Method

This repository implements a discrete logarithm calculator using the **Index Calculus Method**. The goal is to compute the discrete logarithm of a number \( \beta \) with respect to a given base \( \alpha \) in a finite field defined by a large prime modulus \( p \). The method uses the **factor base** and B-smooth numbers to create a system of equations that is solved using modular arithmetic. Additionally, the repository includes a separate script to generate values for \( \beta \).

## Overview of the Process

### 1. **Generate the Factor Base:**
   - The factor base is a list of prime numbers used to factorize the powers of the base \( \alpha \). This base is used for checking whether the numbers \( \alpha^k \mod p \) are B-smooth.
   
### 2. **Check B-Smoothness:**
   - For each power \( \alpha^k \mod p \), check if it can be fully factorized in terms of the primes in the factor base. If so, the number is called **B-smooth**.
   
### 3. **Find Relations:**
   - Powers of \( \alpha \) are computed for various exponents, and each result is tested for B-smoothness. Relations between the logarithms of the elements in the factor base are generated for each B-smooth number.

### 4. **Solve the System of Linear Equations:**
   - The relations from the previous step are used to form a system of linear equations, which is then solved using **Gaussian elimination** (via SymPy). The solution provides the logarithms of the elements in the factor base.

### 5. **Calculate the Logarithm of \( \beta \):**
   - Using the previously computed logarithms for the factor base, the discrete logarithm of \( \beta \) is calculated. This step involves factorizing \( \beta \) and applying the logarithms of its prime factors.

### 6. **Subgroup Information:**
   - The code assumes that \( \alpha = 2317547 \) generates a subgroup of order 59407 in the finite field defined by modulus \( p = 10930889 \). The logarithms are calculated modulo the order of the subgroup to account for the non-primitive nature of \( \alpha \).

## Files in the Repository

### 1. **`main.py`**:
   - The main script that implements the **Index Calculus Method** for computing the discrete logarithm of \( \beta \). This script includes the generation of the factor base, B-smoothness checking, relations finding, and solving the system of linear equations.
   
### 2. **`Beta_generation_Tanouir.py`**:
   - A separate script used to generate values of \( \beta \), which are powers of \( \alpha \) modulo \( p \), for testing and analysis.

## How to Run the Code

### Requirements
- Python 3.x
- The required Python packages are listed in the `requirements.txt` file.




### Explications supplémentaires :
1. **Install the Dependencies** : Cette étape permet d'installer toutes les bibliothèques Python nécessaires via `pip`, en utilisant le fichier `requirements.txt`.

2. **Generate a Value for \( \beta \)** : Avant d'exécuter le script principal, on génère un nombre \( \beta \) en utilisant le script `Beta_generation_Tanouir.py`. Cela est nécessaire pour tester et calculer le logarithme discret de \( \beta \).

3. **Run the 'main.py' File** : Après avoir généré \( \beta \), il faut exécuter le script principal `main.py` qui utilise la méthode des logarithmes discrets par calcul de calcul d'index pour effectuer la tâche.

Vous pouvez maintenant copier et coller ce contenu directement dans votre fichier `README.md` sur GitHub.

### Steps to Run:

1. **Install the Dependencies**:
   First, install the necessary Python packages by running:
   ```bash
   pip install -r requirements.txt

2. **Generate a Value for \( \beta \)**:
  Before running the main script, you need to generate a value for \( \beta \). This can be done by running the `Beta_generation_Tanouir.py` script, which computes a value of \( \beta = \alpha^k \mod p \) for a random exponent \( k \). This value of \( \beta \) will be used as the target number whose discrete logarithm you will compute. To generate a value of \( \beta \), run the following command:
    ```bash
    python Beta_generation_Tanouir.py

3. **Run the `main.py` file.**






