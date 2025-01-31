This repository consolidates four different activities related to API development using FastAPI. Each folder represents a different activity, focusing on various aspects of API creation, logic building, and implementation.
Folder Structure
lab1-main/
lab2-main/
lab3-main/
lab4-main/
Each folder contains the corresponding codebase for a specific activity. Below is a description of each activity and its purpose.

Activity 1: Factorial APIObjectivesIntroduce FastAPI as a technology stack for developing APIs.

Review Python as a programming language for API development.
Create, run, and test APIs using FastAPI.
Practice logic building and technical expertise through coding.
DescriptionIn this activity, we developed an API using FastAPI that calculates the factorial of a given number. The API follows these requirements:
Endpoint: /factorial/{starting_number}
Logic:
Computes the factorial of the input value.
If the input value is 0, the endpoint returns { "result": false }.
The computation is implemented using a while loop.
Example UsageRequest:GET /factorial/5Response:{
  "result": 120
}Edge Case:GET /factorial/0Response:{
  "result": false
}The implementation ensures efficient calculation while demonstrating fundamental API development concepts in FastAPI.


Activity 2: To-Do List APIObjectivesIdentify and differentiate different ways to parameterize an API.


Discuss HTTP methods and their uses based on best practices.
Use HTTP methods and parameters to create a simple CRUD simulation API.
DescriptionIn this activity, we developed a To-Do List API using FastAPI. The API follows these specifications:
Initial Data on API Run:
task_db = [
    {"task_id": 1, "task_title": "Laboratory Activity", "task_desc": "Create Lab Act 2", "is_finished": False}
]Endpoints:
GET /tasks/{task_id} - Retrieve a specific task by its ID.
POST /tasks - Add a new task to the list.
PATCH /tasks/{task_id} - Update an existing task.
DELETE /tasks/{task_id} - Remove a task from the list.
Response Format:
Successful transactions return { "status": "ok" }.
Errors return { "error": <error_message> }.
Validations:
Ensure no null values.
Prevent negative numbers.
Handle invalid inputs such as division by zero.
This activity highlights proper API parameterization, HTTP method usage, and best practices for building a CRUD-based API.

Activity 3: JSON Handling APIObjectivesFamiliarize and identify JSON as a primary data format for API development.


Parse JSON strings and traverse data in the JSON string using Python.
Convert Python data structures into a valid JSON format.
DescriptionIn this activity, we developed an API using FastAPI that retrieves user posts and their respective comments using JSON data. The API follows these specifications:
Prerequisites:
Clone the repository: GitHub Repository
Navigate to the lab3 folder.
Create a virtual environment and install the required dependencies.
Endpoint:
GET /detailed_post/{userID} - Retrieves all posts for a given user along with their comments.
Functionality:
Given a userID, the API fetches all posts by that user.
Each post includes all associated comments.
Uses appropriate key names based on the data being outputted.
Sample Output:
Refer to the expected_output.json file in the repository for the expected structure.
Required Output:
GitHub repository containing:
Updated main.py with the implemented API.
Optional requirements.txt file for dependencies.
This activity emphasizes handling JSON data, parsing it efficiently, and structuring responses in a clear and organized manner.

Activity 4: API Versioning, Authentication, and Error HandlingObjectivesImplement versioning, authentication, and proper HTTP exception handling in API development.

Implement best practices in handling environment variables.
DescriptionThis activity extends the To-Do List API from Activity 2 by adding API versioning, authentication, and error handling. The API follows these specifications:
Versioning:
The first version is named apiv1.
The updated version is named apiv2.
Error Handling:
If accessing a task that does not exist → Return 404 Not Found.
If deleting a task that does not exist → Return 404 Not Found.
If updating a task that does not exist → Return 404 Not Found.
If a task is successfully added → Return 201 Created.
If a task is successfully updated → Return 204 No Content.
If a task is successfully deleted → Return 204 No Content.
If there are no tasks available → Return 204 No Content.
All other unspecified cases return 200 OK.
API Authentication:
An API key is required for accessing the endpoints.
The API key is stored in a .env file and loaded into the application.
The .env file should not be included in the repository.
A .gitignore file is added to prevent accidental inclusion of .env.
Required Output:GitHub repository containing:
Updated API with versioning, authentication, and error handling.
.gitignore file including .env.
API key (to be shared via private message, not included in the repository).
Example format: LAB4_API_KEY=my_api_key (ensure the variable matches the implementation).
This activity focuses on best practices for securing and maintaining APIs in a professional development environment.
Setup InstructionsTo run any of the activities, follow these steps:
Install dependencies:
pip install fastapi uvicorn python-dotenvNavigate to the respective activity folder.
Run the FastAPI server:
uvicorn main:app --reloadAccess the API documentation at:
http://127.0.0.1:8000/docsEach activity folder contains its respective main.py file, which should be executed accordingly.
