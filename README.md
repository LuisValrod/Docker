# Docker
 **Link to visit**<br>
 With this link, you can connect you can create and connect your docker container to a sql server<br>
 <a href="https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-linux-ver15&preserve-view=true&tabs=cli&pivots=cs1-bash#pullandrun2019">Link</a><br>

 **Link to install sql management studio**
 With this link, you can download sql management studio and install it<br>
 <a href="https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16">Link</a><br><br>
 - Remember:
  - create a directory in your docker container: `/$ mkdir /var/opt/mssql/backup`
  - go to this directory: `cd /var/opt/mssql/backup`
  - get the database you are looking for: wget  https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2019.bak (The link is a bak file, and it could be any database you want)
  - Restore databases in SMS: >Right click on Databases > Restore Database > Device > Three dots > add > Find the database stored in the directory previously created

# Docker Commands
- ` docker run -d -p 8080:80 docker/welcome-to-docker` to run a new container
- `docker run --name data-engineering-postgres -e POSTGRES_PASSWORD=secret -d postgres` 
- `docker stop name_or_id_container` to stop the container
- `docker start name_or_id_container` to start container
- `docker ps` to see list of active containers
- `doceker ps -a` to see list of all containers
- `docker rm name_or_id_container` to delete a container
- `docker exec -u postgres data-engineering-postgres createdb postgres-db`
- `docker exec -it data-engineering-postgres psql -U postgres -d postgres-db` 

