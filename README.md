# Stock Data Fetcher

This project fetches stock data from the Finviz API at regular intervals and appends the data to a CSV file. The program is designed to run between specified hours and saves the fetched data along with a timestamp for each entry.

## Features

- Fetches stock data from Finviz API.
- Appends fetched data to a CSV file with timestamps.
- Runs between specified start and end times.
- Can be configured to wait for a specified duration between each data fetch.

## Prerequisites

- Python 3.x
- Required Python packages:
  - `requests`
  - `pytz`

## Installation

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/yourusername/stock-data-fetcher.git
    cd stock-data-fetcher
    ```

2. Install the required Python packages:

    ```bash
    pip install requests pytz
    ```

## Configuration

Before running the script, you can configure the following parameters to suit your needs:

- `API_URL`: The URL of the Finviz API to fetch stock data.
- `FILE_PATH`: The path to the CSV file where data will be saved.
- `USER_AGENT`: The user agent string to use for the HTTP request.
- `WAIT_TIME_SECONDS`: The number of seconds to wait between each data fetch.
- `START_HOUR`: The hour of the day (in 24-hour format) to start fetching data.
- `END_HOUR`: The hour of the day (in 24-hour format) to stop fetching data.
- `END_MINUTE`: The minute of the hour to stop fetching data.

## Usage

To run the script, simply execute the `main.py` file:

```bash
python main.py



How It Works
The script calculates the start and end times for fetching data based on the current date and specified hours and minutes.
It enters a loop that continues running until the current time reaches the end time.
Within the loop:
The script checks if the current time is greater than or equal to the start time.
If it is, it fetches data from the Finviz API.
The fetched data is then appended to the specified CSV file along with a timestamp.
The script waits for the specified duration before fetching data again.
Troubleshooting
If the script fails to fetch data, it will print an error message with the status code and response text.
Make sure the Finviz API URL and your internet connection are working correctly.
Ensure that you have the necessary write permissions for the CSV file path.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

License
This project is licensed under the MIT License.
