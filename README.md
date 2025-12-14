# 🛒 Secure Product Management System (Backend)

A secure **Product Management System backend** built using **FastAPI**, **PostgreSQL**, and **JWT authentication**. The system demonstrates **authentication, authorization, and protected CRUD operations** on products, following industry-standard backend practices.

This project is suitable as a **final-year academic project** or **backend portfolio project**, focusing on security and clean architecture rather than UI.

---

## 🚀 Features

### 🔐 Authentication & Security

* JWT-based authentication (HTTP Bearer)
* Secure password hashing using `bcrypt`
* Environment-based configuration using `.env`
* Protected API routes

### 👥 User Management

* User registration
* User login with JWT token issuance
* Authenticated access to protected endpoints

### 📦 Product Management

* Add new products
* View all products
* View product by ID
* Update product details
* Delete products

> ⚠️ Only authenticated users can create, update, or delete products

---

## 🛠️ Tech Stack

* **Backend Framework:** FastAPI
* **Database:** PostgreSQL
* **ORM:** SQLAlchemy
* **Authentication:** JWT (HTTP Bearer)
* **Password Hashing:** Passlib (bcrypt)
* **Environment Management:** python-dotenv
* **API Testing:** Swagger UI

---

## 📂 Project Structure

```
project/
│
├── main.py          # API routes
├── database.py      # Database connection
├── models.py        # SQLAlchemy models
├── schemas.py       # Pydantic schemas
├── security.py      # Password hashing & verification
├── jwt_utils.py     # JWT creation & verification
├── .env.example     # Environment variable template
├── .gitignore
└── README.md
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2️⃣ Create virtual environment

```bash
python -m venv myenv
myenv\\Scripts\\activate  # Windows
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Configure environment variables

Create a `.env` file in the project root:

```env
DATABASE_URL=postgresql://<user>:<password>@localhost:5432/<db_name>
SECRET_KEY=<your_generated_secret_key>
```

> ⚠️ Never commit `.env` to GitHub

---

## ▶️ Run the application

```bash
uvicorn main:app --reload
```

Open browser:

```
http://127.0.0.1:8000/docs
```

---

## 🔑 Authentication Flow

1. **Register user** (`/register`)
2. **Login user** (`/login`) → receive JWT token
3. Use token in **Authorization header**:

   ```
   Authorization: Bearer <token>
   ```
4. Access protected product APIs

---

## 🧪 Testing

* Swagger UI available at `/docs`
* Accessing protected routes without token returns `401`
* JWT verification enforced on each request

---

## 🎓 Academic Relevance

This project demonstrates:

* Secure backend API design
* JWT-based authentication
* Route-level authorization
* Database integration with ORM


---

## 🔮 Future Enhancements

* Role-based access (Admin/User)
* Product categories
* Pagination & search
* Streamlit or React frontend

---

## 👨‍💻 Author

**Mayank Bisht**

---

## 📄 License

This project is for academic and learning purposes only.
