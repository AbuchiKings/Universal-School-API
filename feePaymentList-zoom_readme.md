# Fee Payment Lis & Zoom

# Description
This documentation is about the fees payment list and zoom meetings features of the universal school system application.

## API Features
This API consists of the features indicated below:

### Fee Payment List
* This API is for maintaining a record of student who have paid their fees in a given term.
* A school administartor can create the school payment list.
* A school administrator can edit or delete from school payment list.
* School administartor and staff can view the school payment list.

### Zoom
* Staff and Admin can make use of this feature.
* Users must activate their account befor using.
* Users can create account on zoom and carry out other CRUD operations on their accounts.
* A user account can be deleted by the user or a school administrator or an admin.
* Account deletion from non account owners does not delete account permanently from zoom, it simply disassociates the account.
* Users can create, update, retrieve and update a meeting.
* Only the creator of a meeting, Schoo-admininstrator or app admin can delete a meeting.


| Endpoint                                                            | Function                                                            |
| --------------------------------------------------------------------| --------------------------------------------------------------------|
| POST/api/v1/schools/:id/fees/list                                   | Creates a fee payment list                                          |
| GET/api/v1/schools/:id/fees/list                                    | Retrieves the fee payment list of a given school                    |
| PATCH/api/v1/schools/:id/fees/list/:list_id                         | Adds a payment record to fee payment list                           |
| DELETE/api/v1/schools/:id/fees/list/:list_id                        | Deletes a fee payment list                                          |
| DELETE/api/v1/schools/:id/fees/list/:list_id/student/student_id     | Deletes a specific student from the fee payment list                |
| POST/api/v1/schools/:id/meetings/users                              | Creates a new user on zoom                                          |
| GET/api/v1/schools/:id/meetings/users                               | Retrieves all zoom registered user on the app                       |
| GET/api/v1/schools/:id/meetings/users/:user_id                      | Retrieves a specific user from zoom                                 |
| GET/api/v1/schools/:id/meetings/local/users                         | Retrieves users from app's database                                |
| DELETE/api/v1/schools/:id/meetings/users/:user_id                   | Deletes or disassociates user account                               |
| POST/api/v1/schools/:id/users/:user_id/meetings                     | Creates a meeting                                                   |
| POST/api/v1/schools/:id/users/:user_id/lectures                     | Creates a lecture for a particular class                            |
| GET/api/v1/schools/:id/meetings/:meeting_id                         | Retrieves a zoom meeting                                            |
| GET/api/v1/schools/:id/lectures/:lecture_id                         | Retrieves a specific zoom lecture                                   |
| GET/api/v1/schools/:id/meetings                                     | Retrieves all meetings                                              |
| GET/api/v1/schools/:id/lectures                                     | Retrieves all lectures                                              |
| PATCH/api/v1/schools/:id/meetings/:meeting_id                       | Updates a meeting                                                   |
| PATCH/api/v1/schools/:id/lectures/:lecture_id                       | Updates a lecture                                                   |
| PATCH/api/v1/schools/:id/lectures/:lecture_id/attendance            | Updates a lecture attendance list                                   |
| DELETE/api/v1/schools/:id/meetings/:meeting_id                      | Deltes a meeting                                                    |
| DELETE/api/v1/schools/:id/lectures/:lecture_id                      | Deltes a lecture                                                    |
| PATCH/api/v1/schools/:id/meetings/:meeting_id/end                   | Ends a meeting                                                      |
| PATCH/api/v1/schools/:id/lectures/:lecture_id/end                   | Ends a lecture                                                      | 


### Sample Requests and Responses From The API

- [Fee Payment List](#fee-payment-list)
    - [Create Fee Payment List](#create-fee-payment-list)
    - [Retrieve Fee Payment List](#retrieve-fee-payment-list)
    - [Update Fee Payment List](#update-fee-payment-list)
    - [Delete Fee Payment List](#delete-fee-payment-list)
    - [Delete Fee Payment List Item](#delete-fee-payment-list-item)

- [Zoom](#zoom)
    - [Create User](#create-user)
    - [Retrieve User](#retrieve-user)
    - [Retrieve Users](#retrieve-users)
    - [Retrieve Users Local](#retrieve-users-local)
    - [Delete User](#delete-user)
    - [Create Meeting](#create-meeting)
    - [Create Lecture](#create-lecture)
    - [Retrieve Meeting](#retrieve-meeting)
    - [Retrieve Meetings](#retrieve-meetings)
    - [Retrieve Lecture](#retrieve-lecture)
    - [Retrieve Lectures](#retrieve-lectures)
    - [Update Meeting](#update-meeting)
    - [Update Lecture](#update-lecture)
    - [Update Lecture Attendance](#update-lecture-attendance)
    - [Delete Meeting](#delete-meeting)
    - [Delete Lecture](#delete-lecture)
    - [End Meeting](#end-meeting)
    - [End Lecture](#end-lecture)


###  Fee Payment List

### Create Fee Payment List
* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/fees/list
    * Body: (application/json)
    ``` {
            "term": 1
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Fees payment list was created successfully",
            "results": 1,
            "data": {
                "paymentsIn": "Naira",
                "_id": "5f062f85aa103f0848cf5e41",
                "term": 1,
                "createdOn": "2020-07-08T20:41:41.000Z",
                "school": "5ecb08dfd2595416f0dc9977",
                "year": "2020",
                "paidList": [],
                "__v": 0
            }
        }
    ```


### Retrieve Fee Payment List

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/fees/list

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
           "status": "success",
            "message": "Fees Payment list retrieved successfully",
            "results": 1,
            "data": [
                {
                    "_id": "5f06111fb568e500bcd46951",
                    "paymentsIn": "Naira",
                    "term": 2,
                    "createdOn": "2020-07-08T18:31:59.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "year": "2020",
                    "paidList": [
                        {
                            "_id": "5f0612c5b568e500bcd46952",
                            "student": "5ecb1917ef9ab21050ca1f7b",
                            "class": "Basic 2",
                            "amount": 300000,
                            "paidOn": "2020-10-31T23:00:00.000Z"
                        },
                        {
                            "_id": "5f06135bb568e500bcd46954",
                            "student": "5ecb1918ef9ab21050ca1f7d",
                            "class": "Basic 1",
                            "amount": 300000,
                            "paidOn": "2020-01-24T23:00:00.000Z"
                        },
                        {
                            "_id": "5f061411b568e500bcd46956",
                            "student": "5ecb1918ef9ab21050ca1f7e",
                            "class": "SS 1",
                            "amount": 350000,
                            "paidOn": "2020-07-04T00:00:00.000Z"
                        }
                    ],
                    "__v": 0
                }
            ]
        }
    ```


### Update Fee Payment List
* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/fees/list/5f062f85aa103f0848cf5e41
    * Body: (application/json)
    ```
        {       
            "paidList": { 
                "student":"5ecb1918ef9ab21050ca1f7e",
                "class": "SS 1",
                "amount": 350000,
                "paidOn": "2020-07-04"
            }
        }
    ```

* Response
    * Status: 200 - OK
    * Body: application/json

    ``` {
           "status": "success",
            "message": "Fees Payment list retrieved successfully",
            "results": 1,
            "data": [
                {
                    "_id": "5f06111fb568e500bcd46951",
                    "paymentsIn": "Naira",
                    "term": 2,
                    "createdOn": "2020-07-08T18:31:59.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "year": "2020",
                    "paidList": [
                        {
                            "_id": "5f0612c5b568e500bcd46952",
                            "student": "5ecb1917ef9ab21050ca1f7b",
                            "class": "Basic 2",
                            "amount": 300000,
                            "paidOn": "2020-10-31T23:00:00.000Z"
                        },
                        {
                            "_id": "5f06135bb568e500bcd46954",
                            "student": "5ecb1918ef9ab21050ca1f7d",
                            "class": "Basic 1",
                            "amount": 300000,
                            "paidOn": "2020-01-24T23:00:00.000Z"
                        },
                        {
                            "_id": "5f061411b568e500bcd46956",
                            "student": "5ecb1918ef9ab21050ca1f7e",
                            "class": "SS 1",
                            "amount": 350000,
                            "paidOn": "2020-07-04T00:00:00.000Z"
                        }
                    ],
                    "__v": 0
                }
            ]
        }
    ```

### Delete Fee Payment List
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9979/fees/list/5f0613b4b568e500bcd46955

* Response:
    * Status: 204 - No content


### Delete Fee Payment List Item
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/fees/list/5f062f85aa103f0848cf5e41/student/5ecb1918ef9ab21050ca1f7a

* Response:
    * Status: 204 -  No content 


### Zoom

### Create User
* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/users
    * Body: (application/json)
    ``` {
            "email": "abuchi@mail.com",
            "type": 2,
            "first_name": "Abuchi",
            "last_name": "Kings"
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
            "status": "success",
            "message": "You have been successfully registered. Please check your email",
            "data": {
                "_id": "5f074b336b31991d784c57a9",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "user": "5f010459d9994c2308ac5757",
                "name": "Abuchi Ndinigwe",
                "email": "abuchi@mail.com",
                "type": 1,
                "category": "Admin",
                "createdOn": "2020-07-09T16:52:02.000Z",
                "__v": 0
            }
        }
    ```


### Retrieve User

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/users/5f010459d9994c2308ac5757

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "User was successfuly retrieved",
            "results": 1,
            "data": {
                "id": "q7dxbi9JRzuAepiGZ8sP5w",
                "first_name": "Abuchi",
                "last_name": "Ndinigwe",
                "email": "abuchikings@hotmail.com",
                "type": 1,
                "role_name": "Member",
                "pmi": 4157326842,
                "use_pmi": false,
                "personal_meeting_url": "https://us02web.zoom.us/j/4157326842?pwd=R0FkSkZFVmd2dFJ3NWl3aXY5NFFhQT09",
                "timezone": "",
                "verified": 1,
                "dept": "",
                "created_at": "2020-07-09T17:01:34Z",
                "last_login_time": "2020-07-09T17:01:34Z",
                "host_key": "498814",
                "jid": "q7dxbi9jrzuaepigz8sp5w@xmpp.zoom.us",
                "group_ids": [],
                "im_group_ids": [],
                "account_id": "yfDysesBScekzFp8JoYPEg",
                "language": "en-US",
                "phone_country": "",
                "phone_number": "",
                "status": "active",
                "job_title": "",
                "location": ""
            }
        }
    ```

### Retrieve Users

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/users

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Users successfuly retrieved",
            "results": 1,
            "data": {
                "page_count": 1,
                "page_number": 1,
                "page_size": 20,
                "total_records": 2,
                "users": [
                    {
                        "id": "UndNPm3NSMCfEXsB5s8Wwg",
                        "first_name": "Olufemi",
                        "last_name": "Aghe",
                        "email": "olufemiaghe@gmail.com",
                        "type": 2,
                        "pmi": 8171037187,
                        "timezone": "Africa/Bangui",
                        "verified": 1,
                        "created_at": "2020-04-23T09:05:38Z",
                        "last_login_time": "2020-07-08T11:11:27Z",
                        "pic_url": "https://lh5.googleusercontent.com/-9qEAUO-R434/AI/AAA...",
                        "language": "en-US",
                        "phone_number": "",
                        "status": "active"
                    },
                    {
                        "id": "q7dxbi9JRzuAepiGZ8sP5w",
                        "first_name": "Abuchi",
                        "last_name": "Ndinigwe",
                        "email": "abuchikings@hotmail.com",
                        "type": 1,
                        "pmi": 4157326842,
                        "timezone": "",
                        "verified": 1,
                        "created_at": "2020-07-09T17:01:34Z",
                        "last_login_time": "2020-07-09T17:01:34Z",
                        "language": "en-US",
                        "status": "active"
                    }
                ]
            }
        }
    ```

### Retrieve Users Local

* Request:
    * Endpoint: GET//api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/users

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Users was successfuly retrieved",
            "results": 1,
            "data": [
                {
                    "_id": "5ee94dbaa0d73f22cc6d7dce",
                    "userId": "IEGcDC3LQai_UQ9Sc_Z6kw",
                    "user": "5ecb18d0ef9ab21050ca1f1f",
                    "name": "Abuchi Ndinigwe",
                    "email": "abuchikings@hotmail.com",
                    "type": 1,
                    "category": "Admin",
                    "createdOn": "2020-06-16T22:54:50.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "__v": 0
                },
                ...
            ]
        }
    ```

### Delete User
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/users/5f010459d9994c2308ac5757

* Response:
    * Status: 204 -  No content


### Create Meeting

* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/users/5f010459d9994c2308ac5757/meetings
    * Body: (application/json)
    ``` {
            "topic": "Staff meeting",
            "type": "2",
            "start_time": "2020-07-19T12:02:00Z",
            "password":"qwerty123",
            "duration": "30",
            "agenda": "Discussion on upcoming inter-house sports",
            "recipients":["Staff", "Stapent"],
            "fields":{
                "term": "1",
                "year": "2020"
            },
            "settings": {
              "host_video": "true",
              "participant_video": "false",
              "join_before_host": "true",
              "mute_upon_entry": "true",
              "watermark": "false",
              "use_pmi": "true",
              "approval_type": "0",
              "audio": "both",
              "auto_recording": "local"
            }
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
             "status": "success",
            "message": "Meeting was created successfully",
            "results": 1,
            "data": {
                "_id": "5f0d5896cb572109fcc7eab2",
                "recipients": [
                    "Staff",
                    "Stapent"
                ],
                "term": 1,
                "year": "2020",
                "school": "5ecb08dfd2595416f0dc9977",
                "staff": "5f010459d9994c2308ac5757",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "__v": 0,
                "agenda": "Discussion on upcoming inter-house sports",
                "created_at": "2020-07-14T07:02:39Z",
                "duration": 30,
                "id": "86036785303",
                "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                "password": "qwerty123",
                "start_time": "2020-07-19T12:02:00Z",
                "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.        eyJhdWQiOiJjbGllbnQiLCJ1aWQiOiJxN2R4Ymk5SlJ6dUFlcGlHWjhzUDV3IiwiaXNzIjoid2ViIiwic3R5IjoxMD",
                "topic": "Staff meeting"
            }
        }
    ```


### Create Lecture

* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/users/5f010459d9994c2308ac5757/lectures
    * Body: (application/json)
    ``` {
            "topic": "The rise of the Roman Empire",
            "type": "2",
            "start_time": "2020-06-19T14:02:00Z",
            "password":"qwerty123",
            "duration": "30",
            "agenda": "Discussions on viscosity and suface tension",
            "fields":{
                "class": "SS3",
                "term": "2",
                "year": "2020",
                "subject": "history"
            },
            "settings": {
              "host_video": "true",
              "participant_video": "false",
              "join_before_host": "true",
              "mute_upon_entry": "true",
              "watermark": "false",
              "use_pmi": "true",
              "approval_type": "0",
              "audio": "both",
              "auto_recording": "local"
            }
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
             "status": "success",
            "message": "Meeting was created successfully",
            "results": 1,
            "data": {
                "_id": "5f0d58abcb572109fcc7eab3",
                "attendance": [],
                "class": "SS3",
                "term": 2,
                "year": "2020",
                "subject": "history",
                "school": "5ecb08dfd2595416f0dc9977",
                "staff": "5f010459d9994c2308ac5757",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "__v": 0,
                "agenda": "Discussions on lorem ipsum",
                "created_at": "2020-07-14T07:02:59Z",
                "duration": 30,
                "id": "87575300200",
                "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                "password": "qwerty123",
                "start_time": "2020-06-19T14:02:00Z",
                "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLCJ1aWQiOiJxN24Ymk5S...",
                "topic": "The rise of the Roman Empire"
            }
        }
    ```

### Retrieve Meeting

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/5f0d5896cb572109fcc7eab2

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Retrieved successfully",
            "results": 1,
            "data": {
                "_id": "5f0d5896cb572109fcc7eab2",
                "recipients": [
                    "Staff",
                    "Stapent"
                ],
                "term": 1,
                "year": "2020",
                "school": "5ecb08dfd2595416f0dc9977",
                "staff": "5f010459d9994c2308ac5757",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "__v": 0,
                "agenda": "Discussion on upcoming inter-house sports",
                "created_at": "2020-07-14T07:02:39Z",
                "duration": 30,
                "id": "86036785303",
                "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                "password": "qwerty123",
                "start_time": "2020-07-19T12:02:00Z",
                "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLCJ1aWQiOiJxN2R4Y...",
                "topic": "Staff meeting"
            }
        }
    ```

### Retrieve Meetings

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Retrieved successfully",
            "results": 1,
            "data": [
                {
                    "_id": "5f0d5896cb572109fcc7eab2",
                    "recipients": [
                        "Staff",
                        "Stapent"
                    ],
                    "term": 1,
                    "year": "2020",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "staff": "5f010459d9994c2308ac5757",
                    "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                    "__v": 0,
                    "agenda": "Discussion on upcoming inter-house sports",
                    "created_at": "2020-07-14T07:02:39Z",
                    "duration": 30,
                    "id": "86036785303",
                    "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                    "password": "qwerty123",
                    "start_time": "2020-07-19T12:02:00Z",
                    "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.        eyJhdWQiOiJjbGllbnQiLCJ1aWQiOiJxN2R4Ymk5SlJ6dUFlcGlHWjhzUD...",
                    "topic": "Staff meeting"
                },
                ...
            ]
        }
    ```

### Retrieve Lecture

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/lectures/5f0d58abcb572109fcc7eab3

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Retrieved successfully",
            "results": 1,
            "data": {
                "_id": "5f0d58abcb572109fcc7eab3",
                "attendance": [],
                "class": "SS3",
                "term": 2,
                "year": "2020",
                "subject": "history",
                "school": "5ecb08dfd2595416f0dc9977",
                "staff": "5f010459d9994c2308ac5757",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "__v": 0,
                "agenda": "Discussions on lorem ipsum...",
                "created_at": "2020-07-14T07:02:59Z",
                "duration": 30,
                "id": "87575300200",
                "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                "password": "qwerty123",
                "start_time": "2020-06-19T14:02:00Z",
                "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXdWQiOiJjbGllbnQiLCJ1aWQiOiJxN2R4Ymk5S...",
                "topic": "The rise of the Roman Empire"
            }
        }
    ```

### Retrieve Lectures

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/lectures

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Retrieved successfully",
            "results": 3,
            "data": [
                {
                    "_id": "5eea6a686c98871ed4feabfe",
                    "attendance": [
                        "amandababatunde68",
                        "esthermonday5",
                        "iniobongokeke1",
                        "amaraatanda14"
                    ],
                    "class": "SS2",
                    "term": 2,
                    "year": "2020",
                    "subject": "chemistry",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "staff": "5ecb18d0ef9ab21050ca1f1f",
                    "userId": "IEGcDC3LQai_UQ9Sc_Z6kw",
                    "__v": 2,
                    "agenda": "Discussion on energy changes in exothermic and endothermic reactions, Laws of Thermodynamics",
                    "created_at": "2020-06-17T19:09:17Z",
                    "duration": 30,
                    "id": "84047439162",
                    "join_url": "https://us02web.zoom.us/j/6590467167",
                    "password": null,
                    "start_time": "2020-06-18T13:02:00Z",
                    "start_url": "https://us02web.zoom.us/s/6590467167?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLC...",
                    "topic": "Energy and Chemical Reactions"
                },
                {
                    "_id": "5eea6ad06c98871ed4feabff",
                    "attendance": [],
                    "class": "SS1",
                    "term": 1,
                    "year": "2020",
                    "subject": "biology",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "staff": "5ecb18d0ef9ab21050ca1f1f",
                    "userId": "IEGcDC3LQai_UQ9Sc_Z6kw",
                    "__v": 0,
                    "agenda": "Discussion on asexual reproductions as seen in unicellular organisms like Amoeba, Paramecium and Chlamydomonas",
                    "created_at": "2020-06-17T19:11:01Z",
                    "duration": 30,
                    "id": "87305682904",
                    "join_url": "https://us02web.zoom.us/j/6590467167",
                    "password": null,
                    "start_time": "2020-06-19T10:02:00Z",
                    "start_url": "https://us02web.zoom.us/s/6590467167?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLCJ1ak...",
                    "topic": "Asexual reproduction in microbes"
                }
            ]
        }
    ```

### Update Meeting
* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/5f0d5896cb572109fcc7eab2
    * NB: Update to meeting details on the database is made by a webhook events so response won't reflect change
    * Body: (application/json)
    ```
        {       
            "start_time": "2020-08-21T16:00:334Z",
            "duration": 53,
            "password": "abcde32",
            "settings": {
              "mute_upon_entry": false
            },
              "fields":{
                "term": "3"
            }
        }
    ```

* Response
    * Status: 200 - OK
    * Body: application/json

    ``` {
           "status": "success",
            "message": "Updated successfully",
            "results": 1,
            "data": {
                "_id": "5f0d5896cb572109fcc7eab2",
                "recipients": [
                    "Staff",
                    "Stapent"
                ],
                "term": 3,
                "year": "2020",
                "school": "5ecb08dfd2595416f0dc9977",
                "staff": "5f010459d9994c2308ac5757",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "__v": 0,
                "agenda": "Discussion on upcoming inter-house sports",
                "created_at": "2020-07-14T07:02:39Z",
                "duration": 30,
                "id": "86036785303",
                "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                "password": "qwerty123",
                "start_time": "2020-07-19T12:02:00Z",
                "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLCJ1aW...",
                "topic": "Staff meeting"
            }
        }
    ```

### Update Lecture
* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/lectures/5f0d58abcb572109fcc7eab3
    * NB: Update to meeting details on the database is made by a webhook events so response won't reflect change
    * Body: (application/json)
    ```
        {       
            "start_time": "2020-08-21T16:00:334Z",
            "duration": 53,
            "password": "abdd123",
            "settings": {
              "mute_upon_entry": false
            },
              "fields":{
                "class": "SS2",
                "term": "3"
            }
        }
    ```

* Response
    * Status: 200 - OK
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Updated successfully",
            "results": 1,
            "data": {
                "_id": "5f0d58abcb572109fcc7eab3",
                "attendance": [],
                "class": "SS2",
                "term": 3,
                "year": "2020",
                "subject": "history",
                "school": "5ecb08dfd2595416f0dc9977",
                "staff": "5f010459d9994c2308ac5757",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "__v": 0,
                "agenda": "Discussions on viscosity and suface tension",
                "created_at": "2020-07-14T07:02:59Z",
                "duration": 30,
                "id": "87575300200",
                "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                "password": "qwerty123",
                "start_time": "2020-06-19T14:02:00Z",
                "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLCJ1aWQiO...",
                "topic": "The rise of the Roman Empire"
            }
        }
    ```

### Update Lecture Attendance
* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/lectures/5f0d5896cb572109fcc7eab2
    * Body: (application/json)
    ```
        {       
            "attendance": ["amandababatunde68", "amakemohammed72", "wasiuedet9" ]
        }
    ```

* Response
    * Status: 200 - OK
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Successfully updated",
            "results": 1,
            "data": {
                "_id": "5f0d58abcb572109fcc7eab3",
                "attendance": [
                    "amandababatunde68",
                    "amakemohammed72",
                    "wasiuedet9"
                ],
                "class": "SS2",
                "term": 3,
                "year": "2020",
                "subject": "history",
                "school": "5ecb08dfd2595416f0dc9977",
                "staff": "5f010459d9994c2308ac5757",
                "userId": "q7dxbi9JRzuAepiGZ8sP5w",
                "__v": 0,
                "agenda": "Discussions on viscosity and suface tension",
                "created_at": "2020-07-14T07:02:59Z",
                "duration": 30,
                "id": "87575300200",
                "join_url": "https://us02web.zoom.us/j/4157326842?pwd=TUpyNzFYOUVIdlNHME5jMjFkeVlEUT09",
                "password": "qwerty123",
                "start_time": "2020-06-19T14:02:00Z",
                "start_url": "https://us02web.zoom.us/s/4157326842?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbn...",
                "topic": "The rise of the Roman Empire"
            }
        }
    ```

### Delete Meeting
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/meetings/5f0b6c19bf974e0b245c59b3/users/5f010459d9994c2308ac5757

* Response:
    * Status: 204 -  No content

### Delete Lecture
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/lectures/5f0b6c19bf974e0b245c59b3/users/5f010459d9994c2308ac5757

* Response:
    * Status: 204 -  No content


### End Meeting
* Request:
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/lectures/5f0b6c19bf974e0b245c59b3/users/5f010459d9994c2308ac5757
    * Body: (application/json)
    ```
        {       
            "action": "end"
        }
    ```

* Response:
    * Status: 204 -  No content


### End Lecture
* Request:
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/lectures/5f0b6c19bf974e0b245c59b3/users/5f010459d9994c2308ac5757
    * Body: (application/json)
    ```
        {       
            "action": "end"
        }
    ```

* Response:
    * Status: 204 -  No content

[Back to main documentation](README.md)