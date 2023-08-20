1. Build and Run Services : 
    docker compose up --build 

2. Enter to Each DB Services : 
    mysql -u <USER> -p <Password>

3. To Add the Master DB info , Do this on Both Services :
    CHANGE MASTER TO
    MASTER_HOST='<MASTER_HOST>',
    MASTER_USER='<MASTER_REPLICATION_USER>',
    MASTER_PASSWORD='<MASTER_REPLICATION_PASSWORD>';
    <!-- CHANGE MASTER TO
    MASTER_HOST='master',
    MASTER_USER='root',
    MASTER_PASSWORD='root'; -->

    Then Start Slave Server By: 
        START SLAVE;
        RESET SLAVE;
        STOP SLAVE;

4. To Check the status of Master/Slave Run the command:
    SHOW MASTER/SLAVE STATUS\G;

5. To Create New DB :
    CREATE DATABASE <DB_NAME>;
    SHOW DATABASES;

