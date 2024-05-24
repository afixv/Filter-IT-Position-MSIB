# MSIB IT Opportunities Filter

This project retrieves internship opportunities from the [Magang Kampus Merdeka](kampusmerdeka.kemdikbud.go.id/program/magang/browse) and filters them for IT-related positions. The filtered data is then saved into both Excel and CSV formats.

You can also view the filtered data on the [Github Pages](https://afixv.github.io/Filter-IT-Position-MSIB/) of this repository.

## Table of Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Description of Code](#description-of-code)
- [Output](#output)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The MSIB IT Opportunities Filter script connects to the Magang Kampus Merdeka API, retrieves internship opportunities, filters them to include only those relevant to IT, and saves the filtered opportunities into Excel and CSV files.

## Requirements

- Python 3.x
- Requests library
- Pandas library
- OpenPyXL library

## Installation

1. Clone the repository:

    ```bash
    
    git clone https://github.com/yourusername/MSIB-IT-Opportunities-Filter.git
    cd MSIB-IT-Opportunities-Filter
    
    ```

2. Create a virtual environment and activate it:

    ```bash
    
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    
    ```

3. Install the required packages:

    ```bash
    
    pip install -r requirements.txt
    
    ```

## Usage

Run the script to fetch, filter, and save IT opportunities:

```bash

python script.py

```

This will generate two files:

  - MSIB_IT_updated_at_YYYY-MM-DD.xlsx
  - MSIB_IT_updated_at_YYYY-MM-DD.csv

Where YYYY-MM-DD is the current date.

## Description of Code

`get_data_from_api(url)`

Fetches data from the given API URL.

`filter_it_opportunities(data)`

Filters the data to include only IT-related opportunities. The filtering logic ensures that if the keyword "engineer" is present, it must also include another IT-related keyword to avoid non-IT engineering roles.

### Main Execution

  - Fetches data from the Magang Kampus Merdeka API.
  - Filters the data for IT opportunities.
  - Saves the filtered data into an Excel and a CSV file with the current date in the filename.

## Output

The script outputs two files:

  - An Excel file containing the filtered IT opportunities.
  - A CSV file containing the same data.
  - Both files are named with the current date to ensure they are easily identifiable.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This project is licensed under the MIT License.
