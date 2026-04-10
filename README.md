# TransferIQ — Web App

## Local Run

```bash
pip install -r requirements.txt
python app.py
# Open: http://localhost:5000
```

## Deploy on Render / Railway / Heroku

### Render
1. New Web Service → connect repo
2. Build Command: `pip install -r requirements.txt`
3. Start Command: `gunicorn app:app`
4. Done!

### Railway
1. New Project → Deploy from GitHub
2. Auto-detects Procfile → deploys automatically

### Heroku
```bash
heroku create transferiq-app
git push heroku main
```

## Structure
```
TransferIQ_deploy/
├── app.py                        ← Flask backend
├── templates/
│   └── index.html                ← Frontend
├── models/
│   └── best_model_v2.pkl         ← Ridge Regression model
├── data/
│   └── featured_dataset_final.csv ← Player data
├── requirements.txt
├── Procfile                      ← For cloud deploy
└── README.md
```
