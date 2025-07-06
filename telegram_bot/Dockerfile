# Telegram Bot Dockerfile
FROM python:3.9-slim

WORKDIR /app

# Install aiogram
COPY ../aiogram/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY ../aiogram/ /app/

# Command to run the bot
CMD ["python", "bot/main.py"]
