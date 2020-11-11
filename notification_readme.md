# Real-Time Notification 

## Description
This documentation is about the notification features of the universal school system application.

This file also documents the set of features that consists the connection requests functionality.

## API Features
This API consists of the features indicated below:


### Notification Subscription
* This API makes use of firebase cloud messaging for real-time notification.
* A user gets subscribed to notifications when they install the app.
* Subscription to notification is per device.
* When a user subscribes to a notification, a token is issued which is saved on the serves.
* Tokens can be retrieved from the server.
* A user unsubscribes from notification by making a delete request for tokens.

### Notification 
* Notification objects are of three types: eventNotification, resourceNotification and weeklyReport.
* Event notifications are user created and can be created by schools to notify members or parents about an update.
* Event notifications can only be created by staff.
* Resource notifications are generated whenever a teacher creates a resource like lecture, assessment or exams which needs students attention.
* Weekly reports are notifications sent weekly to the overall app administration.
* There are other types of notification like subscription, feepayment ( used to notify app manager and school administrator about payments) and assessmentSubmission,. These notifications are not persisited on the server.
* For each type of notification, a notification log is created for every recipient to track isRead status and persisited on the server.
* For each type of notification, a notification message is sent to individual recipients.
* The notificationid for notification logs whose notification objects are not persisited on the server are references to: payment reciepts(in the case of payments), assessment results (in the case of assessmentSubmission).
* Every user can delete their notificationLog.
* Notification objects can be retrieved using the notificationId asscoiated with a log.


## Connection Notifications
This includes notifications for DUO group and parent to student or student to student connections.

### DUO Group Notifications
* When a user wants to form a DUO group with another user, the requested user recieves a notification  which expresses the intent of the requesting user.
* When a user wants to form a DUO group with another user, the requesting user recieves a notification  if the requested user declines the invitation.
* When a user wants to form a DUO group with another user, the requesting user recieves a notification  if the requested user accepts the invitation.   

### Connect With Student Notifications
* When a parent or stapent or a student(potential sibling) wants to connect with a student, the requested student recieves a notification.
* When a student declines an invitation to connect, the requesting student or stapent or parent recieves a notification.
* When a student accepts an invitation to connect, the requesting student or stapent or parent recieves a notification
* Users can see all their pending connection requests.
* Users can cancel any of their pending connection requests.


| Endpoint                                                             | Function                                                                       |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| POST/api/v1/users/me/:user_id/notification/subscription              | Subscribes a user to notifications                                             |
| GET/api/v1/users/me/:user_id/notification/token                      | Retrieves a user tokens                                                        |
| PATCH/api/v1/users/me/:user_id/notification/subscription             | Adds a new token to user tokens                                                |
| DELETE/api/v1/users/me/:user_id/notification/subscription            | Unsubscribes a user from notifications                                         |
| POST/api/v1/users/me/:user_id/notification                           | Creates an event notification                                                  |
| GET/api/v1/:user_id/notification/:notification_id/:type              | Retrieves a notification object base on type                                   |
| DELETE/api/v1/:user_id/notification/:notification_id/:type           | Deletes a notification object                                                  |
| GET/api/v1/:user_id/notification/logs                                | Retrieves all notification logs of a user                                      |
| DELETE/api/v1/:user_id/notification/logs/:log_id                     | Deletes a specific notification log                                            |
| GET/api/v1/users/me/notifications/                                   | Retrieve all my notifications                                                  |
| GET/api/v1/users/me/notifications/5efdf92b7cb1c727086dd60b           | Retrieve specific notification                                                 |
| DELETE/api/v1/users/me/notifications/5efdf92b7cb1c727086dd60b        | Delete specific notification                                                   |
| POST/api/v1/users/me/schools/5ecb08dfd2595416f0dc9978                |                                                                                |
| /request_connection_with_student                                     | Request Connection With Student (Potential Parents/Stapents/Siblings)          |
| POST/api/v1/users/me/schools/5ef61f730639851ca826dcf7/notifications  |
| /5efaaea9e8772a04bc2bb77b/decline_request_to_connect_with_student    | Student Declines Request To Connect                                            |
| PATCH/api/v1/users/me/schools/5ef61f730639851ca826dcf7/notifications |
| /5efdf92b7cb1c727086dd60b/accept_request_to_connect_with_student     | Student Accepts Request To Connect                                             |
| DELETE/api/v1/users/me/schools/5ef61f730639851ca826dcf7/             |
| /cancel_request_to_connect_with_student?childUsername=amaakwukwuma90 | Potential Parent or Stapent or Sibling Cancels Already Sent Request To Connect |
| GET/api/v1/users/me/schools/5ecb08dfd2595416f0dc9978                 |
| /my_pending_connection_requests                                      | Retrieve All My Pending Connection Requests                                    |

### Sample Requests and Responses From The API
- [Notification Subscription](#notification-subscription)
    - [Subscribe User](#subscribe-user)
    - [Retrieve User Tokens](#retrieve-user-tokens)
    - [Update User Tokens](#update-user-token)
    - [Unsubscribe User](#unsubscribe-user)


- [Notification](#notification)
    - [Create Event Notification](#create-event-notification)
    - [Retrieve Notification](#retrieve-notification)
    - [Delete Notification](#delete-notification)
    - [Get Notification Logs](#get-notification-logs)
    - [Delete Notification Log](#delete-notification-log)


- [Connection Notification](#connection-notification)
    - [Retrieve Connection Notifications](#retrieve-connection-notifications)
    - [Retrieve A Connection Notifications](#retrieve-a-connection-notifications)
    - [Delete A Connection Notification](#delete-a-connection-notification)
    - [Connect With Student](#connect-with-student)
    - [Decline Request To Connect](#decline-request-to-connect)
    - [Accept Request To Connect](#accept-request-to-connect)
    - [Cancel Request To Connect](#cancel-request-to-connect)
    - [Retrieve Pending Connection Requests](#retrieve-pending-connection-requests)


###  Notification Subscription

### Subscribe User
* Request
    * Endpoint: POST/api/v1/users/me/5f010459d9994c2308ac5757/notification/subscription
    * Body: (application/json)
    ```
        {       
            "token": "dW_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr41icL10ZNk6nD6SfC5jg9A83tlyCZVd9mg8pipUSWP"
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Subscription was successfully updated",
            "results": 1,
            "data": {
                "_id": "5f0106d0f4a61422fc1a5d8f",
                "tokens": [
                    "W_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr41icL10ZNk6nD6SfC5jg9A83tlyCZVd9mg8pipUSWP"
                ],
                "user_id": "5f010459d9994c2308ac5757",
                "userCategory": "Admin",
                "createdOn": "2020-07-04T22:46:40.000Z",
                "__v": 0
            }
        }
    ```

### Retrieve User Tokens

* Request:
    * Endpoint: GET/api/v1/users/me/5f010459d9994c2308ac5757/notification/token

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            status": "success",
            "message": "Notification tokens retrieved successfully",
            "results": 1,
            "data": {
                "_id": "5f0106d0f4a61422fc1a5d8f",
                "tokens": [
                    "W_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr41icL10ZNk6nD6SfC5jg9A83tlyCZVd9mg8pipUSWP",
                    "dW_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr41icL10ZNk6nD6SfC5jg9A83tlyCZVd9mg8pipUSWP",
                    "twghW_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr4C5jg9A83tlyCZVd9mg8pipUSWP"
                ],
                "user_id": "5f010459d9994c2308ac5757",
                "userCategory": "Admin",
                "createdOn": "2020-07-04T22:46:40.000Z",
                "__v": 0
            }
        }
    ```

### Update User Tokens
* Request
    * Endpoint: PATCH/api/v1/users/me/5f010459d9994c2308ac5757/notification/subscription
    * Body: (application/json)
    ```
        {       
            "token": "dW_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr41icL10ZNk6nD6SfC5jg9A83tlyCZVd9mg8pipUSWP"
        }
    ```

* Response
    * Status: 200 - OK
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Subscription was successfully updated",
            "results": 1,
            "data": {
                "_id": "5f0106d0f4a61422fc1a5d8f",
                "tokens": [
                    "W_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr41icL10ZNk6nD6SfC5jg9A83tlyCZVd9mg8pipUSWP",
                    "dW_TMGfZHw_14tOSsvhGw2:APA91bHFw0BPZ3nKIWoCGQc0fu717d6sNaLiLGm5gQiWGYNEjYpd75t5cOIw0jV6EG57zrT5iG6FgHtlzWVLHE6OUtCFk1AQMr41icL10ZNk6nD6SfC5jg9A83tlyCZVd9mg8pipUSWP",
                ],
                "user_id": "5f010459d9994c2308ac5757",
                "userCategory": "Admin",
                "createdOn": "2020-07-04T22:46:40.000Z",
                "__v": 0
            }
        }
    ```

### Unsubscribe User
* Request:
    * Endpoint: DELETE/api/v1/users/me/5f010459d9994c2308ac5757/notification/subscription

* Response: 
    * Status: 204 - No Content


###  Notification

### Create Event Notification
* Request
    * Endpoint: POST/api/v1/users/me/5ecb18d0ef9ab21050ca1f1f/notification
    * Body: (application/json)
    ```
        {       
            "title": "End of year party",
            "message": "You are invited to our end of year party taking place at....",
            "type": "eventNotification",
            "recipients": ["Staff", "Parents"]       
        }
    ```

* Response
    * Status: 201 - Created
    * Body: application/json

    ``` {
            "status": "success",
            "message": "Notification for event has been successfully created",
            "results": 1,
            "data": {
                "recipients": [
                    "Staff", "Parents"
                ],
                "type": "eventNotification",
                "_id": "5f0387546982100d6c761872",
                "title": "End of year party",
                "message": "You are invited to our end of year party taking place at....",
                "createdBy": "5f010459d9994c2308ac5757",
                "createdOn": "2020-07-06T20:19:32.000Z",
                "__v": 0
            }
        }
    ```


### Retrieve Notification

* Request:
    * Endpoint: GET/api/v1/users/me/5ecb18d0ef9ab21050ca1f1f/notification/5f0387546982100d6c761872/eventNotification

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Notification  retrieved successfully",
            "results": 1,
            "data": {
                "_id": "5f0387546982100d6c761872",
                "recipients": [
                    "Staff"
                ],
                "type": "eventNotification",
                "title": "End of year party",
                "message": "You are invited to our end of year party taking place at....",
                "createdBy": "5f010459d9994c2308ac5757",
                "createdOn": "2020-07-06T20:19:32.000Z",
                "__v": 0
            }
        }
    ```

### Delete Notification
* Request:
    * Endpoint: DELETE/api/v1/users/me/5ecb18d0ef9ab21050ca1f1f/notification/5f0387546982100d6c761872/eventNotification

* Response: 
    * Status: 204 - No Content

### Get Notification Logs

* Request:
    * Endpoint: GET/api/v1/users/me/5f010459d9994c2308ac5757/notification/logs

* Response:
    * Status: 200 - OK
    * Body: (application/json)

    ```
        {
            "status": "success",
            "message": "Notifications retreievd successfully",
            "results": 4,
            "data": [
                {
                    "_id": "5f0117dfc7a5ab2514e636d3",
                    "type": "eventNotification",
                    "isRead": true,
                    "title": "PTA Meeting",
                    "category": "Admin",
                    "user_id": "5f010459d9994c2308ac5757",
                    "notificationId": "5f0117dfc7a5ab2514e636d2",
                    "__v": 0
                },
                {
                    "_id": "5f011800c7a5ab2514e636d5",
                    "type": "eventNotification",
                    "isRead": false,
                    "title": "Graduation Ceremony",
                    "category": "Admin",
                    "user_id": "5f010459d9994c2308ac5757",
                    "notificationId": "5f011800c7a5ab2514e636d4",
                    "__v": 0
                },

                {
                    "_id": "5f01f63357d3f316b009dd13",
                    "isRead": false,
                    "title": "Weekly Report",
                    "category": "Admin",
                    "user_id": "5f010459d9994c2308ac5757",
                    "notificationId": "5f01f63357d3f316b009dd12",
                    "type": "weeklyReport",
                    "__v": 0
                },
                {
                    "_id": "5f01f6a8c0d90e0b84add9e0",
                    "isRead": false,
                    "title": "Weekly Report",
                    "category": "Admin",
                    "user_id": "5f010459d9994c2308ac5757",
                    "notificationId": "5f01f6a8c0d90e0b84add9df",
                    "type": "weeklyReport",
                    "__v": 0
                },
            ]
        }
    ```


### Delete Notification Log
* Request:
    * Endpoint: DELETE/api/v1/users/me/5f010459d9994c2308ac5757/notification/5f038338cdb18c14d40b2d7f/logs/5f03ad69e18f531584f6a772

* Response: 
    * Status: 204 - No Content


### Retrieve Connection Notifications
* Request:
    * Endpoint: GET/api/v1/users/me/notifications/

* Response:
    * Status:200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Your notifications",
        "results": 1,
        "data": [
            {
                "sender": {
                    "username": "King50",
                    "category": "Stapent"
                },
                "recipient": {
                    "id": "5efdf8737cb1c727086dd608",
                    "username": "amaakwukwuma90",
                    "category": "Student"
                },
                "hasBeenRead": false,
                "_id": "5efdf92b7cb1c727086dd60b",
                "school": "5ef61f730639851ca826dcf7",
                "createdAt": "2020-07-02T15:11:39.635Z",
                "subject": "Connect With Parent",
                "description": "King50, a Stapent from Shalom Academy Group Of Schools, claims that you are his child and thus, wants to connect with you. You need to indicate if this user is indeed your parent. If he is not your parent, you also need to respond.",
                "senderId": "5efdf6e57cb1c727086dd605",
                "__v": 0
            }
        ]
    }
    ```  

### Retrieve A Connection Notification
* Request:
    * Endpoint: GET/api/v1/users/me/notifications/5efdf92b7cb1c727086dd60b

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully retrieved your notification",
        "results": 1,
        "data": {
            "sender": {
                "username": "King50",
                "category": "Stapent"
            },
            "recipient": {
                "id": "5efdf8737cb1c727086dd608",
                "username": "amaakwukwuma90",
                "category": "Student"
            },
            "hasBeenRead": true,
            "_id": "5efdf92b7cb1c727086dd60b",
            "school": "5ef61f730639851ca826dcf7",
            "createdAt": "2020-07-02T15:11:39.635Z",
            "subject": "Connect With Parent",
            "description": "King50, a Stapent from Shalom Academy Group Of Schools, claims that you are his child and thus, wants to connect with you. You need to indicate if this user is indeed your parent. If he is not your parent, you also need to respond.",
            "senderId": "5efdf6e57cb1c727086dd605",
            "__v": 0
        }
    }
    ```  

### Delete A Connection Notification
* Request:
    * Endpoint: DELETE/api/v1/users/me/notifications/5efdf92b7cb1c727086dd60b

* Response:
    * Status: 204 - no content 

### Connect With Student
A Potential Parent Or Stapent Or Sibling Can Use This Endpoint To Request Connection With A Student
* Request:
    * Endpoint: POST/api/v1/users/me/schools/5ecb08dfd2595416f0dc9978/request_connection_with_student
    * Body:(application/json)
    ```
    {
        "childUsername": "sophiaokeke90"
    }
    ``` 

* Response:
    * Status: 200 - ok
    * Body: (application/json)
    ```
    {
        "status": "Success",
        "message": "Your request has been sent to the student"
    }
    ```  

### Decline Request To Connect

A Student Can Use This Endpoint To Decline A Request To Connect From A Potential Sibling Or Parent Or Stapent

* Request:
    * Endpoint: POST/api/v1/users/me/schools/5ef61f730639851ca826dcf7/notifications/5efaaea9e8772a04bc2bb77b/decline_request_to_connect_with_student

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "You have declined the request."
    }
    ```  

### Accept Request To Connect

A Student Can Use This Endpoint To Accept A Request To Connect From A Potential Sibling Or Parent Or Stapent

* Request:
    * Endpoint: PATCH/api/v1/users/me/schools/5ef61f730639851ca826dcf7/notifications/5efdf92b7cb1c727086dd60b/accept_request_to_connect_with_student

* Response: 
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "You have accepted the request. You and your Sibling are now connected."
    }
    ``` 

### Cancel Request To Connect
 
A Potential Sibling Or Parent Or Stapent Can Use This Endpoint To Cancel Their Already Sent Request To Connect

* Request:
    * Endpoint: DELETE/api/v1/users/me/schools/5ef61f730639851ca826dcf7//api/v1/users/me/schools/5ef61f730639851ca826dcf7/

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "The connection request has been cancelled"
    }
    ```  

### Retrieve Pending Connection Requests
This endpoint serves several purposes:

1. This endpoint is for parents and stapents to see the usernames of all the students that they have made connection requests to.

2. Students can also use this endpoint to see the usernames of all the students that they have made connection requests to.

* Request:
    * Endpoint: GET/api/v1/users/me/schools/5ecb08dfd2595416f0dc9978/my_pending_connection_requests

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "Successfully retrieved all your pending connection requests",
        "results": 2,
        "data": [
            {
                "childUsername": "ritamonday63"
            },
            {
                "childUsername": "sophiaokeke90"
            }
        ]
    }
    ``` 