# node-js-crud-with-mongo
An application demonstrating use of docker compose, dockerfile , Mongo Db and Node Js to perform basic CRUD operation.

## Description
This app simply provide two end-points to add and get list of users. We use MongoDb for performing storing and fetching the users details. 

<<**TODO:** Add update and delete operation as two more end-points. >>

User structure takes only first name and last name , you may add few too. 
```javascript
 firsName: {
        type: String,
        required: true
    },
   lastName: {
        type: String,
        required: true
    }
```

Two end-points i.e. create and fetch users will look like: 
### Add user
![Add users to MongoDb](https://github.com/jai2036/node-js-crud-with-mongo/blob/master/images/Add_users_to_users_collections.png)

### Fetch all users
![Get all users from MongoDB](https://github.com/jai2036/node-js-crud-with-mongo/blob/master/images/get_all_users_from_db.png)


## Dependecies
1. Docker 
2. Node Js and Mongo DB will be fetched using docker file. :)

## Executing
1. Create a project direcotry (optional) 
```bash
$ mkdir -p Projects 
$ cd Projects
```
2. Clone the repo
```bash
~/Projects/$ gh repo clone jai2036/node-js-crud-with-mongo 
```
3. Go to app directory (~/Projects/node-js-crud-with-mongo/) and build the dockerfile. 
```bash
~node-js-crud-with-mongo/$ docker build -t jai/myapp .
```
4. Run the image.
```bash
# list images and copy the id
~node-js-crud-with-mongo/$ docker images
# Run your image 
~node-js-crud-with-mongo/$ docker run -d -p 1337:1337 <image id>
```
5. Boom! Your end-points are ready to be accessed. 
```html
http://localhost:1337/api/users/add
http://localhost:1337/api/users
```
## Author
Jai K. 

### Version History

+  02 Create & Fetch operation added.
+  01 Initial release. 
