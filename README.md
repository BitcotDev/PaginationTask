# level2Task
Create a List view and implement pagination. 

1. Create a single screen application which will display a list of passengers who took airline trips.
2. Below API which will provide a list of passengers who took different airline trips.

**API**

https://api.instantwebtools.net/v1/passenger?page=0&size=10

**Response**

{
 "totalPassengers": 30284,
    "totalPages": 3029,
    "data": [
        {
            "_id": "5ff6f54d41f00e4af3833574",
            "name": "Leonardo",
            "trips": 250,
            "airline": [
                {
                    "id": 5,
                    "name": "Eva Air",
                    "country": "Taiwan",
                    "logo": "https://upload.wikimedia.org/wikipedia/en/thumb/e/ed/EVA_Air_logo.svg/250px-EVA_Air_logo.svg.png",
                    "slogan": "Sharing the World, Flying Together",
                    "head_quaters": "376, Hsin-Nan Rd., Sec. 1, Luzhu, Taoyuan City, Taiwan",
                    "website": "www.evaair.com",
                    "established": "1989"
                }
            ],
            "__v": 0
        },
        {
            "_id": "5ff6f54d41f00e32cd833575",
            "name": "Pedro",
            "trips": null,
            "airline": [
                {
                    "id": 4,
                    "name": "Emirates",
                    "country": "Dubai",
                    "logo": "https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Emirates_logo.svg/150px-Emirates_logo.svg.png",
                    "slogan": "From Dubai to destinations around the world.",
                    "head_quaters": "Garhoud, Dubai, United Arab Emirates",
                    "website": "www.emirates.com/",
                    "established": "1985"
                }
            ],
            "__v": 0
        }
      ]
}

# Design:

![5 – 5](https://user-images.githubusercontent.com/36688362/156924855-c0ec49ea-1523-4bb7-bc07-219df7f8b9c3.png)

1. Goal of the App is to integrate the above API and implement pagination when the user is scrolling down to see more passengers. 
2. You can decide how many passengers you can show in a list for a single page, but make sure it doesn't take too long to load the API. 
3. While scrolling down the app, User should not get blocked from interacting screen when you are doing pagination
4. Add loader in table view footer view when ur paginating to get next page details
5. Please follow design as close as possible


# API Integration:

1. Title label use **data -> name** from json
2. Sub title label (explanatory text) **data -> airline - > name**
3. Third label (extra information) use **data -> trips**
4. Icon use **data -> airline -> logo url**

