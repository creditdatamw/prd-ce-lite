[![](https://img.shields.io/github/license/creditdatamw/prd-ce-lite.svg)](./LICENSE)
![](https://travis-ci.org/creditdatamw/prd-ce-lite.svg?branch=master)

Pentaho Report Designer Lite Build
===



Pentaho Report Designer is a visual report design tool that's great for designing reports that can be exported to PDF, HTML, Excel etc... This project generates a _lite_ build of the [Pentaho Report Designer](https://help.pentaho.com/Documentation/8.2/Products/Report_Designer).


### Background / Motivation

We use Pentaho Report Engine, for example [here](https://github.com/creditdatamw/kapenta), and  oftentimes our developers/designers need to download the (updated) Report Designer - a process which takes time due to the large size of the default build.

The [pom](pom.xml) file in this repo creates a build of the Pentaho Report Designer that:

* strips out some things that we don't really need (or use yet) for most reports;
* is smaller than the stock/default build of the Pentaho Report Designer
* includes the [Maria DB Java Library](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/)

### Versioning

The version for the lite build has the following form:

`<pentaho-version>-<lite-version>`

e.g. `8.3.0.0-371-lite-2`

### Building

#### Pre-requisites for building the project:
* Git
* Maven, version 3.5+
* Java JDK 1.8

```sh
$ git clone https://github.com/creditdatamw/prd-ce-lite.git
$ cd prd-ce-lite
$ mvn clean install
# A zip file will be created in the target directory
```

### Downloading Releases

We may upload builds via the [releases page](https://github.com/creditdatamw/prd-ce-lite/releases) but until then, see instructions above for building from source.

### System Requirements

You will need to have Java 8+ to run the Pentaho Report Designer and atleast 2 GB of RAM.

*NOTE*: If you try to run the report-designer scripts and the program doesn't start it's possible that you do not have enough RAM. Fortunately, you can change the JVM settings by editing the approapriate script for your OS (e.g. `report-designer.bat` on Windows). You can try to reduce the required memory by changing `-Xms` JVM option. For example from, `-Xms1024m` to `-Xms512m` - although we can't guarantee best  performance with such a 

### Disclaimer

This is NOT an official Credit Data CRB Ltd project and the copyrights and trademarks belong Hitachi Vintara etc...

This project is licensed under the same license as the report designer, LGPL. Please see [pentaho-reporting](https://github.com/pentaho/pentaho-reporting) for more
