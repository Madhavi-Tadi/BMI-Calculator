# BMI-Calculator
# Prompt user for height and weight
read -p "Enter height in meters (M): " height
read -p "Enter weight in kilograms (KG): " weight
# Prompt user for Age
read -p "Enter age in years (Y): " age

# Calculate BMI
#BMI means body mass index
bmi=$(echo "scale=2; $weight / ($height * $height)" | bc)

# Display the result
echo "BMI is $bmi"

# Categorize BMI as per age
#age is below 19
if [ $age -le 19 ]; then
    if [ "$(echo "$bmi < 5" | bc)" -eq 1 ]; then
        echo "You are underweight"
    elif [ "$(echo "$bmi <= 84" | bc)" -eq 1 ]; then
        echo "You are normal weight"
    elif [ "$(echo "$bmi >= 85" | bc)" -eq 1 ]; then
        echo "You are overweight"
    fi
#age is above 19
else
    if [ "$(echo "$bmi < 18.5" | bc)" -eq 1 ]; then
        echo "You are underweight"
    elif [ "$(echo "$bmi <= 24.9" | bc)" -eq 1 ]; then
        echo "You are normal weight"
    elif [ "$(echo "$bmi <= 29.9" | bc)" -eq 1 ]; then
        echo "You are overweight"
    elif [ "$(echo "$bmi >= 30" | bc)" -eq 1 ]; then
        echo "You are obese"
    fi
fi
