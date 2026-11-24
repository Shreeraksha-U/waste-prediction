# Waste Generation Forecasting System (INNOVATE Hackathon)

Forecasts waste generated per city/area so municipalities can see hotspots and plan bin placement.
 
 
Qualified to last round 
 
## Structure
- Backend/forecaster.py - data loading, forecasting, hotspot ranking, bin recommendations
- Script/train.py - runs the pipeline, prints backtest metric
- UI/app.py - Streamlit dashboard
- data/waste.csv - put the Kaggle dataset here (not committed)

## Run
```bash
pip install -r requirements.txt
python Script/train.py --data data/waste.csv
streamlit run UI/app.py
```

Dataset: Kaggle, *Waste Management and Recycling in Indian Cities*.

## Database
```bash
python Script/seed_db.py --data data/waste.csv --reset   # creates data/waste.db
```
Tables: users, regions, waste_records, forecasts, bin_capacity.
The model script saves predictions with Backend.db.save_forecasts(conn, df, model_name).

<img width="1011" height="519" alt="7" src="https://github.com/user-attachments/assets/029b158a-9870-4d44-b069-24e8b1d15893" />
<img width="846" height="598" alt="6" src="https://github.com/user-attachments/assets/b5df394f-0cf3-46b0-9f4a-1d9897f01f8c" />
<img width="826" height="547" alt="5" src="https://github.com/user-attachments/assets/49b758bc-ed7d-4e62-be6d-53a8fc456311" />
<img width="888" height="584" alt="4" src="https://github.com/user-attachments/assets/15b64f44-a126-4790-b248-2a44664ef5f2" />
<img width="991" height="575" alt="3" src="https://github.com/user-attachments/assets/7d48be4f-a3ea-4088-b8a8-8b53398539f6" />
<img width="945" height="595" alt="2" src="https://github.com/user-attachments/assets/e729ba30-b03f-42cb-a4f1-9db40e32bed5" />
<img width="691" height="479" alt="01" src="https://github.com/user-attachments/assets/b3e49d21-225d-46f1-a111-e7ffd0e74230" />


