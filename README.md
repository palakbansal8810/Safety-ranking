# Safety Index Prediction API

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
## Usage

1. Start the Flask server:
   ```bash
   python app.py
   ```

2. Send a POST request to the `/predict` endpoint with the following JSON payload:
   ```json
   {
       "latitude": 28.7041,
       "longitude": 77.1025
   }
   ```

   ### Example usage:
   Using `curl`:
   ```bash
   curl -X POST http://127.0.0.1:5000/predict \
        -H "Content-Type: application/json" \
        -d '{"latitude": 28.7041, "longitude": 77.1025}'
   ```

3. Example response:
   ```json
   {
       "district": "North Delhi",
       "state": "Delhi",
       "year": 2025,
       "safety_index": 0.78
   }
   ```

## File Structure
```
.
├── app.py                          # Main Flask app
├── rating.py                       # Helper functions for prediction
├── model.pkl                       # Trained ML model
├── dataset/    
│   ├── district_mapping.csv        # Encoded district data
│   ├── state_mapping.csv           # Encoded state data
│   ├── district-wise-data.csv      # Raw dataset
├── requirements.txt                # List of dependencies
├── README.md                       # Documentation
```
