# SIH26012 — Project Execution Manual
**Team Winners | AI Cadastral Mapping Platform**

## Running the Dashboard

```bash
# Start static file server
python -m http.server 9090
# Open: http://localhost:9090/index.html
```

## Running the FastAPI Backend

```bash
pip install -r requirements.txt
python app.py
# API:   http://127.0.0.1:8000
# Docs:  http://127.0.0.1:8000/docs
```

## Key Endpoints

| Method | Path | Description |
|:---|:---|:---|
| GET | `/` | System health & metadata |
| GET | `/api/v1/pipeline/stats` | Live pipeline monitoring |
| POST | `/api/v1/imagery/analyze` | Submit drone tile for AI analysis |
| GET | `/api/v1/audit/logs` | Last 20 cryptographic audit records |
| POST | `/api/v1/action/dispatch` | Dispatch field survey team |
| GET | `/api/v1/team` | Team Winners metadata |

## Running Tests

```bash
pytest test_app.py -v
```

## Docker Deployment

```bash
docker-compose up --build
```
