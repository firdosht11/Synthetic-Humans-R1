# Directory Structure

This document outlines the structure of the Synthetic Humans R1 repository. It's meant to help you organize your local files when setting up the repository.

## Main Structure

```
Synthetic-Humans-R1/
│
├── 1_⌂_HOME.py                     # Main entry point for the Streamlit app
├── .env                           # Environment variables (not in repo - create from .env.example)
├── .env.example                   # Example environment variables file
├── requirements.txt               # Python dependencies
├── README.md                      # Project overview
│
├── pages/                         # Streamlit pages
│   ├── 1_HUMANS.py
│   ├── 2_Customers.py
│   ├── 3_↳_Segments.py
│   ├── 4_Collaborators.py
│   ├── 5_↳_Roles.py
│   ├── 7_EMPATHY.py
│   ├── 8_Interview.py
│   ├── 9_Qual_Study.py            # Qualitative Study page
│   ├── 10_Quant_Study.py
│   ├── 12_INNOVATION.py
│   ├── 13_Ideation.py
│   ├── 15_Collaboration.py
│   ├── 17_VALIDATION.py
│   ├── 18_Describe_1.py
│   ├── 19_Describe_2.py
│   ├── 21_Show.py
│   ├── 25_Settings.py
│   └── 26_Help.py
│
├── modules/                        # Core modules
│   ├── utils.py                   # Utility functions
│   ├── apikeylist.py              # API key definitions
│   │
│   └── syn/                       # Synthetic human modules
│       ├── syncoder.py            # Encryption/decryption for synthetic humans
│       ├── synhuman.py            # Synthetic human class
│       ├── synllm.py              # LLM integration for synthetic humans
│       ├── synparser.py           # Parser for synthetic human data
│       ├── synprompts.py          # Prompts for synthetic humans
│       └── synuistyle.py          # UI styling for synthetic humans
│
├── synhumans/                      # Synthetic human data
│   ├── qual/                      # Qualitative study synthetic humans
│   │   ├── general/               # General segment
│   │   ├── nike/                  # Nike segment
│   │   ├── neom/                  # Neom segment
│   │   ├── disney/                # Disney segment
│   │   └── plume/                 # Plume segment
│   │
│   └── interviews/                # Interview data
│
├── assets/                         # Static assets
│   └── images/                    # Images for the app
│
└── data/                           # Data files
```

## Note on Empty Directories

When cloning this repository, you might need to create some empty directories that Git doesn't track. Make sure to create these directories if they don't exist:

- `synhumans/qual/general/`
- `synhumans/qual/nike/`
- `synhumans/qual/neom/`
- `synhumans/qual/disney/`
- `synhumans/qual/plume/`
- `synhumans/interviews/`
- `assets/images/`
- `data/`

You can do this with the following command:

```bash
mkdir -p synhumans/qual/{general,nike,neom,disney,plume} synhumans/interviews assets/images data
```