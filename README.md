# Restaurant-2 RestaurantTS - Modern Next.js Frontend Restaurant Website (Design 2)

![project23](https://github.com/user-attachments/assets/8c0b14ce-5afb-4387-8c2f-48ee1fbb7c2b) ![Screenshot 2024-09-13 at 03 34 24](https://github.com/user-attachments/assets/0bc0ad55-6c33-4ecf-9a6b-44627ebc2396) ![Screenshot 2024-09-13 at 03 35 51](https://github.com/user-attachments/assets/42ea4942-e2cc-4119-b83a-31c49062ec90) ![Screenshot 2024-09-13 at 03 34 55](https://github.com/user-attachments/assets/3107bdb9-cc73-4ca6-b79d-4f4748eeab59) ![Screenshot 2024-09-13 at 03 35 33](https://github.com/user-attachments/assets/24751061-c447-4196-840e-825695fa0d1d)

---

## Project Summary

**RestaurantTS** is a modern, fully static Restaurant Landing Page built with [Next.js 14](https://nextjs.org/), React.js, and TypeScript. The project demonstrates how to create a visually appealing, performant, and interactive single-page website using a contemporary frontend stack: TailwindCSS for styling, Framer Motion for animation, Radix-UI for accessible components, and more. This project serves as both a professional portfolio piece and a practical learning resource for anyone wanting to master modern React and Next.js development with TypeScript and TailwindCSS.

- **Live-Demo:** [https://restaurant-ts-arnob.vercel.app/](https://restaurant-ts-arnob.vercel.app/)

> **Note:** This static webpage is built using TypeScript. For the JavaScript version, see [RestaurantJS-NextJS-Website](https://github.com/arnobt78/RestaurantJS-NextJS-Website).

---

## Table of Contents

1. [Project Summary](#project-summary)
2. [Tech Stack & Dependencies](#tech-stack--dependencies)
3. [Project Structure](#project-structure)
4. [How to Run the Project](#how-to-run-the-project)
5. [Main Components & Features](#main-components--features)
6. [APIs, Routes & Core Logic](#apis-routes--core-logic)
7. [Styling, Animations & Accessibility](#styling-animations--accessibility)
8. [Learning Purposes & Teaching Points](#learning-purposes--teaching-points)
9. [Code Examples & Usage](#code-examples--usage)
10. [Deployment](#deployment)
11. [Resources](#resources)
12. [Conclusion](#conclusion)

---

## Tech Stack & Dependencies

- **Framework:** [Next.js 14](https://nextjs.org/) (React-based, supports server-side rendering and static exports)
- **Language:** [TypeScript](https://www.typescriptlang.org/) (strong typing for safer code)
- **Styling:** [TailwindCSS](https://tailwindcss.com/) (utility-first CSS)
- **Animation:** [Framer Motion](https://www.framer.com/motion/)
- **UI Components:** [Radix-UI](https://www.radix-ui.com/)
- **Date Handling:** [date-fns](https://date-fns.org/)
- **Maps:** [React-Leaflet](https://react-leaflet.js.org/)
- **Icons:** [Lucide-React](https://lucide.dev/), [react-icons](https://react-icons.github.io/react-icons/)
- **Responsive Design:** [react-responsive](https://github.com/contra/react-responsive)
- **Other:** [react-scroll](https://github.com/fisshy/react-scroll), [react-day-picker](https://react-day-picker.js.org/), [tailwindcss-animate](https://www.npmjs.com/package/tailwindcss-animate)
- **Font Optimization:** Uses [next/font](https://nextjs.org/docs/basic-features/font-optimization) for automatic font loading

**Install all dependencies:**
```bash
npm install
```
Or, install specific packages:
```bash
npm i framer-motion date-fns react-leaflet lucide-react react-day-picker react-scroll react-icons react-responsive tailwindcss-animate radix-ui
```

---

## Project Structure

A typical structure for this project (may vary if you customize):

```
RestaurantTS--TailwindCSS-Fundamental-Project-4/
├── app/
│   ├── page.tsx           # Main landing page component
│   ├── layout.tsx         # Root layout for the app
│   └── ...                # Other pages or API routes (if any)
├── components/
│   ├── Header.tsx         # Navigation bar
│   ├── Hero.tsx           # Hero section (main banner)
│   ├── Menu.tsx           # Menu listing
│   ├── ReservationForm.tsx# Booking/reservation form
│   ├── LocationMap.tsx    # Embedded map (React-Leaflet)
│   └── ...                # Other reusable UI components
├── public/
│   ├── images/            # Static assets
│   └── ...                # Favicon, etc.
├── styles/
│   ├── globals.css        # TailwindCSS base styles
├── tailwind.config.js     # TailwindCSS configuration
├── tsconfig.json          # TypeScript configuration
├── package.json           # Project metadata and dependencies
└── README.md              # This file
```

---

## How to Run the Project

**Requirements:** Node.js (see [official instructions](https://nodejs.org/en/) for installation)

### 1. Clone the repository
```bash
git clone https://github.com/arnobt78/RestaurantTS--TailwindCSS-Fundamental-Project-4.git
cd RestaurantTS--TailwindCSS-Fundamental-Project-4
```

### 2. Install dependencies
```bash
npm install
```

### 3. Run the development server
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Visit [http://localhost:3000](http://localhost:3000) in your browser. The page reloads automatically as you edit.

---

## Main Components & Features

- **Responsive Layout:** Adapts seamlessly to all devices, mobile to desktop.
- **Animated Sections:** Smooth entry effects with Framer Motion and Tailwind Animate.
- **Hero Banner:** Eye-catching introduction with call-to-action button.
- **Menu Showcase:** Interactive menu cards, category filtering, and appealing food images.
- **Reservation Form:** Collects user input for table booking with date picker (react-day-picker).
- **Location Map:** Embedded map using React-Leaflet, shows restaurant location interactively.
- **Contact & Footer:** Contact details, social links, and copyright.

---

## APIs, Routes & Core Logic

This is a static site—no backend or database—but demonstrates core Next.js routing and component logic:

- **Routing:** Uses [app directory routing](https://nextjs.org/docs/app/building-your-application/routing).
  - `app/page.tsx` is the main route ("/").
- **APIs:** No external API calls; all data is local/static or passed as props.
- **State Management:** Uses React's `useState` and `useEffect` for form handling, menu interactivity, and UI state.
- **Components:** Modular, reusable React functional components, each with clear props and TypeScript types.
- **Forms:** Basic validation and controlled input for reservations.

---

## Styling, Animations & Accessibility

- **TailwindCSS:** Utility classes for rapid, consistent styling.
- **Framer Motion:** Used for entrance animations (fade-in, slide-up, etc.).
- **Radix-UI:** Headless UI primitives for accessible dropdowns, dialogs, etc.
- **Accessibility:** Semantic HTML, keyboard navigation support, ARIA attributes where needed.

Example: Animate a section
```tsx
import { motion } from "framer-motion";

<motion.div
  initial={{ opacity: 0, y: 40 }}
  animate={{ opacity: 1, y: 0 }}
  transition={{ duration: 0.8 }}
>
  {/* Section content */}
</motion.div>
```

---

## Learning Purposes & Teaching Points

- **TypeScript in Next.js:** Strong typing for components and props.
- **Modern React Patterns:** Functional components, hooks, and context.
- **Utility-First CSS:** Rapid prototyping and responsive design with Tailwind.
- **Static Export:** Next.js static site generation for fast, SEO-friendly sites.
- **Component Reusability:** Break UI into logical, reusable pieces.
- **Accessibility:** Building inclusive interfaces from the start.
- **Animation:** Adding polish and engagement with minimal code.

---

## Code Examples & Usage

### Example: Menu Item Component (TypeScript + TailwindCSS)
```tsx
// components/MenuItem.tsx
type MenuItemProps = {
  name: string;
  description: string;
  price: number;
  imageUrl: string;
};

export default function MenuItem({ name, description, price, imageUrl }: MenuItemProps) {
  return (
    <div className="bg-white rounded-lg shadow-md p-4 flex flex-col items-center">
      <img src={imageUrl} alt={name} className="w-32 h-32 object-cover rounded-full mb-3" />
      <h3 className="text-xl font-bold">{name}</h3>
      <p className="text-gray-500">{description}</p>
      <span className="text-lg font-semibold text-green-700">${price.toFixed(2)}</span>
    </div>
  );
}
```

### Example: Reservation Form Validation
```tsx
const [name, setName] = useState("");
const [date, setDate] = useState<Date | null>(null);

const handleSubmit = (e: React.FormEvent) => {
  e.preventDefault();
  if (!name || !date) {
    alert("Please fill all required fields!");
    return;
  }
  // Submit logic...
};
```

---

## Deployment

The easiest way to deploy is with [Vercel](https://vercel.com/):

1. Push your code to GitHub.
2. Go to [Vercel New Project](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app).
3. Import your repo and follow the prompts.
4. Your site will be live at a public URL.

See [Next.js deployment docs](https://nextjs.org/docs/deployment) for more details.

---

## Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Learn Next.js](https://nextjs.org/learn)
- [Next.js GitHub Repository](https://github.com/vercel/next.js/)
- [TailwindCSS Docs](https://tailwindcss.com/docs)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- [Framer Motion Guide](https://www.framer.com/motion/)
- [Radix-UI Docs](https://www.radix-ui.com/docs/primitives/overview/introduction)
- [date-fns Docs](https://date-fns.org/docs/Getting-Started)
- [React-Leaflet Docs](https://react-leaflet.js.org/)
- [Lucide React](https://lucide.dev/)

---

## Conclusion

This project is a comprehensive demonstration of building a visually rich, accessible, and performant static website using the latest web technologies. It is suitable both as a portfolio piece and as a learning resource for those wishing to master Next.js, TypeScript, React, and TailwindCSS in real-world scenarios. Feel free to use, fork, and adapt this project for your own learning or restaurant business!

---

## Happy Coding! 🎉

Feel free to use this project repository and extend this project further!

If you have any questions or want to share your work, reach out via GitHub or my portfolio at [https://arnob-mahmud.vercel.app/](https://arnob-mahmud.vercel.app/).

**Enjoy building and learning!** 🚀

Thank you! 😊

---
