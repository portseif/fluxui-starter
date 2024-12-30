# FluxUI Starter (Laravel + Livewire + Flux)

A ready-to-use template for new projects leveraging [Laravel](https://laravel.com), [Livewire](https://laravel-livewire.com), and [Flux](https://github.com/livewire/flux) (aka FluxUI). Use this repository as a GitHub template to spin up new projects quickly with a preconfigured environment.

---

## Features

- **Laravel 10+**
  Modern PHP framework for fast, elegant web applications.
- **Livewire**
  Build dynamic interfaces using server-driven components.
- **Flux (FluxUI)**
  Streamlined frontend utilities integrated with Livewire.

---

## Requirements

- **PHP 8.1+** (with necessary extensions, e.g. `mbstring`, `openssl`, `pdo_mysql`)
- **Composer 2+**
- **Node.js 16+** and **npm 8+** (or **Yarn**)
- **Database** (MySQL, PostgreSQL, or SQLite)
- Local environment (e.g. [Laravel Herd](https://laravel.com/docs/master/valet) or Docker)

---

## Getting Started

1. **Clone or Use Template**
   - Click **Use this template** on GitHub to create a new repo, or clone/fork this repository.
   - If you use the template, you can skip the next step.
   ```bash
   git clone git@github.com:portseif/fluxui-starter.git
   cd fluxui-starter
   ```

2. **Install & Configure**
   ```bash
   composer install
   npm install
   cp .env.example .env
   php artisan key:generate
   php artisan migrate
   npm run dev
   php artisan serve
   ```
   - Update `.env` for database, mail, etc. as needed.

3. **Livewire Components**
   ```bash
   php artisan make:livewire ExampleComponent
   ```
   - Reference in a Blade file:
   ```blade
   <livewire:example-component />
   ```
# Tailwind Setup
- ## Tailwind Configuration (tailwind.config.js)
```js
module.exports = {
  content: [
    './resources/**/*.blade.php',
    './resources/**/*.js',
    './vendor/livewire/flux/**/*.blade.php',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

- ## Tailwind CSS (resources/css/app.css)
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

# Project Structure
```
fluxui-starter/
 ┣ app/
 ┃ ┣ Http/Controllers/
 ┃ ┣ Models/
 ┃ ┗ ...
 ┣ resources/
 ┃ ┣ css/
 ┃ ┣ js/
 ┃ ┗ views/
 ┣ public/
 ┣ vendor/
 ┣ composer.json
 ┣ package.json
 ┣ tailwind.config.js
 ┗ ...
```
---

# Contributing
1.	Fork this repository.
2.	Create a feature branch.
3.	Submit a pull request.

All contributions are welcome.

---

# License

This project is open-sourced under the MIT License - see the LICENSE file for details.
