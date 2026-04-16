# Auction Search Backend API

A backend API project built with **Node.js**, **Express**, **MongoDB**, and **Mongoose** to manage auction listing data in a local development environment.

This project focuses on backend fundamentals such as database connection setup, schema modeling, seed and clear scripts, and a keyword-based search endpoint for auction listings.

## Overview

The API supports a simple auction-style data workflow by allowing local auction data to be stored, reset, and searched through MongoDB.

This project was a good exercise in:
- structuring an Express backend
- connecting Node.js to MongoDB
- designing a Mongoose model
- creating local database utility scripts
- building and testing an API search route
- documenting project setup and usage clearly

## Features

- MongoDB database connection setup
- Auction listing schema using Mongoose
- Seed script to insert sample auction data
- Clear script to remove auction data
- Search API endpoint for keyword-based lookup
- Search checks both title and description fields
- Local development workflow with environment variables
- Evidence folder showing build progress and testing

## Tech Stack

- **Node.js**
- **Express**
- **MongoDB**
- **Mongoose**
- **JavaScript**
- **Postman**
- **dotenv**

## Project Structure

~~~text
m5-p1/
├── backend/
├── evidence/
├── README.md
├── MISSION.md
└── .gitignore
~~~

## Search Endpoint

### GET `/api/auctions/search?q=keyword`

Searches auction listings by keyword using MongoDB.

The endpoint checks:
- `title`
- `description`

### Example

~~~text
GET /api/auctions/search?q=toyota
~~~

Example browser or Postman request:

~~~text
http://localhost:5000/api/auctions/search?q=toyota
~~~

## Local Setup

### 1. Install dependencies

~~~bash
npm install
~~~

### 2. Create a `.env` file

~~~env
MONGO_URI=your_connection_string_here
~~~

### 3. Start the development server

~~~bash
npm run dev
~~~

## Utility Scripts

### Seed sample data

~~~bash
npm run seed
~~~

This resets the auction collection and inserts sample auction documents.

### Clear all data

~~~bash
npm run clear
~~~

This removes all auction documents from the collection.

## Example Workflow

1. Start MongoDB connection
2. Seed the database with sample auction data
3. Run the backend server
4. Test the search endpoint in the browser or Postman
5. Review returned auction results from MongoDB

## Evidence

The `evidence/` folder contains screenshots showing:
- local MongoDB setup
- database connection
- project structure
- seeded data
- API testing
- search endpoint testing

## What I Practiced

Through this project, I practiced:

- backend project setup
- Express route structure
- MongoDB integration
- Mongoose model creation
- local CLI workflow design
- API testing and documentation
- organizing a backend repo clearly for review

## Notes

This repo represents a backend-focused project and is intended as a portfolio piece showing practical experience with **Express APIs**, **MongoDB workflows**, and **search-based endpoint design** in a local development setup.
