
ChatGPT said:
ChatGPT
Flask Superheroes API Challenge
In this challenge, you'll develop an API for tracking superheroes and their powers.

Overview
This repo includes:

A Flask backend with some features already implemented.
A complete React frontend for testing the API.
Tests that can be run with pytest -x.
A Postman collection (challenge-2-superheroes.postman_collection.json) for testing your routes.
Setup
Navigate to the code-challenge folder in your code editor.

Install dependencies:

bash
Copy code
pipenv install
pipenv shell
npm install --prefix client
Start the Flask API:

bash
Copy code
python server/app.py
Access it at localhost:5555.

Start the React app:

bash
Copy code
npm start --prefix client
Access it at localhost:4000.

You only need to focus on the Flask API; the frontend is for testing.

Models
You'll implement an API with the following data model:

A Hero has many Powers through HeroPower.
A Power has many Heroes through HeroPower.
Use these commands to set up your database:

bash
Copy code
export FLASK_APP=server/app.py
flask db init
flask db upgrade head
Then, define the relationships in server/models.py and run migrations:

bash
Copy code
flask db revision --autogenerate -m 'message'
flask db upgrade head
python server/seed.py
Validations
Add these validations:

For HeroPower: strength must be 'Strong', 'Weak', or 'Average'.
For Power: description must be at least 20 characters long.
Routes
Implement the following routes:

GET /heroes
Returns a list of heroes.

GET /heroes/
Returns a specific hero or an error if not found.

GET /powers
Returns a list of powers.

GET /powers/
Returns a specific power or an error if not found.

PATCH /powers/
Updates an existing power, returning the updated power or validation errors.

POST /hero_powers
Creates a new HeroPower, returning the created object or validation errors.

Good luck, and happy coding!
