# EXPENSE TRACKER

#### Video Demo: https://youtu.be/yiW4xIV5rvs?si=dcr678fGsUfUkGiU


#### Description:

The **Expense Tracker** is a software that I designed to help people with expense management, allowing users to manage personal finances by recording for future analysis. Its features cover functions that can add new expenses, calculate totals, filter by category, and delete entries, those resources ensure success in tracking expenses. Data is saved in a CSV file called “expenses.csv”, enabling persistence storage, while a user-friendly interface ensures a smooth experience. With its modular structure, this program is both practical for immediate use and adaptable for future enhancements.


## Features:

1. **Add Expense**
    Users can add expense by specifying the amount and its category (e.i., "Food", "House Rent", "Internet").

2. **List Expenses**
    The program displays all recorded expenses in a structured format, showing their added amounts, categorues, and running total.

3. **Show Total Expenses**
    If the user wants to see only the total expenses, they can choose this option, and the total will be displayed for quick analysis.

4. **Filter by Category**
    Easily filter expenses by a specific category to analyze spending patterns.

5. **Delete Last Expense**
    The last expense recorded can be removed, ensuring quick correction of errors or modifications.

6. **Clear Expenses**
    Provides a clean slate by deleting all recorded expenses, both from memory and the CSv file.

7. **Exit**
    An easy way to close the program down.

## File Structure:

- **`project.py`**
    The following functions are included:
    - `load_expenses_from_csv(file_path)`: Loads expenses from a csv file by using 'os' (used to find the file_path) and 'csv' (used to open, read and append) modules.
    - `save_expenses_to_csv(file_path, expenses)`: Saves the current expense data to a CSV file named 'expenses.csv' by openning and writing to it for future use.
    - `add_expense(expenses, amount, category)`: Adds a new expense by appending it to the list.
    - `print_all_expenses(expenses)`: Prints a detailed list of all expenses and a total at the end.
    - `total_expenses(expenses)`: Calculates and returns the total amount spent.
    - `filter_expenses_by_category(expenses, category)`: Filters expenses based on the given category with a total at the end.
    - `delete_last_expense(expenses)`: Removes the most recently added expense in case of a user error.
    - `clear_all_expenses(file_path, expenses)`: Clears all expenses from "expenses.csv" file and overwrites it with an empty record.

- **`test_project.py`**
    A comprehensive suite of units tests for the project, written using `pytest`. The following tests are included:
    - `test_total_expenses(sample_expenses)`: tests the total inside of sample_expenses using the `total_expenses(expenses)` function.
    - `test_filter_expenses_by_category(sample_expenses)`: tests the `filter_expenses_by_category(expenses, category)` function by filtering a category inside of the sample_expenses.
    - `test_delete_last_expense(capsys, sample_expenses)`: tests the deleting function `delete_last_expense(expenses)` to delete the last expenses added.

- **`requirements.txt`**
    This file pip install the required library to run the project.

## Design Choices:

1. **Use CSV file**
    I decided to use CSV by its simplicity and human readability. CSV allows users to view and edit their expenses outside the program if needed.

2. **Error Handling**
    Validations are included to handle incorrect or invalid inputs. For example, the program ensures that expenses amounts are numeric and positive, reprompting until the correct input is provided.

## Before run the program:
    Install dependencies by running:
    pip install -r requirements.txt

