# Average Bicycle Counts by Day and Hour

[![goodtables.io](https://goodtables.io/badge/github/Stephen-Gates/bicycle-counts.svg)](https://goodtables.io/github/Stephen-Gates/bicycle-counts)

This dataset contains average counts of bicycle traffic by hour of the day and day of the week. It includes the location of data collection sites.

The data is a snapshot and not planned to be kept up-to-date. The main purpose of this repository is to develop a data package and schemas for this dataset.

## Data
The data is collected from bicycle counters across 14 active transport sites. As more sites come on line in the future these will be added to the dataset. These bicycle counters were installed in conjunction with the State Cycle Unit and are permanent installations that provide 24/7 bicycle counting data.

The [data](https://github.com/Stephen-Gates/bicycle-counts/tree/master/data) is made up of two of files.

1. [Average Bicycle Counts by Day and Hour](https://data.qld.gov.au/dataset/average-bicycle-counts-by-day-and-hour/resource/48adfb7a-28d1-4b00-9330-fc73c9ecbdf2), by Transport and Main Roads, Queensland Government, licensed under [Creative Commons Attribution](http://creativecommons.org/licenses/by/3.0/au/) sourced on 20 September 2016.
2. [Active transport sites](https://data.qld.gov.au/dataset/average-bicycle-counts-by-day-and-hour/resource/6b22171f-fb7a-477c-8225-654b118533cd), by Transport and Main Roads, Queensland Government, licensed under [Creative Commons Attribution](http://creativecommons.org/licenses/by/3.0/au/) sourced on 20 September 2016.

Each data file is defined by a [schema](https://github.com/Stephen-Gates/bicycle-counts/tree/master/schemas). The schemas follow the [json table schema specification](http://specs.frictionlessdata.io/json-table-schema/).

These schemas will be combined into a [datapackage.json](https://github.com/Stephen-Gates/bicycle-counts/blob/master/datapackage.json) file to fully describe the data collection. The datapackage.json file will follow the [data package specification](http://specs.frictionlessdata.io/data-packages/).

## Preparation
The data was downloaded from the source and then uploaded to GitHub.

## Tests
The focus of the tests is to ensure the schemas are correct. The [tests](https://github.com/Stephen-Gates/bicycle-counts/tree/master/tests) are invalid data that is used to ensure the schema detects all errors (e.g. incorrect [types](http://specs.frictionlessdata.io/json-table-schema/#field-types-and-formats) and violated [constraints](http://specs.frictionlessdata.io/json-table-schema/#field-constraints)).

## Results
The [results](https://github.com/Stephen-Gates/bicycle-counts/blob/master/results/results.md) can be verified using links to  [Good Tables](http://goodtables.okfnlabs.org). Tests include:
- testing the valid data without a schema
- testing the valid data with a schema
- testing the invalid data with a schema

Good Tables doesn't check all types of errors (yet). Somethings not checked include:
- Foreign keys. (See Good Tables [#17](https://github.com/frictionlessdata/goodtables/issues/17),  [#8](https://github.com/frictionlessdata/goodtables/issues/8))
- Some constraints (See Good Tables [#55](https://github.com/frictionlessdata/goodtables/issues/55))

### Continuous Testing
[GoodTables.io](http://goodtables.io/) provides continuous data testing. Everytime there's a change in this repository the tests are re-run.
Here's the latest results:
[![goodtables.io](https://goodtables.io/badge/github/Stephen-Gates/bicycle-counts.svg)](https://goodtables.io/github/Stephen-Gates/bicycle-counts)

## Schemas
The [schemas](https://github.com/Stephen-Gates/bicycle-counts/tree/master/schemas) were created using [Data Packagist](http://datapackagist.okfnlabs.org). Using Data Packagist:

- add some basic information about the data file (name, description, license, etc.)
- upload the data file

Data Packagist will create a datapackage.json file for you. Download this file.

Good Tables can only use a json table schema for validation ([see goodtables-web #65](https://github.com/frictionlessdata/goodtables-web/issues/65)). You can extract the json table schema from the datapackage.json file. It's this bit `{fields: [...]}`. Save this a separate file.

Edit the schema file with a text editor (e.g. [ATOM](https://atom.io), [jsoneditoronline.org](http://www.jsoneditoronline.org)) and add constraints, refine types and formats, etc. You may like to use the [json table schema schema](https://raw.githubusercontent.com/frictionlessdata/schemas/master/json-table-schema.json) to improve your editing experience.

Some constraints use regular expressions to define a pattern. Use a online tool to help create and test a regular expresion e.g. [regexr.com](http://regexr.com/) or [regex101](https://regex101.com/).

## View the Data Package
Data packages are about providing machine-readable metadata for your data. You can [view a human-readable version of the data package](http://data.okfn.org/tools/view?url=https%3A%2F%2Fraw.githubusercontent.com%2FStephen-Gates%2Fbicycle-counts%2Fmaster%2Fdatapackage.json) data, and readme files using the [Data Package Viewer](http://data.okfn.org/tools/view). There are a couple of [issues](https://github.com/okfn/data.okfn.org-new/issues) with the viewer including providing an incorrect link to the metadata [data.okfn.org-new #9](https://github.com/okfn/data.okfn.org-new/issues).

## License
All items in this repository, apart from the data, are licensed under [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/).
