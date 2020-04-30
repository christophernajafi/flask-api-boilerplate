# Flask API Boilerplate

## About

An API written in Python using the Flask framework that authenticates using JSON web tokens and enables a user to create a store and add items to and delete items from the store.

## Deployed Link on Heroku

<https://flask-api-boilerplate-cn.herokuapp.com/>

## Technology Stack

- Flask
- SQLAlchemy
- PostgreSQL

## Testing Routes Using Postman

```javascript
// URL: https://flask-api-boilerplate-cn.herokuapp.com/register
// Type: POST
// Body:
{
  "username": "aUsername",
  "password": "aPassword"
}

// URL: https://flask-api-boilerplate-cn.herokuapp.com/auth
// Type: POST
// Returns jwt token
// Body:
{
  "username": "aUsername",
  "password": "aPassword"
}
// Tests:
const jsonData = JSON.parse(responseBody);
tests["Access token was not empty."] = jsonData.access_token !== undefined;
postman.setEnvironmentVariable("jwt_token", jsonData.access_token);

// URL: https://flask-api-boilerplate-cn.herokuapp.com/stores
// Type: GET
// Returns an array of stores

// URL: https://flask-api-boilerplate-cn.herokuapp.com/store/<name>
// Type: POST
// Add a store

// URL: https://flask-api-boilerplate-cn.herokuapp.com/store/<name>
// Type: GET
// Returns data on a specific store

// URL: https://flask-api-boilerplate-cn.herokuapp.com/store/<name>
// Type: DELETE
// Delete a specific store

// URL: https://flask-api-boilerplate-cn.herokuapp.com/items
// Type: GET
// Returns an array of items

// URL: https://flask-api-boilerplate-cn.herokuapp.com/item/<name>
// Type: POST
// Adds a new item to the store
// Body:
{
  "name": "exampleNameOfItem",
  "price": 9.99,
  "store_id": 1
}

// URL: https://flask-api-boilerplate-cn.herokuapp.com/item/<name>
// Type: GET
// Returns data on a specific item

// URL: https://flask-api-boilerplate-cn.herokuapp.com/item/<name>
// Type: PUT
// Updates data on a specific item

// URL: https://flask-api-boilerplate-cn.herokuapp.com/item/<name>
// Type: DELETE
// Deletes a specific item
```

## Running App Locally

```shell
# Clone repo
git clone https://github.com/christophernajafi/flask-api-boilerplate.git

# Change directory
cd flask-api-boilerplate

# Install packages
pip3 install flask flask-restful flask-jwt pyjwt flask_sqlalchemy

# Start app
python3 app.py
```
