# BMI Calculator

This is a simple Bash script that calculates the **Body Mass Index (BMI)** based on the user's height, weight, and age. The script also categorizes the BMI into appropriate health categories based on the user's age.

## Features

- Accepts **height** (in meters), **weight** (in kilograms), and **age** (in years) as input.
- Validates user inputs to ensure they are positive numbers.
- Calculates BMI using the formula:

BMI = weight / (height * height)

markdown
Copy
Edit
- Categorizes BMI based on age:
- For users **19 years or younger**, thresholds are based on pediatric BMI guidelines.
- For users **20 years or older**, thresholds follow standard WHO BMI categories.

## BMI Categories

### Adults (Age ≥ 20)
| Category        | BMI Range      |
|-----------------|----------------|
| Underweight     | BMI < 18.5     |
| Normal Weight   | 18.5 ≤ BMI ≤ 24.9 |
| Overweight      | 25 ≤ BMI ≤ 29.9 |
| Obese           | BMI ≥ 30       |

### Adolescents (Age ≤ 19)
| Category        | BMI Range      |
|-----------------|----------------|
| Underweight     | BMI < 18.5     |
| Normal Weight   | 18.5 ≤ BMI ≤ 24.9 |
| Overweight      | BMI > 24.9     |

## Prerequisites

- Bash shell (Linux/Mac or WSL on Windows).
- `bc` (Basic Calculator) command-line tool must be installed.

## How to Use

1. Clone or download this repository.
2. Make the script executable:
 ```bash
 chmod +x bmi.sh
Run the script:

bash
Copy
Edit
./bmi.sh
Follow the on-screen prompts to enter your height, weight, and age.

**Example**

$ ./bmi.sh
Enter height in meters (e.g., 1.75): 1.75
Enter weight in kilograms (e.g., 68): 68
Enter age in years (e.g., 25): 25
BMI is 22.20
You are normal weight.
