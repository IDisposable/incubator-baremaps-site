---
layout: default
title: How to build with Maven
permalink: /developer-manual/how-to-build-with-maven/
---

# How to build with Maven

This guide describes the basics of compiling Baremaps from source. In order to run Apache Baremaps, you first need to install Java 17 or a later version.
[SDKMAN](https://sdkman.io/){:target="_blank"} provides a convenient Command Line Interface (CLI) to install and upgrade Java. We also suggest you use the most recent version of Maven
to compile [(at least 3.x.x)](https://maven.apache.org/download.cgi){:target="_blank"}. 

### Linux or OSX

To start you can run the command `mvn clean package` from the root folder of the Baremaps project.  Upon successful
compilation you should see something similar to the following output in your terminal. 
```
[INFO] Building zip: /path-to-project/baremaps/baremaps-cli/target/baremaps.zip
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for baremaps 0.7.1-SNAPSHOT:
[INFO] 
[INFO] baremaps ........................................... SUCCESS [  4.172 s]
[INFO] baremaps-core ...................................... SUCCESS [ 59.018 s]
[INFO] baremaps-benchmark ................................. SUCCESS [  1.775 s]
[INFO] baremaps-ogcapi .................................... SUCCESS [  9.796 s]
[INFO] baremaps-server .................................... SUCCESS [  0.787 s]
[INFO] baremaps-cli ....................................... SUCCESS [ 20.687 s]
[INFO] ------------------------------------------------------------------------
```

It is important to note the first line in the output above that notes where the location of the `baremaps.zip` file resides.
Referencing the location of the `baremaps.zip` file, you can run the following to unzip 
and place Baremaps into your `PATH`
```
$ unzip /path-to-project/baremaps/baremaps-cli/target/baremaps.zip
$ export PATH=$PATH:`pwd`/baremaps/bin
```

Executing the `baremaps` command should now result in an output similar to the following:

```
Usage: baremaps [COMMAND]
A toolkit for producing vector tiles.
Commands:
  import  Import OpenStreetMap data in the Postgresql database.
  update  Update OpenStreetMap data in the Postgresql database.
  export  Export vector tiles from the Postgresql database.
  serve   Serve vector tiles from the the Postgresql database.
```

From here, head into [Installing PostGIS](/getting-started/installing-postgis/) if you plan to work with vector tiles.

If you want to work on [Geocoding](/examples/geocoding/) or
[IP to location](/examples/ip-to-location/), head directly into the related examples.

### Windows TODO...
