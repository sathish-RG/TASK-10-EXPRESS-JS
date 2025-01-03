# Recipe Management Application

This is a simple CRUD (Create, Read, Update, Delete) application for managing recipes, built using **Node.js**, **Express.js**, and **Mongoose**. It follows the **MVC (Model-View-Controller)** architecture and integrates with **MongoDB** for data storage.

---

## Features
- Create a new recipe
- Retrieve all recipes
- Retrieve a recipe by ID
- Update a recipe by ID
- Delete a recipe by ID
- Proper error handling and validation

---

## Technologies Used
- **Node.js**: JavaScript runtime environment.
- **Express.js**: Web application framework for Node.js.
- **Mongoose**: ODM library for MongoDB.
- **MongoDB**: NoSQL database for storing recipes.
- **Postman**: For API testing and documentation.

---

## Installation and Setup

### Prerequisites
- Install [Node.js](https://nodejs.org/).
- Install [MongoDB](https://www.mongodb.com/).

### Steps
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd recipe-manager
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add the following variables:
     ```env
     MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/recipes
     PORT=3000
     ```

4. Start the server:
   ```bash
   npm run dev
   ```

5. The application will run on [http://localhost:3000](http://localhost:3000).

---

## API Endpoints

### Base URL
`https://task-10-express-js.onrender.com/api/recipes`

### Endpoints

#### 1. Create a Recipe
- **Method**: `POST`
- **URL**: `/`
- **Request Body**:
  ```json
  {
      "title": "Spaghetti Carbonara",
      "ingredients": "Spaghetti, Eggs, Parmesan Cheese, Pancetta, Black Pepper, Salt",
      "instructions": "1. Cook spaghetti according to package instructions. 2. In a bowl, whisk eggs and Parmesan. 3. In a pan, cook pancetta until crispy. 4. Add cooked spaghetti to the pan and mix well. 5. Remove from heat and quickly stir in the egg mixture to create a creamy sauce. 6. Season with black pepper and salt to taste. Serve immediately."
  }
- **Response**: Created recipe object.

#### 2. Get All Recipes
- **Method**: `GET`
- **URL**: `/`
- **Response**: List of all recipes.

#### 3. Get Recipe by ID
- **Method**: `GET`
- **URL**: `/:id`
- **Response**: Recipe object with the specified ID.

#### 4. Update a Recipe by ID
- **Method**: `PUT`
- **URL**: `/:id`
- **Request Body**: Any fields to update (e.g., `title`, `ingredients`, `instructions`).
- **Response**: Updated recipe object.

#### 5. Delete a Recipe by ID
- **Method**: `DELETE`
- **URL**: `/:id`
- **Response**: Success message.

---

## Error Handling
The application handles errors such as:
- Invalid or missing fields.
- Non-existent recipe IDs.
- Server errors.

All errors are returned as JSON responses with appropriate HTTP status codes.

---

## Postman Documentation
A Postman collection is provided to test all API endpoints. Import the collection to Postman and start testing.

---

## Folder Structure
```
project/
├── controllers/
│   └── recipeController.js
├── models/
│   └── Recipe.js
├── routes/
│   └── recipeRoutes.js
├── config/
│   └── database.js
├── app.js
├── package.json
└── README.md
```

---

## Future Improvements
- Add user authentication (e.g., JWT).
- Include pagination for large recipe lists.
- Enhance validations using libraries like `express-validator`.
- Add support for file uploads (e.g., recipe images).

---

## License
This project is open-source and available under the [MIT License](LICENSE).
