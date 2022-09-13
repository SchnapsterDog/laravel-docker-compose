# Set-up Laravel Docker Compose 

Based on https://github.com/aschmelyun/docker-compose-laravel.git

A pretty simplified Docker Compose workflow that sets up a LEMP network of containers for local Laravel development.

## ❔ What you need to run the Nginx Docker Container locally?

### Windows Users
- 👉 [Installed Docker Desktop](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe)
- 👉 [Enabled WSL 2 feature on Windows](https://docs.docker.com/desktop/windows/wsl/)
- 👉 [Download and install the Linux kernel update package](https://docs.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)

---

## ⚙ Installation

### Project setup for Windows Users

Only once:
- open ubuntu app on windows
- clone the project
- navigate to the project folder
- copy .env.example file to .env
- `docker compose run --rm composer install`
- `docker compose build`
- `docker-compose run --rm artisan key:generate`

Run the project locally
- `docker compose up`

#### Composer dump autoload
- `docker-compose run --rm composer dump-autoload`

#### Run Migration
- `docker-compose run --rm artisan migrate`

#### Compiling front-end files
- `docker-compose run --rm npm run dev`
