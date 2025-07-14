This is a README file for the Python script `Cleaning_customer_call__list.ipynb`.

## Customer Call List Cleaning

This Jupyter Notebook (`Cleaning_customer_call__list.ipynb`) script is designed to clean and standardize a customer call list dataset. It performs several data cleaning operations using the `pandas` library.

### Dataset

The script expects an Excel file named `Customer Call List.xlsx` to be present in the same directory as the notebook.

### Cleaning Steps

The script performs the following data cleaning operations:

*   **Import Libraries**: Imports the `pandas` library for data manipulation and `re` for regular expressions.
*   **Load Data**: Loads the `Customer Call List.xlsx` file into a pandas DataFrame.
*   **Remove Duplicates**: Identifies and removes duplicate rows from the dataset.
*   **Drop Unnecessary Column**: Removes the `Not_Useful_Column` as it is not relevant for analysis.
*   **Clean Last Name Column**: Removes special characters (`/`, `_`, `.`) from the `Last_Name` column.
*   **Standardize 'Paying Customer' Column**: Replaces inconsistent values (`Y`, `N`, `N/a`) in the `Paying Customer` column with standardized `Yes`, `No`, or `None`.
*   **Clean 'Address' Column**: Replaces 'N/a' values in the `Address` column with 'None'.
*   **Standardize 'Phone_Number' Column**:
    *   Defines a function `standardize_phone_number` that uses regular expressions to extract only digits from phone numbers.
    *   Formats 10-digit phone numbers into `XXX-XXX-XXXX` format.
    *   Replaces 'N/a' values in the `Phone_Number` column with 'None'.
*   **Standardize 'Do_Not_Contact' Column**: Replaces inconsistent values (`Y`, `N`) in the `Do_Not_Contact` column with standardized `Yes` or `No`.

### How to Use

1.  **Ensure Dependencies**: Make sure you have `pandas` installed (`pip install pandas`).
2.  **Place Data File**: Place your `Customer Call List.xlsx` file in the same directory as the `Cleaning_customer_call__list.ipynb` notebook.
3.  **Run the Notebook**: Open the Jupyter Notebook and run all cells in sequence.
