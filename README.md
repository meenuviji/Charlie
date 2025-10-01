# Charlie — MBTA Chatbot
_Not affiliated with the MBTA. For educational purposes._

## 1. Introduction
The Massachusetts Bay Transportation Authority (MBTA) provides a wide range of services such as subways, buses, commuter rail, and ferries that millions of riders rely on daily. Currently, riders often need to use multiple sources such as the MBTA website, third-party apps, or station boards to find schedules, track delays, check vehicle locations, or view service alerts. This fragmented experience can be inconvenient, especially during peak hours or unexpected disruptions.

This project proposes building a conversational chatbot that centralizes MBTA transit information into a single, user-friendly interface. Using the MBTA V3 API (api-v3.mbta.com) and GTFS-Realtime feeds, the chatbot will allow riders to ask natural language questions such as “When is the next Red Line train to Alewife?”, “Why is the Green Line delayed?”, or “Where is my bus right now?” and receive real-time, accurate responses. Beyond schedules and predictions, the chatbot will also provide details on routes, stops, fares, service advisories, and delay causes.

By offering a natural and accessible way to interact with MBTA data, this solution aims to simplify the rider experience, reduce confusion, and improve access to critical transit updates in real time.

---

## 2. Features (MVP)
- Natural-language queries for next arrivals, delays, and vehicle locations
- Real-time schedules/predictions via MBTA V3 REST API
- Service alerts and (when available) delay reasons via GTFS-Realtime/Alerts
- Simple REST API (FastAPI) you can call from any chat UI

## 3. Architecture
```
User → Chat UI → Backend (FastAPI)
                     ├─ NLU (rule-based v1)
                     ├─ Resolver (intent → MBTA endpoint)
                     └─ MBTA Client (HTTP to api-v3.mbta.com + GTFS-RT)
```
- Backend: FastAPI + httpx
- Optional: Redis for short-term caching

## 4. License
MIT License — see `LICENSE`.

## 5. Disclaimer
This project is **not affiliated with** or endorsed by the Massachusetts Bay Transportation Authority (MBTA). All MBTA data are accessed from publicly available APIs and feeds.
