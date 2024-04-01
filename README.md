# 🖥️ R | Analyzing and Visualizing Biological Data | Data Visualization and Manipulation in R

## Description
- This project involves two tasks: data visualization and function definition in R. In Problem 2, the code focuses on loading data from an Excel file, visualizing it using ggplot2, and displaying the plots. This task enhances skills in data import and visualization, utilizing popular R packages for data analysis. In Problem 3, the code defines a custom function to extract middle elements from a vector, demonstrating proficiency in function definition, conditional statements, and vector manipulation. Overall, the project improves skills in R programming, data analysis, and function creation for common data manipulation tasks.

## 📊 Data Visualization with ggplot2

<b> Code Overview: </b>
- This code loads data from an Excel file (`BeaverData.xlsx`) using the `readxl` package, creates two plots using `ggplot2` to visualize body temperature against time of day, and displays the plots.

```r
if (!require("readxl")) install.packages("readxl", dependencies = TRUE)
if (!require("ggplot2")) install.packages("ggplot2", dependencies = TRUE)
library(readxl)
library(ggplot2)
library(readxl)
BeaverData <- read_excel("Downloads/BeaverData.xlsx")
print(BeaverData)
plot1 <- ggplot(BeaverData, aes(x = time, y = temp)) +
  geom_point() +
  geom_smooth(method = "lm") +
  labs(title = "Body Temperature vs Time of Day",
       x = "Day",
       y = "Temp")
plot2 <- ggplot(BeaverData, aes(x = time, y = temp)) +
  geom_line() +
  labs(title = "Body Temperature vs Time of Day",
       x = "Time of Day",
       y = "Body Temperature")
print(plot1)
print(plot2)
```

<b> Skills Developed - </b>

Package Management: 
- Demonstrates installing and loading packages (`readxl` and `ggplot2`) for data import and visualization.
  
Data Import: 
- Reads data from an Excel file into R using the `read_excel` function.
  
Data Visualization: 
- Creates scatter and line plots with smooth lines using `ggplot2`, customizing labels and titles.

## 🌱 Function for Extracting Middle Elements

<b> Code Overview: </b>
- This code defines a function `getMiddle()` to extract middle elements from a vector, excluding the first and last elements. It then applies the function to a test vector and prints the result.

```r
getMiddle <- function(input_vector) {
  if (length(input_vector) < 3) {
    print("Vector must have at least three elements.")
    return(NULL)}
  middle_vector <- input_vector[-c(1, length(input_vector))]
  return(middle_vector)}
testVector <- c(1, 2, 3, 4, 5)
result <- getMiddle(testVector)
print(result)
```

<b> Skills Developed - </b>

Custom Function Definition: 
- Defines a custom function to perform a specific task, enhancing code modularity and reusability.
  
Conditional Statements: 
- Implements conditional logic to handle cases where the input vector has fewer than three elements.
  
Vector Manipulation: 
- Utilizes indexing operations to extract middle elements from a vector.
