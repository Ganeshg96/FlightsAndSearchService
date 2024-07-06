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
    
    ```
