## Source Nodes
Reference: [Source Nodes](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=nodes-overview)

|    | Node | Description |
| --- | :--- | :---------- |
| ![Database](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/databasenodeicon.jpg)  | Database | Imports data from a database using ODBC (Open Database Connectivity), including Microsoft SQL Server, Db2, Oracle, and others.. |
| ![Excel](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/excelimportnodeicon.jpg) | Excel | Imports data from a Microsoft Excel file (.xlsx or .xls). |
| ![Fixed File](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/fixedfilenodeicon.jpg) | Fixed File | Imports data from fixed-field text files, i.e. files whose fields are not delimited but start at the same position and are of a fixed length. |
| ![Statistics File](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/spssfilenodeicon.jpg) | Statistics File | Reads data from an IBM SPSS Statistics file (.sav or .zsav), as well as cache files saved in IBM SPSS Modeler. |
| ![Variable File](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/varfile_node_icon.jpg) | Variable File | Reads data from text files, like .csv (Comma-Separated Values) or .dat files. |


## Record Operations Nodes
Reference: [Record Operations Nodes](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=nodes-overview-record-operations)

|    | Node | Description |
| --- | :--- | :---------- |
| ![Aggregate](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/aggregatenodeicon.jpg) | Aggregate | Summarizes info overall records. |
| ![Append](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/appendnodeicon.jpg) | Append | Adds records from one dataset to another (like `Union` in SQL). |
| ![Balance](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/balancenodeicon.jpg) | Balancing | Makes the distribution of a categorical field more equal. |
| ![Distinct](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/distinctnodeicon.jpg) | Distinct | Removes or keeps duplicate records & create a composite record. |
| ![Merge](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/mergenodeicon.jpg) | Merge | Adds fields from one dataset to another. |
| ![Sample](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/samplenodeicon.jpg) | Sample | Draws simple and complex samples. |
| ![Select](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/select_node_icon.jpg) | Select | Selects or discards a subset of records from the data stream. |
| ![Sort](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/sortnodeicon.jpg) | Sort | Sorts records into ascending or descending order based on the values of one or more fields. |
| ![Space-Time-Boxes](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/spacetimenodeicon.jpg) | Space-Time-Boxes | Describes where an entity is, at what point in time, by combining a spatial grid with a time interval. |

## Field Operations Nodes
Reference: [Field Operations Nodes](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=nodes-field-operations-overview)

|    | Node | Description |
| --- | :--- | :---------- |
| ![Automated Data Preparation (ADP)](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/adp_node_icon.jpg) | Auto Data Prep | Analyzes data and applies or recommends fixes, deriving new attributes, and sampling. |
| ![Binning](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/binningnodeicon.jpg) | Binning | Recodes a continuous field into a nominal field. |
| ![Derive](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/derive_node_icon.jpg) | Derive | Creates one or more fields from one or more fields. Creates field(s) as: formula, flag, nominal, state, count, and conditional. |
| ![Filler](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/fillernodeicon.jpg) | Filler | Replaces field values and changes storage. You can replace values based on: a CLEM condition, or to replace all blanks or null values with a specific value. |
| ![Filter](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/filternodeicon.jpg) | Filter | Removes and renames fields to map them from a source to another. |
| ![Reclassify](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/reclassifynodeicon.jpg) | Reclassify | Transforms (recodes) a set of categorical values to another. Useful for reducing categories. It can replace an existing field or create a new one. |
| ![Restructure](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/restructurenodeicon.jpg) | Restructure | Expands a continuous field into a series of fields, indexed by a nominal field. |
| ![Set to Flag](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/settoflagnodeicon.jpg) | SetToFlag | Derives multiple flag fields based on the categorical values defined for one or more nominal fields. |
| ![Type](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/typenodeicon.jpg) | Type | Specifies field metadata and properties. Like the measurement level (continuous, nominal, ordinal, or flag). |

## Graphs Nodes
Reference: [Graph Nodes](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=nodes-common-graph-features)

|    | Node | Description |
| --- | :--- | :---------- |
| ![Distribution](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/distributionnodeicon.jpg) | Distribution | Shows the occurrence of categorical values, or the relation between two categorical fields. |
| ![Histogram](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/histogramnodeicon.jpg) | Histogram | Visualizes the relation between one categorical and one continuous. |
| ![Plot](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/plotnodeicon.jpg) | Plot | Shows the relationship between numeric fields. |

## Output Nodes
Reference: [Output Nodes](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=nodes-overview-output)

|    | Node | Description |
| --- | :--- | :---------- |
| ![Data Audit](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/dataauditnodeicon.jpg) | Data Audit | Provides a comprehensive first look at the data, summary statistics, histograms. |
| ![Matrix](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/matrixnodeicon.jpg) | [Matrix](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=nodes-matrix-node) |  Creates a table that shows relationships between 2 categorical fields. See [Matrix node output browser](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=node-matrix-output-browser) for Chi-square. |
| ![Means](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/meansnodeicon.jpg) | Means | Visualizes the relation between 1 categorical field & 1 continuous field. |
| ![Statistics](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/statisticsnodeicon.jpg) | Statistics | Provides basic summary information about numeric fields. |
| ![Table](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/table_node_icon.jpg) | Table | Displays the data in a table format, which can also be written to a file. |
| ![Analysis](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/analysisnodeicon.jpg) | Analysis | Performs various comparisons between predicted values and actual values for one or more model nuggets (supervised models only). |
| ![Transform](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/transformnodeicon.jpg) | Transform | Allows you to select and visually preview the results of transformations before applying them to selected fields. |
| ![Set Globals](https://www.ibm.com/docs/en/SS3RA7_18.4.0/modeler_mainhelp_client_ddita/clementine/images/setglobalsnodeicon.jpg) | Set Globals | Computes summary values that can be used in CLEM expressions in other nodes. |


## Modeling Nodes
Reference: [Modeling Nodes](https://www.ibm.com/docs/en/spss-modeler/18.4.0?topic=overview-modeling-nodes)

|    | Node | Description |
| --- | :--- | :---------- |
| ![Auto Classifier](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/binaryclassifiernodeicon.jpg) | Auto classifier | Constructs and compares predictive models. |
| ![Auto Numeric](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/rangepredictornodeicon.jpg) | Auto Numeric |Allows comparison and creation of predictive models for continuous numeric outcomes (regression). |
| ![Auto Cluster](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/autoclusternodeicon.jpg) | Auto Cluster | Estimates and compares clustering models, which identify groups of records that have similar characteristics. |
| ![CHAID](https://www.ibm.com/docs/en/SS3RA7_18.3.0/modeler_mainhelp_client_ddita/clementine/images/chaidnodeicon.jpg) | CHAID | The CHAID node generates decision trees using chi-square statistics to identify optimal splits. Target field can be categorical or numeric field. |
