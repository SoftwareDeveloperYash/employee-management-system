# Employee Management System (EMS)

A simple console-based **Employee Management System** built in Java. It allows users to add, view, update, and remove employee records, with each employee's data stored in a separate text file.

## Features

- **Add Employee** – Create a new employee record with details like name, father's name, ID, email, position, contact, and salary.
- **View Employee** – Display the details of an existing employee using their Employee ID.
- **Update Employee** – Modify existing employee details by searching and replacing text in their record.
- **Remove Employee** – Delete an employee's record permanently.
- **Exit** – Cleanly exit the application.

## Project Structure

```
EmployManagementSystem.java   # Main file containing all classes
file<Employee_ID>.txt         # Auto-generated file for each employee's data
```

### Classes

| Class               | Responsibility                                          |
|---------------------|----------------------------------------------------------|
| `MainMenu`           | Displays the main menu options                          |
| `EmployDetail`        | Collects employee details from user input                |
| `Employee_Add`        | Creates a new employee file with entered details          |
| `Employee_Show`       | Reads and displays an employee's details from file        |
| `Employee_Remove`     | Deletes an employee's file                                |
| `Employee_Update`     | Finds and replaces text within an employee's file          |
| `CodeExit`            | Displays exit message and terminates the program           |
| `EmployManagementSystem` | Main class with `main()` method driving the menu loop    |

## How It Works

1. On startup, the menu is displayed with 5 options.
2. Based on user input, the program performs one of the following:
   - **1** → Add a new employee (creates `file<ID>.txt`)
   - **2** → View an employee's details (reads `file<ID>.txt`)
   - **3** → Remove an employee (deletes `file<ID>.txt`)
   - **4** → Update employee details (find & replace within `file<ID>.txt`)
   - **5** → Exit the application
3. Each employee's data is stored as a plain text file named `file<Employee_ID>.txt` in the project directory.

## Prerequisites

- Java Development Kit (JDK) 8 or higher installed on your system.

## How to Compile & Run

```bash
# Compile
javac EmployManagementSystem.java

# Run
java EmployManagementSystem
```

## Sample Usage

```
*******************************************
      EMPLOYEE MANAGEMENT SYSTEM
*******************************************
        --------------------
         ~$ Yashwanth Bhukya
        --------------------

Press 1 : To Add an Employee Details
Press 2 : To See an Employee Details
Press 3 : To Remove an Employee
Press 4 : To Update Employee Details
Press 5 : To Exit the EMS Portal

Please Enter choice :1
Enter Employee's name --------: John Doe
Enter Employee's Father name -: Richard Doe
Enter Employee's ID ----------: 101
Enter Employee's Email ID ----: john@example.com
Enter Employee's Position ----: Software Engineer
Enter Employee contact Info --: 9876543210
Enter Employee's Salary ------: 55000

Employee has been Added :)
```

## Known Limitations

- Employee data is stored in unencrypted plain text files — not suitable for production or sensitive data.
- The `Employee_Update` method uses simple `replaceAll` text substitution, which can unintentionally match unrelated text if the search string is not unique/specific.
- No input validation is performed on numeric fields like salary or contact number.
- Screen clearing (`\033[H\033[2J`) works reliably only on ANSI-compatible terminals (may not work properly on Windows CMD).

## Possible Improvements

- Switch to a structured storage format (CSV, JSON, or a database) instead of plain text files.
- Add input validation and exception handling for malformed inputs.
- Implement a search/list-all-employees feature.
- Add unit tests for core operations (add, update, remove, view).

## Author
**Yashwanth Bhukya**
