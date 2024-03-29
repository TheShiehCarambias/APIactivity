# CRUD API
Inserts, extracts, updates and deletes data from the database


## API DESCRIPTION

The API serves as an interface for interacting with a MySQL database named "demo." It provides endpoints to perform the following operations on a table called "names":

Insert new records with first names and last names.
Retrieve existing records from the table.
Update records based on their unique identifiers.
Delete records by their unique identifiers.

 
## API ENDPOINTS

Endpoint: /postName

HTTP Method: POST

Functionality: This endpoint is used to insert first name (fname) and last name (lname) into a MySQL database named "demo." The endpoint expects a JSON payload in the request body, containing the fname and lname fields. It then inserts this data into the "names" table in the database.

Required Parameters:

fname: The first name to be inserted into the database.
lname: The last name to be inserted into the database.


Endpoint: /getName
HTTP Method: GET
Functionality: This endpoint is used to extract or read data from MySQL database named "demo". 
Required Parameters: No required parameters.

Endpoint: /updateName
HTTP Method: POST
Functionality: This endpoint is used to update data from MySQL database named "demo". 
Required Parameters:

id: the unique identifiers of data
fname: The update of the first name in the database.
lname: The update of the last name in the database.

Endpoint: /deleteName
HTTP Method: GET
Functionality: This endpoint is used to delete data from MySQL database named "demo". 
Required Parameters: 
id: The ID number to be deleted in the database.

## Request
Endpoint: /postName
 {
  "fname": "manny",
  "lname": "hortizuela"
}

Structure 
"fname" (First Name): This field represents the first name of the individual whose data you want to insert into the database. In the example payload, it's set to "manny."
"lname" (Last Name): This field represents the last name of the individual. In the example payload, it's set to "hortizuela."

Endpoint: /getName
No required request payload

Endpoint: /updateName
{
  "id":1,
  "lname":"wick",
   "fname":"john"
}
Structure 
"id": the unique identifier of the data to be updated
"fname" (First Name): This field represents the first name of the individual whose data you want to update in the database. In the example payload, it's set to "manny."
"lname" (Last Name): This field represents the last name of the individual. In the example payload, it's set to "hortizuela."


Endpoint: /deleteName
{
  "id":1
}

Structure 
"id": the unique identifier of the data to be deleted



## Response
JSON Payload postName:
{
         "status":"success","data":null
}

JSON Response Structure:
"status": Indicates the status of the operation, either "success" or "error."
"data": An optional field that may contain additional information or data. In the case of a successful operation, this field is set to null.
Possible Status Codes:
"status": "success" if the operation was successful.
"status": "error" if there was an issue during the operation.

JSON Payload getName:
Response payload:
{
         "status":"success","data":["lname":"hortizuela","fname":"manny","lname":"licayan","fname":"arnold"]
}

JSON Response Structure:
"status": Indicates the status of the operation, either "success" or "error."
"data": An array containing the retrieved data. If no data is found, it can be an empty array.
Possible Status Codes:
"status": "success" if the operation was successful.
"status": "error" if there was an issue during the operation.

JSON Payload updateName:
Response payload:
{
         "status":"success","data":null
}


JSON Response Structure:
"status": Indicates the status of the operation, either "success" or "error."
"data": An optional field that may contain additional information or data. In the case of a successful operation, this field is set to null.
Possible Status Codes:
"status": "success" if the operation was successful.
"status": "error" if there was an issue during the operation.

JSON Payload deleteName:
Response payload:
{
         "status":"success","data":null
}

JSON Response Structure:
"status": Indicates the status of the operation, either "success" or "error."
"data": An optional field that may contain additional information or data. In the case of a successful operation, this field is set to null.
Possible Status Codes:
"status": "success" if the operation was successful.
"status": "error" if there was an issue during the operation.


## Usage
1. Open Xampp
2. Create a database demo
3. Create a database table
4. Create columns named fname and lname
5. Create a folder named api inside the htdocs folder in your xampp.
6. Create a folder named public inside the api folder.
7. Create your php file consists of your API Endpoints(postName, getName, updateName, deleteName)
8. Save your file in a folder named public.
9. Enter your Endpoints in the postman
10. Set the HTTP method to be used
11. Write a request payload.


## License
Open source license



## Contributors
Manny R. Hortizuela



## Contact
For queries, contact me @carambiasshieh4@gmail.com
