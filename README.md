# Business-Valuation-Tool-R---Simulations-and-Dashboard
Interactive R-based business valuation tool featuring DCF analysis, Monte Carlo simulation, and a Shiny dashboard for dynamic financial modeling and sensitivity analysis

## Overview
This R-based application provides a comprehensive business valuation tool that implements Discounted Cash Flow (DCF) analysis with Monte Carlo simulation capabilities. The tool includes sensitivity analysis features and an interactive Shiny dashboard for detailed valuation exploration.

## Features
- Monte Carlo simulation for business valuation
- Sensitivity analysis examining WACC and growth rate impacts
- Interactive Shiny dashboard with real-time simulation capabilities
- Visualization tools including heat maps and density plots
- Customizable parameters for valuation modeling

## Prerequisites
The following R packages are required:
```R
library(dplyr)
library(tidyverse)
library(ggplot2)
library(shiny)
library(shinydashboard)
library(plotly)
```

## Installation
1. Clone this repository
2. Install the required packages:
```R
install.packages(c("dplyr", "tidyverse", "ggplot2", "shiny", "shinydashboard", "plotly"))
```
3. Run the R script in your preferred R environment

## Usage
The tool offers three main components:

### 1. Basic Valuation Function
```R
s_ent_function(
    srevenue_0 = 100,      # Initial revenue
    sassets_0 = 80,        # Initial assets
    swacc = 0.12,          # Weighted Average Cost of Capital
    sassets_to = 1.3,      # Asset turnover ratio
    sgrowth = 0.5,         # Growth rate
    sgrowthstd = 0.1,      # Growth rate standard deviation
    smargin = 0.15,        # Profit margin
    smarginstd = 0.03,     # Margin standard deviation
    sterminal_g = 0.03,    # Terminal growth rate
    sterminalstd = 0.01    # Terminal growth standard deviation
)
```

### 2. Sensitivity Analysis
The script includes functionality to create heat maps showing how variations in WACC and growth rates affect the valuation.

### 3. Interactive Dashboard
The Shiny dashboard provides:
- Adjustable parameters through sliders
- Real-time Monte Carlo simulation
- Density plot visualization
- Summary statistics table

## Dashboard Parameters
- WACC (Weighted Average Cost of Capital): 8% - 16%
- Growth Rate: 3% - 10%
- Margin: 10% - 20%
- Terminal Growth Rate: 2% - 6%

## Methodology
The valuation model uses:
- Discounted Cash Flow (DCF) analysis
- Monte Carlo simulation for risk assessment
- NOPAT (Net Operating Profit After Tax) calculations
- Terminal value estimation using perpetuity growth model

## Key Components
1. **Cash Flow Projection**: Projects future cash flows based on input parameters
2. **Risk Analysis**: Incorporates uncertainty through Monte Carlo simulation
3. **Sensitivity Testing**: Examines how parameter changes affect valuation
4. **Interactive Visualization**: Provides real-time insight into valuation dynamics

## Contributing
Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss proposed changes.

## Notes
- All monetary values are in base currency units
- Default parameters are set for demonstration purposes and should be adjusted for actual use
- The model assumes steady-state conditions for terminal value calculations
