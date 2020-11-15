# Real-Time Chat 

## Description
This documentation is about the chat features of the universal school system application.

## API Endpoints and Their Functionality For Chat Features

| Endpoint                                                                                                                                                 | Functionality                                             |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| POST/api/v1/schools/5ecb08dfd2595416f0dc9977/chats                                                                                                       | Create a new message in a school's chat forum.            |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/chats                                                                                                        | See all chats in a school's chat forum                    |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/chats/5ee381872e0f06116c10b4a2                                                                               | See specific chat in a school's chat forum                |
| PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/chats/5ee381872e0f06116c10b4a2                                                                             | Update specific chat in a school's chat forum             |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/chats/5ee381872e0f06116c10b4a2                                                                            | Delete specific chat in a school's chat forum             |
| POST/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats                                                                      | Create a new message in a classroom's chat forum          |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats                                                                       | See all the chats in a classroom's chat forum             |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats/5ee4cb3e668ef404bcf67dff                                              | See specific chat message in a classroom's chat forum     |
| PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats/5ee4cb3e668ef404bcf67dff                                            | Update specific chat message in a classroom's chat forum  |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats/5ee4cb3e668ef404bcf67dff                                           | Delete specific chat message in a classroom's chat forum  |
| POST/api/v1/schools/5ecb08dfd2595416f0dc9977/groups                                                                                                      | Create a new group within a school                        |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups                                                                                                       | See all the groups in a school                            |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/my_groups                                                                                             | See all the groups you are a member of in a school        |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475                                                                              | See the details of a specific group in a school           |
| PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475                                                                            | Update group name and description                         |
| PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/add_new_member                                                             | Add a new member to the group                             |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/remove_member?memberUsername=memberusername&memberCategory=membercategory | Remove a member from the group                            |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/remove_myself                                                             | Remove yourself from a group                              |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/                                                                          | Delete a group                                            |
| POST/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats                                                                       | Create a new chat message in group                        |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats                                                                        | Get group chat messages                                   |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats/5ee84372dd34471c5c063b32                                               | Get specific group chat message                           |
| PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats/5ee84372dd34471c5c063b32                                             | Update Group Chat Message                                 |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats/5ee84372dd34471c5c063b32                                            | Delete Group Chat Message                                 |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8d0e79ba18f1fe865844e                                                                                 | Get School PTA Group                                      |
| PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8d0e79ba18f1fe865844e                                                                               | Update School PTA Group                                   |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8d0e79ba18f1fe865844e                                                                              | Delete School PTA Group                                   |
| POST/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats                                                                          | Create Chat In PTA Forum                                  |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats                                                                           | Retrieve PTA Forum Chats                                  |
| GET/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats/5ee96c80e2d7311d58729004                                                  | Retrieve Specific Group Chat                              |
| PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats/5ee96c80e2d7311d58729004                                                | Update Specific Group Chat                                |
| DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats/5ee96c80e2d7311d58729004                                               | Delete Specific Group Chat                                |
| POST/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/request?id=id&username=username&category=user_category                                                  | Make Request To Another User Form A Duo Group             |
| POST/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/decline_request?id=id&username=username&category=user_category                                          | Decline Request From Another User To Form A Duo Group     |
| POST/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/accept_request?id=id&username=username&category=user_category                                           | Accept Request To Form A Duo Group From Another User      |
| PATCH/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5eed12ccd96a0904a82f8aaa/disable                                                                       | Disable A Duo Group Of Which You Are A Member             |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/disabled_duo_groups                                                                                      | Retreive All Your Disabled Duo Groups                     |
| PATCH/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5eed12ccd96a0904a82f8aaa/enable                                                                        | Re-enable A Duo Group Which You Previously Disabled       |
| DELETE/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5eed12ccd96a0904a82f8aaa/                                                                             | Deletion Of A DUO Group By A School-Administrator         |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/                                                                                                         | Retrieve All School DUO Groups                            |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/active_duo_groups                                                                                        | Retrieve All My Active DUO Groups                         |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e                                                                                 | Retrieve Specific DUO Group                               |
| DELETE/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/cancel/request?id=5eec13c8703e9013c4f66ee3&username=amaakwukwuma90&category=Student                   | Cancel Request To Form A DUO Group                        |
| POST/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats                                                                          | Create Message In DUO Group                               |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats                                                                           | Retrieve All Messages In a DUO Group                      |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats/5ef1a13834f7030db4aa25e9                                                  | Retrieve Specific Message In a DUO Group                  |
| PATCH/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats/5ef1a13834f7030db4aa25e9                                                | Update Specific Message In DUO Group                      |
| DELETE/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats/5ef1a13834f7030db4aa25e9                                               | Delete Specific Message In DUO Group                      |
| POST/api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists                                                                                                  | Blacklist A Pair Of Users From Forming DUO Groups         |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists                                                                                                   | Retrieve All The Blacklisted Pair Of Users In Your School |
| GET/api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists/5ef1762011e59811f89ba3b5                                                                          | Retrieve A Specific Blacklisted Pair Of Users             |
| DELETE/api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists/5ef1762011e59811f89ba3b5                                                                       | Un-Blacklist A Pair Of Users                              |
| GET/api/v1/users/me/my_pending_requests_to_form_duo_group                                                                                                | Retrieve All My Pending Requests To Form A DUO group      |

## Chat Foundations

There are some features that are absolutely neccessary for their corresponding chat feature to be successfully operationalized.

For instance before members of a school and classroom cannot chat when the school itself or classroom does not yet exist.

The school and classroom features are already in place.

However, prior to implementing the chat features, there was currently nothing of that sort for groups, PTA and groups for only two individuals.

This is why they can be found specified below:

* [Groups](#groups)
* [PTA](#pta)
* [DUO](#duo)

## Groups
The ability to form groups is a very essential aspect of the universal school system.

This is because, it allows students and teachers to form study groups, research groups, and other collaborative forums.

Furthermore, the group feature forms the basis of the group chat functionality.

Any person attached to a school can create a group within that school. The group creator, automatically becomes the group's admin. 

Both students and staff or stapents can be members of thesame group.

Only the School-Administrator or Parent_School-Administrator, Principal or Parent_Principal and Vice-Principal or Parent_Vice-Principal can see all the groups in a school.

Logged in users can see all the groups which they are members of.

In order to see the details of a specific group, you must either be a member of that group or be one of the school's top administrative officers.

In order to update the name and description of a specific group, you must be the group's admin.

Only the group admin can delete a specific group.

Only the group admin can add a new member to a specific group.

Only the group admin can remove a group member from the group.

Logged in users can remove themselves from any group they belong to.

## Sample Requests and Responses For Group API

## Create Group
* Request:
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/groups
    * Body:(application/json)
    ```
    {
        "name": "English Research Assignment",
        "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Phonetics English assignment."
    }
    ``` 

* Response:
    * Status: 201 - created
    * Body:(application/json)
    ```
    {
    "status": "success",
    "message": "New Group Created Successfully!",
    "results": 1,
    "data": {
        "_id": "5ee7b1b905d98f1ae03e84bf",
        "name": "English Research Assignment",
        "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Phonetics English assignment.",
        "school": "5ecb08dfd2595416f0dc9977",
        "members": [
            {
                "_id": "5ee7b1b905d98f1ae03e84c0",
                "memberId": "5ed2bbf7ca1dbc1d6c009635",
                "memberUsername": "wasiuedet9",
                "memberCategory": "Student"
            }
        ],
        "createdAt": "2020-06-15T17:36:57.354Z",
        "admin": {
            "id": "5ed2bbf7ca1dbc1d6c009635",
            "username": "wasiuedet9",
            "category": "Student"
        },
        "__v": 0
    }
    ``` 


## Get All Groups
* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups 

* Response:
    * Status: 200 - ok
    * Body: (application/json)
    ```
    {
    "status": "success",
    "message": "Successful",
    "results": 2,
    "data": [
        {
            "admin": {
                "id": "5ed2bbf7ca1dbc1d6c009635",
                "username": "wasiuedet9",
                "category": "Student"
            },
            "_id": "5ee6c3d22f837f1e2c39c475",
            "name": "Chemistry Research Assignment",
            "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Redux reaction Chemistry assignment.",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee6c3d22f837f1e2c39c476",
                    "memberId": "5ed2bbf7ca1dbc1d6c009635",
                    "memberUsername": "wasiuedet9",
                    "memberCategory": "Student"
                }
            ],
            "createdAt": "2020-06-15T00:41:54.136Z",
            "__v": 0
        },
        {
            "admin": {
                "id": "5ed2bbf7ca1dbc1d6c009635",
                "username": "wasiuedet9",
                "category": "Student"
            },
            "_id": "5ee6c42a2f837f1e2c39c477",
            "name": "Biology Research Assignment",
            "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Sense Organs Biology assignment.",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee6c42a2f837f1e2c39c478",
                    "memberId": "5ed2bbf7ca1dbc1d6c009635",
                    "memberUsername": "wasiuedet9",
                    "memberCategory": "Student"
                }
            ],
            "createdAt": "2020-06-15T00:43:22.703Z",
            "__v": 0
        }
    ]
    ``` 

## Get My Groups
* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/my_groups

* Response:
    * Status: 200 - ok
    * Body:(application/json)
    ```
    {
        "status": "success",
        "message": "Successful",
        "results": 2,
        "data": [
            {
                "admin": {
                    "id": "5ed2bbf7ca1dbc1d6c009635",
                    "username": "wasiuedet9",
                    "category": "Student"
                },
                "_id": "5ee6c3d22f837f1e2c39c475",
                "name": "Biology Research Assignment",
                "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Sense Organs Biology assignment.",
                "school": "5ecb08dfd2595416f0dc9977",
                "members": [
                    {
                        "_id": "5ee6c3d22f837f1e2c39c476",
                        "memberId": "5ed2bbf7ca1dbc1d6c009635",
                        "memberUsername": "wasiuedet9",
                        "memberCategory": "Student"
                    }
                ],
                "createdAt": "2020-06-15T00:41:54.136Z",
                "__v": 0
            },
            {
                "admin": {
                    "id": "5ed2bbf7ca1dbc1d6c009635",
                    "username": "wasiuedet9",
                    "category": "Student"
                },
                "_id": "5ee6c42a2f837f1e2c39c477",
                "name": "Chemistry Research Assignment",
                "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Redux reaction Chemistry assignment.",
                "school": "5ecb08dfd2595416f0dc9977",
                "members": [
                    {
                        "_id": "5ee6c42a2f837f1e2c39c478",
                        "memberId": "5ed2bbf7ca1dbc1d6c009635",
                        "memberUsername": "wasiuedet9",
                        "memberCategory": "Student"
                    }
                ],
                "createdAt": "2020-06-15T00:43:22.703Z",
                "__v": 0
            }
        ]
    }
    ``` 

## Get Specific Group
* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475 

* Response:
    * Status: 200 - ok
    * Body:(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully Retrieved Group",
        "results": 1,
        "data": {
            "admin": {
                "id": "5ed2bbf7ca1dbc1d6c009635",
                "username": "wasiuedet9",
                "category": "Student"
            },
            "_id": "5ee6c3d22f837f1e2c39c475",
            "name": "Biology Research Assignment",
            "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Sense Organs Biology assignment.",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee6c3d22f837f1e2c39c476",
                    "memberId": "5ed2bbf7ca1dbc1d6c009635",
                    "memberUsername": "wasiuedet9",
                    "memberCategory": "Student"
                }
            ],
            "createdAt": "2020-06-15T00:41:54.136Z",
            "__v": 0
        }
    }
    ``` 

## Update Group Name and Description
* Request:
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475
    * Body: (application/json)
    ```
    {
        "name": "Mathematics Research Assignment",
        "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Surds Mathematics assignment.",
    }
    ```

* Response:
    * Status: 200 - ok
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "Successfully Updated Group",
        "results": 1,
        "data": {
            "admin": {
                "id": "5ed2bbf7ca1dbc1d6c009635",
                "username": "wasiuedet9",
                "category": "Student"
            },
            "_id": "5ee6c3d22f837f1e2c39c475",
            "name": "Mathematics Research Assignment",
            "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Surds Mathematics assignment.",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee6c3d22f837f1e2c39c476",
                    "memberId": "5ed2bbf7ca1dbc1d6c009635",
                    "memberUsername": "wasiuedet9",
                    "memberCategory": "Student"
                }
            ],
            "createdAt": "2020-06-15T00:41:54.136Z",
            "__v": 0
        }
    }
    ``` 

## Add New Member to Group
* Request:
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/add_new_member
    * Body(application/json)
    ```
    {
        "memberUsername": "musageorge72",
        "memberCategory": "Student"
    }
    ``` 

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully Updated Group",
        "results": 1,
        "data": {
            "admin": {
                "id": "5ed2bbf7ca1dbc1d6c009635",
                "username": "wasiuedet9",
                "category": "Student"
            },
            "_id": "5ee6c3d22f837f1e2c39c475",
            "name": "Mathematics Research Assignment",
            "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Surds Mathematics assignment.",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee6c3d22f837f1e2c39c476",
                    "memberId": "5ed2bbf7ca1dbc1d6c009635",
                    "memberUsername": "wasiuedet9",
                    "memberCategory": "Student"
                },
                {
                    "_id": "5ee6e1236923fa1daceae87f",
                    "memberId": "5ed2bbf7ca1dbc1d6c009636",
                    "memberUsername": "musageorge72",
                    "memberCategory": "Student"
                }
            ],
            "createdAt": "2020-06-15T00:41:54.136Z",
            "__v": 1
        }
    }
    ``` 

## Delete Member From Group
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/remove_member?memberUsername=musageorge72&memberCategory=Student

* Response:
    * Status: 200 - ok
    * Body:(application/json)
    ```
    {
        "status": "success",
        "message": "Member Removed Successfully",
        "results": 1,
        "data": {
            "admin": {
                "id": "5ed2bbf7ca1dbc1d6c009635",
                "username": "wasiuedet9",
                "category": "Student"
            },
            "_id": "5ee6c3d22f837f1e2c39c475",
            "name": "Mathematics Research Assignment",
            "description": "This group is for Senior Secondary School Two students who are interested in collaborating with their fellow classmates on their Surds Mathematics assignment.",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee6c3d22f837f1e2c39c476",
                    "memberId": "5ed2bbf7ca1dbc1d6c009635",
                    "memberUsername": "wasiuedet9",
                    "memberCategory": "Student"
                }
            ],
            "createdAt": "2020-06-15T00:41:54.136Z",
            "__v": 2
        }
    }
    ``` 

## Remove Myself From Group
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/remove_myself

* Response:
    * Status: 200 - ok
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "You are no longer a member of this group.",
        "results": null,
        "data": null
    }
    ``` 

## Delete Group
* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee6c3d22f837f1e2c39c475/

* Response:
    * Status: 204 - no content

## PTA
Each school must have a PTA association, a forum, where parents, stapents and teachers can come together and deliberate on key issues that involve the well-being of the school's students.

This PTA group, is what forms the basis of the PTA group chat.

A PTA group is created automatically for each school upon registration. Thus, there is no need for manual creation.

When a Staff deletes their account on the platform, they automatically exit the PTA Forum  of their school.

When a Stapent deletes their account on the platform, they automatically exit the PTA Forum of their school.

When a Staff registers under a school on the platform, the staff is automatically a member of that school's PTA association.

When a Stapent registers under a school on the platform, the stapent is automatically a member of that school's PTA association.

When a school is deleted from the platform, the PTA is also deleted if it exists.

When a parent registers under a school on the app, the parent automatically joins the PTA group of the school.

When a parent leaves the platform, the parent is automatically removed from the school PTA group.

When a student leaves a school or exits the platform, his or her parent automatically leaves the PTA group of the school, unless the student has a sibling in that school.

## Sample Requests and Responses For PTA Group API

## Retreive School PTA Group Details
* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8d0e79ba18f1fe865844e     

* Response:
    * Status: 200 - ok
    * Body:(application/json)
    ```
    {
        "status": "success",
        "message": "New PTA Group Created Successfully!",
        "results": 1,
        "data": {
            "name": "Hopebay College Parent-Teachers-Association",
            "description": "This Parents-Teachers-Association group, as the name implies, is a forum that is meant to serve the purpose of connecting the Staff and Parents of our great school.",
            "_id": "5ee8d0e79ba18f1fe865844e",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee8d0e79ba18f1fe865844f",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d4",
                    "memberUsername": "bukolaayantola18",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658450",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d5",
                    "memberUsername": "godswillafolabi76",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658451",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d6",
                    "memberUsername": "amaraokoli25",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658452",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d7",
                    "memberUsername": "amakemmuoma15",
                    "memberCategory": "Stapent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658453",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d8",
                    "memberUsername": "bbatundeobasola39",
                    "memberCategory": "Stapent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658454",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d9",
                    "memberUsername": "abuchionyebuchi13",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658455",
                    "memberId": "5ed2baf8ca1dbc1d6c0095db",
                    "memberUsername": "amakeolamide13",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658456",
                    "memberId": "5ed2baf8ca1dbc1d6c0095da",
                    "memberUsername": "aishammaduka13",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658457",
                    "memberId": "5ed2baf8ca1dbc1d6c0095dc",
                    "memberUsername": "samuelbbatunde14",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658458",
                    "memberId": "5ed2baf8ca1dbc1d6c0095dd",
                    "memberUsername": "yemieffiong59",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658459",
                    "memberId": "5ee84a1cc26e61001741a276",
                    "memberUsername": "femivita",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845a",
                    "memberId": "5ecb08e3d2595416f0dc997e",
                    "memberUsername": "chinyerebabatunde",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845b",
                    "memberId": "5ecb08e3d2595416f0dc9981",
                    "memberUsername": "ibukunokeke",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845c",
                    "memberId": "5ecb08e3d2595416f0dc9982",
                    "memberUsername": "musaatanda",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845d",
                    "memberId": "5ecb08e3d2595416f0dc9983",
                    "memberUsername": "amakeobiwuru",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845e",
                    "memberId": "5ecb08e3d2595416f0dc9984",
                    "memberUsername": "jumokemohammed",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845f",
                    "memberId": "5ecb08e3d2595416f0dc9985",
                    "memberUsername": "yemiedet",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658460",
                    "memberId": "5ecb08e3d2595416f0dc9986",
                    "memberUsername": "esthergeorge",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658461",
                    "memberId": "5ecb08e3d2595416f0dc9987",
                    "memberUsername": "chinyereobi",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658462",
                    "memberId": "5ecb08e3d2595416f0dc9989",
                    "memberUsername": "mondayonyebuchi",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658463",
                    "memberId": "5ecb08e3d2595416f0dc9988",
                    "memberUsername": "sophiadoyle",
                    "memberCategory": "Parent"
                }
            ],
            "createdAt": "2020-06-16T14:02:15.952Z",
            "admin": {
                "id": "5ed2baf8ca1dbc1d6c0095d4",
                "username": "bukolaayantola18",
                "category": "Staff"
            },
            "__v": 0
        }
    }
    ``` 

## Update PTA Group Details
* Request:
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8d0e79ba18f1fe865844e
    * Body(application/json)
    ```
    {
        "name": "Hopebay College Parent Teachers Association"
    }
    ``` 

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully Updated PTA Group",
        "results": 1,
        "data": {
            "admin": {
                "id": "5ed2baf8ca1dbc1d6c0095d4",
                "username": "bukolaayantola18",
                "category": "Staff"
            },
            "name": "Hopebay College Parent Teachers Association",
            "description": "This Parents-Teachers-Association group, as the name implies, is a forum that is meant to serve the purpose of connecting the Staff and Parents of our great school.",
            "_id": "5ee8d0e79ba18f1fe865844e",
            "school": "5ecb08dfd2595416f0dc9977",
            "members": [
                {
                    "_id": "5ee8d0e79ba18f1fe865844f",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d4",
                    "memberUsername": "bukolaayantola18",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658450",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d5",
                    "memberUsername": "godswillafolabi76",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658451",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d6",
                    "memberUsername": "amaraokoli25",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658452",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d7",
                    "memberUsername": "amakemmuoma15",
                    "memberCategory": "Stapent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658453",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d8",
                    "memberUsername": "bbatundeobasola39",
                    "memberCategory": "Stapent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658454",
                    "memberId": "5ed2baf8ca1dbc1d6c0095d9",
                    "memberUsername": "abuchionyebuchi13",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658455",
                    "memberId": "5ed2baf8ca1dbc1d6c0095db",
                    "memberUsername": "amakeolamide13",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658456",
                    "memberId": "5ed2baf8ca1dbc1d6c0095da",
                    "memberUsername": "aishammaduka13",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658457",
                    "memberId": "5ed2baf8ca1dbc1d6c0095dc",
                    "memberUsername": "samuelbbatunde14",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658458",
                    "memberId": "5ed2baf8ca1dbc1d6c0095dd",
                    "memberUsername": "yemieffiong59",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658459",
                    "memberId": "5ee84a1cc26e61001741a276",
                    "memberUsername": "femivita",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845a",
                    "memberId": "5ecb08e3d2595416f0dc997e",
                    "memberUsername": "chinyerebabatunde",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845b",
                    "memberId": "5ecb08e3d2595416f0dc9981",
                    "memberUsername": "ibukunokeke",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845c",
                    "memberId": "5ecb08e3d2595416f0dc9982",
                    "memberUsername": "musaatanda",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845d",
                    "memberId": "5ecb08e3d2595416f0dc9983",
                    "memberUsername": "amakeobiwuru",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845e",
                    "memberId": "5ecb08e3d2595416f0dc9984",
                    "memberUsername": "jumokemohammed",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe865845f",
                    "memberId": "5ecb08e3d2595416f0dc9985",
                    "memberUsername": "yemiedet",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658460",
                    "memberId": "5ecb08e3d2595416f0dc9986",
                    "memberUsername": "esthergeorge",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658461",
                    "memberId": "5ecb08e3d2595416f0dc9987",
                    "memberUsername": "chinyereobi",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658462",
                    "memberId": "5ecb08e3d2595416f0dc9989",
                    "memberUsername": "mondayonyebuchi",
                    "memberCategory": "Parent"
                },
                {
                    "_id": "5ee8d0e79ba18f1fe8658463",
                    "memberId": "5ecb08e3d2595416f0dc9988",
                    "memberUsername": "sophiadoyle",
                    "memberCategory": "Parent"
                }
            ],
            "createdAt": "2020-06-16T14:02:15.952Z",
            "__v": 0
        }
    }
    ``` 

## Delete School PTA Group Details

* Request:
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8d0e79ba18f1fe865844e

* Response:
    * Status: 204 - no content

## DUO
A DUO Group is a group meant for only two individuals. It is meant to provide the foundation for one on one chat.

When a school is created, a member list is created automatically for the school, which gets updated anytime a staff, stapent, student and parent connected to that school, gets registered or deleted.

A user who is connected to a school can make a request to another user connected to thesame school to form a duo group. Users are notified of requests and no user can form a duo group with a member of another school.

Requested users can decline requests to form duo groups. Requesting users recieve a notification, anytime their request is declined.

When a requested user accepts a request to form a duo group, the duo group is then automatically created and the requesting user is notified.

A requesting user can cancel the request to form a DUO group, if the requested user has not yet responded.

A user can disable any duo group that they belong to. Their partner will be notified of the action.

Users can see all their disabled DUO groups.

A user can re-enable any duo group that they have previously disabled. Their partner will be notified of the action.

A School-Administrator or Parent_School-Administrator or Principal or Parent_Principal delete any DUO group that is formed within their school domain. The group members will be notified of the action.

Users can not make multiple requests to another user form a DUO group, when their last request to that same user is still pending (neither declined nor accepted).

Users cannot form DUO groups with themeselves, neither can they respond to their own requests.

Major operations cannot be performed on disabled groups, untill they are enabled.

A School-Administrator or Parent_School-Administrator or Principal or Parent_Principal can see all the DUO groups within their school.

Users can see all their active DUO groups(non-disabled or enabled groups).

A specific DUO group (both enabled and disabled) can be retrieved.

School-Administrators or Parent_School-Administrators can prevent a pair of users from ever forming a DUO group, by blacklisting them. The two users would be notified of this event.

School-Administrators or Parent_School-Administrators can always delete a blacklist, thus allowing the pair of users to form a DUO group. The two usrs would be notified that they can now form a DUO group. 

School-Administrators or Parent_School-Administrators can retrieve their school's blacklists, as well as a specific blacklist.

School-Administrators or Parent_School-Administrators cannot blacklist users that do not belong to their school.

Users can see all their pending requests to form a DUO group.

## Sample Requests and Responses For DUO Group API

## Request To Form A DUO Group

* Request:
    * Endpoint: POST//api/v1/schools/5eec015f91083c10c8ff5cd2/duo/request?id=5eec0be13dea180de83c3c8d&username=Pan10&category=Staff

* Response:
    * Status: 200c - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "Your request to form a duo group has been sent to Pan10"
    }
    ```  

## My Pending Requests To Form A DUO Group
* Request:
    * Endpoint:GET/api/v1/users/me/my_pending_requests_to_form_duo_group

* Response:
    * Status: 200 - OK
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "Successfully retrieved all your pending requests to form a DUO group",
        "results": 2,
        "data": [
            {
                "recipientUsername": "ritamonday63",
                "recipientCategory": "Student"
            },
            {
                "recipientUsername": "moseseze80",
                "recipientCategory": "Staff"
            }
        ]
    }
    ```

## Decline Request To Form DUO Group

* Request:
    * Endpoint: POST/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/decline_request?id=5eec13c8703e9013c4f66ee3&username=amaakwukwuma90&category=Student

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "Your declining message to form a duo group has been sent to amaakwukwuma90"
    }
    ``` 

## Accept Request To Form DUO Group

* Request:
    * Endpoint: POST/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/accept_request?id=5eec13c8703e9013c4f66ee3&username=amaakwukwuma90&category=Student

* Response:
    * Status: 201 - created
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Duo Group Created Successfully",
        "results": 1,
        "data": {
            "_id": "5eeccbd132a0e40b448e19e5",
            "school": "5eec015f91083c10c8ff5cd2",
            "createdAt": "2020-06-19T14:29:37.867Z",
            "members": [
                {
                    "_id": "5eeccbd132a0e40b448e19e6",
                    "memberId": "5eec0be13dea180de83c3c8d",
                    "memberUsername": "Pan10",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5eeccbd132a0e40b448e19e7",
                    "memberId": "5eec13c8703e9013c4f66ee3",
                    "memberUsername": "amaakwukwuma90",
                    "memberCategory": "Student"
                }
            ],
            "__v": 0
        }
    }
    ``` 

## Disable DUO Group

* Request:
    * Endpoint: PATCH/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5eed12ccd96a0904a82f8aaa/disable

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "Successfully disabled the duo group."
    }
    ```

## Re-enable DUO Group

* Request:
    * Endpoint: PATCH/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5eed12ccd96a0904a82f8aaa/enable

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "Success",
        "message": "Successfully re-enabled the duo group."
    }
    ``` 

## Delete DUO Group

* Request:
    * Endpoint: DELETE/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5eed12ccd96a0904a82f8aaa/

* Response:
    * Status: 240 - no content 

## Retrieve All School DUO Groups

* Request:
    * Endpoint: GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Retrieved all the DUO groups in your school",
        "results": 2,
        "data": [
            {
                "isEnabled": true,
                "_id": "5ef000b1ddaf42153429a51e",
                "school": "5eec015f91083c10c8ff5cd2",
                "createdAt": "2020-06-22T00:52:01.673Z",
                "members": [
                    {
                        "_id": "5ef000b1ddaf42153429a51f",
                        "memberId": "5eec0be13dea180de83c3c8d",
                        "memberUsername": "Pan10",
                        "memberCategory": "Staff"
                    },
                    {
                        "_id": "5ef000b1ddaf42153429a520",
                        "memberId": "5eec13c8703e9013c4f66ee3",
                        "memberUsername": "amaakwukwuma90",
                        "memberCategory": "Student"
                    }
                ],
                "__v": 0
            },
            {
                "isEnabled": true,
                "_id": "5ef09b36a6735b1594a17dfe",
                "school": "5eec015f91083c10c8ff5cd2",
                "createdAt": "2020-06-22T11:51:18.056Z",
                "members": [
                    {
                        "_id": "5ef09b36a6735b1594a17dff",
                        "memberId": "5eec2a48ec204d0844fca0fe",
                        "memberUsername": "Patience24",
                        "memberCategory": "Parent"
                    },
                    {
                        "_id": "5ef09b36a6735b1594a17e00",
                        "memberId": "5eec13c8703e9013c4f66ee3",
                        "memberUsername": "amaakwukwuma90",
                        "memberCategory": "Student"
                    }
                ],
                "__v": 0
            }
        ]
    }
    ```  

## Retrieve All My Enabled DUO Groups:

* Request:
    * Endpoint: GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/active_duo_groups

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully retrieved all your active duo groups",
        "results": 2,
        "data": [
            {
                "isEnabled": true,
                "_id": "5ef000b1ddaf42153429a51e",
                "school": "5eec015f91083c10c8ff5cd2",
                "createdAt": "2020-06-22T00:52:01.673Z",
                "members": [
                    {
                        "_id": "5ef000b1ddaf42153429a51f",
                        "memberId": "5eec0be13dea180de83c3c8d",
                        "memberUsername": "Pan10",
                        "memberCategory": "Staff"
                    },
                    {
                        "_id": "5ef000b1ddaf42153429a520",
                        "memberId": "5eec13c8703e9013c4f66ee3",
                        "memberUsername": "amaakwukwuma90",
                        "memberCategory": "Student"
                    }
                ],
                "__v": 0
            },
            {
                "isEnabled": true,
                "_id": "5ef09b36a6735b1594a17dfe",
                "school": "5eec015f91083c10c8ff5cd2",
                "createdAt": "2020-06-22T11:51:18.056Z",
                "members": [
                    {
                        "_id": "5ef09b36a6735b1594a17dff",
                        "memberId": "5eec2a48ec204d0844fca0fe",
                        "memberUsername": "Patience24",
                        "memberCategory": "Parent"
                    },
                    {
                        "_id": "5ef09b36a6735b1594a17e00",
                        "memberId": "5eec13c8703e9013c4f66ee3",
                        "memberUsername": "amaakwukwuma90",
                        "memberCategory": "Student"
                    }
                ],
                "__v": 0
            }
        ]
    }
    ``` 
## Retrieve Specific DUO Group

* Request:
    * Endpoint: GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully Retrieved The Duo Group",
        "results": 1,
        "data": {
            "isEnabled": true,
            "_id": "5ef000b1ddaf42153429a51e",
            "school": "5eec015f91083c10c8ff5cd2",
            "createdAt": "2020-06-22T00:52:01.673Z",
            "members": [
                {
                    "_id": "5ef000b1ddaf42153429a51f",
                    "memberId": "5eec0be13dea180de83c3c8d",
                    "memberUsername": "Pan10",
                    "memberCategory": "Staff"
                },
                {
                    "_id": "5ef000b1ddaf42153429a520",
                    "memberId": "5eec13c8703e9013c4f66ee3",
                    "memberUsername": "amaakwukwuma90",
                    "memberCategory": "Student"
                }
            ],
            "__v": 0
        }
    }
    ``` 

## Cancel Request To Form A DUO Group

* Request:
    * Endpoint: DELETE/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/cancel/request?id=5eec13c8703e9013c4f66ee3&username=amaakwukwuma90&category=Student

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Your request has been successfully cancelled.",
        "results": 1,
        "data": {
            "sender": {
                "username": "Peter10",
                "category": "Staff"
            },
            "recipient": {
                "id": "5eec13c8703e9013c4f66ee3",
                "username": "amaakwukwuma90",
                "category": "Student"
            },
            "hasBeenRead": false,
            "_id": "5ef101a57be2611a6c36ddcf",
            "school": "5eec015f91083c10c8ff5cd2",
            "createdAt": "2020-06-22T19:08:21.339Z",
            "subject": "Let Us Form A Duo Group",
            "description": "Peter10, a Staff from Orient Academy, located at 30, Old Lagos Asaba Road, Agbor, Delta wants the both of you to form a duo group. You are at liberty to accept or decline the request.",
            "senderId": "5eea5fb63da930162c9aaf93",
            "__v": 0
        }
    }
    ```  
## Blacklist Users From Forming A DUO Group

* Request:
    * Endpoint: POST/api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists
    * Body(application/json)
    ```
    {
    "description": "These two users were found guily of sex chatting.",
    "memberOneUsername": "Peter10",
    "memberOneCategory": "Staff",
    "memberTwoUsername": "amaakwukwuma90",
    "memberTwoCategory": "Student"
    }
    ``` 
* Response:
    * Status: 201 - created
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully Blacklisted The DUO",
        "results": 1,
        "data": {
            "_id": "5ef0c27ebc38020d70346c07",
            "school": "5eec015f91083c10c8ff5cd2",
            "memberOne": {
                "memberOneUsername": "Peter10",
                "memberOneCategory": "Staff"
            },
            "memberTwo": {
                "memberTwoUsername": "amaakwukwuma90",
                "memberTwoCategory": "Student"
            },
            "description": "These two users were found guily of sex chatting.",
            "__v": 0
        }
    }
    ``` 

## Delete A Blacklist

* Request:
    * Endpoint: DELETE//api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists/5ef0c27ebc38020d70346c07

* Response:
    * Status: 204 - no content

## Retrieve All Blacklists For Specific School

* Request:
    * Endpoint: GET/api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists
    
* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully retrieved all the blacklists for your school",
        "results": 2,
        "data": [
            {
                "memberOne": {
                    "memberOneUsername": "Peter10",
                    "memberOneCategory": "Staff"
                },
                "memberTwo": {
                    "memberTwoUsername": "amaakwukwuma90",
                    "memberTwoCategory": "Student"
                },
                "_id": "5ef1762011e59811f89ba3b5",
                "school": "5eec015f91083c10c8ff5cd2",
                "description": "These two users were found guily of sex chatting.",
                "__v": 0
            },
            {
                "memberOne": {
                    "memberOneUsername": "Peter10",
                    "memberOneCategory": "Staff"
                },
                "memberTwo": {
                    "memberTwoUsername": "Patience24",
                    "memberTwoCategory": "Parent"
                },
                "_id": "5ef1780cfcb2141e9ce50a74",
                "school": "5eec015f91083c10c8ff5cd2",
                "description": "These two users were found guily of violent communication.",
                "__v": 0
            }
        ]
    }
    ```  

## Retrieve Specific Blacklist

* Request:
    * Endpoint: GET/api/v1/schools/5eec015f91083c10c8ff5cd2/blacklists/5ef1762011e59811f89ba3b5

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Blacklist retrieved successfully",
        "results": 1,
        "data": {
            "memberOne": {
                "memberOneUsername": "Peter10",
                "memberOneCategory": "Staff"
            },
            "memberTwo": {
                "memberTwoUsername": "amaakwukwuma90",
                "memberTwoCategory": "Student"
            },
            "_id": "5ef1762011e59811f89ba3b5",
            "school": "5eec015f91083c10c8ff5cd2",
            "description": "These two users were found guily of sex chatting.",
            "__v": 0
        }
    }
    ``` 

## Chat Features

There are five main categories of chatting within the application:

* [General School Chat Forum](#general-school-chat-forum)
* [Classroom Chat Forum](#classroom-chat-forum)
* [Group Chat](#group-chat)
* [PTA Chat Forum](#pta-chat-forum)
* [One on One Chat](#one-on-one-chat)

It should be noted that every data being emitted and received, is in JSON format.

## General School Chat Forum
Each school has it's own chat forum, mainly for the purpose of allowing the school management to reach everyone connected to the school in one place.

Anyone can be a member of this forum, provided you are connected to the school, either as a staff, stapent or as a student or finally, as a parent.

Only members of a school forum, can see the school forum's conversations.

When a message is sent to the school forum, the message is saved to the database for backup purposes.

The messages of a school forum can be retrieved, updated and destroyed.

Only the creator of a message in the school forum and the school management (School-Administrator, Principal and Vice-Principal or Parent_School-Administrator, Parent_Principal and Parent_Vice-Principal) have the right to update and delete the message.

Only logged in individuals who are connected to the school can send messages to that school forum.

## Web Socket Events Workflow For General School Chat Forum
* A socket connection is established, once a user is on a views(User Interface) meant for chatting.
  
* The client needs to emit a **joinSchool** event, along with the user's details which should contain his or her username and school (unique schoolId).
* The data being sent from client to server needs to look like this: {username: "myUsername": school: "5ecb08dfd2595416f0dc9977"} 
* Immediately, the user is added to the school forum.
  
* Next, a **message** event, is emitted from the server to the client in order to display a welcome message to the user who just joined the forum.
* The data being sent looks like this: {username: "Universal School System", text: "welcome", time: "7:15 PM"}
 
* Following this, another **message** event is emitted from the server to all the clients in the forum in order to display a message to everyone except the new client that the user has just joined the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has joined the chat", time: "7:15 PM"}

* Then, a **schoolUsers** event is emitted from the server to the client, sending along the school id and the usernames of all the people who are in the school forum. The purpose of this is to display this information on the user interface.
* The data being sent looks like this: {school: "5ecb08dfd2595416f0dc9977", users: ["myUsername", "anotherUsername", "stillAnotherUsername"]}

* When a user sends a message to the forum, the **chatMessage** event is emitted from the client to the server, along with a message variable.
* The message variable contains data like this: "There will be a mid-term break starting from Friday this week, till Tuesday next week".

* Then a **message** event is again emitted from the server to the client, in order to display the message to everyone in the forum.
* The data being sent looks like this: {username: "bukolaayantola18", text: "There will be a mid-term break starting from Friday this week, till Tuesday next week", time: "8:20 AM"}

* When a user leaves the forum, a **disconnect** event is received on the server.
 
* Then a **message** event is emitted from the server to the client in order to alert everyone that the user has left the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has left the chat", time: "9:40 PM"}

* Finally a **schoolUsers** event is emitted from the server to the client in order to refresh and update the list of people who are currently chatting in the forum.
* The data being sent looks like this: {school: "5ecb08dfd2595416f0dc9977", users: ["anotherUsername", "stillAnotherUsername"]} 


## CRUD Operations: Sample API Requests and Responses For General School Chat

## Create Message:

* Request
    * Endpoint: POST/api/v1/school/5ecb08dfd2595416f0dc9977/chats
    * Body(application/json)
    ```
    {
        "text": "I officially welcome you all to a new term. Hope you're all ready for a new round of academic activities? This term holds great promise for all of us."
    }
    ``` 

* Response
    * Status: 201 - created
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "Message Saved!",
        "results": 1,
        "data": {
            "_id": "5ee381872e0f06116c10b4a2",
            "text": "I officially welcome you all to a new term. Hope you're all ready for a new round of academic activities? This term holds great promise for all of us.",
            "username": "bukolaayantola18",
            "time": "2020-06-12T13:22:15.314Z",
            "formattedTime": "23:15 pm",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Staff",
            "userRole": "Principal",
            "userId": "5ed2baf8ca1dbc1d6c0095d4",
            "__v": 0
        }
    }
    ``` 

## Retrieve Messages

* Request:
    * Endpoint: GET/api/v1/school/5ecb08dfd2595416f0dc9977/chats 

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Messages Retrieved Successfully!",
        "results": 3,
        "data": [
            {
                "_id": "5ee381872e0f06116c10b4a2",
                "text": "I officially welcome you all to a new term. Hope you're all ready for a new round of academic activities? This term holds great promise for all of us.",
                "username": "bukolaayantola18",
                "time": "2020-06-12T13:22:15.314Z",
                "formattedTime": "23:15 pm",
                "school": "5ecb08dfd2595416f0dc9977",
                "userCategory": "Staff",
                "userRole": "Principal",
                "userId": "5ed2baf8ca1dbc1d6c0095d4",
                "__v": 0
            },
            {
                "_id": "5ee39a9c2e0f06116c10b4a3",
                "text": "I am fully pumped up for a new school session.",
                "username": "amandababatunde68",
                "time": "2020-06-12T15:09:16.583Z",
                "formattedTime": "10:16 am",
                "school": "5ecb08dfd2595416f0dc9977",
                "userCategory": "Student",
                "userRole": "Student",
                "userId": "5ed2bbf7ca1dbc1d6c00962e",
                "__v": 0
            },
            {
                "_id": "5ee39bb72e0f06116c10b4a4",
                "text": "I am grateful to the school staff for taking good care of my children throughout the last school session.",
                "username": "chinyerebabatunde",
                "time": "2020-06-12T15:13:59.323Z",
                "formattedTime": "16:14 pm",
                "school": "5ecb08dfd2595416f0dc9977",
                "userCategory": "Parent",
                "userRole": "Parent",
                "userId": "5ecb08e3d2595416f0dc997e",
                "__v": 0
            }
        ]
    }
    ```

## Retrieve Message

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/chats/5ee381872e0f06116c10b4a2

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Retrieved Successfully",
        "results": 1,
        "data": {
            "_id": "5ee381872e0f06116c10b4a2",
            "text": "I officially welcome you all to a new term. Hope you're all ready for a new round of academic activities? This term holds great promise for all of us.",
            "username": "bukolaayantola18",
            "time": "2020-06-12T13:22:15.314Z",
            "formattedTime": "23:15 pm",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Staff",
            "userRole": "Principal",
            "userId": "5ed2baf8ca1dbc1d6c0095d4",
            "__v": 0
        }
    }
    ``` 

## Update Message

* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/chats/5ee381872e0f06116c10b4a2
    * Body(application/json)
    ```
    {
        "text": "I welcome you all to a new session."
    }
    ``` 

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Updated Successfully",
        "results": 1,
        "data": {
            "_id": "5ee381872e0f06116c10b4a2",
            "text": "I welcome you all to a new session.",
            "username": "bukolaayantola18",
            "time": "2020-06-12T13:22:15.314Z",
            "formattedTime": "23:15 pm",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Staff",
            "userRole": "Principal",
            "userId": "5ed2baf8ca1dbc1d6c0095d4",
            "__v": 0
        }
    }
    ```

## Delete Message

* Request
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/chats/5ee381872e0f06116c10b4a2

* Response
    * Status: 204 - no content


## Classroom Chat Forum
Each classroom in a school has it's own chat forum, mainly for the purpose of connecting the classroom teachers and students.

Only students and teachers of the classroom can be a member of the classroom's chat forum.

Only members of the classroom forum, can see the classroom's conversations.

When a message is sent to the classroom forum, the message is saved to the database for backup purposes.

The messages of a classroom forum can be retrieved, updated and destroyed.

Only the creator of a message in the classroom forum, the class Form-Teacher or Parent_Form-Teacher and the school management (School-Administrator, Principal and Vice-Principal or Parent_School-Administrator, Parent_Principal and Parent_Vice-Principal) have the right to update and delete the message.

Only logged in individuals who are connected to the classroom can send messages to that class forum.

## Web Socket Events Workflow For General School Chat Forum
* A socket connection is established, once a user is on a views(User Interface) meant for chatting.
  
* The client needs to emit a **joinClassroom** event, along with the user's details which should contain his or her username and classroom (unique classId).
* The data being sent from client to server needs to look like this: {username: "myUsername": classroom: "5ed503549d420d1d3849a079"} 
* Immediately, the user is added to the classroom forum.
  
* Next, a **message** event, is emitted from the server to the client in order to display a welcome message to the user who just joined the forum.
* The data being sent looks like this: {username: "Universal School System", text: "welcome", time: "5:05 PM"}
 
* Following this, another **message** event is emitted from the server to all the clients in the forum in order to display a message to everyone except the new client that the user has just joined the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has joined the chat", time: "7:15 PM"}

* Then, a **classroomStudents** event is emitted from the server to the client, sending along the classroom id and the usernames of all the people who are in the classroom forum. The purpose of this is to display this information on the user interface.
* The data being sent looks like this: {classroom: "5ed503549d420d1d3849a079", students: ["myUsername", "anotherUsername", "stillAnotherUsername"]}

* When a user sends a message to the forum, the **chatMessage** event is emitted from the client to the server, along with a message variable.
* The message variable contains data like this: "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any.".

* Then a **message** event is again emitted from the server to the client, in order to display the message to everyone in the forum.
* The data being sent looks like this: {username: "bukolaayantola18", text: "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any.", time: "8:20 AM"}

* When a user leaves the forum, a **disconnect** event is received on the server.
 
* Then a **message** event is emitted from the server to the client in order to alert everyone that the user has left the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has left the chat", time: "9:40 PM"}

* Finally a **classroomStudents** event is emitted from the server to the client in order to refresh and update the list of people who are currently chatting in the forum.
* The data being sent looks like this: {classroom: "5ed503549d420d1d3849a079", students: ["anotherUsername", "stillAnotherUsername"]} 


## CRUD Operations: Sample API Requests and Responses For Classroom Forum Chats

## Create Message:

* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats
    * Body(application/json)
    ```
    {
        "text": "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any."
    }
    ``` 

* Response
    * Status: 201 - created
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "Message Saved!",
        "results": 1,
        "data": {
            "_id": "5ee4c2469d276c1638e4720b",
            "text": "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any.",
            "username": "godswillafolabi76",
            "time": "2020-06-13T12:10:46.850Z",
            "formattedTime": "13:10 pm",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Staff",
            "userRole": "Vice-Principal",
            "userId": "5ed2baf8ca1dbc1d6c0095d5",
            "classId": "5ed503549d420d1d3849a079",
            "__v": 0
        }
    }
    ``` 

## Retrieve Messages

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Messages Retrieved Successfully!",
        "results": 2,
        "data": [
            {
                "_id": "5ee4cb3e668ef404bcf67dff",
                "text": "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any.",
                "username": "godswillafolabi76",
                "time": "2020-06-13T12:49:02.174Z",
                "formattedTime": "13:49 pm",
                "school": "5ecb08dfd2595416f0dc9977",
                "userCategory": "Staff",
                "userRole": "Vice-Principal",
                "userId": "5ed2baf8ca1dbc1d6c0095d5",
                "classId": "5ed503549d420d1d3849a079",
                "__v": 0
            },
            {
                "_id": "5ee4cb73668ef404bcf67e00",
                "text": "I just finished mastering the latest lecture resource on advanced trigonometry. It was an enlightening study.",
                "username": "wasiuedet9",
                "time": "2020-06-13T12:49:55.238Z",
                "formattedTime": "13:49 pm",
                "school": "5ecb08dfd2595416f0dc9977",
                "userCategory": "Student",
                "userRole": "Student",
                "userId": "5ed2bbf7ca1dbc1d6c009635",
                "classId": "5ed503549d420d1d3849a079",
                "__v": 0
            }
        ]
    }
    ```

## Retrieve Message

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats/5ee4cb3e668ef404bcf67dff

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Retrieved Successfully",
        "results": 1,
        "data": {
            "_id": "5ee4cb3e668ef404bcf67dff",
            "text": "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any.",
            "username": "godswillafolabi76",
            "time": "2020-06-13T12:49:02.174Z",
            "formattedTime": "13:49 pm",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Staff",
            "userRole": "Vice-Principal",
            "userId": "5ed2baf8ca1dbc1d6c0095d5",
            "classId": "5ed503549d420d1d3849a079",
            "__v": 0
        }
    }
    ``` 

## Update Message

* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats/5ee4cb3e668ef404bcf67dff
    * Body(application/json)
    ```
    {
        "text": "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any. There will be a test on this lecture on Wednesday."
    }
    ``` 

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
    "status": "success",
    "message": "Message Updated Successfully",
    "results": 1,
    "data": {
        "_id": "5ee4cb3e668ef404bcf67dff",
        "text": "Hey everyone. I have uploaded a lecture resource for you all. Please ensure to master the material and give me feedback if you have any. There will be a test on this lecture on Wednesday.",
        "username": "godswillafolabi76",
        "time": "2020-06-13T12:49:02.174Z",
        "formattedTime": "13:49 pm",
        "school": "5ecb08dfd2595416f0dc9977",
        "userCategory": "Staff",
        "userRole": "Vice-Principal",
        "userId": "5ed2baf8ca1dbc1d6c0095d5",
        "classId": "5ed503549d420d1d3849a079",
        "__v": 0
    }
}
    ```

## Delete Message

* Request
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/classes/5ed503549d420d1d3849a079/chats/5ee4cb3e668ef404bcf67dff

* Response
    * Status: 204 - no content


## Group Chat
Individuals in a school, can come together to engage in group chatting. Both students and teachers can chat in thesame group and there are no classroom limitations.

Any member of the group itself can send a message to the group's chat forum.

Only members of the group's forum, can see the group's conversations.

When a message is sent to the group forum, the message is saved to the database for backup purposes.

The messages of a group forum can be retrieved, updated and destroyed.

Only the creator of a message in the group forum, the group admin and the school management (School-Administrator, Principal and Vice-Principal or Parent_School-Administrator, Parent_Principal and Parent_Vice-Principal) have the right to update and delete the message.

Only logged in individuals who are connected to the group can send messages to that group forum.

## Web Socket Events Workflow For Group Chat Forum
* A socket connection is established, once a user is on a views(User Interface) meant for chatting.
  
* The client needs to emit a **joinGroup** event, along with the user's details which should contain his or her username and group (unique groupId).
* The data being sent from client to server needs to look like this: {username: "myUsername": group: "5ed503549d420d1d3849a079"} 
* Immediately, the user is added to the group forum.
  
* Next, a **message** event, is emitted from the server to the client in order to display a welcome message to the user who just joined the forum.
* The data being sent looks like this: {username: "Universal School System", text: "welcome", time: "5:05 PM"}
 
* Following this, another **message** event is emitted from the server to all the clients in the forum in order to display a message to everyone except the new client that the user has just joined the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has joined the chat", time: "7:15 PM"}

* Then, a **groupMembers** event is emitted from the server to the client, sending along the group id and the usernames of all the people who are in the group forum. The purpose of this is to display this information on the user interface.
* The data being sent looks like this: {group: "5ed503549d420d1d3849a079", groupMembers: ["myUsername", "anotherUsername", "stillAnotherUsername"]}

* When a user sends a message to the forum, the **chatMessage** event is emitted from the client to the server, along with a message variable.
* The message variable contains data like this: "Hello guys. How is everyone doing today? I heard that this assignment is also going to be one of our exam questions.".

* Then a **message** event is again emitted from the server to the client, in order to display the message to everyone in the forum.
* The data being sent looks like this: {username: "wasiuedet9", text: "Hello guys. How is everyone doing today? I heard that this assignment is also going to be one of our exam questions.", time: "8:20 AM"}

* When a user leaves the forum, a **disconnect** event is received on the server.
 
* Then a **message** event is emitted from the server to the client in order to alert everyone that the user has left the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has left the chat", time: "9:40 PM"}

* Finally a **groupMembers** event is emitted from the server to the client in order to refresh and update the list of people who are currently chatting in the forum.
* The data being sent looks like this: {group: "5ed503549d420d1d3849a079", groupMembers: ["anotherUsername", "stillAnotherUsername"]} 


## CRUD Operations: Sample API Requests and Responses For Group Chat

## Create Message:

* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats
    * Body(application/json)
    ```
    {
        "text": "Hello guys. How is everyone doing today? I heard that this assignment is also going to be one of our exam questions."   
    }
    ``` 

* Response
    * Status: 201 - created
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "Message Saved!",
        "results": 1,
        "data": {
            "_id": "5ee841d7dd34471c5c063b30",
            "text": "Hello guys. How is everyone doing today? I heard that this assignment is also going to be one of our exam questions.",
            "username": "wasiuedet9",
            "time": "2020-06-16T03:51:51.243Z",
            "formattedTime": "4:51 am",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Student",
            "userRole": "Student",
            "userId": "5ed2bbf7ca1dbc1d6c009635",
            "groupId": "5ee7b1b905d98f1ae03e84bf",
            "__v": 0
        }
    }
    ``` 

## Retrieve Messages

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
    "status": "success",
    "message": "Messages Retrieved Successfully!",
    "results": 2,
    "data": [
        {
            "_id": "5ee841d7dd34471c5c063b30",
            "text": "Hello guys. How is everyone doing today? I heard that this assignment is also going to be one of our exam questions.",
            "username": "wasiuedet9",
            "time": "2020-06-16T03:51:51.243Z",
            "formattedTime": "4:51 am",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Student",
            "userRole": "Student",
            "userId": "5ed2bbf7ca1dbc1d6c009635",
            "groupId": "5ee7b1b905d98f1ae03e84bf",
            "__v": 0
        },
        {
            "_id": "5ee84372dd34471c5c063b32",
            "text": "Yea. It's true. All the more reason to take this assignment seriously.",
            "username": "musageorge72",
            "time": "2020-06-16T03:58:42.134Z",
            "formattedTime": "4:58 am",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Student",
            "userRole": "Student",
            "userId": "5ed2bbf7ca1dbc1d6c009636",
            "groupId": "5ee7b1b905d98f1ae03e84bf",
            "__v": 0
        }
    ]
    ```

## Retrieve Message

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats/5ee84372dd34471c5c063b32

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Retrieved Successfully",
        "results": 1,
        "data": {
            "_id": "5ee84372dd34471c5c063b32",
            "text": "Yea. It's true. All the more reason to take this assignment seriously.",
            "username": "musageorge72",
            "time": "2020-06-16T03:58:42.134Z",
            "formattedTime": "4:58 am",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Student",
            "userRole": "Student",
            "userId": "5ed2bbf7ca1dbc1d6c009636",
            "groupId": "5ee7b1b905d98f1ae03e84bf",
            "__v": 0
        }
    }
    ``` 

## Update Message

* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats/5ee84372dd34471c5c063b32
    * Body(application/json)
    ```
    {
        "text": "Yea. It's true. All the more reason to take this assignment seriously. I heard that we will be submitting this assignment on Friday."
    }
    ``` 

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Updated Successfully",
        "results": 1,
        "data": {
            "_id": "5ee84372dd34471c5c063b32",
            "text": "Yea. It's true. All the more reason to take this assignment seriously. I heard that we will be submitting this assignment on Friday.",
            "username": "musageorge72",
            "formattedTime": "4:58 am",
            "time": "2020-06-16T03:58:42.134Z",\
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Student",
            "userRole": "Student",
            "userId": "5ed2bbf7ca1dbc1d6c009636",
            "groupId": "5ee7b1b905d98f1ae03e84bf",
            "__v": 0
        }
    }
    ```

## Delete Message

* Request
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats/5ee84372dd34471c5c063b32

* Response
    * Status: 204 - no content

## PTA Chat Forum

## Pta Group Chat
Staff, Stapents and Parents of a school, can come together to engage in civilized discussions. Students are not allowed in this forum.

Any staff or parent or stapent of the school can send messages to the forum.

Only members of the forum, can see the PTA's conversations.

When a message is sent to the PTA group forum, the message is saved to the database for backup purposes.

These messages can be retrieved, updated and destroyed.

Only the creator of a message in the PTA forum, and the school management (School-Administrator, Principal and Vice-Principal or Parent_School-Administrator, Parent_Principal and Parent_Vice-Principal) have the right to update and delete the message.

Only logged in individuals who are connected to the PTA forum can send messages to that forum.

## Web Socket Events Workflow For Pta Chat Forum
* A socket connection is established, once a user is on a views(User Interface) meant for chatting.
  
* The client needs to emit a **joinPta** event, along with the user's details which should contain his or her username and group (unique ptaId).
* The data being sent from client to server needs to look like this: {username: "myUsername": schoolPta: "5ed503549d420d1d3849a079"} 
* Immediately, the user is added to the pta group forum.
  
* Next, a **message** event, is emitted from the server to the client in order to display a welcome message to the user who just joined the forum.
* The data being sent looks like this: {username: "Universal School System", text: "welcome", time: "5:05 PM"}
 
* Following this, another **message** event is emitted from the server to all the clients in the forum in order to display a message to everyone except the new client that the user has just joined the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has joined the chat", time: "7:15 PM"}

* Then, a **schoolPtaMembers** event is emitted from the server to the client, sending along the pta id and the usernames of all the people who are in the pta group forum. The purpose of this is to display this information on the user interface.
* The data being sent looks like this: {schoolPta: "5ed503549d420d1d3849a079", schoolPtaMembers: ["myUsername", "anotherUsername", "stillAnotherUsername"]}

* When a user sends a message to the forum, the **chatMessage** event is emitted from the client to the server, along with a message variable.
* The message variable contains data like this: "Good afternoon everyone. Welcome to today's meeting.".

* Then a **message** event is again emitted from the server to the client, in order to display the message to everyone in the forum.
* The data being sent looks like this: {username: "bukolaayantola18", text: "Good afternoon everyone. Welcome to today's meeting.", time: "8:20 AM"}

* When a user leaves the forum, a **disconnect** event is received on the server.
 
* Then a **message** event is emitted from the server to the client in order to alert everyone that the user has left the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has left the chat", time: "9:40 PM"}

* Finally a **schoolPtaMembers** event is emitted from the server to the client in order to refresh and update the list of people who are currently chatting in the forum.
* The data being sent looks like this: {schoolPta: "5ed503549d420d1d3849a079", schoolPtaMembers: ["anotherUsername", "stillAnotherUsername"]} 


## CRUD Operations: Sample API Requests and Responses For PTA Group Chat

## Create Message:

* Request
    * Endpoint: POST/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats
    * Body(application/json)
    ```
    {
    "text": "Good afternoon everyone. Welcome to today's meeting."  
    }
    ``` 

* Response
    * Status: 201 - created
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "Message Saved!",
        "results": 1,
        "data": {
            "_id": "5ee969a65f02e71794e03c89",
            "text": "Good afternoon everyone. Welcome to today's meeting.",
            "username": "bukolaayantola18",
            "time": "2020-06-17T00:53:58.829Z",
            "formattedTime": "1:53 am",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Staff",
            "userRole": "Principal",
            "userId": "5ed2baf8ca1dbc1d6c0095d4",
            "ptaId": "5ee8dc3a26efbc1ce4a93653",
            "__v": 0
        }
    }
    ``` 

## Retrieve Messages

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/groups/5ee7b1b905d98f1ae03e84bf/chats

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Messages Retrieved Successfully!",
        "results": 2,
        "data": [
            {
                "_id": "5ee969a65f02e71794e03c89",
                "text": "Good afternoon everyone. Welcome to today's meeting.",
                "username": "bukolaayantola18",
                "time": "2020-06-17T00:53:58.829Z",
                "formattedTime": "01:53 am",
                "school": "5ecb08dfd2595416f0dc9977",
                "userCategory": "Staff",
                "userRole": "Principal",
                "userId": "5ed2baf8ca1dbc1d6c0095d4",
                "ptaId": "5ee8dc3a26efbc1ce4a93653",
                "__v": 0
            },
            {
                "_id": "5ee96c80e2d7311d58729004",
                "text": "Good afternoon. Thank you for having us.",
                "username": "chinyerebabatunde",
                "time": "2020-06-17T01:06:08.454Z",
                "formattedTime": "02:06 am",
                "school": "5ecb08dfd2595416f0dc9977",
                "userCategory": "Parent",
                "userRole": "Parent",
                "userId": "5ecb08e3d2595416f0dc997e",
                "ptaId": "5ee8dc3a26efbc1ce4a93653",
                "__v": 0
            }
        ]
    }
    ```

## Retrieve Message

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats/5ee96c80e2d7311d58729004

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Retrieved Successfully",
        "results": 1,
        "data": {
            "_id": "5ee96c80e2d7311d58729004",
            "text": "Good afternoon. Thank you for having us.",
            "username": "chinyerebabatunde",
            "time": "2020-06-17T01:06:08.454Z",
            "formattedTime": "02:06 am",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Parent",
            "userRole": "Parent",
            "userId": "5ecb08e3d2595416f0dc997e",
            "ptaId": "5ee8dc3a26efbc1ce4a93653",
            "__v": 0
        }
    }
    ``` 

## Update Message

* Request
    * Endpoint: PATCH/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats/5ee96c80e2d7311d58729004
    * Body(application/json)
    ```
    {
        "text": "Good afternoon. Thank you for having me. You are a gracious host."
    }
    ``` 

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Updated Successfully",
        "results": 1,
        "data": {
            "_id": "5ee96c80e2d7311d58729004",
            "text": "Good afternoon. Thank you for having me. You are a gracious host.",
            "username": "chinyerebabatunde",
            "time": "2020-06-17T01:06:08.454Z",
            "formattedTime": "02:06 am",
            "school": "5ecb08dfd2595416f0dc9977",
            "userCategory": "Parent",
            "userRole": "Parent",
            "userId": "5ecb08e3d2595416f0dc997e",
            "ptaId": "5ee8dc3a26efbc1ce4a93653",
            "__v": 0
        }
    }
    ```

## Delete Message

* Request
    * Endpoint: DELETE/api/v1/schools/5ecb08dfd2595416f0dc9977/pta/5ee8dc3a26efbc1ce4a93653/chats/5ee96c80e2d7311d58729004

* Response
    * Status: 204 - no content



## One on One Chat
Two Individuals connected to thesame school, can come together to chat. It does not matter whether the chatting parties are students or parents or staff, in as much as they are connected to the same school.

For any two individuals to chat, a DUO group must exist for them, as already explained above.

Parents are connected to a school, based on their children.

Only the two members of the DUO group can send messages to each other.

Only the two members of the DUO group, can see each other's messages.

Messages are saved to the database for backup purposes.

The messages of a DUO group can be retrieved, updated and destroyed.

Only the creator of a message, and the school management (School-Administrator, Principal and Vice-Principal or Parent_School-Administrator,Parent_ Principal and Parent_Vice-Principal) have the right to update and delete the message.

## Web Socket Events Workflow For Group Chat Forum
* A socket connection is established, once a user is on a views(User Interface) meant for chatting.
  
* The client needs to emit a **joinChat** event, along with the user's details which should contain his or her username and chatId (unique chatId).
* Please note that the chatId, in this case is thesame as the duoId. Later on, this seeming contradictoriness, will be addressed.
* The data being sent from client to server needs to look like this: {username: "myUsername": chatId: "5ed503549d420d1d3849a079"} 
* Immediately, the user is added to the DUO group chat.
  
* Next, a **message** event, is emitted from the server to the client in order to display a welcome message to the user who just joined the chat.
* The data being sent looks like this: {username: "Universal School System", text: "welcome", time: "5:05 PM"}
 
* Following this, another **message** event is emitted from the server to the other client in the duo group chat in order to display a message, saying that the new user has just joined the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has joined the chat", time: "7:15 PM"}

* Then, a **chatMembers** event is emitted from the server to the client, sending along the chatId and the usernames of the two individuals who are in the duo group chat. The purpose of this is to display this information on the user interface.
* The data being sent looks like this: {chatId: "5ed503549d420d1d3849a079", individuals: ["myUsername", "anotherUsername"]}

* When a user sends a message in the DUO group, the **chatMessage** event is emitted from the client to the server, along with a message variable.
* The message variable contains data like this: "Good morning ama. Please tell me more. What exactly do you want to know?".

* Then a **message** event is again emitted from the server to the client, in order to display the message to the two individuals in the DUO group chat.
* The data being sent looks like this: {username: "Pan10", text: "Good morning ama. Please tell me more. What exactly do you want to know?", time: "8:20 AM"}

* When an individual leaves the chat, a **disconnect** event is received on the server.
 
* Then a **message** event is emitted from the server to the client in order to tell the other individual that the user has left the chat.
* The data being sent looks like this: {username: "Universal School System", text: "myUsername has left the chat", time: "9:40 PM"}

* Finally a **chatMembers** event is once again emitted from the server to the client.
* The data being sent looks like this: {chatId: "5ed503549d420d1d3849a079", individuals: ["anotherUsername"]} 


## CRUD Operations: Sample API Requests and Responses For One on One Chat

## Create Message:

* Request
    * Endpoint: POST/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats
    * Body(application/json)
    ```
    {
        "text": "Good morning ama. Please tell me more. What exactly do you want to know?"
    }
    ``` 

* Response
    * Status: 201 - created
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "Message Saved!",
        "results": 1,
        "data": {
            "_id": "5ef1a1a434f7030db4aa25ea",
            "text": "Good morning ama. Please tell me more. What exactly do you want to know?",
            "username": "Pan10",
            "time": "2020-06-23T06:31:00.825Z",
            "formattedTime": "07:31 am",
            "school": "5eec015f91083c10c8ff5cd2",
            "userCategory": "Staff",
            "userRole": "Principal",
            "userId": "5eec0be13dea180de83c3c8d",
            "duoId": "5ef000b1ddaf42153429a51e",
            "__v": 0
    }

    ``` 

## Retrieve Messages

* Request:
    * Endpoint: GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Messages Retrieved Successfully!",
        "results": 2,
        "data": [
            {
                "_id": "5ef1a13834f7030db4aa25e9",
                "text": "Good morning sir. Please I need some career advice.",
                "username": "amaakwukwuma90",
                "time": "2020-06-23T06:29:12.794Z",
                "formattedTime": "07:29 am",
                "school": "5eec015f91083c10c8ff5cd2",
                "userCategory": "Student",
                "userRole": "Student",
                "userId": "5eec13c8703e9013c4f66ee3",
                "duoId": "5ef000b1ddaf42153429a51e",
                "__v": 0
            },
            {
                "_id": "5ef1a1a434f7030db4aa25ea",
                "text": "Good morning ama. Please tell me more. What exactly do you want to know?",
                "username": "Pan10",
                "time": "2020-06-23T06:31:00.825Z",
                "formattedTime": "07:31 am",
                "school": "5eec015f91083c10c8ff5cd2",
                "userCategory": "Staff",
                "userRole": "Principal",
                "userId": "5eec0be13dea180de83c3c8d",
                "duoId": "5ef000b1ddaf42153429a51e",
                "__v": 0
            }
        ]
    }
    ```

## Retrieve Message

* Request:
    * Endpoint: GET/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats/5ef1a13834f7030db4aa25e9

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Retrieved Successfully",
        "results": 1,
        "data": {
           "_id": "5ef1a13834f7030db4aa25e9",
            "text": "Good morning sir. Please I need some career advice.",
            "username": "amaakwukwuma90",
            "time": "2020-06-23T06:29:12.794Z",
            "formattedTime": "07:29 am",
            "school": "5eec015f91083c10c8ff5cd2",
            "userCategory": "Student",
            "userRole": "Student",
            "userId": "5eec13c8703e9013c4f66ee3",
            "duoId": "5ef000b1ddaf42153429a51e"
        }
    }
    ``` 

## Update Message

* Request
    * Endpoint: PATCH/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats/5ef1a13834f7030db4aa25e9
    * Body(application/json)
    ```
    {
        "text": "Good morning sir. Hope you slept well? Please I need some advice from you about career related issues."
    }
    ``` 

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Message Updated Successfully",
        "results": 1,
        "data": {
            "_id": "5ef1a13834f7030db4aa25e9",
            "text": "Good morning sir. Hope you slept well? Please I need some advice from you about career related issues.",
            "username": "amaakwukwuma90",
            "time": "2020-06-23T06:29:12.794Z",
            "formattedTime": "07:29 am",
            "school": "5eec015f91083c10c8ff5cd2",
            "userCategory": "Student",
            "userRole": "Student",
            "userId": "5eec13c8703e9013c4f66ee3",
            "duoId": "5ef000b1ddaf42153429a51e",
            "__v": 0
        }
    }
    ```

## Delete Message

* Request
    * Endpoint: DELETE/api/v1/schools/5eec015f91083c10c8ff5cd2/duo/5ef000b1ddaf42153429a51e/chats/5ef1a13834f7030db4aa25e9

* Response
    * Status: 204 - no content

[Back to main documentation](README.md)