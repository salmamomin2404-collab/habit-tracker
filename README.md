# 💰 Expense Tracker

A beginner-friendly full-stack Expense Tracker application built using **React**, **Vite**, **Node.js**, **Express**, and **SQLite**.

This project allows users to record daily expenses, filter them by category, view monthly spending summaries, and manage expenses through a clean and responsive interface.

---

# 🚀 Features

- ➕ Add new expenses
- 📋 View all expenses
- 🗂 Filter expenses by category
- 📄 Paginated expense list
- 📅 Monthly expense summary
- 📊 Category-wise spending bars
- 🗑 Delete expenses
- 💾 SQLite database storage
- 🔄 REST API using Express
- 🌐 React frontend with Fetch API

---

# 🛠 Tech Stack

## Frontend

- React
- Vite
- JavaScript (ES6)
- CSS

## Backend

- Node.js
- Express
- better-sqlite3
- CORS

## Database

- SQLite (`data.db`)

---

# 📁 Project Structure

```
Expense-Tracker/
│
├── backend/
│   ├── index.js
│   ├── package.json
│   └── data.db
│
└── frontend/
    ├── src/
    │   ├── App.jsx
    │   ├── App.css
    │   ├── main.jsx
    │   └── index.css
    │
    └── package.json
```

---

# 📦 Installation

## 1. Clone the repository

```bash
git clone <repository-url>
```

---

## 2. Start Backend

Open a terminal inside the **backend** folder.

```bash
cd backend
node index.js
```

The backend starts on:

```
http://localhost:5000
```

---

## 3. Start Frontend

Open another terminal inside the **frontend** folder.

```bash
cd frontend
npm run dev
```

Vite will start the React application (usually on):

```
http://localhost:5173
```

---

# 💾 Database

The application automatically creates a SQLite database named:

```
data.db
```

It also creates the following table if it doesn't already exist.

## expenses

| Column | Type |
|---------|------|
| id | INTEGER PRIMARY KEY AUTOINCREMENT |
| title | TEXT |
| amount | REAL |
| category | TEXT |
| date | TEXT |
| created_at | TEXT |

---

# 📝 Expense Categories

The application supports these categories:

- 🍔 Food
- 🚌 Transport
- 💡 Bills
- 🎬 Entertainment
- 📦 Other

---

# 🌐 REST API

## Create Expense

**POST**

```
/expenses
```

### Request

```json
{
  "title": "Groceries",
  "amount": 450.50,
  "category": "Food",
  "date": "2026-07-06"
}
```

### Success Response

```json
{
  "id": 1,
  "title": "Groceries",
  "amount": 450.5,
  "category": "Food",
  "date": "2026-07-06",
  "created_at": "2026-07-06T10:15:00.000Z"
}
```

---

## Get Expenses

**GET**

```
/expenses
```

### Optional Query Parameters

| Parameter | Description |
|-----------|-------------|
| page | Page number |
| limit | Records per page |
| category | Filter by category |
| month | Filter by month (YYYY-MM) |

Examples:

```
GET /expenses?page=1
```

```
GET /expenses?category=Food
```

```
GET /expenses?month=2026-07
```

---

## Monthly Summary

**GET**

```
/expenses/summary
```

Example:

```
GET /expenses/summary?month=2026-07
```

Example Response

```json
{
  "month": "2026-07",
  "categories": [
    {
      "category": "Food",
      "total": 1200.5
    },
    {
      "category": "Bills",
      "total": 850
    }
  ],
  "grandTotal": 2050.5
}
```

---

## Update Expense

**PUT**

```
/expenses/:id
```

Example Request

```json
{
  "amount": 650
}
```

Only the supplied fields are updated.

---

## Delete Expense

**DELETE**

```
/expenses/:id
```

Example Response

```json
{
  "message": "Expense 5 deleted"
}
```

---

# 🖥 Frontend Features

### Add Expense

- Expense title
- Amount
- Category selection
- Date picker
- Input validation

---

### Monthly Summary

- Select any month
- Category-wise totals
- Horizontal spending bars
- Grand total
- Loading indicator
- Empty-state message

---

### Expense List

Each expense displays:

- Title
- Category tag
- Amount
- Date
- Delete button

Additional features:

- Category filtering
- Pagination
- Loading state
- Empty state

---

# ✔ Validation

The application validates:

- Title cannot be empty.
- Amount must be greater than zero.
- Category is required.
- Date is required.

---

# 📄 Pagination

Expense records support pagination.

The interface includes:

- ◀ Previous button
- Next ▶ button
- Current page indicator
- Automatic total page calculation

---

# 🎨 User Interface

The application includes:

- Responsive centered layout
- Card-based design
- Category tags
- Summary progress bars
- Styled buttons
- Clean typography
- Beginner-friendly layout

---

# 📚 Technologies Used

- React
- Vite
- JavaScript
- Node.js
- Express
- SQLite
- better-sqlite3
- Fetch API
- CSS3

---

# 🔮 Future Improvements

Some ideas for extending this project:

- Edit expenses from the UI
- Search expenses by title
- Sort by amount or date
- Export expenses to CSV
- Expense charts and graphs
- Budget planning
- Dark mode
- Annual reports
- Import/Export database
- Mobile-friendly improvements

---

# 🎯 Learning Objectives

This project demonstrates:

- Building REST APIs with Express
- Working with SQLite using better-sqlite3
- CRUD operations
- React Hooks (`useState`, `useEffect`)
- Fetch API
- Form validation
- Pagination
- Filtering
- State management
- Full-stack application development

---

# 👨‍💻 Author

**Expense Tracker**

A beginner-friendly full-stack project created for learning **React**, **Express**, and **SQLite** development.# habit-tracker
