# Full-Stack Web Development Setup on Fedora

This guide outlines the essential tools and software you should install on your Fedora system to set up a full-stack web development environment. It covers frontend, backend, databases, containerization, version control, and other useful utilities for development.


## 1. Essential System Tools

### Git
Git is a version control system for managing source code.

```bash
sudo dnf install git
```

### Curl & Wget
These tools are used to download files or interact with APIs from the command line.

```bash
sudo dnf install curl wget
```

### Text Editors
Install your preferred text editor for quick edits in the terminal.

```bash
sudo dnf install vim
```

Or install **Nano** or **Emacs** if preferred.

## 2. Frontend Development

### Node.js & npm
Node.js is a JavaScript runtime used in frontend development. **npm** is the Node package manager.

```bash
sudo dnf install nodejs
```

To manage packages, **Yarn** is an alternative to npm:

```bash
npm install -g yarn
```

### Frameworks & CLIs

- **React CLI**:
    ```bash
    npm install -g create-react-app
    ```

- **Vue CLI**:
    ```bash
    npm install -g @vue/cli
    ```

- **Angular CLI**:
    ```bash
    npm install -g @angular/cli
    ```

### Code Quality Tools

- **Prettier** (Code formatter):
    ```bash
    npm install -g prettier
    ```

- **ESLint** (Linter for JavaScript):
    ```bash
    npm install -g eslint
    ```

### Build Tools

- **Webpack** (Module bundler):
    ```bash
    npm install -g webpack webpack-cli
    ```

- **Babel** (JavaScript compiler):
    ```bash
    npm install -g @babel/cli @babel/preset-env
    ```

## 3. Backend Development

### Python

Install Python for backend frameworks like Django or Flask:

```bash
sudo dnf install python3
```

To create isolated environments, use **Virtualenv**:

```bash
pip3 install virtualenv
```

### Ruby & Rails

For Ruby on Rails development:

```bash
sudo dnf install ruby
gem install rails
```

### PHP

For PHP-based backend frameworks (e.g., Laravel, WordPress):

```bash
sudo dnf install php php-cli php-fpm
```

### Go (Golang)

For Go-based backend development:

```bash
sudo dnf install golang
```

### Java

For backend development with Java (e.g., Spring Boot):

```bash
sudo dnf install java-17-openjdk
```

### Docker

Docker simplifies deployment by using containers:

```bash
sudo dnf install docker
sudo systemctl start docker
sudo systemctl enable docker
```

Also, install **Docker Compose** for multi-container setups:

```bash
sudo dnf install docker-compose
```

### Web Servers

Install Nginx or Apache for web server deployment:

- **Nginx**:
    ```bash
    sudo dnf install nginx
    ```

- **Apache**:
    ```bash
    sudo dnf install httpd
    ```

## 4. Databases

### MySQL / MariaDB

For relational databases like MySQL or MariaDB:

```bash
sudo dnf install mysql-server
sudo systemctl start mysqld
sudo systemctl enable mysqld
```

### PostgreSQL

For relational databases with advanced features:

```bash
sudo dnf install postgresql-server
sudo postgresql-setup --initdb
sudo systemctl start postgresql
sudo systemctl enable postgresql
```

### MongoDB

For NoSQL databases (document-based):

```bash
sudo dnf install mongodb-server
sudo systemctl start mongod
sudo systemctl enable mongod
```

### SQLite

A lightweight SQL database for smaller projects:

```bash
sudo dnf install sqlite
```

## 5. APIs & Other Services

### GraphQL

If you are working with GraphQL APIs, you can use Apollo Server:

```bash
npm install apollo-server
```

### Redis

For caching and message brokering:

```bash
sudo dnf install redis
sudo systemctl start redis
sudo systemctl enable redis
```

## 6. Development Tools

### Postman / Insomnia

For testing and debugging APIs:

- Install Postman (via Flatpak):
    ```bash
    flatpak install flathub com.getpostman.Postman
    ```

### Visual Studio Code

A popular code editor for full-stack development:

```bash
flatpak install flathub com.visualstudio.code
```

### JetBrains IDEs

For a full-featured IDE, you can use JetBrains tools like **WebStorm** or **PhpStorm**.

## 7. Testing Frameworks

### Jest

A testing framework for JavaScript:

```bash
npm install --save-dev jest
```

### Mocha / Chai

For Node.js testing:

```bash
npm install --save-dev mocha chai
```

### Cypress / Selenium

For end-to-end testing:

```bash
npm install --save-dev cypress
```

## 8. Version Management Tools

### NVM (Node Version Manager)

To manage multiple Node.js versions:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

### RVM (Ruby Version Manager)

For managing multiple Ruby versions:

```bash
sudo dnf install gcc libyaml-devel libffi-devel
\curl -sSL https://get.rvm.io | bash -s stable
```

## 9. Other Useful Tools

### Zsh & Oh My Zsh

A better terminal shell with plugins and themes:

```bash
sudo dnf install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Tmux

A terminal multiplexer for working with multiple terminal sessions:

```bash
sudo dnf install tmux
```

## 10. Containerization & Virtualization Tools

### Podman

A Docker alternative for managing containers:

```bash
sudo dnf install podman
```

### Kubernetes (Minikube)

For local Kubernetes clusters:

```bash
sudo dnf install minikube
```
