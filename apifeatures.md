# Special Api Features
There are some features that every API should possess for easy usage and accessibility.

They include:

* [Filtering](#filtering)
* [Sorting](#sorting)
* [Pagination](#pagination)
* [Field Limiting](#field-limiting)

Being a standard API, we have made these features available as well. 

The essence of this documentation is to show you how to interact with the API using the above features.

## Filtering
The purpose of filtering is to enable the api's users to retrieve documents that match the specified input.

For example purposes, we shall be using the endpoint that retrieves all the parents in a school. 

However, note that this filtering feature would work on every endpoint, where multiple documents are being retrieved.

To display the power of filtering, we shall pass through two stages.

1. Retrieve all the parents in a school without filtering
2. Retrieve all the parents in a school with filtering (filter the male stapents that teach mathematics)

Note that by **stapents**, I mean those staff officials who are also parents (have children in the school).

The purpose of this filtering is to return only the parents, who are stapents in the school. 

### Retrieving All The Parents In A School Without Filtering

From the category field of each parent, you can see that users from the Parent and Stapent category are returned.

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9978/

* Response
    * Status: 200 - ok
    * Body: (application/json)
    ```
    {
        "status": "success",
        "message": "Successfully retrieved all parents",
        "results": 11,
        "data": [
            {
                "children": [],
                "role": "Parent",
                "category": "Parent",
                "isVerified": true,
                "_id": "5ecb08e3d2595416f0dc999d",
                "fullname": "Lawrence Constance Mbanefo",
                "email": "lawrencembanefo@hotmail.com",
                "username": "lawrencembanefo",
                "phoneNumber": "+2347072517831",
                "gender": "female",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0
            },
            {
                "children": [],
                "role": "Parent",
                "category": "Parent",
                "isVerified": true,
                "_id": "5ecb08e3d2595416f0dc999e",
                "fullname": "Jumoke Teslim Olasupo",
                "email": "jumokeolasupo@gmail.com",
                "username": "jumokeolasupo",
                "phoneNumber": "+2347072617865",
                "gender": "female",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0
            },
            {
                "children": [],
                "role": "Parent",
                "category": "Parent",
                "isVerified": true,
                "_id": "5ecb08e3d2595416f0dc999f",
                "fullname": "Musa Ebuka Tafawa",
                "email": "musatafawa@hotmail.com",
                "username": "musatafawa",
                "phoneNumber": "+2347072717899",
                "gender": "female",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0
            },
            {
                "children": [],
                "role": "Parent",
                "category": "Parent",
                "isVerified": true,
                "_id": "5ecb08e3d2595416f0dc99a0",
                "fullname": "Echezona Onyeka Omotosho",
                "email": "echezonaomotosho@outlook.com",
                "username": "echezonaomotosho",
                "phoneNumber": "+2347072817933",
                "gender": "female",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0
            },
            {
                "children": [],
                "role": "Parent",
                "category": "Parent",
                "isVerified": true,
                "_id": "5ecb08e3d2595416f0dc99a1",
                "fullname": "Imaobong Teslim Nwafor",
                "email": "imaobongnwafor@aol.com",
                "username": "imaobongnwafor",
                "phoneNumber": "+2348172917967",
                "gender": "female",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0
            },
            {
                "children": [],
                "role": "Parent_Form-Teacher",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c1a",
                "subjects": [
                    "Mathematics",
                    "Accounting"
                ],
                "classes": [
                    "Junior Secondary School Two",
                    "Senior Secondary School Three"
                ],
                "fullname": "Juliet Imaobong Akintunde",
                "email": "julietakintunde@outlook.com",
                "username": "julietakintunde1",
                "phoneNumber": "+2349073818273",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            },
            {
                "children": [],
                "role": "Parent_Principal",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c16",
                "subjects": [
                    "Chemistry",
                    "Igbo Language"
                ],
                "classes": [
                    "Senior Secondary School Three",
                    "Senior Secondary School Three"
                ],
                "fullname": "Emeka Ngozi Solarin",
                "email": "emekasolarin@hotmail.com",
                "username": "emekasolarin88",
                "phoneNumber": "+2347073418137",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            },
            {
                "children": [],
                "role": "Parent_Vice-Principal",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c17",
                "subjects": [
                    "Mathematics",
                    "Mathematics"
                ],
                "classes": [
                    "Junior Secondary School One",
                    "Junior Secondary School Two"
                ],
                "fullname": "Chioma Chiamaka Mohammed",
                "email": "chiomamohammed@aol.com",
                "username": "chiomamohammed33",
                "phoneNumber": "+2348173518171",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            },
            {
                "children": [],
                "role": "Parent_Teacher",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c18",
                "subjects": [
                    "Geography",
                    "Biology"
                ],
                "classes": [
                    "Senior Secondary School Three",
                    "Senior Secondary School Two"
                ],
                "fullname": "Amara Matthew Idika",
                "email": "amaraidika@aol.com",
                "username": "amaraidika87",
                "phoneNumber": "+2347073618205",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            },
            {
                "children": [],
                "role": "Parent_Bursar",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c19",
                "subjects": [
                    "Mathematics",
                    "Basic science"
                ],
                "classes": [
                    "Senior Secondary School One",
                    "Senior Secondary School One"
                ],
                "fullname": "Gbemisola Folake Nweke",
                "email": "gbemisolanweke@aol.com",
                "username": "gbemisolanweke50",
                "phoneNumber": "+2348173718239",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            },
            {
                "children": [],
                "role": "Parent_Form-Teacher",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c1b",
                "subjects": [
                    "Biology",
                    "Physics"
                ],
                "classes": [
                    "Junior Secondary School Three",
                    "Senior Secondary School Three"
                ],
                "fullname": "Titilayo Abubakar Bbatunde",
                "email": "titilayobbatunde@outlook.com",
                "username": "titilayobbatunde65",
                "phoneNumber": "+2349073918307",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            }
        ]
    }
    ``` 

### Retrieve All The Parents In a School With Filtering (Filter The Male Stapents That Teach Mathematics)

Notice from the response, that only male Stapents who teach Mathematics are returned.

No user from the Parent category is returned in the output.

* Request:
    * Endpoint: GET/api/v1/schools/5ecb08dfd2595416f0dc9978/parents?category=Stapent&gender=male&subjects=Mathematics

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Successfully retrieved all parents",
        "results": 3,
        "data": [
            {
                "children": [],
                "role": "Parent_Form-Teacher",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c1a",
                "subjects": [
                    "Mathematics",
                    "Accounting"
                ],
                "classes": [
                    "Junior Secondary School Two",
                    "Senior Secondary School Three"
                ],
                "fullname": "Juliet Imaobong Akintunde",
                "email": "julietakintunde@outlook.com",
                "username": "julietakintunde1",
                "phoneNumber": "+2349073818273",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            },
            {
                "children": [],
                "role": "Parent_Vice-Principal",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c17",
                "subjects": [
                    "Mathematics",
                    "Mathematics"
                ],
                "classes": [
                    "Junior Secondary School One",
                    "Junior Secondary School Two"
                ],
                "fullname": "Chioma Chiamaka Mohammed",
                "email": "chiomamohammed@aol.com",
                "username": "chiomamohammed33",
                "phoneNumber": "+2348173518171",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            },
            {
                "children": [],
                "role": "Parent_Bursar",
                "category": "Stapent",
                "isVerified": true,
                "_id": "5f0382c3ff5ad20e60294c19",
                "subjects": [
                    "Mathematics",
                    "Basic science"
                ],
                "classes": [
                    "Senior Secondary School One",
                    "Senior Secondary School One"
                ],
                "fullname": "Gbemisola Folake Nweke",
                "email": "gbemisolanweke@aol.com",
                "username": "gbemisolanweke50",
                "phoneNumber": "+2348173718239",
                "gender": "male",
                "school": "5ecb08dfd2595416f0dc9978",
                "__v": 0,
                "classesAndSubjects": [],
                "formTeacherOfTheseClasses": []
            }
        ]
    }
    ``` 

The filtering example above is a very basic one. There are more advanced filtering use cases, for example:

* Returning schools whose population is greater than or less than or equal to a given value.

Whenever an advanced filter like this needs to be performed, the user can make a request to the api creators for more information.

## Sorting
The essence of sorting, is to sort the returned documents according to a certain order.

For instance, in our example, we are going to retrieve a list of all the schools that are registered on our platform based on their population, in descending order (from highest to lowest).

We are going to follow two stages:

1. Retrieve all the schools without sorting
2. Retrieve the schools in sorted form.

### Retrieve The Schools Without Sorting
* Request
    * Endpoint: GET/api/v1/schools

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Schools retrieved successfully",
        "results": 11,
        "data": [
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9976",
                "admin": "amakesolarin63",
                "name": "Community High School Ojo",
                "address": "10 Olanrewaju Street, Satelite Town, Lagos",
                "population": 2509,
                "email": "community-high@yahoo.com",
                "phoneNumber": "+2348064745859",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "002",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9977",
                "admin": "funshoikokwu90",
                "name": "Hopebay College",
                "address": "30 Ezekiel Street, Satelite Town, Rivers",
                "population": 2756,
                "email": "hopebay@yahoo.com",
                "phoneNumber": "+2349032745059",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "001",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9979",
                "admin": "emekasolarin88",
                "name": "Meadow Academy",
                "address": "7 Falomo Road, Ijaiye, Ogun",
                "population": 7644,
                "email": "info@meadowacademy.org",
                "phoneNumber": "+2348175309861",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "003",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9975",
                "admin": "bukolaayantola18",
                "name": "Marist Comprehensive",
                "address": "1057 Agege Road, Agege, Lagos",
                "population": 4599,
                "email": "marist@gmail.com",
                "phoneNumber": "+2348065753440",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "004",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9978",
                "admin": "ngozicole43",
                "name": "Atlantic Hall",
                "address": "7 Balogun Street, Lekki, Lagos",
                "population": 7469,
                "email": "atlantic-hall@yahoo.com",
                "phoneNumber": "+2347037345059",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "005",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997a",
                "admin": "imaobongnwankwo13",
                "name": "Higher Achievers",
                "address": "7 Cole Street Off Ajegunle Bus-Stop , Ikeja, Lagos",
                "population": 3584,
                "email": "higher_achievers@gmail.org",
                "phoneNumber": "+2348175304561",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "006",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997b",
                "admin": "echezonaimitiari71",
                "name": "Crescent College",
                "address": "6 Morenikeji Street, Maraba, Kwara",
                "population": 6545,
                "email": "hello@crescent.net",
                "phoneNumber": "+2348175665861",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "007",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997d",
                "admin": "emekabbatunde80",
                "name": "Kings College",
                "address": "55 Obi Street New Housing Estate, Onitsha, Anambra",
                "population": 5098,
                "email": "helpdesk@kgc.com",
                "phoneNumber": "+2349072652148",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "008",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997c",
                "admin": "chiamakanwafor80",
                "name": "Notre Girls College",
                "address": "55 Lamido Street Ahmed Musa GRA, Gwagwalada, Abuja",
                "population": 8476,
                "email": "ngc@gmail.com",
                "phoneNumber": "+2347084765431",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "009",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5f00c23eb625d1189033cea6",
                "name": "Orient Academy",
                "email": "orientacademy@gmail.com",
                "admin": "ngwodo@gmail.com",
                "population": 5499,
                "registeredOn": "2020-07-04T17:53:49.000Z",
                "address": "No 440, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064058820",
                "schoolCode": "0010",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5f037b70df5a4e057cc0309d",
                "name": "Peniel Academy",
                "email": "penielacademy@gmail.com",
                "admin": "peterpan@gmail.com",
                "population": 5349,
                "registeredOn": "2020-07-06T19:28:35.000Z",
                "address": "No 31, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064158820",
                "schoolCode": "0011",
                "__v": 0
            }
        ]
    }
    ``` 

### Retrieve All The Registered Schools Sorted In Descending Order Based On Population

* Request
    * Endpoint: GET/api/v1/schools?sort=-population

Observer the minus sign (-) before the population.

If you were sorting in ascending order (lowest to highest), you would omit the minus sign. 

* Response
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Schools retrieved successfully",
        "results": 11,
        "data": [
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997c",
                "admin": "chiamakanwafor80",
                "name": "Notre Girls College",
                "address": "55 Lamido Street Ahmed Musa GRA, Gwagwalada, Abuja",
                "population": 8476,
                "email": "ngc@gmail.com",
                "phoneNumber": "+2347084765431",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "009",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9979",
                "admin": "emekasolarin88",
                "name": "Meadow Academy",
                "address": "7 Falomo Road, Ijaiye, Ogun",
                "population": 7644,
                "email": "info@meadowacademy.org",
                "phoneNumber": "+2348175309861",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "003",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9978",
                "admin": "ngozicole43",
                "name": "Atlantic Hall",
                "address": "7 Balogun Street, Lekki, Lagos",
                "population": 7469,
                "email": "atlantic-hall@yahoo.com",
                "phoneNumber": "+2347037345059",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "005",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997b",
                "admin": "echezonaimitiari71",
                "name": "Crescent College",
                "address": "6 Morenikeji Street, Maraba, Kwara",
                "population": 6545,
                "email": "hello@crescent.net",
                "phoneNumber": "+2348175665861",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "007",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5f00c23eb625d1189033cea6",
                "name": "Orient Academy",
                "email": "orientacademy@gmail.com",
                "admin": "ngwodo@gmail.com",
                "population": 5499,
                "registeredOn": "2020-07-04T17:53:49.000Z",
                "address": "No 440, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064058820",
                "schoolCode": "0010",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5f037b70df5a4e057cc0309d",
                "name": "Peniel Academy",
                "email": "penielacademy@gmail.com",
                "admin": "peterpan@gmail.com",
                "population": 5349,
                "registeredOn": "2020-07-06T19:28:35.000Z",
                "address": "No 31, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064158820",
                "schoolCode": "0011",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997d",
                "admin": "emekabbatunde80",
                "name": "Kings College",
                "address": "55 Obi Street New Housing Estate, Onitsha, Anambra",
                "population": 5098,
                "email": "helpdesk@kgc.com",
                "phoneNumber": "+2349072652148",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "008",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9975",
                "admin": "bukolaayantola18",
                "name": "Marist Comprehensive",
                "address": "1057 Agege Road, Agege, Lagos",
                "population": 4599,
                "email": "marist@gmail.com",
                "phoneNumber": "+2348065753440",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "004",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997a",
                "admin": "imaobongnwankwo13",
                "name": "Higher Achievers",
                "address": "7 Cole Street Off Ajegunle Bus-Stop , Ikeja, Lagos",
                "population": 3584,
                "email": "higher_achievers@gmail.org",
                "phoneNumber": "+2348175304561",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "006",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9977",
                "admin": "funshoikokwu90",
                "name": "Hopebay College",
                "address": "30 Ezekiel Street, Satelite Town, Rivers",
                "population": 2756,
                "email": "hopebay@yahoo.com",
                "phoneNumber": "+2349032745059",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "001",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9976",
                "admin": "amakesolarin63",
                "name": "Community High School Ojo",
                "address": "10 Olanrewaju Street, Satelite Town, Lagos",
                "population": 2509,
                "email": "community-high@yahoo.com",
                "phoneNumber": "+2348064745859",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "002",
                "__v": 0
            }
        ]
    }
    ``` 

## Pagination
Our api resources or documents can be very large. 

When a dataset is queried, the returned documents can be astronomically much, if pagination is not utilized.

Basically, with pagination, anyone interacting with the api, can specify how much documents they want to recieve per page and they can navigate from page to page.

The example below, will show you how to limit the number of documents that show up per page and how to move from page to page.

For this purpose, we will be using a single example.

The example below, will fetch the contents of page one, with ten documents for each page.

This will work for other pages like page two, page three and so on. Furthermore you can also extend the returned documents limit from ten to eleven, hundred, five hundred and so on.

The documents we want to retrieve are the registered schools on the platform.

This will work on other datasets apart from the school's resources. For example, it could also work on books, questions, lectures, timetables and so on...

* Request:
    * Endpoint: GET/api/v1/schools?page=1&limit=10

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Schools retrieved successfully",
        "results": 10,
        "data": [
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9976",
                "admin": "amakesolarin63",
                "name": "Community High School Ojo",
                "address": "10 Olanrewaju Street, Satelite Town, Lagos",
                "population": 2509,
                "email": "community-high@yahoo.com",
                "phoneNumber": "+2348064745859",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "002",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9977",
                "admin": "funshoikokwu90",
                "name": "Hopebay College",
                "address": "30 Ezekiel Street, Satelite Town, Rivers",
                "population": 2756,
                "email": "hopebay@yahoo.com",
                "phoneNumber": "+2349032745059",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "001",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9979",
                "admin": "emekasolarin88",
                "name": "Meadow Academy",
                "address": "7 Falomo Road, Ijaiye, Ogun",
                "population": 7644,
                "email": "info@meadowacademy.org",
                "phoneNumber": "+2348175309861",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "003",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9975",
                "admin": "bukolaayantola18",
                "name": "Marist Comprehensive",
                "address": "1057 Agege Road, Agege, Lagos",
                "population": 4599,
                "email": "marist@gmail.com",
                "phoneNumber": "+2348065753440",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "004",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9978",
                "admin": "ngozicole43",
                "name": "Atlantic Hall",
                "address": "7 Balogun Street, Lekki, Lagos",
                "population": 7469,
                "email": "atlantic-hall@yahoo.com",
                "phoneNumber": "+2347037345059",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "005",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997a",
                "admin": "imaobongnwankwo13",
                "name": "Higher Achievers",
                "address": "7 Cole Street Off Ajegunle Bus-Stop , Ikeja, Lagos",
                "population": 3584,
                "email": "higher_achievers@gmail.org",
                "phoneNumber": "+2348175304561",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "006",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997b",
                "admin": "echezonaimitiari71",
                "name": "Crescent College",
                "address": "6 Morenikeji Street, Maraba, Kwara",
                "population": 6545,
                "email": "hello@crescent.net",
                "phoneNumber": "+2348175665861",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "007",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997d",
                "admin": "emekabbatunde80",
                "name": "Kings College",
                "address": "55 Obi Street New Housing Estate, Onitsha, Anambra",
                "population": 5098,
                "email": "helpdesk@kgc.com",
                "phoneNumber": "+2349072652148",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "008",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997c",
                "admin": "chiamakanwafor80",
                "name": "Notre Girls College",
                "address": "55 Lamido Street Ahmed Musa GRA, Gwagwalada, Abuja",
                "population": 8476,
                "email": "ngc@gmail.com",
                "phoneNumber": "+2347084765431",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "009",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5f00c23eb625d1189033cea6",
                "name": "Orient Academy",
                "email": "orientacademy@gmail.com",
                "admin": "ngwodo@gmail.com",
                "population": 5499,
                "registeredOn": "2020-07-04T17:53:49.000Z",
                "address": "No 440, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064058820",
                "schoolCode": "0010",
                "__v": 0
            }
        ]
    }
    ```

## Field Limiting

When retrieving documents, there are some document fields that we might not want to show up in the response because of their un-necessity.

Meanwhile, there are times, when we might want only some specific fields to show up in the response.

We are going to have three examples below to showcase the power of field limiting.

1. Retrieve documents without any field limiting.

2. Retrieve documents and return all the fields in the response except some specific ones.

3. Retrieve documents and return only the specified fields, leaving out the rest.

For this purpose, we are going to work with the school dataset.

### Retrieve Registered Schools On The Platform Without Any Field Limiting.
* Request:
    * Endpoint: GET/api/v1/schools

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Schools retrieved successfully",
        "results": 11,
        "data": [
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9976",
                "admin": "amakesolarin63",
                "name": "Community High School Ojo",
                "address": "10 Olanrewaju Street, Satelite Town, Lagos",
                "population": 2509,
                "email": "community-high@yahoo.com",
                "phoneNumber": "+2348064745859",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "002",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9977",
                "admin": "funshoikokwu90",
                "name": "Hopebay College",
                "address": "30 Ezekiel Street, Satelite Town, Rivers",
                "population": 2756,
                "email": "hopebay@yahoo.com",
                "phoneNumber": "+2349032745059",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "001",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9979",
                "admin": "emekasolarin88",
                "name": "Meadow Academy",
                "address": "7 Falomo Road, Ijaiye, Ogun",
                "population": 7644,
                "email": "info@meadowacademy.org",
                "phoneNumber": "+2348175309861",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "003",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9975",
                "admin": "bukolaayantola18",
                "name": "Marist Comprehensive",
                "address": "1057 Agege Road, Agege, Lagos",
                "population": 4599,
                "email": "marist@gmail.com",
                "phoneNumber": "+2348065753440",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "004",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc9978",
                "admin": "ngozicole43",
                "name": "Atlantic Hall",
                "address": "7 Balogun Street, Lekki, Lagos",
                "population": 7469,
                "email": "atlantic-hall@yahoo.com",
                "phoneNumber": "+2347037345059",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "005",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997a",
                "admin": "imaobongnwankwo13",
                "name": "Higher Achievers",
                "address": "7 Cole Street Off Ajegunle Bus-Stop , Ikeja, Lagos",
                "population": 3584,
                "email": "higher_achievers@gmail.org",
                "phoneNumber": "+2348175304561",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "006",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997b",
                "admin": "echezonaimitiari71",
                "name": "Crescent College",
                "address": "6 Morenikeji Street, Maraba, Kwara",
                "population": 6545,
                "email": "hello@crescent.net",
                "phoneNumber": "+2348175665861",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "imageUrl": "https://example.com/ex.jpg",
                "schoolCode": "007",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997d",
                "admin": "emekabbatunde80",
                "name": "Kings College",
                "address": "55 Obi Street New Housing Estate, Onitsha, Anambra",
                "population": 5098,
                "email": "helpdesk@kgc.com",
                "phoneNumber": "+2349072652148",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "008",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5ecb08dfd2595416f0dc997c",
                "admin": "chiamakanwafor80",
                "name": "Notre Girls College",
                "address": "55 Lamido Street Ahmed Musa GRA, Gwagwalada, Abuja",
                "population": 8476,
                "email": "ngc@gmail.com",
                "phoneNumber": "+2347084765431",
                "imageUrl": "https://example.com/ex.jpg",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "schoolCode": "009",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5f00c23eb625d1189033cea6",
                "name": "Orient Academy",
                "email": "orientacademy@gmail.com",
                "admin": "ngwodo@gmail.com",
                "population": 5499,
                "registeredOn": "2020-07-04T17:53:49.000Z",
                "address": "No 440, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064058820",
                "schoolCode": "0010",
                "imagesFolder": "1qicwYI6mYOfvE9fQ4fIl01GhMzirRFr7",
                "booksFolder": "19EgC6Tv6BPDwP7_pO2aTfjBYr0Rrzx95",
                "lecturesFolder": "1YLYeyEtkQkDOFwVhrD4tx4YoRhkXwyIa",
                "__v": 0
            },
            {
                "isSubscribed": false,
                "_id": "5f037b70df5a4e057cc0309d",
                "name": "Peniel Academy",
                "email": "penielacademy@gmail.com",
                "admin": "peterpan@gmail.com",
                "population": 5349,
                "registeredOn": "2020-07-06T19:28:35.000Z",
                "address": "No 31, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064158820",
                "schoolCode": "0011",
                "imagesFolder": "1DmFWBUyjmh8VCMGWeTY204dYcQTwih6E",
                "booksFolder": "1G1jaa0_KvmsQ6P6ZpvNpfoVGrHLbFv0D",
                "lecturesFolder": "1dkynoGH6mBH6y0_s4nK2GsQHvKMMaZOq",
                "__v": 0
            }
        ]
    }
    ``` 

### Retrieve Registered Schools On The Platform and Return All The Fields In The Response Except Some Specific Ones.

* Request:
    * Endpoint: GET/api/v1/schools?fields=-isSubscribed,-registeredOn,-schoolCode,-imagesFolder,-booksFolder,-lecturesFolder

Notice that there is a minus sign before each field name.

* Response:
    * Status: 200 - Ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Schools retrieved successfully",
        "results": 11,
        "data": [
            {
                "_id": "5ecb08dfd2595416f0dc9976",
                "admin": "amakesolarin63",
                "name": "Community High School Ojo",
                "address": "10 Olanrewaju Street, Satelite Town, Lagos",
                "population": 2509,
                "email": "community-high@yahoo.com",
                "phoneNumber": "+2348064745859",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc9977",
                "admin": "funshoikokwu90",
                "name": "Hopebay College",
                "address": "30 Ezekiel Street, Satelite Town, Rivers",
                "population": 2756,
                "email": "hopebay@yahoo.com",
                "phoneNumber": "+2349032745059",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc9979",
                "admin": "emekasolarin88",
                "name": "Meadow Academy",
                "address": "7 Falomo Road, Ijaiye, Ogun",
                "population": 7644,
                "email": "info@meadowacademy.org",
                "phoneNumber": "+2348175309861",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc9975",
                "admin": "bukolaayantola18",
                "name": "Marist Comprehensive",
                "address": "1057 Agege Road, Agege, Lagos",
                "population": 4599,
                "email": "marist@gmail.com",
                "phoneNumber": "+2348065753440",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc9978",
                "admin": "ngozicole43",
                "name": "Atlantic Hall",
                "address": "7 Balogun Street, Lekki, Lagos",
                "population": 7469,
                "email": "atlantic-hall@yahoo.com",
                "phoneNumber": "+2347037345059",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc997a",
                "admin": "imaobongnwankwo13",
                "name": "Higher Achievers",
                "address": "7 Cole Street Off Ajegunle Bus-Stop , Ikeja, Lagos",
                "population": 3584,
                "email": "higher_achievers@gmail.org",
                "phoneNumber": "+2348175304561",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc997b",
                "admin": "echezonaimitiari71",
                "name": "Crescent College",
                "address": "6 Morenikeji Street, Maraba, Kwara",
                "population": 6545,
                "email": "hello@crescent.net",
                "phoneNumber": "+2348175665861",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc997d",
                "admin": "emekabbatunde80",
                "name": "Kings College",
                "address": "55 Obi Street New Housing Estate, Onitsha, Anambra",
                "population": 5098,
                "email": "helpdesk@kgc.com",
                "phoneNumber": "+2349072652148",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5ecb08dfd2595416f0dc997c",
                "admin": "chiamakanwafor80",
                "name": "Notre Girls College",
                "address": "55 Lamido Street Ahmed Musa GRA, Gwagwalada, Abuja",
                "population": 8476,
                "email": "ngc@gmail.com",
                "phoneNumber": "+2347084765431",
                "imageUrl": "https://example.com/ex.jpg",
                "__v": 0
            },
            {
                "_id": "5f00c23eb625d1189033cea6",
                "name": "Orient Academy",
                "email": "orientacademy@gmail.com",
                "admin": "ngwodo@gmail.com",
                "population": 5499,
                "address": "No 440, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064058820",
                "__v": 0
            },
            {
                "_id": "5f037b70df5a4e057cc0309d",
                "name": "Peniel Academy",
                "email": "penielacademy@gmail.com",
                "admin": "peterpan@gmail.com",
                "population": 5349,
                "address": "No 31, Old Lagos Asaba Road, Boji Boji Agbor, Delta State",
                "phoneNumber": "+2349064158820",
                "__v": 0
            }
        ]
    }
    ``` 

### Retrieve Registered Schools On The Platform and Return Only The Specified Fields, Leaving Out The Rest.

* Request:
    * Endpoint: GET/api/v1/schools?fields=name,address,email,imageUrl

Notice that there is no minus sign before each field name.

* Response:
    * Status: 200 - ok
    * Body(application/json)
    ```
    {
        "status": "success",
        "message": "Schools retrieved successfully",
        "results": 11,
        "data": [
            {
                "_id": "5ecb08dfd2595416f0dc9976",
                "name": "Community High School Ojo",
                "address": "10 Olanrewaju Street, Satelite Town, Lagos",
                "email": "community-high@yahoo.com",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc9977",
                "name": "Hopebay College",
                "address": "30 Ezekiel Street, Satelite Town, Rivers",
                "email": "hopebay@yahoo.com",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc9979",
                "name": "Meadow Academy",
                "address": "7 Falomo Road, Ijaiye, Ogun",
                "email": "info@meadowacademy.org",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc9975",
                "name": "Marist Comprehensive",
                "address": "1057 Agege Road, Agege, Lagos",
                "email": "marist@gmail.com",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc9978",
                "name": "Atlantic Hall",
                "address": "7 Balogun Street, Lekki, Lagos",
                "email": "atlantic-hall@yahoo.com",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc997a",
                "name": "Higher Achievers",
                "address": "7 Cole Street Off Ajegunle Bus-Stop , Ikeja, Lagos",
                "email": "higher_achievers@gmail.org",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc997b",
                "name": "Crescent College",
                "address": "6 Morenikeji Street, Maraba, Kwara",
                "email": "hello@crescent.net",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc997d",
                "name": "Kings College",
                "address": "55 Obi Street New Housing Estate, Onitsha, Anambra",
                "email": "helpdesk@kgc.com",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5ecb08dfd2595416f0dc997c",
                "name": "Notre Girls College",
                "address": "55 Lamido Street Ahmed Musa GRA, Gwagwalada, Abuja",
                "email": "ngc@gmail.com",
                "imageUrl": "https://example.com/ex.jpg"
            },
            {
                "_id": "5f00c23eb625d1189033cea6",
                "name": "Orient Academy",
                "email": "orientacademy@gmail.com",
                "address": "No 440, Old Lagos Asaba Road, Boji Boji Agbor, Delta State"
            },
            {
                "_id": "5f037b70df5a4e057cc0309d",
                "name": "Peniel Academy",
                "email": "penielacademy@gmail.com",
                "address": "No 31, Old Lagos Asaba Road, Boji Boji Agbor, Delta State"
            }
        ]
    }
    ``` 

[Back to main documentation](README.md)