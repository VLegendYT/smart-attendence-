# Smart Attendance System

A startup-style full-stack IoT attendance platform built for final-year demonstrations, IEEE presentations, and portfolio showcases. The project combines a modern SaaS dashboard, Flask face-recognition APIs, Supabase-backed persistence, and ESP32-CAM device firmware.

## Stack

- Frontend: React, Vite, TailwindCSS, React Router, Recharts, Axios, Supabase Auth
- Backend: Flask, OpenCV, `face_recognition`, Supabase Python client, JWT verification
- Embedded: ESP32-CAM Arduino firmware, OLED status display, WiFi heartbeat + recognition calls
- Database: Supabase PostgreSQL with RLS, indexes, triggers, and sample seed rows

## Folder Structure
## Description
Added the attendance management feature.

## Changes Made
- Added attendance page
- Updated navigation
- Fixed UI issues

## Testing
Tested successfully in Chrome.

```text
project-root/
├── backend/
├── frontend/
├── embedded/
├── docs/
└── README.md
```

## Highlights

- Multi-page responsive admin dashboard with glassmorphism styling and dark/light mode
- Protected frontend routes powered by Supabase Auth
- Separate unauthenticated ESP32 API endpoints
- Face registration, face matching, and duplicate attendance prevention
- Dashboard KPIs, weekly analytics, recent activity, and device status cards
- Direct-to-Supabase SQL schema for rapid setup

## Quick Start

### Backend

```bash
pip install -r backend/requirements.txt
python backend/run.py
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

## Important Notes

- `face_recognition` requires native dependencies such as `dlib`; install tools appropriate for your OS before running it locally.
- Configure Supabase Auth JWT metadata so admins carry a `role` or `app_metadata.role` of `admin`.
- ESP32 endpoints intentionally bypass authentication as requested, so deploy them only behind trusted network boundaries or a secure gateway in production.

## Documentation

- [Architecture](docs/architecture.md)
- [API](docs/api.md)
- [Setup](docs/setup.md)
