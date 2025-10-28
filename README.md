# Charlie — MBTA Chatbot

**Charlie** is an interactive chatbot built to provide real-time MBTA (Massachusetts Bay Transportation Authority) transit information such as train arrivals, departures, and route details.  
This project demonstrates the integration of API-driven data pipelines with a conversational interface, showcasing a blend of **data engineering**, **MLOps**, and **natural language processing** concepts.

---

## Project Overview
The goal of this project is to develop a chatbot that:
- Fetches **live MBTA data** (train, route, and schedule details) using the official MBTA API  
- Processes and structures data through a **Python-based data pipeline**
- Delivers real-time responses to user queries such as:
  - “When is the next Orange Line train at Ruggles?”
  - “Show me the upcoming Green Line departures.”
- Integrates with a chatbot front end for conversational interaction

---

## Key Components
- **API Integration:** MBTA v3 API for live transit data  
- **Data Processing:** Python (requests, pandas) for ETL and formatting  
- **Chatbot Interface:** Python/Flask-based conversational layer  
- **Logging & Scheduling:** Airflow (for scheduled API pulls)  
- **Containerization:** Docker Compose setup for reproducible environments  

---

## Expected Output
- Real-time transit information responses
- JSON-formatted outputs for API queries
- Interactive chatbot UI that responds to user input
- Logged datasets for historical analysis of MBTA performance

---


---

## Future Enhancements
- Add natural language understanding (NLU) to interpret complex queries  
- Integrate with predictive models for delay forecasting  
- Deploy chatbot as a Streamlit or web-based application  

---

**Note:**  
This project is not affiliated with the MBTA. It is developed purely for educational and research purposes.
