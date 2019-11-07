Appointment Scheduler
================

**Appointment** is a custom web application that allows you to book
appointments with you via the web. Moreover, it provides the ability to sync your data with
Google Calendar so you can use them with other services. It will run smoothly with
your existing website, because it can be installed in a single folder of the server and of course,
both sites can share the same database.

### Features

The project was designed to be flexible and reliable so as to be able to meet the needs of any
kind of enterprise. You can read the main features of the system below:

* Full users and appointments management.
* Services and service providers organization.
* Workflow and booking rules.
* Google Calendar synchronization.
* Email notifications system.
* Translated user interface.
* User community support.

### Installation

Since it is a web application, it runs on a web server and thus you will need to
perform the following steps in order to install the system on your server:

* Make sure that your server has Apache/Nginx, PHP and MySQL installed.
* Create a new database (or use an existing).
* Copy the source folder on your server.
* Make sure that the "storage" directory is writable.
* Rename the "config-sample.php" file to "config.php" and set your server properties.

### Docker
To start using Docker in development configuration, with source files mounted into container, run:
```
docker-compose up
```

Production deployment can be made by changing required values in .env file (DB_PASSWORD, APP_URL, APP_PORT) and running:
```
docker-compose -f docker-compose.prod.yml up -d
```

Database data will be stored in named volume `easyappointments_easy-appointments-data`, and app storage (logs, cache, uploads) in `easyappointments_easy-appointments-storage`.
To find where exactly they are stored, you can run 
```
docker volume inspect easyappointments_easy-appointments-storage
```

Production containers will automatically be restarted in case of crash / server reboot. For more info, take a look into `docker-compose.prod.yml` file.

