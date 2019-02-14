+++
title = "Import Fields to a System"
Weight = 4
+++


You can upload field metadata for a System in a zipped JSON file using
the upload option on the System detail page.

Fields JSON Import File Format
------------------------------

Use the following schema information to format the JSON file that is
used to load field metadata for a System.

**Format:**

{

\"version\": \"2018-02-07\",

\"fields\":\[

{

\"name\": \"\...\",

\"location\": {\...},

\"type\": {..}

}

\]

}

 

You can request a sample JSON file by [submitting a request to
support](Contact%20Support.htm).

 

Properties in "root":

+-----------------+-----------------+-----------------+-----------------+
| Property        | Description     | Presence        | Example 1       |
+-----------------+-----------------+-----------------+-----------------+
| version         | Schema version  | Must be present | "2018-02-07"    |
|                 | as string       |                 |                 |
|                 |                 | **NOTE**: This  |                 |
|                 |                 | is a hard coded |                 |
|                 |                 | value that MUST |                 |
|                 |                 | be set to this  |                 |
|                 |                 | exact string    |                 |
|                 |                 | for this        |                 |
|                 |                 | version of the  |                 |
|                 |                 | API             |                 |
+-----------------+-----------------+-----------------+-----------------+
| fields          | Array of JSON   | Must be present |                 |
|                 | object          |                 |                 |
|                 |                 | **NOTE**: See   |                 |
|                 |                 | properties      |                 |
|                 |                 | below           |                 |
+-----------------+-----------------+-----------------+-----------------+

Properties in "fields" array:

+-----------------+-----------------+-----------------+-----------------+
| Property        | Description     | Presence        | Example 1       |
+-----------------+-----------------+-----------------+-----------------+
| name            | The friendly    | Must be present | Customer Name   |
|                 | name of the     |                 |                 |
|                 | field.          | **NOTE**: This  |                 |
|                 |                 | is the Friendly |                 |
|                 |                 | Name that       |                 |
|                 |                 | displays in the |                 |
|                 |                 | UI on the Data  |                 |
|                 |                 | Set page.       |                 |
+-----------------+-----------------+-----------------+-----------------+
| location        | The full        | Must be present | JSON { ... }    |
|                 | system-specific |                 |                 |
|                 | path, location  |                 | (see "location" |
|                 | information for |                 | table below)    |
|                 | a field.  This  |                 |                 |
|                 | is a JSON bag.  |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| type            | The full        | Must be present | JSON { ... }    |
|                 | system-specific |                 |                 |
|                 | data type       |                 | (see "type"     |
|                 | information for |                 | table below)    |
|                 | a field.  This  |                 |                 |
|                 | is a JSON bag.  |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| tags            | An array of     | May be present. | \[ "KUNNR",     |
|                 | terms that      |                 | "Customer Name" |
|                 | should be       |                 |  \]             |
|                 | indexed along   |                 |                 |
|                 | with this field |                 |                 |
|                 | for search.     |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| usage           | Contains        | May be present. |                 |
|                 | system-specific | Default is the  |                 |
|                 | usage or        | empty string.   |                 |
|                 | context data,   |                 |                 |
|                 | if available.   |                 |                 |
|                 |                 |                 |                 |
|                 | For example,    |                 |                 |
|                 | the content of  |                 |                 |
|                 | a database's    |                 |                 |
|                 | data            |                 |                 |
|                 | dictionary, a   |                 |                 |
|                 | MSSQL column    |                 |                 |
|                 | comment, etc.   |                 |                 |
+-----------------+-----------------+-----------------+-----------------+

Properties in "location":

+-----------------+-----------------+-----------------+-----------------+
| Property        | Description     | Presence        | Example 1       |
+-----------------+-----------------+-----------------+-----------------+
| technicalName   | A short name of | Must be present | KUNNR           |
|                 | the field name  |                 |                 |
|                 |                 | **NOTE**: This  |                 |
|                 |                 | is the          |                 |
|                 |                 | Technical Name  |                 |
|                 |                 | that displays   |                 |
|                 |                 | in the UI on    |                 |
|                 |                 | the Data Set    |                 |
|                 |                 | page.           |                 |
+-----------------+-----------------+-----------------+-----------------+
| path            | The full        | Must be present | dbo.KNA1.KUNNR  |
|                 | system-specific |                 |                 |
|                 | path, location  | **NOTE**: This  |                 |
|                 | information for | is the Location |                 |
|                 | a field         | (under the      |                 |
|                 |                 | system name)    |                 |
|                 |                 | that displays   |                 |
|                 |                 | in the UI on    |                 |
|                 |                 | the Data Set    |                 |
|                 |                 | page.           |                 |
+-----------------+-----------------+-----------------+-----------------+
| \<custom        | Any other       | May be present. |                 |
| properties\>    | custom property |                 |                 |
|                 | that            |                 |                 |
|                 | integrators may |                 |                 |
|                 | choose to       |                 |                 |
|                 | upload; any     |                 |                 |
|                 | other           |                 |                 |
|                 | system-specific |                 |                 |
|                 | properties.     |                 |                 |
+-----------------+-----------------+-----------------+-----------------+

Properties in "type":

+-----------------+-----------------+-----------------+-----------------+
| Property        | Description     | Presence        | Example 1       |
+-----------------+-----------------+-----------------+-----------------+
| dataTypeIntent  | A simplified    | May be present  | text            |
|                 | data type from  |                 |                 |
|                 | this list:      |                 |                 |
|                 | text, number,   |                 |                 |
|                 | Boolean, date,  |                 |                 |
|                 | money,          |                 |                 |
|                 | location,       |                 |                 |
|                 | binary,         |                 |                 |
|                 | identifier      |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| baseDataType    | The field data  | Must be present | nvarchar        |
|                 | type            |                 |                 |
|                 |                 | **NOTE**: This  |                 |
|                 |                 | is displayed in |                 |
|                 |                 | the UI on the   |                 |
|                 |                 | Add Fields tab  |                 |
|                 |                 | on the Data Set |                 |
|                 |                 | page.           |                 |
+-----------------+-----------------+-----------------+-----------------+
| range           | Range           | Must be present | JSON { ... }    |
|                 | constraints     | if applicable.  | (see "range"    |
|                 |                 |                 | table below)    |
+-----------------+-----------------+-----------------+-----------------+
| precision       | A precision for | Must be present |                 |
|                 | numeric data    | when            |                 |
|                 | types           | baseDataType is |                 |
|                 |                 | numeric;        |                 |
|                 |                 | otherwise, must |                 |
|                 |                 | not be present. |                 |
|                 |                 |                 |                 |
|                 |                 | **NOTE:** This  |                 |
|                 |                 | is displayed in |                 |
|                 |                 | the UI on the   |                 |
|                 |                 | Add Fields tab  |                 |
|                 |                 | on the Data Set |                 |
|                 |                 | detail page on  |                 |
|                 |                 | the Data Set -  |                 |
|                 |                 | Fields and Data |                 |
|                 |                 | Set - Add       |                 |
|                 |                 | Fields tabs.    |                 |
+-----------------+-----------------+-----------------+-----------------+
| length          | A length value  | Must be present | 36              |
|                 | for characters  | when            |                 |
|                 | types           | baseDataType is |                 |
|                 |                 | an array of     |                 |
|                 |                 | characters or   |                 |
|                 |                 | bytes;          |                 |
|                 |                 | otherwise, must |                 |
|                 |                 | not be present. |                 |
|                 |                 |                 |                 |
|                 |                 | **NOTE**: This  |                 |
|                 |                 | is displayed in |                 |
|                 |                 | the UI on the   |                 |
|                 |                 | Add Fields tab  |                 |
|                 |                 | on the Data Set |                 |
|                 |                 | page.           |                 |
+-----------------+-----------------+-----------------+-----------------+
| encoding        | Additional      | Must be present | "Utf-8",        |
|                 | details about   | if applicable   | "latin-1",      |
|                 | the encoding of |                 | IEEE-754        |
|                 | the field       | **NOTE**: This  | floating point, |
|                 |                 | can be a        | binary data is  |
|                 |                 | string.         | in big-endian   |
|                 |                 |                 | or              |
|                 |                 |                 | little-endian,  |
|                 |                 |                 | bools are       |
|                 |                 |                 | 0xFFFFF or      |
|                 |                 |                 | 0x00001 etc.    |
+-----------------+-----------------+-----------------+-----------------+
| identity        | Indicates       | May be present. | true            |
|                 | whether this    |                 |                 |
|                 | field is an     | **NOTE**:       |                 |
|                 | identifier in   | Default to      |                 |
|                 | the underlying  | false.          |                 |
|                 | model (e.g., a  |                 |                 |
|                 | primary key in  |                 |                 |
|                 | a relational db |                 |                 |
|                 | context, or a   |                 |                 |
|                 | resource        |                 |                 |
|                 |  identifier in  |                 |                 |
|                 | a REST API      |                 |                 |
|                 | context)        |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| optional        | A determination | May be present. | true            |
|                 | if the field    |                 |                 |
|                 | can be nullable | **NOTE**:       |                 |
|                 |                 | Default to      |                 |
|                 |                 | false.          |                 |
+-----------------+-----------------+-----------------+-----------------+
| \<custom        | Any other       | May be present. |                 |
| properties\>    | custom property |                 |                 |
|                 | that            |                 |                 |
|                 | integrators may |                 |                 |
|                 | choose to       |                 |                 |
|                 | upload; any     |                 |                 |
|                 | other           |                 |                 |
|                 | system-specific |                 |                 |
|                 | properties.     |                 |                 |
+-----------------+-----------------+-----------------+-----------------+

Proposed properties in "range":

+-----------------+-----------------+-----------------+-----------------+
| Property        | Description     | Presence        | Example 1       |
+-----------------+-----------------+-----------------+-----------------+
| minValue        | A minimum value | Must be present | -7.25           |
|                 | for numeric     | if applicable.  |                 |
|                 | data            | Must not be     |                 |
|                 |                 | present if not  |                 |
|                 |                 | applicable.     |                 |
+-----------------+-----------------+-----------------+-----------------+
| maxValue        | A maximum value | Must be present | 13              |
|                 | for numeric     | if applicable.  |                 |
|                 | data            | Must not be     |                 |
|                 |                 | present if not  |                 |
|                 |                 | applicable.     |                 |
+-----------------+-----------------+-----------------+-----------------+
| rangeValues     | A finite list   | May be present  | \[ "Sunday",    |
|                 | of values drawn | if applicable.  | "Monday",       |
|                 | from the        | (If the data    | "Tuesday",      |
|                 | default range   | set would be    | "Wednesday",    |
|                 | of the          | really long, it | "Thursday",     |
|                 | baseDataType.   | might not be    | "Friday",       |
|                 |                 | possible to     | "Saturday" \]   |
|                 |                 | include.)       |                 |
|                 |                 |                 |                 |
|                 |                 |                 |                 |
|                 |                 |                 |                 |
|                 |                 | Must not be     |                 |
|                 |                 | present if not  |                 |
|                 |                 | applicable.     |                 |
+-----------------+-----------------+-----------------+-----------------+
| rangeDataType   | The name of the | May be present  | "DaysOfTheWeek" |
|                 | range           | if applicable.  | ,               |
|                 | constraint      |                 | "dbo.DaysOfTheW |
|                 | (e.g. a FK      |                 | eek"            |
|                 | table name)     |                 |                 |
|                 |                 | If applicable   |                 |
|                 |                 | and rangeValues |                 |
|                 |                 | is not present, |                 |
|                 |                 | then this       |                 |
|                 |                 | property must   |                 |
|                 |                 | be present.     |                 |
+-----------------+-----------------+-----------------+-----------------+

**The upload file must be zipped (compressed)**. The zipped file can
contain multiple JSON files to organize the files.

For example:

SAPFileUpload.zip can contain:

-   SAP (directory - **optional**)
    -   HRFields.json
    -   FinanceFields.json
    -   LegalFields.json

Or it can contain one file

SAPFileUpload.zip

-   SAP (directory - **optional**)
    -   Fields.json

To upload field metadata for a System:

1.  [Add a System](Set%20Up%20a%20System.htm).

    OR

    [Search for a System and open the detail
    page](Enhanced%20Search.htm).

2.  Click the drop-down menu for the System.

    ![](Resources/Images/SystemsDropDown.png)

3.  Select **Upload Metadata**.
4.  Drag and Drop the JSON file onto the upload modal.

    OR

    Browse for the file.

5.  Click **Upload**.

**IMPORTANT**: You will receive a message in the
[Notifications](Notifications.htm) panel once the file has been
processed to indicate success or to inform you of issues with the
import.

After you receive a message that the upload succeeded, you can use your
browser refresh option to update the count in the
[Fields](Set%20Up%20a%20System.htm#Fields) panel to verify the upload.
Next, the fields can be used to set up Data Sets. Refer to [Set Up a
Data Set](Set%20Up%20a%20Data%20Set.htm).

[]{#RemoveFields}Remove Fields from a System
--------------------------------------------

You can remove specific fields (or a group of fields) from a System if
you re-import to a System with the import file in which fields that
**had been previously imported** to that System are not included. The
fields that you choose to exclude from the newly imported file are
marked as Removed from System in any [Data
Set](Set%20Up%20a%20Data%20Set.htm) where the fields had been added.

If a field that was removed from a System is subsequently re-included in
the import file and imported to the System again it is made "active"
again in any data set in which it has been used.
