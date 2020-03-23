# Flask API Template

## About

An API template written in Python that includes authentication using JSON web tokens and enables an authenticated user to create a store and add items to and delete items from the store.

## Deployed Link on Heroku

<https://flask-api-template-cn.herokuapp.com/>

## Technology Stack

- Flask
- SQLAlchemy
- PostgreSQL

## Testing Routes Using Postman

```javascript
// URL: https://flask-api-template-cn.herokuapp.com/register
// Type: POST
// Body:
{
  "username": "aUsername",
  "password": "aPassword"
}

// URL: https://flask-api-template-cn.herokuapp.com/auth
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

// URL: https://flask-api-template-cn.herokuapp.com/items
// Type: GET
// Returns an array of items

// URL: https://flask-api-template-cn.herokuapp.com/item/<name>
// Type: GET
// Returns data on specific item

// URL: https://flask-api-template-cn.herokuapp.com/item/<name>
// Type: POST
// Posts a new item to the store
// Body:
{
  "name": "exampleNameOfItem",
  "price": 9.99
}

// URL: https://flask-api-template-cn.herokuapp.com/item/<name>
// Type: DELETE
```

## Running App Locally

```shell
# Clone repo
git clone https://github.com/christophernajafi/flask-api-template

# Install packages
pip3 install flask flask-restful flask-jwt pyjwt flask_sqlalchemy

# Start app
python3 app.py
```

<!-- # Make sure PostgreSQL is running
# Create database called 'flask-api' -->
