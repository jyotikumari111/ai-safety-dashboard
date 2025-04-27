

# AI Safety Incident Dashboard

Frontend Intern Take-Home Assignment for HumanChain.

## 🚀 Project Overview

This is a simple interactive dashboard to **view, filter, sort, and add AI Safety Incidents**.  
Built using **React** + **TypeScript**, focused on clean structure, responsive design, and basic user interaction handling.

---

## 🛠 Tech Stack

- **React 18**
- **TypeScript**
- **Vite**
- **TailwindCSS** (optional but lightweight for fast styling)

---

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/ai-safety-dashboard.git
cd ai-safety-dashboard
```

2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

Project will be running at `http://localhost:5173`.

---

## 🎯 Features

- View a list of AI safety incidents (Title, Severity, Reported Date)
- **Filter** incidents by severity: `All`, `Low`, `Medium`, `High`
- **Sort** incidents by reported date: `Newest First`, `Oldest First`
- Expand/collapse to view **full description** for each incident
- **Add new incidents** via a form with basic validation
- Fully **responsive layout** (Flexbox/Grid)
- Clean **hover effects** and user-friendly interface

---

## ✨ Design Decisions

- **State Management**: Local `useState` for simplicity; scalable to Redux/Zustand if needed.
- **Data Handling**: Incidents managed entirely **in memory** as per assignment guidelines.
- **Component Separation**: Broken down into small reusable components (`IncidentList`, `IncidentForm`, `FilterSortControls`) for maintainability.
- **ID Generation**: Used `Date.now()` for simplicity — for production, a UUID generator would be preferable.
- **Accessibility**: Added basic `hover/focus` styles to improve usability.

---

## ⚡ Challenges

- Handling local component states cleanly while keeping code readable.
- Ensuring the expanded "View Details" toggle didn't affect other items.
- Managing types strictly with TypeScript for safer props and state transitions.


---

✅ **Extra TailwindCSS Styling Tips:**

If you don't have Tailwind installed yet but want nice hover effects, install it:

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

In `tailwind.config.ts`, enable basic paths:

```ts
content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
```

And replace `/src/index.css` with:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

/* Custom tweaks */
body {
  @apply bg-gray-100 text-gray-800;
}
```

