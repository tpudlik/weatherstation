# Minimal Raspberry Pi Weather Station #

This project consists of two components:

*   A Python program for the Raspberry Pi which monitors temperature and
    humidity using a [DHT22][DHT22] sensor, and uploads the data to an
    Amazon Web Services (AWS) SQL database.
*   A web application meant to run on AWS that displays the data.

This is hardly a real weather station---for that, check out (say) Tor Hveem's
[Amatyr][Amatyr] project.  In fact, I built it for indoor use, to monitor how
the temperature inside the house changes with the time of day and the seasons.


## Hardware ##

### Bill of Materials ###

### Circuit diagram ###

See [this tutorial][DHT22 tutorial] for a circuit schematic.


## Software Installation and Configuration ##

### On the Pi ###

### On AWS ###

First, create a Postgres database instance in Amazon's Relational Database
Service (RDS).  Make sure external connections to the database are allowed.




## Why a Remote Database? ##

The Raspberry Pi is perfectly capable of hosting a SQL database and serving
web pages.  I decided to use a cloud solution to improve availability,
guarantee backup, and allow easy access to the database from devices other
than the Pi.


[Amatyr]: https://github.com/torhve/Amatyr
[DHT22]: https://www.adafruit.com/products/385
[DHT22 tutorial]: https://learn.adafruit.com/dht-humidity-sensing-on-raspberry-pi-with-gdocs-logging