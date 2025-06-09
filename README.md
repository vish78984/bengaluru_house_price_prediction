def calculate_bmi(weight, height):
    """Calculate BMI and return category"""
    bmi = weight / (height ** 2)
    if bmi < 18.5:
        return bmi, "Underweight"
    elif 18.5 <= bmi < 24.9:
        return bmi, "Normal weight"
    elif 25 <= bmi < 29.9:
        return bmi, "Overweight"
    else:
        return bmi, "Obesity"

# Input
try:
    weight = float(input("Enter your weight in kg: "))
    height = float(input("Enter your height in meters: "))
    bmi, category = calculate_bmi(weight, height)
    print(f"Your BMI is {bmi:.2f} and you are categorized as: {category}")
except ValueError:
    print("Please enter valid numeric input.")
