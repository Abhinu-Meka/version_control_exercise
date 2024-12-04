# version_control_exercise

## Setup

Create a virtual environment (first time only):

```sh
conda create -n reports-env-2024 python=3.10
```

Activate the environment (whenever you come back to this project):

```sh
conda activate reports-env-2024
```

Install packages:

```sh
pip install -r requirements.txt
```
[Obtain an API Key](https://www.alphavantage.co/support/#api-key) from AlphaVantage.

Create a ".env" file and add contents like the following (using your own AlphaVantage API Key):

```sh
ALPHAVANTAGE_API_KEY="..."
```

Install packages for SendGrid:

```sh
pip install -r requirements.txt
```
Obtain an API Key from SendGrid and set Single Sender Address.

In the ".env" file, add contents like the following (using your own SendGrid API Key):

```sh
SENDGRID_API_KEY = "..."
SENDGRID_SENDER_ADDRESS = "..."
```

## Usage

Run the example script:

```sh
python app/my_script.py
```

Run the unemployment report:

```sh
#ALPHAVANTAGE_API_KEY="..." python app/unemployment.py

python -m app.unemployment
```

Run the stocks report:

```sh
python -m app.stock
```

Run the example email sending file:
```sh
python -m app.email_service
```

### web app

```sh
# Mac OS:
FLASK_APP=web_app flask run

# Windows OS:
# ... if `export` doesn't work for you, try `set` instead
# ... or set FLASK_APP variable via ".env" file
export FLASK_APP=web_app
flask run
```