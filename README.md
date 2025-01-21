# Invoice Generator

This project is a Python-based tool for converting invoice data stored in Excel files into PDF format. It leverages libraries like `pandas`, `glob`, `fpdf`, and `pathlib` to automate the process of creating professional-looking invoices.

## Features

- Automatically processes multiple Excel files from a specified directory.
- Extracts invoice numbers and dates from file names.
- Reads and formats invoice data using `pandas`.
- Generates PDF invoices with headers, tables, and totals.
- Includes the company logo on each invoice.

## Prerequisites

Before running the project, ensure that the following are installed:

- Python 3.8+
- Required Python libraries:
  - `pandas`
  - `fpdf`
  - `openpyxl` (to handle Excel files)

You can install the required libraries using the following command:

```bash
pip install pandas fpdf openpyxl
```

## Project Structure

```
Invoice-Generator/
├── Invoices/           # Directory containing Excel invoice files
├── PDFs/               # Output directory for generated PDFs
├── logo.png            # Company logo for the PDF header
├── main.py             # Main script for the project
└── README.md           # Project documentation
```

## How to Use

1. **Place Invoice Files**
   - Add your Excel files containing invoice data to the `Invoices/` directory.
   - Ensure the file names follow the format `invoiceNumber-date.xlsx` (e.g., `1001-20250101.xlsx`).

2. **Run the Script**
   - Execute the `main.py` script:

   ```bash
   python main.py
   ```

3. **Generated PDFs**
   - The PDF invoices will be created in the `PDFs/` directory, with the same name as the input Excel files.

## Code Overview

The script performs the following steps:

1. **Import Libraries**: Utilizes `glob` to handle multiple files, `pathlib` for file paths, `pandas` for data manipulation, and `fpdf` for PDF generation.
2. **File Processing**: Reads all Excel files from the `Invoices/` directory.
3. **Extract Metadata**: Extracts invoice numbers and dates from file names.
4. **Generate PDF**:
   - Creates a header with the invoice number and date.
   - Reads and formats data from the Excel file into a table.
   - Calculates the total sum and appends it to the PDF.
   - Adds a company logo and finalizes the PDF output.

## Example Input

An Excel file (`1001-20250101.xlsx`) with the following structure:

| product_id | product_name | amount_purchased | price_per_unit | total_price |
|------------|--------------|------------------|----------------|-------------|
| 101        | Item A       | 2                | 50.00          | 100.00      |
| 102        | Item B       | 3                | 30.00          | 90.00       |

## Example Output

A PDF invoice with:

- Invoice number and date.
- Tabular data for all purchased products.
- Total sum of all items.
- Company name and logo.

## Contribution

Feel free to fork this repository and submit pull requests for improvements or new features.

## License

This project is licensed under the MIT License.

## Contact

If you have any questions or suggestions, feel free to reach out to **Mohan Rao Ganala** via [LinkedIn](https://linkedin.com/in/mohan-rao-ganala).
