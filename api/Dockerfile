FROM python:3.13-slim

WORKDIR /hoogle-drive

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV PYTHONPATH="${PYTHONPATH}:/hoogle-drive"

CMD ["uvicorn", "api.src.main:app", "--host", "0.0.0.0", "--port", "8080"]
