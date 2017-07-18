# Tic-tac-toe Game Notes

## Requirements
- docker 17+
- docker-compose 1.14

### Optional requirements
- NPM - to build front-end

## Running
Build containers
```
docker-compose build
```

Run the containers
```
docker-compose up
```

Install API dependencies
```
docker exec -it ttt-api-php composer install
```

## Running tests
```
docker exec -it ttt-api-php bin/phpunit
```

## Components
Access project in the browser
- http://localhost:8888/ - front-end UI
- http://localhost:8888/api/ - API

For additional details see README.md in the `ttt-api` and `ttt-front` folders 

## Implementation details
- API supports NxN grids
- Used docker-compose to create integrated environment, projects
  are however completely separate entities
- Used latest version of the PHP (7.1.7)
- Used ES15 for the front-end with the babel and browserify
- PHPUnit for the functional as well as unit tests

## Future improvements
- Better UI, possibly also highlight winning line
- More robust API (validation, configurable)
- Support 2 players or switching of the bots 
- Front-end tests are missing
- Front-end could use some reactive framework to simplify logic drastically
- Integrate with the CI/CD tools to report on test coverage and deploy automatically
