FROM python:3.10

LABEL authors="adama.fofana"
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

ARG DATABASE_URL
ENV DATABASE_URL=$DATABASE_URL

EXPOSE 8000
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
