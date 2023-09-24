Hi, this is a submission for DemoUp Cliplister test for Backend Developer position.

The project consists of 3 projects (microservices)
- Asset microservice: responsible on Asset management
- Categories microservice: responsible on categories management (WIP)
- Collection microservice: responsibe on collections management (WIP)


The test focuses mainly on the first microservice (Asset Microservice)

# Asset Microservice

## Architecture
The microservice consists on an express js app and postgres database running via docker

## Run the project
To run the project, please make sure the following dependencies are isntalled `docker`, `docker-compose` and `node`.

1. Create a new .env file
`
DB_HOST=localhost
DB_PORT=5432
DB_USER=user
DB_PASS=pass
DB_NAME=assetdb

NODE_ENV=development

# MICROSERVICES
CATEGORIES_URL=http://127.0.0.1:3002
`

2. run npm install
3. run `docker-compose up` to run the database
4. Once the database is running, you can can run `npm run init-schema` this will run migrations and seed databse with dummy data.
5. run `npm run start`
6. Feel free to use the app

## Documentation:

| Method | Route         | Description                     | params                                                                                                                                                |
| ------ | ------------- | ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| GET    | /assets       | Returns the list of assets      |                                                                                                                                                       |
| GET    | /assets/:uuid | Returns the details of an asset | :uuid: string                                                                                                                                         |
| POST   | /assets       | Create a new assets             | name: string, type: image or video or document, content: a base64 string of the asset, categories: Array of uuid that contains the list of categories |
| DELETE | /assets/:uuid | Delete an asset                 | uuid: string                                                                                                                                          |

# Notes:
The list of categories is available when activating the catgories microservice


# Categories Microservice
This microservice is WIP (Work In Progress)

## Architecture
The microservice consists on an express js app and postgres database running via docker

## Run the project
To run the project, please make sure the following dependencies are isntalled `docker`, `docker-compose` and `node`.

1. Create a new .env file
`
DB_HOST=localhost
DB_PORT=5432
DB_USER=user
DB_PASS=pass
DB_NAME=categoriesdb

NODE_ENV=development
`

2. run npm install
3. run `docker-compose up` to run the database
4. run `npm run start`
5. Feel free to use the app

## Documentation:

| Method | Route         | Description                     | params                                                                                                                                                |
| ------ | ------------- | ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| GET    | /categories   | Returns the list of categories  |                                                                                                                                                       |

# collections Microservice
This microservice is WIP (Work In Progress)

## Architecture
The microservice consists on an express js app and postgres database running via docker

## Run the project
To run the project, please make sure the following dependencies are isntalled `docker`, `docker-compose` and `node`.

1. Create a new .env file
`
DB_HOST=localhost
DB_PORT=5432
DB_USER=user
DB_PASS=pass
DB_NAME=collectionsdb

NODE_ENV=development
`

2. run npm install
3. run `docker-compose up` to run the database
4. run `npm run start`
4. Feel fre to use the app

## Documentation:

| Method | Route         | Description                     | params                                                                                                                                                |
| ------ | ------------- | ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| GET    | /collections  | Returns the list of collections |                                                                                                                                                       |
