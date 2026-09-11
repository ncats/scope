# SCOPE WORKFLOW README

This README provides the essential information required to run the SCOPE workflow.

A small test dataset is included with the workflow for testing and execution purposes. The complete screening library and corresponding hit information used in the SCOPE manuscript are available in the Supplementary Information and can also be used as inputs to the workflow.

# FILES INCLUDED

SCOPE_Workflow.knwf
KNIME workflow implementing the SCOPE analysis. The workflow was developed and tested using KNIME version 4.5.3.
Test_Input_Background.xlsx
Example screening-library input file for testing the SCOPE workflow.
Test_Input_Hits.xlsx
Example hit-list input file containing the Sample IDs of screening hits.

# MYSQL CONNECTOR CONFIGURATION

The MySQL Connector nodes in the workflow are pre-populated with the required hostname and database information, together with the following credentials:

Username: knime
Password: ncats

Windows:
The MySQL Connector node was tested using the default MySQL 8 driver (Version 8.0.0).

If connection issues are encountered, add the following JDBC parameter:

useSSL = false

macOS:
Select an available built-in MySQL 8 driver for the connection, for example:

MySQL v8.0.29 (ID: built-in-mysql-8.0.29)

# EXTERNAL DATABASE RESOURCES

SCOPE accesses PubChem, ChEMBL, and IUPHAR programmatically using their corresponding APIs or database connections.

Users must separately obtain the following files for PharmGKB and DrugBank:

PharmGKB
Required files:

chemicals.tsv
relationships.tsv

Download from:
https://www.clinpgx.org/downloads

DrugBank
Required file:

Full DrugBank database XML file

Users must obtain the appropriate DrugBank license before downloading and using the database.

After downloading these files, provide them as inputs to the corresponding database metanodes within the SCOPE workflow.  