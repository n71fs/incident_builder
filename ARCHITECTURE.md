# Architecture Overview

This project is intentionally split into the following components:

1. Web API
   - Accepts job requests
   - Validates limits
   - Exposes job status and downloads

2. Job Queue
   - Manages asynchronous processing
   - Limits concurrency
   - Tracks job lifecycle

3. Worker
   - Performs audio processing
   - Uses ffmpeg for M4A generation
   - Streams audio from object storage
   - Uploads results back to object storage

The worker MUST be able to run independently of the web API.

No real-time audio streaming is required.
No frontend framework is assumed at this stage.

This prevents Codex from:
	•	merging API + worker
	•	inventing WebSockets
	•	trying to stream audio live
