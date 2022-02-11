## Docker

### Build Image

Run `docker-compose build` from the project's root.

### Run Checker Service in Docker container locally

Run `docker-compose up` from the project's root.

### Swagger

Available at: `http://<serverip>:3001/api/`.

### UI

Available at: http://<serverip>:3081

### Preparation
It would be fine if several shelters (bunkers) are created using Admin account.

You can use already populated SQLite database (myDb). 
Ready myDb file should be placed into /init folder
and ENV variable 'INIT' must be set to 'yes' or 'cond' before docker image build (docker-compose or docker).


### Notes
Default admin credentials are specified in api config file.

If you run `s4femap-api` service using docker-compose, the `host` parameter for checker will be `192.168.50.3:8079`, when checker is placed into the same subnet.
Otherwise use <serverip>:3001

IP can be changed in `s4femap-api`'s docker-compose `ipv4_address` section.
Port can be changed in `s4femap-api`'s Dockerfile `EXPOSE` section.

