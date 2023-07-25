# Project-Hausinventar

Die Datenbank besteht aus 3 Collections:
- bigstuff
- notsobigstuff
- smallstuff
  
## RUN LOCALLY

Clone the project

```bash
  git clone https://github.com/Paulaner690/Projekt_Hausinventar.git
```

Go to the project directory

```bash
  cd backend
```

Install dependencies

```bash
  npm install
```

Start the backend server

```bash
  npm run dev
```

---

Open a new Terminal and navigate to frontend:
```bash
  cd frontend
```

Install dependencies

```bash
  npm install
```


## ENVIRONMENT VARIABLES

To run this project, you will need to add the following environment variables to your .env file

`CLOUDINARY_API_SECRET`

`CLOUDINARY_API_KEY`

`CLOUDINARY_CLOUDNAME`

`MONGO_URI`

## START SERVER

Runs the app in the development mode.

```bash
  npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

## ENDPOINTS

#### Get all items from a category

```bash
  GET /api/bigstuff
```
```bash
  GET /api/notsobigstuff
```
```bash
  GET /api/smallstuff
```
#### Get one item by ID

```bash
  GET /api/bigstuff/:id
```
```bash
  GET /api/notsobigstuff/:id
```
```bash
  GET /api/smallstuff/:id
```
#### Post an item to a category

```bash
  POST /api/bigstuff
```
```bash
  POST /api/notsobigstuff
```
```bash
  POST /api/smallstuff
```
#### Update an item by ID

```bash
  PUT /api/bigstuff/:id
```
```bash
  PUT /api/notsobigstuff/:id
```
```bash
  PUT /api/smallstuff/:id
```
#### Delete an item by ID

```bash
  DELETE /api/bigstuff/:id
```
```bash
  DELETE /api/notsobigstuff/:id
```
```bash
  DELETE /api/smallstuff/:id
```

## EXAMPLES

#### Get all items from BIG STUFF:
```bash
  GET /api/bigstuff
```

What you get:
- An array of all objects from the category big stuff
```bash
  [
  {
    "_id": "64be2d9923a1e6a62ec281c0",
    "title": "Bett",
    "room": "Schlafzimmer",
    "image": {
      "url": "https://res.cloudinary.com/dryqtwdls/image/upload/v1690185113/Hausinventar/qmipw4hmqahqqu7mdayr.webp",
      "imageId": "Hausinventar/qmipw4hmqahqqu7mdayr",
      "_id": "64be2d9923a1e6a62ec281c1"
    },
    "content": "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis aspernatur provident at labore repudiandae reiciendis praesentium, amet repellendus ipsum, expedita ratione corrupti sapiente vel quasi! ",
    "__v": 0
  },
  {
    "_id": "64be2dc623a1e6a62ec281c3",
    "title": "Sessel",
    "room": "Flur",
    "image": {
      "url": "https://res.cloudinary.com/dryqtwdls/image/upload/v1690185158/Hausinventar/t7ae56ejquawbdvhwujr.webp",
      "imageId": "Hausinventar/t7ae56ejquawbdvhwujr",
      "_id": "64be2dc623a1e6a62ec281c4"
    },
    "content": "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis aspernatur provident at labore repudiandae reiciendis praesentium, amet repellendus ipsum, expedita ratione corrupti sapiente vel quasi!",
    "__v": 0
  },
...
```

#### Get one BIG STUFF item by ID 
```bash
  GET /api/bigstuff/${id}
  GET /api/bigstuff/64be2d9923a1e6a62ec281c0
```

What you get:
- A single object based on the id param /:id (64be2d9923a1e6a62ec281c0)
```bash
{
  "_id": "64be2d9923a1e6a62ec281c0",
  "title": "Bett",
  "room": "Schlafzimmer",
  "image": {
    "url": "https://res.cloudinary.com/dryqtwdls/image/upload/v1690185113/Hausinventar/qmipw4hmqahqqu7mdayr.webp",
    "imageId": "Hausinventar/qmipw4hmqahqqu7mdayr",
    "_id": "64be2d9923a1e6a62ec281c1"
  },
  "content": "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis aspernatur provident at labore repudiandae reiciendis praesentium, amet repellendus ipsum, expedita ratione corrupti sapiente vel quasi! ",
  "__v": 0
}
```

#### Post a BIG STUFF item 

Create a new object in the collection big stuff
```bash
  POST /api/bigstuff
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `title`   | `string` | **Required**. title of the item       |
| `room`    | `string` | **Required**. room of the item        |
| `content` | `string` | **Required**. description of the item |
| `url`     | `string` | **Required**. image URL of the item |
| `imageId` | `string` | **Required**. imageId of the item |

MongoDB creates an ID after posting


#### Update a BIG STUFF item 
```bash
  PUT /api/bigstuff/${id}
```
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `id`      | `string` | **Required**. ID of the item| 

Now you can update the content of each parameter in the body.

#### Delete a BIG STUFF item 
```bash
  DELETE /api/bigstuff/${id}
```
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `id`      | `string` | **Required**. ID of the item|  

What you get:

```bash
"item was deleted"
```
