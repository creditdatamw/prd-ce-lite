Pentaho Report Designer Lite Build
===

This project generates a _lite_ build of the [Pentaho Report Designer](https://help.pentaho.com/Documentation/8.2/Products/Report_Designer) by Hitachi Vintara.

Pentaho Report Designer is a visual report design tool and it's great for creating pixel perfect reports.

### Background / Motivation

We use Pentaho Report Designer, for example [here](https://github.com/creditdatamw/kapenta), and  sometimes our developers/designers need to (re-)download a version of the report designer.

The [pom](pom.xml) file in this repo creates a build of the Pentaho Report Designer that strips out some things that we don't really need (or use yet) for most reports. The result is a smaller build of the Pentaho Report Designer that takes less space on disk. Since internet is an issue in our country/environment, having a smaller sized package makes all the difference in time and cost ;)

### Versioning

The version for the lite build has the following form:

`<pentaho-version>-<lite-version>`

e.g. `8.3.0.0-371-lite-1`

### Building

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

*NOTE*: If you click the report-designer scripts and the program doesn't start you may not have enough RAM, you can change the JVM settings by editing the scripts - changing `-Xms1024m` to `-Xms512m` , for example - although this won't guarantee best or correct performance..

### Disclaimer

This is NOT an official Credit Data CRB Ltd project and the copyrights and trademarks belong Hitachi Vintara etc...

This project is licensed under the same license as the report designer, LGPL. Please see [pentaho-reporting](https://github.com/pentaho/pentaho-reporting) for more

