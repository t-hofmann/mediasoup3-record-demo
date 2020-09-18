# Recording Demo

NOTE: Work in Progress not yet fully working.
"Start Record" works after patch is applied (refer to pull-request on typo "videoCodec").
"Stop Record" seems not to work.

The demo is implemented with docker and docker-compose.
The docker-compose.yml defines two services:
- recording-server
- recording-app

The local directory `./recordings` is mounted as a volume into the server, recorded files will be stored there.

The access point to the Web-GUI is provided by the "recording-app"-service and is available at:
https://localhost:8080

## Usage

- first start

    `$> docker-compose up -d`

- subsequent starts

  `$> docker-compose start`

- stopping services

  `$> docker-compose stop`

- viewing log files

  `$> docker-compose logs -f`
