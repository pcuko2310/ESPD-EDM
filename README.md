# ESPD Exchange Data Model (EDM)

## Introduction

The ESPD Exchange Data Model is the technical representation of the legal European Single Procurement Document. It is used to support interoperability between ESPD services provided all over Europe.

## Documentation

* [v2.0.2](https://espd.github.io/ESPD-EDM/v2.0.2/)
* [v2.0.1](https://espd.github.io/ESPD-EDM/v2.0.1/)
* [v2.0.0](https://espd.github.io/ESPD-EDM/v2.0.0/)
* [v1.0.3](https://espd.github.io/ESPD-EDM/v2.0.2/) [See v2.0.2 documentation, chapter "I.5 Forward compatibility"]
* [v1.0.2](https://espd.github.io/ESPD-EDM/v1.0.2/)
* [v1.0.1](https://github.com/ESPD/ESPD-EDM/blob/1.0.1/docs/src/main/asciidoc/index.adoc)

## Roadmap

* **Version 2.0.2** (April 2018): 
- Set of Schematron-based artefacts provided to validate REGULATED and SELF-CONTAINED ESPD Request and Response XML instances. Includes validation of the criteria taxonomy. See the artefacts in link:./dist/val[dist/val/] folder and the new online documentation chapter on XML validation.
- Set of XSL-T 2.0 stylesheets provided to convert ESPD Request and Response XML instances from v1.0.3 into REGULATED v2.0.2 XML instances. See the link:./dist/xslt/Versions_1-2_Mapping[dist/xslt/Versions_1-2_Mapping] folder.
- Documentation bugs fixed.

* **Version 1.0.3** (April 2018): Minor documentation fixes applied to version 1.0.2. The data model was not changed.  Only the documentation was updated to reflect the changes made until the July 2017 release of the Commission ESPD. It has no impact on current ESPD services based on v1.0.2. The update criteria taxonomy can be found here: ./dist/cl/ods/ESPD-CriteriaTaxonomy(Data-Structures)_V1.0.3.ods[Criteria Taxonomy (Data Structures)]. See also documentation about v2.0.2 chapter "I.5 Forward compatibility").

* **Version 2.0.1** (Jan. 2018): Bug fixes detected in the previous versions; change requests related to these bugs were collected in this Github Issues space (see Issues for the details. See also the Release Notes above and the 'dist/rn' folder for details on those issues related to v2.0.2 that have been closed). 

* **Version 2.0.0** (Sept. 2017): The goal of version 2.0.0 is that the ESPD-EDM is self contained. Meaning that public buyers can specify directly in their ESPD services criteria instead of defining them in the procurement document or the notice. Examples are that the public buyer can specify the number of years needed for the turnovers, the financial ratios needed for the procedure or that they can specify certificates needed. Something else that will be implemented in version 2.0.0 is the possibility to weight criteria which is important to reduce the number of participants in a procedure. Issues for this release are:
  * https://github.com/ESPD/ESPD-EDM/issues/

* **Version 1.0.2**: Version 1.0.2 has no impact on current implementation. It was published in July 2016. It fixes the issue: 
  * https://github.com/ESPD/ESPD-EDM/issues/2
  
* **Version 1.0.1**: Version 1.0.1 is used since December 2015. This version is based on UBL 2.1.

## Installation

The recommended way to get started using the `exchange-model` in a `Java` project is with a dependency management system.

### With Maven

```xml
<dependency>
  <groupId>eu.europa.ec.grow.espd</groupId>
  <artifactId>exchange-model</artifactId>
  <version>1.0.2</version>
</dependency>
```

### With Gradle

```groovy
dependencies {
    compile("eu.europa.ec.grow.espd:exchange-model:1.0.2")
}
```

### Version 2.0.2

**Please note that this version requires Java 8**

```xml
<dependency>
  <groupId>eu.europa.ec.grow.espd</groupId>
  <artifactId>exchange-model2</artifactId>
  <version>2.0.2-SNAPSHOT</version>
</dependency>
```

Version 2 of the `Exchange Model` has a different `artifactId`, i.e. `exchange-model2`, in order to support 
the usage of both versions at the same time inside a `Java` `Maven` project.

In order to use the snapshot version, you might have to enable the `Maven` snapshot repository in your `pom.xml`.


```xml
<repositories>
  <repository>
    <id>oss-sonatype</id>
    <name>oss-sonatype</name>
    <url>https://oss.sonatype.org/content/repositories/snapshots/</url>
    <snapshots>
      <enabled>true</enabled>
    </snapshots>
  </repository>
</repositories>
```

## Use
The ESPD-EDM is made publicly available through Github. 
* If you just want to browse or access the model, you don't need to be registered in Github.
* If you want to create issues concerning the ESPD-EDM you have to be a registered user in Github. Please assign all issues in this repository to paulakeen
