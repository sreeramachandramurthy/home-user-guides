# Home User Guides

User Guides

## Documentation

[https://sreeramachandramurthy.github.io/home-user-guides/](https://sreeramachandramurthy.github.io/home-user-guides/ 'Home User Guides')

## Project Local Setup

### Prerequistes

* Install Python (Python 3)  
  `apt install python3`
* Install PIP  
  `curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`

  `python3 get-pip.py`
* Install Python Virtual Environment  
  `apt install python3-venv`

### Setup Virtual Environment

* Navigate to working directory  
  `cd home-user-guides/`
* Create a Virtual Environment  
  `pyton3 -m venv .venv`
* Activate the Virtual Environment  
  `source .venv/bin/activate`
* Install Packages & Dependencies  
  `python -m pip install -r requirements.txt`

Alternatively you can install the latest packages and dependencies

* Install MkDocs  
  `python -m pip install mkdocs`
* Install MkDocs Material  
  `python -m pip install mkdocs-material`
* Freeze current State  
  `pip freeze > requirements.txt`

### Virtual Environment Usage

* Activate the Virtual Environment  
  `source .venv/bin/activate`
* Deactivate the Virtual Environment  
  `deactivate`

### Upgrade MkDocs

* Upgrade MkDocs & MkDocs Material  
  `pip install --upgrade --force-reinstall mkdocs-material`
