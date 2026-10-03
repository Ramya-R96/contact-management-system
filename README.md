# Contact Management System

A simple Contact Management System built using **Node.js, Express.js, MongoDB, and Mongoose**.

## Technologies Used

* Node.js
* Express.js
* MongoDB
* Mongoose
* dotenv
* Nodemon

## Features

* Create a new contact
* View all contacts
* View a contact by ID
* Update contact details
* Delete a contact
* Validate phone number
* Validate email format
* Unique contact ID
* Unique email

## Contact Fields

| Field     | Type   | Validation                    |
| --------- | ------ | ----------------------------- |
| contactId | String | Required, Unique              |
| name      | String | Required                      |
| phone     | String | Required, 10 digits           |
| email     | String | Required, Unique, Valid email |

## Project Setup

### 1. Install Dependencies

```bash
npm install
```

### 2. Environment Variables

Create a `.env` file and add your MongoDB connection string:

```text
MONGO_URI=your_mongodb_connection_string
```

The database used is:

```text
contact_management
```

### 3. Start the Server

```bash
node src/server.js
```

Or use Nodemon:

```bash
npx nodemon src/server.js
```

The server runs on:

```text
http://localhost:3000
```

## API Endpoints

| Method | Endpoint        | Description          |
| ------ | --------------- | -------------------- |
| POST   | `/contacts`     | Create a new contact |
| GET    | `/contacts`     | Get all contacts     |
| GET    | `/contacts/:id` | Get contact by ID    |
| PUT    | `/contacts/:id` | Update contact       |
| DELETE | `/contacts/:id` | Delete contact       |

## 1. POST - Create Contact

**Endpoint:**

```text
POST /contacts
```

**Request Body:**

```json
{
  "contactId": "C007",
  "name": "Rahul",
  "phone": "9876543219",
  "email": "rahul@example.com"
}
```

**Response:**

```json
{
  "contactId": "C007",
  "name": "Rahul",
  "phone": "9876543219",
  "email": "rahul@example.com"
}
```

## 2. GET - Get All Contacts

**Endpoint:**

```text
GET /contacts
```

**Response:**

```json
[
  {
    "contactId": "C007", 
    "name": "Rahul",
    "phone": "9876543219",
    "email": "rahul@example.com"
  }
]
```

## 3. GET - Get Contact by ID

**Endpoint:**

```text
GET /contacts/:id
```

Example:

```text
GET /contacts/6ac105515b165745aa93105d
```

## 4. PUT - Update Contact

**Endpoint:**

```text
PUT /contacts/:id
```

**Request Body:**

```json
{
  "name": "Rahul Kumar",
  "phone": "9876543220",
  "email": "rahulkumar@example.com"
}
```

## 5. DELETE - Delete Contact

**Endpoint:**

```text
DELETE /contacts/:id
```

**Response:**

```json
{
  "message": "Contact deleted successfully"
}
```

## Validation

The application validates:

* Contact ID must be unique.
* Name is required.
* Phone number must contain exactly 10 digits.
* Email must be in a valid format.
* Email must be unique.

## Database

**Database:** `contact_management`

**Collection:** `contacts`

## CRUD Operations

* **POST → Create**
* **GET → Read**
* **PUT → Update**
* **DELETE → Delete**

## Project Structure

```text
my-project/
│
├── src/
│   ├── server.js
│   ├── models/
│   └── routes/
│
├── .env
├── .gitignore
├── package.json
├── package-lock.json
└── README.md
```

## Author

**Ramya R**

