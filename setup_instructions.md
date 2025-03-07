# Setting Up Synthetic Humans R1

This repository is set up with the basic structure and essential files for the Synthetic Humans qualitative research platform. To complete the setup with all your local files, follow these instructions:

## Initial Setup

1. Clone this repository:
```bash
git clone https://github.com/firdosht11/Synthetic-Humans-R1.git
cd Synthetic-Humans-R1
```

2. Create a virtual environment and install dependencies:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Copy the `.env.example` file to `.env` and fill in your API keys:
```bash
cp .env.example .env
# Edit the .env file with your API keys
```

## File Structure

The application consists of the following main components:

- `1_⌂_HOME.py`: Main Streamlit application entry point
- `pages/`: Directory containing all the application pages
- `modules/`: Core application modules with utilities and synthetic human functionality
- `synhumans/`: Directory for synthetic human profile data
- `assets/`: Images and other static assets

## Uploading Your Local Files

To upload all your local files to this repository, use the following commands:

```bash
# Add all files
git add .

# Commit changes
git commit -m "Add all project files"

# Push to GitHub
git push origin main
```

## Additional Resources

- The `requirements.txt` file includes all necessary dependencies
- The `.env.example` file shows the required environment variables
- The `README.md` file provides an overview of the application and its features

## Contact

For questions or issues, please contact the repository owner or create an issue on GitHub.