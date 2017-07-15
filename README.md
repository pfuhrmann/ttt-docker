# Tic-tac-toe

## Requirements

- docker 17+
- docker-compose 1.14

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

## Components

Access project in the browser

- http://localhost:8888/ - front-end UI
- http://localhost:8888/api/ - API

For additional details see README.md in the `ttt-api` and `ttt-front` folders 
