cd expense-tracker-api
docker-compose up --build

cd prometheus
docker-compose up --build

cd grafana
docker-compose up --build

cd expense-tracker
docker build -t frontend .
docker run -p 8080:8080 frontend

cd kong
docker-compose up --build

docker-compose down