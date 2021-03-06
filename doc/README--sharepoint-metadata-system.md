![version](https://img.shields.io/badge/Version-8.0-green)


# FGC CRISPR Sharepoint Metadata database

## Table of Contents

* [Overview](#intro)
* [Entering data](#entry)
* [Approving Multiple Entries](#apprv)
* [Validating the analysis config](#valid)
* [Bugs, Issues, or Requests](#bugs)
* [Acknowledgements](#ack)

## <a name="intro"></a> Overview

The FGC CRISPR Metadata system performs the following functions:

* Provides a database schema and data-entry system for gathering relevant metadata for FGC CRISPR screens (e.g. Cas 9 activity, Cell model, Sample types, etc).
* Produces an analysis config that can be provided to the AZ/CRUK [CRISPR analysis pipeline](https://bitbucket.astrazeneca.com/projects/DA/repos/az-cruk-crispr-pipeline/browse) for generating candidate pooled-CRISPR screen hits.
* Provides a means to validate the data in the analysis pipeline config JSON file.

## <a name="entry"></a> Entering data

Whenever metadata for a new screen is available, the following steps should be followed:

1. Create new entries for any new 'Entity Concepts' so that they are available in the drop-down menus in the main data tables.
2. Enter the data in the following order so that parent fields are available in the relevant drop-down menus in each table:
    1. Project
    2. Experiment
    3. Experiment-Sample
    4. Sample-Sequencing Request
    5. Sequenced Sample
    6. Analysis
    7. Comparison
    8. Comparison Sample
3. Once you are happy that everything is there then approve all the new rows in each table (see [Approving Multiple Entries](#apprv) to speed this up).
4. Once approved, a new analysis config JSON file will be produced in the 'Output Files' section (see Navigation panel at the top).

![output](output_files.png)

## <a name="apprv"></a>Approving Multiple Entries

Approving each row in each table one at a time is very slow. This can be sped up as follows:

1. When in a table view, click on the left-most circle at the top of the table so that ticks appear down the left-hand side for all the rows in the table.

![toggle](toggle.png)

2. Click on the 'details pane' icon (an 'i' in a circle in the top-right).

![details](details_pane.png)

3. In the 'Bulk edit properties' side-panel, in the 'Item Status' drop-down menu select 'Approved'.

![bulk edit](bulk_edit.png)

## <a name="valid"></a> Validating the analysis config JSON

The analysis config JSON can be validated using an R markdown script provided in the library for the Sharepoint site and linked to in the Navigation panel.

## <a name="bugs"></a> Bugs, Issues, or Requests

Please contact [Alex Kalinka](mailto:alex.kalinka@cancer.org.uk).

## <a name="ack"></a> Acknowledgements

|Task|Responsible|
---|---|
|Schema design|Jenny McKelvie, Ultan McDermott, Mike Firth|
|Sharepoint implementation|James Beckenham|
|Sharepoint admin|James Beckenham|
|Updated design for v8|Alex Kalinka, Jennifer Hillis, David Walter|

