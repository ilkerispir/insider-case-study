# NBA Case Study

## Preview Link
* https://insider.ilkerispir.com/

## API Reference

#### Get all items

```http
  POST /api/teams
```

#### Get item

```http
  POST /api/players
```

## Run Command

```bash
docker run -d -p 8080:8080 ilkerispir/nba
```

Contanier push GCP repo 
```
gcloud builds submit --tag gcr.io/ikerispir/nba-case
```

Contanier deploy Cloud Run 
```
gcloud run deploy nba-case --image ikerispir/nba --region europe-west3 --platform managed --allow-unauthenticated
```

## Remove all containers & images
```
docker rm -vf $(docker ps -a -q)
docker rmi -f $(docker images -a -q)
```

## Backend

* Lang: [Golang](https://golang.org/)
* Framework: [Gin Gonic](https://gin-gonic.com/)

## Frontend

* Lang: [Node v16](https://nodejs.org/en/)
* Framework: [React.js](https://reactjs.org/)
* UI Kit: [Antd](https://ant.design/)
* Modules: [Axios](https://www.npmjs.com/package/axios)


## React.js Error Watch Problem
```bash
fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```