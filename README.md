Part of the SPA 2015 Distributed Databases session. This is a
single node of a diy distributed database. It's a RESTful API
server that wraps up a simple integer to string map.

## Installation
Executables have been pre-built for Windows.
You can find them on the 
[downloads page](https://github.com/vgrigoriu/diy-dist-db-node/blob/master/downloads/snapshot/downloads.md).
From this page find the distribution relevant to you, follow it's link, and then click on
GitHub "Raw" button to download. Then unzip to get the executable.

## Running
Call the program passing it a free local PORT.

    diy-dist-db-node <PORT>

## Adding things
Add things to the map with HTTP POST. For example, in Powershell:

```powershell
curl http://localhost:<PORT>/things -Method POST -ContentType application/json -Body '{"Id": 3, "Value": "cucu"}'
```

## Querying things
To query for a particular thing in the map use an HTTP GET
request with the thing's id number.

    curl http://localhost:<PORT>/things/3 

## Listing all things
To list everything in the map, use a single HTTP GET request.

    curl http://localhost:<PORT>/things
