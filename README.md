# 🚗 AutoHub Namibia

A modern 3D-inspired vehicle marketplace built with **Flet**, **FastAPI**, **PostgreSQL**, and **Cloudinary**. AutoHub Namibia connects vehicle buyers, private sellers, and dealerships through a fast, responsive, and visually engaging platform.

---

## 🌟 Features

### For Buyers
- Browse thousands of vehicle listings
- Advanced vehicle search and filtering
- Save favorite vehicles
- Compare vehicles side-by-side
- Contact dealers directly via WhatsApp
- View detailed vehicle specifications
- Explore featured and recently added vehicles

### For Private Sellers
- Create and manage listings
- Upload multiple vehicle images
- Track inquiries from potential buyers
- Edit and update listings anytime

### For Dealerships
- Dedicated dealership profiles
- Inventory management dashboard
- Vehicle performance analytics
- Lead and inquiry tracking
- Company branding and logo support

### Admin Features
- Manage users and dealerships
- Approve and moderate listings
- Platform analytics
- Spam and abuse management
- System monitoring

---

## 🛠 Tech Stack

### Frontend
- Flet (Python)

### Backend
- FastAPI

### Database
- PostgreSQL
- Supabase

### Image Storage
- Cloudinary

### Authentication
- JWT Authentication
- Role-based access control

### Deployment
- Vercel (Frontend)
- Railway / Render (Backend)
- Supabase Database

---

## 🎨 Design Philosophy

AutoHub Namibia is designed to provide a premium automotive experience with:

- 3D-inspired UI components
- Glassmorphism effects
- Smooth animations
- Dark modern theme
- Responsive mobile-first design
- Fast loading performance
- Luxury showroom aesthetics

---

## 📂 Project Structure

```bash
AutoHub-Namibia/
│
├── frontend/
│   ├── pages/
│   ├── components/
│   ├── layouts/
│   ├── assets/
│   └── app.py
│
├── backend/
│   ├── api/
│   ├── models/
│   ├── services/
│   ├── database/
│   ├── auth/
│   └── main.py
│
├── uploads/
│
├── docs/
│
├── tests/
│
├── requirements.txt
│
└── README.md
```

---

## 🚀 Getting Started

### Clone Repository

```bash
git clone https://github.com/yourusername/autohub-namibia.git

cd autohub-namibia
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

Windows:

```bash
venv\Scripts\activate
```

Linux / macOS:

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ⚙️ Environment Variables

Create a `.env` file:

```env
DATABASE_URL=
SUPABASE_URL=
SUPABASE_KEY=

CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=

SECRET_KEY=

JWT_ALGORITHM=HS256
```

---

## 🗄 Database Schema

### Users

| Field | Type |
|---------|---------|
| id | UUID |
| name | String |
| email | String |
| password_hash | String |
| role | String |

### Dealers

| Field | Type |
|---------|---------|
| id | UUID |
| company_name | String |
| logo | String |
| location | String |
| description | Text |

### Vehicles

| Field | Type |
|---------|---------|
| id | UUID |
| dealer_id | UUID |
| make | String |
| model | String |
| year | Integer |
| mileage | Integer |
| price | Decimal |
| fuel_type | String |
| transmission | String |
| description | Text |

### Vehicle Images

| Field | Type |
|---------|---------|
| id | UUID |
| vehicle_id | UUID |
| image_url | String |

### Favorites

| Field | Type |
|---------|---------|
| id | UUID |
| user_id | UUID |
| vehicle_id | UUID |

### Inquiries

| Field | Type |
|---------|---------|
| id | UUID |
| user_id | UUID |
| vehicle_id | UUID |
| message | Text |

---

## 🔑 API Endpoints

### Authentication

```http
POST /register
POST /login
POST /logout
```

### Vehicles

```http
GET /vehicles
GET /vehicles/{id}
POST /vehicles
PUT /vehicles/{id}
DELETE /vehicles/{id}
```

### Dealers

```http
GET /dealers
GET /dealers/{id}
POST /dealers
```

### Favorites

```http
POST /favorites
DELETE /favorites/{id}
GET /favorites
```

### Inquiries

```http
POST /inquiries
GET /inquiries
```

---

## 📱 Future Roadmap

### Version 1.0
- Vehicle listings
- Dealer dashboard
- Search functionality
- Favorites system
- WhatsApp integration

### Version 2.0
- Vehicle financing calculator
- AI-powered vehicle recommendations
- Vehicle comparison tool
- Featured dealership subscriptions

### Version 3.0
- Mobile app
- Vehicle valuation system
- AI chatbot assistant
- Vehicle inspection booking

### Version 4.0
- Insurance integration
- Loan pre-approval integration
- Regional expansion across Southern Africa

---

## 🔒 Security

- Password hashing
- JWT authentication
- Role-based permissions
- Secure API endpoints
- Input validation
- SQL injection protection

---

## 📈 Performance Goals

- Support 20,000+ vehicle listings
- Support 300,000+ optimized images
- Fast CDN image delivery
- Responsive search results
- Mobile-first experience

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License.

---

## 🇳🇦 Vision

AutoHub Namibia aims to become the leading digital automotive marketplace in Namibia by helping buyers find quality vehicles and enabling dealerships to showcase inventory through a modern, technology-driven platform.
