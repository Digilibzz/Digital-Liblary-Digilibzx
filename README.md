
<div align="center">

<h1>📚 Digilibzx - Digital Library Management System</h1>

![Digilibz Banner](https://img.shields.io/badge/Digilibz-Digital%20Library-blue?style=for-the-badge)
  ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
  ![Next.js](https://img.shields.io/badge/Next.js-black?style=for-the-badge&logo=next.js&logoColor=white)
  ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
  ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

**Digilibz** is a comprehensive and modern full-stack digital library management solution, developed by integrating robust **Java Spring Boot** technology on the backend and responsive **Next.js** on the frontend to deliver a seamless and fast user experience. Specifically designed to transform library operations in academic or public environments into an efficient digital ecosystem, this system not only simplifies core circulation processes such as automated book borrowing and returning but also enriches user interaction through review features, real-time notifications, and AI-based summaries. It also equips administrators with an analytical statistics dashboard for inventory management and library activity monitoring that is transparent, structured, and measurable within a single unified platform.

</div>

<br>

## Key Features

### 👤 User

* **Smart Search:** Search for books by title, category, or author.
* **Self-Service Circulation:** Perform borrowing requests and view estimated return dates.
* **Transaction History:** Monitor borrowing status (Pending, Borrowed, Returned, Overdue).
* **Review System:** Provide reviews and ratings for read books.
* **Real-time Notifications:** Receive updates on borrowing status.
* **AI Features:** Automatic book summaries (AI Summarize).

### 🛠 Admin

* **Statistics Dashboard:** Visualize borrowing data, popular books, and user activity.
* **Book Management:** Add, edit, and delete book data (including cover uploads).
* **User Management:** Manage user accounts (Admins, Lecturers, Students).
* **Borrowing Approval:** Approve or reject book borrowing requests.
* **Return Management:** Process book returns and handle late fines.

---

<br>

## 🛠️ Tech Stack

### Backend

* **Framework:** Java Spring Boot 3.x
* **Language:** Java 17+
* **Database:** MySQL
* **Security:** Spring Security & JWT Authentication
* **Build Tool:** Maven

### Frontend

* **Framework:** Next.js 14/15 (App Router)
* **Language:** TypeScript
* **Styling:** Tailwind CSS & Shadcn UI
* **State Management:** React Hooks
* **Package Manager:** pnpm / npm

---

<br>

## 📂 Project Structure

```text
root/
├── backend/            # Backend Source Code (Spring Boot)
│   ├── src/main/java   # Controllers, Services, Repositories, Models
│   └── src/main/resources
│       └── db/         # SQL Backup (backup.sql)
├── frontend/           # Frontend Source Code (Next.js)
│   ├── app/            # Pages & Routing
│   ├── components/     # Reusable UI Components
│   └── lib/            # API Helper Functions
└── document/           # Project Documentation (API Docs, ERD, SRS)

```

---

<br>

## ⚙️ Installation & Setup Guide

Follow these steps to run the project locally on your machine.

### 1. Database Preparation

1. Ensure **MySQL** is running.
2. Create a new database named `digilibz_db` (or adjust according to your configuration).
3. Import the initial database file located at:
`backend/src/main/resources/db/backup.sql`

### 2. Backend Configuration (Spring Boot)

1. Open the `backend` folder in your IDE (IntelliJ IDEA / VS Code).
2. Open the `src/main/resources/application.properties` (or `.yml`) file.
3. Adjust your database configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/digilibz_db
spring.datasource.username=root
spring.datasource.password=your_mysql_password

# JWT Configuration
jwt.secret=insert_your_long_secure_secret_key_here
jwt.expiration=86400000

```

4. Run the application with the command:

```bash
mvn spring-boot:run

```

*The Backend will run on port `8080`.*

### 3. Frontend Configuration (Next.js)

1. Open a new terminal and navigate to the `frontend` folder.

```bash
cd frontend

```

2. Install dependencies:

```bash
pnpm install
# or if using npm:
npm install

```

3. Create a `.env.local` file inside the `frontend` folder and add:

```env
NEXT_PUBLIC_API_URL=http://localhost:8080/api

```

4. Run the frontend server:

```bash
pnpm dev
# or
npm run dev

```

*The Frontend will run at `http://localhost:3000`.*

---

<br>

## 📝 API Documentation

Complete documentation regarding API endpoints can be found in the `document/` folder:

* [API Documentation](https://www.google.com/search?q=document/DocsApi.md)

<br>

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
