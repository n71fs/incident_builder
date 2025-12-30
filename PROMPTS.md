# Codex Prompts

Use the prompts below when working with Codex. Always reference SPEC.md.

---

## Worker Implementation

"You are implementing the worker for the project described in SPEC.md.

Write a Python module called `worker.py` that:
- accepts a job payload (JSON)
- queries a PostgreSQL database for audio clips in a time range and talkgroup list
- builds an audio timeline per talkgroup
- supports two playback modes: back_to_back and real_time
- generates M4A files using ffmpeg
- uploads outputs to DigitalOcean Spaces (S3 compatible)
- writes a manifest.json

Assume:
- ffmpeg is installed
- boto3 is available
- database credentials are provided via environment variables

Do not include the web API.
Focus only on the worker logic."

---

## ffmpeg Review

"Review the ffmpeg usage in the worker.
Ensure silence duration is accurate, timestamps are preserved, and AAC encoding is 96 kbps.
Update the code if needed."

---

## API Implementation

"Using SPEC.md, implement a REST API with:
- POST /api/jobs
- GET /api/jobs/{job_id}
- GET /api/jobs/{job_id}/download

Enforce limits defined in SPEC.md.
Use FastAPI or Django REST Framework."

---

## Job Queue

"Implement a Redis-backed job queue to execute the worker asynchronously.
Include job status tracking and error handling."

You will copy/paste from this file constantly.
