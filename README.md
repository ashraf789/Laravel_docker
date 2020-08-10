# Run laravel project by docker 
### Environment setup
- install and run docker to your local computer https://www.docker.com/get-started
- copy all files from laravel-docker folder to inside your laravle project.
- rename .env.docker to .env 

### Docker instructions
1. For the first time, build the project [from second time build is not required] <br> 
` docker-compose build ` <br>

2. Run the project <br> 
` docker-compose up ` <br>

    **Now our project is running you can access app from web browser by http://localhost/ <br>
    If you run the project for the first time you also have to follow the below instructions <br>**


3. install required composer packages<br>
` docker exec -it app composer install `<br>

4. install node packages<br>
` docker exec -it app npm install `<br>

5. migrate databases<br>
` docker exec -it app php artisan migrate `<br>

6. seed generate (optional)<br>
` docker exec -it app php artisan db:seed `<br>

### Additional information
- To open a container shell<br> 
`docker exec -it container_name sh` <br>
    Example: if you want to access mysql(container) shell <br>
`docker exec -it mysql sh `<br>

- database access <br>
first access the mysql shell then run the below command <br>
`mysql -uroot -pboos`

