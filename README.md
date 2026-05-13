# ecqm-content
To support the development of FHIR-based electronic Clinical Quality Measures (eCQMs) and digital Quality Measures (dQMs), the CQFramework organization hosts multiple content repositories. These repositories are all listed below with a short description of the intent and content of each:

|Repository|Description|Status|Build Site|
|----|----|----|----|
|[dqm-content-cms-2026](https://github.com/cqframework/dqm-content-cms-2026)|This repository contains example dQM content built using the USQualityCore 0.1.0-cibuild, US Core 6.1.0-derived, and CarinBB 2.1.1 models. The examples have been developed purely for testing purposes to demonstrate advanced dQM measure specification capability. Measure content in this repository was developed manually using the VSCode CQL Authoring plugin.|Active|[CI Build](http://build.fhir.org/ig/cqframework/dqm-content-cms-2026)|
|[dqm-content-qicore-2026](https://github.com/cqframework/dqm-content-qicore-2026)|This repository contains example dQM content built using the QICore 7.0.0, US Core 7.0.0, and CarinBB 2.1.1 models. The examples have been developed purely for testing purposes to demonstrate advanced dQM measure specification capability. Measure content in this repository was developed manually using the VSCode CQL Authoring plugin.|Stable|[CI Build](http://build.fhir.org/ig/cqframework/dqm-content-qicore-2026)|
|[dqm-content-cms-2025](https://github.com/cqframework/dqm-content-cms-2025)|This repository contains draft 2025AU content refactored to use the USQualityCore 0.1.0-cibuild, and US Core 6.1.0-derived models. All measure content in this repository was copied from the dqm-content-qicore-2025 repository and refactored using the VSCode CQL Authoring plugin.|Active|[CI Build](http://build.fhir.org/ig/cqframework/dqm-content-cms-2025)|
|[dqm-content-qicore-2025](https://github.com/cqframework/dqm-content-qicore-2025)|This repository contains draft 2025AU content built using MADiE against the QICore 6.0.0 model. All measure content in this repository was developed in the MADiE tool and exported as FHIR bundles that are then placed as source for a FHIR content implementation guide, including tests developed in MADiE and exported to the appropriate test directories so the tests can be run in the VSCode CQL Authoring plugin.|Stable|[CI Build](http://build.fhir.org/ig/cqframework/dqm-content-qicore-2025)|
|[ecqm-content-qicore-2025](https://github.com/cqframework/ecqm-content-qicore-2025)|This repository contains draft 2025AU content built using the QICore 6.0.0 model. Measure content in this repository was updated from measure packages initially exported from the MADiE tool, then uplifted to QICore 6.0.0 using the VSCode CQL Authoring plugin.|Active|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2025)|
|[dqm-content-cms-2024](https://github.com/cqframework/dqm-content-cms-2024)|This repository contains a subset of the content in the 2024 repository specifically built to support testing at the CMS Quality Conference.|Stable|[CI Build](http://build.fhir.org/ig/cqframework/dqm-content-cms-2024)|
|[ecqm-content-qicore-2024-subset](https://github.com/cqframework/ecqm-content-qicore-2024-subset)|This repository contains a subset of the content in the 2024 repository, focused on supporting the testing of measure release packaging. See the Manifest library examples in this repository for examples of measure release packages in the authoring, testing, and final release publication stages of the AU authoring process.|Stable|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2024-subset)|
|[ecqm-content-qicore-2024](https://github.com/cqframework/ecqm-content-qicore-2024)|This repository contains 2024AU content built using the QICore 4.1.1 model. Measure content in this repository was exported from the MADiE tool. NOTE: For the January 2025 Connectathon specifically, some of the measures in this repository have been updated with draft changes for the 2025AU cycle, but are still using QICore 4.1.1.|Stable|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2024)|
|[ecqm-content-qicore-2023](https://github.com/cqframework/ecqm-content-qicore-2023)|This repository contains 2023AU content built using the QICore model. Measure content in this repository was exported from the MADiE tool.|Legacy|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2023)|
|[ecqm-content-qicore-2022](https://github.com/cqframework/ecqm-content-qicore-2022)|This repository contains 2022AU content built using the QICore model, as opposed to FHIR directly. Measure content in this repository is intended to be able to imported into the MADIE tool, but not MAT-on-FHIR.|Legacy|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2022)|
|[ecqm-content-qicore-2021](https://github.com/cqframework/ecqm-content-qicore-2021)|This repository contains 2021AU content built using the FHIR model, but with QICoreElements libraries that facilitate accessing extensions defined in QICore. Measure content in this repository is exploratory in nature and is not intended to be able to be imported in MADIE or MAT-on-FHIR, only to support past connectathon usage. All current development efforts should be focused on the qicore-2022 repository. |Legacy|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2021)|
|[ecqm-content-qicore-2020](https://github.com/cqframework/ecqm-content-qicore-2020)|This repository contains 2020AU content built using the QICore model, as opposed to FHIR directly. Measure content in this repository is intended to be able to imported in MADIE, but not MAT-on-FHIR. |Legacy|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-qicore-2020)|
|[ecqm-content-r4-2022](https://github.com/cqframework/ecqm-content-r4-2022)|This repository contains 2022AU content for FHIR R4. Measure content in this repository should **not** make use of fluent functions to ensure that the libraries can be added to MAT-on-FHIR.|Legacy|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-r4-2022)|
|[ecqm-content-r4-2021](https://github.com/cqframework/ecqm-content-r4-2021)|This repository contains 2021AU content for FHIR R4.|Legacy|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-r4-2021)|
|[ecqm-content-r4](https://github.com/cqframework/ecqm-content-r4)|This repository contains 2020AU measure content for FHIR R4.|Legacy|[CI Build](http://build.fhir.org/ig/cqframework/ecqm-content-r4)|
|[draft-measures](https://github.com/cqframework/draft-measures)|This is the first draft measures repository and contains 2019AU and some 2020AU measure content for FHIR DSTU2, STU3, and R4.|Legacy|[CI Build](http://build.fhir.org/ig/cqframework/draft-measures)|

The measures in these repositories are examples and works in progress and should not be considered final specifications or recommendations for clinical guidance. These examples will help guide and direct the process of finding conventions and usage patterns that meet the needs of the various stakeholders in the measure development community.

All of these repositories are set up as FHIR IGs with auto-build so that commits to the repository will trigger a push to the FHIR build site.

Note that these are all _draft_ content in various stages of development, and that the newer repositories have more focus. Each repository has a _status_ that indicates:

* Active - The content in the repository is under active development and changes frequently
* Stable - The content in the repository is considered stable and supporting direct testing. Although fixes will be applied, the content is not under active development and does not change frequently
* Legacy - The content in the repository is no longer being updated and it provided solely for historical and legacy testing support

## Shared Libraries
To facilitate reuse of definitions by multiple measures, each repository contains shared libraries, as detailed below:

### FHIRHelpers
The FHIRHelpers library was initially defined as part of the CQL-to-ELM translator, and is still distributed there, to provide implicit conversions from the FHIR data types to CQL defined types (i.e. FHIR.string to System.String). The current version of the FHIRHelpers library is published as part of the [CQFramework Common IG](http://fhir.org/guides/cqf/common). However, current tooling does not yet have the ability to automatically download the library from this published location, so the FHIRHelpers library is copied to each individual repository with a unique version. Note that this version is also sometimes determined by the version assigned by the MAT. Documentation for the functions in FHIRHelpers is available in the [FHIRHelpers library page](https://build.fhir.org/ig/cqframework/cqf/Library-FHIRHelpers.html) of the CQF Common IG.

### FHIRCommon
The FHIRCommon library contains declarations that are common to all use of CQL with FHIR, including decision support rules, quality measures, and case reporting. Documentation for the FHIRCommon library is available in the [FHIRCommon library page](https://build.fhir.org/ig/cqframework/cqf/Library-FHIRCommon.html) of the CQF Common IG. Note that this library should NOT be used when using QICore authoring, use QICoreCommon instead.

### QICoreCommon
The QICoreCommon library contains declarations that are common to all use of CQL with QICore.

### CQMCommon (previously MATGlobalCommonFunctions)
The CQMCommon library contains declarations that are commonly used in eCQMs and shared across the logic of multiple measures, such as the `Encounter Inpatient` value set, and the `Inpatient Encounter` population criteria definition. This library also contains functions for calculating hospitalization duration as well as hospital arrival and departure times.

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

