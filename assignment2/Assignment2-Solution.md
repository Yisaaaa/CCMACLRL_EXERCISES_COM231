# Linear Regression Activity: Predicting Exam Scores

We want to predict a student’s **Exam Score ($y$)** based on the number of **Hours Studied ($x$)**.

---

## Data

| Student | Hours Studied ($x$) | Exam Score ($y$) |
| ------- | ------------------- | ---------------- |
| 1       | 1                   | 52               |
| 2       | 2                   | 57               |
| 3       | 3                   | 61               |
| 4       | 4                   | 65               |
| 5       | 5                   | 70               |

---

## Task

We want to fit a **linear regression line** of the form:

$$
y = mx + b
$$

A new student studied **6 hours**. We want to predict the **Exam Score** using the regression equation.

---

### 1. Fill in the table (14 points)

- Compute **$x^2$** for each student.
- Compute **$xy$** for each student.
- Find the totals: **$Σx$**, **$Σy$**, **$Σx^2$**, and **$Σxy$**.

| Student | Hours Studied ($x$) | Exam Score ($y$) | $xy$          | $x^2$          |
| ------- | ------------------- | ---------------- | ------------- | -------------- |
| 1       | 1                   | 52               | **52**         | **1**          |
| 2       | 2                   | 57               | **114**         | **4**          |
| 3       | 3                   | 61               | **183**         | **9**          |
| 4       | 4                   | 65               | **260**         | **16**          |
| 5       | 5                   | 70               | **350**         | **25**          |
|         | $Σx$ = **15**        | $Σx$ = **305**     | $Σxy$ = **959** | $Σx^2$ = **55** |



---

## 2. Compute the Slope $m$ (5 points)

$$
m = \frac{n(\sum xy) - (\sum x)(\sum y)}{n(\sum x^2) - (\sum x)^2}
$$

$$
m = 4.4
$$


<img width="300" height="400" alt="image" src="slope.jpg" />

---

## 3: Compute the Intercept $b$ (5 points)

$$
b = \frac{\sum y - m \sum x}{n}
$$

$$
b = 47.8
$$

<img width="300" height="400" alt="image" src="y_cept.jpg" />

---

## 4. Regression Equation (5 points)

Write the regression line:

$$
y = mx + b
$$

$$
y = 4.4(x) + 47.8
$$

---

## 5. Draw the regression line using a scatter plot (10 points)

- Calculate $y_{predict}$ for each data points
- Draw a regression line using $y_{predict}$
- Use a circle 🔵 for all data points
- Use a red line for the regression line

<img width="300" height="300" alt="image" src="line.png" />


| Student | Hours Studied ($x$) | Exam Score ($y$) | Predicted Exam Score ($y_{predict}$) |
| ------- | ------------------- | ---------------- | ------------------------------------ |
| 1       | 1                   | 52               | **52.2**                                    |
| 2       | 2                   | 57               | **56.6**                                    |
| 3       | 3                   | 61               | **61**                                    |
| 4       | 4                   | 65               | **65.4**                                    |
| 5       | 5                   | 70               | **69.8**                                    |


<img width="400" height="300" alt="image" src="y_pred.jpg" />

---

## 6. Calculate the Sum of Squared Errors (20 points)

$$
SSE = \sum (y*i - y*{predict})^2
$$

| Student | Hours Studied ($x$) | Exam Score ($y$) | Predicted Exam Score ($y_{predict}$) | $y_i-y_{predict}$ | $(y_i-y_{predict})^2$ |
| ------- | ------------------- | ---------------- | ------------------------------------ | ----------------- | --------------------- |
| 1       | 1                   | 52               | **52.2**                             | **-0.2**          | **0.04**              |
| 2       | 2                   | 57               | **56.6**                             | **0.4**           | **0.16**              |
| 3       | 3                   | 61               | **61**                               | **0**             | **0**                 |
| 4       | 4                   | 65               | **65.4**                             | **-0.4**          | **0.16**              |
| 5       | 5                   | 70               | **69.8**                             | **0.2**           | **0.04**              |
|         |                     |                  |                                      |                   | $SSE$ = 0.40          |

<img width="500" height="200" alt="image" src="sse.jpg" />

<br>
<br>

---

## 7. Calculate the Sum of Squared Total (20 points)

- Get $\bar{y}$ using this formula :

$$
\bar{y} = \frac{\sum y_i}{n}
$$

<img width="400" height="200" alt="image" src="y_mean.jpg" />

<br>
<br>

- Get $SST$ using this formula :

$$
SST = \sum (y_i - \bar{y})^2
$$

| Student | Hours Studied ($x$) | Exam Score ($y$) | Mean ($\bar{y}$) | $y_i-\bar{y}$ | $(y_i-\bar{y})^2$ |
| ------- | ------------------- | ---------------- | ---------------- | ------------- | ----------------- |
| 1       | 1                   | 52               | **61**                | **-9**            | **81**                 |
| 2       | 2                   | 57               | **61**                | **-4**            | **16**                 |
| 3       | 3                   | 61               | **61**                | **0**             | **0**                 |
| 4       | 4                   | 65               | **61**                | **4**             | **16**                 |
| 5       | 5                   | 70               | **61**                | **9**             | **81**                 |
|         |                     |                  |                  |               | $SST$ = **194**         |


<img width="300" height="200" alt="image" src="sst.jpg" />

---

## 8. Compute $R^2$ (20 points)

- Get $R^2$ using this formula :

$$
R^2 = 1 - \frac{SSE}{SST}
$$

$$
R^2 = 0.998
$$

<img width="300" height="200" alt="image" src="r2.jpg" />

---

## 9. Prediction (1 point)

Use your equation to predict the exam score for a student who studied **6 hours**.

$$
y = m(6) + b
$$

$$
y = 4.4(6) + 47.8
$$
$$
y = 74.2
$$

