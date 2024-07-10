/
    - src/
        index.js // server
        models/
        controllers/
        middlewares/
        services/
        utils/
        config/
        repository/
    - tests/ [later]
    - static/
    - temp/

    # welcome to flights service
    ## project setup
    - clone the project on your local
    - Execute `npm install` on the same path as your root directory of the downloaded project
    - create a `.env`  file in the root directory and add the following environment variables 
        - `PORT=3000`
    - inside the `src/config` folder create a new file `config.json` and then add the following piece of json

    ```
    {
    "development": {
        "username": "<Your_DB_Login_Name>",
        "password": "<your DB password>",
        "database": "Flight_Search_DB_DEV",
        "host": "127.0.0.1",
        "dialect": "mysql"
    }
    }


    ```
    - once you've added your db config as listed above, go to the source folder from your terminal and execute `npx sequelize db:create`
      and then execute

      `npx sequelize`
    ```

    ## DB Design
        - Airplane table
        - Flight
        - Airport 
        - City

        - A flight belongs to an airplane but on airplane can be used in multiple flights
        - A city has many airports but one airport belongs to a city
        - one airport can have any flights, but a flight belongs one airport

    ## Tables

    ## City --> id, name, created_at, updated_at
    ## Airport --> id, name, address, city_id, created_at, updated_at
       Relationship --> City has many airports and Airport belongs to a city (one to many)


    ```
    npx sequelize model:generate --name Airport --attributes name:String,address:String,cityId:integer

    ```    