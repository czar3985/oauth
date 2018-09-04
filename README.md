# OAuth2.0 for Restaurants
Working code for Authentication and Authorization

The restaurants application keeps a database of Restaurants and Menu Items for each restaurant.

## Prerequisites

    python 2.7.x
    sqlalchemy
    sqlite3
    flask
    database_setup.py
    project.py
    lotsofmenus.py
    Google developer account
    Facebook developer account

## Usage

Run **database_setup.py** to initialize the database.

Run **lotsofmenus.py** to populate the database with restaurants and menu items. (Optional)

Follow the steps in Google and Facebook developer consoles to create client ID and secret. 
Download the client secret JSON file from Google and save as **client_secrets.json** in the same folder as project.py.
Create an **fb_client_secrets.json** file and indicate the client ID and secret:

```json
{
    "web": {
        "app_id": "PLACE_CLIENT_ID_HERE",
        "app_secret": "PLACE_CLIENT_SECRET_HERE"
    }
}
```

Run **project.py** to run the Flask web server. 

In your browser visit **http://localhost:5000** to view the restaurant menu app.  

## Running Python Scripts

The following resource gives more information on how to run python scripts: How to Run a Python Script via a File or the Shell.

## URLs

restaurants page: http://localhost:5000/restaurant/

menu page for each restaurant ID in the server PC Ex: http://localhost:5000/restaurant/1/

## Database Structure

```
Table Name: restaurant
Columns:
{'primary_key': 0, 'nullable': False, 'default': None, 'autoincrement': 'auto', 'type': VARCHAR(length=250), 'name': u'name'}
{'primary_key': 1, 'nullable': False, 'default': None, 'autoincrement': 'auto', 'type': INTEGER(), 'name': u'id'}

Table Name: menu_item
Columns:
{'primary_key': 0, 'nullable': False, 'default': None, 'autoincrement': 'auto', 'type': VARCHAR(length=80), 'name': u'name'}
{'primary_key': 1, 'nullable': False, 'default': None, 'autoincrement': 'auto', 'type': INTEGER(), 'name': u'id'}
{'primary_key': 0, 'nullable': True, 'default': None, 'autoincrement': 'auto', 'type': VARCHAR(length=250), 'name': u'description'}
{'primary_key': 0, 'nullable': True, 'default': None, 'autoincrement': 'auto', 'type': VARCHAR(length=8), 'name': u'price'}
{'primary_key': 0, 'nullable': True, 'default': None, 'autoincrement': 'auto', 'type': VARCHAR(length=250), 'name': u'course'}
{'primary_key': 0, 'nullable': True, 'default': None, 'autoincrement': 'auto', 'type': INTEGER(), 'name': u'restaurant_id'}
```

## Features

    View restaurants in the database
    Edit a restaurant
    Delete a restaurant
    Add restaurants
    View menu entries for each restaurant in the database
    Create a new menu item for each restaurant
    Update a menu item
    Delete a menu item from the database
    Search for restaurants or food
    Make use of JSON API endpoints for a list of restaurants, menus for each restaurant and specific menu item
    Logins and user checking using Google OAuth
    TBD: Facebook login

Ex.

http://localhost:5000/restaurant/JSON,

http://localhost:5000/restaurant/1/menu/JSON,

http://localhost:5000/restaurant/1/menu/1/JSON