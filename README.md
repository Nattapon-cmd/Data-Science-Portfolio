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

Example Output
The program will display the final calculated price as shown below:

The price of a 2023 laptop with 16GB RAM is: 29000.00 Baht
The price of a 2025 laptop with 32GB RAM is: 45000.00 Baht
---

# Laptop Price Estimator

## Overview
This project is a simple simulation model designed to estimate the price of a laptop using two main factors: the age of the laptop and the amount of RAM. It's a great way to practice using functions and conditional logic in Python.

---
## How It Works
The core principle lies in the function. `calculate_laptop_price()` uses a formula to calculate the price based on these factors:
- **Base price:** Starting at 25,000 baht
- **Age discount:** The price will decrease by 2,000 baht per year as the laptop ages.
- **RAM increment:** The price will increase by 1,500 baht for every 8 GB of RAM added above the base 8 GB.
- **Base price:** The function guarantees that the price will not fall below 10,000 baht, even for very old laptops.

---
## Usage
Users can call the function by passing in two variables: `year` (the year of release, e.g., 2024) and `ram_gb` (the amount of RAM in GB, e.g., 16).

```python
def calculate_laptop_price(year, ram_gb):
"""
Calculates the laptop price based on the year and RAM.
This is a simplified example.
"""
base_price = 25,000 
year_factor = (2025 - year) * 2000 
ram_factor = (ram_gb - 8) * 1500 
price = base_price - year_factor + ram_factor 
return max(price, 10000)

# Example Usage
laptop_option_1 = calculate_laptop_price(2024, 16)
laptop_option_2 = calculate_laptop_price(2023, 32)
laptop_option_3 = calculate_laptop_price(2025, 8)
laptop_option_4 = calculate_laptop_price(2022, 64)

Example Output
The program displays the calculated price for each option based on the provided code:

Option 1: price is 35000 THB
Option 2: Price is 57000 THB
Option 3: Price is 25000 THB
Option 4: Price is 103000 THB

---

# Electricity Cost Calculator

## Overview
โปรเจกต์นี้เป็นสคริปต์ Python ที่เรียบง่ายสำหรับคำนวณค่าใช้จ่ายไฟฟ้าทั้งหมด โดยอิงจากปริมาณการใช้งานไฟฟ้าและราคาต่อหน่วย เป็นการฝึกใช้ฟังก์ชันและตัวแปรในภาษา Python.

---

## How It Works
หลักการทำงานหลักอยู่ในฟังก์ชัน `get_electricity_cost()` ซึ่งจะนำปริมาณการใช้ไฟฟ้ามาคูณกับราคาต่อหน่วย เพื่อให้ได้ยอดรวมค่าใช้จ่ายไฟฟ้าทั้งหมด.

---

## Usage
ผู้ใช้สามารถเรียกใช้ฟังก์ชันได้โดยส่งค่าสองตัวแปร ได้แก่ `usage_kwh` (ปริมาณการใช้ไฟฟ้าในหน่วยกิโลวัตต์-ชั่วโมง) และ `kwh_price` (ราคาต่อหน่วยในหน่วยบาท).

```python
def get_electricity_cost(usage_kwh, kwh_price):
    """
    Calculates the total electricity cost based on usage and price per unit.

    Parameters:
    usage_kwh (float): The amount of electricity used in kilowatt-hours (kWh).
    kwh_price (float): The price of electricity per unit (Bath/kWh).

    Returns:
    float: The calculated total electricity used cost.
    """

    # Calculate the total electricity cost
    cost = usage_kwh * kwh_price
    return cost

# Example of function usage
# Define the electricity usage and price per unit
electricity_usage = 150.5
price_per_kwh = 3.90

# Call the function to calculate the electricity bill
total_cost = get_electricity_cost(electricity_usage, price_per_kwh)

Example Output
โปรแกรมจะแสดงผลการคำนวณค่าใช้จ่ายไฟฟ้าทั้งหมดที่ได้:

Electricity Usage: 150.5 kwh
Price per Unit: 3.9 Baht 
Total Electricity Cost: 586.95 Baht
