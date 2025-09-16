# Data-Science-Portfolio
My Data Science portfolio, featuring projects from foundational learning to advanced Kaggle competitions.

---

# Laptop Price Predictor

## Overview
This project is a simple Python script designed to estimate a laptop's price based on its age and RAM size. It serves as a foundational exercise to practice creating and using functions in Python.

---

## How It Works
The core logic is contained within the `calculate_laptop_price()` function. The script uses a simple formula to calculate the final price:
- **Base Price:** Starts with a base price of **25,000 Baht**.
- **Age-Based Deduction:** The price is reduced by **3,000 Baht** for every year the laptop is old.
- **RAM-Based Increase:** The price is increased by **5,000 Baht** for every 8 GB of RAM installed.

---

## Usage
To use the function, you just need to call it with two parameters: `release_year` (e.g., 2023) and `ram_size_gb` (e.g., 16).

```python
def calculate_laptop_price(release_year, ram_size_gb):
    """
    Calculates the final price of a laptop based on its age and RAM size.
    """
    current_year = 2025
    years_old = current_year - release_year
    base_price = 25000

    age_deduction = years_old * 3000
    ram_increase = (ram_size_gb / 8) * 5000
    final_price = base_price - age_deduction + ram_increase
    return final_price

# Example Usage
price_example_1 = calculate_laptop_price(release_year=2023, ram_size_gb=16)
price_example_2 = calculate_laptop_price(release_year=2025, ram_size_gb=32)

## Example Output
The program will display the final calculated price as shown below:
The price of a 2023 laptop with 16GB RAM is: 29000.00 Baht
The price of a 2025 laptop with 32GB RAM is: 45000.00 Baht
