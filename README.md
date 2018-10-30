## Background
This project provides some API endpoints to create a job. The actual endpoint to save the job is POST /jobs, 
while the other endpoints are providing some additional functionality that clients may need.

A job represents a task or some job a consumer needs to be done by a tradesman/craftsman.
It is something like "Paint my 60m2 flat" or "Fix the bathroom sink".
Every job is categorized in a "Service". You can think of them like categories. eg: "Boat building & boat repair" or "Cleaning of gutters".
Also every job needs some additional data like a description and when the job should be done.

## The Task
You should review and refactor this project, so it matches your criteria for good code and has a state that you're fine with. 
Feel free to change anything you want.
Please write a small documentation where you explain what you have changed and why you think your refactored code is better than the original code.

## Results
If you are finished, please create a .zip archive with your name as filename and upload it here:
https://www.dropbox.com/request/H5TZGaVAcaR0WZntIfiQ  
The archive should contain the complete project including the .git folder but you can leave out the /vendor/ directory to keep it small.


## Run the project
### Setup
- `docker-compose up -d`
- `docker run --rm --interactive --tty --volume $PWD/jobs:/app --volume $COMPOSER_HOME:/tmp composer install`
- `docker-compose exec php bin/console doctrine:migrations:migrate`

## Tests
- `docker-compose exec php bin/console doctrine:database:create --env=test`
- `docker-compose exec php vendor/bin/phpunit`
