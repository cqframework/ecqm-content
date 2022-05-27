# ecqm-content
To support the development of FHIR-based electronic Clinical Quality Measures (eCQMs) and digital Quality Measures (dQMs), the CQFramework organization hosts multiple content repositories. These repositories are all listed below with a short description of the intent and content of each:

|Repository|Description|Build Site|
|----|----|----|
|[draft-measures](https://github.com/cqframework/draft-measures)|This is the first draft measures repository and contains 2019AU and some 2020AU measure content for FHIR DSTU2, STU3, and R4.|[CI Build](http://build.fhir.org/ig/cqframework/draft-measures)|
|[ecqm-content-r4](https://github.com/cqframework/ecqm-content-r4)|This repository contains 2020AU measure content for FHIR R4.|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-r4)|
|[ecqm-content-r4-2021](https://github.com/cqframework/ecqm-content-r4-2021)|This repository contains 2021AU content for FHIR R4.|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-r4-2021)|
|[ecqm-content-r4-2022](https://github.com/cqframework/ecqm-content-r4-2022)|This repository contains 2022AU content for FHIR R4.|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-r4-2022)|
|[ecqm-content-qicore-2020](https://github.com/cqframework/ecqm-content-qicore-2020)|This repository contains 2020AU content built using the QICore model, as opposed to FHIR directly. |[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2020)|
|[ecqm-content-qicore-2021](https://github.com/cqframework/ecqm-content-qicore-2021)|This repository contains 2021AU content built using the FHIR model, but with QICoreElements libraries that facilitate accessing extensions defined in QICore.|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2021)|
|[ecqm-content-qicore-2022](https://github.com/cqframework/ecqm-content-qicore-2022)|This repository contains 2022AU content built using the QICore model, as opposed to FHIR directly.|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2022)|

The measures in these repositories are examples and works in progress and should not be considered final specifications or recommendations for clinical guidance. These examples will help guide and direct the process of finding conventions and usage patterns that meet the needs of the various stakeholders in the measure development community.

All of these repositories are set up as FHIR IGs with auto-build so that commits to the repository will trigger a push to the FHIR build site.

Note that these are all _draft_ content in various stages of development, and that the newer repositories have more focus.

General documentation for the repository structure and bundling tooling follows.

## Repository Structure
Each repository is setup like any HL7 FHIR IG project including the CQL files and test data which means the file structure will be as follows:

```
   |-- _genonce.bat
   |-- _genonce.sh
   |-- _refresh.bat
   |-- _refresh.sh
   |-- _updatePublisher.bat
   |-- _updatePublisher.sh
   |-- _updateCQFTooling.bat
   |-- _updateCQFTooling.sh
   |-- ig.ini
   |-- bundles
       |-- mat
           |--<mat export bundles>
       |-- measure
           |--EXM124
   |-- input
       |-- ecqm-content-r4-2022.xml
       |-- cql
           |-- EXM124.cql
       |-- resources
           |-- library
               |-- EXM124.json
           |-- measure
               |-- EXM124.json
       |-- tests
           |-- measure
               |-- EXM124
       |-- vocabulary
           |-- valueset
```

## Refresh IG Processing

The CQF Tooling provides support for refreshing measure and library resources based on
the content of the CQL libraries, as well as packaging the measures as artifacts that
include dependencies and test cases.

To run this tooling, make sure it is available locally using the `_updateCQFTooling` script,
then run the `_refresh` script. This script should be run whenever CQL content changes,
and prior to the publishing process.

## Extracting MAT Packages

The CQF Tooling provides support for extracting a MAT exported package into the
directories of this repository so that the measure is included in the published
implementation guide. To do this, place the MAT export files (unzipped) in a
directory in the `bundles\mat` directory, and then run the following tooling
command:

```
[tooling-jar] -ExtractMatBundle bundles\mat\[bundle-directory]\[bundle-file]
```

For example:

```
input-cache\tooling-1.4.1-SNAPSHOT-jar-with-dependencies.jar -ExtractMATBundle bundles\mat\CLONE124_v6_03-Artifacts\measure-json-bundle.json
```

Then run the `_refresh` command to refresh the implementation guide content with
the new content, and then run `_genonce` to publish the implementation guide.

