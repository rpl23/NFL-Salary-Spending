# NFL Salary Cap Analysis Dashboard

An interactive dashboard for analyzing NFL team salary cap distributions across offense and defense. This project provides comprehensive visualizations and insights into team spending patterns for the 2024 season.

## Features

- **Interactive Visualizations**
  - Offense vs Defense Spending Scatter Plot
  - Top 10 Total Spenders Bar Chart
  - Offensive/Defensive Split Analysis
  - Spending Distribution Box Plots

- **Data Analysis**
  - Team-by-team spending breakdown
  - Offensive/defensive spending ratios
  - Statistical distribution analysis
  - Key spending insights and trends

## Requirements

```bash
pip install pandas numpy matplotlib seaborn plotly requests beautifulsoup4
```

### Dependencies
- pandas
- numpy
- plotly
- requests
- beautifulsoup4
- datetime

## Installation

1. Clone the repository
```bash
git clone [repository-url]
cd nfl-salary-analysis
```

2. Install required packages
```bash
pip install -r requirements.txt
```

## Usage

1. Run the main script:
```python
python nfl_salary_analysis.py
```

2. The script will:
   - Fetch current NFL salary data
   - Generate an interactive dashboard
   - Save the dashboard as 'nfl_salary_analysis_2024.html'
   - Print key insights to the console

## Project Structure

```
.
├── nfl_salary_analysis.py    # Main script
├── requirements.txt          # Project dependencies
└── nfl_salary_analysis_2024.html  # Generated dashboard
```

## Functions

### `scrape_salary_data()`
- Retrieves NFL salary cap data
- Returns a DataFrame with team-by-team offensive and defensive spending

### `create_dashboard(df)`
- Creates an interactive Plotly dashboard with four key visualizations
- Parameters:
  - `df`: DataFrame containing salary data
- Returns: Plotly figure object

### `generate_insights(df)`
- Calculates key statistics and insights from the salary data
- Returns dictionary of insights including:
  - Total spending statistics
  - Offensive/defensive spending breakdowns
  - Team-specific highlights

### `main()`
- Orchestrates the entire analysis pipeline
- Returns dashboard and insights objects

## Dashboard Components

1. **Offense vs Defense Scatter Plot**
   - Interactive visualization of team spending distribution
   - Hover for detailed team information

2. **Top 10 Spenders Bar Chart**
   - Stacked bar chart of highest-spending teams
   - Split by offensive and defensive spending

3. **Offensive/Defensive Split Analysis**
   - Percentage breakdown of spending by team
   - Sorted by total spending

4. **Spending Distribution**
   - Box plots showing statistical distribution
   - Separate analysis for offensive and defensive spending

## Data Structure

The analysis uses the following data format:
```python
{
    'Team': str,       # Team abbreviation
    'Offense': float,  # Offensive spending
    'Defense': float   # Defensive spending
}
```

## Customization

To modify the dashboard:
1. Edit the `create_dashboard()` function for visual changes
2. Update the `scrape_salary_data()` function for different data sources
3. Modify color schemes and layout in the Plotly configuration

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Error Handling

The script includes error handling for:
- Data scraping failures
- Invalid data formats
- Dashboard generation issues

## Output

The script generates:
1. Interactive HTML dashboard
2. Console output with key insights
3. Reusable data structures for further analysis

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Salary data sourced from Over The Cap
- Built with Plotly's interactive visualization library
