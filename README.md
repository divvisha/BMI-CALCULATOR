# EXPERIMENT-8 CREATE A BMI CALCULATOR

## AIM:

To create a BMI calculator using react js.

## SOFTWARE:

Visual Studio Code

## ALGORITHM

1) Create a new project using Create React App or your preferred method.
Set up the necessary dependencies.
2) In your components directory, create a new file called "BMICalculator.js".
Import the necessary React dependencies.
3) Define the BMICalculator component
4) Open your App.js file.Import the BMICalculator component
5) Use the BMICalculator component in the main App component
6) Run your React.js development server to see the BMI calculator in action.

## PROGRAM:
```
java

import React, { useState } from 'react';

function BMICalculator() {
  const [weight, setWeight] = useState('');
  const [height, setHeight] = useState('');
  const [bmi, setBMI] = useState(null);

  const calculateBMI = () => {
    const heightInMeters = height / 100;    
    const bmiValue = weight / (heightInMeters * heightInMeters);
    setBMI(bmiValue.toFixed(2));
  };

  return (
    <div>
      <h2>BMI Calculator</h2>
      <div>
        <label htmlFor="weight">Weight (kg):</label>
        <input
          type="text"
          id="weight"
          value={weight}
          onChange={(e) => setWeight(e.target.value)}
        />
      </div>
      <div>
        <label htmlFor="height">Height (cm):</label>
        <input
          type="text"
          id="height"
          value={height}
          onChange={(e) => setHeight(e.target.value)}
        />
      </div>
      <button onClick={calculateBMI}>Calculate BMI</button>
      {bmi && <p>Your BMI is: {bmi}</p>}
    </div>
  );
}

export default BMICalculator;
```

## OUTPUT:
<img width="343" alt="bmi 1" src="https://github.com/divvisha/BMI-CALCULATOR/assets/127508123/7e306db1-af0d-4dd0-a7a4-ce3327b738c6">

### After the Calculation:

<img width="454" alt="bmi 2" src="https://github.com/divvisha/BMI-CALCULATOR/assets/127508123/3944cf3b-2a3d-4562-b50f-9c2577822908">


## RESULT:

Thus the BMI calculator is created.
