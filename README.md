# GPS Toll-Based System Simulation using Python & Streamlit

This project is a **web-based simulation** of a GPS toll system built with **Streamlit**.  
Users can:

- Enter a start and destination address  
- Visualize the route on an interactive map  
- Automatically calculate distance and toll  
- Store each trip in a database and view transaction history with charts   

---

## 🚀 Features

- **Get Started Screen** with welcome title and image  
- **Email capture** before entering the simulation  
- **User registration** via username (stored in SQLite DB)  
- **Geocoding of addresses** to latitude/longitude using Geopy  
- **Distance calculation** between two locations (km)  
- **Toll calculation** based on distance (base rate: `$0.1` per km)   
- **Interactive map** using Folium (start, end markers + route line)  
- **Transaction history** with:
  - Line chart of toll over time (Plotly)
  - Detailed transaction table (pandas + SQLite)   

---

## 🧱 Tech Stack

- **Python**
- **Streamlit** – Web UI framework  
- **Folium** + **streamlit-folium** – Interactive map display  
- **Geopy** – Geocoding and distance calculation  
- **Pandas** – Data handling for transaction history  
- **SQLite3** – Lightweight database for users & transactions  
- **Plotly** – Interactive charts (toll history)  
- **Pillow (PIL)** – Image handling for the welcome screen   

---

## 📁 Project Structure

```text
.
├── app.py                 # Main Streamlit application (UI + logic)
├── database.py            # Reusable DB helper functions (optional import) 
├── toll_calculator.py     # Simple toll calculation function
├── requirements.txt       # Python dependencies
└── Presentation(GPS).pptx # Project presentation / documentation

## Requirements
- Python 3.8+
- Packages: `streamlit`, `folium`, `streamlit-folium`, `pandas`, `numpy`,
  `geopy`, `plotly`, `pillow`, `sqlite3` (standard library)

## Setup
```bash
python -m venv venv
venv\Scripts\activate        # Windows
# or: source venv/bin/activate  # macOS/Linux

pip install -r requirements.txt
pip install streamlit plotly pillow