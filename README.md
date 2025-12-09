# HashTrack-Futuristic-AI-Powered-Hashtag-Trend-Analysis-Platform
Real-time social media analytics powered by Apache Spark, PySpark ML, and a 3D neon dashboard
# HashTrack — Futuristic 3D Dashboard (HashTrack)

This repository provides a futuristic HashTrack UI (dark neon theme, THREE.js 3D hashtag model)
and a Flask backend that loads a CSV and can trigger Spark jobs.

## Quickstart (dev)

1. Put your dataset at:
   /mnt/data/social_media_hashtag_trends_3000_rows.csv
   or set env var HASHTRACK_DATA_PATH.

2. Create venv & install:
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt

3. Start backend:
   python backend/app.py

4. Start websocket demo (optional):
   python ws_server.py

5. Open UI:
   http://localhost:5000

## Run Spark jobs
Ensure spark-submit is installed and on PATH.

Example:
curl -X POST http://localhost:5000/api/run_spark -H "Content-Type: application/json" -d '{"job":"trending"}'
