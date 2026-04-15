# 💰 Dr. Seba Client - Commission Revenue Forecasting

> *AI-powered commission revenue forecasting system for healthcare professionals*

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-green.svg)](https://fastapi.tiangolo.com/)
[![Django](https://img.shields.io/badge/Django-4.0+-darkgreen.svg)](https://www.djangoproject.com/)
[![CatBoost](https://img.shields.io/badge/CatBoost-1.1+-orange.svg)](https://catboost.ai/)

---

## 📋 Overview

Dr. Seba Client হল একটি intelligent revenue forecasting system যা healthcare professionals দের ভবিষ্যৎ commission revenue আগাম জানিয়ে দেয়। এটি গড়ে উঠেছে CatBoost মেশিন লার্নিং মডেল এবং ডেটা বিশ্লেষণ এর উপর।

### 🎯 মূল বৈশিষ্ট্য
- ✅ **Single-day Prediction**: পরের দিনের revenue পূর্বাভাস
- ✅ **Multi-day Forecast**: ৩৬৫ দিন পর্যন্ত বিস্তারিত পূর্বাভাস  
- ✅ **Advanced Analytics**: দৈনিক, সাপ্তাহিক, এবং মাসিক বিশ্লেষণ
- ✅ **Real-time Integration**: FastAPI backend সহ তাৎক্ষণিক ফলাফল
- ✅ **User-friendly Interface**: Django ভিত্তিক সুন্দর UI
- ✅ **Statistical Insights**: Min, Max, Mean, Std Dev বিশ্লেষণ

### 🏗️ আর্কিটেকচার
এই প্রজেক্টটি **মাইক্রোসার্ভিসেস** আর্কিটেকচার অনুসরণ করে:
- **Backend API** (port 8000): FastAPI + CatBoost + Machine Learning
- **Frontend UI** (port 8001): Django + Bootstrap + Interactive Forms

---

## 📁 প্রজেক্ট স্ট্রাকচার

```
dr-seba-client/
│
├─ 📦 api/                           # FastAPI Backend
│  ├─ main.py                        # API endpoints & Uvicorn server
│  ├─ models.py                      # Pydantic request/response models
│  ├─ config.py                      # Configuration & constants
│  └─ requirements.txt               # API dependencies
│
├─ 🎨 ui/                            # Django Frontend  
│  ├─ forecaster/                    # Main Django app
│  │  ├─ views.py                    # Business logic & API integration
│  │  ├─ urls.py                     # URL routing
│  │  └─ migrations/                 # Database migrations
│  ├─ forecasting_ui/                # Django project configuration
│  │  ├─ settings.py                 # Django settings
│  │  ├─ urls.py                     # Project-level routing
│  │  └─ static/                     # CSS & static files
│  ├─ templates/                     # HTML templates
│  ├─ manage.py                      # Django management script
│  ├─ db.sqlite3                     # SQLite database
│  └─ requirements.txt               # UI dependencies
│
├─ 🤖 models/                        # Pre-trained ML models
│  └─ commission_revenue_forecasting_model.pkl
│
├─ 📊 data/                          # Dataset & training data
├─ 🧪 tests/                         # Unit tests
├─ 🔐 .gitignore                     # Git ignore file
├─ 📄 README.md                      # This file
├─ 🚀 RUN_TEAM_ACCESS.ps1            # Auto-start script (PowerShell)
├─ 🛑 STOP_SERVERS.ps1               # Auto-stop script
└─ .venv/                            # Virtual environment (excluded from repo)

```

---

## 🚀 দ্রুত শুরু করুন

### প্রয়োজনীয়তা
- **Python 3.8+**
- **pip** (Python package manager)
- **Git**
- **Windows/macOS/Linux**

### ইনস্টলেশন

#### ১. রিপোজিটরি ক্লোন করুন
```bash
git clone https://github.com/yourusername/dr-seba-client.git
cd dr-seba-client
```

#### ২. ভার্চুয়াল এনভায়রনমেন্ট তৈরি করুন
```bash
# Windows
python -m venv .venv
.venv\Scripts\Activate.ps1

# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate
```

#### ३. ডিপেন্ডেন্সি ইনস্টল করুন
```bash
# API dependencies
cd api
pip install -r requirements.txt
cd ..

# UI dependencies
cd ui
pip install -r requirements.txt
cd ..
```

---

## ▶️ অ্যাপ্লিকেশন চালু করুন

### অপশন ১: স্বয়ংক্রিয় (সুপারিশকৃত)
```bash
# Windows PowerShell
.\RUN_TEAM_ACCESS.ps1

# Windows Command Prompt
RUN_TEAM_ACCESS.bat
```

### অপশন ২: ম্যানুয়াল (সব প্ল্যাটফর্ম)

**টার্মিনাল ১ - API সার্ভার:**
```bash
cd api
python main.py
# API চলবে: http://localhost:8000
```

**টার্মিনাল ২ - Django UI:**
```bash
cd ui
python manage.py runserver 8001 --noreload
# UI চলবে: http://localhost:8001
```

### 📍 অ্যাক্সেস পয়েন্ট
| সেবা | URL | উদ্দেশ্য |
|------|-----|---------|
| 🎨 **ইউজার ইন্টারফেস** | http://localhost:8001 | ফোরকাস্টিং ফর্ম এবং ফলাফল |
| 📚 **API ডকুমেন্টেশন** | http://localhost:8000/docs | Interactive Swagger UI |
| 💚 **health চেক** | http://localhost:8000/health | API স্ট্যাটাস ভেরিফিকেশন |
| 🔧 **ReDoc** | http://localhost:8000/redoc | Alternative API docs |


## � অ্যাপ্লিকেশন থামান

```bash
# Windows PowerShell
.\STOP_SERVERS.ps1

# Windows Command Prompt
STOP_SERVERS.bat

# Manual (সব প্ল্যাটফর্ম)
# প্রতিটি টার্মিনালে Ctrl+C চাপুন
```

---

## 📊 API এন্ডপয়েন্টগুলি

### 🔍 `/predict` - একদিনের পূর্বাভাস
```bash
POST /predict
```
**Response:** একদিনের commission revenue পূর্বাভাস

### 📈 `/forecast?days=30` - মাল্টি-ডে বিশ্লেষণ
```bash
POST /forecast?days=30
```
**Response:** ৩০ দিনের বিস্তারিত ফোরকাস্ট + পরিসংখ্যান

### ❤️ `/health` - সেবা স্বাস্থ্য
```bash
GET /health
```
**Response:** API স্ট্যাটাস এবং মডেল তথ্য

---

## 🧪 পরীক্ষা চালান

```bash
cd tests
python -m pytest -v
```

---

## 📚 প্রযুক্তি স্ট্যাক

| উপাদান | প্যাকেজ | সংস্করণ |
|--------|---------|---------|
| **Backend Framework** | FastAPI | 0.104+ |
| **Web Server** | Uvicorn | 0.24+ |
| **Frontend Framework** | Django | 4.0+ |
| **Machine Learning** | CatBoost | 1.1+ |
| **Data Processing** | Pandas | 1.5+ |
| **Numerical Computing** | NumPy | 1.23+ |
| **Data Validation** | Pydantic | 2.0+ |
| **Database** | SQLite | Cross-platform |
| **HTTP Client** | Requests | 2.31+ |

---

## 📝 পরিবেশ পরিবর্তনশীল

Optional `.env` ফাইল:
```env
DEBUG=True
DJANGO_SECRET_KEY=your-secret-key-here
API_BASE_URL=http://localhost:8000
ALLOWED_HOSTS=localhost,127.0.0.1
```

---

## 🐛 সাধারণ সমস্যা এবং সমাধান

| সমস্যা | কারণ | সমাধান |
|--------|------|--------|
| Cannot connect to API | API সার্ভার চলছে না | `python main.py` কমান্ড চালান |
| Port 8000 already in use | অন্য অ্যাপ্লিকেশন ব্যবহার করছে | `netstat -ano \| findstr :8000` দিয়ে চেক করুন |
| Port 8001 already in use | অন্য Django চলছে | ভিন্ন পোর্ট ব্যবহার করুন: `python manage.py runserver 8002` |
| Module not found | ডিপেন্ডেন্সি সঠিক নয় | `pip install -r requirements.txt --force-reinstall` চালান |
| Model load failed | মডেল ফাইল গায়েব | `models/` ফোল্ডার যাচাই করুন |

---

## 📧 যোগাযোগ এবং সহায়তা

| ভূমিকা | নাম | যোগাযোগ |
|--------|-----|---------|
| 👨‍🏫 **Mentor** | Nusrat Jahan | 📧 nusratadiba88@gmail.com |
| 🏢 **Client** | Dr. Seba | - |

> যেকোনো সমস্যা বা প্রশ্নের জন্য mentor এর সাথে যোগাযোগ করুন

---

## 📋 ডেভেলপমেন্ট চেকলিস্ট

- [x] FastAPI Backend ডেভেলপমেন্ট
- [x] Django Frontend তৈরি
- [x] CatBoost ML মডেল ইন্টিগ্রেশন
- [x] API-UI সংযোগ
- [x] ডাটাবেস সেটআপ (SQLite)
- [x] GitHub রিপোজিটরি তৈরি
- [x] Professional Documentation
- [ ] Comprehensive Unit Tests
- [ ] Docker Containerization
- [ ] CI/CD Pipeline (GitHub Actions)
- [ ] Deployment to Production

---

## 📊 প্রজেক্ট পরিসংখ্যান

```
Total Files:              30+
Lines of Code:            2000+
API Endpoints:            3
Database Models:          2
Trained ML Models:        1
Test Coverage:            50%+
Supported Districts:      8
Specializations:          10
Max Forecast Days:        365
```

---

## 📄 লাইসেন্স

এই প্রজেক্টটি **Dr. Seba Client** এর জন্য মালিকানাধীন এবং গোপনীয়।  
অননুমোদিত কপি, পরিবর্তন বা বিতরণ সম্পূর্ণভাবে নিষিদ্ধ।

---

## 🎯 ভবিষ্যৎ রোডম্যাপ

- [ ] Mobile app (React Native)
- [ ] Advanced analytics dashboard
- [ ] Real-time notifications
- [ ] Multi-language support
- [ ] Cloud deployment (AWS/Azure)
- [ ] API rate limiting
- [ ] User authentication system
- [ ] Export reports (PDF/Excel)

---

**Project Status:** ✅ Active Development  
**Last Updated:** এপ্রিল ২০২৬  
**Maintained by:** Dr. Seba Development Team  
**GitHub:** https://github.com/yourusername/dr-seba-client

---

*Built with ❤️ for Dr. Seba Client*
