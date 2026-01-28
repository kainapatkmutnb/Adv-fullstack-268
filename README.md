# Adv-fullstack-268

## 📚 Book CRUD API (No Database)

RESTful API สำหรับจัดการข้อมูลหนังสือ โดยใช้ Express.js และเก็บข้อมูลใน Memory (ไม่ใช้ Database)

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 หรือสูงกว่า)
- npm

### Installation

1. **Clone repository**

   ```bash
   git clone https://github.com/your-username/Adv-fullstack-268.git
   cd Adv-fullstack-268
   ```

2. **ติดตั้ง dependencies**

   ```bash
   npm install
   ```

3. **สร้างไฟล์ .env** (optional)

   ```bash
   PORT=5000
   ```

4. **รันเซิร์ฟเวอร์**

   ```bash
   # Development mode (with auto-reload)
   npm run dev

   # Production mode
   npm start
   ```

   หรือรันไฟล์ `CRUDBookNoDB.js` โดยตรง:

   ```bash
   node CRUDBookNoDB.js
   ```

---

## 📁 Project Structure

```
Adv-fullstack-268/
├── src/
│   └── index.js          # Main application
├── CRUDBookNoDB.js       # CRUD Book API (No Database)
├── package.json
├── .env
├── .gitignore
└── README.md
```

---

## 🔌 API Endpoints

| Method | Endpoint     | Description             |
| ------ | ------------ | ----------------------- |
| GET    | `/books`     | ดึงข้อมูลหนังสือทั้งหมด |
| GET    | `/books/:id` | ดึงข้อมูลหนังสือตาม ID  |
| POST   | `/books`     | เพิ่มหนังสือใหม่        |
| PUT    | `/books/:id` | แก้ไขข้อมูลหนังสือ      |
| DELETE | `/books/:id` | ลบหนังสือ               |

---

## 📝 API Usage Examples

> 💡 **Tip**: ใช้ [Postman](https://www.postman.com/) สำหรับทดสอบ API ได้สะดวกยิ่งขึ้น

### GET - ดึงข้อมูลหนังสือทั้งหมด

```bash
curl http://localhost:5000/books
```

### GET - ดึงข้อมูลหนังสือตาม ID

```bash
curl http://localhost:5000/books/1
```

### POST - เพิ่มหนังสือใหม่

```bash
curl -X POST http://localhost:5000/books \
  -H "Content-Type: application/json" \
  -d '{"title": "New Book", "author": "New Author"}'
```

### PUT - แก้ไขข้อมูลหนังสือ

```bash
curl -X PUT http://localhost:5000/books/1 \
  -H "Content-Type: application/json" \
  -d '{"title": "Updated Book", "author": "Updated Author"}'
```

### DELETE - ลบหนังสือ

```bash
curl -X DELETE http://localhost:5000/books/1
```

---

## 📦 Dependencies

- **express** - Web framework
- **dotenv** - Environment variables

### Dev Dependencies

- **nodemon** - Auto-reload server on file changes
- **prettier** - Code formatter

---

## 🛠️ Scripts

| Script           | Description                  |
| ---------------- | ---------------------------- |
| `npm start`      | รันเซิร์ฟเวอร์ (production)  |
| `npm run dev`    | รันเซิร์ฟเวอร์ (development) |
| `npm run format` | Format code with Prettier    |
