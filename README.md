# compilation_lab
 
# LAB1
This project is about using FastAPI, a tool that helps us build and run APIs using Python. The goal is to learn how to create an API, test it, and improve coding skills. 
This API calculates the factorial of a number, which means multiplying all whole numbers from that number down to 1.  
The code starts by importing FastAPI and setting up an API application using app = FastAPI(). 
It creates a GET request endpoint, @app.get("/factorial/{starting_number}"), where {starting_number} is replaced by any number provided by the user. 
The function factorial(starting_number: int) does the actual math. If the number is 0, the API responds with { "result": False }. 
Otherwise, it calculates the factorial using a while loop that keeps multiplying numbers until it reaches 1, and then it returns the result in a JSON format. 
To use the API, first install FastAPI and Uvicorn by running pip install fastapi uvicorn, then save the script as main.py and start the server with uvicorn main:app --reload. 
You can test it by going to http://127.0.0.1:8000/factorial/5, which should return { "starting_number": 5, "factorial": 120 }. 
FastAPI also provides built-in testing pages, which you can access at Swagger UI (http://127.0.0.1:8000/docs) or Redoc UI (http://127.0.0.1:8000/redoc). 
This API is a simple yet powerful way to understand how FastAPI works and practice Python skills while building something useful.

# LAB2
This project builds a To-Do List API using FastAPI, focusing on API parameterization, HTTP methods, and CRUD operations. 
The API includes endpoints for retrieving (GET /tasks/{task_id}), creating (POST /tasks), updating (PATCH /tasks/{task_id}), and deleting (DELETE /tasks/{task_id}) tasks. 
Each endpoint returns { "status": "ok" } for success or { "error": <error message> } for issues, ensuring data integrity. 
The TaskDB class manages task operations, while FastAPI handles API requests. 
To run, install FastAPI and Uvicorn, save the script, and start the server with uvicorn main:app --reload. 
Test via http://127.0.0.1:8000/docs (Swagger UI) or http://127.0.0.1:8000/redoc.

# LAB3
This project builds a Detailed Post API using FastAPI, designed to retrieve user-specific posts and their corresponding comments in JSON format. 
The API helps in understanding JSON as a primary data format, parsing JSON strings, and converting Python data structures into valid JSON. 
It includes a GET /detailed_post/{userID} endpoint that, given a userID, fetches all posts by that user along with comments for each post. 
The API ensures proper key-value structuring for clarity and usability. 
To implement this, FastAPI processes the request, retrieves the relevant data, and returns a structured JSON response. 
Running this API follows the same steps as other FastAPI projects: install dependencies, save the script, and start the server using Uvicorn. 
The API can be tested through http://127.0.0.1:8000/docs (Swagger UI) or http://127.0.0.1:8000/redoc, making it a practical exercise in handling JSON data in Python.

# LAB4
This code is a FastAPI application that manages tasks in a to-do list. 
The tasks are stored in memory, with each task having a unique ID, name, details, and completion status. 
The code provides multiple endpoints to interact with tasks: viewing a specific task, listing all tasks, adding a new task, updating an existing task, modifying parts of a task, and deleting a task. 
It includes error handling, like returning a "404 Not Found" error when a task doesn't exist, and proper success codes like "201 Created" for adding tasks, "204 No Content" for updates or deletions, and "200 OK" for general success. 
Additionally, the app uses an API key stored in an environment file (.env) to authenticate requests and prevent unauthorized access, and it ensures that the .env file is kept secure by adding it to a .gitignore file. 
The code also handles situations like when there are no tasks to show, returning a "204 No Content" status.

# LAB5
The objective is to take the API you developed in Laboratory Activity #4 which includes task management features like adding, updating, and deleting tasks, with authentication and versioning and deploy it to a cloud platform called Render. 
Render is a cloud platform that allows you to easily host web applications, APIs, and databases. 
In simpler terms, you need to upload your API code to Render so it can be accessed online by anyone, just like how websites are hosted on the internet. 
This deployment process will allow your FastAPI app to run continuously on Render, making it publicly available without needing to keep your own computer running the app.
