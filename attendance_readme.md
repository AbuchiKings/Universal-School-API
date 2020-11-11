# Attendance 

## Description
This documentation is about the school attendance API of the universal school system application.

## API Features
This API consists of the features indicated below:


### Students Attendance
* Only one attendance record can be created for a class in a given week.
* Attendance record are taken on daily basis and by class.
* Staff can create an attendance record.
* Staff can add or remove a student from an attendance record of a specific day.
* Staff can retrieve attendance records or a specific attendance record.
* Attendance record can be filtered by class, term, week and year.
* Staff can retrieve all students in an attendance record.

### Staff Attendance
* Only one attendance record can be created for the staff of a school in a given week.
* Attendance record are taken on daily basis.
* School admin can create an attendance record.
* School admin can add or remove a staff from an attendance record of a specific day.
* Staff can retrieve attendance records or a specific attendance record.
* Attendance record can be filtered by term, week and year.


| Endpoint                                                                              | Function                                             |
| --------------------------------------------------------------------------------------| -----------------------------------------------------|
| POST/api/v1/schools/:id/students/attendance/class                                     | Creates a new attendance record a                    |
| GET/api/v1/schools/:id/students/attendance/class                                      | Retrieeves all the attendance record of a school     |
| GET/api/v1/schools/:id/students/attendance/:attendance_id/class/:class_title          | Retrieves a specific attendance record               | 
| GET/api/v1/schools/:id/students/attendance/:attendance_id/weekdays/:day               | Retrieves students from a specific attendance record |
| PATCH/api/v1/schools/:id/students/attendance/:attendance_id/class/:class_title        | Updates an attendance record.                        |
| DELETE/api/v1/schools/:id/students/attendance/:attendance_id/class/:class_title       | Deletes a specific attendance record                 |
| DELETE/api/v1/schools/:id/students/student_id/attendance/:attendance_id/weekdays/:day | Deltes a student from attendance list of a given day |
| POST/api/v1/schools/:id/staff/attendance/weekly                                       | Creates a new weekly attendance for staff            |
| GET/api/v1/schools/:id/staff/attendance/weekly                                        | Retrieves attendance records for staff of a school   |
| GET/api/v1/schools/:id/staff/attendance/:attendance_id/weekly/:week                   | Retrieves a specific staff attendance record         |
| PATCH/api/v1/schools/:id/staff/attendance/:attendance_id/weekly/:week                 | Updates a specific staff attendance record           |
| DELETE/api/v1/schools/:id/staff/attendance/:attendance_id/weekly/:week                | Deletes a staff attendance record                    |
| DELETE/api/v1/schools/:id/staff/:staff_id/attendance/:attendance_id/weekdays/:day     | Deletes a specific staff from a staff attendance     |




### Sample Requests and Responses From The API

- [Student Attendance](#student-attendance)
    - [Create Student Attendance](#create-student-attendance)
    - [Retrieve Student Attendance](#retrieve-student-attendance)
    - [Retrieve A Student Attendance](#retrieve-a-student-attendance)
    - [Retrieve Students From Attendance](#retrieve-students-from-attendance)
    - [Update Student Attendance](#update-student-attendance)
    - [Delete Student Attendance](#delete-student-attendance)
    - [Delete Student From Attendance](#delete-student-from-attendance)


- [Staff Attendance](#staff-attendance)
    - [Create Staff Attendance](#create-staff-attendance)
    - [Retrieve Staff Attendance](#retrieve-staff-attendance)
    - [Retrieve A Staff Attendance](#retrieve-a-staff-attendance)
    - [Update Staff Attendance](#update-staff-attendance)
    - [Delete Staff Attendance](#delete-staff-attendance)
    - [Delete Staff From Attendance](#delete-staff-from-attendance)

###  Student Attendance

### Create Student Attendance
* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/students/attendance/class
    * Body: (application/json)
    ```
        {       
            "class": "Basic2",
            "term": "2",
            "year": "2021",
            "formTeacher": "5ecb18d3ef9ab21050ca1f26",
            "week": 1
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Created successfuly",
            "results": 1,
            "data": {
                "monday": [],
                "tuesday": [],
                "wednesday": [],
                "thursday": [],
                "friday": [],
                "saturday": [],
                "_id": "5f1246d1f73f8c12dc841944",
                "class": "Basic2",
                "term": 2,
                "year": "2021",
                "formTeacher": "5ecb18d3ef9ab21050ca1f26",
                "week": 5,
                "createdOn": "2020-07-18T00:48:17.000Z",
                "school": "5ecb08dfd2595416f0dc9977",
                "__v": 0
            }
        }
    ```

### Retrieve Student Attendance

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/students/attendance/class
    * Querystrings: class, term, year, week

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
             "status": "success",
            "message": "Attendance retrieved successfully",
            "results": 2,
            "data": [
                {
                    "monday": [
                        "5ecb1918ef9ab21050ca1f81",
                        "5ecb1918ef9ab21050ca1f82",
                        "5ecb1917ef9ab21050ca1f7b",
                        "5ecb1918ef9ab21050ca1f85",
                        "5ecb1918ef9ab21050ca1f7d"
                    ],
                    "tuesday": [],
                    "wednesday": [],
                    "thursday": [],
                    "friday": [],
                    "saturday": [],
                    "_id": "5f121ed4a9c42405d82b845c",
                    "class": "Basic2",
                    "term": 2,
                    "year": "2021",
                    "formTeacher": "5ecb18d3ef9ab21050ca1f26",
                    "week": 1,
                    "createdOn": "2020-07-17T21:57:40.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "__v": 1
                },
                {
                    "monday": [],
                    "tuesday": [],
                    "wednesday": [],
                    "thursday": [],
                    "friday": [],
                    "saturday": [],
                    "_id": "5f121f3da9c42405d82b845d",
                    "class": "Basic2",
                    "term": 3,
                    "year": "2020",
                    "formTeacher": "5ecb18d3ef9ab21050ca1f26",
                    "week": 12,
                    "createdOn": "2020-07-17T21:59:25.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "__v": 0
                }
            ]
        }
    ```

### Retrieve A Student Attendance

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/students/attendance/5f121ed4a9c42405d82b845c/class/Basic2

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
             "status": "success",
            "message": "Attendance retrieved successfully",
            "results": 1,
            "data": {
                "_id": "5f121ed4a9c42405d82b845c",
                "monday": [
                    "5ecb1918ef9ab21050ca1f81",
                    "5ecb1918ef9ab21050ca1f82",
                    "5ecb1917ef9ab21050ca1f7b",
                    "5ecb1918ef9ab21050ca1f85",
                    "5ecb1918ef9ab21050ca1f7f",
                    "5ecb1918ef9ab21050ca1f7d"
                ],
                "tuesday": [],
                "wednesday": [],
                "thursday": [],
                "friday": [],
                "saturday": [],
                "class": "Basic2",
                "term": 2,
                "year": "2021",
                "formTeacher": "5ecb18d3ef9ab21050ca1f26",
                "week": 1,
                "createdOn": "2020-07-17T21:57:40.000Z",
                "school": "5ecb08dfd2595416f0dc9977",
                "__v": 0
            }
        }
    ```


### Retrieve Students From Attendance

* Request:
    * Endpoint: {{URL}}/api/v1/schools/5ecb08dfd2595416f0dc9977/students/attendance/5f121ed4a9c42405d82b845c/weekdays/monday

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Students retrieved successfully",
            "results": 4,
            "data": [
                {
                    "_id": "5ecb1917ef9ab21050ca1f7b",
                    "fullname": "Amanda Gboyega Babatunde",
                    "username": "amandababatunde87"
                },
                {
                    "_id": "5ecb1918ef9ab21050ca1f7d",
                    "fullname": "Esther Eketi Atanda",
                    "username": "esthermonday5"
                },
                {
                    "_id": "5ecb1918ef9ab21050ca1f7f",
                    "fullname": "Amara Chikaodili Mohammed",
                    "username": "amaraatanda14"
                },
                {
                    "_id": "5ecb1918ef9ab21050ca1f81",
                    "fullname": "Amake Habbeeb George",
                    "username": "amakemohammed72"
                }
            ]
        }
    ```

### Update Student Attendance
* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/students/attendance/5f121ed4a9c42405d82b845c/class/Basic2?day=monday
    * Querystrings: day
    * Body: (application/json)
    ```
        {       
            "monday": [
                "5ecb1918ef9ab21050ca1f81", "5ecb1918ef9ab21050ca1f82","5ecb1917ef9ab21050ca1f7b",
                "5ecb1918ef9ab21050ca1f85", "5ecb1918ef9ab21050ca1f7f", "5ecb1918ef9ab21050ca1f7d"
            ]
        }
    ```

* Response
    * Status: 200 - OK
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Attendnace was updated successfully",
            "results": 1,
            "data": {
                "_id": "5f121ed4a9c42405d82b845c",
                "monday": [
                    "5ecb1918ef9ab21050ca1f81",
                    "5ecb1918ef9ab21050ca1f82",
                    "5ecb1917ef9ab21050ca1f7b",
                    "5ecb1918ef9ab21050ca1f85",
                    "5ecb1918ef9ab21050ca1f7f",
                    "5ecb1918ef9ab21050ca1f7d"
                ],
                "tuesday": [],
                "wednesday": [],
                "thursday": [],
                "friday": [],
                "saturday": [],
                "class": "Basic2",
                "term": 2,
                "year": "2021",
                "formTeacher": "5ecb18d3ef9ab21050ca1f26",
                "week": 1,
                "createdOn": "2020-07-17T21:57:40.000Z",
                "school": "5ecb08dfd2595416f0dc9977",
                "__v": 0
            }
        }
    ```

### Delete Student Attendance
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/students/attendance/5f121ed4a9c42405d82b845c/class/Basic2

* Response: 
    * Status: 204 - No Content
    
### Delete Student From Attendance
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/students/5ecb1918ef9ab21050ca1f81/attendance/5f121ed4a9c42405d82b845c/weekdays/monday

* Response: 
    * Status: 204 - No Content


###  Staff Attendance

### Create Staff Attendance
* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/staff/attendance/weekly
    * Body: (application/json)
    ```
        {       
            "term": "2",
            "year": "2021",
            "schoolAdmin": "5ecb18d3ef9ab21050ca1f21",
            "tuesday": [
                {"id":"5ecb18d3ef9ab21050ca1f21",
                "category":"Staff",
                "fullname":"Bukola Samson Ayantola"},
                {"id":"5ecb18d3ef9ab21050ca1f22",
                "category":"Staff",
                "fullname":"Godswill Kevin Afolabi"},
                {"id":"5ecb18d3ef9ab21050ca1f23",
                "category":"Staff",
                "fullname":"Amara Victoria Okoli"}
            ],
            "week": 2
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Attendance has been successfully created",
            "results": 1,
            "data": {
                "_id": "5f12d555c7eb9325b4ea822e",
                "term": 2,
                "year": "2021",
                "schoolAdmin": "5ecb18d3ef9ab21050ca1f21",
                "tuesday": [
                    {
                        "_id": "5f12d555c7eb9325b4ea822f",
                        "id": "5ecb18d3ef9ab21050ca1f21",
                        "category": "Staff",
                        "fullname": "Bukola Samson Ayantola"
                    },
                    {
                        "_id": "5f12d555c7eb9325b4ea8230",
                        "id": "5ecb18d3ef9ab21050ca1f22",
                        "category": "Staff",
                        "fullname": "Godswill Kevin Afolabi"
                    },
                    {
                        "_id": "5f12d555c7eb9325b4ea8231",
                        "id": "5ecb18d3ef9ab21050ca1f23",
                        "category": "Staff",
                        "fullname": "Amara Victoria Okoli"
                    }
                ],
                "week": 2,
                "createdOn": "2020-07-18T10:56:21.000Z",
                "school": "5ecb08dfd2595416f0dc9977",
                "monday": [],
                "wednesday": [],
                "thursday": [],
                "friday": [],
                "saturday": [],
                "__v": 0
            }
        }
    ```

### Retrieve Staff Attendance

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/staff/attendance/weekly
    * Querystrings: term, year, week

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Attendance retrieved successfully",
            "results": 3,
            "data": [
                {
                    "_id": "5f12d2fec7eb9325b4ea8224",
                    "term": 2,
                    "year": "2021",
                    "schoolAdmin": "5ecb18d3ef9ab21050ca1f21",
                    "week": 5,
                    "createdOn": "2020-07-18T10:46:22.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "monday": [],
                    "tuesday": [],
                    "wednesday": [],
                    "thursday": [],
                    "friday": [],
                    "saturday": [],
                    "__v": 0
                },
                {
                    "_id": "5f12d4cdc7eb9325b4ea8226",
                    "term": 2,
                    "year": "2021",
                    "schoolAdmin": "5ecb18d3ef9ab21050ca1f21",
                    "friday": [
                        {
                            "_id": "5f12d4cdc7eb9325b4ea8227",
                            "id": "5ecb18d3ef9ab21050ca1f21",
                            "category": "Staff",
                            "fullname": "Bukola Samson Ayantola"
                        },
                        {
                            "_id": "5f12d4cdc7eb9325b4ea8228",
                            "id": "5ecb18d3ef9ab21050ca1f22",
                            "category": "Staff",
                            "fullname": "Godswill Kevin Afolabi"
                        },
                        {
                            "_id": "5f12d4cdc7eb9325b4ea8229",
                            "id": "5ecb18d3ef9ab21050ca1f23",
                            "category": "Staff",
                            "fullname": "Amara Victoria Okoli"
                        }
                    ],
                    "week": 7,
                    "createdOn": "2020-07-18T10:54:05.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "monday": [],
                    "tuesday": [],
                    "wednesday": [],
                    "thursday": [],
                    "saturday": [],
                    "__v": 0
                },
                {
                    "_id": "5f12d555c7eb9325b4ea822e",
                    "term": 2,
                    "year": "2021",
                    "schoolAdmin": "5ecb18d3ef9ab21050ca1f21",
                    "tuesday": [
                        {
                            "_id": "5f12d555c7eb9325b4ea822f",
                            "id": "5ecb18d3ef9ab21050ca1f21",
                            "category": "Staff",
                            "fullname": "Bukola Samson Ayantola"
                        },
                        {
                            "_id": "5f12d555c7eb9325b4ea8230",
                            "id": "5ecb18d3ef9ab21050ca1f22",
                            "category": "Staff",
                            "fullname": "Godswill Kevin Afolabi"
                        },
                        {
                            "_id": "5f12d555c7eb9325b4ea8231",
                            "id": "5ecb18d3ef9ab21050ca1f23",
                            "category": "Staff",
                            "fullname": "Amara Victoria Okoli"
                        }
                    ],
                    "week": 2,
                    "createdOn": "2020-07-18T10:56:21.000Z",
                    "school": "5ecb08dfd2595416f0dc9977",
                    "monday": [],
                    "wednesday": [],
                    "thursday": [],
                    "friday": [],
                    "saturday": [],
                    "__v": 0
                }
            ]
        }
    ```

### Retrieve A Staff Attendance

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/staff/attendance/5f12d4cdc7eb9325b4ea8226/weekly/7

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Attendance retrieved successfully",
            "results": 1,
            "data": {
                "_id": "5f12d4cdc7eb9325b4ea8226",
                "term": 3,
                "year": "2021",
                "schoolAdmin": "5ecb18d3ef9ab21050ca1f21",
                "friday": [
                    {
                        "_id": "5f12d4cdc7eb9325b4ea8227",
                        "id": "5ecb18d3ef9ab21050ca1f21",
                        "category": "Staff",
                        "fullname": "Bukola Samson Ayantola"
                    },
                    {
                        "_id": "5f12d4cdc7eb9325b4ea8229",
                        "id": "5ecb18d3ef9ab21050ca1f23",
                        "category": "Staff",
                        "fullname": "Amara Victoria Okoli"
                    }
                ],
                "week": 7,
                "createdOn": "2020-07-18T10:54:05.000Z",
                "school": "5ecb08dfd2595416f0dc9977",
                "monday": [],
                "tuesday": [
                    {
                        "_id": "5f12dbef8907251544dc28e4",
                        "id": "5ecb18d3ef9ab21050ca1f21",
                        "category": "Staff",
                        "fullname": "Bukola Samson Ayantola"
                    },
                    {
                        "_id": "5f12dbef8907251544dc28e5",
                        "id": "5ecb18d3ef9ab21050ca1f22",
                        "category": "Staff",
                        "fullname": "Godswill Kevin Afolabi"
                    },
                    {
                        "_id": "5f12dbef8907251544dc28e6",
                        "id": "5ecb18d3ef9ab21050ca1f23",
                        "category": "Staff",
                        "fullname": "Amara Victoria Okoli"
                    }
                ],
                "wednesday": [],
                "thursday": [],
                "saturday": [],
                "__v": 0
            }
        }
    ```


### Update Staff Attendance
* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/staff/attendance/5f12d4cdc7eb9325b4ea8226/weekly/7?day=tuesday
    * Querystrings: day
    * Body: (application/json)
    ```
        {       
            "tuesday": [
                {"id":"5ecb18d3ef9ab21050ca1f21",
                "category":"Staff",
                "fullname":"Bukola Samson Ayantola"},
                {"id":"5ecb18d3ef9ab21050ca1f22",
                "category":"Staff",
                "fullname":"Godswill Kevin Afolabi"},
                {"id":"5ecb18d3ef9ab21050ca1f23",
                "category":"Staff",
                "fullname":"Amara Victoria Okoli"}
            ],
            "term": 3
        }
    ```

* Response
    * Status: 200 - OK
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Attendnace was updated successfully",
            "results": 1,
            "data": {
                "_id": "5f12d4cdc7eb9325b4ea8226",
                "term": 3,
                "year": "2021",
                "schoolAdmin": "5ecb18d3ef9ab21050ca1f21",
                "friday": [
                    {
                        "_id": "5f12d4cdc7eb9325b4ea8227",
                        "id": "5ecb18d3ef9ab21050ca1f21",
                        "category": "Staff",
                        "fullname": "Bukola Samson Ayantola"
                    },
                    {
                        "_id": "5f12d4cdc7eb9325b4ea8228",
                        "id": "5ecb18d3ef9ab21050ca1f22",
                        "category": "Staff",
                        "fullname": "Godswill Kevin Afolabi"
                    },
                    {
                        "_id": "5f12d4cdc7eb9325b4ea8229",
                        "id": "5ecb18d3ef9ab21050ca1f23",
                        "category": "Staff",
                        "fullname": "Amara Victoria Okoli"
                    }
                ],
                "week": 7,
                "createdOn": "2020-07-18T10:54:05.000Z",
                "school": "5ecb08dfd2595416f0dc9977",
                "monday": [],
                "tuesday": [
                    {
                        "_id": "5f12dbef8907251544dc28e4",
                        "id": "5ecb18d3ef9ab21050ca1f21",
                        "category": "Staff",
                        "fullname": "Bukola Samson Ayantola"
                    },
                    {
                        "_id": "5f12dbef8907251544dc28e5",
                        "id": "5ecb18d3ef9ab21050ca1f22",
                        "category": "Staff",
                        "fullname": "Godswill Kevin Afolabi"
                    },
                    {
                        "_id": "5f12dbef8907251544dc28e6",
                        "id": "5ecb18d3ef9ab21050ca1f23",
                        "category": "Staff",
                        "fullname": "Amara Victoria Okoli"
                    }
                ],
                "wednesday": [],
                "thursday": [],
                "saturday": [],
                "__v": 0
            }
        }
    ```

### Delete Staff Attendance
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/staff/attendance/5f12d2fec7eb9325b4ea8224/weekly/5

* Response: 
    * Status: 204 - No Content
    
### Delete Staff From Attendance
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/staff/5ecb18d3ef9ab21050ca1f22/attendance/5f12d4cdc7eb9325b4ea8226/weekdays/friday

* Response: 
    * Status: 204 - No Content

