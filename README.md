# Docker-NodeJS-MySQL
Docker created with the stack of nodejs and mysql

### Sample Nodejs connection to MySQL server using mysql2 library

```
import mysql from "mysql2";
import config from "./config";

// create the connection to database
const connection = mysql.createPool({
    host: config.MYSQL_HOST,
    user: config.MYSQL_USER,
    database: config.MYSQL_DATABASE,
    password : config.MYSQL_PASSWORD,
    port: config.MYSQL_PORT,
    waitForConnections: true,
    connectionLimit: 10,
    queueLimit: 0,
});

export default connection;
```

Rename .env.example to .env and change path directory `ENV_APP_DIR_HOST`

And you're all set you are ready to run your nodejs application!
