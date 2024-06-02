FROM python:3.12-slim

WORKDIR /app

COPY . /app
RUN apt-get update && \
    apt-get install -y python3-venv python3-pip && \
    rm-rf /var/lib/apt/lists/*
 
RUN python3 -m venv/venv

ENV PATH="/venv/bin:$PATH"
    
RUN /venv/bin/pip install --upgrade pip && \
    /venv/bin/pip install --no-cache-dir -r requirements.txt

CMD ["/venv/bin/python" "manage.py", "runserver", "0.0.0.0:8000"]
