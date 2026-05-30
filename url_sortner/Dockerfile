FROM python:3.11

WORKDIR /code

# Copy only requirements first for better layer caching
COPY url_sortner/requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

# Copy application code from the repository subfolder
COPY url_sortner/ .

EXPOSE 8000

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
