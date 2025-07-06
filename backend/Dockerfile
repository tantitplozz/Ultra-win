# Backend Dockerfile (FastAPI)
FROM python:3.9-slim

WORKDIR /app

# Install dependencies
COPY ../fastapi/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY ../fastapi/ /app/

# Copy source code from cloned repos
COPY ../MetaGPT /app/MetaGPT
COPY ../langgraph /app/langgraph
COPY ../playwright-python /app/playwright-python
COPY ../playwright_stealth /app/playwright_stealth
COPY ../gologin /app/gologin

# Expose port and run the application
EXPOSE 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
