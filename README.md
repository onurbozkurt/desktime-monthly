# Desktime Monthly Statistics

A Ruby command-line tool to fetch and display monthly work statistics from Desktime API.

## Features

- Fetches monthly work statistics from Desktime API
- Displays total and daily average work hours
- Shows online time, productive time, and overall productivity
- Lists the most productive days of the month
- Formats time durations in a human-readable way (hours and minutes)

## Prerequisites

- Ruby (any recent version)
- Bundler gem
- Desktime API key
- Your Desktime employee ID

## Installation

1. Clone this repository
2. Install dependencies:
```bash
bundle install
```
3. Copy the example environment file:
```bash
cp .env.example .env
```
4. Edit `.env` and add your Desktime API key and employee ID:
```
DESKTIME_API_KEY=your_api_key_here
EMPLOYEE_ID=your_employee_id
```

## Usage

Run the script to see your monthly statistics:

```bash
ruby desktime_hours.rb
```

The script will show:
- Total work days in the month
- Total time (online, productive, and desktime)
- Daily averages
- Overall productivity percentage
- Your top 3 most productive days

## Sample Output

```
Desktime Statistics for December 2024
--------------------------------
Work Days: 22

Total Time:
  Online Time: 39h 4m
  Productive Time: 16h 48m
  Desktime Time: 39h 4m

Daily Averages:
  Online Time: 1h 47m
  Productive Time: 46m
  Overall Productivity: 43.01%

Most Productive Days:
  2024-12-04: 23m (73.39% productive)
  2024-12-12: 1h 38m (62.65% productive)
  2024-12-01: 4h 10m (57.39% productive)
```

## Dependencies

- `httparty`: For making HTTP requests to the Desktime API
- `dotenv`: For managing environment variables
