
## CRUD Application (FastAPI)

### Description:

I've created this project to test my **understanding** of the **FastAPI** (one of the python library). bellow are the step by step instructions to implement this project

### Folder Structrue:

/project_root

│── main.py                 [Main FastAPI application]

│── requirements.txt        [Optional: List of dependencies, libraires]

│── README.md               [Project documentation]

│── /venv                   [Virtual environment (optional)]


### Implementation:

1. Navigate to root folder and Create virtual environment using command: **py -m venv venv**
2. Install the required libraies, use command **pip install fastapi, uvicorn, sqlalchemy, pymysql**
3. create main.py file in root folder and follow the below steps:
    * **Line 9 :** create the db connecter link in the format: [mysql+pymysql://{db_username}:{db_password}@{db_host_addres}/{db_name}] 
    * **Line 11-13 :** setup session parameters
    * **Line 16-20 :** create table model (such models can be used to create the tables in databse using orm principles)
    * **Line 23 :** create the table in the database
    * **Line 26-37 :** create the validation clases(this will be used to validate the data passed at the endpoints)
    * **Line 40-48 :** initialize the FastAPI and create the db session (this will be used to interact with the database)
    * **Line 51-89 :** here will be creating the endpoints and the function associated with them.
4. Run the application with command **uvicorn main:app --reload**


### API Endpoints

| Method | Endpoint         | Description                |
|:------:|:----------------:|:--------------------------:|
| POST   | /items/          | create new item            |
| GET    | /items/          | retrive all items          |
| GET    | /items/{item_id} | retrive single item by id  |
| PUT    | /items/{item_id} | update the item by id      |
| DELETE | /items/{item_id} | delete the item by id      |
