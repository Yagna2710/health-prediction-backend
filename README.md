# Health Prediction Backend

Flask API for health risk prediction and insurance recommendations.

## Deployment on Render

1. Push your code to GitHub
2. Go to [Render Dashboard](https://dashboard.render.com/)
3. Click "New +" and select "Web Service"
4. Connect your GitHub repository
5. Configure:
   - **Root Directory**: `backend`
   - **Environment**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `gunicorn app:app`
6. Add environment variable:
   - `CORS_ORIGINS`: Your Vercel frontend URL (e.g., `https://your-app.vercel.app`)
7. Click "Create Web Service"

## Local Development

```bash
cd backend
pip install -r requirements.txt
python app.py
```

The server will run on http://localhost:5000

## Environment Variables

Create a `.env` file in the backend directory:

```
PORT=5000
FLASK_ENV=development
CORS_ORIGINS=http://localhost:5173
```
