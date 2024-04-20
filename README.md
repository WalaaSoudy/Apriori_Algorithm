# Apriori_Algorithm

This Python GUI application provides functionalities for processing data using the Apriori algorithm for association rule mining.

## Features

- **File Selection**: Users can select a CSV, TXT, or Excel file containing transactional data.
- **Data Configuration**: Allows users to specify the percentage of data to use, minimum support, and minimum confidence for association rule mining.
- **Process Data Button**: Executes the data processing and association rule mining based on user-defined configurations.
- **Output Display**: Displays frequent itemsets, all combinations, and association rules in a scrollable text area.

## Data Preprocessing

The application preprocesses the data in the following steps:

1. **Load Data**: Loads transactional data from the selected file and groups transactions by transaction number.
2. **Calculate Support Count**: Calculates the support count for each individual item in the transactional data.
3. **Apriori Algorithm**: Applies the Apriori algorithm to find frequent itemsets based on the specified minimum support count.
4. **Filtering**: Filters out infrequent itemsets and retains only frequent itemsets with support count greater than or equal to the minimum support count.

## Code Explanation

### Class `DataProcessorGUI`

- **Initialization**: Initializes the GUI window with the specified title, size, and style configurations.
- **Widgets Creation**: Creates various widgets including labels, entry fields, buttons, and a text area for displaying output.
- **File Browsing**: Implements the functionality to browse and select a file using the `browse_file` method.
- **Data Processing**: Executes data processing and association rule mining using the `process_data` method.
- **Output Display**: Clears the output text area and displays frequent itemsets, all combinations, and association rules.

### Data Processing Functions

- **`load_data`**: Loads transactional data from the selected file and groups transactions by transaction number.
- **`calculate_support_count_item`**: Calculates the support count for each individual item in the transactional data.
- **`apriori`**: Applies the Apriori algorithm to find frequent itemsets based on the specified minimum support count.
- **`filter_by_support_count`**: Filters out infrequent itemsets based on the minimum support count.
- **`generate_strong_association_rules`**: Generates strong association rules based on frequent itemsets and minimum confidence.
- **`generate_all_combinations`**: Generates all possible combinations of items from frequent itemsets.

### Entry Point

- Creates an instance of the `DataProcessorGUI` class and starts the GUI application.

## Requirements

- Python 3.x
- tkinter
- pandas

