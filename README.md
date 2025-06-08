# CSV Manager – SaaS App with Next.js & OpenSaaS

This is a full-stack SaaS-style application for uploading, storing, and managing CSV files. Built using **Next.js**, **Node.js**, **PostgreSQL**, and **Prisma**, this project also integrates **OpenSaaS** for user authentication and AI-powered development via **Cursor AI**.

Built for the Full Stack Developer Assessment | June 2025

---

## Features

-  Auth: User signup/login using OpenSaaS Auth
-  CSV Upload: Drag-and-drop support with file validation
-  Data Management: 
  - Automatic schema mapping for uploaded CSVs
  - Row and column storage with dynamic headers
  - Editable, sortable, and paginated table view
-  Scoped Data: Each user only sees their own uploads
-  Cursor AI: Used extensively for architecture, code snippets, and troubleshooting
-  Prisma + PostgreSQL integration for scalable data modeling

---

##  Tech Stack

- **Framework**: [Next.js](https://nextjs.org/) with App Router
- **Database**: [PostgreSQL](https://www.postgresql.org/)
- **ORM**: [Prisma](https://www.prisma.io/)
- **UI Library**: [shadcn/ui](https://ui.shadcn.com/)
- **Auth & Boilerplate**: [OpenSaaS](https://www.opensaas.sh/)
- **AI Development**: [Cursor AI](https://www.cursor.sh/)

---

## Getting Started

Clone the repo and install dependencies:

```bash
git clone https://github.com/Gopaswathy98/csv-manager-opensaas.git
cd csv-manager-opensaas
npm install
```

Set up your `.env` file:

```env
DATABASE_URL="postgresql://postgres:admin123@localhost:5432/csvmanager"
AUTH_SECRET="your-secure-secret"
BASE_URL="http://localhost:3000"
NODE_ENV="development"
```

Run the database:

```bash
npx prisma generate
npx prisma migrate dev
```

Run the dev server:

```bash
npm run dev
```

Open `http://localhost:3000` to get started.

---

## Folder Structure

```
/app
  /api/csv          → API routes for upload/list
  /dashboard        → Table view for CSVs
  /auth             → Handled by OpenSaaS
/lib
  prisma.ts         → Prisma client
/components
  CsvManager.tsx    → Dynamic table UI
```

---

## Completed Tasks

- [x] Authentication with OpenSaaS
- [x] CSV upload with metadata parsing
- [x] Prisma schema for `CsvFile` and `CsvRow`
- [x] Table rendering with dynamic headers
- [x] Pagination, sorting, and cell editing
- [x] User-specific data access control

---

## AI Development Log  

This project was built using **Cursor AI** to:
- Scaffold Prisma schemas
- Design REST API endpoints
- Implement upload logic and table rendering
- Solve environment and migration issues

_Exported Cursor AI chat history included in project documentation._

---

## 🧪 Testing

Use sample CSVs and login via the `/sign-up` route. All uploads are scoped to the logged-in user. Admin access is not required.

---

## 📄 License

MIT © 2025 – 
