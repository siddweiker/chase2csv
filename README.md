# Chase Bank Statement Converter
A small utility for converting Chase (bank) statements to CSV

### Purpose
The CSV file generated matches the account activity you download from Chase online. The reason this script exists is because Chase only limits you to the past 90 days of activity when downloading CSV data. The reason for having the data in CSV is to use it with [h]ledger (plain text accounting)

### Installing
 * Written in Python 3.6
 * Install pdfminer with: `pip install pdfminer.six`

### Help
```
usage: chase2csv.py [-h] [--start START] [--end END]
                    [--date-format DATE_FORMAT] [--output OUTPUT] [--dir DIR]

optional arguments:
  -h, --help            show this help message and exit
  --start START         The Start Date to filter items (inclusive), uses the
                        date-format
  --end END             The End Date to filter items (exclusive), uses the
                        date-format
  --date-format DATE_FORMAT
                        The output date format, default: '%m/%d/%Y'
  --output OUTPUT       The output filename
  --dir DIR             The directory to scan pdfs from
  ```
  
  ### Output
   * A CSV file named `Extracted_Chase_Activity_Stmt_YYYYMMDD.csv`
   * CSV Header: `Type,Trans Date,Post Date,Description,Amount`
   * Trans Date is left empty as the statement does not contain it
 
