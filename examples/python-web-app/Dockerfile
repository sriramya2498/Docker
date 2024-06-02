FROM python:3.12-slim

WORKDIR /app

COPY . /app
RUN apt-get update && \
    apt-get install -y python3-venv python3-pip && \
    rm-rf /var/lib/apt/lists/*
 
RUN python3 -m venv/venv

ENV PATH="/venv/bin:$PATH"
    
RUN pip install --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt

CMD ["python" "manage.py", "runserver", "0.0.0.0:8000"]
