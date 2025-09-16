# Data-Science-Portfolio
My Data Science portfolio, featuring projects from foundational learning to advanced Kaggle competitions.
# Laptop Price Calculator

## Overview
This is a simple Python script designed to estimate the price of a laptop. The calculation is based on two main factors: the laptop's age and its RAM size. This project is a foundational exercise to practice creating and using functions in Python.

## How It Works
The script uses a simple formula to calculate the final price:
- **Base Price:** Starts with a base price of 25,000 Baht.
- **Age-based Depreciation:** The price is reduced by 3,000 Baht for every year the laptop is old.
- **RAM-based Increase:** The price is increased by 5,000 Baht for every 8 GB of RAM installed.

The core logic is contained within the `calculate_laptop_price` function.

## How to Use
To use the function, you just need to call it with two parameters:
- `release_year`: The year the laptop was first released (e.g., 2023).
- `ram_size_gb`: The total RAM in GB (e.g., 16, 32).

**Example Usage:**
```python
# Example 1: Calculating the price for a 2-year-old laptop (released in 2023) with 16 GB of RAM.
calculate_laptop_price(release_year=2023, ram_size_gb=16)

# Example 2: Calculating the price for a brand new 2025 laptop with 32 GB of RAM.
calculate_laptop_price(release_year=2025, ram_size_gb=32)
Results
The price of a 2023 laptop with 16GB RAM is: 29,000.00 Baht

The price of a 2025 laptop with 32GB RAM is: 45,000.00 Baht
