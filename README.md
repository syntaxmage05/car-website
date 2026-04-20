https://github.com/user-attachments/assets/bd921052-8d25-41da-ad7b-5e02ec028d93

<div id="top">

<!-- HEADER STYLE: CLASSIC -->
<div align="center">

# CAR-WEBSITE

<em>Drive Your Journey with Confidence and Style</em>

<!-- BADGES -->
<img src="https://img.shields.io/github/last-commit/syntaxmage05/car-website?style=flat&logo=git&logoColor=white&color=0080ff" alt="last-commit">
<img src="https://img.shields.io/github/languages/top/syntaxmage05/car-website?style=flat&color=0080ff" alt="repo-top-language">
<img src="https://img.shields.io/github/languages/count/syntaxmage05/car-website?style=flat&color=0080ff" alt="repo-language-count">

<em>Built with the tools and technologies:</em>

<img src="https://img.shields.io/badge/Ruby-CC342D.svg?style=flat&logo=Ruby&logoColor=white" alt="Ruby">
<img src="https://img.shields.io/badge/Rails-CC0000.svg?style=flat&logo=Ruby-on-Rails&logoColor=white" alt="Rails">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=flat&logo=PostgreSQL&logoColor=white" alt="PostgreSQL">
<img src="https://img.shields.io/badge/Hotwire-FF5F1F.svg?style=flat&logo=hotwire&logoColor=white" alt="Hotwire">
<img src="https://img.shields.io/badge/Stimulus-77E8B9.svg?style=flat&logo=stimulus&logoColor=black" alt="Stimulus">
<br>
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4.svg?style=flat&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
<img src="https://img.shields.io/badge/esbuild-FFCF00.svg?style=flat&logo=esbuild&logoColor=black" alt="esbuild">
<img src="https://img.shields.io/badge/Docker-2496ED.svg?style=flat&logo=Docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?style=flat&logo=GitHub-Actions&logoColor=white" alt="GitHub Actions">

</div>
<br>

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Quick Start (Local Development)](#quick-start-local-development)
  - [Running with Docker](#running-with-docker)
- [Testing & Code Quality](#testing--code-quality)
- [Environment Variables](#environment-variables)
- [Deployment](#deployment)

---

## Overview

`car-website` is a Rails 8 application for showcasing, managing, and selling vehicles online. It includes an admin workflow for inventory management and a public-facing storefront where visitors can browse listings, compare cars, and send enquiries.

---

## Features

- 🚗 Inventory management for makes, models, and cars.
- 🖼️ Multiple image uploads per car using Active Storage.
- 🔐 Authentication and role-based authorization (Devise + Rolify + Pundit).
- 🧭 Public catalog with filters and detailed vehicle pages.
- ⚡ Modern Rails frontend stack with Hotwire, Stimulus, and Tailwind.
- 📦 Docker-ready deployment flow and CI-friendly project layout.

---

## Tech Stack

- **Backend:** Ruby on Rails 8
- **Database:** PostgreSQL
- **Frontend:** Hotwire (Turbo + Stimulus), Tailwind CSS, esbuild
- **Auth / Access Control:** Devise, Rolify, Pundit
- **Background Infrastructure:** Solid Queue, Solid Cache, Solid Cable
- **Deployment:** Docker + Kamal

---

## Getting Started

### Prerequisites

Install the following tools before running locally:

- Ruby (compatible with the app's Gemfile / lockfile)
- Bundler
- PostgreSQL
- Node.js + npm or yarn

### Quick Start (Local Development)

1. **Clone the repository**

   ```sh
   git clone https://github.com/syntaxmage05/car-website.git
   cd car-website
   ```

2. **Install dependencies**

   ```sh
   bundle install
   yarn install
   ```

3. **Set up the database**

   ```sh
   bin/rails db:create
   bin/rails db:migrate
   # Optional: load seed data
   bin/rails db:seed
   ```

4. **Start the development server**

   ```sh
   bin/dev
   ```

5. Open your browser at:

   ```text
   http://localhost:3000
   ```

### Running with Docker

Build and run the project in a container:

```sh
docker build -t car-website .
docker run --rm -p 3000:3000 car-website
```

---

## Testing & Code Quality

Run the default Rails test suite:

```sh
bin/rails test
```

Run security and lint checks (if configured in your environment):

```sh
bin/brakeman
bin/rubocop
```

---

## Environment Variables

You can configure optional integrations through environment variables (for example WhatsApp contact settings used for enquiries):

```env
WHATSAPP_PHONE=1234567890
```

For production, set required secrets using Rails credentials and your deployment environment.

---

## Deployment

This app includes Kamal configuration at `config/deploy.yml`. Typical deployment workflow:

```sh
bin/kamal setup
bin/kamal deploy
```

Review and customize `config/deploy.yml` before deploying.

---

<div align="left"><a href="#top">⬆ Return</a></div>

---
