FROM python:3.12-slim

WORKDIR /app

COPY . /app
RUN apt-get update && \
    apt-get install -y python3-venv && \
    apt-get install -r python3-pip && \
 
RUN python3 -m venv/venv
    
RUN /venv/bin/pip install --upgrade pip && \
    /venv/bin/pip install --no-cache-dir -r requirements.txt
ENV PATH="/venv/bin:$PATH"


ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
