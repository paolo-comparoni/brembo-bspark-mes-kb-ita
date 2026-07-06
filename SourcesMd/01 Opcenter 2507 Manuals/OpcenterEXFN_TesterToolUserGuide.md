---
title: "OpcenterEXFN_TesterToolUserGuide"
source_file: "SourcesMd/01 Opcenter 2507 Manuals/OpcenterEXFN_TesterToolUserGuide.md"
project: "Brembo B-Spark - Standard Platform Documentation"
platform: "Siemens Opcenter Execution Foundation 2401"
scope: "Core_Standard_Manual"
plants: [SHARED]
---

# Opcenter Execution Foundation 2401 - Tester Tool User Guide

> Documento sorgente: `E:\BremboDocs\01 Opcenter 2507 Manuals\OpcenterEXFN_TesterToolUserGuide.pdf`
> Tipo: PDF - Pagine originali: 55

## Guidelines

This manual contains notes of varying importance that should be read with care:

- **Important**: Highlights key information on handling the product, the product itself, or a particular part of the documentation.
- **Note**: Provides supplementary information regarding handling the product, the product itself, or a specific part of the documentation.

### Trademarks

All names identified by ® are registered trademarks of Siemens AG. The remaining trademarks in this publication may be trademarks whose use by third parties for their own purposes could violate the rights of the owner.

### Disclaimer of Liability

We have reviewed the contents of this publication to ensure consistency with the hardware and software described. Since variance cannot be precluded entirely, we cannot guarantee full consistency. However, the information in this publication is reviewed regularly and any necessary corrections are included in subsequent editions.

### Cybersecurity Information

Siemens provides products and solutions with industrial cybersecurity functions that support the secure operation of plants, systems, machines and networks. In order to protect plants, systems, machines and networks against cyber threats, it is necessary to implement and continuously maintain a holistic, state-of-the-art industrial cybersecurity concept. Siemens products and solutions constitute one element of such a concept. Customers are responsible for preventing unauthorized access to their plants, systems, machines and networks. Such systems, machines and components should only be connected to an enterprise network or the internet if and to the extent such a connection is necessary and only when appropriate security measures (for example, firewalls and/or network segmentation) are in place. For additional information on industrial cybersecurity measures that may be implemented, please visit https://www.siemens.com/cybersecurity-industry.

Siemens products and solutions undergo continuous development to make them more secure. Siemens strongly recommends that product updates are applied as soon as they are available and that the latest product versions are used. Use of product versions that are no longer supported, and failure to apply the latest updates may increase customer’s exposure to cyber threats. To stay informed about product updates, subscribe to the Siemens Industrial Cybersecurity RSS feed under https://www.siemens.com/cert.

## Publication Information

- **Product**: Opcenter Execution Foundation
- **Version**: 2401.0001
- **Document**: Tester Tool User Guide
- **Publication date**: 04/2024
- **Revision**: PL20240221511718776
- **Category**: Development, Support
- **Summary**: Provides information on how to create automated tests by means of the Opcenter Execution Foundation Tester Tool.
- **Audience**: System Integrator, Support Engineer, Project Engineer, Commissioning Engineer, Developer
- **State**: Published
- **Author**: Siemens AG
- **Language**: en-US
- **Company**: Siemens AG, Digital Industries
- **Address**: Postfach 48 48, 90026 Nürnberg, Germany
- **Generated on**: 20240424_173856
- **Notice**: Technical data subject to change

## 1 Introduction to the Opcenter Execution Foundation Tester Tool

Opcenter Execution Foundation supports you in improving and speeding up test and validation phases for your
project.
For this purpose, the product provides a dedicated tool, named Opcenter Execution Foundation Tester, to create
automated tests without having specific skills on software coding. These tests can then be run in your test
environment.

Opcenter Execution Foundation Tester Tool Capabilities
The main capabilities of the Opcenter Execution Foundation Tester tool are:
- Command execution and data query: the tool is able to call a logic sequence of commands and data query,
testing the business logic behind the UI Application.
- Automated initialization of master data: the master data are automatically initialized, adopting the proper
commands of the application.
- Authoring and execution of acceptance tests: each business use case has a dedicated acceptance test, which
can be created and executed in the tool.
- Execution of non regression tests after the software upgrade: the whole list of acceptance tests can be executed
any time a software upgrade is performed on different scenarios, by setting different input parameters.
- Simulation of third-party interaction: MES solutions are connected with Shopfloor, ERP systems and many other
third-party systems. The tool simulates the messages from and to these systems for the completeness of the
implementation and execution of the acceptance tests.
- User-friendly and no code tool: testing activities can be performed by Business Industry process experts, not
skilled on software coding.

Benefits of the Opcenter Execution Foundation Tester Tool
Many are the benefits in adopting the Opcenter Execution Foundation Tester tool.
- Improving efficiency in automatic test management
- Reducing design and implementation errors
- Optimizing of test authoring time
- Improving test time-execution
- Improving software quality.
In addition to them, from the customer perspective the tool also provides the following benefits:
- Adoption of a template for several plants: a single test template can be designed and then tailored on the
peculiarities of each plant.
- Test Definitions for new custom Commands: all Custom implementations and extensions can be tested
improving the standard test.
- Dedicated Non-Regression Test Suite for each plant: any scenario upgrade can be validated executing nonregression tests.
- Rapid check on Test Output data.
- Automatic Initialization of Master Data.
- Simulation of third-party systems.

## 2 How to Configure a Test Suite

### 2.1 How to Create Test Suites

In the Opcenter Execution Foundation Tester tool three entities are defined:
- at the top of the entity hierarchy, a Test Suite that consists of a collection of tests,
- each test is represented by a Test Definition and it is made up of Test Steps,
- each Test Steps can be a Command call, an Entity query, a Reading Function call, or a custom action.

Workflow
1. How to Create Test Suites
2. How to Configure Test Definitions
3. How to Configure Test Steps.

What to do next
Once Test Suite is configured, it can be executed. See How to Execute a Test Suite.

The first step to create a test with the Opcenter Execution Foundation Tester tool is the Test Suite creation.
Once created, the Test Suite can later be opened as described in Opening the Test Suite.

Prerequisites
You must have write permissions on the local folder in which to save the Test Suite.

Procedure
1. Copy the OpcenterEXFNTester folder from the product ISO image to a local path.
2. Start the Opcenter Execution Foundation Tester tool, by double-clicking the OpcenterEXFNTester.exe utility.
The tool opens with an empty Test Suite.
3. Set the Connection Parameters:
Parameters

Description

Host

Either of the following:
- the Opcenter Execution Foundation runtime machine, in
which Opcenter Execution Foundation is configured (domain
included). You can use localhost if you are configuring the
Test Suite on the same machine in which the Test will be
executed.
- the ip address.

Use Https

To be set only if the https connection is required. The default value is
http.

User Name

The local Opcenter Execution Foundation user name to connect to the
Opcenter Execution Foundation machine. The user must be a test user
(not a production user) and must have administrative rights in order to
execute commands and perform queries.

Parameters

Description

Password

The local Opcenter Execution Foundation password to connect to the
Opcenter Execution Foundation machine. The password is encrypted by
the tool.

4. If you want to reset statistics before to save the Suite, set the Reset Statistics before to Save the
Suite checkbox.
5. Click Initialize. The metadata is retrieved from the runtime system and the list of the installed applications is
displayed in the Metadata Browser area.
6. Set the Test settings:
Parameters

Description

Plant

The Id of the Plant in which the Test will be executed. If this field is
left empty, the default plant (the first created plant) will be
automatically set.

Suite Tag

A value that can be used in the command call parameters. It can
contain fixed values, dynamic values or a combination of both.
Fixed values can be manually typed. To insert dynamic values, open
the context menu by right-clicking the Suite Tag field and selecting
one of the following:
- Unique Identifiers
- DateTime Values
- Random Values
Example, SuitTag_#GUID#. Here, SuitTag_ is the fixed value and
#GUID# is the dynamic value retrieved by selecting Unique
Identifiers > Global Unique ID.

Iterations

The number of executions of each Test in the Test Suite. It is useful
for performance Tests.

Step Delay

Delay in milliseconds in executing each Step, to be applied before
each execution starts. It is useful during the Test preparation.

Break on Error

If set, the Test execution is stopped when a Step fails.

Log Verbose

If set, all payloads and results of each Step will be included in the
log.

Save Execution Log

If set, the log is automatically saved as text file at the end of the
execution. The text file contains the list of the executed Steps, the
related result (passed or failed) and the execution time.

Parameters

Description

Save Raw Statistics

If set, when the execution ends, statistics of the execution time of
each Test Step, Test Definition and Test Suite are saved in a
dedicated CSV files inside the Test Suite.

7. In the Metadata Browser area, select the required metadata from the available ones in the list:
Metadata

Description

Application Name

The list of the installed applications in the Solution (for example,
Material App).
When selecting an application, the related Commands, Entities and
Reading Functions are displayed in the dedicated area.

Commands

The list of all Commands in the selected application (for example,
CreateMaterial Command.
When selecting a Command, the related parameters are displayed in
the dedicated area. Mandatory parameters are shown with a
different color.

Entities

The list of all Entities in the selected application.
When selecting a Entity, the related parameters are displayed in the
dedicated area. Mandatory parameters are shown with a different
color.

Reading Functions

The list of all Reading Functions in the selected application.
When selecting a Reading Function, the related parameters are
displayed in the dedicated area. Mandatory parameters are shown
with a different color.

8. In the Variables area, click the plus icon to add a variable, defining it with the related name and value (for
example, Equipment name and Machine1 value). Variables will be used inside the Test Step configuration and
they can be useful to configure the value data used in the call parameters. If you refer to the variable value in
many Test Steps, you can change their value by modifying the single variable. Variables are similar to the Suite
Tag, but their values are always fixed.
9. Click Save Suite to save the Test Suite. Otherwise, click Save Suite As and select one of the following formats:
- .opexts, to save the Test Suite in json format,
- .opextx to save the Test Suite in compact json format,
- .opexty to save the Test Suite in a encrypted format. In this case, a password is required to save the Test
Suite.

### Opening the Test Suite

Opening the Test Suite
To open a previously created Test Suite:
1. Click the Open Suite button.
2. Browse one of the following files, depending on how you chose to save the Test Suite.
- .opexts, if you have saved the Test Suite in json format,
- .opextx, if you have saved the Test Suite in compact json format,
- .opexty, if you have saved the Test Suite in a encrypted format. In this case, a password is required to
open the Test Suite.

> Note: If the password is forgotten, it will no longer be possible to recover it and, consequently, to open the related Test Suite.

### 2.2 How to Configure Test Definitions

Once the Test Suite is created, you can create the Test Definitions in one of the following ways:
- from scratch: in this case, the Test Definition must be then populated by creating Test Steps,
- from metadata: in this case, the Test Definition will be created starting from the required Commands and
Entities, with a Step for each Command/Entity,
- from a CSV file: in this case, the Test Definition will be created starting from a CSV file, and each Step in the Test
Definition will be executed for each row in the CSV data,
- from Excel file: in this case, the Test Definition will be created starting from an Excel file, and each Step in the
Test Definition will be executed for each row of the related spreadsheet of the Excel file
Once created, you can perform many operations on Tests, for example they can be copied and deleted. See
Available Operations on Tests Definitions.

### 2.2.1 Creating Test Definitions from Scratch

The following procedure describes how to create a Test Definition from scratch. Then, it must be then populated
with the required Test Steps.

Procedure
1. In the created Test Suite, select the Test Definitions tab.
2. Click Add.
3. Set the following parameters:

Parameter

Description

Name

The name of the test. A default name is automatically created when click
the Add button, and you can modify it by inserting the desired one. It
should be unique in the Suite.

Category

Optional. The category of the test (for example Acceptance).

Description

Optional. The description describing the test.

CSV Data Path

To be set only if you want to create the Test Definition from a CSV file. This
field indicates the path in which the CSV file is located. See Creating Test
Definitions from a CSV file.

Test Tag

It can be useful when steps in the Test refer to it in their parameters. For
example, if you use #UNIQUE_STR_ID#, every time the Test is executed, a
new string value is generated, and each step referring the Test Tag will use
the new value. In this way, the Test can be executed many times, avoiding
ID collisions.

Iterations

To execute many times the Test during the same Test Suite execution.
This field is disabled if you use a CSV file to create the Test Definition.

End On Error

To stop the Test Definition in case of errors.

Is Enabled

This option is enabled by default. You can remove this setting to disable a
Test. It can be useful during the Test Suite preparation, or to define a Test
that must not be executed in the normal Suite Run but contains some
steps to be executed in some situations or during data initialization.
Once disabled, tests are displayed in grey.

### 2.2.2 Creating Test Definitions from Metadata

The following procedure describes how to create a Test Definition starting from metadata. In particular, it can be
created:
- from Commands
- from Entities.
The Test Definition will be automatically populated with a Step for each Command/Entity.

Creating a Test Definition from Commands
1. In the Test Suite tab, in the Metadata Browser area > Commands tab, right-click one or more Commands in
the list.
2. Click Generate Tests for selected Commands. The system creates a Test, available in the Test Definitions tab,
with a Step for each selected Command.

Creating a Test Definition from Entities
1. In the Test Suite tab, in the Metadata Browser area > Entities tab, right-click one or more Entities in the list.
2. Click Generate Tests for selected Entities. For each entity, the system creates a Test, available in the Test
Definitions tab, with Commands having a name containing the entity name (usually CRUD commands) and
entity read Step. The steps will be sorted so that you can run the tests with a few changes.

### 2.2.3 Creating Test Definitions from a CSV file

The following procedure describes how to create a Test Definition from a CSV file. Each steps in the Test Definition
will be executed for each row in the CSV data.

This approach can be useful to initialize a test scenario.

Procedure
Create a Test Definition from scratch, setting the CSV/Excel Data Path parameter, as follows:
1. Browse the CSV file by clicking the dedicated button next to the field.
2. Edit the CSV file by clicking the dedicated button next to the field. Using the context menu, you can insert tags to
get CSV field value as data for command calls parameters. In the fields, you can also insert Json objects.
3. In the CSV Editor, define the row structure as you need.
4. Click OK.

### 2.2.4 Creating Test Definitions from an Excel file

The following procedure describes how to create a Test Definition from an excel file (xslx). Each step in the Test
Definition will be executed for each row of the related spreadsheet in the CSV data.
This approach can be useful to initialize a test scenario.

Procedure
> Note: In order to use the xlsx file as input for a test definition, the structure of the spreadsheet and the parameters can be created and modified only from Excel. Inside the xlsx editor it is only possible to display the data and select the desired spreadsheet.

To create a Test Definition from scratch it is possible to use the CSV/Excel Data Path parameter, as follows:
1. Browse for the xslx file by clicking the dedicated button next to the field.
2. From the file system windows, select Excel Files (*.xlsx) as type.

3. Open the xlsx editor by clicking the dedicated button next to the field. Using the Selected Spreadsheet
dropdown you can select the desired spreadsheet defined in the excel file.

4. After selecting the spreadsheet, the CSV/Excel Data Pathis updated with the excel file and related spreadsheet.

Inside the test step, the parameters of the excel spreadsheet can be retrieved through the Take Test CSV Data
option:

> Note: If you change the content of the Excel file after the test definition has been linked to it, you can:
>
> 1) Refresh the test definition with the related button next to the field of CSV/Excel Data Path. This option will keep the outcome of all the previous executed test definitions.
> 2) Click on Reset, open the CSV/Excel editor and click OK to update the Test Definition with the Excel spreadsheet content. This option will also reset the outcome of all the previous executed test definitions.

### 2.2.5 Modifying Test Definitions from CSV file to an Excel file

The following procedure describes how to update an existing Test Definition created from a CSV file to a Test
Definition created from an Excel file (xslx).
This approach can be useful to store all the data from different csv files to a unique xlsx file.

Procedure
1. Open Excel and create a new blank workbook.
2. .From the Data tab click on From Text/CSV button, select the existing csv file from the related directory and
click Import.

3. The content of the csv is displayed: select the Do not detect data types and click on Transform Data.

4. Inside the Power Query Editor, select the Use First Row as Headers option.

Inside the Power Query Editor, it is possible to change the type of each column, according to the test steps

configuration.

5. Click on Close & Load button to load the spreadsheet in the excel file.
6. Repeat the same operation for each csv file that needs to be imported in the excel file.
7. Save the excel file in the "(*.xlsx)" type in the desired location.
8. Inside the Test Definition, select the related spreadsheet for the input following the procedure of Creating Test
Definitions from an Excel file.

### 2.3 How to Configure Test Steps

Each Test Definition can contain many Test Steps, which can be configured as Command calls, Entity queries,
Reading Function calls or Custom Actions.
After creating a Test Definition from scratch, you can proceed configuring the required Test Steps.
Once created, you can perform many operations on Test Steps, for example they can be copied and deleted.
See Available Operations on Test Steps.

Workflow
1. Create Test Steps.
2. Configure Test Steps as one of the following:
- Command Calls
- Entity Queries
- Custom Actions.

Available Operations on Steps
Operatio
n

Description

Copy

To create a copy of the selected Step with the same properties. You can insert a new name, but you
cannot change the Type.

Delete

To delete the selected Step. Before deleting it, the system asks you a confirmation.

### 2.3.1 Creating Test Steps

After creating a Test Definition from scratch, you can create the required Test Steps.

Procedure
1. In the Test Definitions tab, select a Test Definition and click the plus icon in the right bar.
2. In the New Test Step dialog box, set the following parameters and click OK:
Parameter

Description

Step ID

The name of the Step. It must be unique in the Test context and cannot
contain spaces or dots.

Step Type

The type of the Step. It cannot be changed after the step creation.
Possible values are:
- Execute a Command Call
- Read data related to an Entity
- Get data by Reading Functions
- Execute a Custom Action.

### 2.3.2 Configuring Test Steps as Command Calls

Once a Test Step is created, you can configure it as a Command call, by setting the required Command parameters.

Procedure
1. In the Test Definitions tab, select a Test Step.
2. In the Properties tab, set the following parameters:
Parameters

Description

Step ID

The identifier of the Step (for example, AddMaterial). It is
automatically set by selecting the Step.

Application

The Application related to the selected Step (for example,
MaterialApp).

Command

The Command related to the selected Step (for example,
CreateMaterial command).

3. Set the execution options:

Option

Description

Is Enabled

If set, it enables the Step. Disabled Step are displayed in grey.

Option

Description

Expect Success

It change the expected result. If set, a success is expected,
otherwise a failure is expected.

Skip on Error

It avoids to break the execution when the Step fails, if the Break on
Error parameter is set in the Test Suite.

4. In the Call Parameters grid, the system displays the list of the call parameters, depending on the Application
and Command previously set. Mandatory fields are shown in bold. The call parameter values are automatically
set by the tool but you can change them, for example doing one of the following:
- Retrieve the value from a CSV file, by right-clicking the call parameter value in the grid, selecting Take
Test CSV Data and then selecting the required field name.
- Insert a dynamic tag, by right-clicking a call parameter value in the grid and selecting a tag. This tag will
be replaced during the execution.
- Retrieve the output value from another Step, by right-clicking the call parameter value in the grid and
selecting Get Value from Step Result. Then, select the parameter from which to get data.
- Retrieve the parameter value from another Step, by right-clicking the call parameter value in the grid and
selecting Get Value from Step Parameter. Then, select the parameter from which to get data.
- Set the Tags manually.
You can set the value by using variables. For example, if you have defined in the Test Suite a variable with
Equipment name and Machine1 value, the value to be inserted here is #SUITE_VAR.Equipment#.

> Note on Autonumbering Pattern usage: When using the Autonumbering Pattern, the system automatically insert the Tag #AUTO_Nid#. Then, during the execution, this tag will be replaced with «\u0091Nid». If you want to use a different pattern, type the Id instead of NId.
5. (Optional) In the Additional Arguments grid, specify any additional arguments you want to add to the
Command payload. The Is Collection check box is used to represent list of values. For more information on
the Command extensibility pattern, refer to the Opcenter Execution Foundation Extensibility Guide.

6. If you want to set complex parameters, do one of the following:
- Get the value from another Step with a Tag.
- Write the value in Json format.
- Click Edit... and set the parameter values in the Edit Parameter editor. The editor is available for
complex type, collections and text with unlimited length. You can also open a sub-instance of the editor.
In case of collection parameters, you can open the Collection Editor and set the parameter values.

6. Save the operation by clicking the apply change icon in the right bar.
7. In the Payload tab, take a look at the preview of the payload, but bear in mind that it can change during the
execution, due to dynamic tags. You can select the text box and paste a payload (Ctrl-V). For more
information, see How to Review the Test Suite Execution.

If you have added additional arguments, the payload is extended with the 'additional' section:

The default timeout for the command execution is 0 (that means 30 seconds): it can be changed up to 3600
seconds
The command can be executed with a different user form the one set in the connection parameters typing the
new User and Password

### 2.3.3 Configuring Test Steps as Entity Queries

Once a Test Step is created, you can configure it as an entity query.

Procedure
1. In the Test Definitions tab, select a Test Step.
2. In the Properties tab, set the following parameters:

Parameters

Description

Step ID

The identifier of the Step (for example, Material). It is
automatically set by selecting the Step.

Application

The Application related to the selected Step (for example,
MaterialApp).

Parameters

Description

Entity

The Command related to the selected Step (for example, Material
entity).

3. Set the execution options:
Option

Description

Is Enabled

If set, it enables the Step. Disabled Step are displayed in grey.

Expect Success

It change the expected result. If set, a success is expected,
otherwise a failure is expected.

Skip on Error

It avoids to break the execution when the Step fails, if the Break on
Error parameter is set in the Test Suite.

4. In the Filter Properties grid, the system displays the list of the filter properties, depending on the Application
and Entity previously set. Mandatory fields are shown in bold. The filter property values are automatically set by
the tool but you can change them, as well as you can set values by using variables, as you already known for the
call parameters in Configuring Test Steps as Command Calls.

> Note: The default compare operator is =, but you can also use the following supported operators: <, >, <=, >=, !=, [[ (the last one means “contains”).

5. Set the following parameters:
Option

Description

Expand

Select the sub-entity to be expanded.

Extra OData Parameters

To add extra parameters, paying attention to format them correctly.

Max Rows

The maximum number of returned rows to avoid performance issues.

Expected

The expected number of entities retrieved by query.

Retries

The retry count to wait for rows. The retry count can be useful to wait
for some procedures that are executed in asynchronous mode. For
example, if you have a step that starts a Work Order, you can want to
wait until it is completed. So, you can add a Step that queries the
Order, sets the status attribute to «Executed», set the Expected = 1 and
Retries = 60 and delay = 1 to perform again the query every second

Delay

Delay (seconds) after which the retries will be performed

6. Save the operation by clicking the apply change icon in the right bar.
7. In the Query tab, take a look at the Odata queries that will be executed. For more information, see How to
Review the Test Suite Execution.

8. In the Data tab, take a look at the result of the queries in tabular form. For more information, see How to Review
the Test Suite Execution.

### 2.3.4 Configuring Test Steps as Custom Actions

Once a Test Step is created, you can configure it as a Custom Action.
Custom Actions are special functions that allow executing activities not provided by Opcenter Execution
Foundation.
These actions can be useful to:
- Initialize the test scenario
- Reset the database
- Copy the output files after the test execution
- Post a command to an http endpoint (for example to Opcenter Connect MOM).

Procedure
1. In the Test Definitions tab, select a Test Definition and click the plus icon in the right bar.
2. In the New Test Step dialog box, set the following parameters:

### 2.3.4.1 Using ExecuteSQL Action

The ExecuteSQL action allows executing any kind of SQL script. In the example below, a database will be restored
from a previous backup.

Procedure
1. In the Properties tab, in the Action field select ExecuteSQL.
2. Set the following call parameters:
Parameter

Description

DataSource

The SQL Server instance name (i.e. <SQL Server machine
name>\<SQL Server instance>).

InitialCatalog

The name that will be assigned to the database.

IntegratedSecurity

Option to login to the database, instead of using UserName and
Password.

UserName

The user name to log in to the database. It is not used if the
IntegratedSecurity option is enabled.

Parameter

Description

Password

The password to log in to the database. It is not used if the
IntegratedSecurity option is enabled.

SQLText

The SQL text to be executed. Use the Text Editor to write it.

SQLTextFile

The path of an external file containing the SQL text to be
executed.
If both SQLText and SQLTextFile are specified, SQLText will be
used only if the file is not available.

TimeOut

The default value is 30 seconds.

### 2.3.4.2 Using HttpPost Action

The HttpPost action allows posting any payload to an Http endpoint. In the example below, an Order will be sent to
an external system.

Procedure
1. In the Properties tab, in the Action field select HttpPost.
2. Set the following call parameters:

Parameter

Description

Protocol

Connection protocol with the endpoint to reach. Possible values are:
- http
- https

Host

The Endpoint concatenated to the Url.

Port

The Port on which the connection is enabled.

UserName

The user name for the authentication. It is not used if the Bearer
option is enabled.

Password

The password for the authentication. It is not used if the Bearer
option is enabled.

Bearer

Option for the authentication.

Url

The URL to which the post will be executed.

Payload

The Payload to be posted. Use the Text Editor to write it.

PayloadFile

The path of an external file containing the Payload to be posted.
If both Payload and PayloadFile are specified, Payload will be used
only if the file is not available.

### 2.3.4.3 Using StartProcess Action

The StartProcess action allows executing any Windows process. In the example below, it allows executing a Batch
file.

Procedure
1. In the Properties tab, in the Action field select StartProcess.
2. Set the following call parameters:

Parameter

Description

FilePath

The Path of the process to be executed.

Arguments

The argument passed to the process. They are handled as a string
collection. Use the Collection Editor to specify the required arguments.

WaitForExit

If set to True, you wait for the process to be completed.

GetOutput

If set to True, you get the process output as Result.

Parameter

Description

TimeOut

The default value is 30 seconds.

3. In the Result tab, take a look at the output of the executed Process.

> Note: If in the property FilePath the #SUITE_FOLDER# parameter is used, it must be edited manually as #SUITE_FOLDER_DS# to take the proper path as input.

### 2.3.4.4 Using Wait Action

The Wait action allows setting a wait time, using a combination of minutes, seconds and milliseconds.

Procedure
1. In the Properties tab, in the Action field select Wait.
2. Set the following call parameters:
Parameter

Description

Minutes

To set a wait time of one or more minutes.

Parameter

Description

Seconds

To set a wait time of one or more seconds.

Milliseconds

To set a wait time of one or more milliseconds.

### 2.3.4.5 Using IfThisSkipNext Action

The IfThisSkipNext action allows skipping the next Step if a condition is verified. It could be useful during the
execution of the Initialization Steps, to avoid errors on already existing objects.

Procedure
1. In the Properties tab, in the Action field select IfThisSkipNext.
2. Set the following call parameters:

Parameter

Description

CheckingValue

It can be a single value retrieved from a previous Step, or a complex
text composed by many parts.

IsEqualTo

To check the condition in which CheckingValue is equal to the
expected one.

Contains

To check the condition in which CheckingValue contains an
expected string.

IsNotNull

To check the condition in which CheckingValue exists.

NegateCheck

To apply a “NOT” operator on the condition.

Parameter

Description

SkipAll

If set to True, all next Steps are skipped.

SkipToStep

To skip to a specific Step. To be set to the Step ID.

### 2.3.4.6 Using CreateTextFile Action

The CreateTextFile action allows creating a text file, such as xml, json, csv, containing data retrieved from previous
Steps.

Procedure
1. In the Properties tab, in the Action field select CreateTextFile.
2. Set the following call parameters:
Parameter

Description

FileText

The text that will be saved into the file. In the text, you can insert dynamic
Tags that will be resolved during the execution.

FilePath

The file path that will be generated using Tags.

Here, an example of text with tags:

Here, an example of the created file:

### 2.3.4.7 Using CopyFile Action

The CopyFile action allows to copy an existing file inside a folder. The copied file can have the same name or can be
renamed.
If a file with the same name and extension already exists, the new file will not be overwritten.
Is possible to delete the source file after the copy

Procedure
1. In the Properties tab, in the Action field select CopyFile.
2. Set the following call parameters:
Parameter

Description

SourceFilePath

The folder path that contains the file to be copied

TargetFilePath

folder\filename where the file is copied

DeleteSource

If true the source file in SourceFilePath is deleted

### 2.3.4.8 Using RunVSTest Action

The RunVSTest action allows executing tests developed with Visual Studio.
This action can be useful when you have to execute a very complex test already developed.

Procedure
1. In the Properties tab, in the Action field select RunVSTest.
2. Set the following call parameters:
Parameter

Description

VSTestFilePath

The path of the library containing the Test.

SettingsFilePath

The path of the .runsettings file.

TestName

The name of the Test.

TimeOut

The default value is 30 seconds.

Parameter

Description

UseTestRunner

If the test has to be executed on a machine where Visual Studio is
not installed, use the Test.Runner.Console helper, instead of the
standard Test Execution Command Line Tool.
To use the helper, set this option to True.

> Note: The Test.Runner.Console.exe should be available in a subfolder named TestRunner under the Tester Tool folder. If you want to use another folder, you have to add it to the Environment variable Path.

3. In the Result tab, take a look at the result.

### 2.3.4.9 Using SetVariables Action

The SetVariables action allows:
- Setting the value of variables defined at Test Suite level or at Test level. Variables at Test Suite level must
already exist, while variables at Test level can be added. See Using SetVariables with simple values.
- Setting the value of variables using several string and mathematical functions. See Using SetVariables using
Functions.

Using SetVariables with simple values
1. In the Properties tab, in the Action field select SetVariables.
2. Set the following call parameters:
Parameter

Description

Variables

Each element in the Variables collection must have the format:
[VarName]=[Value].
Variables at Test Suite level have the prefix suite. (that can be
omitted). Variables at Test level must have the prefix test. or this.

Using SetVariables using Functions
In the Properties tab, in the Action field select SetVariables.
Here, the string and mathematical functions to be used to set the variable values:
String Functions:
- SubString(Value, Start, Len)
- Replace(Value, SubStr, RepStr)
- ReplaceSub(Val, Start, Len, Rep)
- Remove(Value, Start, Len)
- Trim(Value)
- ToLower(Value)

- ToUpper(Value)
- PadLeft(Value, TotalLen, Char)
- PadRight(Value, TotalLen, Char)
Mathematical Functions:
- Sum(V1, V2, V3, ...)
- Subtract(V1, V2)
- Product(V1, V2, V3, ...)
- Divide(V1, V2)
- Mod(V1, V2)
- Percent(Value, %)
- Round(Value, Digits)
- Power(Value, Exp)
- Quotient(Value)
- Avg(V1, V2, V3, ...)
- Min(V1, V2, V3, ...)
- Max(V1, V2, V3, ...)

> Note:
> - Functions are case insensitive.
> - Functions cannot be nested.

### 2.3.4.10 Using ExecSubTest Action

The ExecSubTest action allows executing a Sub-Test, such as a subroutine.

Procedure
1. In the Properties tab, in the Action field select ExecSubTest.
2. Set the following call parameters:
Parameter

Description

TestName

The name of the Test.

TestTag

This field can be ignored.

CSVDataPath

This field can be ignored.

Iterations

This field can be ignored.

TestVariables

The value of Sub-Test variables.
From the Sub-Test, you can access the variable values using the
tag #TEST_VAR.xxx#.

ResultFromSteps

The result of executed steps can be retrieved from the Sub-Test
after the execution.

ReturnVariables

The value of test variables can be retrieved from the Sub-Test after
the execution.

3. Since the Sub-Tests must not be enabled, remove the setting in the Is Enabled option.

### 2.3.4.11 Using ForEachExecStep Action

The ForEachExecStep action allows executing a Step for each element in a result array. For example, you can
update all materials returned by a query.

Procedure
1. In the Properties tab, in the Action field select ForEachExecStep.
2. Set the following call parameters:
Parameter

Description

DataSourceStep

When the action is executed, it reads the elements in the Result
array of DataSourceStep and for each of them:
- Sets its result with the element
- Calls the ExecutionStep
- Waits specified delay

ExecutionStep

Step called with the input retrieved from DataSourceStep
parameter.

ForEachDelay

If it is not specified, the value set in the Step Delay parameter in
the Test Suite tab will be considered.

3. Since the Execution Step must not be enabled, remove the setting in the Is Enabled option.

### 2.3.4.12 Using Transform Action

The Transform action allows creating an array of “virtual entities” by getting data from elements of an array,
returned by another Step specified with a dedicated parameter (DataSourceStep).
It is possible also to insert additional data from other steps, tags and constants.
The definition of the output entity can be performed specifying the list of properties or using a custom json
structure.

Procedure
1. In the Properties tab, in the Action field select Transform.
2. Set the following call parameters:
Parameter

Description

DataSourceStep

When the action is executed, it gets data from elements of an array,
returned by another Step specified with DataSourceStep.

EntityProperty

Each property can have the format:
- Only name of source property
- [Name]=[DataPath]
- [Name]=#xxx# tag
- [Name]=constant
- [Name]=string with placeholders

Parameter

Description

EntityStructure

Dynamic data can be inserted using <<DataTokenPath>>
placeholders.

### 2.3.4.13 Using LoadTextFile Action

The LoadTextFile action allows loading a text file. The content of the file will be available in the Result tab as an
array of lines (strings) that can be checked with Asserts and used as input data from another Step.
If the file contains json or xml data, instead of the text lines, it is possible to set the Result with the read Json object
(if xml, an equivalent json object will be generated). In this case, the attributes of json object can be read as usual. If
is also possible to use wildcards in filename (e.g. C:\Temp\File*.xml) and, in this case, the last modified file will be
loaded.

Procedure
1. In the Properties tab, in the Action field select LoadTextFile.
2. Set the following call parameters:

Parameter

Description

FilePath

The file path that will be generated using Tags.

Parameter

Description

ParseAsJson

If set to true, set the Result with the read Json object.

### 2.3.4.14 Using ListFiles Action

The ListFiles action allows to retrieve the list of files inside a folder. The list of the files will be available in
the Result and Data tab.
Is possible to search files filtering the extension and to sort them by Name, Size, Date, Extension.

Procedure
1. In the Properties tab, in the Action field select ListFiles.
2. Set the following call parameters:
Parameter

Description

FolderPath

The folder path that contains the list of the files

SearchPattern

used to filter the file extensions (e.g. *.dll)

SortBy

property used to sort the files (Name, Size, Date, Extension)

Descending

if true descending sort is applied

### 2.3.4.15 Using DeleteFile Action

The DeleteFile action allows to delete a file inside a directory.

Procedure
1. In the Properties tab, in the Action field select DeleteFile.
2. Set the following call parameters:
Parameter

Description

FilePath

The file to be deleted

## 3 How to Execute a Test Suite

The Opcenter Execution Foundation Tester tool allows performing many types of execution:
- Runnig a single Step
- Runnig a single Test
- Running the entire Test Suite
- Running the Test Suite using an external Agent.
For other operations available on the execution, see Available Operations on the Execution.
You can also execute the Test Suite via script, as well as perform other execution-related operations. See How to
Perform Execution-Related Operations via Scripts.

> Note: When executing a Test Suite, local data can be modified. We recommend that you run the tool only in a test environment.

Prerequisites
You must have write permissions on the local folder in which to execute the Test Suite.

Available Operations on the Execution
Operatio
n

Description

Skip Step

To skip a failed Step.

Resume

To resume the execution.

Stop

To stop the execution if it cannot be resumed.

Pause

To pause the execution of the Test Suite.

Do Step

To execute a single Step when the execution is paused.

Do Test

To execute the Test until it is completed.

Using
Break
Point

To pause the execution before a specific Step.

What to do next
When the execution is completed or, especially, when an error occurs, it is useful to review the execution. See How
to Review the Test Suite Execution.

### 3.1 Running a Single Step

During the Test Suite preparation, it is useful to run a single Step, for example to ensure correctness of parameters.
When you need to insert a Tag getting data from a Step, if you run that Step in advance, you can view all result
attributes and select one of them from the related combo box.

Procedure
1. In the Test Definition tab, select a Step.
2. Click Do Step. The selected Step will be executed.
3. In the Payload tab, take a look at the Parameters with Resolved Tags. Tags resolved before the execution can
change to the actual values after the execution. See How to Review the Test Suite Execution.

### 3.2 Running a Single Test

You can execute a single Test with all related Steps. All Steps will be executed as many times as the number set in
the Iteration parameter in the Test Suite.

Procedure
1. In the Test Definition tab, select a Step.
2. Click Do Test. The selected Test will be executed and all Steps will be executed.

3. To slow down the execution, in the Test Suite Tab, for each Step set the Step Delay field to a delay in
milliseconds.
During the Test execution, Steps change their status, and the progress bar allows evaluating the remaining time to
the end. If you click Do Test before the end of the Test, the execution will be interrupted.

### 3.3 Running the Test Suite

You can run the entire Test Suite with all Tests and Steps. The execution will be repeated as many times as the
number set in the Iteration parameter in the Test Suite.
A Test Suite can be also run by running the Test Suite with multi-user execution. This option can be useful for
enhancing performances and loading multiple tests.

Running the Test Suite
1. In the Test Definition tab, click Play. The execution will start. During the execution, Tests and Steps change
their status, and the progress bar allows evaluating the remaining time to the end. Once the execution is
finished, the system sets the following parameters:

Parameters

Description

Runs

The number of executions.

Average

The average execution time in seconds.

Parameters

Description

Min

The minimum execution time in seconds.

Max

The maximum execution time in seconds.

2. If you want to reset statistics, click the Reset Statistics button, or set the Reset Statistics before to Save the
Suite checkbox to reset statistics before to save the Suite.

Running the Test Suite with multi-user execution
In the Multi Agent tab you can execute a test simulating the multi-user execution.

1. When the configuration is saved, click the Start Agent button: the agents will execute all the enabled test
definitions saved inside the Test Suite.

2. The following parameters can be configured:
Parameter

Description

N. of Agents

The number of users that will be used for execution. Depending on the resources of
the machine, you can execute up to 500 agents.

Users

To be used by Agents. Each Agent will use one of the users inserted in dialog box. You
can include a user in one of the following ways:
- Manually, inserting user and password (that is encrypted after typing it)
- from a csv file containing the list of users and passwords (that are
encrypted after import)
If no user is defined, the credentials set in the connection parameters of the Test Suite
will be used for each agent.
If the number of users is lower than the number of agents, the list of users will be
reused until the number of agent is reached. Example: N. of Agents: 4
List of Users: Operator1, Operator2. Each user will be used to run 2 agents.

Start Delay

To set a delay time before the next agents are started. It can range from 0 (all agents
will start at the same time) to 3600 seconds.

Get Output

If set, the execution of the selected agent can be monitored in the output window.
Note: when you simulate the execution of a high number of agents and test steps, we
suggest that you disable the Get Output option and enable the Save Execution Log
option at Test Suite Level.

If Save Raw Statistics and Save Execution Log options have been set in the Test Suite, statistics and logs will be
automatically saved for each Agent.
If Save Raw Statistic has been set, after the test execution you can click the Overall Statistics button that will
generate an Overall folder (inside the Statistics folder) containing the csv files of the Test Steps, Test Definition
and Test Suite with Minimum, Average and Maximum time retrieved from the execution.

Best practice before starting the execution of the required agents and users
1. Set an initial configuration to check that the execution of each agent is the expected one (e.g. N. of Agents = 4,
Start Delay = 1) and save the Test Suite.
2. Click on Start Agent and check that the execution of each agent is the expected one. Note: By selecting a
specific agent, you can monitor its execution in the output window on the right:

3. If the test result is the expected one, you can set: N. of Agent, Users and Start Delay according to the desired
execution.
4. Disable the Get Output option.
5. Save the test suite.
During the test execution, if you want to add more agents, click One More and you can stop all Agents, or the
selected ones, by clicking Stop Agents or Stop Selected, respectively.

## 4 How to Perform Execution-Related Operations via Scripts

Opcenter Execution Foundation allows you to execute the Test Suite by running the OpcenterEXFNTester.exe
utility from command line, as well as perform other execution-related operations.
The Test Suite can also be executed via OpcenterEXFNTesterAgent.exe utility, as well as other execution-related
operations.

Prerequisites
You must have write permissions on the local folder in which to execute the Test Suite.

Available Operations
- Perform execution-related operations via OpcenterEXFNTester.exe utility.
- Perform execution-related operations via OpcenterEXFNTesterAgent.exe utility.

### 4.1 Performing Execution-Related Operations via OpcenterEXFNTester.exe

Opcenter Execution Foundation allows you to execute the Test Suite by running the OpcenterEXFNTester.exe
utility from command line, as well as perform other execution-related operations.

Procedure
1. From the local folder in which the OpcenterEXFNTester.exe utility is located, run the command prompt.
2. Type <LocalPath>\OpcenterEXFNTester.exe -h. An help text is displayed.
3. Type -File=<LocalPath>\<TestSuiteName>.<TestSuiteFormat> to load the Test Suite. <TestSuiteFormat>
can be opexts, opextx or opexty, depending on the format you have selected when saving the Test Suite.
4. Do one or more of the following:
- overwrite Test Suite settings, previously set when creating the Test Suite
- execute the Test Suite and/or perform other execution-related operations.

Overwriting Test Suite settings
Type one or more of the following, according to your needs. For the parameter description, see How to Create Test
Suites.
Parameters

Description

- -Host
- -User
- -Pwd
- -UseHttps

To override Test Suite Settings

-Plant

To override the Plant

-Tag

To override Test Suite Tags

Parameters

Description

- -BreakOnError
- -SaveLog
- -LogVerbose
- -SaveStat

To override the execution options. Possible values to be set:
true, false.

- -Var:BaseMatNId
- -Var:BaseId

To override Suite Variables

By executing the following example, Test Suite settings will be overwritten.
Example
<LocalPath>\OpcenterEXFNTester.exe -File=<LocalPath>\<TestSuiteName>.opexts
-Host=<TestMachineName> -User=<TestUser> -Pwd=<TestPwd> -UseHttps=false

Performing execution-related operations
Type one or more of the following, according to your needs.
Operation

Description

-Init

To initialize the Connection. This operation is automatically performed
when running the Test Suite (-Play).

-Reset

To reset the statistics saved in the Test Suite file.

-Play

To run the Test Suite.

-Save

To save the Test Suite when the execution succeeded. The Test Suite will
be saved in the same original format (.opexts, .opextx or .opexty with
the same password required for opening it).

-AutoClose

To close the application after the execution.

-ForceClose

To force the application to close when the execution fails.

By executing the following example, Test Suite statistics will be reset. Then, the Test Suite will be run and saved,
and the application will be closed after the execution, also in case of execution failure.

Example
<LocalPath>\OpcenterEXFNTester.exe -File=<LocalPath>\<TestSuiteName>.opexts -Reset
-Play -AutoClose -ForceClose -Save

### 4.2 Performing Execution-Related Operations via OpcenterEXFNTesterAgent.exe

Opcenter Execution Foundation allows you to execute the Test Suite by running the
OpcenterEXFNTesterAgent.exe utility from command line, as well as perform other execution-related operations.

Procedure
1. From the local folder in which the OpcenterEXFNTester.exe utility is located, run the command prompt.
2. Type <LocalPath>\OpcenterEXFNTesterAgent.exe -h. An help text is displayed.
3. Type -File=<LocalPath>\<TestSuiteName>.<TestSuiteFormat> to load the Test Suite. <TestSuiteFormat>
can be opexts, opextx or opexty, depending on the format you have selected when saving the Test Suite.
4. Do one or more of the following:
- overwrite Test Suite settings, previously set when creating the Test Suite
- execute the Test Suite and/or perform other execution-related operations.

Overwriting Test Suite settings
Type one or more of the following, according to your needs. For the parameter description, see How to Create Test
Suites.
Parameters

Description

- -Host
- -User
- -Pwd
- -UseHttps

To override Test Suite Settings

-Plant

To override the Plant

-Tag

To override Test Suite Tags

- -BreakOnError
- -SaveLog
- -LogVerbose
- -SaveStat

To override the execution options. Possible values to be set:
true, false.

- -Var:BaseMatNId
- -Var:BaseId

To override Suite Variables

By executing the following example, Test Suite settings will be overwritten.

Example
<LocalPath>\OpcenterEXFNTesterAgent.exe -File=<LocalPath>\<TestSuiteName>.opexts
-Host=<TestMachineName> -User=<TestUser> -Pwd=<TestPwd> -UseHttps=false
-Var:<SuiteVar>=<VarValue>

Performing execution-related operations
Type one or more of the following, according to your needs.
Operation

Description

-Test

To execute only a single test.

-Reset

To reset the statistics saved in the Test Suite file.

-Save

To save the Test Suite when the execution succeeded. The Test Suite will be
saved in the same original format (.opexts, .opextx or .opexty with the
same password required for opening it).

-FilePwd

It is related to the password required to run the .opexty encrypted file. If not
specified, the password will be required in the command prompt. If the file
is saved in one of the other formats (.opexts or .opextx), this field will be
ignored.

By executing the following example, Test Suite statistics will be reset. Then, a single Test will be run and the Test
Suite saved.
Example
<LocalPath>\OpcenterEXFNTesterAgent.exe -File=<LocalPath>\<TestSuiteName>.opexts
-Reset -Test=<TestName> -Save

## 5 How to Review the Test Suite Execution

When the execution of the Test Suite is completed or, especially, when an error occurs, it is useful to review the
status of each executed Steps. For this purpose, the tool interface provides many tabs.
Tab

Description

Propertie
s

To see the properties of the Step.

Payload

To see the payload used for the call. It is displayed only in case of Test Steps configured setting
Command parameters.

Query

To see the executed Odata queries. It is displayed only in case of Test Steps configured to read
data from Entities.

Data

To see the result of the queries in tabular form. It is displayed only in case of Test Steps configured
to read data from Entities.

Result

To see the result of the Step. To check the result content, in the Asserts on Result's Content
grid you can set Asserts. You can refer to an attribute in the text box of the Result tab using a
standard Json Token Path and select the check type from the drop down. Succeeded asserts are
displayed in green, while failed asserts in red.

Execution Log

> Note:
> - For the first value in Entity result data, you can omit value[]. and use the parameter name.
> - To check boolean values, use [IsTrue] and [IsFalse].

To see the execution log containing all information about executed Tests and Steps. You can see
the log both at the end and during the Test Suite execution.
If Save Raw Statistics and Save Execution Log options have been set in the Test Suite, statistics
and log will be automatically saved at the end of Test Suite execution.

In this way, if an error occurs during the execution, you can see all this information, edit the Step and try to solve
the problem. If the problem cannot be solved during the execution, you can skip the Step (see Available Operations
on the Execution).
If the execution of the Test Suite is successfully completed, you can anyway take a look at this information, in order
to review the status of each executed Steps.
