<div align="center">
  <img src="./assets/suga_logo.png" width="100" height="100" alt="SugaCart Logo" style="border-radius: 20px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
  <h1 style="margin-top: 12px; font-size: 2.5rem; font-weight: 800;">SugaCart.com</h1>
  <p style="font-size: 1.15rem; color: #64748b; max-width: 650px;">
    A modern, high-performance multi-vendor e-commerce platform featuring a custom pastel aesthetic, real-time cart state management, and dedicated merchant & admin analytics portals.
  </p>

  <p>
    <img src="https://img.shields.io/badge/Next.js_15.5-black?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js 15" />
    <img src="https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React 19" />
    <img src="https://img.shields.io/badge/Tailwind_CSS_v4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
    <img src="https://img.shields.io/badge/Redux_Toolkit-764ABC?style=for-the-badge&logo=redux&logoColor=white" alt="Redux Toolkit" />
    <img src="https://img.shields.io/badge/Prisma_ORM-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma ORM" />
    <img src="https://img.shields.io/badge/Deployed_on-Vercel-black?style=for-the-badge&logo=vercel" alt="Vercel" />
    <img src="https://img.shields.io/badge/License-MIT-pink?style=for-the-badge" alt="MIT License" />
  </p>
</div>

---

## 📖 Table of Contents

- [✨ Key Features](#-key-features)
- [🛠️ Tech Stack](#-tech-stack)
- [🏗️ System Architecture](#-system-architecture)
- [📁 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
- [⚙️ Environment Variables](#️-environment-variables)
- [🌐 Deployment](#-deployment)
- [📜 License](#-license)
- [👤 Author](#-author)

---

## ✨ Key Features

### 🛍️ Customer Storefront
- **Dynamic Hero Banner:** Custom pastel pink themed hero section featuring high-res product showcases and category promotions.
- **Instant Product Search:** Debounced keyword search with URL query synchronization for shareable product queries.
- **Categories Marquee:** Smooth infinite CSS animation showcasing product categories with seamless hover effects.
- **Redux Cart Management:** Real-time quantity adjustments, persistent client-side totals, and slide-in notifications via `react-hot-toast`.
- **Ratings & Reviews:** Interactive star-rating modal system allowing customers to submit and view product feedback.

### 🏪 Merchant & Seller Portal
- **Store Onboarding:** Multi-step seller registration with image upload preview and administrative approval workflow.
- **Product Management:** Dedicated portal to add, update, manage stock levels, and organize products by categories.
- **Order Tracking:** Real-time visibility into incoming orders, itemized receipts, and fulfillment status.

### 🛡️ Super Admin Management Panel
- **Store Approvals:** Verification pipeline to review and approve/reject new vendor applications.
- **Interactive Analytics:** Sales and order volume charts powered by Recharts with clean area visualizations.
- **Promotions & Coupons:** Administrative engine to generate, activate, and track custom discount codes.

### 🎨 Custom UI & Theming
- **Signature Pastel Theme:** Watercolor ambient pink palette (`#fdf0f4`), multi-point ambient radial aura, and responsive glassmorphism navigation.
- **High-Res Favicon & Branding:** Multi-resolution custom favicon (`favicon.ico` & `icon.png`) with dynamic App Router metadata.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Framework** | [Next.js 15.5](https://nextjs.org/) (App Router, Turbopack, Server-Side Rendering) |
| **Frontend Library** | [React 19](https://react.dev/) |
| **Styling** | [Tailwind CSS v4](https://tailwindcss.com/) & Glassmorphism |
| **State Management** | [Redux Toolkit](https://redux-toolkit.js.org/) (`cartSlice`, `productSlice`, `addressSlice`, `ratingSlice`) |
| **Database & ORM** | [Prisma ORM](https://www.prisma.io/) with Relational Data Schema |
| **Data Visualization** | [Recharts 3](https://recharts.org/) (Order & Sales Area Charts) |
| **Icons & Notifications** | [Lucide React](https://lucide.dev/), [React Hot Toast](https://react-hot-toast.com/) |
| **Deployment** | [Vercel](https://vercel.com/) (Serverless Architecture, Global CDN) |

---

## 📁 Project Structure

```bash
suga-cart.com/
├── app/
│   ├── (public)/              # Public customer-facing storefront routes
│   │   ├── cart/              # Shopping cart & checkout flow
│   │   ├── create-store/      # Merchant registration & onboarding
│   │   ├── product/[id]/      # Dynamic product detail pages
│   │   ├── shop/              # Product catalog & filterable search
│   │   └── page.jsx           # Main landing page
│   ├── admin/                 # Admin management & store verification
│   ├── store/                 # Merchant portal & product management
│   ├── globals.css            # Tailwind CSS v4 & custom pastel styling
│   ├── icon.png               # High-resolution browser favicon
│   └── layout.jsx             # Root layout, metadata & Redux StoreProvider
├── assets/                    # Optimized logos, models & media assets
├── components/                # Reusable UI component library
│   ├── admin/                 # Admin navbar, sidebar & statistics cards
│   ├── store/                 # Seller navigation & inventory tables
│   ├── Hero.jsx               # Hero banner with boy model & promo cards
│   ├── Navbar.jsx             # Sticky glassmorphism navigation bar
│   ├── Footer.jsx             # Footer with multi-column sitemap
│   └── ...                    # ProductCard, RatingModal, OrderSummary
├── lib/                       # Redux Toolkit store & feature slices
├── prisma/                    # Database schema definitions
└── public/                    # Static public assets
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js `v18.18+` or `v20+` (Node 24 tested)
- npm or yarn

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/shouryakumar246001/suga-cart.com.git
   cd suga-cart.com
   ```

2. **Install dependencies:**
   ```bash
   npm install --legacy-peer-deps
   ```

3. **Set up Environment Variables:**
   Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```

4. **Run the development server:**
   ```bash
   npm run dev
   ```

5. **Open in your browser:**
   Visit [http://localhost:3000](http://localhost:3000) to view the application.

---

## ⚙️ Environment Variables

Create a `.env` file in the root directory:

```env
# Currency Configuration
NEXT_PUBLIC_CURRENCY_SYMBOL='$'
```

---

## 🌐 Deployment

This application is optimized for deployment on **[Vercel](https://vercel.com/)**:

1. Push your code to your GitHub repository.
2. Import the repository in [Vercel Dashboard](https://vercel.com/new).
3. Set the Framework Preset to **Next.js**.
4. Click **Deploy**.

---

## 📜 License

This project is open-source and licensed under the [MIT License](./LICENSE.md).

---

## 👤 Author

**Shourya Kumar**
- GitHub: [@shouryakumar246001](https://github.com/shouryakumar246001)
- Project Repository: [suga-cart.com](https://github.com/shouryakumar246001/suga-cart.com)
