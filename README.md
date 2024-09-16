
# Sharp CMS

Welcome to **Sharp CMS**, a powerful and flexible starter project designed to help developers quickly build admin dashboards or content management systems (CMS) using Laravel and Filament. This kit is optimized for scalability, ease of use, and modern web development practices.

## Features

- **Laravel 10**: Robust backend framework with MVC architecture.
- **Filament**: Lightweight and user-friendly admin panel system.
- **Tailwind CSS**: Utility-first CSS framework for fast UI development.
- **Livewire**: Simplified dynamic UIs without the need for heavy JavaScript.
- **Alpine.js**: Lightweight JavaScript framework for minimal reactivity.
- **Authentication**: Out-of-the-box authentication with Laravel Breeze (optional).
- **REST API (Optional)**: Easily extendable API using Laravel Sanctum.

## Prerequisites

Make sure you have the following installed on your local machine:

- PHP 8.1+
- Composer
- Node.js (with npm or Yarn)
- MySQL or PostgreSQL (or any supported database)
- A web server like Apache or Nginx (or use Laravel's built-in server)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ekmillard/sharp-cms.git
   cd sharp-cms
   ```

2. **Install dependencies:**

   Run the following commands to install PHP and Node dependencies:

   ```bash
   composer install
   npm install
   ```

3. **Set up environment variables:**

   Copy the `.env.example` file to create your `.env` file:

   ```bash
   cp .env.example .env
   ```

   Update your `.env` file with the correct database credentials and other application-specific settings.

4. **Generate an application key:**

   ```bash
   php artisan key:generate
   ```

5. **Run migrations:**

   Set up your database tables by running migrations:

   ```bash
   php artisan migrate
   ```

6. **Compile assets:**

   Use Laravel Mix to compile Tailwind CSS and other assets:

   ```bash
   npm run dev
   ```

7. **Serve the application:**

   Start the Laravel development server:

   ```bash
   php artisan serve
   ```

   Your application will now be running at [http://localhost:8000](http://localhost:8000).

## Admin Panel

The admin panel is powered by Filament and can be accessed at `/admin`. After completing the installation, you can set up an admin user by running the following command:

```bash
php artisan make:filament-user
```

Follow the prompt to create an admin account.

## Folder Structure

- `app/` - Core application files.
- `resources/views/` - Blade views for frontend and admin panel.
- `resources/css/` - Tailwind CSS styles.
- `resources/js/` - Alpine.js scripts.
- `routes/web.php` - Web routes, including the admin routes.
- `routes/api.php` - API routes.
- `config/filament.php` - Filament configuration.
- `public/` - Compiled CSS and JS files.
- `database/migrations/` - Database schema and migration files.

## Customization

### Authentication

- **Breeze** is installed by default for lightweight user authentication.
- You can customize user authentication by editing the views in `resources/views/auth/` and routes in `routes/web.php`.

### API (Optional)

This project can be extended to include an API with Laravel Sanctum for authentication. You can add your API routes in `routes/api.php`.

### Admin Resources

Filament makes it easy to create admin resources such as CRUD (Create, Read, Update, Delete) interfaces. Use the following command to create a new resource:

```bash
php artisan make:filament-resource ModelName
```

This will generate a resource to manage your model directly from the admin panel.

## Frontend Customization

The frontend is powered by **Tailwind CSS** and **Alpine.js** for dynamic components. You can customize your layouts and pages in `resources/views/`.

### Tailwind CSS

Tailwind's configuration can be adjusted in `tailwind.config.js`. Styles can be written in `resources/css/app.css` or inline in your Blade templates.

### Alpine.js

You can add interactive components with Alpine.js by including scripts in `resources/js/app.js`.

## Contributing

If you want to contribute to the project, feel free to fork the repository, make changes, and submit a pull request. We welcome all contributions to improve **Sharp CMS**.

## License

This project is open-source and available under the [MIT License](LICENSE).

## Support

For any issues or questions, please open an issue on the repository or contact the project maintainers.
