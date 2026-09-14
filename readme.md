# Student Grade Calculator

This is a simple Java console application that reads a student's name and their scores for three trimesters, calculates their final grade, and determines whether they passed or failed the academic year. 

## Project Structure

The project is divided into two primary files:

* **`Program_3.java`**: The main entry point of the application. It handles user input (reading the student's name and three grades), instantiates the `Student` object, and prints the final results. *(Note: The class inside this file is named `Program`)*.

* **`Student.java`**: An entity class representing the student. It stores the student's name and grades, and contains the logic to calculate the final grade and the missing points required to pass.

## Logic and Evaluation

The program evaluates the student based on a total maximum score of 100 points, distributed across three grades. The passing criteria are as follows:

* **Final Grade**: The sum of all three grades.
  
  $$
  Final Grade = grade1 + grade2 + grade3
  $$

* **Passing Threshold**: A student needs a minimum of **60.0 points** to pass.
  * If the final grade is $\ge 60.0$, the program outputs **PASSED**.
  * If the final grade is $< 60.0$, the program outputs **FAILED** and calculates the missing points required to reach 60.0:
    
    $$
    Missing Points = 60.0 - Final Grade
    $$

## How to Run

1. Ensure you have Java installed on your machine.
2. Open your terminal or command prompt and navigate to the project's root directory.
3. Compile the Java files (assuming they are inside `application` and `entities` folders):

   ```bash
   javac application/Program_3.java entities/Student.java
   ```

4. Run the compiled application:

   ```bash
   java application.Program
   ```

5. Enter the student's name followed by their three grades when prompted. Note: The program uses the US locale, so ensure you use a dot (`.`) for decimal values (e.g., `85.5`).