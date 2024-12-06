# Evry-Bot-z
Masih dalam perkembangan
name: Bot Automation

on:
  push:
    branches:
      - main 
  pull_request:
    branches:
      - main 

jobs:
  run-bot:
    runs-on: ubuntu-latest  

    steps:
     Checkout kode dari repositori
      - name: Checkout code
        uses: actions/checkout@v2  

      - name: Set up Python
        uses: actions/setup-python@v2
        with:
          python-version: '3.x' 

      - name: Install dependencies
        run: |
          pip install -r requirements.txt 

      - name: Run bot script
        run: |
          python bot.py  

print("Bot is running successfully!")

requests
flask
