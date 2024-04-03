
# Page Table Translation

## Description
This project implements a basic simulation of a page table used in operating systems for translating logical addresses to physical addresses. It demonstrates how logical addresses (consisting of a page number and an offset) are mapped to physical frame numbers using a page/frame table. The program handles cases where the requested page is not present in memory, simulating a page fault condition.

## Features
- **Page/Frame Table Implementation**: A data structure to represent the page/frame table for mapping logical page numbers to physical frame numbers.
- **Address Translation**: Translates given logical addresses to physical addresses using the page/frame table.
- **Page Fault Handling**: Appropriately handles cases where a page fault occurs, indicating the page is not present in memory.
- **Page Number and Offset Extraction**: For a given set of logical addresses in hexadecimal, the program outputs the corresponding page numbers and offsets.

## Setup
To run this program, you will need Python 3 installed on your machine. Python 3.6 or higher is recommended. No external libraries are required.

1. Clone this repository to your local machine using Git:
   ```
   git clone <repository-url>
   ```
2. Navigate to the cloned directory:
   ```
   cd page-table-translation
   ```

## Usage
Run the script from the command line by navigating to the project directory and executing:
```
python page_table_translation.py
```

### Input
The program expects logical addresses in hexadecimal format. These can be modified directly in the script under the `addresses` list variable.

Example:
```python
addresses = ["0x3A7F", "0xABCD", "0x5678"]
```

### Output
The script will print the translation of logical addresses to physical addresses, including the page number and offset for each address. If a page fault occurs, it will be indicated accordingly.

Example Output:
```
Logical Address: 0x3A7F => Physical Address: 0x017F, Page Number: 0x0D, Offset: 0x7F
Logical Address: 0xABCD => Page Fault at Page Number: 0x2B, Offset: 0xCD
Logical Address: 0x5678 => Physical Address: 0x0378, Page Number: 0x15, Offset: 0x78
```
