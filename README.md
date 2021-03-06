![easyTravel Logo](https://github.com/dynatrace-innovationlab/easyTravel-Builder/blob/images/easyTravel-logo.png)

# easyTravel-Docker

This project builds and deploys the [Dynatrace easyTravel](https://community.dynatrace.com/community/display/DL/Demo+Applications+-+easyTravel) demo application in [Docker](https://www.docker.com/). All components are readily available on the [Docker Hub](https://hub.docker.com/u/dynatrace/).

## Application Components

| Component | Component
|:----------|:---------
| mongodb   | A pre-populated travel database (MongoDB).
| backend   | The easyTravel Business Backend (Java).
| frontend  | The easyTravel Customer Frontend (Java).
| nginx     | A reverse-proxy for the easyTravel Customer Frontend (NGINX).
| loadgen   | A synthetic UEM load generator (Java).

## Run easyTravel in Docker

You can run easyTravel by using [Docker Compose](https://docs.docker.com/compose/) with the provided `docker-compose.yml` file like so:

```
docker-compose up
```

## Monitor easyTravel with Dynatrace AppMon

Please refer to the [Dynatrace-Docker](https://github.com/dynatrace/Dynatrace-Docker) project on how to quickly bring up an entire Dockerized Dynatrace environment. Then, use [Docker Compose](https://docs.docker.com/compose/) with the provided `docker-compose-withDtAppMon.yml` file to have the application monitored by [Dynatrace AppMon](http://www.dynatrace.com/en/application-monitoring/):

```
docker-compose -f docker-compose-withDtAppMon.yml up
```

## Problems? Questions? Suggestions?

This offering is [Dynatrace Community Supported](https://community.dynatrace.com/community/display/DL/Support+Levels#SupportLevels-Communitysupported/NotSupportedbyDynatrace(providedbyacommunitymember)). Feel free to share any problems, questions and suggestions with your peers on the Dynatrace Community's [Application Monitoring & UEM Forum](https://answers.dynatrace.com/spaces/146/index.html).

## License

Licensed under the MIT License. See the [LICENSE](https://github.com/dynatrace-innovationlab/easyTravel-Docker/blob/master/LICENSE) file for details.