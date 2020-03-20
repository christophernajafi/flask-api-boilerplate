# Flask API Template

## About

An API template written in Python that includes authentication using JSON web tokens and enables an authenticated user to create a store and add items to and delete items from the store.

## Deployed Link on Heroku

<https://flask-api-cn.herokuapp.com/>

## Technology Stack

- Flask
- SQLAlchemy
- PostgreSQL

## Testing Routes Using Postman

```json
// Endpoints
/register
/login
/logout

/stores
/store/<string:name>
/items
/item/<string:name>
/user/<int:user_id>
/refresh
```

## Running App Locally

```shell
# Clone repo
git clone https://github.com/christophernajafi/flask-api-template

# Install packages
pip3 install flask flask-restful flask-jwt pyjwt flask-jwt-extended flask_sqlalchemy

# Run app locally
python3 app.py
```

<!-- # Make sure PostgreSQL is running
# Create database called 'flask-api' -->
