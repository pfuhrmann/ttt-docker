# Tic-tac-toe Implementation Notes

## Implementation details
- API supports NxN grids
- Implemented 2 types of bots, clueless and unbeatable
- Used docker-compose to create integrated environment, projects
  are however completely separate entities
- Used latest version of the PHP (7.1.7)
- Used ES15 for the front-end with the babel and browserify
- PHPUnit for the functional as well as unit tests
- Standards used PSR-1, PSR-2, PSR-4, PSR-7

## Requirements
- docker 17+
- docker-compose 1.14

### Optional requirements
- `npm` - to build front-end

## Building and Running
### PHP
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

### *(optional) Front-end
* this step is optional because `bundle.js` is already provided
  and integrated with the nginx
  
Install front-end dependencies
```
cd ttt-front
npm install
```

Run development server
```
npm run start
```

Build Dependencies
```
npm run build
```

## Running tests
```
docker exec -it ttt-api-php bin/phpunit
```

## Components
Access project in the browser
- [http://localhost:8888/](http://localhost:8888/) - front-end UI
- [http://localhost:8888/api/](http://localhost:8888/api/) - API

For additional details see README.md in the `ttt-api` and `ttt-front` folders 

## Future improvements
- Better UI (highlight winning line, possibility to choose AI level,
  support for the NxN grids)
- More robust API (validation, configurable, speed up minimax, medium
  intensity AI level)
- Support 2 players or switching of the bots 
- Front-end tests are missing
- Front-end could use some reactive framework to simplify logic drastically
- Integrate with the CI/CD tools to report on test coverage and deploy automatically
