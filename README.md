# Next.js — Complete Learning Guide

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-Framework-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/React-Library-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/TypeScript-Language-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/Learning-In%20Progress-DC2626?style=for-the-badge" alt="Learning in Progress"/>
</p>

<p align="center">
  <b>Learn • Build • Practice • Grow</b>
</p>

<p align="center">
  A structured learning repository for Next.js, covering the App Router, layouts, pages, routing, React Server Components, data fetching, styling, API development, and full-stack projects.
</p>

---

## 📌 About This Repository

This repository is dedicated to learning **Next.js step by step**, from the fundamentals to advanced concepts used in modern web development.

It contains organized notes, practical examples, code snippets, and projects designed to strengthen my understanding of Next.js and its integration with React.

### 🎯 Learning Objectives

- Understand Next.js and its core features.
- Create Next.js applications.
- Learn the App Router architecture.
- Work with pages, layouts, and nested routes.
- Understand Server Components and Client Components.
- Implement dynamic routes and navigation.
- Fetch data from APIs and databases.
- Handle loading states, errors, and not-found pages.
- Build API endpoints using Route Handlers.
- Implement metadata and SEO.
- Learn authentication and authorization concepts.
- Build responsive and full-stack applications.

---

## 📚 Table of Contents

1. [Introduction to Next.js](#-introduction-to-nextjs)
2. [Why Next.js?](#-why-nextjs)
3. [Key Features](#-key-features)
4. [Prerequisites](#-prerequisites)
5. [Project Setup](#-project-setup)
6. [Project Structure](#-project-structure)
7. [App Router](#-app-router)
8. [Pages and Layouts](#-pages-and-layouts)
9. [Navigation and Links](#-navigation-and-links)
10. [Dynamic Routes](#-dynamic-routes)
11. [Server and Client Components](#-server-and-client-components)
12. [Styling](#-styling)
13. [Data Fetching](#-data-fetching)
14. [Route Handlers](#-route-handlers)
15. [Loading and Error Handling](#-loading-and-error-handling)
16. [Metadata and SEO](#-metadata-and-seo)
17. [Environment Variables](#-environment-variables)
18. [Learning Roadmap](#-learning-roadmap)
19. [Practice Projects](#-practice-projects)
20. [Best Practices](#-best-practices)
21. [Useful Resources](#-useful-resources)
22. [Author](#-author)

---

## 🔰 Introduction to Next.js

**Next.js** is a React framework for building modern web applications. It provides features for routing, rendering, data fetching, optimization, and server-side functionality.

React is primarily a UI library, while Next.js adds an application framework around React.

### What Can You Build with Next.js?

- Personal portfolios.
- Blogs and content websites.
- E-commerce applications.
- Admin dashboards.
- SaaS platforms.
- Authentication systems.
- Full-stack web applications.
- Documentation websites.
- Real-time application interfaces.

---

## 🤔 Why Next.js?

Building a production-ready React application often requires decisions about routing, rendering, data fetching, and deployment.

Next.js provides an integrated framework for many of these needs.

### Key Advantages

- File-system-based routing.
- Server Components and Client Components.
- Multiple rendering strategies.
- Built-in navigation and loading conventions.
- Server-side data access.
- Route Handlers for HTTP endpoints.
- Metadata support for SEO.
- Image and font optimization.
- Flexible deployment options.

**Important:** Next.js does not automatically make every page faster or SEO-perfect. Performance depends on implementation, rendering choices, caching, and the application itself.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| App Router | Organizes routes using the `app/` directory. |
| File-System Routing | Files and folders define routes. |
| Layouts | Share UI across pages and route segments. |
| Server Components | Render components on the server by default in the App Router. |
| Client Components | Support state, event handlers, and browser APIs. |
| Data Fetching | Retrieve data from APIs, databases, and other sources. |
| Route Handlers | Create HTTP endpoints using supported HTTP methods. |
| Metadata API | Define page titles, descriptions, and metadata. |
| Image Component | Optimize image delivery with `next/image`. |
| Font Optimization | Manage web fonts with `next/font`. |

---

## 🧰 Prerequisites

Before learning Next.js, understand these fundamentals:

- HTML and CSS.
- JavaScript ES6+.
- Arrow functions and modules.
- Arrays, objects, and array methods.
- Promises and `async` / `await`.
- React components and JSX.
- Props and state.
- React Hooks.
- Basic HTTP and REST API concepts.
- Basic Git and GitHub.

TypeScript is useful for larger projects but can be learned alongside Next.js.

---

## ⚙️ Project Setup

### Step 1: Check Node.js and npm

```bash
node -v
npm -v
```

Install a Node.js version supported by your chosen Next.js release.

### Step 2: Create a Next.js Application

```bash
npx create-next-app@latest nextjs-practice
```

Follow the prompts to select TypeScript, ESLint, Tailwind CSS, a `src/` directory, and the App Router according to your preferences.

### Step 3: Open the Project

```bash
cd nextjs-practice
```

### Step 4: Start the Development Server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

### Step 5: Build for Production

```bash
npm run build
npm run start
```

The production server runs the application after a successful build.

---

## 📁 Project Structure

A typical Next.js application using the App Router may look like this:

```text
nextjs-practice/
│
├── public/
│   ├── images/
│   └── icons/
│
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── globals.css
│   │   ├── loading.tsx
│   │   ├── error.tsx
│   │   ├── not-found.tsx
│   │   │
│   │   ├── about/
│   │   │   └── page.tsx
│   │   │
│   │   ├── blog/
│   │   │   ├── page.tsx
│   │   │   └── [slug]/
│   │   │       └── page.tsx
│   │   │
│   │   └── api/
│   │       └── users/
│   │           └── route.ts
│   │
│   ├── components/
│   ├── lib/
│   └── types/
│
├── .env.local
├── .gitignore
├── next.config.ts
├── package.json
├── tsconfig.json
└── README.md
```

### Important Directories

- `app/` — routes, layouts, pages, and route-level conventions.
- `components/` — reusable UI components.
- `lib/` — shared utilities and application logic.
- `types/` — reusable TypeScript types.
- `public/` — static assets served from the site root.
- `.env.local` — local environment variables; do not commit secrets.

This is an example structure, not a requirement. JavaScript projects may use `.js` and `.jsx` instead of TypeScript extensions.

---

## 🛣️ App Router

The App Router is Next.js's file-system routing system built around the `app/` directory.

### Basic Route Structure

```text
app/
├── page.tsx
├── about/
│   └── page.tsx
└── contact/
    └── page.tsx
```

This structure defines:

| File | URL |
|---|---|
| `app/page.tsx` | `/` |
| `app/about/page.tsx` | `/about` |
| `app/contact/page.tsx` | `/contact` |

### Example: Home Page

```tsx
export default function HomePage() {
  return (
    <main>
      <h1>Welcome to Next.js</h1>
      <p>Learning Next.js step by step.</p>
    </main>
  );
}
```

A `page.tsx` file makes its route segment accessible as a page.

---

## 📄 Pages and Layouts

### Pages

A page defines the UI for a specific route.

Example: `app/about/page.tsx`

```tsx
export default function AboutPage() {
  return (
    <main>
      <h1>About Me</h1>
      <p>This is my About page.</p>
    </main>
  );
}
```

### Layouts

A layout provides shared UI for its child routes.

Example: `app/layout.tsx`

```tsx
import type { Metadata } from "next";
import "./globals.css";

export const metadata: Metadata = {
  title: "Next.js Learning",
  description: "Learning modern web development with Next.js.",
};

export default function RootLayout({
  children,
}: Readonly<{
  children: React.ReactNode;
}>) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```

The root layout is required in the App Router and defines the document's outer structure.

---

## 🔗 Navigation and Links

Next.js provides the `Link` component for client-side navigation between application routes.

```tsx
import Link from "next/link";

export default function Navigation() {
  return (
    <nav>
      <Link href="/">Home</Link>
      <Link href="/about">About</Link>
      <Link href="/contact">Contact</Link>
    </nav>
  );
}
```

### Programmatic Navigation

Use `useRouter()` from `next/navigation` in a Client Component when navigation needs to happen in response to an event or other client-side logic.

```tsx
"use client";

import { useRouter } from "next/navigation";

export default function DashboardButton() {
  const router = useRouter();

  return (
    <button onClick={() => router.push("/dashboard")}>
      Open Dashboard
    </button>
  );
}
```

---

## 🔀 Dynamic Routes

Dynamic routes allow a page to handle different values using the same route structure.

### Example Structure

```text
app/
└── products/
    └── [id]/
        └── page.tsx
```

The route `/products/123` matches the dynamic segment `[id]`.

### Example: Dynamic Product Page

```tsx
type ProductPageProps = {
  params: Promise<{
    id: string;
  }>;
};

export default async function ProductPage({
  params,
}: ProductPageProps) {
  const { id } = await params;

  return (
    <main>
      <h1>Product Details</h1>
      <p>Product ID: {id}</p>
    </main>
  );
}
```

In current App Router versions, `params` is asynchronous. Check the documentation for the Next.js version used by your project.

### Common Dynamic Route Patterns

- `[id]` — one dynamic segment.
- `[...slug]` — one or more path segments.
- `[[...slug]]` — optional catch-all segment.

---

## ⚛️ Server and Client Components

The App Router uses React Server Components by default.

### Server Components

Server Components are suitable for:

- Reading data on the server.
- Accessing server-only resources.
- Keeping private server logic out of the client bundle.
- Rendering content that does not require browser interactivity.

Example:

```tsx
export default function ServerPage() {
  return <h1>Rendered using a Server Component</h1>;
}
```

### Client Components

Client Components are needed for:

- React state and interactive Hooks.
- Event handlers.
- Browser APIs.
- Effects and client-side interactions.

Example:

```tsx
"use client";

import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```

### Key Differences

| Server Components | Client Components |
|---|---|
| Default in the App Router | Declared using `"use client"` when needed |
| Can access server-side resources | Support browser-side interactivity |
| Do not use client Hooks such as `useState` | Can use `useState` and `useEffect` |
| Can reduce client-side JavaScript | Add their client-side code to the bundle |

**Best practice:** Keep components on the server by default and introduce Client Components only where interactivity is required.

---

## 🎨 Styling

Next.js supports multiple styling approaches.

### 1. Global CSS

Import a global stylesheet from the root layout.

```tsx
import "./globals.css";
```

### 2. CSS Modules

Create `Button.module.css`:

```css
.button {
  padding: 12px 20px;
  border-radius: 8px;
  background: #2563eb;
  color: white;
}
```

Use it in a component:

```tsx
import styles from "./Button.module.css";

export default function Button() {
  return (
    <button className={styles.button}>
      Click Me
    </button>
  );
}
```

### 3. Other Styling Options

- Sass / SCSS.
- Tailwind CSS.
- CSS-in-JS solutions compatible with your rendering setup.
- Plain CSS.

Choose a styling approach based on project requirements and maintainability.

---

## 🌐 Data Fetching

Next.js supports data fetching in Server Components, Client Components, and Route Handlers.

### Example: Fetch Data in a Server Component

```tsx
type User = {
  id: number;
  name: string;
  email: string;
};

export default async function UsersPage() {
  const response = await fetch(
    "https://jsonplaceholder.typicode.com/users"
  );

  if (!response.ok) {
    throw new Error("Failed to fetch users");
  }

  const users: User[] = await response.json();

  return (
    <main>
      <h1>Users</h1>

      <ul>
        {users.map((user) => (
          <li key={user.id}>
            {user.name} — {user.email}
          </li>
        ))}
      </ul>
    </main>
  );
}
```

### Important Concepts

- `async` / `await`.
- HTTP response handling.
- Loading and error UI.
- Cache behavior and revalidation.
- Server-side data access.
- Client-side data fetching when needed.
- Database integration.

Next.js caching behavior varies by version and API. Explicitly configure caching or revalidation when your application requires particular freshness guarantees.

---

## 🔌 Route Handlers

Route Handlers allow you to define HTTP endpoints using a `route.ts` or `route.js` file inside the App Router.

### Example Structure

```text
app/
└── api/
    └── users/
        └── route.ts
```

### Example: GET and POST

```tsx
import { NextResponse } from "next/server";

export async function GET() {
  return NextResponse.json({
    message: "Users API is working",
  });
}

export async function POST(request: Request) {
  const body = await request.json();

  return NextResponse.json(
    {
      message: "Data received",
      data: body,
    },
    { status: 201 }
  );
}
```

Visit `/api/users` to test the GET endpoint.

For production APIs, validate incoming data, handle errors, and implement authentication and authorization where required.

---

## ⏳ Loading and Error Handling

The App Router provides special files for common route states.

### Loading UI

Create `app/loading.tsx`:

```tsx
export default function Loading() {
  return <p>Loading...</p>;
}
```

### Error UI

Create `app/error.tsx`:

```tsx
"use client";

export default function ErrorPage({
  reset,
}: {
  error: Error & { digest?: string };
  reset: () => void;
}) {
  return (
    <main>
      <h1>Something went wrong</h1>
      <button onClick={() => reset()}>
        Try Again
      </button>
    </main>
  );
}
```

An `error.tsx` file creates an error boundary for its route segment. It must be a Client Component.

### Not Found UI

Create `app/not-found.tsx`:

```tsx
export default function NotFound() {
  return (
    <main>
      <h1>404 — Page Not Found</h1>
      <p>The requested page could not be found.</p>
    </main>
  );
}
```

---

## 🔍 Metadata and SEO

Next.js supports metadata through a `metadata` export or a `generateMetadata()` function in eligible Server Components.

### Static Metadata

```tsx
import type { Metadata } from "next";

export const metadata: Metadata = {
  title: "About | My Website",
  description: "Learn more about my website and projects.",
};

export default function AboutPage() {
  return <h1>About Us</h1>;
}
```

### Why Metadata Matters

- Describes the page's content.
- Helps search engines understand the page.
- Controls common browser and link-preview metadata.
- Supports page-specific titles and descriptions.

SEO also depends on content quality, accessibility, performance, crawlability, and correct indexing configuration.

---

## 🔐 Environment Variables

Environment variables allow you to configure applications without hardcoding environment-specific values.

Create `.env.local`:

```env
DATABASE_URL=your_database_connection_string
API_SECRET=your_secret_value
NEXT_PUBLIC_API_URL=https://example.com/api
```

Read a server-only variable:

```tsx
const databaseUrl = process.env.DATABASE_URL;
```

Read a public variable:

```tsx
const apiUrl = process.env.NEXT_PUBLIC_API_URL;
```

**Security rules:**

- Never commit `.env.local` containing secrets.
- Do not expose private keys or credentials with the `NEXT_PUBLIC_` prefix.
- Validate required environment variables.
- Use server-side code for private credentials.
- Configure production variables in your hosting environment.

---

## 🖼️ Images and Fonts

### Image Optimization

Next.js provides the `Image` component.

```tsx
import Image from "next/image";

export default function ProfileImage() {
  return (
    <Image
      src="/images/profile.jpg"
      alt="Profile"
      width={300}
      height={300}
    />
  );
}
```

Images stored in `public/images/` can be referenced using `/images/profile.jpg`.

For remote images, configure permitted remote sources in your Next.js image configuration.

### Font Optimization

Next.js also provides `next/font` to help load fonts efficiently.

```tsx
import { Geist } from "next/font/google";

const geist = Geist({
  subsets: ["latin"],
});

export default function RootLayout({
  children,
}: Readonly<{
  children: React.ReactNode;
}>) {
  return (
    <html lang="en">
      <body className={geist.className}>
        {children}
      </body>
    </html>
  );
}
```

---

## 🗺️ Learning Roadmap

Track your progress as you work through the repository.

### Fundamentals

- [ ] Introduction to Next.js
- [ ] Next.js versus React
- [ ] Project setup and configuration
- [ ] Understanding the App Router
- [ ] File-system routing
- [ ] Pages and layouts

### Routing

- [ ] Navigation with `Link`
- [ ] Programmatic navigation
- [ ] Dynamic routes
- [ ] Catch-all routes
- [ ] Route groups
- [ ] Nested layouts
- [ ] Loading and error conventions

### React Integration

- [ ] Server Components
- [ ] Client Components
- [ ] Props and component composition
- [ ] State and event handling
- [ ] Form handling
- [ ] Context and shared state

### Styling and Assets

- [ ] Global CSS
- [ ] CSS Modules
- [ ] Sass / SCSS
- [ ] Tailwind CSS
- [ ] Image optimization
- [ ] Font optimization

### Data and Backend

- [ ] Data fetching
- [ ] HTTP requests
- [ ] Caching and revalidation
- [ ] Route Handlers
- [ ] Forms and mutations
- [ ] Database integration
- [ ] Environment variables
- [ ] Authentication and authorization

### Production

- [ ] Metadata and SEO
- [ ] Error handling
- [ ] Performance optimization
- [ ] Security fundamentals
- [ ] Testing
- [ ] Production builds
- [ ] Deployment

---

## 🚀 Practice Projects

Build these projects to strengthen your understanding.

| Level | Project | Concepts |
|---|---|---|
| Beginner | Personal Portfolio | Pages, layouts, styling |
| Beginner | Multi-Page Website | Navigation and nested routes |
| Beginner | Blog Website | Dynamic routes and metadata |
| Intermediate | Todo Application | Forms and state management |
| Intermediate | Weather Dashboard | API integration and loading states |
| Intermediate | Admin Dashboard | Layouts and protected routes |
| Intermediate | Product Catalogue | Dynamic routes and data fetching |
| Advanced | E-commerce Application | Products, cart, authentication |
| Advanced | Full-Stack Task Manager | Database, validation, authorization |
| Advanced | SaaS Dashboard | Server-side logic and scalable architecture |

Start with small projects and gradually add features as you learn.

---

## ✅ Best Practices

- Use the App Router for new projects unless you have a specific reason to use the Pages Router.
- Keep Server Components as the default where practical.
- Use Client Components only for features that require client-side capabilities.
- Keep reusable components organized.
- Use meaningful route and file names.
- Validate user input on the server.
- Never expose secrets to the browser.
- Handle loading, error, and empty states.
- Use TypeScript for improved maintainability when appropriate.
- Configure caching and revalidation intentionally.
- Optimize images and fonts.
- Test important application behavior.
- Review production builds before deployment.

---

## 📖 Useful Resources

- [Next.js Official Documentation](https://nextjs.org/docs)
- [Next.js Learn Course](https://nextjs.org/learn)
- [Next.js App Router](https://nextjs.org/docs/app)
- [Next.js API Reference](https://nextjs.org/docs/app/api-reference)
- [React Official Documentation](https://react.dev/)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
- [Vercel Documentation](https://vercel.com/docs)

---

## 👨‍💻 Author

**Amol Pawar**

Full Stack Developer | React.js Developer

Learning, practicing, and building projects to improve my frontend and full-stack development skills.

- GitHub: [@amolpawar24](https://github.com/amolpawar24)
- Portfolio: [amolpawar24.vercel.app](https://amolpawar24.vercel.app/)

---

## ⭐ Support

If this repository helps you learn Next.js, consider giving it a star ⭐.

Explore the examples, practice the concepts, and build your own projects as you progress.

<p align="center">
  <b>Learn • Build • Grow</b>
</p>

<p align="center">
  Made with ❤️ by Amol Pawar
</p>