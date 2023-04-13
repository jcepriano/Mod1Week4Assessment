# Mod1 Week4 Assessment
This assessment has two parts - some questions about this week's lessons, and an exercise focused on our Testing lesson. Work on the Questions first, then move on to the Exercise!

## Setup

Fork this repository!

## Questions (12 Points Possible)
Edit this `README.md` file - answer the BLANK questions before moving on to the exercise.  Make sure to SAVE your changes to the README before moving on!

1. Review the class definition below:
    ```c#
    public class Chair
    {
        public int Height { get; }
        public bool HasBack { get; }

        public Chair(int height, bool hasBack)
        {
            Height = height;
            HasBack = hasBack;
        }
    }
    ```
    Which of the following is NOT a valid way to create an instance of Chair? And why does this option not work?  
    A. `var bench = new Chair(24, true);`  
    B. `Chair bench = new Chair(24, true);`  
    C. `var bench = new(24, true);`  
    D. `Chair bench = new(24, true);`  
    
    C. C does not work because it's not being specified that we want a new instance of "Chair".
    
2. Imagine you are interviewing for your first job.  The interviewer asks "What can you tell me about OOP?".  Write your response below:

OOP is a type of coding where we can use objects to formulate blocks of code in our program. We can create and use objects that have methods in our program. In a class, we can write out exactly what we want the method to do when it's being used.

3. What is Automated Testing?

Automated testing is creating a second project in a program to test the code we've written. This second project is used to make sure any and all methods that have been created in a class are working properly.

4. What are some benefits of creating tests for our projects?

Creating tests gives the programmer an oportunity to assess public properties in a class. This allows the programmer to make sure properties that are meant for the user to see are working as expected.

5. When you create a test project, you do not immediately have access to the class(es) in the project that you are testing.  What do you need to do in order to have access to those classes?

To get access to the properties in a class, you first need to add a project reference. You do this by right clicking on the test project, going to "Add" in the drop down menu, and then "Project Reference..." where you can select the class.

6. Take a look at the class below.  Write out the **names** of each test you would write to verify that this class is working.
```c#
    public class Vehicle
    {
        public int NumberOfWheels { get; }
        public string Color { get; private set;  }
        public int MilesDriven { get; private set; }

        public Vehicle(int numberOfWheels, string color)
        {
            NumberOfWheels = numberOfWheels;
            Color = color;
            MilesDriven = 0;
        }

        public string Sumary()
        {
            string summary = $"This {Color} vehicle has {NumberOfWheels} wheels, and has driven {MilesDriven} miles.";
            return summary;
        }

        public void Drive()
        {
            MilesDriven += 5;
        }

        public void Paint(string newColor)
        {
            Color = newColor;
        }
    }
```
1. public void ConstructorSetsValues()
2. public void ReturnSummary()
3. public void CalculateMiles()
4. public void SetsNewColor()

## Exercise (8 Points Possible)
In Visual Studio, clone your forked repository.  
In this solution, there is a `Vehicle` project and a `Vehicle.UnitTests` project.  The class in `Vehicle.cs` is complete, but the tests for that class are not yet finished.  Add tests to the `VehicleTests.cs` file so that all the methods and properties for the `Vehicle` class have tests.  When finished, there should be a minimum of 4 tests (one is already completed for you!).

### Submission

When completed, commit the progress you have made, and push your project to GitHub.  Instructors will be following up with some video feedback!

### Rubric

This assessment has a total of **20 Points**.  Earning **10 or more** points is a **pass** and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
