# Metadata on table structure

Data values are often written in tables.
To know what a value within the table actually means, one must interpret metadata.
The column header gives information on the documented parameter, e.g. the abbreviation "TOC" in the column header can mean "total organic carbon, measured by a laboratory combustion method in weight-percentage".
This actual meaning can be documented within:
 - the table in additional header, or comment rows (e.g. example RIES, SWIG),
 - an additional document, e.g. an pdf report (e.g. example LENZ and SEIBERT), or
 - in formalized structures (e.g. table metadata in example for Bonares metadata, [example for pangaea metadata](https://doi.pangaea.de/10.1594/PANGAEA.971025) or [frictionless table schema](https://specs.frictionlessdata.io//table-schema/)).

The position of a value in relation to other columns is relational metadata, so all values within one row usually belong to one single observation or event, which is uniquely identified by a primary key.
This primary key can be a single column, e.g. the ID of an experiment or observation, or can be a combination of multiple columns, e.g. a time stamp in addition to the experiment ID.

## Using data of tables

To uptake foreign data from published tables for own analysis workflows one needs to read and understand the metadata.
Humans are easily able to link the description within pdf-reports to the table and can then manually extract relevant data values.
Nevertheless, this manual linkage is a time intensive process, which can be done for single foreign data sets, but becomes unrational for a large number of foreign data sets.

By providing the metadata within a formalized structure, one allows machines to interpret the metadata and to combine data values of different data sets for specific measured parameters for an own analysis.
Within SoilPulse we applied the fricionless table schema to document table metadata and to make cross data set queries, while the pangaea [data warehouse](https://www.pangaea.de/tools/) demonstrates a comparable functionality.

## Pangaea schema / metadata

Pangaea holds for every table column the parameter name, its abbreviation, Unit and a pangaea internal ID out of a [provided list of parameters](https://www.pangaea.de/lists/parameter/all-byname), so data can be queried across data sets within pangaea.
This metadata is provided graphically when [displaying a record of pangaea at the website](https://doi.pangaea.de/10.1594/PANGAEA.937089) and is provided with the [downloadable data file](https://doi.pangaea.de/10.1594/PANGAEA.937089?format=textfile).
The column headers can be shown as "variableMeasured" in the [Knowledgehub](https://cordra.knowledgehub.nfdi4earth.de/objects/n4e/dthb-oai-pangaea.de-doi-10.1594-PANGAEA.937089) and as "subjects" at [datacite](https://api.datacite.org/dois/10.1594/PANGAEA.937089). 
The knowledgehub provides the distribution URL to the actual data file, while datacite references only to the pangaea landing page of the record.

The python package pangaeapy allows to recast pangaea datasets to the frictionless schema, including information on unit and putting the concept/ detailed description of pangaea into the frictionless field 'title'.
E.g.:  `{'name': 'Infiltration', 'title': 'Infiltration rate', 'type': 'number', 'unit': 'min/cm'}`

## Bonares schema / metadata

Bonares provides table structure metadata in xml exports within the tags `<bnr:column></bnr:column>`, including information on the name, description, unit, data type and missing values for each column ([example](https://maps.bonares.de/finder/resources/dataform/xml/6e28000a-ee94-4a09-83fd-69223d6ddd26)).

## Frictionless schema

The python package [friction-py](https://github.com/frictionlessdata/frictionless-py) applies the fricitonless [table schema](https://specs.frictionlessdata.io//table-schema/).
This can be extended for units ([applied by unitpackage](https://github.com/echemdb/unitpackage)) and concepts and methods, as applied by SoilPulse with references to controlled vocabularies ([example in development](https://github.com/SoilPulse/MetadataGenerator/blob/create_examples/catalogue/temp_1/to_publish/piped_package.json)).
