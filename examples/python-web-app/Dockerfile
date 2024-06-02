FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt/app
COPY devops /app
RUN apt-get update && \
    apt-get install -y python3-venv && \
    apt-get install -r python3-pip && \
    python3 -m venv/venv
    /venv/bin/pip install --upgrade pip && \
    /venv/bin/pip install --no-cache-dir -r requirements.txt
    cd devops
ENV PATH="/venv/bin:$PATH"


ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
