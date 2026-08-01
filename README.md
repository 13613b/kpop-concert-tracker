# K-Pop Concert Tracker

K-Pop Concert Tracker is a web application for organizing past and upcoming K-Pop concerts. Users can save concert details and personal memories, edit existing entries, delete concerts and view saved concerts in a monthly calendar.

## Features

- Add concerts with artist, tour, city, country, date, ticket price and personal notes
- View all saved concerts and the total number of entries
- Edit existing concert entries
- Delete concerts after a confirmation prompt
- Display concerts in a monthly calendar
- Open concert details directly from the calendar
- Switch between light mode and dark mode
- Increase or decrease the font size
- Open KpopOfficial as an external source for K-Pop information
- Store concert data permanently in MongoDB Atlas
- Responsive layout for desktop and smaller screens

## Screenshots

Screenshots of the home page, concert form, concert overview and calendar will be added before submission.

## Technologies

### Frontend

- Angular
- TypeScript
- HTML
- CSS
- Angular Forms
- Angular HttpClient

### Backend

- Node.js
- Express
- Mongoose
- dotenv
- CORS

### Database

- MongoDB Atlas

## Project structure

```text
kpop-concert-tracker/
├── backend/
│   ├── .env.example
│   ├── package.json
│   └── server.js
├── frontend/
│   └── frontend-app/
│       ├── public/
│       ├── src/
│       ├── angular.json
│       └── package.json
└── README.md
```

## Prerequisites

The following software and services are required:

- Git
- Node.js and npm
- A free MongoDB Atlas account
- A MongoDB Atlas cluster and database user

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/13613b/kpop-concert-tracker.git
cd kpop-concert-tracker
```

### 2. Configure and start the backend

Open the backend directory and install its dependencies:

```bash
cd backend
npm install
```

Copy `.env.example` to a new file called `.env`. Paste the connection string provided by MongoDB Atlas and add `kpop_concert_tracker` as the database name:

```env
MONGODB_URI="PASTE_YOUR_MONGODB_ATLAS_CONNECTION_STRING_HERE"
PORT=3000
```

Replace the placeholder with the complete private connection string. The `.env` file contains private credentials and must never be committed to Git.

Make sure that the current IP address is included in the MongoDB Atlas IP access list. Then start the backend:

```bash
npm start
```

The successful start is shown by these messages:

```text
Connected to MongoDB
Server running on port 3000
```

If the database is empty, the backend automatically inserts two example concerts.

### 3. Install and start the frontend

Open a second terminal:

```bash
cd frontend/frontend-app
npm install
npm start
```

Open the application in a browser:

```text
http://localhost:4200
```

The backend must continue running in the first terminal while the application is used.

## Usage

### Add a concert

1. Open the home page.
2. Select **Add New Concert**.
3. Enter the concert information.
4. Select the date with the date picker so the concert can appear in the calendar.
5. Select **Add Concert**.

### View, edit or delete concerts

1. Open **My Concerts**.
2. Select **Edit** to change a concert and save the updated information.
3. Select **Delete** and confirm the prompt to remove a concert.

### Use the calendar

1. Open **My Calendar**.
2. Navigate between months with **Previous Month** and **Next Month**.
3. Select a concert inside a calendar day to view its details.

### Display settings

- Use the moon or sun button to switch between dark mode and light mode.
- Use **A-** and **A+** to adjust the font size.

## REST API

The backend runs on `http://localhost:3000` and provides these routes:

| Method | Route | Purpose |
| --- | --- | --- |
| GET | `/api/concerts` | Return all concerts |
| GET | `/api/concerts/:id` | Return one concert |
| POST | `/api/concerts` | Create a concert |
| PUT | `/api/concerts/:id` | Update a concert |
| DELETE | `/api/concerts/:id` | Delete a concert |

## Use of AI tools

- **ChatGPT / Codex:** Used for explanations, debugging support, improving responsive form layout, connecting the Node.js backend to MongoDB with Mongoose and structuring the project documentation.

All generated or suggested code was reviewed and tested as part of the project. The application code and its functionality must be explainable during the submission discussion.

## Possible future improvements

- Search and filter concerts
- Add concert status categories such as past, upcoming and dream concert
- Add image uploads with appropriately licensed images
- Add user registration and login
- Deploy the frontend and backend

## Author

Ela-Nur Kuyubasioglu, 2026
