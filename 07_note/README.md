## 2026-04-25
- Created GitHub repo
- Added initial README
- Added CSV data

## 2026-05-07
- Modified initial README

## 2026-05-29
feat: complete Phase 1 PoC - initial RDF storage and SPARQL verification
- Successfully deployed Apache Jena Fuseki (v5.6.0) in a local environment.
- Loaded the initial explicit knowledge dataset (infrastructure project domain).
- Verified data extraction using a standard SPARQL query (?sub ?pred ?obj).
- Visualized data fragmentation/vocabulary mismatch in the graph (e.g., duplicated project nodes), proving the core problem statement of explicit knowledge silos.

## 2026-06-09
- Updated initial README

## 2026-06-16
- Updated initial README

## 2026-06-24
- Neo4j Aura Introduction

## 2026-08-03

### Environment Setup

- Installed Protégé Desktop 5.6.9
- Confirmed successful startup
- Created the first ontology
- Saved the ontology as an `.owl` file

### Initial Ontology Modeling

- Created the following classes:
  - `Dataset`
  - `Sample`
  - `Measurement`
  - `TemperatureMeasurement`
  - `PHMeasurement`
- Defined `TemperatureMeasurement` and `PHMeasurement` as subclasses of `Measurement`
- Created the following object properties:
  - `hasSample`
  - `hasMeasurement`
- Defined object property domains and ranges:
  - `hasSample`: `Dataset` → `Sample`
  - `hasMeasurement`: `Sample` → `Measurement`
- Created the following data properties:
  - `sampleID`
  - `measurementValue`
  - `hasUnit`
- Defined data property domains and ranges:
  - `sampleID`: `Sample` → `xsd:string`
  - `measurementValue`: `Measurement` → `xsd:decimal`
  - `hasUnit`: `Measurement` → `xsd:string`

### Manual Data Instantiation

- Created a small CSV dataset containing sample IDs, temperature values, and pH values
- Manually instantiated one CSV row in Protégé as a reference example
- Created the following individuals:
  - `Dataset01`
  - `S001`
  - `S001_Temperature`
  - `S001_PH`
- Added object property assertions:
  - `Dataset01 hasSample S001`
  - `S001 hasMeasurement S001_Temperature`
  - `S001 hasMeasurement S001_PH`
- Added data property assertions:
  - `S001 sampleID "S001"`
  - `S001_Temperature measurementValue 25.1`
  - `S001_Temperature hasUnit "degreeCelsius"`
  - `S001_PH measurementValue 7.2`
  - `S001_PH hasUnit "pH"`

### Notes

- Confirmed the distinction between classes, individuals, object properties, and data properties
- Practiced defining domains and ranges for ontology properties
- Manually modeled one CSV row to understand the target RDF/OWL structure before automating data import
- Confirmed the local Protégé environment for future ontology, SHACL, and CSV-to-RDF experiments
