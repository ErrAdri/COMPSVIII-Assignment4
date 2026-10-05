# My PHP Project

Base template for starting a PHP project, ready to open in PhpStorm.

## Structure

```
php-starter/
├── config/
│   └── config.php      # General configuration (app name, environment, errors)
├── src/
│   └── helpers.php     # Helper functions (e.g. HTML escaping)
├── public/
│   ├── index.php       # Entry point (document root)
│   └── assets/
│       └── style.css
└── README.md
```

## How to open it in PhpStorm

1. `File > Open` and select the `php-starter` folder.
2. Set up a PHP interpreter: `Settings > PHP > CLI Interpreter` (add one if you don't have it, pointing to your local PHP installation).
3. Mark the `public/` folder as the **Document Root**:
   - Right-click `public` > `Mark Directory as` > `Sources Root` (optional, for autocompletion).
4. Set up a development server:
   - `Run > Edit Configurations > + > PHP Built-in Web Server`
   - Document root: `public/`
   - Port: for example `8000`
5. Run it with the ▶ button, or start it manually:
```bash
   php -S localhost:8000 -t public
```
6. Open `http://localhost:8000` in your browser.

## What's included as an example

- POST form handling with simple validation.
- HTML output escaping (`e()`) to prevent XSS.
- Sessions (visit counter).
- Separation into `config/`, `src/` and `public/` so it's easy to scale.