# Synthetic Humans R1

A qualitative research platform using synthetic humans to conduct interviews and generate insights.

## Overview

This application is built using Streamlit and provides a platform for conducting qualitative research with synthetic human profiles. Users can configure and run studies with synthetic participants, collect data, and generate insights.

## Features

- **Qualitative Study Platform**: Run interviews with synthetic participants
- **Customizable Questions**: Configure interview questions for your study
- **Demographic Selection**: Choose from different demographic segments
- **Visualization Dashboard**: View participant demographics and data visualizations
- **Insight Generation**: AI-powered insights from interview responses
- **Export Options**: Download study results in PDF format
- **Themes and UI Customization**: Multiple color themes and UI settings

## Getting Started

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Add your API keys to the `.env` file
4. Run the app: `streamlit run 1_⌂_HOME.py`

## Key Components

- **Study Configuration**: Set up study parameters and questions
- **Participant Selection**: Choose participant demographics and count
- **Interview Process**: Automated interviews with synthetic humans
- **Results Analysis**: AI-powered insights from response data
- **Data Visualization**: Charts and graphs of demographic information
- **Report Generation**: Professional PDF reports of study findings

## File Structure

- `pages/`: Streamlit app pages
- `modules/`: Core application modules
- `modules/syn/`: Synthetic human generation and parsing utilities
- `synhumans/`: Synthetic human profile data
- `assets/`: Images and other static assets

## Technologies

- Streamlit
- OpenAI API
- PIL (Python Imaging Library)
- Matplotlib
- PDFKit
- Pandas