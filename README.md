# MPCMS — Cooperative Management System

A web-based Cooperative Management System built with **Laravel** (PHP) and **Tailwind CSS**, hosted via GitHub Pages at [mpcms.me](https://mpcms.me).

---

## How to Upload Your VS Code Project Files to This Repository

Follow these steps to push all your project files from VS Code to this GitHub repository.

### Prerequisites

- [Git](https://git-scm.com/downloads) installed on your computer
- [VS Code](https://code.visualstudio.com/) with the built-in **Source Control** panel
- A GitHub account with access to this repository

---

### Option A — Using VS Code's Built-in Git UI

1. **Open your project folder** in VS Code (`File → Open Folder`).
2. Click the **Source Control icon** in the left sidebar (or press `Ctrl+Shift+G`).
3. If the folder is not yet a Git repository, click **"Initialize Repository"**.
4. **Stage all files** by clicking the **+** next to *Changes* (or individual files).
5. Enter a **commit message** in the text box (e.g. `Add project files`).
6. Click the **✓ Commit** button.
7. Click **"Publish Branch"** (or **"Push"**) to upload to GitHub.
   - If prompted, sign in to GitHub and authorize VS Code.

---

### Option B — Using the Terminal Inside VS Code

Open the integrated terminal in VS Code (`` Ctrl+` `` or `View → Terminal`) and run:

```bash
# 1. Navigate to your project folder (if not already there)
cd /path/to/your/project

# 2. Initialize a Git repository (skip if already initialized)
git init

# 3. Connect to this GitHub repository
git remote add origin https://github.com/RichterP-sys/RichterP-sys.github.io.git

# 4. Stage all files
git add .

# 5. Create your first commit
git commit -m "Add project files"

# 6. Push to GitHub
git push -u origin main
```

> **Tip:** If your default branch is named `master` instead of `main`, replace `main` with `master` in the last command.

---

### What Gets Ignored

A `.gitignore` file is already configured to exclude files that should **not** be committed:

| Excluded | Reason |
|---|---|
| `vendor/` | PHP dependencies — run `composer install` locally |
| `node_modules/` | JS dependencies — run `npm install` locally |
| `.env` | Contains secrets (database passwords, API keys) |
| `storage/*.key` | Application encryption keys |

---

### Recommended VS Code Extensions

A `.vscode/extensions.json` file is included. When you open this project in VS Code, it will suggest installing:

- **PHP Intelephense** — PHP code intelligence
- **Laravel Blade Snippets** — Blade template support
- **Tailwind CSS IntelliSense** — Autocomplete for Tailwind classes
- **Prettier** — Code formatting
- **Live Server** — Preview HTML files in the browser

---

## Local Development Setup

```bash
# Install PHP dependencies
composer install

# Install JS dependencies
npm install

# Copy environment file and generate app key
cp .env.example .env
php artisan key:generate

# Run database migrations
php artisan migrate

# Start development server
php artisan serve
```

Then visit `http://localhost:8000` in your browser.

---

## License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
