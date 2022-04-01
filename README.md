# Floor Finder

## How to start the project

- Step 1: install [node.js](https://nodejs.org/en/download/)
- Step 2: `npm install`

## How to start the Express server

- Step 1: `npm start`
- Step 2: Open web browser and enter http://localhost:3000 to check the server status

## How to install MySQL

### For macOS

install mysql using Homebrew: `brew install mysql` then follow the instructions from brew

### For Windows

[MySQL Installer](https://dev.mysql.com/downloads/installer/)

## How to create a database in MySQL and a dev user

- Step 1: login MySQL from terminal: `mysql -uroot -p`
- Step 2: create a floor_finder database: `CREATE DATABASE floor_finder;`
- Step 3: creat a new user account: `CREATE USER ‘dev’@’localhost’ IDENTIFIED BY ‘your_password_here’;`
- Step 4: grant global privileges to a dev user connecting via localhost `GRANT ALL ON floor_finder.\* TO 'dev'@'localhost'`;

**_Now the database is ready to use._**

## Data setup

- Step 1: set up db password environment variable: `export DB_PASSWORD=your_password_here`
- Step 2: set up tables: `npm run mysql:setup`
- Step 3: populate the data using the web scraper

## How to run the web scraper

`npm run fetch`

## How to run linting

`npm run lint`

## API Example

### Search office

- Search with keyword `Academic`: `http://localhost:3000/api/search?keyword=Academic&start=0&size=10`