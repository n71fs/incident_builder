# Incident Audio Builder

Incident Audio Builder is a web-based tool for compiling archived radio traffic into playable incident audio files.

Users can select a time range and one or more talkgroups, choose between real-time playback or back-to-back audio, and generate M4A files directly from recordings stored in object storage. Jobs are processed asynchronously and delivered via secure download links.

## Status

🚧 Early development — core worker and API scaffolding in progress.

## High-Level Features

- Compile radio traffic into M4A files
- Real-time or gapless playback
- Batch processing per talkgroup
- Asynchronous job execution
- DigitalOcean Spaces (S3-compatible) storage

## Technology (planned)

- Python
- ffmpeg
- PostgreSQL
- Redis (job queue)
- DigitalOcean Spaces

See `SPEC.md` for full technical details.
