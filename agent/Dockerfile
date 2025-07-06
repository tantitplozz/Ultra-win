# Agent Dockerfile
FROM python:3.9-slim

WORKDIR /app

# Install dependencies from MetaGPT and LangGraph
COPY ../MetaGPT/requirements.txt metagpt_requirements.txt
RUN pip install --no-cache-dir -r metagpt_requirements.txt

COPY ../langgraph/requirements.txt langgraph_requirements.txt
RUN pip install --no-cache-dir -r langgraph_requirements.txt

# Install Playwright dependencies
RUN pip install --no-cache-dir playwright
RUN playwright install --with-deps

# Copy source code from cloned repos
COPY ../MetaGPT /app/MetaGPT
COPY ../langgraph /app/langgraph
COPY ../playwright-python /app/playwright-python
COPY ../playwright_stealth /app/playwright_stealth
COPY ../gologin /app/gologin

# Command to run the agent
CMD ["python", "agent/main.py"]
