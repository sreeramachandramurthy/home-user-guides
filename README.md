# Home User Guides

User Guides

## Documentation

[https://sreeramachandramurthy.github.io/home-user-guides/](https://sreeramachandramurthy.github.io/home-user-guides/ 'Home User Guides')

## Project Local Setup

### Prerequistes

* Install Python (Python 3)

```bash
sudo apt install python3
```

* Install PIP

```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
```

* Install Python Virtual Environment

```bash
sudo apt install python3-venv
sudo apt install python3.12-venv
```

### Setup Virtual Environment

* Navigate to working directory

```bash
cd home-user-guides/
```

* Create a Virtual Environment

```bash
python3 -m venv .venv
```

* Activate the Virtual Environment

```bash
source .venv/bin/activate
```

* Install Packages & Dependencies

```bash
python -m pip install -r requirements.txt
```

Alternatively you can install the latest packages and dependencies

* Install MkDocs

```bash
python -m pip install mkdocs
```

* Install MkDocs Material

```bash
python -m pip install mkdocs-material
```

* Freeze current State

```bash
pip freeze > requirements.txt
```

### Virtual Environment Usage

* Activate the Virtual Environment

```bash
source .venv/bin/activate
```

* Deactivate the Virtual Environment

```bash
deactivate
```

### Upgrade MkDocs & MkDocs Material

* Upgrade MkDocs & MkDocs Material

```bash
pip install --upgrade --force-reinstall mkdocs-material
```
