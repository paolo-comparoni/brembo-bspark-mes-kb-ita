# OpcenterEXDS_ProductOverview

> Documento sorgente: `E:\BremboDocs\01 Opcenter 2507 Manuals\OpcenterEXDS_ProductOverview.pdf`  
> Tipo: PDF · Pagine: 155


## Pagina 1

Opcenter Execution Discrete 2507

Product Overview

08/2025
PL20250519659659531


## Pagina 2

Guidelines
This manual contains notes of varying importance that should be read with care; i.e.:
Important:
Highlights key information on handling the product, the product itself or to a particular part of the documentation.
Note: Provides supplementary information regarding handling the product, the product itself or a specific part of
the documentation.
Trademarks
All names identified by ® are registered trademarks of Siemens AG.
The remaining trademarks in this publication may be trademarks whose use by third parties for their own purposes
could violate the rights of the owner.
Disclaimer of Liability
We have reviewed the contents of this publication to ensure consistency with the hardware and software
described. Since variance cannot be precluded entirely, we cannot guarantee full consistency. However, the
information in this publication is reviewed regularly and any necessary corrections are included in subsequent
editions.
Cybersecurity Information
Siemens provides products and solutions with industrial cybersecurity functions that support the secure operation
of plants, systems, machines and networks.
In order to protect plants, systems, machines and networks against cyber threats, it is necessary to implement and continuously maintain - a holistic, state-of-the-art industrial cybersecurity concept. Siemens products and
solutions constitute one element of such a concept.
Customers are responsible for preventing unauthorized access to their plants, systems, machines and networks.
Such systems, machines and components should only be connected to an enterprise network or the internet if and
to the extent such a connection is necessary and only when appropriate security measures (e.g. firewalls and/or
network segmentation) are in place.
For additional information on industrial cybersecurity measures that may be implemented, please visit
https://www.siemens.com/cybersecurity-industry.

Siemens products and solutions undergo continuous development to make them more secure. Siemens strongly
recommends that product updates are applied as soon as they are available and that the latest product versions
are used. Use of product versions that are no longer supported, and failure to apply the latest updates may increase
customer’s exposure to cyber threats.

To stay informed about product updates, subscribe to the Siemens Industrial Cybersecurity RSS feed under
https://www.siemens.com/cert.

Siemens AG

PL20250519659659531

Copyright © Siemens AG 2025

Digital Industries

20250801_112841

Technical data subject to change

Postfach 48 48
90026 NÜRNBERG
GERMANY


## Pagina 3

Table of Contents
1

What is Opcenter Execution Discrete? ...............................................................9

2

Basic Concepts ..................................................................................................12

2.1

Common Terms...................................................................................................................... 12

2.1.1

Revisions............................................................................................................................................................... 12

2.1.2

States and Lifecycles............................................................................................................................................ 12

2.2

User Management Definition for Access Control.................................................................. 13

2.2.1

Users and Groups ................................................................................................................................................. 13

2.2.2

Roles ..................................................................................................................................................................... 14

2.2.3

Multiplant Support............................................................................................................................................... 15

2.3

Production Environment Configuration ............................................................................... 15

2.3.1

Business Plant Model: Equipment Levels and Machines ................................................................................... 16

2.3.2

Numbering Patterns ............................................................................................................................................ 18

2.3.3

Reasons ................................................................................................................................................................ 18

2.3.4

Tool Definitions .................................................................................................................................................... 18

2.3.5

Materials and Material Tracking Units ................................................................................................................ 19

2.3.6

Containers and Container Types......................................................................................................................... 24

2.3.7

Setpoints .............................................................................................................................................................. 26

2.3.8

Certifications, Human Resources and Skills ....................................................................................................... 27

2.3.9

Teams ................................................................................................................................................................... 28

2.3.10 Defects, Failures and their related Elements...................................................................................................... 28
2.3.11 Non-Conformances and Rework Codes.............................................................................................................. 29
2.3.12 Work Operations .................................................................................................................................................. 35
2.3.13 Operation/Step Categories.................................................................................................................................. 35
2.3.14 Work Instruction Definitions................................................................................................................................ 36
2.3.15 Interlocking Checks.............................................................................................................................................. 36
2.3.16 Line Side Positions............................................................................................................................................... 37
2.3.17 Bills of Features and their related Elements....................................................................................................... 37
2.3.18 Product Configuration ......................................................................................................................................... 38
2.3.19 Qualification Criteria............................................................................................................................................ 38
2.3.20 Production Flow Control ..................................................................................................................................... 40
2.3.20.1 Milestone Attributes............................................................................................................................................. 41
2.3.21 Quality Gates ........................................................................................................................................................ 44

2.4

Production Environment Configuration in Additive Manufacturing ................................... 44

2.4.1

Print Job Files....................................................................................................................................................... 44

Opcenter Execution Discrete 2507 - Product Overview

iii


## Pagina 4

2.4.2

Substrates ............................................................................................................................................................ 45

2.4.3

Powder Materials and Powder Material Batches................................................................................................ 46

2.5

Production Process Configuration........................................................................................ 48

2.5.1

As Planned BOPs, Master Plans, Processes, Operations and Steps .................................................................. 48

2.5.1.1 Alternative Process Operations........................................................................................................................... 52
2.5.2

Sequences and Dependencies ............................................................................................................................ 52

2.5.3

Catalogs................................................................................................................................................................ 53

2.5.4

Work Instructions, Documents and Document Items ........................................................................................ 53

2.5.4.1 Document Items................................................................................................................................................... 55

2.6

Production Execution Management ..................................................................................... 56

2.6.1

Tools ..................................................................................................................................................................... 56

2.6.2

Pre-Kitting ............................................................................................................................................................ 58

2.6.3

ERP Order and ERP Order State Machine............................................................................................................ 58

2.6.4

Work Orders, Work Order Operations and Work Order Steps............................................................................ 59

2.6.4.1 Alternative Work Order Operations..................................................................................................................... 67
2.6.4.2 Results and Result Types ..................................................................................................................................... 69
2.6.5

Execution Groups and Execution Group Phases ................................................................................................ 69

2.6.6

Transportation Management .............................................................................................................................. 72

2.6.6.1 Logistic Classes .................................................................................................................................................... 73
2.6.6.2 Buffer Definitions and Buffers ............................................................................................................................. 73
2.6.6.3 Logistic Requests ................................................................................................................................................. 74
2.6.6.4 Handling Units and Transport Operations ......................................................................................................... 76
2.6.7

Non-Productive Activities .................................................................................................................................... 78

2.6.8

Offline Sessions and Offline Actions ................................................................................................................... 79

2.6.9

Change Packages ................................................................................................................................................. 81

2.7

Quality Management.............................................................................................................. 83

2.8

Notification Handling............................................................................................................. 87

2.8.1

Notifications ......................................................................................................................................................... 87

2.8.2

Signatures............................................................................................................................................................. 87

2.9

Production Execution Monitoring ......................................................................................... 88

2.9.1

Genealogy............................................................................................................................................................. 88

2.10

Integration with External Systems ........................................................................................ 89

2.10.1 Advanced Planning and Scheduling (APS).......................................................................................................... 89
2.10.2 Distributed Numerical Control (DNC) ................................................................................................................. 89
2.10.3 Closed-Loop Manufacturing ................................................................................................................................ 90
2.10.4 Structured Messages............................................................................................................................................ 90

iv

Opcenter Execution Discrete2507 - Product Overview


## Pagina 5

2.10.5 Import Data Flows................................................................................................................................................ 90
2.10.6 Output Messages.................................................................................................................................................. 91
2.10.6.1 Output Message Sections .................................................................................................................................... 92
2.10.7 Kanban Calls....................................................................................................................................................... 105
2.10.8 Teamcenter Share.............................................................................................................................................. 106
2.10.9 Additive Manufacturing Network ...................................................................................................................... 106
2.10.10 Intraplant Logistics (IPL).................................................................................................................................... 106

2.11

Support of Hybrid Scenarios Englobing Opcenter Execution Process.............................. 106

3

Product Features.............................................................................................107

3.1

Access Control through Roles and Certifications ............................................................... 108

3.2

Team Management .............................................................................................................. 109

3.3

Labor Tracking ..................................................................................................................... 109

3.4

System Localization............................................................................................................. 110

3.5

Native Data Definition and Management for Engineering and Runtime Needs ............... 110

3.6

Operation/Step Category Management.............................................................................. 111

3.7

Material Management .......................................................................................................... 112

3.8

Container Management ....................................................................................................... 113

3.9

Tool Management ................................................................................................................ 114

3.10

Screwing Tool Management................................................................................................ 115

3.11

Open Protocol Tool Management ....................................................................................... 117

3.12

Barcode Management.......................................................................................................... 118

3.13

ID and Serial Number Generation ....................................................................................... 118

3.14

Readily-Available Work Instructions and Documents........................................................ 119

3.15

Document Item Management.............................................................................................. 121

3.16

Functionalities for As Planned BOP, Master Plan and Process Management ................... 122

3.17

Feature Management........................................................................................................... 122

3.18

Product Configuration Management .................................................................................. 123

3.19

Production Flow Control Management............................................................................... 124

3.20

Qualification Criteria Management for Master Plan Contexts ........................................... 124

3.21

Dedicated Catalogs for Reusing Processes, Operations and Steps................................... 124

3.22

Versatile Work Order Management ..................................................................................... 125

3.23

Alternative Paths for Operation Execution ......................................................................... 125

3.24

Pre-Kitting for Reserving Specific Material Tracking Units ................................................ 126

Opcenter Execution Discrete 2507 - Product Overview

v


## Pagina 6

3.25

Runtime Work Order Execution........................................................................................... 126

3.26

Result Management ............................................................................................................. 127

3.27

Interlocking Checks for Governing Work Order Operation Execution............................... 128

3.28

Exchange of Messages with the Shop Floor........................................................................ 129

3.29

Adoption of Execution Groups for Maximizing Productivity.............................................. 129

3.30

On The Fly Management of Changes to the Production Process ...................................... 130

3.31

Change Package Management ............................................................................................ 130

3.32

Work Order Dispatching....................................................................................................... 130

3.33

Order Work In Progress (WIP) Monitoring........................................................................... 131

3.34

Use of Tasks for Managing Work Order Operation/Step Progression ............................... 131

3.35

Runtime Data Collection Capabilities ................................................................................. 132

3.36

Semi-Automatic Acquisition of Values................................................................................ 133

3.37

Runtime Behavior for Machines and Tools ......................................................................... 135

3.38

Non-Productive Activity Management................................................................................ 136

3.39

Label Printing ....................................................................................................................... 136

3.40

Work Order Operation Execution Using the High Automation User Interface.................. 136

3.41

Production Execution in Offline Mode ................................................................................ 137

3.42

Line Side Inventory and Kanban Call Management ........................................................... 138

3.43

Non-Conformances and Rework Codes for Runtime Quality Management ..................... 138

3.44

Electronic Signature and Buy-Off Management................................................................. 139

3.45

Data Tracing for Production Activities ................................................................................ 140

3.46

Quality Inspections .............................................................................................................. 141

3.47

Advanced Planning and Scheduling Integration (Opcenter APS) ..................................... 142

3.48

Integration with Teamcenter and SAP................................................................................ 142

3.49

Integration with Generic Distributed Numerical Control (DNC) Systems ......................... 145

3.50

Integration with Opcenter Connect MOM ........................................................................... 146

3.51

Integration with Teamcenter Share .................................................................................... 146

3.52

Integration with the Shop Floor via OPC UA....................................................................... 147

3.52.1 Handshake Protocols......................................................................................................................................... 148
3.52.1.1 PLC to MES (synchronous mode) ...................................................................................................................... 148
3.52.1.2 From PLC to MES (asynchronous mode)........................................................................................................... 149

3.53

Integration with Additive Manufacturing Network ............................................................ 150

3.54

Integration with Intraplant Logistics (Opcenter IPL) ......................................................... 150

vi

Opcenter Execution Discrete2507 - Product Overview


## Pagina 7

3.55

Powder Batch Management ................................................................................................ 151

3.56

Substrate Management ....................................................................................................... 152

3.57

Print Job File Management.................................................................................................. 153

3.58

Print Job File Pre-Transfer Management............................................................................ 153

3.59

Management of Intra-Plant Logistics.................................................................................. 154

3.60

Monitoring of the Production Status .................................................................................. 154

3.61

Quality Gate Management................................................................................................... 155

Opcenter Execution Discrete 2507 - Product Overview

vii


## Pagina 8

8

ID

OpcenterEXDS_ProductOverview

Title

Product Overview

Product Title

Opcenter Execution Discrete

Version Title

2507

Product Version

OpcenterEXDS_2507

Category

Concepts

Summary

The document aims at giving an overview of Opcenter Execution
Discrete.

Audience

System Integrator, Customer Decision-Maker, Supervisor

Revision

PL20250519659659531

State

Published

Author

Siemens AG

Language

en-US

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 9

What is Opcenter Execution Discrete?

1 What is Opcenter Execution Discrete?
Opcenter Execution Discrete is designed to satisfy the most common needs of industries with a hierarchical
structure in which specific macro-areas are dedicated to executing discrete manufacturing functionalities in various
stages in order to produce the desired product. The industries targeted operate in the following categories:
• Automotive tier suppliers
• A&D tier suppliers
• Energy & Utilities
• Industrial Machinery and Heavy Equipment
• White Goods and Home Appliances
• Complex Parts Manufacturing and Assembly
• Additive Manufacturing.

Manufacturing Solutions Available in Opcenter EX DS
Opcenter EX DS offers the following manufacturing Solutions, from which you can choose to take advantage of
those functionalities that are most fitting to satisfy your particular needs:
• U4DM, dedicated to the management of Discrete functionalities in a complex production environment that
includes also Additive Manufacturing and High Variance activities.
• DS, dedicated exclusively to the management of Discrete functionalities. This Solution does not include
functionalities related to Additive Manufacturing and/or High Variance production environments.
• OnePieceFlow, dedicated to the management of Discrete functionalities in a complex production environment
that also includes High Variance activities.

Functionalities and Features
Opcenter EX DS provides you with all basic functionalities for:
• Modelling your production environment, consisting in locations, machines required for production, work
operations, tools, materials, etc..
• Defining how products are produced (that is, defining the various operations and/or steps involved in their
production).
• Creating production orders, in which you define the type of production to be adopted and the quantity to be
produced for the order you have in mind.
• Scheduling production according to your needs.
• Tracking and monitoring production, to see how the execution of your work order is progressing.
For an overview of the main features offered by Opcenter EX DS, see Product Features.

Industry Templates
Thanks to the introduction of a series of Low Code UI Applications powered by Mendix, Opcenter EX DS can address
the specific needs of different types of production more effectively. Each of these Apps presents dedicated User
Interfaces that are particularly suited for use in a given context, thereby simplifying the work of those users who
must perform production-related activities. In brief, these dedicated User interfaces can be considered as Industryspecific templates.
The table below summarizes the various production types and the Low Code UI Apps that are currently available for
use in these contexts.

Opcenter Execution Discrete 2507 - Product Overview

9


## Pagina 10

What is Opcenter Execution Discrete?

If your plant executes....

Then adopt...

Serialized, FlexibleSerialized or FullQuantity
production

Opcenter Execution Discrete Complex Manufacturing

TransferBatch or FlexibleBatch production

Opcenter Execution Discrete Repetitive Manufacturing

high-automated production

Opcenter Execution Discrete One Piece Flow

quality-testing activities

Opcenter Execution Discrete Quality Execution

Each of the aforementioned Low Code UI Apps can be either used in stand-alone mode or in combination with one
or more of the other Low Code UI Apps.
In addition, depending on the role that you have been assigned, instead of using the legacy UI screens provided by
Opcenter Execution Discrete, you can choose to adopt engineering and system UI screens offered by Low Code UI
Applications powered by Mendix. In detail:
For User Role...

You can use engineering and system screens provided by Low
Code UI App....

Product Engineer

Opcenter EX DS Product Engineer

Production Coordinator

Opcenter EX DS Production Coordinator

System Administrator

Opcenter EX DS System
This Low Code UI App provides the essential UIs in Opcenter
EX FN screens for one-shot use to perform basic system
configuration settings: i.e., Status Machine, Numbering
Pattern and UoM.

System Administrator

Opcenter EX DS System Administrator
This Low Code UI App provides the essential UIs in Opcenter
EX FN screens for one-shot use to monitor the system: i.e.,
Application Log, Data Maintenance, Barcode Rule History.

A complete list of the currently released engineering and system UI screens is available in page Apps and Extension
Apps included in the Available Discrete Solutions of the Opcenter Execution Discrete User Manual.

Licensing schema
There are different types of floating licenses.
• Opcenter Execution DS Server (mandatory): 1 server license for environment, no matter the number of actual
hosts the solution is running on.
• Opcenter Execution DS Client (mandatory): 1 client license for each concurrent user.

10

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 11

What is Opcenter Execution Discrete?

• Opcenter Execution High Availability (optional) : This license becomes mandatory if the environment is made
up of 3 or more hosts. It allows customers to set up a distributed environment for HA and load balancing.
• Opcenter Execution Additional Site (optional): It allows customers to configure additional plants for a
multiplant deployment (it is not needed for default plant).
• Opcenter Low-Code Adaptation Package (optional): This license is mandatory for those users who intend to
customize one of the available Low Code UI Applications powered by Mendix on their own, without intervention
from Siemens or one of its Partners.
Licenses for Hybrid Scenarios
As of Opcenter Execution Discrete 2507, by purchasing the Opcenter Execution DS Server and Opcenter
Execution DS Client licenses, it is possible to download Opcenter Execution Process from Support Center
and install it on the same machine to take advantage of Process functionalities within a Hybrid scenario.
There is no need to purchase a distinct license for Opcenter Execution Process.
Opcenter Execution Discrete licensing modules include also Opcenter Execution Foundation ones (Opcenter
Execution FN Server and Opcenter Execution FN Client). For more information on Licensing schema, see section
What Is the Opcenter Execution Foundation Licensing Schema? in the Opcenter Execution Foundation Product
Overview.
The Opcenter Execution FN Server license includes the OEE Server license, which allows customers to
configure up to 5 equipment with OEE capabilities. For more information, please refer to Opcenter EX FN
OEE product documentation.

For Opcenter Execution DS Client, in order to correctly visualize 3D files, the following licenses are required:
• for offline mode, MX-AS-3DVIEW-T1 - 3D Viewer Integration
• for offline mode, PLM VIS WEB (WTK1100)
• for online mode, TCM 55045 - Electronic Work Instructions Advanced

Opcenter Execution Discrete 2507 - Product Overview

11


## Pagina 12

Basic Concepts
Common Terms

2 Basic Concepts
This section presents the basic concepts that are the groundwork to using Opcenter Execution Discrete.
To simplify becoming familiar with these concepts within your actual work context, the basic concepts have been
divided into sections reflecting the general workflow that must be executed in order to use the product properly
and to full advantage.
In this manner, you will gradually comprehend those fundamentals in line with your job and the various procedures
you need to perform, adopting a step-by-step learning approach.
Therefore, in addition to common terms often used in describing entities, you will find the basic concepts for:
• Defining user management for access control
• Configuring the production environment
• Configuring the production processes
• Managing production execution
• Handling notifications
• Managing Quality Inspections
• Monitoring production execution
• Integrating Opcenter Execution Discrete with other systems
• Support of Hybrid Scenarios Englobing Opcenter Execution Process.
The functionalities inherent to the basic concepts presented here are illustrated in detail in the Product
Features section.

2.1 Common Terms
Here is a series of common terms often used when describing certain entities:
• Revisions
• States and Lifecycles.

2.1.1 Revisions
In Opcenter Execution Discrete, certain MES entities can be modified as needed, also making major changes to its
structure: the end result is known as a Revision of the original MES entity.
Revisions can be created for the following entities:
• Materials
• Tool Definitions
• Processes, Process Operations and Process Steps
• Buffer Definitions
• Production Flow Control Diagrams
• Bill of Features
• Product Configurations
• Output Messages

2.1.2 States and Lifecycles
The actual progression of the various elements making up the structure of the production process can be followed
by observing how they undergo a transition in status.

12

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 13

Basic Concepts
User Management Definition for Access Control

A state corresponds to the "here and now" condition of an element: whenever the element undergoes a transition,
it will assume another state. The totality of the state transitions that are feasible form what is known as the lifecycle
of the various MES entities.
The following entities have a lifecycle:
• Work Orders, Work Order Operations and Work Order Steps
• Non-Conformances and Rework Codes
• Powder Material batches
• Tools
• Material Tracking Units (MTUs)
• Containers
• Machines
• Substrates
• Setpoints
• ERP Orders
• Execution Groups and Execution Group Phases
• Buffers, Logistic Requests, Handling Units and Transport Operations
• Offline Sessions and Offline Actions
• Buy-Offs
• Change Packages.

2.2 User Management Definition for Access Control
The basic concepts listed below come into play directly while installing and configuring Opcenter
Execution Discrete: the descriptions provided in this section are very generic, but sufficient so that you can
have a general idea as to "who" can do "what" within the system.
For greater details regarding Users, Groups and Roles, see the Opcenter Execution Discrete Installation and
Configuration Manual.
Here are the basic concepts that represent the groundwork for user management and access control:
• Users and Groups
• Roles
• Multiplant Support.

2.2.1 Users and Groups
The adoption of user management is fundamental to any system, as it permits restricting access to sensitive data,
while ensuring that only individuals with the appropriate know-how and who hold a certain position within the
organizational hierarchy of a business perform certain tasks.

Users
In Opcenter Execution Discrete, a User is an individual who can access the application. Each User has a login and a
password.
The list of Opcenter EX DS users is logically separate from the list of Windows users on the machine where Opcenter
EX DS is installed. During installation, a dedicated user with administrative rights is created from a Windows user.
Additional users can be created at a later time: for more details, see the Opcenter Execution Discrete Installation and
Configuration Manual.

Opcenter Execution Discrete 2507 - Product Overview

13


## Pagina 14

Basic Concepts
User Management Definition for Access Control

Optionally, the system can track which Users are logged at a certain time, so that an individual with the appropriate
Role can assign the execution of some Work Order Operations only to specific Users (for example, only to Users who
are currently present in the Plant and possess a specific Skill).
Through appropriate configuration, during the execution of a Work Order, the system can display all its Work Order
Operations or only those assigned to the currently-logged User.

Groups
A Group represents a set of users who have been placed together according to certain rules (for example, they might
share certain characteristics). In a Windows operating system, users can be grouped. In Opcenter EX DS, it is
possible to use these Windows groups, as well as create new groups.

2.2.2 Roles
Roles serve the purpose of granting and restricting access to Opcenter Execution Discrete’s functionalities.
Through appropriate assignment, they allow you to establish clear boundaries as to which actions a certain user
can (and cannot) perform.
It is possible to assign a Role to a single User or to a group of users (User Group).
The product comes provided with several Roles that are installed by default, via the Post-Setup Configuration Tool.
These Roles realistically cover the most common figures present within a Discrete Manufacturing
production environment.
There also exists the possibility of creating custom Roles to satisfy your needs: for information, see
the Opcenter Execution Foundation Development and Configuration Manual.

Here are the default Roles created automatically:
Role

Description

SuperUser

Has access to all functionalities, both engineering and runtime.

SystemAdministrator

Has access to all system functionalities for administration
purposes.

ProductEngineer

• Has access to all configuration and engineering functionality.
• Can create Work Orders.

ProductionCoordinator

• Has visibility on WIP and quality functionalities.
• Has access to Work Order management functions, but cannot
change engineering data.

Operator

• Has visibility on WIP (Work In Progress) and quality
functionalities.
• Has access to Work Order management execution functions.

14

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 15

Basic Concepts
Production Environment Configuration

Role

Description

MPP

Has rights to integrate Opcenter EX DS with Teamcenter
Manufacturing and define Bills of Processes.

APS

Has rights to integrate Opcenter EX DS with Opcenter APS and
download scheduled Work Orders/Work Order Operations from
the Opcenter APS system to the Opcenter EX DS system.

ShopFloorDevice

Has the rights to start and complete Work Order Operations and to
declare and sentence Non-Conformances.

Guest

Has only read-only access on all functionalities.

2.2.3 Multiplant Support
Opcenter Execution Discrete is able to manage a multiplant scenario, supporting multiple factories from a unique
central installation. This means that you can create more plants that are served by a centralized Regional Hub. In a
multiplant scenario, a Manufacturing Solution can be configured both with common settings and options for plantspecific tuning.
For more information on How to Manage the Manufacturing Solution in a Multiplant scenario, see the Multiplant
Management chapter in Opcenter Execution FoundationInstallation Guide.

2.3 Production Environment Configuration
The list of basic concepts provided below is valid for standard production environments. If your
production environment adopts Additive Manufacturing, see Production Environment Configuration in
Additive Manufacturing for those basic concepts specific to this context.

Here are the basic concepts for configuring your production environment:
• Business Plant Model: Equipment Levels and Machines
• Numbering Patterns
• Reasons
• Tool Definitions
• Materials and Material Tracking Units
• Containers and Container Types
• Setpoints
• Certifications, Human Resources and Skills
• Teams
• Defects, Failures and their related Elements
• Non-Conformances and Rework Codes
• Work Operations
• Operation/Step Categories
• Work Instruction Definitions
• Interlocking Checks

Opcenter Execution Discrete 2507 - Product Overview

15


## Pagina 16

Basic Concepts
Production Environment Configuration

• Line Side Positions
• Bills of Features and their related Elements
• Product Configuration
• Qualification Criteria
• Production Flow Control
• Milestone Attributes.
• Quality Gates

2.3.1 Business Plant Model: Equipment Levels and Machines
In Opcenter Execution Discrete, Business Plant Model management is dedicated to defining two distinct yet related
aspects of production within your business:
• The physical context within which production takes place.
• The means that must be used for production.
Within the context of the product:
• The term Equipment Level indicates the place where production is executed (on an organizational level, be
it company-related and/or work-related).
• The term Machine indicates a physical means (that is, piece of equipment) used for production.

Equipment Levels
For what concerns Equipment Levels, the ISA-95 standard has been adopted, following the top-down hierarchy
represented by these abstract Levels:
• Enterprise - 100
• Site - 200
• Area - 300
• WorkCenter - 400
• Unit - 700
ANSI/ISA-95 (more commonly known as ISA-95) is an international standard established by the
International Society of Automation for developing an automated interface between enterprise and
control systems.
Business Plant Model entities with a Level value of 100, 200, 300 and 400 included define a hierarchy of places
within the business. Higher levels englobe lower levels.
Business Plant Model entities with a Level value of 700 (that is, Units) are considered Machines.
Enterprise and Site (also referred to as Plant) are conceived in geographical terms, whereas Area and
WorkCenters are viewed in terms that are more related to how the production itself is organized.

Machines
A Machine is a physical device (for example, a drill or a milling machine) or workstation that is used in the
production environment. Different machines (even if belonging to the same type and/or in the same equipment
level) can have different features.
Machines are instantiated from Equipment Configurations, to which you can associate, through the provided UADM
Equipment Type, the following pre-defined, machine-related properties:
• Is3DPrinter, to identify the machine as a 3D Printer in Additive Manufacturing production.
• EnabledForCompleteByDifferentUser, to enable Work Order Operations to be completed by users that did not
start them.

16

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 17

Basic Concepts
Production Environment Configuration

• Lockable, to avoid concurrent execution at runtime, by locking them.
• ActiveNonConformanceNr, to indicate the number of Non-Conformances active on the specified machine.
• IsActive, to indicate that the machine is currently active.

Machine States
State

Description

Ready

The Machine is available for production.

Running

The Machine is currently running.

Busy

The Machine is currently used in a Work Order Operation.

Repair

The Machine is undergoing maintenance activities.

OnHold

The Machine is currently not available for production for some reason.

Scrapped

The Machine is no longer available for production because it is damaged.

Possible State Transitions for Machines
Source Status

Possible Target States

Ready

• Busy
• Repair
• OnHold
• Scrapped
• Running

Running

• Ready
• Scrapped

Busy

• Ready
• Scrapped

Repair

• Ready
• OnHold
• Scrapped

OnHold

• Ready
• Scrapped

Scrapped

Ready

Opcenter Execution Discrete 2507 - Product Overview

17


## Pagina 18

Basic Concepts
Production Environment Configuration

The Business Plant Model at a Glance
The Business Plant Model can be summarized as follows:
• An Enterprise represents the entire company.
• A Site may be a physical plant or factory owned by the company.
• A Plant may be a physical plant or factory owned by the company.
• An Area may be a sector within a factory.
• An Area may be divided into WorkCenters that focus on a specific type of production.
• A Production Line may represent an assembly line.
• A Workplace may represent a Workstation.
• A Unit coincides with a Machine, which represents the actual device or workstation involved in the production
process.
Starting from Opcenter EX DS 3.0, the Plant is configured via the Opcenter Execution Foundation
Equipment App. Plant Configurations from previous versions must be adapted considering that:
• any piece of Equipment is now created as Equipment Configuration.
• the Cell is an Equipment Configuration mapped to the WorkCenter level.
• the Machine is an Equipment Configuration mapped to the Unit level.
• The Machine Definition is an Equipment Type.
• Previous machine-related properties are now provided via the UADM Equipment Type.

2.3.2 Numbering Patterns
A particularly delicate aspect for many MES users involves the generation of unique identifiers for:
• The Work Orders that need to be executed.
• The material batches involved in the production process for satisfying a Work Order.
• The serial number codes for Material Tracking Units that are single pieces.
In many businesses, the rules used to form these identifiers are normalized according to internal conventions.
In Opcenter Execution Discrete, it is possible to "model" a Numbering Pattern that satisfies your needs, providing a
way to create unique identifiers.

2.3.3 Reasons
A Reason represents a justification to be used by the Operator should it be necessary to pause or skip the execution
of a Work Order Operation, or place a Work Order in Hold or Future Hold status: it is mandatory that a Reason be
provided in order to apply these changes to the execution in question.
Likewise, Reasons are used to justify pausing the execution of an Execution Group.

2.3.4 Tool Definitions
In all industries, tools play an essential role in production activities, be they mounted on a machine (for example, a
bit in a drill) or used manually by a worker (for example, a screwdriver or a smoothing file).
Within the context of the product, a Tool Definition is an abstract representation of a specific tool (for example, "drill
bit, 5 mm"). A Tool Definition is instantiated multiple times to represent the number of actual Tools used in the
plant (for example, "fifty individual 5mm drill bits").
Once created, a Tool Definition can be modified as needed: the end result is a Revision of the original Tool
Definition.

18

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 19

Basic Concepts
Production Environment Configuration

It is possible to set threshold values on Tool Definitions to define:
• how many times their instantiations (that is, the Tools instantiated from them) can be used;
• for how long their instantiations can be used;
• when their instantiations will expire.
Tool Definitions can be set as Lockable during execution: in this manner, it is possible to define which resources
cannot be used concurrently.
Documents can be associated to a Tool Definition (for example, to provide instructions and/or safety procedures to
Operators).
For information on functionalities related to Tool Definitions, see Tool Management.

Example of Tool Instantiation

2.3.5 Materials and Material Tracking Units
Industrial production typically works taking "raw" resources that enter the plant and are consumed or produced to
create intermediate, additional or final products. These "raw" resources, as well as intermediate and final
materials, are generically referred to as Materials.
In our context, the groundwork necessary in preparation of production involves defining these materials as
Materials during Engineering. The instantiation of these Materials will subsequently generate Material Tracking
Units (MTUs) in Runtime.
For information on functionalities related to Materials and Material Tracking Units, see Material Management.
Powder Material and Powder Material Batches
In Additive Manufacturing contexts, Materials and Material Tracking Units are referred to as Powder
Materials and Powder Material Batches, respectively.
For more information, see Powder Materials and Powder Material Batches.

Materials
A Material is an abstract representation of a specific material type. A Material is instantiated to represent actual
items that are consumed or produced in the plant.
The Material Specification Type that you set for the Material to be consumed/assembled or produced during the
execution of a specific Operation (or Step) will affect:

Opcenter Execution Discrete 2507 - Product Overview

19


## Pagina 20

Basic Concepts
Production Environment Configuration

• The manner in which the Material in question will be consumed, in relation to its initial quantity (input Material
Specification Types).
• The output quantity to be produced, in relation to the Material's quantity (output Material Specification Types).

Direction

Material Specification Type

Description

Additive
(not available in the drop-down list and
automatically selected only if the
selected Material is of type AMPowder)

Adopted specifically for Additive Manufacturing
powders.

Alternative

Only one Material among those proposed must
be consumed. This Material will be consumed in
full.

As Required

The quantity to be consumed for each Material
can range from zero to the total quantity of each
Material, meaning that the consumption of the
Material in question can span from not being
consumed in any extent to being consumed in
full.

AutoConsume

A Material for which it is necessary to trace the
consumption regardless of the involved Batch or
Serial Number.

Disassemble

Setting this Material Specification Type affects
how disassembly is performed: if a compound
Material resulting from an assembly of Materials
is successively disassembled, all those Materials
set to Normal Part with the same ID relative to
the completed Work Order Operations (or the
completed Work Order Steps related to the
completed Work Order Operations) belonging to
the same Work Order will be disassembled
(dismantled) from the compound Material.

Material Recording

A Material for which the consumption quantity
value usually received from the field is recorded
as it is, with no additional validations applied.

The entire quantity of the Material must be
consumed: however, once mixed (combined),
the quantity that has been introduced can no
longer be separated, either in full or in part, from
the Powder Material Batch resulting from the
execution of the Operation or Step.

Input

20

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 21

Basic Concepts
Production Environment Configuration

Direction

Material Specification Type

Description

Normal Part (default value)

The entire quantity of the Material must be
consumed.

Range Parts

The portion (partial quantity) of the Material to
be consumed can range from greater than zero
to the total quantity of the Material itself.

Reference

This Material is not directly consumed or
assembled, but is used as a reference for other
activities performed in Work Order Operations.

Selected Fit

The total part quantity for the selected range
must be equal to the maximum quantity of one
of the parts.

Track Loaded AM Powder
(available in the drop-down list only if
the selected Material is of type
AMPowder)

Adopted specifically for Additive Manufacturing
powders.

By-Product

This Material Specification Type is peculiar to
those cases in which, in addition to a distinct
product to be produced, during the execution of
the same Operation (or Step), there will
inevitably be also a resulting by-product
(derivative) that may or may not be further
processed to produce something else.

Output

The quantity of the Powder Material consumed
during a printing operation is tracked, after the
operation has been completed, by rescaling the
quantity of the Powder Batch loaded into the 3D
Printer and used to print the parts for which
consumption must be tracked.

To clarify, an example of a by-product could be
the titanium metal chips that are generated
during a milling or turning operation. At times,
these chips are ignored, but considering
titanium is a precious metal, it is very likely that
the Operator will want to collect them.
The quantity to be produced can range from
zero to the total quantity of each Material. At
runtime, the Operator can specify the actual
quantity produced.

Opcenter Execution Discrete 2507 - Product Overview

21


## Pagina 22

Basic Concepts
Production Environment Configuration

Direction

Material Specification Type

Description

Co-Product

This Material Specification Type is peculiar to
those cases in which you intentionally want
more than one distinct product to be
produced during the execution of the same
Operation (or Step).
The quantity to be produced can range from
zero to the total quantity of each Material. At
runtime, the Operator can specify the actual
quantity produced.

Custom Material Specification Types
System Integrators can create custom Material Specification Types for determining Material consumption/
assembly modalities that differ from those illustrated above and are peculiar to specific needs, focusing
either on the quantity of the Material to be consumed (input) or the quantity of Material to be produced
(output).

The same Material can have one or more Revisions (versions), which are created to permit a differentiation in its use
while maintaining its basic characteristics. For example, one Revision of a Material has been generated for use in a
production plant that produces washing machines, whereas another Revision of the same Material is to be used in
another plant that produces dryers.
It is possible to group Materials specifying a Functional Code, that is, a unique name to define their functionality or
class (for example, "insulation", "electronics", "hardware" and so on). It is also possible to indicate the name of
their Supplier (that is, the external vendor that provides them).

Material Tracking Units
A Material Tracking Unit is an actual item that is consumed or produced during the execution of a Work Order.
Material Tracking Units are instantiated from the abstract Materials.
In our context, there exist two different types of Material Tracking Units, for which a distinction is made on the basis
of how these Material Tracking Units can be identified:
• Batches
• Serial Numbers.
The various system interfaces involving these two Material Tracking Unit types are automatically updated
according to the selected type.
Material Tracking Units can also be identified based on its Barcode and can be consumed by scanning the Barcode.
If anomalies or defects are discovered on existing Material Tracking Units, it is possible to declare NonConformances on them.
During the execution of a Work Order, Material Tracking Units can be consumed manually, with the intervention of
an Operator.

Batches
A Batch is a Material Tracking Unit made up of pieces that are not significant enough to be identified individually.
The entire batch is distinguished by a unique identifier, whereas the single elements making up the batch are not.

22

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 23

Basic Concepts
Production Environment Configuration

For example, a set of bolts does not distinguish each bolt, but just gives their quantity. The identifier is applied to
the set as a whole.
Batches can be both consumed and produced.
Batches to be consumed can be split into smaller quantities. As a result, new Batches are created in the system,
which are uniquely identified and have their own genealogy.
The split can be performed by indicating a specific target quantity to be applied to a single new Material Batch.
Powder Material Batches can also be mixed together to form a Batch having a greater size: for example, if there are
leftover batches of the same Material after consumption at runtime, and you want to combine them to form a single
batch. When two or more Powder Material Batches that identify raw materials are mixed together, a new Raw
Material Batch is created in the system and the two source raw materials are no longer available for consumption.
Likewise, the new Raw Material Batch will have its own genealogy.
You can mix Raw Material Batches only if certain conditions are satisfied. For more information, see also section
Mixing Powder Material Batches of the Opcenter Execution Discrete User Manual.

Serial Numbers
A Serial Number is a Material Tracking Unit that is sufficiently significant to be uniquely identified.
Serial Numbers can be both consumed and produced.
The identifiers applied to Serial Numbers are also called serial numbers.
Serial Numbers are numbered upon their creation.

Material Tracking Unit (MTU) States
State

Description

Available

The MTU is available for production.

Repair

The MTU is undergoing maintenance so that it can return available for use in
the production cycle.

Scrapped

The MTU has been removed from production because it does not satisfy the
minimum standards or it cannot be repaired to a satisfactory degree.

Opcenter Execution Discrete 2507 - Product Overview

23


## Pagina 24

Basic Concepts
Production Environment Configuration

Possible State Transitions for Material Tracking Units (MTUs)
Source Status

Possible Target States

Available

• Repair
• Scrapped

Repair

• Available
• Scrapped

Scrapped

Not applicable.

2.3.6 Containers and Container Types
Containers are specialized Material Tracking Unit Aggregates that are configured to contain or hold and move
Material Tracking Units (be they semi-finished products or MTUs to be consumed) during the production process.
Containers represent physical entities where the MTUs can be loaded. MTUs can also be stored in the Containers,
temporarily, for the time between one production operation and the next. Configurable as reusable, these
Containers can be loaded with MTUs and once the MTUs are unloaded, the empty Containers can be used again.
Containers can be associated to a particular Work Order or made available to any Work Order provided that the
Container is either compatible with the consumed or produced Materials of the Work Order or it is not compatible
with any Materials. Work Order Operations can be executed by associating them with one or more Containers after
loading them with the Material Tracking Units. If configured as reusable, Containers can be reused once the
associated Work Order Operations are completed and the Container is unloaded and ready to be loaded again. For
more information on managing Containers, see Container Management.
Containers can be created by configuring Material Tracking Unit Aggregates with compatible Materials, preloading
the Container with Material Tracking Units and optionally associating the Container to a Work Order.
Alternatively, these configurations can be set in a template and then the template can be used to configure multiple
Containers with the same properties. These templates are called Container Types and configurations such as
Material association and the reusable property can be configured at the Container Type level.
Documents that can be useful to the Operator can also be associated to the Container Type and the Containers
created from these Container Types inherit those documents.
The configurations of the Container Type will be automatically inherited by all the Containers based on the specific
Container Type but, except for documents, they can be changed Container by Container (for example, existing
compatible Materials can be removed and new ones can be linked or the reusable property can be changed).
In Additive Manufacturing contexts, it is possible to define specific Containers (Powder Containers) which can then
be loaded with a single Powder Material Batch, provided that the Batch is not already loaded into a 3D Printer. If
another Batch, belonging to the same Powder, is loaded in the Container, the system performs an automatic
replenishment by mixing the new batch with the existing one, creating a new batch as target. When pre-loading the
Batches, if compatible Materials have been defined, only Batches from compatible Powders can be selected.

Container States

24

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 25

Basic Concepts
Production Environment Configuration

State

Description

Active

The Container has been started at least on one of the associated Work
Order Operations.

Complete

The Container has been completed on all associated Work Order
Operations.

Discarded

The Container, that is flagged as not reusable, has been fully unloaded.

New

The Container has been created.

Pause

The Container has been paused on at least one of the associated Work
Order Operations.

Ready

The Container is available for a new Work Order Operation.

Unloaded

The Container, that is flagged as reusable, has been fully unloaded.

Possible State Transitions for Containers
Source Status

Possible Target States

Active

• Ready
• Pause
• Complete

New

Active

Pause

• Active
• Unloaded

Ready

• Unloaded
• Discarded

Unloaded

Ready (only for reusable Containers)

Complete

• Unloaded
• Discarded

Opcenter Execution Discrete 2507 - Product Overview

25


## Pagina 26

Basic Concepts
Production Environment Configuration

2.3.7 Setpoints
Setpoints are used to drive how a Machine or a Tool must behave at runtime, thereby eliminating the need for shopfloor operators to perform manual adjustments.
On their own, Setpoints are merely empty containers: in order to function, they must be filled with one or more
variables.
For example, if a certain Machine must reach a certain temperature before it can be used in executing a Work Order
Operation, then the Setpoint to be associated to that specific Machine will contain variable "temperature", the
value of which is equal to that specific temperature.
During runtime, the Setpoint variable's value will be transferred to the Machine: the Machine, which is linked to the
Automation Layer, must necessarily reach the temperature specified in the Setpoint before it can be used.
Setpoints can be associated to the following items thus declaring their compatibility:
• Equipment Types and Equipment Configurations
• Tool Definitions and Tools.
If you associate a Setpoint to an Equipment Type or Tool Definition, the same Setpoint will be inherited by all
Machines or Tools generated from the Equipment Type or Tool Definition to which the Setpoint was associated.
For more information, see section "How to Configure Setpoints" in the Opcenter Execution Discrete User Manual.

Setpoint States
State

Description

Edit

A Setpoint is created.

Release

A Setpoint is released.

Obsolete

This state is declared when a Setpoint is invalid.

Possible State Transitions for Setpoints
Source Status

Possible Target States

Edit

• Release
• Obsolete

Release

Obsolete

Obsolete

Not applicable.

26

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 27

Basic Concepts
Production Environment Configuration

2.3.8 Certifications, Human Resources and Skills
Certifications and Skills play an important role in restricting access to sensitive data, while ensuring that only
individuals with the appropriate know-how and who hold a certain position within the organizational hierarchy of a
business perform certain tasks. They work together with Users and Roles in placing limitations on "who" can
perform "what" within your system.

Certifications
A Certification represents an "authorization" that is created ad-hoc with particular characteristics and then assigned
to a User or Role to define the sphere of action within which he/she can operate. Users and Roles can be "certified"
to:
• Perform a certain task (that is, start, pause or complete a specific operation).
• View the details of a certain operation.
• Operate in a certain Workcenter.
• Use a certain machine.
• Produce a certain material.
A Certification can be formed by grouping together:
• One or more Materials
• One or more Equipment Types
• One or more Workcenters
• One or more Skills
• Any combination of the above.
Opcenter EX DS adopts access control through Certifications to simplify the task of keeping tabs on "where" within
a production plant "who" can perform "what" to produce "which" materials using "which" machinery.
Possessing a Certification that is currently valid is essential for a User/Role in order to perform runtime operations:
whenever a Certification is assigned to a User or Role, it must necessarily have an expiration date.
In runtime, the system verifies that the User/Role possesses the appropriate Certifications to determine whether
he/she is certified to do whatever he/she is about to undertake (for example, pause a certain operation, run a
certain type of machinery, or produce a particular material).
In addition, the system checks that the Certification assigned to the User/Role is currently valid: if the Certification
has expired, the User/Role will not be authorized to proceed.
If configured, the system performs further checks in order to verify that the certification is valid for the assigned
Material and/or the Equipment.
In some cases, certain operations require that the User/Role possess a specific Certification: in this case,
the system will verify whether the User/Role possesses this particular Certification, overriding any other
Certifications that he/she may have.

Human Resources
In case of complex or crucial activities that require more users with specific Skills, it is possible to configure Human
Resources to be associated with Process Operations, Process Steps, Work Order Operations and Work Order Steps.
In detail, each Human Resource lists the Certifications required to start a Work Order Operation/Step, specifying
how many users must possess each Certification. If the Human Resource requires that:
• a single Certification is possessed by a single user, any user with the proper certification and skills can start the
related Work Order Operation or Step.
• one or more Certifications are possessed by many users, only teams including a list of users with the proper
Certifications can start the related Work Order Operation or Step.

Opcenter Execution Discrete 2507 - Product Overview

27


## Pagina 28

Basic Concepts
Production Environment Configuration

Skills
A Skill represents a specific requirement that can be associated to Process Operations, Work Order Operations,
Process Steps and/or Work Order Steps, to permit a more granular control on their execution.
Skills are linked to Certifications: by creating Certifications that include one or more specific Skills, it is possible to
allow or deny the execution of specific Process Operations, Work Order Operations and/or Work Order Steps.
Optionally, Skills can have a level, which represents the degree of proficiency required to authorize the operation.
When skill levels are used, it is possible to define if higher levels also include lower levels, or if they are mutually
exclusive.
It is also possible to configure the system behavior when multiple skills are involved in a single Operation: for
example, if all of them are required or just one.

2.3.9 Teams
Teams are groups of Users that can be formed for the purpose of performing production operations together.
While Roles represent a more permanent way to group individuals according to their know-how or position within
the business hierarchy, Teams are flexible and designed to be created "on the fly" and disbanded when no longer
necessary (for example, when two or more operators are needed to perform an assembly operation because the
part is too large to be assembled by one person).
A single Team member can start/pause/complete Work Order Operations on behalf of the entire Team. Each
individual of the group takes responsibility of actions of the other Team members as a collective responsibility.
For more information, see Team management.

2.3.10 Defects, Failures and their related Elements
Although both Defects and Failures, as well as their respective Defect Groups and Sub-Failures, are
available in Opcenter Execution Discrete, it is strongly recommended that you use Failures and SubFailures in all new projects, as Defects and Defect Groups have been deprecated.
The eventuality that the execution of a Work Order might not be flawless and thus produce defective products must
be taken into consideration when configuring your production environment. It must be possible to indicate and
classify any discrepancies and departures from what is expected as the end result of manufacturing activities.
Such discrepancies are classified into two categories, Defects and Failures. You can configure Non-Conformances by
adding a Defect or a Failure.
Defects and Failures represent single flaws in production that are either detected during the execution of a Work
Order or assigned to weak points regarding the quality of the associated Machine, Material Tracking Unit, Tool or
Work Order Operation.
In addition, Failures, Defects and/or Defect Groups can be associated to Machines, Equipment Types, or Materials.
Opcenter Execution Discrete provides pre-defined Defects, which can be modified and deleted. In addition, if you
possess the appropriate rights, you can create custom Defects. Defects can be grouped in Defect Groups, and each
Defect can be assigned to more Defect Groups.
Failures are managed through the Defect App provided by the Opcenter Execution Foundation platform.

Defect Groups and Defect Sub-Groups

28

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 29

Basic Concepts
Production Environment Configuration

Opcenter EX DS comes provided with a catalog of default Defect Groups: provided you possess the appropriate
rights, if you are a Product Engineer, you can expand this catalog to include custom Defect Groups.
For example, Opcenter EX DS provides the following default Defect Groups:
• Product: Represents defects found in the product that is being manufactured.
• Component: Represents defects found in components used as material to be consumed to manufacture the final
product
• Instructions: Represents defects found in the Work Instructions or Documents used to define the end-to-end
manufacturing of the product.
• Tooling: Represents defects found in the Tools used to manufacture the product.
If necessary, these default Defect Groups can be broken down to form a hierarchy of Defect Sub-Groups. Predefined Defect Sub-Groups are provided by default.

Failures and Sub-Failures
Opcenter EX DS does not provide any pre-defined Failures by default. They can be created as standalone Failures or they can be organized into more specific Sub-Failures.

2.3.11 Non-Conformances and Rework Codes
Once production is up and running, it is essential that any problems that may arise during the execution of a Work
Order be notified, analyzed and solved as promptly as possible. This is necessary to ensure that production remains
on the charted course, satisfying the expected levels of quality that are key to success.
To achieve these goals, you must be familiar with:
• Non-Conformances
• Rework Codes.
It is also suggested that you see the basic concepts related to Notification Handling for additional insight.

Non-Conformances
In Opcenter Execution Discrete, production problems are managed by declaring a Non-Conformance. NonConformances are used as key elements in determining whether the production in progress needs to be adjusted
somehow to achieve better performance levels and better end results (that is, a final product of higher quality in
less time).
An individual with the appropriate Role (Production Coordinator) has the task of evaluating (or sentencing) a NonConformance to decide what to do to rectify the situation and, if possible, correct the Defects and
Failures presented therein. It is possible to inhibit the completion of a Work Order if there are unresolved NonConformances on its Operations.
Non-Conformances can be declared even after production has been completed.
The system tracks the history of Non-Conformances, logging all the info about defects, actions, and users involved.
Data can then be analyzed to identify possible production issues and correct them.
Non-Conformances of type Quality can also be declared and sentenced automatically by Machines on a Material
Tracking Unit, the Machine itself, or on a Work Order Operation. For example, a Machine with self-diagnostic
capabilities could detect a fault and automatically declare a Non-Conformance on itself.

Available Non-Conformance Types

Opcenter Execution Discrete 2507 - Product Overview

29


## Pagina 30

Basic Concepts
Production Environment Configuration

Non-Conformance Type

Description

Quality

This type of Non-Conformance is declared when Defects or Failures are
found in either the product that is being manufactured or in the
Machines, Material Tracking Units (both single and aggregate in
Containers) or Tools involved in the production. Quality NonConformances can also be declared and sentenced automatically by
Machines and/or Workcenters. For example, a Machine with selfdiagnostic capabilities could detect a fault and automatically declare a
Non-Conformance on itself.

Change (also referred to as Change
Requests)

A Change Request is declared when something needs to be changed in
the production workflow.
For example, the Work Order Operation needs a different Tool that what
was previously foreseen, because the Material used is particularly rigid.
At this point, by opening a Change Request, it is possible to notify the
appropriate figure (Production Coordinator or Product Engineer) that a
change must be made to the Work Order Operation's resources on-thefly. This can also involve adding Work Instructions and/or Operations. In
this case, the Non-Conformance can be linked to an entire Work Order
Operation or only to a specific Serial Number produced by it.

States and Lifecycles of Non-Conformances and Requests
The Lifecycle of a Non-Conformance or a Request represents the states that the Non-Conformance/Request
assumes because of the activities or tasks performed on it from creation, resolution, and finally, to completion. For
example, declaring a Non-Conformance results in setting the state of the Non-Conformance to Open, while the
decision to scrap a Work Order might set the Non-Conformance to Scrap. Whenever a Non-Conformance is set to
Scrap, it is possible to automatically close all the Non-Conformances associated with the source entity, by setting
an appropriate configuration key. The available states depend on the type of source entity.
The declaration of a Non-Conformance has an impact on how Work Order Operations will progress during the
execution of a Work Order. Depending on how the Production Coordinator decides to handle (that is, sentence) the
Non-Conformance, the path followed in the execution of the Work Order is determined.
Opcenter EX DS provides the following product lifecycles:
• for Quality Non-Conformances:
• QUALITY WORKFLOW: associated to Work Order Operations.
• QUALITY ITEM WORKFLOW: associated to Machines, Tools and Material Tracking Units/Containers.
• DefectWF: associated to Material Tracking Units.
Custom Non-Conformance Lifecycles
Quality Non-Conformances can also have custom Non-Conformance Lifecycles, according to the user's
needs. Once the required business logic is implemented and the custom Non-Conformance Lifecycle has
been configured with its states, behaviors and transitions, it will be handled by the system in the same
manner as the default Non-Conformance Lifecycles.
For more information, see How to Configure Custom Non-Conformance Lifecycles in the Opcenter Execution
Discrete User Manual.
• for Change Requests:
• WORKFLOW FOR CHANGE MGT: for Non-Conformances of type Change.

30

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 31

Basic Concepts
Production Environment Configuration

QUALITY WORKFLOW States
State

Description

Open

The Quality Non-Conformance has been declared.

Scrap

The Quality Non-Conformance has caused the Work Order to be
scrapped.

Rework

The Quality Non-Conformance has caused the Work Order to
require reworking.

Concession

The Quality Non-Conformance requires approval from the Product
Engineer in order to execute the Work Order differently from the
Process created by the Product Engineer.

Close and Return to Work

The Quality Non-Conformance has been closed and the Operator
can return to performing his tasks.

Set WKC Hold

The Quality Non-Conformance blocks the Workcenter/Machine on
which the Work Order Operation is being executed.

Pending

The request for approval from the Product Engineer in order to
allow for deviations to the Process is pending.

Accept

The request for approval from the Product Engineer in order to
allow for deviations to the Process has been accepted.

Rejected

The request for approval from the Product Engineer in order to
allow for deviations to the Process has been rejected.

Notified-Engineering-Issue

(Only for integration with PLM systems) The PLM system has
confirmed the reception of the Quality Non-Conformance.

Possible State Transitions for QUALITY WORKFLOW
Source Status

Possible Target States

Open

• Close and Return to Work
• Rework
• Concession
• Notified-Engineering-Issue
• Scrap
• Set WKC Hold

Opcenter Execution Discrete 2507 - Product Overview

31


## Pagina 32

Basic Concepts
Production Environment Configuration

Source Status

Possible Target States

Scrap

Not applicable.

Rework

Not applicable.

Concession

• Accept
• Pending

Close and Return to Work

Not applicable.

Set WKC Hold

Not applicable.

Pending

• Rejected
• Accept

Accept

Not applicable.

Rejected

Not applicable.

Notified-Engineering-Issue

Open

DefectWF States
State

Description

Open

• The Defect has been opened.
• The Defect has been re-opened because the issue has not been
solved.

Cancelled

The Defect has been cancelled because it was opened by mistake.

Fixed

The Defect has been fixed.

Certified

The Defect has been certified.

Possible State Transitions for DefectWF
Source Status

Possible Target States

Open

Cancelled

32

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 33

Basic Concepts
Production Environment Configuration

Source Status

Possible Target States

Open

Fixed

Fixed

Open

Open

Certified

Fixed

Certified

QUALITY ITEM WORKFLOW States
State

Description

Open

The Quality Non-Conformance has been declared.

Scrap

The Quality Non-Conformance has caused the Item to be
scrapped.

Rework

The Quality Non-Conformance has caused the Item to require
reworking.

Repair

The Quality Non-Conformance has caused the Item to be
repaired.

Close and Return to Work

The Quality Non-Conformance has been closed and the Operator
can return to performing his/her tasks.

Possible State Transitions for QUALITY ITEM WORKFLOW
Source Status

Possible Target States

Open

• Repair
• Scrap
• Rework
• Close and Return to Work

Scrap

Not applicable.

Rework

Not applicable.

Repair

• Close and Return to Work
• Scrap

Opcenter Execution Discrete 2507 - Product Overview

33


## Pagina 34

Basic Concepts
Production Environment Configuration

Source Status

Possible Target States

Close and Return to Work

Not applicable.

WORKFLOW FOR CHANGE MGT States
State

Description

Open

The Change Request has been opened.

Rejected

The Change Request has been rejected.

Close

The Change Request has been closed.

Possible State Transitions for WORKFLOW FOR CHANGE MGT
Source Status

Possible Target States

Open

• Close
• Rejected

Rejected

Not applicable.

Close

Not applicable.

Rework Codes
With appropriate configuration, it is also possible for the system itself to suggest one or more Rework Processes to
be performed in response to a specific Defect (or Defect Group) or a Failure (or Sub-Failures) contained in a NonConformance that has been declared.
These suggested operations are known as Rework Codes. Rework Codes represent an association involving a
Process, which has been defined to rework an item, a Defect (or a group of Defects) or a Failure (or Sub-Failures)
and a Final Material: thanks to this association, whenever a Non-Conformance is declared in the presence of a
certain Defect or a Failure during the execution of a certain Work Order Operation to produce a certain Final
Material, the system will present a set of the most appropriate Rework Codes from which to choose to rectify the
Defect or Failure. At this point, the Process associated to the selected Rework Code will be executed to correct the
Defect and allow the production process to move on to produce the desired Final Material.

A Practical Example
In a factory that produces washing machines, during the execution of a certain Work Order, an Operator in the
assembly area detects a Defect (for example, "part does not fit in lodging"). Ideally, more than one Defect can be
grouped together to form a Non-Conformance.
The Operator opens a Non-Conformance, specifying the Defect(s) found and providing any additional information
(a document such as a photo of the part and the lodging into which it must be inserted) in attachment to assist the
Production Coordinator in evaluating the situation (that is, sentencing the Non-Conformance).

34

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 35

Basic Concepts
Production Environment Configuration

An alert informs the Production Coordinator that there is a Non-Conformance to be dealt with in regard to the
specific Work Order.
The Production Coordinator then accesses the Non-Conformance and, after examining its details and any
documents in attachment, sentences the Non-Conformance. If Rework Codes have been defined for the Defect
encountered, they will be presented to the Production Coordinator for selection to rectify the Defect in question.

2.3.12 Work Operations
Work Operations serve the purpose of establishing how the Work Order Operations will behave during runtime.
For example, you can determine that a Work Order Operation:
• Be automatically completed after it has been started by an Operator.
• Be automatically started after the preceding Work Order Operation has been completed with success.
Work Operations can be used together with Dependencies on Work Order Operations to drive the automatic Start/
Complete of successive Work Order Operations. For example, if Work Order Operation "A" has Work Order
Operation "B" as a dependent and the Work Operation associated to Work Order Operation "A" is related to AutoStart and Work Order Operation "B" has Auto-Start as its Dependency Type, when Work Order Operation "A"
starts, then Work Order Operation "B" will be started automatically.
The product comes provided with a set of predefined Work Operations, dedicated to particular types of frequent
operations which can be performed during the production process.
Additional Work Operations can be created in two ways before you configure your production processes:
• From scratch.
• By making a copy of an existing Work Operation and then customizing it.
Modifications can be made to any Work Operation, provided that it is not currently associated to a Work Order
Operation which is in the Active state.

2.3.13 Operation/Step Categories
In particular contexts, Operation/Step Categories represent a more immediate way for both the system and users to
identify the purpose for which a Process Operation (or Process Step, Work Order Operation, Work Order Step) is to
be performed.
This manner of grouping the aforementioned entities by "purpose" is adopted primarily to facilitate creating a
synergy between the product's business logic and custom business process flows provided by the Customer. Once
this synergy is established, the system will automatically launch the Customer's custom business process flows
whenever the Operations/Steps are run during the execution.
All Process Operations (as well as all Process Steps, Work Order Operations and Work Order Steps) necessarily
belong to an Operation/Step Category: if no value is entered to indicate a specific Operation/Step Category, the
entity being configured will automatically be assigned with the default Operation/Step Category provided by the
system.
Here are some examples of Operation/Step Categories:
• Quality
• Assembly
• Manufacturing
• Movement
• Traceability
• Screwing
• Open Protocol

Opcenter Execution Discrete 2507 - Product Overview

35


## Pagina 36

Basic Concepts
Production Environment Configuration

• Generic Data Collection.

2.3.14 Work Instruction Definitions
In modern manufacturing processes, it is essential that precise and up-to-date information (for example,
instructions on how to handle a particular material; a checklist specifying all the tools involved in executing a
certain process; a video showing how to perform a certain step manually) be readily available to operators. In the
past, paper-based documentation was used, but this was not an optimal solution.
Likewise, data collection may be required to satisfy a variety of needs present in a production plant. For example,
data collection may be necessary to obtain concrete elements for:
• Evaluating production re-organization.
• Testing purposes.
In Opcenter Execution Discrete, a Work Instruction Definition is an abstract representation of a specific Work
Instruction (for example, "Instructions for measuring finished-product thickness").
It may consist in text outlining a step-by-step procedure and/or data-collection sections into which measurements
and values are to be entered during runtime. therefore, these entities satisfy the need to provide Operators with
guidance in performing their job, while permitting data collection at the same time.
For more information, see Readily-Available Work Instructions and Documents.

2.3.15 Interlocking Checks
The start and completion of a Work Order Operation's (or Work Order Step's) execution can be governed by the
outcome of the Interlocking Checks enabled for it.
Interlocking Checks verify whether one or more conditions have been satisfied in full in relation to the Work Order
Operation or Work Order Step in question: if the outcome of all these checks is successful, the execution of the Work
Order Operation or Work Order Step will either be started (Inbound Interlocking Checks satisfied) or
completed (Outbound Interlocking Checks satisfied).
Certain Interlocking Checks can be considered both Inbound and Outbound.
The various Interlocking Checks enabled on a specific Work Order Operation or Work Order Step are handled by two
dedicated Orchestrators, commands that read which Outbound Interlocking Checks and Inbound Interlocking
Checks have been enabled, respectively. The Orchestrators execute their enabled Interlocking Checks in parallel
and wait for their completion. The outcome of each Interlocking Check is then traced.
If the Work Order Operation on which Interlocking Checks have been enabled contains Work Order Steps, if
necessary, all the Interlocking Checks will be performed on both the Work Order Operation and its Work Order
Steps: these checks must be satisfied on the whole in order for the Work Order Operation's execution to be started
or completed.
Interlocking Checks are triggered automatically (that is, when the Work Order Operation or Work Order Step is to be
started or completed automatically) prior to the start (or completion).
Interlocking Checks can also be triggered via the usage of Operation/Step Categories: if no Interlocking Checks are
associated to a Work Order Operation or Work Order Step, but the Work Order Operation (or Work Order Step itself)
has been classified with an Operation/Step Category, to which Interlocking Checks are linked, then the execution of
the Interlocking Checks will be triggered upon start or completion.

Standard Interlocking Checks
Outbound

36

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 37

Basic Concepts
Production Environment Configuration

• DocumentsUploaded: Verifies how many documents have been uploaded in relation to the current Work Order
Operation as a whole (that is, in relation to the Work Order Operation and its Work Order Steps, if present).
• AllPartsAssembled: Verifies that all components have been assembled on the Work Order Operation (as well as
on its Work Order Steps, where present), according to the Material Specifications or BoMs.
• AllStepsCompleted: Verifies that all the Steps belonging to the active Work Order Operation have been
completed.
For more details on each Interlocking Check, see the Opcenter Execution Discrete User Manual.

Custom Interlocking Checks
In Opcenter Execution Discrete, users can implement custom Inbound and Outbound Interlocking Checks,
according to their needs: for more information, see Interlocking Checks for Governing Work Order Operation
Execution. Once the required business logic is implemented and the custom Interlocking Check is configured, it will
be handled by the system in the same manner as a standard Interlocking Check.
For more information on how to implement the business logic of a custom Interlocking Check, see section
How to Develop Custom Interlocking Checks of the Opcenter Execution Discrete Extensibility Guide.
For more information on how to create a Custom Interlocking Check in Opcenter Execution Discrete and
use it during production execution, see section Configuring Custom Interlocking Checks of the Opcenter
Execution Discrete User Manual.

2.3.16 Line Side Positions
When a production item is produced, a list of Materials, represented by the Bill of Materials, is used to produce the
final product.
Line Side Positions are abstract representations of specific areas or accessories (for example racks) allocated to
store Materials in one or more Equipment within the manufacturing environment, in order to constitute what can
be called a Line Side Inventory.
Line Side Positions can be managed either automatically or manually by an Operator at runtime. They can be
configured specifying the initial quantity and the maximum capacity allowed and, in case of automatically
managed Line Side Positions, associated with thresholds to set target quantities and priorities for replenishment.
Line Side Positions are made up of sub-locations called Bins, which contain defined quantities of a certain Material
and which are used to replenish Line Side Positions.
Each Line Side Position links a piece of Equipment (either Workcenter or Unit) to a Material, so that it is possible to
configure where the Material must be consumed and how much of that Material must be consumed in each piece of
Equipment.
More specifically, when an operation is completed on a given Equipment at runtime, the quantity of the Line Side
Position is decreased according to the intersection between Materials with the AutoConsume Material
Specification Type, and those associated to the Line Side Position.
When the Threshold reaches or falls below the configured value, a Kanban Call is sent to the Warehouse to request a
replenishment, using a Kanban Output Message.

2.3.17 Bills of Features and their related Elements
A Bill of Features is used to establish which specific characteristics must be present in a product that you intend to
manufacture. It represents the sum of all those characteristics that are deemed essential, as well as all possible
variations available for its optional characteristics, if present.
Bills of Features are made up of:

Opcenter Execution Discrete 2507 - Product Overview

37


## Pagina 38

Basic Concepts
Production Environment Configuration

• Features, which specify a set of mandatory characteristics that the product must possess and for which it is
necessary to define a value.
• Feature Values, which can be associated to Features to better customize the product according to your needs.
• Options, which specify a set of optional characteristics of the product and which can be selected or not.
All of these elements concur to what is known as High Variance production. In this particular type of production, it is
possible to customize your end product (car, washer, etc.) to reflect your specific needs moving from a basic
framework to which you apply different characteristics.
Once defined, Bills of Features can be associated to Product Configurations, to better categorize the product to be
produced on the basis of the ERP Order details.

Examples
For the Bill of Features, in an automotive scenario, you can define:
• Feature Color, which can have the following values: green or red.
• Feature Engine, which can have the following values: gasoline or diesel.
In different production contexts, the same item can be designed either as a Feature or as an Option. For example,
Roof:
• you can define the Roof as a Feature with two values: open or closed.
• you can define the Open Roof as an Option to be added or not.

2.3.18 Product Configuration
Product Configurations are necessary to customize the production on the basis of the ERP Order details. Each
Product Configuration can be associated with a Final Product Type and related Final Product Family, to better
categorize the outputs of a given production line.
Once created, Product Configurations are empty containers which can then be associated with the following
structures, depending on the product which must be produced:
• Bills of Features, made up of Features, Feature Values and Options.
• Bills of Materials, made up of the Materials necessary to produce the Final Product Type associated with the
Product Configuration.
For examples, in those cases where the final target of the production is a Vehicle, you will need both Bill of Features
and Bill of Materials to design the product in every detail, while if the final product is a Bumper only the Bill of
Materials is necessary, in order to define which Materials are needed.
For more information on functionalities regarding Product Configurations, see Product Configuration Management.

2.3.19 Qualification Criteria
Qualification Criteria represent a set of rules that can be set for the Process Operations belonging to the Master Plan
from which the Work Order is created.
The adoption of Qualification Criteria in the production environment makes it possible to select from a Master Plan
only those Operations associated to valid Qualification Criteria and thus deemed necessary to correctly execute a
specific Work Order at runtime.
Likewise, Qualification Criteria can be set for:
• Material Specifications
• Inspection Specifications
• Setpoint Variables
• Tool Specifications

38

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 39

Basic Concepts
Production Environment Configuration

• Operation Folders
to filter out those elements that are appropriate for the Work Order's execution.
Once created, Qualification Criteria are empty containers for which rules must be configured. The product comes
provided with a set of predefined entities and respective properties, which are used to define filter clauses, to
create the final rule which must be validated. Furthermore, different Qualification Criteria can be combined, to
produce complex rules.
If necessary, expert users can extend the entities provided for defining filter clauses to satisfy specific needs.
Qualification Criteria can also be used in conjunction with the Production Flow Control Diagram, thanks to a
dedicated Check.
Qualification Criteria can be validated thanks to a dedicated service known as Production Resolution common
component, already included in the Opcenter EX DS setup, and for which few additional configurations must be
performed. The Production Resolution applies a specific business logic to validate the rules.
The entities and respective properties involved in the configuration of Qualification Criteria rules are:
Entity

Property

Qualification Criteria

Id (to produce complex rules)

ERP Order

• Id
• Name
• Final Product Type
• Final Product Family
• Serial Number
• Customer Type
• Sequence

Work Order

• Final Product
• Plant
• Priority
• Due Date
• Creation Date

Material

Functional Code

Material Tracking Unit

• Id
• Serial Number
• Line Sequence
• Final Product Type

Bill of Materials: represents the Bill of Materials linked to
either the ERP Order or Material Tracking Unit.

Material

Bill of Features (Work Order): represents the Bill of Features
linked to the Work Order.

Feature

Opcenter Execution Discrete 2507 - Product Overview

39


## Pagina 40

Basic Concepts
Production Environment Configuration

Entity

Property

Bill of Features (Production Item): represents the Bill of
Features linked to either the ERP Order or Material Tracking
Unit.

Feature

Example
Qualification Criteria Identifier: Open Roof
Master Plan A:
• Operation 1: Install Open Roof
• Qualification Criteria Open Roof = True
• Operation 2: Install Closed Roof
• Qualification Criteria Open Roof = False
The Work Order will contain only Operation 1.

2.3.20 Production Flow Control
Each product to be produced must undergo a specific Production Flow Control. This means going through a set of
predefined business Milestones, relevant to a specific plant and logically connected through Transitions. An
example could be: a Vehicle body painting or its assembly.
Each Transition must go from a source status to a target status and, for this purpose, each Milestone can be
associated with a series of:
• Checks: specifying preliminary conditions that must be satisfied to allow the MTU to enter a Milestone.
• Attributes: representing the business logic to be executed once the MTU enters a Milestone.
• Actions: defining non-transactional operations to be executed after the MTU has completed the transition from
a Milestone to the following one.
Checks, Attributes and Actions must be successfully completed, otherwise the Milestone cannot be declared.
The product releases a set of predefined Checks, Attributes and Actions listed in the table below. If necessary,
expert users can configure custom Milestone Activities to satisfy any needs your production may have, provided
that the appropriate business logic is applied. For additional information on how to implement custom Milestone
Activities, refer to the How to Implement Custom Checks, Attributes, or Actions page in the Opcenter Execution
Discrete Extensibility Guide.
Production Flow Controls are associated with Material Tracking Units through the Final Product Type. You can
define two Production Flow Controls for each Final Product Type, but only one at a time can be set to active. The
possibility of configuring a second Production Flow Control permits defining a new set of Transitions in case
changes are needed, without stopping those currently active. As soon as the new Production Flow Control is set to
active, the previous one is invalidated.
For more information on functionalities regarding Production Flow Control, see Production Flow Control
Management.

Production Flow Control Business Logic

40

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 41

Basic Concepts
Production Environment Configuration

Milestone Activity

Name/Description

Check

• HAS_OPEN_ISSUES: checks the presence, for a specific MTU, of not
executed or not successfully completed Operations, or of open NonConformances.
• HAS_NO_OPEN_ISSUES: checks, for a specific MTU, that all the
Operations have been executed and successfully completed and that
all the Non-Conformances are closed.
• EVALUATE_QC: before the MTU reaches the Milestone, verifies that
all the Qualification Criteria previously defined are valid in relation
to the characteristics of the current production item.

Attribute

For the complete list of Attributes and their detailed description, refer to
the Milestone Attributes page.

Action

SEND_MESSAGES: specific to the Output Message functionality.
Released Message Definitions can be associated with a Milestone, so
that the Message will be automatically generated and sent as soon as
the MTU to be produced reaches that Milestone at runtime.

Example
The production process can be configured as follows: a Vehicle is allowed to enter a specific Production Line only
after the system verifies that there are no open defects from the previous Production Line (Check). After entering
the new line, the required transactional operations (Attributes) are performed, for example the assignment of a
serial number to the Vehicle. When all Attributes are completed, the status of the Vehicle changes and the specific
non-transactional operations previously configured (Actions) are triggered: in this case, as soon as the Vehicle
enters the Milestone, a message for a Material call is sent to the Warehouse.

2.3.20.1 Milestone Attributes
Milestone Attributes represent transactional operations that are executed when a Material Tracking Unit enters a
Milestone, after the preliminary Checks have been performed and successfully completed.
Milestone Attributes are connected to the start, progress and completion of an ERP Order associated with an MTU,
because if the outcome of each transaction is successful, the ERP Order transitions from one state to another.
The product releases a set of predefined Attributes, each with its own business logic, which are described in detail
below:

Available Milestone Attributes

Opcenter Execution Discrete 2507 - Product Overview

41


## Pagina 42

Basic Concepts
Production Environment Configuration

Attribute

Description

INITIAL

Creates an MTU with the same Final Product Type and Production Line of
the Production Flow Control Diagram with which the Milestone is
associated. The Material selected is the same of the Final Product Type.

CONTINUE

Makes it possible to use a Diagram even if an MTU already exists (created
manually or coming from external systems). Permits also the continuation
of the production flow even if the switch to a second Diagram takes place,
provided that both Diagrams are associated with the same Final Product
Type. It must be associated with the first Milestone of a Diagram.

LINKERP

Links the MTU to a compatible ERP Order which, as a result, transitions
from SCH to LNK, if the following preliminary conditions are satisfied:
• the Final Product Type associated with the MTU is the same of the
corresponding ERP Order.
• the ERP Order status is SCH. The system automatically selects the first
ERP Order in SCH status, choosing among the following parameters in
ascending order: Sequence, Production Date, Delivery Date, Customer
Type.

ASSIGN_SN

Generates a Vehicle Identification Number (VIN), which corresponds to the
serial number of the associated ERP Order.
The following preliminary conditions must be satisfied:
• the ERP Order status is LNK.
• the MTU is linked to the ERP Order.

CALCULATE_LS

Calculates a Line Sequence to be assigned to the MTU, to identify the Final
Product Type in the production line, according to the order in which the
MTU enters this production line.
The following preliminary conditions must be satisfied:
• the ERP Order status is LNK.
• the MTU is linked to the ERP Order.

FREEZE_STRUCTURES

Freezes the Bill of Materials and Bill of Features associated with the MTU,
so that they can no longer be modified.
The following preliminary conditions must be satisfied:
• the ERP Order status is LNK.
• the MTU is linked to the ERP Order.

42

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 43

Basic Concepts
Production Environment Configuration

Attribute

Description

SET_PRODUCTION

Triggers the execution of the main production phase, causing the
transition of the ERP Order from LNK to PRD after the aforementioned
operations have been completed:
The following preliminary conditions must be satisfied:
• the ERP Order status is LNK.
• the MTU is linked to the ERP Order.

START_EXEC

The functionalities previously managed by
START_EXEC_ON_FULL_MP are now managed solely by
START_EXEC.
According to the Execution Type selected for the Final Product Type,
creates and releases a Work Order in Active state with:
• Operations with valid Qualification Criteria.
• Materials that are compatible with the valid Bill of Materials associated
with the ERP Order.
The Operations must belong to the Master Plan associated with the ERP
Order:
• If no Master Plan is associated with the ERP Order, the system selects
the Master Plan defined at Final Product Type level.
• In general, the system selects the most recent updated Master Plan
(attribute: LastUpdatedOn) among those that have been completed.
The following preliminary conditions must be satisfied:
• the Execution Type associated with the Final Product Type is Master
Plan On Qualification Criteria.
• the ERP Order status is PRD.
• the MTU is linked to the ERP Order.

COMPLETE_EXEC

Triggers the completion of the Work Order.
A Work Order exists in the system and it has already transitioned through
the Milestone associated with the START_EXEC attribute.

COMPLETE

Triggers the completion of the ERP Order, making it transition from PRD to
CMP.
The following preliminary conditions must be satisfied:
• the ERP Order status is PRD.
• the MTU is linked to ERP Order.

Opcenter Execution Discrete 2507 - Product Overview

43


## Pagina 44

Basic Concepts
Production Environment Configuration in Additive Manufacturing

Attribute

Description

DELIVER

Triggers the delivery of the ERP Order which transitions from CMP to DLV
and is no more in charge of production.
The following preliminary conditions must be satisfied:
• the ERP Order status is CMP.
• the MTU is linked to the ERP Order.

2.3.21 Quality Gates
During production execution, it is crucial to monitor the quality of products being manufactured and promptly fix
potential unresolved issues that may arise. For this purpose, Opcenter Execution Discrete gives you the possibility
of defining a catalog of Quality Gates which, once created, can be associated with one or more Work Centers and
Units thus designated as Quality Gates.
To monitor the quality of products and to perform the corrective actions at runtime, Quality Gates can then be
associated with one or more Equipment Types, according to your needs, more specifically:
• Work Centers
• Units
Quality Gates can be configured as production blocking points and with the capability of repairing failed Activities.
For more information, see Quality Gate Management.

2.4 Production Environment Configuration in Additive
Manufacturing
Unlike subtractive manufacturing methods that start with a solid block of material and then use a machine (like a
drill or a lathe) to cut away the excess to create a finished part, Additive Manufacturing (also known as 3D
Printing) builds a three-dimensional object by creating a series of layers of material over a base.
This type of production is computer-driven, as the geometry of the object to be produced, as well as the
instructions that drive the 3D printing machines involved, are stored in dedicated files.
The powders used as source materials (typically, metal powders, plastic, concrete) in Additive Manufacturing often
can be recycled and/or mixed together to form new batches for subsequent use: the genealogy of the resulting
batches is tracked by the system and can be viewed.
The main entities involved in Additive Manufacturing are:
• Print Job Files
• Substrates
• Powder Materials
• Powder Material Batches

2.4.1 Print Job Files
Print Job Files contain detailed information that is used by a 3D printer to create a specific product by means of
Additive Manufacturing processes. Such content includes the geometry of the object to be produced and the
instructions that drive the 3D printing machine. These files are typically generated in a dedicated system (CAM), and

44

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 45

Basic Concepts
Production Environment Configuration in Additive Manufacturing

their metadata can also be either imported from that system or manually created within Opcenter EX DS. They are
specific for a printer brand and model or for a printer type.
Interaction with 3D printers is managed through custom plugins that can be created by system integrators. For
information on plugins and other functionalities related to Print Job File usage, see Print Job File management.

2.4.2 Substrates
A Substrate is a build plate that functions as the base of the object that is being produced in Additive Manufacturing
contexts. The material (typically, metal powder, concrete, plastic) is distributed, layer by layer, over the Substrate.
These layers gradually build up to form a 3-dimensional final product.
In Opcenter Execution Discrete, Substrates are considered as a specialized type of Tool. Like Tools, they may need
to undergo maintenance or be subjected to specific treatment so that they can be used in the best possible
condition.
Factors such as the minimum thickness of a Substrate or the number of treatments that it has undergone have
significant impact on the state assumed by a Substrate, as well as on whether it can be used in production. For
more information, see Substrate management.

Substrate States
State

Description

Available

The Substrate is available for production.

Busy

The Substrate is currently used in a Work Order Operation.

WarningAvailable

The current thickness value of the Substrate has fallen below Min
Thickness Warning or the current treatment count value has risen
above Max Treatment Count Warning. The Substrate is still
available for production, but with a warning.

Maintenance

The Substrate is undergoing maintenance activities, and hence, is not
available for production.

OnHold

The Substrate is modified, and its current thickness value has fallen
below Min Thickness Hold or the current treatment count value has
risen above Max Treatment Count Hold. The Substrate is not
available for production.

Possible State Transitions for Substrates
Source Status

Possible Target States

Available

• OnHold
• WarningAvailable

Opcenter Execution Discrete 2507 - Product Overview

45


## Pagina 46

Basic Concepts
Production Environment Configuration in Additive Manufacturing

Source Status

Possible Target States

Busy

• Available
• WarningAvailable

WarningAvailable

OnHold

Maintenance

• Available
• WarningAvailable
• OnHold

OnHold

Not Applicable

Any state transition is possible from the UI while performing a Maintenance activity.

2.4.3 Powder Materials and Powder Material Batches
A Powder Material is a particular type of Material that is used in Additive Manufacturing contexts and requires
specific configuration.
Powder Materials can be associated to Process Operations, Work Order Operations and Execution Group Phases to
specify which Powder must be loaded into the associated 3D Printers and they can also be used to specify that
traceability into the product genealogy is required.
At runtime, Powder Material Batches are instantiated from Powder Materials and represent the actual raw material
to be used in a 3D printing operation.
A recycling operation ensures that:
• Leftover powder material from multiple batches is collected.
• Actions (for example, sieving) performed on the powder material make it reusable for production.
Powder Material Batches can also be mixed to form a new batch or to refill an existing one, provided that certain
conditions are satisfied. The resulting batch, the history of which is traced in a dedicated genealogy page, is then
associated with a new 3D printing operation.
It is possible to declare Non-Conformances on Powder Material Batches if anomalies or defects are discovered.
For more information on functionalities related to Powder Material Batches, see Powder Batch Management.

Powder Material Batch States
State

Description

Available

The Powder Material Batch is available for production.

46

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 47

Basic Concepts
Production Environment Configuration in Additive Manufacturing

State

Description

Busy

The Powder Material Batch, loaded into a 3D printer, is being used in a 3D
printing operation (no actions, for example mixing or recycling, can be
performed on it), and its quantity is greater than Minimum Quantity
Threshold. Once the print is finished, the Powder Batch status is
automatically changed by the system.

Mixable

The Powder Material Batch has been recycled, and its quantity is still less
than Minimum Quantity Threshold. It must be mixed with another Powder
Material Batch in order to be used in production.

Quarantine

The Powder Material Batch is in use. It is loaded into a 3D Printer, but its
quantity has reached Minimum Quantity Threshold. It must be recycled
before it can be mixed again.

Spent

A Powder Material Batch in this state is not available for production. It could
be in this state because:
• It is mixed with another Powder Material Batch, and its quantity is 0.
• It has reached the recycle threshold.

Consumed

A Powder Material Batch in this state is not available for production. It has
been used in a 3D printing operation ad its quantity is 0.

Possible State Transitions for Powder Material Batches
Source Status

Possible Target States

Available

• Busy
• Quarantine
• Spent
• Consumed

Busy

• Quarantine
• Available
• Spent

Mixable

• Spent (Deprecated)
• Quarantine

Quarantine

• Spent
• Mixable
• Available

Opcenter Execution Discrete 2507 - Product Overview

47


## Pagina 48

Basic Concepts
Production Process Configuration

Source Status
Spent

Possible Target States
• Available
• Quarantine
• Spent

2.5 Production Process Configuration
The list of basic concepts provided below is valid for standard production processes. If your production
process involves Additive Manufacturing, see Production Environment Configuration in Additive
Manufacturing for those basic concepts specific to this context.
Here are the basic concepts for configuring your production processes:
• As Planned BOPs, Master Plans, Processes, Operations and Steps
• Alternative Process Operations
• Sequences and Dependencies
• Catalogs
• Items associable to Operations:
• Machines
• Materials
• Tools
• Documents
• Work Instructions
• Skills
• Interlocking Checks
• Quality Inspections
• Human Resources
• Qualification Criteria
• Powders
• Items associable to Steps:
• Materials
• Tools
• Documents
• Work Instructions
• Skills
• Interlocking Checks
• Quality Inspections
• Human Resources

2.5.1 As Planned BOPs, Master Plans, Processes, Operations and Steps
The framework for all production engineering is based on Processes and how they are sequenced. A Process is an
abstract representation of the sequence of operations and steps involved in producing a specific Product.
Processes are a high-level outline that illustrate how to proceed in order to execute a specific manufacturing
activity.
Each runtime instantiation of a Process is referred to as a Work Order.

48

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 49

Basic Concepts
Production Process Configuration

The final materials to be produced, as well as the plant or site where the Process will be instantiated, can be
specified when the Process is created. In alternative, it is possible to create generic Processes valid for multiple
actual productions: in this case, the final materials and/or the production plant will be specified when the Work
Orders will be instantiated.
In addition to instantiating a Process, there are other ways to create a Work Order: for more information,
see Versatile Work Order Management.
The following elements contribute to forming a single Process and are listed hierarchically (top-down):
• Sub-Processes (optional)
• Process Operations
• Process Steps (optional)
Through the use of dedicated Catalogs, it is possible to reutilize Processes, Operations and/or Steps when
configuring your production activity.
It is possible to modify a Process, making changes as needed: the end result is a Revision of the original Process.
Documents can be linked to As Planned BOPs and Master Plans.
Data Segregation Propagation
If an As Planned BoP has a Data Segregation tag associated to the Final Material then, when the As Planned
BoP is completed, the Data Segregation tag is automatically propagated both to the BoP and to the
Documents/Work Instructions associated to it.
In this manner, solely the user associated to the same Data Segregation tag can view both the segregated
BoP and the Documents/Work Instructions associated to the BoP Operations in the system.
If new Documents or Work Instructions must be associated to the BoP at a later time, for example after the
BoP has been completed, thanks to a dedicated button in the user interface it is possible to automatically
propagate the Data Segregation tag to the newly added Documents and Work Instructions.

As Planned BOPs
All Processes involved in your production activity are contained inside what is known as an As Planned BOP: its
contents are whatever concurs to manufacturing the product to which the Processes refer. In detail, all Processes
and their sub-elements (for example, the materials to be consumed) that are involved in the specific production
activity that will be executed are contained inside the As Planned BOP.
Here is an example of the complete structure of an As Planned BOP, in which all optional elements have been
included:

Opcenter Execution Discrete 2507 - Product Overview

49


## Pagina 50

Basic Concepts
Production Process Configuration

The following example illustrates the complete structure of another As Planned BOP, which consists in a single
Process in which there are no Sub-Processes and only two of its Process Operations are made up of Process Steps:

Master Plans
A Master Plan presents characteristics similar to an As Planned BOP, in that it is a structure that, when filled with
appropriate data, is to be used to generate a specific Work Order. Like an As Planned BOP, it can be also imported
from Teamcenter. The difference lies in that:
• As Planned BOPs contain the specific structure, as well as the exact combination of data to be used to generate
a specific Work Order for producing a specific product.
For example, As Planned BOP "XYZ Washing Machine, Energy-Saving Model 1" provides the exact specifications
for producing that particular product.
• Master Plans contain the structure and all the possible combinations of data for producing a generic product.
For example, Master Plan "Washing Machine" provides a generic structure appropriate for a washing machine
and all the possible combinations of data that can determine whether the washing machine to be produced
belongs to one model or another. From the Master Plan, by appropriately filtering the data according to the
Work Order's required list of parts/BoM to produce a certain product, you will generate a Work Order that
satisfies your needs.

50

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 51

Basic Concepts
Production Process Configuration

In the image below, two Work Orders are instantiated from the same Master Plan, but not all Work Order Operations
are included in both Work Orders. To differentiate the type of product (for example, the type of Washing Machine to
be produced) Work Order 1 will only use Operation 10 and Operation 30, while Work Order 2 will use Operation 20
and Operation 40.

Sub-Processes
In the case of complex production activities, it may be necessary to break down a Process into a number of SubProcesses.
Sub-Processes and Process Operations cannot coexist on the same hierarchical level: Processes can be
formed only by either Process Operations directly or by Sub-Processes that are formed by Process
Operations.
Sub-Processes are made up of Process Operations, which, in turn and depending on their complexity, may be
formed by a series of Process Steps.
It is possible to modify a Sub-Process, making changes as needed: the end result is a Revision of the original SubProcess.

Process Operations and Process Steps
Process Operations are the main building blocks that make up an abstract Process: during Engineering, a series of
Process Operations are linked in sequence to form the backbone of a generic Process.
In turn, each Process Operation can exist as the result of the linking of various Process Steps, which are optional.
Process Operations can be linked to different parent Processes or parent Sub-Processes.
When instantiated, Process Operations are known as Work Order Operations, whereas Process Steps are called Work
Order Steps.
Process Operations and Process Steps can be modified, making changes as needed: the end result is a Revision of
the original Process Operation or Process Step.
The order of execution of Process Operations and Process Steps is defined by their Sequence and Dependencies.

Opcenter Execution Discrete 2507 - Product Overview

51


## Pagina 52

Basic Concepts
Production Process Configuration

It is possible to adopt groups of alternative Process Operations in place of the Process Operations that have already
been defined as part of your main execution flow for a specific Process.
In certain contexts, it is advantageous to classify Process Operations according to the purpose for which
they are to be performed: for more information, see Operation/Step Categories.

Example of Process Configuration
To clarify how a Process is defined, here is an example taken from the white-appliance industry.
Let's say you need to assemble a washing-machine drum in your production plant. To achieve your goal, you must
outline a Process, which we will call DrumAssembly.
Process "DrumAssembly" consists in a number of Process Operations that must be performed in a specific
sequence: these Process Operations are "DrumElementRetrieval", "DrumElementPreparation",
"DrumElementPositioning" and "DrumElementWelding".
Each Process Operation consists in a series of Process Steps, which must be performed in a specific sequence: for
example, Process Operation "DrumElementWelding" may involve Process Steps whereby:
• The welding machine is verified prior to activation.
• The welding machine is positioned directly above the drum element.
• The welding machine is activated to weld the drum element.
• The welding machine is moved away from the welded drum element.

2.5.1.1 Alternative Process Operations
Alternative Process Operations are Process Operations that can be adopted in alternative to the main execution
flow configured for a specific Process by setting dependencies between the Process Operations.
If appropriately configured, Alternative Process Operations offer the possibility of foreseeing various ways to
manufacture the same product.
• A Process Operation cannot belong to different groups of Alternative Process Operations.
• The Process Operations making up a group must belong to the same Process.
Alternative groups of Process Operations are created by a Product Engineer who ensures that:
• the Production Type of the Work Orders instantiated from the involved Process is set to either Serialized or Full
Quantity.
• at least three Process Operations are available for a specific Process.
• the aforementioned Process Operations are in sequence and one is configured as the predecessor of all the
others.
• one of the alternative paths is set as the preferred one.
It is possible to change the preference of one Alternative Process Operation over another, according to
your needs.
For details on how execution plays out (that is, which paths are followed) when Alternative Groups of Operations
are involved, see the examples and diagrams provided in Alternative Work Order Operations.

2.5.2 Sequences and Dependencies
Sequences are numeric indexes (typically, multiples of 10) that indicate the order of execution of:

52

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 53

Basic Concepts
Production Process Configuration

• Work Order Operations making up a Work Order.
• Work Order Steps making up a Work Order Operation.
• Work Orders in a series based on Work Order Operation external dependencies.
For example, the first Work Order Step of a Work Order Operation may have Sequence 10, the second 20, and so on.
The execution of Work Order Operations can be non-linear and involve additional constraints and conditions. For
example:
• It is possible to define Dependencies between Work Order Operations, allowing their execution only after the
start or the end of a previous one.
• Work Order Operations without Dependencies on others can be executed "out of route", that is, in every
moment during the execution of their Work Order.
• Work Order Operations can be defined as Optional, therefore possibly skipping its execution.
• The start and/or the completion of a Work Order Operation can be either manual or automatic.
Sequences and Dependencies can be defined by the Product Engineer for Process Operations and Process Steps:
these Sequences and Dependencies are then inherited in runtime by the instantiated Work Order Operations and
Work Order Steps.
Dependencies between Process Operations or Work Order Operations are graphically displayed during Work Order
creation and execution.
It is possible to define Dependencies between Work Order Operations:
• belonging to the same Work Order.
• belonging to different Work Orders.
In the case of a series of Work Orders, the sequence number merely indicates a hypothetical order of execution.
Therefore, if not explicitly configured through dependencies between the Work Order Operations, successive Work
Orders belonging to the same series may be released for execution, even if the first Work Order in the sequence has
not been completed.
There exists the possibility of defining alternative paths for execution: keep in mind that this entails
introducing a more complex level of dependencies.

2.5.3 Catalogs
In Discrete manufacturing, process configuration is a crucial and time-consuming aspect: where possible, it should
be possible to leverage on existing know-how to speed up this task and streamline production. Therefore, it is
extremely important to be able to reutilize the main elements involved in configuring how your production must be
executed: that is, the possibility of using the Processes, Operations and Steps that make up the backbone of your
production must be effortless and not limited to solely one given context.
In Opcenter Execution Discrete, three dedicated Catalogs function as libraries for containing, respectively, all
the Processes, Operations and Steps currently available in the system, to permit their reutilization in different
contexts within the same production plant.
For more information, see Dedicated Catalogs for Reusing Processes, Operations and Steps.

2.5.4 Work Instructions, Documents and Document Items
Work Instructions and Documents contribute greatly to the successful execution of production processes: for an
Operator, it is important to have the right information on hand at the right time so he/she can perform his/her job in
a speedy and accurate manner.

Opcenter Execution Discrete 2507 - Product Overview

53


## Pagina 54

Basic Concepts
Production Process Configuration

As need be, it is possible to create a collection of documents (Work Instructions, Documents and Document Items)
from which to choose for subsequent association. In any case, this collection of associable documents can contain
files that are pertinent to one or more of the MES entities for which associating a document is feasible: no
distinction as to their possible "destination of use" is made.
In particular, Document Items are designed for grouping Documents: their adoption allows you to better organize
your Documents according to your needs and facilitate their eventual linking to other entities.
For both Work Instructions and Documents, there exist no limitations regarding the file format used for Work
Instructions and Documents. Also, more than one Work Instruction (or Document) can be associated to a single MES
entity.
For more information on the functionalities related to Work Instructions and Documents, as well as Document
previewing, see Readily-Available Work Instructions and Documents.
For details regarding Document Item functionalities, see Document Item Management.

Work Instructions
Work Instructions are the runtime instantiation of Work Instruction Specifications, which in turn are generated from
Work Instruction Definitions. They serve the purpose of providing the Operator with a specific outline as to which
actions he/she must perform during execution in order to complete a certain Operation, Step or Execution Group
successfully.
This outline may consist of one or more of the following sections:
• a section containing specific step-by-step instructions for carrying out a specific activity. These instructions may
require acknowledgement by the Operator before he/she can continue carrying out his/her activities.
• a Data Collection section, which is similar to a form designed to contain the requested measurements and
values. The Operator will fill in this section during runtime as part of the activity being performed.
Work Instructions can be attached to the following entities:
• Process Operations
• Process Steps
• Work Order Operations
• Work Order Steps
• Serial Numbers
• Execution Group Phases
so that they can be accessed when execution reaches that particular moment during production.
When a Work Instruction containing a Data Collection section is associated to Serial Numbers produced by a Work
Order Operation, the association can be global (that is, with all the produced Serial Numbers) or partial. In the latter
case, the Operator will be able to specify at runtime the exact list of Serial Numbers to be associated.
Work Instructions can also be shared among Work Order Operations/Work Order Steps belonging to the same Work
Order and having the same Association Type (that is, Operation, Serial Number, Serial Number on Demand). In
this case, values for Data Collections collected at runtime for a shared Work Instruction will be displayed on any
Work Order Operation/Work Order Step using the same Work Instruction, as shown in the following image.

54

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 55

Basic Concepts
Production Process Configuration

Documents
Documents serve the purpose of providing the Operator with additional insight while performing his tasks.
Documents can be imported and linked to the following entities:
• Materials
• Tool Definitions
• Process Operations
• Process Steps
• Work Order Operations
• Work Order Steps
• Material Tracking Units
• Execution Group Phases
• Non-Conformances
• Container Types.

2.5.4.1 Document Items
Document Items are used to group together Documents sharing certain characteristics or serving a specific purpose
to facilitate their linking to other entities.
Document Items can be imported and linked to the following entities:
• Process Operations
• Process Steps
• Work Order Operations
• Work Order Steps.

Opcenter Execution Discrete 2507 - Product Overview

55


## Pagina 56

Basic Concepts
Production Execution Management

2.6 Production Execution Management
The list of basic concepts provided below is valid for standard production execution. If your production
execution involves Additive Manufacturing, see Production Environment Configuration in Additive
Manufacturing for those basic concepts specific to this context.
Also, for concepts specific to Intra-Plant Logistics (that is, the management of how Materials are
transported inside your plant), see Transportation Management.
Here are the basic concepts for managing production execution:
• Tools
• Material Tracking Units
• Pre-Kitting
• ERP Order and ERP Order State Machine
• Work Orders, Work Order Operations and Work Order Steps
• Alternative Work Order Operations
• Results and Result Types
• Execution Groups and Execution Group Phases
• Non-Conformances
• Non-Productive Activities
• Offline Sessions and Offline Actions
• Change Packages.

2.6.1 Tools
In Opcenter Execution Discrete, a Tool is conceived as a utensil used to execute a specific Work Order Operation.
Tools are instantiated from Tool Definitions.
It is possible to set threshold values on Tools to define:
• the number of times they can be used;
• for how long they can be used;
• when they will expire.
When a Work Order Operation that requires a Tool is executed, you can specify the identifier of the actual Tool used,
how many times the Tool has been used and the duration of its use.
Tools can be set as Lockable during execution: in this manner, it is possible to define which resources cannot be
used concurrently.
By associating Setpoints to a Tool, it is possible to drive its runtime behavior automatically, thereby eliminating the
need for shop-floor operators to perform manual adjustments.
If anomalies or defects are discovered on existing Tools, it is possible to declare Non-Conformances on them.

Example of Tool Instantiation

56

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 57

Basic Concepts
Production Execution Management

Tool States
State

Description

Available

The Tool is available for production.

Busy

The Tool is currently used in a Work Order Operation.

WarningAvailable

Not applicable.

Maintenance

The Tool is undergoing maintenance activities, and hence, is not
available for production.

OnHold

The Tool is currently not available for production, due to one of the
following conditions:
• The Tool has been used for a number of times that exceeds the
maximum allowed.
• The Tool has been used for an amount of time that exceeds the
maximum planned duration.
• The expiration date and time of the Tool was reached.

Possible State Transition for Tools
Source Status

Possible Target States

Available

OnHold

OnHold

Not applicable.

Opcenter Execution Discrete 2507 - Product Overview

57


## Pagina 58

Basic Concepts
Production Execution Management

2.6.2 Pre-Kitting
The term Pre-Kitting is used to indicate the reservation of Material Tracking Units (be they Serial Numbers or
Batches) and their respective quantities (either in full or in part) for use in specific Work Order Operations or Work
Order Steps. By performing pre-kitting in advance for Work Orders, the Operator can bypass typing in or scanning
the individual Material Tracking Units.
In those contexts in which validation on the reserved Serial Number or Batch has not been configured, assembly
will be performed directly. Instead, if validation is necessary, the Operator must explicitly enter the Serial Number
or Batch Id (either manually or by barcode scanning): if the entered value matches what was pre-kitted during
configuration, only then will assembly be performed.
Pre-kitting refers to a specific Work Order Operation or Work Order Step that belongs to the Work Order in question.
Each element that is pre-kitted is either reserved in full or in part. In detail:
• Serial Numbers that are pre-kitted will by default be considered as having a quantity equal to 1, as a single Serial
Number cannot be divided: thus, pre-kitted Serial Numbers are always considered as "reserved in full".
• When Batches are pre-kitted, you can reserve their available quantities either in full or in part (for those cases in
which reserving only a portion of the Batch's available quantity is necessary). Any remainders of those Batch
quantities that have not been pre-kitted are thus considered as "not reserved": therefore, their eventual future
consumption is not specific to a certain Work Order Operation or Work Order Step of the selected Work Order.

2.6.3 ERP Order and ERP Order State Machine
An ERP Order is a customer order for the production of a specific product and it is associated with a Final Product
Type, which represents the final product of a specific plant. If there are multiple orders corresponding to different
production lines within the plant (for example one for the Engine, one for the Control Panel), the management of
the production must be planned within the ERP System.
Since the production starts only when the ERP Order is received, each ERP Order contains information necessary to
schedule its production. Consequently, dates are very important because they represent the actual progression of
production, from the starting date to the delivery date.
An ERP Order can be identified by a Final Product Family, which represents a specific configuration needed to
produce a certain product and it is the unique identifier of the structures (Bill of Materials and Bill of Features)
making up the Product Configuration needed to produce the Final Product Type associated with the ERP Order. If
you produce the same car for ten times, you have one Bill of Materials and one Bill of Features which are always the
same, belonging to a specific Final Product Family.
Depending on the type of Work Order you intend to use in your production process, there exists two ways of
creating and managing Work Orders retrieving information from the ERP Order:
• using the Production Flow Control, through the proper Milestone Attribute.
• directly from the ERP Order, by setting additional specifications when configuring Final Product Types. This type
of Work Order creation is intended when you need to produce parts which will be subsequently used in the main
execution process of the first production type.

ERP Order State Machine
The ERP Order State Machine manages the entire ERP Order lifecycle, to track and monitor the actual progression of
production for each Final Product Type. The State Machine has a predefined list of states and transitions which
cannot be added or deleted by configuration. The entire structure of the production process can be monitored by
observing how the ERP Order undergoes a transition from one state to another.
For each Final Product Type, you can choose which of the predefined states you want to associate with a specific
predefined behavior, freezing the structures (Bill of Materials and Bill of Features) needed to produce the Final

58

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 59

Basic Concepts
Production Execution Management

Product Type associated with the corresponding ERP Order. After a configurable amount of time, the ERP Order
Data is archived and then deleted.

Available ERP Order States
Status Name

Status Identifier

Description

Received

RCV

The system receives the ERP Order.

Scheduled

SCH

The ERP Order is scheduled for production.

Linked

LNK

(Skipped in case the Work Order is created directly
from the ERP Order and not through the Production
Flow Control) The ERP Order is now linked to the
Material Tracking Unit that must be produced.

In Production

PRD

The ERP Order is in production. This means that the
Product Configuration and the Bill of Materials
associated with the Order can no longer be modified.

Completed

CMP

The ERP Order is completed and ready to be shipped
and delivered.

Delivered

DLV

The ERP Order has been delivered. From this moment
on, the Order is out of MOM boundaries.

2.6.4 Work Orders, Work Order Operations and Work Order Steps
Generally speaking, a Work Order represents a detailed request to execute a specific production cycle. It consists of
one or more Work Order Operations, which represent specific manufacturing activities. Optionally, a Work Order
Operation can be divided into Work Order Steps.
Typically, a Work Order is the runtime instantiation of a Process, and therefore its Work Order Operations and Work
Order Steps are respectively the runtime instantiations of the Process Operations and Process Steps belonging to
the source Process.
Work Orders can also be created manually from scratch, without instantiating a Process. It is also possible to create
a Work Order Header, without Work Order Operations, and at a later time merge it with a Process to obtain an actual
Work Order. This is useful, for example, to track production requests coming from ERP.

Opcenter Execution Discrete 2507 - Product Overview

59


## Pagina 60

Basic Concepts
Production Execution Management

Work Orders can contain Work Order Operation Folders, which are basically logical containers of Work Order
Operations which will then be executed as usual.
The order in which Work Order Operations are executed is determined by their Sequence and Dependencies.
Dependencies can also be established between Work Order Operations belonging to different Work Orders.
Additionally, you can define dependencies from/ to Work Order Operation Folders and/or from/to Work Order
Operation Folders and Work Order Operations: in order to simplify the routing design you are not forced to draw a
dependency for each single Work Order Operation but you can directly refer to its parent Work Order Operation
Folder.
In combination with the dependencies, it is possible to define groups of alternative Work Order Operations that can
be executed in alternative to the main execution flow configured for a specific Work Order.
During the execution of a Work Order, the following may take place:
• Documents are displayed to the Operator (for example, instructions or safety rules).
• One or more Material Tracking Units are consumed or processed.
• One or more Machines execute some activities, with or without the use of Tools.
• Some manual activities are performed, with or without the use of Tools.

60

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 61

Basic Concepts
Production Execution Management

The details regarding the assembly of the elements making up a Work Order (or a group of Work Orders belonging
to the same parent batch) form its genealogy.
Not all Work Orders and their elements (Work Order Operations and Work Order Steps) have a linear lifecycle, and
therefore their status is subject to modification according to the situation: for example, Work Order Operations can
be paused, restarted, etc. for various Reasons.
Work Order can also be imported from Master Plan and As Planned through an XML file. For more information on
importing Work Orders, see the XML File for Work Orders of the Opcenter Execution Discrete Installation and
Configuration Manual.
Data Segregation Propagation
If an As Planned BoP inherits a Data Segregation tag from the Final Material, when a Work Order is created
through the Work Order Header or from a Process, this Data Segregation tag is automatically propagated
from the BoP to the Work Order.
When the Work Order is released to production, the Data Segregation tag is automatically propagated also
to the Documents and Work Instructions associated to its Work Order Operations and Work Order Steps.
If new Documents or Work Instructions must be associated to the Work Order at a later time (for example,
after the Work Order has been completed), thanks to a dedicated button in the user interface the Data
Segregation tag is automatically propagated to the newly added Documents and Work Instructions.
In case a Rework Work Order is created, it will inherit the Data Segregation Tag present in the As Planned
BOP created for the rework.
The Data Segregation Tag of the Work Order is automatically propagated also to the collected Documents
associated to the Work Order Operations and Work Order Steps of the Work Order during runtime.
At runtime, solely the user associated to the same Data Segregation tag can view the segregated Work
Order with the related Documents, collected Documents and Work Instructions. The user can also open
Non-Conformances which will inherit the Data Segregation Tag from the Work Order.

Work Order States
State

Description

Edit

The Work Order can be modified.

Pending

This Work Order has been created to be merged with a Process at a
later time. It is not possible to add Work Order Operations manually.

ReadyForScheduling

This Work Order can be scheduled before it is released for production.

New

This status is assumed by Work Orders when they are released to
production.
A Work Order in New status (that is, released but not yet started) can be
reverted to the Edit status.

Active

A Work Order is in this status if at least one of its Work Order Operations
is in Active status.

Opcenter Execution Discrete 2507 - Product Overview

61


## Pagina 62

Basic Concepts
Production Execution Management

State

Description

Hold

A Work Order is placed in Hold status when there are problems in
execution that need to be resolved. If a Work Order is in Hold status, its
Work Order Operations cannot be started.

Queue

The Work Order assumes this status immediately after completion of
one of its Work Order Operations and prior to moving on the next Work
Order Operation of its sequence.

Pause

A Work Order is placed in Pause status when at least one of its Work
Order Operations is in Partial status and none of its Work Order
Operations are in Active status.

Split

The Work Order has been split into smaller Work Orders to facilitate
production: for example, the original Work Order may be particularly
large, thereby making its execution complicated.

Rework

The Work Order is placed in this status when it needs to be reworked, in
relation to Non-Conformances that are present.

Scrap

The Work Order has been scrapped due to the presence of NonConformances that cannot be rectified.

Verified

The Work Order has contributed to the production of a final product
(Material Tracking Unit) that satisfies expectations: the Work Order in
question can thus be verified.
After performing verification on a Work Order, if it is deliberately placed
in Verified status, it can no longer be modified.
It is necessary to "unverify" a Work Order in Verified status in order to
permit its modification.

Complete

All the Work Order Operations making up the Work Order have been
executed, or some of them have been set in NotExecuted status.

Aborted

The execution of the Work Order has been aborted.

Possible State Transitions for Work Orders

62

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 63

Basic Concepts
Production Execution Management

Source Status

Possible Target States

Edit

• ReadyForScheduling
• New
• Aborted

Pending

• Edit
• ReadyForScheduling
• Aborted

ReadyForScheduling

• New
• Edit

New

• Active
• Hold
• Split
• Rework
• Scrap
• Aborted
• Edit

Active

• Hold
• Queue
• Pause
• Split
• Rework
• Scrap
• Complete
• Aborted

Hold

• Active
• Queue
• Pause
• Split
• Rework
• Scrap

Queue

• Active
• Hold
• Pause
• Split
• Rework
• Scrap
• Complete
• Aborted

Opcenter Execution Discrete 2507 - Product Overview

63


## Pagina 64

Basic Concepts
Production Execution Management

Source Status

Possible Target States

Pause

• Active
• Hold
• Split
• Rework
• Scrap
• Aborted
• Complete

Split

• New
• Complete

Rework

• New
• Active
• Hold
• Queue
• Pause

Scrap

• New
• Active
• Hold
• Queue
• Pause

Verified

Complete

Complete

• Pause
• Split
• Verified

Aborted

Not applicable.

Work Order Operation States
State

Description

Open

The Work Order Operation has been instantiated.

Active

A Work Order Operation is in this status if someone is working on it.

Partial

Only a portion of the quantity to be produced for the Work Order
Operation has been processed: the remainder is yet to be executed.

64

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 65

Basic Concepts
Production Execution Management

State

Description

Future Hold

By setting a Work Order Operation in Future Hold, the Work Order to
which it belongs will in turn be automatically set to Hold status whenever
the Work Order Operation is started or when the Work Order Operations
preceding it (according to their dependencies) are completed.

Complete

The execution of a Work Order Operation has been completed.

NotExecuted

This status is set on:
• a skippable Work Order Operation that has been actually skipped;
• an optional Work Order Operation that has not been executed;
• the Work Order Operations not yet executed belonging to an aborted
Work Order.

Aborted

The execution of the Work Order Operation has been aborted.

Possible State Transitions for Work Order Operations
Source Status

Possible Target States

Open

• Active
• Future Hold
• NotExecuted

Active

• Complete
• Partial

Partial

• Active
• Future Hold

Future Hold

• Open
• Partial

Complete

Partial

NotExecuted

Not applicable.

Aborted

Not applicable.

Work Order Step States

Opcenter Execution Discrete 2507 - Product Overview

65


## Pagina 66

Basic Concepts
Production Execution Management

State

Description

Open

The Work Order Step has been instantiated.

Active

A Work Order Step is in this status if someone is working on it.

Partial

Only a portion of the quantity to be produced for the Work Order Step has
been processed: the remainder is yet to be executed.

Complete

The execution of a Work Order Step has been completed.

NotExecuted

This status is set on a Work Order Step that has been automatically
skipped by the system when the parent Work Order Operation was
completed.

Possible State Transitions for Work Order Steps
Source Status

Possible Target States

Open

• Active
• NotExecuted

Active

• Complete
• Partial

Partial

• Active
• Complete

Complete

Not applicable.

NotExecuted

Not applicable.

Production Types for Work Orders
The actual dynamics of how a Work Order is executed, as well as the type of Material Tracking Unit that is produced,
is determined by the Work Order's production type.
Here are the production types available for Work Orders in Opcenter Execution Discrete.
All the production types are available for serialized materials, while they are not available for materials
that cannot be serialized.

66

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 67

Basic Concepts
Production Execution Management

Production Type

Description

FullQuantity

The Work Order produces a Batch. The quantity specified in each Work
Order Operation is the quantity of the entire Work Order. In order to start
a particular Work Order Operation, it is necessary that the Work Order
Operation preceding it has been completed.

TransferBatch

The Work Order produces a Batch. A single run of a Work Order
Operation can produce only a portion of the entire Work Order. The
remainder can be produced in a subsequent run of the same Work Order
Operation.

Serialized

The Work Order produces serialized items (Serial Numbers) that move
individually from one Work Order Operation to the next. After Work Order
creation, it will be necessary to specify the Serial Numbers codes to be
associated to the Work Order.

FullSerialized

The Work Order produces serialized items (Serial Numbers) that move as
a group from one Work Order Operation to the next. Only after a Work
Order Operation has been completed on all of these serialized items will it
be possible for these Serial Numbers to move on to the next Work Order
Operation. After Work Order creation, it will be necessary to specify the
Serial Numbers codes to be associated to the Work Order.

FlexibleBatch

The Work Order produces a flexible Batch. After the Work Order creation,
the user can modify the quantity of the Work Order to be produced based
on the requirement.

FlexibleSerialized

The Work Order produces serialized items. After the Work Order creation,
the user can modify the quantity of the Work Order to be produced based
on the requirement.

2.6.4.1 Alternative Work Order Operations
Alternative Operations are Work Order Operations that can be executed in alternative to the main execution flow
configured for a specific Work Order by setting dependencies between the Work Order Operations.
They can be configured to manufacture the same product in more than one way: this comes in handy when there
are Work Order Operations configured to start automatically or when some of the Machines involved are not
available for production.
Alternative groups of Work Order Operations are created by a Product Engineer who ensures that:
• at least three Work Order Operations are available for a specific Work Order.
• the aforementioned Work Order Operations are in sequence and one is configured as the predecessor of all the
others.
• one of the alternative paths is set as the preferred one.

Opcenter Execution Discrete 2507 - Product Overview

67


## Pagina 68

Basic Concepts
Production Execution Management

It is possible to change your preference of one Work Order Operation over another, according to your
needs, provided that the Work Order is not in use.
Alternative Work Order Operations can be configured for Serialized and Full Quantity Work Orders.
In the example below, the letters indicate groups of Alternative Operations, whereas the blue arrows indicate the
preferred paths for execution.

At runtime, the Operator is guided in the execution of the Work Order Operations referring to the graph displayed in
the Operator Landing page (legacy).
When Serialized production is involved, the Operator can decide to start Serial Numbers on the same Work Order
Operation or on one of the available alternatives.
Instead, when Full Quantity production is involved, the Operator can start production directly by executing the
Work Order Operation.

For both types of production, upon completion of a Work Order Operation, the system proposes the available paths
and removes the skipped Work Order Operations, thereby preventing the Operator from starting them by mistake.

68

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 69

Basic Concepts
Production Execution Management

2.6.4.2 Results and Result Types
In certain situations, the Shop-Floor Operator may be required to declare the outcome (known as Result) of a
specific Work Order Operation's execution for a Batch or Serial Number (Material Tracking Unit) that is being
produced, both in the case in which the outcome coincides with what was originally planned or otherwise. In this
manner, depending on whether the Work Order Operation was completed successfully (Result OK or a positive
Result) or not (Result NOK or a negative Result), he can decide on adopting a specific strategy that will determine
how the Work Order Operation's execution must proceed for the Batches or Serial Numbers (MTUs) it is producing.
By default, if the Work Order Operation's Result is NOK, the Repeat strategy is adopted, whereby the failed Work
Order Operation will be re-executed for the Batches or Serial Numbers (MTUs) involved and then re-evaluated by
the Shop-Floor Operator to determine whether this second attempt was completed successfully or not. Should the
Result still be deemed NOK, the process of re-execution and re-evaluation will be re-iterated until the Result is
deemed OK.
Two Result Types are provided by default with the system to classify Results as positive (OK) or negative (NOK):
however, if these default Result Types do not satisfy particular needs, it is possible to configure custom Result
Types.
All Results are tracked on the specific Material Tracking Unit to which they refer: the strategies subsequently
adopted to manage such Results are also provided. If desired, in any case, a Result's value or its strategy can be
amended as needed.

Result Management in relation to Activities
Through dedicated configurations, the Result for Work Order Operations can be set at Activity level. An Activity
represents an action which can be performed inside each Operation.
When the result at Activity level is enabled, if a Specification Type (Material, Tool, Work Instruction or Inspection
Definition) is associated to the Operation during the Work Order configuration, multiple Activities are created for
the associated Specification Type. In this manner, the Result is associated to the single Activity and not to the
Operation.
For example, for a Work Order Operation with two Materials, one Activity is created for each associated Material:
Material A will have Activity A and Material B will have Activity B. If one of the Activities is not completed successfully
(for example, a Material is partially consumed, or a Tool is used for less than the number of times expected), the
entire Work Order Operation will have a NOK Result. The failed Activities can be re-executed until the Operation
Result is deemed OK.
In case of negative results for their related Activities, existing Work Instructions can be re-edited from the User
Interface even if they have been already acknowledged or confirmed, to edit the desired values until the Operation
Result is deemed OK.
If necessary, custom Activities can be configured as well as their Results and validations, provided that the
appropriate business logic is applied. For additional information on how to implement these customizations, refer
to the How to Customize Results for Activities page in the Opcenter Execution Discrete Extensibility Guide.

For more information on Result-related functionalities, see Result Management and Runtime Work Order Execution.

2.6.5 Execution Groups and Execution Group Phases
Execution Groups are sets of Work Order Operations (typically belonging to different Work Orders) that are grouped
to be executed together at runtime on the same Equipment. The purpose of Execution Groups is to both maximize
productivity and minimize Equipment downtime, thereby allowing the Machines to work at full capacity. Different
Users can work on the same Execution Group at the same time.

Opcenter Execution Discrete 2507 - Product Overview

69


## Pagina 70

Basic Concepts
Production Execution Management

When Work Order Operations belonging to the same Work Order and joined by linear dependencies are grouped
together in the same Execution Group, Execution Group Phases are automatically created.
Once created (and, if desired, scheduled), Execution Groups can then be released for use in production. After being
released, an Execution Group must be started so to enter the actual production process in runtime. At this point,
the Work Order Operations making up the Execution Group are launched in parallel on the same Machine. An active
Execution Group can be paused, pausing at once all the Work Order Operations joined to it.
Completing an Execution Group means that its Work Order Operations have been executed in full and the Execution
Group can no longer be launched on the Machine to which it is associated. If Execution Group Phases are present,
the same Execution Group can be first started and then completed multiple times, each time completing a phase:
the completion of the last phase actually completes the Execution Group.
When forming an Execution Group, the Work Order Operations involved must satisfy certain conditions. In detail,
the Work Order Operations must:
• Have at least one common Machine on which they can be executed.
• Use Tools belonging to the same Tool Definitions, if any.
• Consume Material Tracking Units belonging to the same Materials, if any.
• Require the same Skills and levels, if any.
It is possible to group Work Order Operations belonging to different Work Orders even if they produce different Final
Materials.
If the Work Order Operations belong to Serialized or TransferBatch Production Types, they can be associated with
an Execution Group to produce only a subset of their quantity, while the remaining quantity can be managed either
by a different Execution Group or by Work Order Operations that do not belong to the Execution Group.
An Execution Group has dedicated scheduling attributes, which are independent from the corresponding attributes
of the individual Work Order Operations involved. If a due date has been defined at Work Order level, when an
Execution Group is scheduled, its due date is automatically calculated. If the Work Orders belonging to the same
Execution Groups have different due dates, the system automatically selects the earliest due date as the date by
which the Execution Group must be completed.
Powder Materials used in Additive Manufacturing production for all the Work Order Operations inside an Execution
Group Phase can be consumed at the same time.
Powder Material Batches, previously loaded into 3D Printers and used for printing operations in Additive
Manufacturing production, can be tracked for all the Work Order Operations inside an Execution Group.
When a new Work Order Operation is added to an existing Execution Group Phase or a new phase is created in an
Execution Group, the Estimated Duration value of the Execution Group Phase is set to the maximum duration of the
operations present in the Execution Group Phase.
Execution Group Phases, if present, have these same scheduling attributes (which in turn are independent from the
corresponding attributes of the Execution Group to which they belong). Furthermore, for each Execution Group
Phase, it is possible to specify a preferred Machine on which the phase should be executed.
Execution Group Phases can have their own Work Instructions.
It is possible to schedule Execution Groups directly from the Opcenter APS environment, provided that the relative
integration is enabled and correctly configured.
The system tracks the history of materials consumed at the Execution Group level and the Execution Group Phase
level.

Execution Group States

70

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 71

Basic Concepts
Production Execution Management

The state of an Execution Group represents the point reached by the various Work Order Operations
(belonging to both the same Work Order and different Work Orders) making up the Execution Group for
what concerns their execution as a whole at runtime on the same Equipment.
State

Description

Edit

The Execution Group can be modified.

ReadyForScheduling

The Execution Group is ready to be scheduled from a scheduling
system. It cannot be started yet.

New

This status is assumed by an Execution Group when it is released to
production.

Active

The Execution Group is in execution.

Queue

The Execution Group is temporarily queued.

Pause

The Execution Group has been paused.

Complete

The Execution Group has been completed.

Aborted

The Execution Group has been aborted.

Possible State Transitions for Execution Groups
Source Status

Possible Target States

Edit

• New
• ReadyForScheduling
• Aborted

ReadyForScheduling

Edit

New

• Active
• Edit
• Aborted

Active

• Pause
• Queue
• Complete
• Aborted

Opcenter Execution Discrete 2507 - Product Overview

71


## Pagina 72

Basic Concepts
Production Execution Management

Source Status

Possible Target States

Queue

• Active
• Aborted

Pause

• Active
• Aborted

Complete

Not applicable.

Execution Group Phase States
State

Description

Open

This is the initial status. In this status, the Execution Group Phase can be
started (if it is the current one).

Active

The Execution Group Phase has been started and it is in execution.

Partial

The Execution Group Phase has been paused.

Complete

The Execution Group Phase has been completed.

Possible State Transitions for Execution Group Phases
Source Status

Possible Target States

Open

Active

Active

• Partial
• Complete

Partial

Active

Complete

Not applicable.

2.6.6 Transportation Management
All those activities regarding the transportation of items within the boundaries of a Plant can be classified as related
to transportation management, also referred to as Intra-Plant Logistics (IPL).
Here are some examples of such activities:

72

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 73

Basic Concepts
Production Execution Management

• Raw materials are moved from a storage area to the machine that will process them.
• Semi-finished products are transported from one machine to another so that they can undergo additional
processing.
• Final materials are moved to another storage area prior to being packaged and subsequently shipped out from
the Plant.
• A specific raw material is transported upon request from a storage area to a specific location inside the Plant so
to permit the continuation of production activities.
• A defective piece is pulled from the normal flow of activities and moved to a specific location so that it can be
checked, reworked or scrapped.
The basic concepts related to Transportation Management in your production plant are:
• Logistic Classes
• Buffer Definitions and Buffers
• Logistic Requests
• Handling Units and Transport Operations.
To examine the flow followed for the transportation of items inside the production plant, see section "The Logistic
Request Flow" on page Logistic Requests.

2.6.6.1 Logistic Classes
A Logistic Class groups together similar Materials or Tool Definitions for transportation or packaging. For example,
Logistic Class "Burner Pipes" groups together all burner pipes that are produced in the same Plant and need to be
transported.
Opcenter EX DS comes with a predefined default Logistic Class, but it is possible to create custom Logistic Classes
tailored to your needs.

2.6.6.2 Buffer Definitions and Buffers
Buffer Definition
A Buffer Definition is an abstract representation of a specific area or accessory (for example, a wagon or cart)
allocated to store items. The configuration of a Buffer Definition takes into account the maximum weight,
maximum volume or maximum quantity, as well as the unit of measure to be used, when defining the overall
capacity allowed. It is possible to configure a Buffer Definition so to allow the storage only of specific Materials and/
or Logistic Classes, specifying minimum and maximum quantities, as well as threshold and target quantities for
automatic replenishment.
The same Buffer Definition can have one or more Revisions (versions). For example, let's say you have created a
Buffer Definition representing a rack with 6 shelves that satisfies certain specifications. At some point in time, you
change the model of the rack because the requirements regarding the rack's shelves have changed, or you decide
to change the rack supplier to lower costs. For this reason, you will modify the original Buffer Definition and change
it accordingly, thereby generating a new Revision of it.

Buffer
A Buffer is the runtime instantiation of a Buffer Definition: it represents the actual area or accessory for storing
specific Material Tracking Units to be used or consumed during production within the Plant. Depending on how its
Buffer Definition has been configured, each Buffer will be allowed to hold only those specific Material Tracking Units
belonging to certain Materials and/or Logistic Classes. The Buffer Status reflects the current state of the Buffer. To
add Material Tracking Units to the Buffer, the Buffer must be in the Released state.

Opcenter Execution Discrete 2507 - Product Overview

73


## Pagina 74

Basic Concepts
Production Execution Management

Buffer States
State

Description

In Work

When a Buffer is created, but not ready to use.

Released

The Buffer is ready to be used.
Note: To add material to the Buffer, the status of the Buffer must be in
the Released state.

Invalid

The Buffer is no longer required.

Possible State Transitions for Buffers
Source Status

Possible Target States

In Work

• Released
• Invalid

Released

• In Work
• Invalid

Invalid

• In Work
• Released

2.6.6.3 Logistic Requests
Declaring a Logistic Request is essential to transportation management within your production plant, as it specifies
what is required (that is, the Material Tracking Unit) and where it is needed in runtime: without a Logistic Request,
no gap in Material Tracking Units contained in a Buffer to permit the continuation of production can be satisfied.
Automatic Logistic Request generation is the most common scenario: by importing a dedicated signal rule installed
with Opcenter Execution Discrete, Logistic Requests are generated automatically by the system whenever the
Buffer level falls below a defined threshold for Material Tracking Units.
For example:
• With no Buffer target value specified and the threshold value for Material Tracking Unit "Tire" defined in the
Buffer Definition is 10.
When numerous Tires are actually pulled from the Buffer (and thus consumed) and the quantity of Tires falls
below 10, a Logistic Request is automatically generated, requesting that the Buffer be replenished with Tires to
reach the defined threshold value once again.
• With Buffer target value specified and the threshold value for Material Tracking Unit "Tire" defined in the Buffer
Definition is 10.
When numerous Tires are actually pulled from the Buffer (and thus consumed) and the quantity of Tires falls
below 10, a Logistic Request is automatically generated, requesting that the Buffer be replenished with Tires to
reach the defined target value once again.

74

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 75

Basic Concepts
Production Execution Management

However, it is also possible to declare Logistic Requests manually, if desired.
A manual Logistic Request can consist in a single Material Request.

The Logistic Request Flow

Logistic Request States
State

Description

Open

The Logistic Request has been created.

Accept

The Logistic Request has been accepted.

Reject

The Logistic Request has been rejected.

Possible State Transitions for Logistic Requests

Opcenter Execution Discrete 2507 - Product Overview

75


## Pagina 76

Basic Concepts
Production Execution Management

Source Status

Possible Target States

Open

• Accept
• Reject

Accept

Not applicable.

Reject

Not applicable.

2.6.6.4 Handling Units and Transport Operations
When a Logistic Request is declared, it can be accepted in order to actually initiate the movement of the required
item, or rejected. When accepting a Logistic Request, it is mandatory that at least one source Buffer be specified.
Only open Logistic Requests can be accepted.
When a Logistic Request is accepted, a new Transport Operation to fulfill the request is automatically generated.
The various states of the Transport Operation specify the various phases of the Transport Operation's execution.
For example, the Released status represents a Transport Operation that can be configured according to your needs
to satisfy the Logistic Request that generated it.
Once the Transport Operation has been released and appropriately configured, the Transport Operation will be
started: the required item(s) will be pulled from a source Buffer and then placed into a Handling Unit.
Handling Units are designed specifically to identify a set of Material Tracking Units that must be moved together
from source to destination. Handling Units can start to proceed toward the destination Buffer provided that they
are in Dispatchable status. Once the Handling Unit is set in motion, it is in OnRoute status: its contents are
transported to the destination Buffer. At this point, the Transport Operation has been completed and the contents
of the Handling Unit can be unloaded.
The Transport Operation History is used to trace the details regarding the Transport Operation's execution,
whereas the Handling Unit History traces the various phases of the Handling Unit's progression.

Handling Unit States
The following table lists the states that a Handling Unit can undergo.
State

Description

New

A Handling Unit is created.

Partial

A Material Tracking Unit is loaded in a Handling Unit.

Dispatchable

This state is declared when a Handling Unit is ready to be dispatched.

Commissioned

Represents the phase in which a driver (e.g. forklift) takes a Handling
Unit to be transported (for a given Transport Operation).

76

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 77

Basic Concepts
Production Execution Management

State

Description

OnRoute

The Handling Unit is being transported (during transportation).

Transported

The Handling Unit has reached a destination.

Unloaded

The content (Material Tracking Unit) of the Handling Unit has been
unloaded: this represents the final state of a Handling Unit.

Lost

This state is declared when the Handling Unit is lost ( and its recovery is
impossible).

Possible State Transitions for Handling Units
Source Status

Possible Target States

New

• Partial
• Dispatchable
• Lost

Partial

• Dispatchable
• Lost

Dispatchable

• Lost
• Commissioned
• OnRoute

Commissioned

• Lost
• OnRoute

OnRoute

Transported

Transported

Unloaded

Unloaded

Not applicable.

Lost

Not applicable.

Transport Operation States
State

Description

Open

Represents the Transport Operation when it is created.

Opcenter Execution Discrete 2507 - Product Overview

77


## Pagina 78

Basic Concepts
Production Execution Management

State

Description

Released

Represents a Transport Operation that is ready to be executed. It can be assigned to the user.

Assigned

Represents a Transport Operation that has been assigned to a user to be executed.

Active

Represents a Transport Operation that is in execution.

Complete

This state represents a Transport Operation that has been completed

Possible State Transitions for Transport Operations
Source Status

Possible Target States

Open

Released

Released

• Assigned
• Active

Assigned

Active

Active

Complete

Complete

Not applicable.

2.6.7 Non-Productive Activities
A Non-Productive Activity is an activity that is not directly related to a production cycle and/or to a specific Work
Order, but that still needs to be tracked and recorded.
Examples of Non-Productive Activities include:
• Cleaning of Machines and Tools
• General maintenance
• Training, mentoring, assistance
• Administrative activities.
For information on functionalities related to Non-Productive Activities, see Non-Productive Activity Management.

Context
Some Non-Productive Activities may not involve production entities (such as a meeting), while others may be
directly related to them (for example, cleaning a specific machine). When declaring the start of a Non-Productive
Activity, a User may optionally specify its context (that is, the production entities related to the activity).
Context entities include:
• Work Order - Work Order Operation - Work Order Operation Step

78

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 79

Basic Concepts
Production Execution Management

• Machine
• Serial Number - Batch ID.

2.6.8 Offline Sessions and Offline Actions
Offline Sessions permit the execution of production from a dedicated client device, without connectivity to
the Opcenter EX DS server. These sessions consist of one or more Offline Actions, which are actions performed
offline at runtime by Operators from their devices: for example, starting a Work Order Operation or Work Order
Step, using a Tool, creating Quality Non-Conformances, etc..
Offline Sessions involve the execution of Work Order Operations that may belong also to different Work Orders.
Once selected for offline execution, the Work Order Operations are checked out (locked) and remain visible on the
server, but cannot be managed by Operators until they are checked in again.
For information on functionalities related to Offline Production Execution, see Production Execution in Offline
Mode.

Offline Session States
State

Description

Created

The Offline Session is created and the related Work Order Operations are
checked out (locked).

Downloaded

The content to be managed by the Offline Session, in terms of Work Order
Operations / Work Order Steps (and related data), is downloaded to the
mobile device.

Failed

The download of the Offline Session was unsuccessful.

Uploaded

The content managed on the device is uploaded to the server, along with all
the actions performed during the offline execution of the production.

CheckingIn

The check-in process of the uploaded content is in progress. This process
involves the re-execution of all the actions that have been performed on the
device by the server.

CheckedIn

The uploaded content is checked in on the server. The managed Work Order
Operations are unlocked and the actions performed while offline have been
replicated on the server.

Discarded

The content of the Offline Session is discarded. All data concerning the Work
Order Operations associated to the Offline Session is purged and made
available again on the server for online execution.

Possible State Transition for Offline Sessions

Opcenter Execution Discrete 2507 - Product Overview

79


## Pagina 80

Basic Concepts
Production Execution Management

Source Status

Possible Target States

Created

• Downloaded
• Discarded
• Failed

Downloaded

• Uploaded
• Discarded

Uploaded

• Discarded
• CheckingIn

Failed

• CheckingIn
• Discarded

CheckingIn

• CheckedIn
• Failed
• Discarded

Offline Action States
State

Description

Uploaded

The Action performed on the device is uploaded to the server.

CheckedIn

The Action performed while offline has been replicated on the server.

Failed

The check-in of the Offline Action on the server was unsuccessful.

Discarded

The content of the Offline Action is discarded.

Possible State Transition for Offline Actions
Source Status

Possible Target States

Uploaded

• CheckedIn
• Failed
• Discarded

Failed

• CheckedIn
• Failed
• Discarded

80

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 81

Basic Concepts
Production Execution Management

2.6.9 Change Packages
During the execution of a Work Order Operation or Work Order Step, an Operator may encounter unexpected
deficiencies or discrepancies regarding the Materials, Tools, Documents, Work Instructions, Machines or Quality
Inspections that are to be used.
For example:
• a double-headed hammer is present, rather than a single-headed one and thus must be substituted;
• there are cans of blue enamel, but the cans of red enamel are missing;
• there are two Documents attached to the Work Order Operation and both are instruction manuals for mounting
a left door, whereas two distinct instruction manuals are required (one for mounting the left door and one for
mounting the right door);
• the Work Instructions contain a diagram and some notes regarding blue enamel, but nothing about red enamel;
• one or more Work Order Operation Steps are missing or must be removed;
• the Work Order Operation can be started on Station1 but Station2 is also available;
• the Quality Inspection aimed to check the thickness of the enamel layer is missing.
In such cases, the Operator can notify the Production Coordinator that some changes must be made on-the-fly to
the Work Order Operation or Work Order Step (in particular, to the set of Specifications required to successfully
execute that specific Work Order Operation). This is done by opening what is known as a Change Package request.
Change Package requests can be opened only on Work Order Operations or Steps of the FullQuantity or Serialized
production type that are in Open or Partial status.
The observations (Notes) provided by the Operator in a Change Package request are an important Runtime aid to
the Production Coordinator in making an evaluation and a subsequent decision concerning the elements that come
into play in the Work Order Operation's execution.
Differences with Change Non-Conformances (Change Requests)
Although presenting similarities with Change Non-Conformances (also referred to as Change Requests),
Change Packages contemplate adding and removing Materials, Tools, Documents, Work Instructions,
Machines and/or Quality Inspections to be used in a specific Work Order Operation's execution.
Contrary to Change Non-Conformances, Change Packages do not permit adding, removing or repeating
Operations in the execution of a Work Order.
As soon as a Change Package is opened (created) by an Operator, the Work Order Operation involved is placed in
Hold status: at this point, the Production Coordinator must decide whether to make the proposed changes to the
Work Order Operation (or Step) or not.
If the Production Coordinator is in favor of adopting the changes specified by the Operator, he/she can modify the
Work Order Operation or Step, by adding and/or removing those items as indicated in the Change Package request.
If a Material in the given Work Order Operation or Step has been already consumed, it will not be possible
for the Production Coordinator to remove it. Likewise, for a Tool that has already been used. Also, if a
sample has been already taken for a given Quality Inspection, it will not be possible to remove the latter.
In line with the examples cited above, such changes can be:
• replacing the wrong Tool with the single-headed hammer;
• adding the missing cans of red enamel;
• removing one of the two left-door instruction manuals and adding a right-door instruction manual;
• editing the Work Instruction and adding information regarding red enamel;
• adding the missing Steps or removing the not needed ones;
• adding the missing Station2;
• adding the missing Quality Inspection to check the enamel layer thickness.

Opcenter Execution Discrete 2507 - Product Overview

81


## Pagina 82

Basic Concepts
Production Execution Management

In order for the changes made to become effective, the Production Coordinator must necessarily accept the Change
Package: the Work Order Operation is then released from Hold status, permitting the execution of the Work Order
Operation to continue.
Rejecting a Change Package means that the Production Coordinator either:
• has decided against making the proposed changes for some reason: the Operator may have raised a "nonissue" (for example, using the double-headed hammer rather than the single-headed one does not negatively
affect the Work Order Operation's execution) or made a mistake (for example, the cans of red enamel were
present, but not seen at first glance).
• made the proposed changes, but then had second thoughts and no longer wants them to be effectively applied.
In both of the cases cited above, the Production Coordinator must reject the Change Package to release the Work
Order Operation from Hold status and permit its execution to continue.
Data Segregation Propagation
In the context of Data Segregation, if the Operator requests a Change Package related to the Documents or
Work Instructions of a segregated Work Order, when the Production Coordinator performs the required
changes and accepts the Change Package, the Data Segregation tag is automatically propagated to the
newly added Documents and Work Instructions.

Change Package States
State

Description

Open

The Change Package has been opened by an Operator in relation to a Work Order Operation or Work
Order Step in execution.

Editing

This status is immediately assumed by the Change Package after being opened.
The Change Package can be edited: free text suggesting the changes to be made to the Work Order
Operation or Work Order Step can be inserted into its Notes.

Accept

The Change Package has been accepted by the Production Coordinator: all the suggested changes
have been made and effectively applied to the Work Order Operation (or Step), which is released
from Hold status and execution is resumed.

Reject

The Change Package has been rejected by the Production Coordinator: none of the suggested
changes have been made and/or effectively applied to the Work Order Operation (or Step), which is
released from Hold status and execution is resumed.

Possible State Transitions for Change Packages
Source Status

Possible Target States

Open

Direct transition to Editing.

82

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 83

Basic Concepts
Quality Management

Source Status

Possible Target States

Editing

• Accept
• Reject

Accept

Not applicable.

Reject

Not applicable.

2.7 Quality Management
Quality Management is the term used to indicate a set of procedures and activities for:
• verifying the quality of manufactured products in an industrial environment;
• limiting the incidence of defective products;
• pinpointing and correcting the causes of defective products.
The possibility to configure Quality Inspections is provided by the Work Instruction App, installed by Opcenter
Execution Foundation.
Natively, these Quality Inspections can then be linked to Process Operations/Steps and Work Order Operations/
Steps.
Quality Inspections can be configured with the following frequency types and will be executed at runtime
accordingly:
• 100 Percent, the Inspection will be executed on every produced item.
• Part Based, the Inspection will be executed whenever a specific number of items has been produced (that is,
each time that the part-based interval elapses).
• Time Based, the Inspection will be executed whenever a specific interval of time elapses.
• Unit Based, the Inspection will be executed at a frequency that is expressed with the implicit Unit of Measure of
the produced Material.
The frequency of execution for Part Based and Unit Based Inspections can be expressed as either a number
or a percentage based on the total number of pieces produced by the Work Order.

At runtime, if properly configured, Operators are notified when the moment in which a Quality Inspection must be
executed is approaching.
Additional information specific to Part Based Quality Inspections is provided in the paragraph below.
At runtime, the Operator can execute Quality Inspections by starting the related Quality Inspection tasks from the
Operator Landing Details page (legacy).
In the various Low Code UI Apps runtime environments, the Operator can execute Quality Inspections from the
Operator Terminal.
Quality Inspections can also be managed as separate activities outside of the manufacturing process. If you want to
manage Quality Inspection in this manner, you can also configure Inspection Master Plans and Inspection
Operations via the Work Instruction App. Once Inspection Definitions are associated to Inspection Operations,
enriched if necessary with Materials and/or Equipment, you can generate Inspection Orders, which once released,
can be executed in a dedicated environment called Inspection Operator Landing page.

Opcenter Execution Discrete 2507 - Product Overview

83


## Pagina 84

Basic Concepts
Quality Management

More information can also be found in section How to Configure Quality Execution of the Opcenter Execution
Foundation User Manual.

Part Based Quality Inspections
Part Based Quality Inspections are executed each time a specific part-based interval elapses (that is, whenever a
specific number of items has been produced).
The produced items are counted thanks to the link between the Quality Inspection and what is known as a
Referenced Operation, which notifies the system to start counting the pieces once the MTUs managed by the
Referenced Operation on a specified piece of Equipment have been:
• completed, in case the Referenced Operation is an Operation inside the routing;
• started, in case the Referenced Operation is the same Manufacturing Operation to which the Inspection
Definition is linked.
Based on the configured Frequency Value, the Operator will be prompted to perform a Quality Inspection for the
MTUs selected by the system. For those MTUs not selected by the system, if there are no other manufacturing
activities to be performed, the Operation having the Quality Inspection will be skipped or not, depending on how
the Skip Quality Inspection automatically configuration key has been set (this is possible only if the Referenced
Operation is not the same Manufacturing Operation to which the Inspection Definition is linked).
In the image below, OP10, OP20 and OP40 are dedicated to manufacturing activities (for example, Material
consumption and Tool usage). Moreover, OP10 is elected as the Referenced Operation, whereas OP30 contains the
Quality Inspection.

In a Work Order that is producing six pieces, if the Frequency Value is set to two, then the Operator will be
prompted to perform the Quality Inspection for a total of three times. The Quality Inspection task is triggered each
time the counter engine detects that two pieces have been completed for OP10.
If, instead, the Inspection Definition has been configured with the Frequency Percentage set to 50%, in a Work
Order that is producing six pieces, the Operator will be prompted to perform the Quality Inspection for a total of
two times, as the Inspection will be triggered every three pieces completed for OP10.
As a general rule:
• It is recommended that Part Based Quality Inspections not be linked to the first Operation in a routing.
• Dependencies between Work Order Operations in the routing must be of type AfterEnd.
• If Quality Inspections are linked to optional Work Order Operations, the Operator must explicitly confirm that
the produced pieces for which no Quality Inspection must be performed are to be skipped.
• One Work Order Operation can be linked to more than one Part Based Quality Inspection, but each Quality
Inspection can only be linked to one Referenced Operation.
• Part Based Quality Inspections are managed only in the case of Serialized, FullSerialized, FlexibleSerialized
and FullQuantity production types.
Moreover, when the scenario foresees multiple Work Orders generated from the same Bill Of Process, if the Part
Based Quality Inspection configuration is not changed manually at the Work Order level, it is shared among the
Work Orders, making it possible also to share the counter. As a consequence, the Quality Inspection is triggered
when the frequency value is satisfied, considering the produced pieces of all the Work Orders.

84

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 85

Basic Concepts
Quality Management

However, it is possible to configure the Part Based Quality Inspection as WO-specific, so that the inspection counter
is not shared among all the Work Orders generated from the same Process, but takes into consideration only those
pieces produced by a specific Work Order.

Time Based Quality Inspections
Time Based Quality Inspections are executed each time a specific interval of time elapses, according to a defined
schedule mode, which can be one of the following types:
• Minute
• Hourly
• Daily
For example, if the Quality Inspection is configured to be automatically triggered every thirty Minutes, and the
Operator performs the first Quality Inspection, a timer is started and, in the Operator Landing page (legacy) the
following icons are displayed:
• the
icon is displayed on the Quality Operation, to indicate that the timer has started and that, for the
moment, no other Inspections are expected by the system. However, the Operator can decide to inspect other
pieces in any case, if necessary.
• If you have configured your system to also notify that the timer is approaching expiration, then the
icon is
shown, to warn the Operator that another Inspection may be performed.
• If an additional Quality Inspection is performed, the timer is reset: otherwise, once the thirty minutes elapse, the
icon notifies the Operator that the timer has expired and that the expected Quality Inspection is in delay.
In the Operator Terminal for Complex and Repetitive Manufacturing, and in the Operator Terminal for Quality
Execution, the corresponding icons are:
•

: to indicate that the timer has started and that, for the moment, no other Inspections are expected by the
system.

•

: to notify that the timer is approaching expiration and to warn the Operator that another Inspection may
be performed.

•

: to notify that the timer has expired and that the expected Quality Inspection is in delay.

However, the Operator can move on and complete all the Work Order Operations in the routing, without performing
any additional Inspection.
Thanks to some prechecks, the system can be configured in order to block the Operator if no Quality
Inspections are performed or allow starting the next Work Order Operation in the routing in any case, even
if no Quality Inspection whatsoever has been performed and the timer did not start.
More information on the available prechecks can be found in section Special Cases regarding Quality
Inspections of the Opcenter Execution Discrete User Manual.
In the image below, OP10, OP30 and OP40 are dedicated to manufacturing activities, whereas OP20 contains the
Quality Inspection.

In this example, we consider OP20 as a Quality-only Operation and OP30 as an optional manufacturing Operation.

Opcenter Execution Discrete 2507 - Product Overview

85


## Pagina 86

Basic Concepts
Quality Management

Once Serial Numbers are started and completed at OP10, they are available for production also on OP20, OP30 and
OP40.
Depending on how you have configured your system considering also the aforementioned pre-checks, Quality
Inspection may not be mandatory and in that case, OP20 and OP30 may be skipped.

Unit Based Quality Inspections
Unit Based Quality Inspections are executed at a frequency that is expressed with the implicit Unit of Measure of the
Material that is going to be inspected. For example 2 Kgs, where Material UoM is Kg.
The produced items are counted thanks to the link between the Quality Inspection and what is known as a
Referenced Operation, which notifies the system to start counting the pieces once the MTUs managed by the
Referenced Operation on a specified piece of Equipment have been:
• completed, in case the Referenced Operation is an Operation inside the routing;
• started, in case the Referenced Operation is the same Manufacturing Operation to which the Inspection
Definition is linked.
Based on the configured Frequency Value, the Operator will be prompted to perform a Quality Inspection for the
MTUs selected by the system. For those MTUs not selected by the system, if there are no other manufacturing
activities to be performed, the Operation having the Quality Inspection will be skipped or not, depending on how
the Skip Quality Inspection automatically configuration key has been set (this is possible only if the Referenced
Operation is not the same Manufacturing Operation to which the Inspection Definition is linked).
In the image below, OP10, OP20 and OP40 are dedicated to manufacturing activities (for example, Material
consumption and Tool usage). Moreover, OP10 is elected as the Referenced Operation, whereas OP30 contains the
Quality Inspection.

In a Work Order that is producing six pieces of a Material, if the Frequency Value is set to two, then the Operator
will be prompted to perform the Quality Inspection for a total of three times. The Quality Inspection task is triggered
each time the counter engine detects that two pieces have been completed for OP10.
If, instead, the Inspection Definition has been configured with the Frequency Percentage set to 50%, in a Work
Order that is producing six pieces, the Operator will be prompted to perform the Quality Inspection for a total of
two times, as the Inspection will be triggered every three pieces completed for OP10.
As a general rule:
• It is recommended that Unit Based Quality Inspections not be linked to the first Operation in a routing.
• Dependencies between Work Order Operations in the routing must be of type AfterEnd.
• If Quality Inspections are linked to optional Work Order Operations, the Operator must explicitly confirm that
the produced pieces for which no Quality Inspection must be performed are to be skipped.
• One Work Order Operation can be linked to more than one Unit Based Quality Inspection, but each Quality
Inspection can only be linked to one Referenced Operation.
• Unit Based Quality Inspections are managed only in the case of Serialized, FullSerialized, FlexibleSerialized,
TransferBatch, FlexibleBatch and FullQuantity production types.
Moreover, when the scenario foresees multiple Work Orders generated from the same Bill Of Process, if the Unit
Based Quality Inspection configuration is not changed manually at the Work Order level, it is shared among the

86

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 87

Basic Concepts
Notification Handling

Work Orders, making it possible also to share the counter. As a consequence, the Quality Inspection is triggered
when the frequency value is satisfied, considering the produced pieces of all the Work Orders.
However, it is possible to configure the Unit Based Quality Inspection as WO-specific, so that the inspection counter
is not shared among all the Work Orders generated from the same Process, but takes into consideration only those
pieces produced by a specific Work Order.

2.8 Notification Handling
Clear communications play an important role in your production plant. Whether you need to respond to an
unforeseen event during execution or acknowledge certain situations to allow production to proceed, it is essential
that certain information be conveyed in a straightforward manner. This is done by using notifications
and signatures.
Here are the basic concepts related to notification handling:
• Notifications
• Signatures.

2.8.1 Notifications
Generally speaking, notifications are used to inform someone involved in the production process as to the presence
of an anomalous or critical situation requiring dedicated intervention.
The types of notifications available in the product are:
• Note notifications: adopted when a note has been added to a Work Order Operation or at the Work Order level
during runtime.
• Work Order notifications: adopted when a Work Order has been released or has been set as ready to be
scheduled.
• Process notifications: adopted when a Process has been completed.
• Buy-Off notifications: adopted when a Work Order Operation or Work Order Step is started and a Buy-Off
signature is required to approve or reject the produced Material Tracking Units.
• Logistic Request notifications: adopted when a Logistic Request is declared.
• Integration Event Failure notifications: adopted when there is a failure related to how an Integration Event
record has been handled by a third-party system (Active Integration, also known as AIG). The Integration Event
record provides information regarding the completion of Work Orders and Work Order Operations.
Non-Conformances can be considered as notifications: for more information, see the dedicated page.
Notifications can also be used to inform the appropriate individuals that a Non-Productive Activity has been
declared.

2.8.2 Signatures
Signatures permit the acknowledgement of certain situations and/or their handling to permit the production
process to proceed.
The types of signatures available in Opcenter Execution Discrete are:
• Buy-Off signatures: adopted when a critical Work Order Operation involved in the product's production must be
acknowledged as having been completed and/or passed inspection, thereby permitting production to proceed
and move on in the production process.
Buy-Offs have a lifecycle: for information on its states and transitions, see below.

Opcenter Execution Discrete 2507 - Product Overview

87


## Pagina 88

Basic Concepts
Production Execution Monitoring

• Electronic Signatures are adopted when the start, pause or completion of a particular Work Order Operation
requires explicit acknowledgement by the person about to perform the operation in question.
For information on this functionality, see also Electronic Signature and Buy-Off Management.

BUY-OFF Lifecycle
State

Description

New

A Buy-Off request has been created.

Pending

A Buy-Off request has been sent and needs to be managed.

Accepted

The Buy-Off request has been accepted and signed by all the entitled users.

Rejected

The Buy-Off request has been rejected. The produced Material Tracking
Unit is considered not to be acceptable and cannot be completed. A NonConformance is created and the status of the MTU is set to IsFrozen.

States and Transitions for BUY-OFF
Source Status

Possible Target States

New

• Pending
• Accepted
• Rejected

Pending

• Accepted
• Rejected

Accepted

Rejected

Rejected

• Accepted
• Pending

2.9 Production Execution Monitoring
Here are the basic concepts for monitoring production execution:
• Work Orders, Work Order Operations and Work Order Steps
• Genealogy
• Non-Conformances.

2.9.1 Genealogy
Generally speaking, a genealogy contains detailed information on the various elements that contributed to the
manufacture of a specific product.

88

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 89

Basic Concepts
Integration with External Systems

It represents the "lineage" of the finished (or intermediate) product. For example, it allows you to backtrack:
• which production entities (Materials, Tools, etc.) were involved in the execution of a certain Work Order.
• the User who started, paused or completed one of its Work Order Operations on a specific machine, including
the timestamp.
• the Work Instructions and Documents associated to its Materials and/or Material Tracking Units during the
various stages of production.
• which "parent" batches were used to create the current batch (the "child" batch) or Serial Number.
• the Execution Group unique identifier details, if a material has been consumed at the Execution Group Phase
level.
• the Execution Group Phase identifier details, if Work Instructions are associated to the Execution Group Phase.
• the print job files details along with the Execution Group and Execution Group Phase unique identifier details,
when a Print Job File is transferred.
• the Material Tracking Unit consumption and production details.
The system displays this information as a tree view and allows you to import/export it as a .json file.

2.10 Integration with External Systems
Here are the basic concepts for integrating Opcenter Execution Discrete with other systems:
• Advanced Planning and Scheduling (APS)
• Distributed Numerical Control (DNC)
• Closed-Loop Manufacturing
• Structured Messages
• Import Data Flows
• Output Messages
• Kanban Calls
• Teamcenter Share
• Intraplant Logistics (IPL).
In addition, Opcenter Execution Discrete provides functionalities for integration with Additive Manufacturing
Network.

2.10.1 Advanced Planning and Scheduling (APS)
Advanced Planning and Scheduling (APS) management is a work methodology designed to maximize productivity,
while limiting costs and waste to a minimum. Production capacity needs to be optimally allocated to satisfy the
demand, but the planning required to achieve optimal production often presents greater complexity compared to
the actual production itself. APS software is specifically designed to achieve optimal planning for production.
Opcenter Execution Discrete offers the possibility of integration with APS software: for information on this feature,
see Advanced Planning and Scheduling Integration (Opcenter APS).

2.10.2 Distributed Numerical Control (DNC)
In modern industrial environments, machine tools controlled through computers (Computer Numerical Control, or
CNC, machines) are widely used. In the past, however, CNC machines were not standardized and each machine had
to be programmed individually. DNC technology is designed to overcome these limitations.
Modern CNC machines often use "distributed" technology: the programs necessary for their operation are stored in
a separate computer and sent to the machines when they are required, one CNC package at a time.
This approach is called Distributed Numerical Control (DNC) and offers the following advantages:

Opcenter Execution Discrete 2507 - Product Overview

89


## Pagina 90

Basic Concepts
Integration with External Systems

• It permits the execution of complex programs that would be too large to be stored into the small memory of
most CNC machines.
• It centralizes the storage of programs, allowing for better maintenance and upgrade.

Integration with DNC systems
The product can interact with generic DNC systems through specific interfaces.
When appropriately configured, it can:
• Store references to CNC programs;
• Associate these references to Materials and Machines, so that the right program can be sent to the right machine
at the right moment.

2.10.3 Closed-Loop Manufacturing
Closed-Loop manufacturing (CLM) focuses on providing a way to bring together product engineering and process
planning with production execution and automation. By adopting a circular exchange of both engineering and
runtime data (that is, data exchange follows a closed loop), any variations or corrective measures necessary for
improving overall performance levels can be implemented rapidly. Feedback from the shopfloor is essential to
determine whether the decisions made in regard to product engineering and production-process scheduling are on
target.
In Opcenter Execution Discrete, a Closed-Loop manufacturing solution can be achieved through integration with
Teamcenter and SAP.

2.10.4 Structured Messages
Certain activities can be automated during production execution thanks to the exchange of structured messages.
Structured messages are XML files containing a series of tags that are presented in a particular layout: these tags are
designed to contain specific information that, upon validation, automatically triggers the execution of certain
actions (for example, the collection of specific types of data, the start and completion of Work Order Operations,
etc.).
In Opcenter Execution Discrete, such messages can be exchanged between the MES layer and the Shop Floor,
provided that is integration with Opcenter Connect MOM 2504(Opcenter CN MOM).
For more information on how to configure the integration of Opcenter EX DS with the Shop Floor using Opcenter CN
MOM, refer to section How to Integrate Opcenter Execution Discrete with Opcenter Connect MOM of the Opcenter
Execution Discrete Installation and Configuration manual.

2.10.5 Import Data Flows
Thanks to the integration with Opcenter Connect MOM, which permits the exchange of structured messages
between the MES layer and the External System, it is possible to import and check existing data structures into
Opcenter Execution Discrete instead of modeling them from scratch, if the system is properly configured.
Each data structure must follow specific constraints to be properly imported and, after being imported, can be
managed only if it is validated by the system.
The product releases a set of predefined Import Data Flows but the user, if necessary, can configure custom Import
Data Flows, provided that data are organized according to a specific XML structure. The files can be provided also in
JSON format, then the system will transform them properly in XML format. For more information on JSON files, see
page JSON File for Full Work Orders of the Opcenter Execution Discrete Installation and Configuration Manual.

90

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 91

Basic Concepts
Integration with External Systems

Validated data are converted into the proper XML format through an XSLT: good nodes are then imported into the
database, while a log is created for bad nodes that have not been imported.
For more information on how to configure the integration with Opcenter Connect MOM, see section How to
Integrate Opcenter Execution Discrete with Opcenter Connect MOM of the Opcenter Execution Discrete Installation and
Configuration Manual.

Available Import Data Flows
Master Data

Data Flow Identifier

Materials

MTMD

Functional Codes

FCMD

Suppliers

SUPMD

ERP Orders

ERPLIST

Features, Feature Values, Options

FEATMD

Bills of Features

LOF

Bills of Materials

BOM

Master Plans, Root Process, Operations

BOP

Inspection Master Plans

IMP

Work Orders, imported from Master Plans or As Planned BOPs.

WorkOrder

Full Work Order, the entire Work Order structure is imported along with
Work Order Operation and Work Order Step data. If, either in the XML or
JSON file, a Master Plan or an As Planned BOP is indicated, the
information contained in the XML or JSON file will be merged with those
contained in the Master Plan or As Planned BOP.

FullWorkOrder

2.10.6 Output Messages
Output Messages are used to export data, either in JSON or XML format, that can then be consumed by thirdparties. The generated Messages are saved in the System File Store and they can be either:
• retrieved through a predefined business logic, which uses a dedicated event to notify that the Message is ready.
• sent to external systems, in the case of integration with either Data Integration System (DIS) or Opcenter
Connect MOM.

Opcenter Execution Discrete 2507 - Product Overview

91


## Pagina 92

Basic Concepts
Integration with External Systems

For additional information on how to send Output Messages in case of integration with Opcenter
Connect MOM, refer to the How to Send Output Messages to Opcenter Connect MOM section in the
Opcenter Execution Discrete Installation and Configuration Guide.
Instead, for more information on how to send Output Messages in case of integration with DIS, refer to
the Configuring Output Messages to Reach DIS section in the Opcenter Execution Discrete Installation
and Configuration Guide.
For each Output Message, the following items can be configured:
• Output Message Destinations, to choose if the Message must be retrieved internally or sent through either
Data Integration System or Opcenter Connect MOM. In addition, while configuring Message Destinations, you
can choose whether to generate the Message in JSON or XML format, depending on how it must be consumed.
• Output Message Definitions, to choose the Message Type to be generated and to properly configure its
structure. Once a Message Definition is released, the Output Message can be sent.
• Output Message Sections, containing information and data on the various entities involved in the production
process. The product releases a set of predefined Sections for each Message Type. Some Sections are
mandatory, whereas others are optional and can be enabled or not according to production needs, in order to
generate the Message with specific information.
If necessary, expert users can implement custom Output Message Sections. For more information, refer to the
How to Implement Custom Output Message Sections page in the Opcenter Execution Discrete Extensibility Guide.

Available Message Types
The product comes provided with the following Message Types:
• Work Order Output Message, to send information on the Work Order structure, for example its Operations and
the associated Specification Types.
• As Built Output Message, to send information on the status of a Work Order that is in progress, including
information on its Operations/Steps and their results.
• Operation Output Message, to send information on the Work Order Operation.
• Standard Output Message, to send information on the Material Tracking Unit.
• JIT/JIS Message (Just in Time/Just in Sequence), to send a Material call to internal or external Suppliers.
• Kanban Message, to request the automatic replenishment of Materials that have reached the warning threshold
to the Warehouse.

Output Messages in Conjunction with Production Flow Control Diagrams
One or more released Output Message Definitions can be associated with a Milestone of the Production Flow
Control Diagram, through the configuration of a predefined Production Flow Control Action. The Message is
automatically generated and sent as soon as the MTU to be produced reaches that specific Milestone at runtime.

2.10.6.1 Output Message Sections
Depending on the Output Message Type chosen while creating the Message Definition, the Sections contained in
each Output Message will vary:
• As Built
• Work Order and Work Order Operation
• Standard and JIT/JIS
• Kanban
The Header Section is included in all Message Types.
In addition, each Message contains the following parameters:
• Message Schema: name of the XSD file (used by external systems to validate the Message).

92

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 93

Basic Concepts
Integration with External Systems

• Message Type: for example, AsBuiltMessage.

Header
MESSAGE_INFO (Information on the Message):
• Adapter Name (visible only in case of external destinations).
• Identifier Template (ID)
• Type. Possible values:
• New, if the Message has been sent for the first time.
• Duplicate, if the same Message (with updated content) has been regenerated.
• Transmission Timestamp
• Message Definition
MESSAGE_SENDER (Information on where the Message has been generated):
• Plant Code
• Plant ERP Code
• Workplace
MESSAGE_DESTINATION
• Destination

As Built
Section Name

Description

Work Order Operation

Mandatory. Information on the Work Order Operation:
• Identifier (ID)
• Name
• Description
• Target Quantity
• Available Quantity
• Partial Worked Quantity
• Produced Quantity
• Reworked Quantity
• Scrapped Quantity
• Category
• Type
• Optional
• Skippable
• Status
• Previous Status
• Sequence
• Priority
• Estimated Start
• Estimated Duration
• Estimated End
• Actual Start
• Paused Duration
• Executed Duration
• Actual End

Opcenter Execution Discrete 2507 - Product Overview

93


## Pagina 94

Basic Concepts
Integration with External Systems

Section Name

Description

Work Order Step

Information on the Work Order Step:
• Identifier (ID)
• Name
• Description
• Target Quantity
• Available Quantity
• Partial Worked Quantity
• Produced Quantity
• Reworked Quantity
• Scrapped Quantity
• Category
• Optional
• Status
• Sequence
• Priority
• Estimated Start
• Estimated Duration
• Estimated End
• Actual Start
• Paused Duration
• Executed Duration
• Actual End

Machine

Information on the Machine:
• Identifier (ID)
• User

Produced Material

Mandatory. Information on the produced Material:
• Identifier (ID)
• Name
• Description
• Code
• Code Type
• Status
• Material
• Quantity (Qty)
• Unit of Measure (UoM)
• Weight
• Weight_UoM
• Volume
• Volume_UoM
• Current Result
• Current Reason

94

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 95

Basic Concepts
Integration with External Systems

Section Name

Description

Consumed Material

Information on the consumed Material:
• Identifier (ID)
• Specification Type
• Type
• Assembled Quantity
• Disassembled Quantity
• User
• Date
• Equipment
• Occurrence
• Logical Position
• Current Result
• Current Reason

Tool

Information on the used Tool:
• Identifier (ID)
• Name
• Description
• Definition ID
• Used Time
• Usage Number
• Usage Duration
• Current Result
• Current Reason
In case of Screwing Tools, the following additional parameters are
provided:
• Bolts Quantity
• Torque Maximum Value
• Torque Minimum Value
• Angle Maximum Value
• Angle Minimum Value
• The BOLTS sub-section. Each BOLT contains:
• Item
• Angle Value
• Torque Value
• Result
• Date

Opcenter Execution Discrete 2507 - Product Overview

95


## Pagina 96

Basic Concepts
Integration with External Systems

Section Name

Description

Work Instruction

Information on Work Instructions and related Operations:
• Name
• Description
• Definition ID
• Status
• Repeated
• Completed
• Current Result
• Current Reason
In addition, for each Operation the following sub-sections are
provided:
• SECTIONS, one for each Work Instruction. Each SECTION
contains the following information:
• Identifier (ID)
• Title
• Completed
• User
• STEPS, one for each Section. Each STEP contains the following
information:
• Identifier (ID)
• Title
• Type
• User
• Execution Date
• ITEM, one sub-section for each Step. Each ITEM contains the
following information:
• Identifier (ID)
• Label
• Value
• Date
• User
• Target
• Out Of Range
• Low Limit
• High Limit

Quality Inspection

Information on Quality Inspections:
• Inspection Value
• Failure ID
• Attribute
• Value
• Visual Failures
• Failure ID
• Failure Count
• Current Result
• Current Reason

96

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 97

Basic Concepts
Integration with External Systems

Section Name

Description

Non-Conformance

Information on Non-Conformances:
• Identifier (ID)
• Severity
• Status
• Context (for example, WorkOrderOperation)
• The FAILURES sub-section, containing the ID of the Failure
under which the Non-Conformance has been categorized.
For Non-Conformances related to Work Order Operations, the
following additional parameters are provided:
• Produced Material ID
• Code
• Code Type

Work Order and Work Order Operation
Section Name

Description

Work Order

Mandatory and available only for Work Order Messages. Information on the Work Order:
• Identifier (ID)
• Name
• Production Type
• Status
• Plant
• Final Material
• Quantity (Initial Quantity, Produced Quantity, Reworked Quantity, Scrapped Quantity)
• Sequence
• Due Date
• Priority
• Time (Estimated Duration, Estimated Start Time, Estimated End Time, Actual Start
Time, Actual End Time)
• Serial Number
• Identifier
• Name
• Code Type
• Code

Opcenter Execution Discrete 2507 - Product Overview

97


## Pagina 98

Basic Concepts
Integration with External Systems

Section Name

Description

Operation

Mandatory and available only for Work Order Operation Messages. Information on the
Work Order Operation:
• Identifier (ID)
• Name
• Description
• Status
• Sequence
• Priority
• Time (Estimated Duration, Estimated Start Time, Estimated End Time, Actual Start
Time, Actual End Time)

Machine

Information on the Machine to be used:
• Name
• Level
• Preferred (True or False)
• Associated Part Program
• Associated Print Job File
• Print Job Production Printer details
• Print Job File Source
• Product Serializable (True or False)
• Runtime Only (True or False)
• Print Job File External Id

Material

Information on the Materials to be consumed:
• Name
• Revision
• Specification Type
• Quantity
• Unit of Measure

Tool

Information on the Tool to be used:
• Identifier (ID)
• Name
• Revision
• Times To Be Used

98

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 99

Basic Concepts
Integration with External Systems

Section Name

Description

Quality
Inspections

Information on associated Quality Inspections:

Work
Instructions

Information on associated Work Instructions:

Skill

Information on associated Skills:

• Identifier (ID)
• Name
• Revision of the Quality Inspection
• Sample Size
• Inspection Definition Item:
• Identifier
• Name
• Quality Characteristic Identifier
• User Id
• Criticality Identifier
• Characteristic Type
• Characteristic Context
• Revision of the Inspection Definition Item

• Identifier (ID)
• Name
• Revision
• Association Type

• Identifier (ID)
• Name
• Level
Human
Resources

Information on associated Humans Resources:

Users

Information on associated Users:

• Name
• Certificate Identifier
• Certificate Name
• Certificate Description
• Number of Users

• Associated Users
• User Identifier

Standard and JIT/JIS

Opcenter Execution Discrete 2507 - Product Overview

99


## Pagina 100

Basic Concepts
Integration with External Systems

Section Name

Description

Material Tracking Unit

Mandatory for both Standard and JIT/JIS. Information on the
Material Tracking Unit:
• Name
• Serial Number
• Code Type
• Line Sequence

ERP Order

Filled with data only if an ERP Order is already linked to an MTU to
be produced. Information on the ERP Order:
• Identifier (ID)
• Final Product Type
• Final Product Family
• Final Material
• Production Type
• Production Starting Date
• Delivery date
• Customer Type
• Serial Number

Bill of Materials

Mandatory only for JIT/JIS. Information on the Materials, making
up the BoM, associated with the MTU or with the ERP Order to be
produced:
• Identifier (ID)
• Name
• Description
• Functional Code
• List of Suppliers
• Quantity
• Consumed Quantity, specific to Line Side Positions and related
Kanban Calls
• Unit of Measure
If the Message is of type JIT/JIS, additional filters can be applied, in
order to request either single Materials, or Materials from specific
Suppliers and with specific Functional Codes, specifying their
quantity as well.
The Bill of Materials to be used is identified following these priority
rules, in the order in which they are listed:
• the frozen Bill of Materials associated with the MTU.
• if the ERP Order is already linked to the MTU, the frozen Bill of
Materials associated with the ERP Order.
• if the MTU is linked to an ERP Order, but the Bill of Materials
associated with the ERP Order is not yet frozen, the Bill of
Materials associated with the Final Product Type/Final Product
Family.

100

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 101

Basic Concepts
Integration with External Systems

Section Name

Description

Bill of Features

Information on the Bill of Features associated with the Product
Configuration and with the MTU and ERP Order to be produced:
• Product Configuration description
• Features and associated Feature Values
• Options
The Bill of Features to be used is identified following these priority
rules, in the order in which they are listed:
• the frozen Bill of Features associated with the MTU.
• if the ERP Order is already linked to the MTU, the frozen Bill of
Features associated with the ERP Order.
• if the MTU is linked to an ERP Order, but the Bill of Features
associated with the ERP Order is not yet frozen, the Bill of
Features associated with the Final Product Type/Final Product
Family.

Production Flow Control History

Information on the Milestones reached by the MTU:
• Milestone Identifier
• Milestone Name
• Workplace associated with the Milestone
• Timestamp of the operation

Traceability Operations

Information on the Traceability Operations performed on the MTU:
• Identifier (ID)
• Serial Number
• Name
• Description
• Result and state
• Barcode Rule associated with the Material
• Material and Serial Number traced
• Workplace
• User

Opcenter Execution Discrete 2507 - Product Overview

101


## Pagina 102

Basic Concepts
Integration with External Systems

Section Name

Description

Generic Data Collection

Information on collected data and related Operations:
• Identifier (ID)
• Name
• Description
• Current Result
• Current Reason
• Status
In addition, for each Operation the following sub-sections are
provided:
• DATA_COLLECTION, one for each Operation, containing
information on the Data Collection:
• Identifier
• Revision
• SECTIONS, one for each Data Collection. Each SECTION
contains the following information:
• Identifier
• Title
• STEPS, one for each Section. Each STEP contains the following
information:
• Identifier
• Title
• Timestamp
• User
• CHARACTERISTICS, one sub-section for each Step.
Each CHARACTERISTIC contains the following information:
• Label
• Value
• UoM

102

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 103

Basic Concepts
Integration with External Systems

Section Name

Description

Screwing Operations

Information on Screwing Operations:
• Operation Identifier
• Name
• Description
• Current Result
• Current Reason
• Status
• Workplace
• User
• Timestamp of the operation
In addition, for each Operation, the Tool Instance sub-section is
provided with the following information about the Automation
Node Instance:
• Identifier (ID)
• Torque Minimum Value
• Torque Maximum Value
• Angle Maximum Value
• Angle Minimum Value
• Bolts Quantity
• The list of bolts containing:
• Bolt identifier
• Torque Value
• Angle Value

Opcenter Execution Discrete 2507 - Product Overview

103


## Pagina 104

Basic Concepts
Integration with External Systems

Section Name

Description

Open Protocol Operations

It can be used solely if the OpenProtocolDS extension app has
been installed and the Open Protocol Service asset has been
configured. Information on Open Protocol Operations:
• Operation Identifier (ID)
• Name
• Description
• Current Result
• Current Reason
• Status
• Workplace
• User
• Timestamp of the operation
In addition, for each Operation, the Tool Instance sub-section
contains, for each Tool Instance Identifier, the related Psets/
Rework Psets (Program Number/Rework Program Number) and
information about the rundowns:
• RUNDOWN_MEASUREMENTS containing:
• Name
• High Limit
• Low Limit
• Result
• Decimal Value
• Target
• RUNDOWN_NODE_VALUES containing:
• Field Key
• Field Value

Delivery Point

Available only for JIT/JIS. Information on the Workplace where the
Materials must be delivered.

Kanban
The Kanban Message contains, a part from the Header Section, only the mandatory Kanban Call Section,
containing information on the Kanban Call and the requested Material:
• Kanban Call Identifier
• Mode (Automatic or Manual)
• Priority
• Quantity of Bins requested
• Quantity of Material expected
• Delivery Point
• Kanban Call Status
• Material Identifier
• Material Revision
• Material Name
• Actual Quantity
• Unit Of Measure

104

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 105

Basic Concepts
Integration with External Systems

2.10.7 Kanban Calls
Kanban Calls represent a message exchange with the external system managing the Warehouse, performed through
output messages containing the requests, that are sent by Opcenter EX DS, and input messages containing the
answers, that come from the external system.
While the Kanban Call is in progress, the system does not send other calls for the same Material in the same
Equipment.
Once a Kanban Call is delivered, the quantity in the Line Side Position is automatically increased with the quantity
received, which is added to the current quantity.
Each Kanban Call is associated with a State Machine with a predefined list of states and transitions, to track and
monitor at runtime the progression of each request associated with the Line Side Position.

Possible State Transitions for Kanban Calls
Source Status

Possible Target States

Open

In Progress

Open

Cancelling

In Progress

Cancelling

Cancelling

Cancelled

In Progress

Shipped

Shipped

Delivered

Example of Kanban Call State Machine

Opcenter Execution Discrete 2507 - Product Overview

105


## Pagina 106

Basic Concepts
Support of Hybrid Scenarios Englobing Opcenter Execution Process

2.10.8 Teamcenter Share
Teamcenter Share is a collaborative cloud environment to which products across the Siemens Xcelerator
portfolio can connect in order to collaborate on design and engineering projects in the cloud.
Opcenter Execution Discrete can benefit from this integration by sharing production-related information, such as
Documents collected at runtime from the Shop Floor or Documents attached to Non-Conformances, with other
users.
For more information on this integration, see Integration with Teamcenter Share.

2.10.9 Additive Manufacturing Network
Additive Manufacturing Network is a Siemens cloud-based solution designed to optimize execution activities in a
capillary manner, from sales orders to delivery, specifically dedicated to meet the needs of Additive Manufacturing
production.
Thanks to the exchange of information between Opcenter Execution Discrete and Additive Manufacturing Network,
a series of items can be imported into Opcenter EX DS to streamline Shop Floor operations.
In addition, Additive Manufacturing Network can be notified as to any change in Opcenter EX DS production status:
therefore, thanks to this functionality, overall visibility on the production process is provided and order status can
be tracked in a fast and simple way.
For more information on this integration, see Integration with Additive Manufacturing Network.

2.10.10 Intraplant Logistics (IPL)
Thanks to dedicated integration, it is possible to take advantage of intraplant logistics capabilities, which include:
• inventory management and tracking
• Kanban-call and JIS/JIT management
permitting the flow of appropriate material to be used in production.
Opcenter Execution Discrete offers the possibility of integration with intraplant logistics software: for information
on this feature, see Integration with Opcenter Intraplant Logistics (Opcenter IPL).

2.11 Support of Hybrid Scenarios Englobing Opcenter Execution
Process
It is possible to host both Opcenter Execution Discrete and Opcenter Execution Process on the same machine to
satisfy the needs of a Hybrid scenario, in which both products concur in an overall production process: the same
plant employs a batch or semi-finished material produced via Opcenter Execution Process to manufacture a final
product by way of Opcenter EX DS. This also permits end-to-end traceability, covering both aspects of the entire
production process.

106

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 107

Product Features
Support of Hybrid Scenarios Englobing Opcenter Execution Process

3 Product Features
Here are the main features offered by Opcenter Execution Discrete: see how its functionalities and business logic
can satisfy the needs of your business.

User Management
• Access Control through Roles and Certifications
• Team Management
• Labor Tracking
• System Localization

Production Management
• Native Data Definition and Management for Engineering and Runtime Needs
• Operation/Step Category Management
• Material Management
• Container Management
• Tool Management
• Screwing Tool Management
• Open Protocol Tool Management
• Barcode Management
• ID and Serial Number Generation
• Readily-Available Work Instructions and Documents
• Functionalities for As Planned BOP, Master Plan and Process Management
• Feature Management
• Product Configuration Management
• Production Flow Control Management
• Qualification Criteria Management for Master Plan Contexts
• Dedicated Catalogs for Reusing Processes, Operations and Steps
• Versatile Work Order Management
• Alternative Paths for Operation Execution
• Pre-Kitting for Reserving Specific Material Tracking Units

Production Execution
• Runtime Work Order Execution
• Result Management
• Interlocking Checks for Governing Work Order Operation Execution
• Exchange of Messages with the Shop Floor
• Adoption of Execution Groups for Maximizing Productivity
• On-The-Fly Management of Changes to the Production Process
• Change Package Management
• Work Order Dispatching
• Order Work in Progress (WIP) monitoring
• Use of Tasks for Managing Work Order Operation/Step Progression
• Runtime Data Collection Capabilities
• Semi-Automatic Acquisition of Values
• Runtime Behavior for Machines and Tools
• Non-Productive Activity Management
• Label Printing
• Work Order Operation Execution Using the High Automation User Interface
• Production Execution in Offline Mode
• Line Side Inventory and Kanban Call Management

Opcenter Execution Discrete 2507 - Product Overview

107


## Pagina 108

Product Features
Access Control through Roles and Certifications

• Monitoring of the Production Status
• Quality Gate Management

Quality Control
• Non-Conformances and Rework Codes for Runtime Quality Management
• Electronic Signature and Buy-Off Management
• Data Tracing for Production Activities
• Quality Inspections

Integration
• Advanced Planning and Scheduling Integration (Opcenter APS)
• Integration with Teamcenter and SAP
• Integration with Generic Distributed Numerical Control (DNC) Systems
• Integration with Opcenter Connect MOM
• Integration with Teamcenter Share
• Integration with the Shop Floor via OPC UA
• Integration with Intraplant Logistics (Opcenter IPL)

Additive Manufacturing
• Integration with Additive Manufacturing Network
• Powder Batch Management
• Substrate Management
• Print Job File Management
• Print Job File Pre-Transfer Management

Intra-Plant Logistics
• Management of Intra-Plant Logistics

3.1 Access Control through Roles and Certifications
In Opcenter Execution Discrete, access control is governed by:
• Roles
In addition to the standard set of Roles that covers the most common figures involved in Discrete Manufacturing
and is installed by default, it is possible to add custom Roles to satisfy your needs.
• Certifications
When adopted in conjunction with Skills, it simplifies the task of defining and establishing the bounds as to
where, within a production plant, a User or Role may perform certain operations to manufacture
certain materials using certain machines: the end results are a higher level of security on all levels within your
business and a significant reduction of the margin of error in production execution

Features regarding Users, Groups and Roles
If you are a Super-User, you can:
• Create new Users and Groups.
• Associate Users with Groups, so that you can grant individual and group access to Opcenter EX DS.
• Associate Users and Groups with Roles.
• Import Users and Groups from Windows Active Directory, to achieve perfect alignment with the Users and
Groups in Opcenter Execution Discrete.

108

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 109

Product Features
Team Management

Features regarding Certifications
As a Product Engineer, to grant ad-hoc access to specific operator functions, you can also create Certifications
containing specific discriminating elements and assign them to the users and Roles present in your system.
In detail, you can:
• Create a blank Certification.
• Associate/remove one or more:
• Materials
• Workcenters
• Equipment Types
• Skills
to/from a Certification.
• Assign (associate) a Certification to a User or Role, setting an expiration date.
• Remove a Certification from a User or Role.
• Update Certification details.
• Delete one or more Certifications, either individually or in one shot.
• Configure one or more Skills to be assigned to specific Users or Roles through Certifications, or associated to
Process Operations and/or Work Order Operations.
• Configure the required Certifications to be possessed by either a single user or a team to start a Work Order
Operation/Step.

3.2 Team Management
The adoption of Teams makes it possible to exploit the capabilities of your workforce to the best possible
advantage, grouping the individuals with the right characteristics together to achieve a certain goal.
Provided you have been assigned with the appropriate Role (Production Coordinator), you can:
• define a Team, including the specific conditions that must be satisfied in order for a person to join it (for
example, some Teams may not have more than a certain number of Team members, or only Operators who
possess certain Skills may join a specific Team).
• assign and unassign Team members to/from a Team.
Operators can join and leave a specific Team: it is not allowed to belong to more than one Team at the same time.
The system tracks the activities performed as a single User and those performed as a Team member separately.
Activities performed by a Team are also tracked in the As Built and Genealogy reports.

3.3 Labor Tracking
Analyzing data regarding the time spent in executing a Work Order is crucial to properly allocating costs in order to
achieve benefits on both the production and profit levels.
In the Production Coordinator Time Update screen, you can update the logged actions (Start,
Pause, Complete) for the selected Work Order Operation and (for completed Work Order Operations) add other
actions (Start, Pause, Complete) .
As a Production Coordinator, you can:
• View the actions performed by an Operator on a specific Work Order.
• Check all times collected during production execution to verify whether they are correct and, if
necessary, update the Labor Time.
• Modify the timestamps for the Actual Start Times and Actual End Times.
• Update an action (Start, Pause, Complete) to the log to rectify what has already been entered by an Operator.

Opcenter Execution Discrete 2507 - Product Overview

109


## Pagina 110

Product Features
System Localization

3.4 System Localization
By default, Opcenter Execution Discrete is provided in English. User Interface localized resources are available in
the Download > Additional Downloads area of the Support Center at https://support.sw.siemens.com/enUS/ after clicking the Opcenter Execution Discrete home card.
However, from a linguistic standpoint, it can be extended to satisfy any needs your business may have in a global
sense. Thanks to its system localization capabilities, Opcenter EX DS supports multiple languages. In addition,
it allows you to add translations for implementing new languages.
By adding dedicated translation files, you can implement new languages for your Opcenter EX DS application so
that your system can be deployed in different countries: see section How to Use Opcenter Execution Discrete in
Multilanguage in the Opcenter Execution Discrete Installation Manual.
In all cases, Unicode characters are supported.

3.5 Native Data Definition and Management for Engineering and
Runtime Needs
In all businesses, data management represents a challenge. Numerous MES entities are involved in your day-to-day
production processes.

Engineering
Opcenter Execution Discrete offers native Engineering data definition: you can define your entities so that it is
possible to model Engineering data (products, their production process and required resources) for your
production operations.

Engineering data definition
As a Product Engineer, you can define the following entities:
• Equipment Levels
• Machines
• Tool Definitions
• Materials (part numbers/products; that is, materials to be consumed, as well as those to be produced)
• Identifier formats
• As Planned BOPs, Processes and Process Operations
• Operation/Step Categories
• Reasons
• Defects, Failures and their related elements
• Rework Codes
• Work Operations
• Certifications
• Work Instruction Definitions
• Buffer Definitions.
For modeling specialized business behavior, Opcenter EX DS comes provided with a predefined list of Work
Order production types (that is, production is executed by portion of a batch, a batch in its entirety or single
element).

Runtime
Work Orders, Work Order Operations, Tools and Material Tracking Units (Serial Numbers and Batches) represent the
pivot around which the main Runtime features offered by Opcenter Execution Discrete revolve. By appropriately

110

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 111

Product Features
Operation/Step Category Management

defining your Work Orders, you can determine the activities and resources you need to produce a certain quantity
of a specified product and subsequently plan execution.
This makes it possible for you as an Operator to perform your planned tasks correctly.
If you are a Production Coordinator, Opcenter EX DS provides you with real-time visibility regarding any work in
progress (WIP). You will be able to know which operations are being carried out on which machine and how far
along the job is to completion.
By defining Batches and Serial Numbers, it will be a simple task for you to identify the materials on the shop-floor
and their relationship to each other (for example, assembly).

Runtime Data Definition
As a Production Coordinator, you can:
• Define Batches and Serial Numbers.
• Define Tools for use in Runtime.
If necessary, you can also:
• Define Work Orders on the basis of an existing Process.
• Define Work Orders manually.

Runtime Data Management
Opcenter EX DS guides you in executing a number of Work Order Operations, so that you can work more efficiently
and achieve your production targets with greater ease.
As an Operator, you can:
• Start a Work Order Operation.
• Pause an active Work Order Operation.
• Skip a Work Order Operation.
• Complete an active Work Order Operation.

These Work Order Operations are feasible only if the operation you want to perform is in a status that
permits its execution: the system also takes the Work Order's status into consideration before allowing
you to proceed. Once the Work Order Operation is executed, Opcenter EX DS will change the Work Order's
status accordingly. For more information, see States and Lifecycles.
In particular, depending on configuration and use case, whenever you start or complete a Work Order Operation,
you will need to either make a selection (for example, on which machine the operation starts) or enter data (for
example, which components will be consumed/assembled; good/rework/scrap counters; which components have
been consumed/assembled; how many times a certain Tool has been used, etc.).

3.6 Operation/Step Category Management
Operation/Step Categories can be used to classify Process Operations, Process Steps, Work Order Operations and
Work Order Steps according to their purpose (for example, "Manual Assembly", "Automatic Assembly", "Cutting",
"Traceability").
Furthermore, in conjunction with the Opcenter Execution Foundation BPFlow App, you can associate Operation/
Step Categories to Process Definitions, so that, providing dedicated custom business logic, the workflows
represented by the Process Definitions are automatically triggered at runtime when, for example, the Work Order
Operation is started.

Opcenter Execution Discrete 2507 - Product Overview

111


## Pagina 112

Product Features
Material Management

Operation/Step Categories can be used to configure the system so that, thanks to dedicated business logic, runtime
screens are automatically displayed on the basis of Work Order Operation attributes. In addition, you can associate
Interlocking Checks to Operation/Step categories. At runtime, the execution of these Interlocking Checks will be
triggered for all Work Order Operations classified with that specific Operation/Step category and for which no
specific Interlocking Checks are associated.
Opcenter Execution Discrete comes provided with:
• a default Operation/Step Category, which will be automatically set for the entity (Process Operation, Process
Step, Work Order Operation, Work Order Step) should no value for the corresponding property be specified at
the time of its configuration. In this case, standard runtime Opcenter EX DS screens will be displayed.
• additional Operation/Step Categories, derived from the default Operation/Step Category, each representing a
specific workflow. In this case, if the value for the corresponding property is specified at the time of the entity
configuration, only the necessary runtime screens will be displayed.
• an Operation/Step Category specific to Additive Manufacturing, dedicated to 3D Printers setup during 3D
printing processes.
As a Product Engineer/Production Coordinator, you can:
• create Operation/Step Categories.
• edit Operation/Step Categories.
• delete Operation/Step Categories.
• associate Operation/Step Categories to Process Definitions (also in conjunction with Machines and/or
Materials).
• activate associations between Operation/Step Categories and Process Definitions.
• remove associations between Operation/Step Categories and Process Definitions.
• set Serialized behavior for the associations between Operation/Step Categories and Process Definitions.
• provide Operation/Step Categories with Interlocking Checks.

3.7 Material Management
Depending on your User Role, Opcenter Execution Discrete provides you with the means for performing
various operations in relation to material management.
As a Product Engineer, you can:
• Create Materials that will be used to instantiate Material Tracking Units in runtime. This can be done in one of
the following ways:
• Create a Material from scratch.
• Copy an existing Material.
• Create a Revision of an existing Material.
• Associate Materials to Processes and/or Work Orders to represent the final materials to be produced.
• Associate Materials to Process Operations and Process Steps to be consumed/assembled or produced in various
ways (including Co-Product and By-Product production).
• Associate Materials to Work Order Operations and Work Order Steps to be consumed/assembled or produced in
various ways (including Co-Product and By-Product production).
In this context, the Work Order has not yet been released for production.
• Delete one or more Materials.
As a Production Coordinator, you can:
• Instantiate Material Tracking Units from Materials.
• Assemble Material Tracking Units.
• Disassemble Material Tracking Units (both in full and in part).
• View historical data about Material Tracking Units.

112

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 113

Product Features
Container Management

As an Operator, you can:
• Enter values about Material Tracking Unit consumption/assembly or production manually.
• Acquire values about Material Tracking Unit consumption/assembly or production from the field and then
confirm them.
• Upload Documents to individual Material Tracking Units.
• Assemble Material Tracking Units.
• Disassemble Material Tracking Units (both in full and in part).
• View historical data about Material Tracking Units.

3.8 Container Management
Adopting Containers in a plant simplifies the movement and identification of Material Tracking Units (be they
finished, semi-finished products or materials to be consumed) in the course of production. For example, it may be
practical to use Containers, which have a unique identifier, to carry items the unique identifier of which does not
yet exist or is not visible.
Once defined, Containers can be either reserved for a specific Work Order or made available to various Work Orders,
provided that the Container has been defined compatible with their to be produced or consumed Materials.
Containers can be loaded with different Materials in different production processes: however, even if a Container is
compatible with various Materials, it cannot contain more than one Material at the same time. Once the first
Material Tracking Unit has been loaded into the Container, only other MTUs belonging to the same Material can be
loaded therein, even if there exist other Materials compatible with that particular Container. Only at the end of the
production process, provided that the Container has been configured as reusable and once all its contents have
been unloaded, it will be possible to load it with other MTUs belonging to another compatible Material.
Containers can be configured as desired within each plant according to production needs. In some cases, it may be
necessary to define Containers for holding several items (the maximum amount of which must be defined in
advance for each Material); in other cases, it may be useful to configure Containers to hold a single large item (for
example, a gearbox).
It is also possible to use more than one Container during the execution of a single Work Order Operation, or for
managing the produced material partially through Containers or without them. This approach is necessary if the
Work Order involves a Quantity exceeding the maximum allowed to be held by a Container: for example, if the Work
Order must produce 10 pieces and Containers designed to hold no more than 2 pieces must be used, you can
choose to use either the same Container 5 times (but this may slow down production), or use 5 distinct Containers
(or any other reasonable combination).
If a Container has been reserved by the Production Coordinator for a specific Work Order, it is automatically
associated to all its Work Order Operations: this information is transmitted to the Operator working on the
production line.
If the Container has not been reserved, the Operator can associate it to any compatible Work Order Operation
requiring a Container immediately before starting its execution.
Both the Production Coordinator and the Operator can load or unload Material Tracking Units working from
different UI pages. Only the Operator can start the execution of Work Order Operations on Containers, but the
Production Coordinator can access the list of Material Tracking Units loaded into each Container and the associated
Work Order, thus easily identifying for example a Container that is stuck because it is currently associated to a
scrapped Work Order.
Given that the system can track where a Container is located at runtime, Containers are associated with a location
that can belong to any level of the Equipment Configuration hierarchy: for example, full Containers are usually
located in the vicinity of a given Equipment, whereas empty Containers can be located inside a warehouse.
Once the association between a Work Order Operation and a Container is established, the Operator uses the ID of
the Container (and not the IDs of its content) for any operation (Start, Pause and Complete) until the content is
unloaded. This association is removed only when a Container has been completely unloaded. Once a Work Order

Opcenter Execution Discrete 2507 - Product Overview

113


## Pagina 114

Product Features
Tool Management

Operation associated to Containers has been started, all the Material Tracking Units that have been loaded into
those Containers, as well as those MTUs managed without Containers in the current Work Order Operation, will be
started. The same is true when pausing or completing the Work Order Operation.
During production execution, the Operator can manage some typical runtime activities, such as using Tools or
consuming Material Tracking Units, directly on the Container, without knowing on which Material Tracking Units
(loaded in the Container) these activities apply. The entire content of the Container automatically inherits
(appropriately rescaled) the activities performed on the Container itself.
In Additive Manufacturing contexts, both the Production Coordinator and the Operator can load or unload Powder
Material Batches and connect Containers to 3D Printers working from different UI pages.
During production execution, the Operator can manage some typical runtime activities, such as consuming Powder
Material Batches loaded in Containers or tracking Powder Material Batches loaded in Containers and used during
3D printing operations.
As a Product Engineer or Production Coordinator, you can:
• create Container Types and Containers
• set Container re-usability
• (in Additive Manufacturing context) set Powder Containers to be used for Powder Material Batches
• define Compatible Materials
• preload Containers with Material Tracking Units
• (in Additive Manufacturing context) preload Containers with Powder Material Batches
• unload Containers to troubleshoot production issues
• reserve Containers for specific Work Orders
• (in Additive Manufacturing context) replenish the quantity of Powder Material Batches loaded in Containers
• (in Additive Manufacturing context) connect Containers to 3D Printers.
As an Operator, you can:
• associate Containers with Work Order Operations
• load Containers with Material Tracking Units
• (in Additive Manufacturing context) load Containers with Powder Material Batches
• (in Additive Manufacturing context) replenish the quantity of Powder Material Batches loaded in Containers
• (in Additive Manufacturing context) connect Containers to 3D Printers
• scan Containers to automatically provide the MTUs to be consumed
• start Work Order Operations on Containers and perform the following runtime activities:
• use Tools
• consume Material Tracking Units
• consume and track Powder Material Batches used during 3D printing operations
• manage Work Instructions
• manage Quality Inspections
• add documents on-the-fly
• pause Work Order Operations on Containers
• complete Work Order Operations on Containers
• unload Containers either partially or completely.

3.9 Tool Management
Depending on your User Role, Opcenter Execution Discrete provides you with the means for performing
various operations in relation to Tool management.
As a Product Engineer, you can:
• Create Tool Definitions that will be used to instantiate Tools in runtime.

114

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 115

Product Features
Screwing Tool Management

• Configure whether a Tool Definition must be set as Lockable in order to define which resources cannot be used
concurrently during execution.
• Associate Tool Definitions to Process Operations and Process Steps (these associations are known as Tool
Specifications).
• Associate Tool Definitions to Work Order Operations and Work Order Steps (also these associations are known
as Tool Specifications).
In this context, the Work Order is not active.
• Update (modify) existing Tool Definitions, thereby creating Revisions.
• Delete one or more Tool Definitions.
Usage thresholds and expiration dates for Tools based on usage at runtime are optional, and can be specified to
avoid using worn-out or expired Tools.
The system automatically increments:
• The counter for the number of times a Tool is used, each time it is used at runtime.
• The current usage time of a Tool based on runtime usage.
When any of the aforementioned thresholds is exceeded, the corresponding Tool will automatically be set to a
status that forbids its use at runtime.
As a Production Coordinator, you can:
• Instantiate Tools from Tool Definitions.
• Lock appropriately-configured Tools so that they can be used only by a specific User for a specific Work Order
Operation on a specific Machine.
• View historical data about Tools.
As an Operator, you can:
• Enter values about Tool usage manually.
• Acquire values about Tool usage from the field and then confirm them.
• View historical data about Tool usage.

3.10 Screwing Tool Management
Screwing Tools (for example, Screwdrivers) are specific Tools used during the execution of Work Order Operations
of type Screwing (for example, those operations required for installing wheels on the vehicle).
If the system is properly configured and linked to the Shop Floor via the Opcenter Execution Foundation
Automation App, values from the field can be automatically acquired for Screwing Tools.
In addition, if the proper Logistic Class is selected at the moment of the Screwing Tool Definition creation, a
predefined Automation Node Type called SCREWDRIVER is automatically associated to the Screwing Tool
Definition from which the Screwing Tool is instantiated. The predefined Automation Node Type includes a set of
predefined Automation Node Parameters, described in detail in the table below.
The Screwing Tool must then be associated to the Automation Node Instance previously created (in turn associated
to the predefined Automation Node Type).
At runtime, each Operation of type screwing is associated to a specific Screwdriver (for example, Screwdriver001).
The Automation Node Instance is an abstract entity which represents the Screwdriver and which inherits the
parameters of the related Automation Node Type, thus enabling the exchange of data with the field at runtime,
such as the actual torque or the actual angle applied during the Screwing operation. This information updates
automatically each time the Automation Layer communicates with the system, updating the operation result as
well, also on the basis of the completed screws.

Opcenter Execution Discrete 2507 - Product Overview

115


## Pagina 116

Product Features
Screwing Tool Management

As a Product Engineer, you can:
• create Screwing Tool Definitions that will be used to instantiate Screwing Tools (for example, Screwdrivers) in
runtime.
• associate Screwing Tool Definitions to Process Operations (these associations are known as Tool Specifications).
• update (modify) existing Screwing Tool Definitions, thereby creating Revisions.
• delete one or more Screwing Tool Definitions.
As a Production Coordinator, you can:
• instantiate Screwing Tools from Screwing Tool Definitions.
• view historical data about Screwing Tools.
• move a Screwing Tool from the specific Equipment (for example, Workplace or Unit) to another.
As an Operator, you can:
• acquire values about Screwing Tool usage from the field and monitor them.
• view historical data about Screwing Tool usage.

Predefined Parameters of the default Automation Node Type
Id

Data Type

Description

ActivatedOn

String

Written and updated by the MES system. Contains
information related to the current operation activated on
a specific Automation Node Instance.

ActualAngle

Real

Written by the field. Actual angle of the screwing
operation that has been executed.

ActualTorque

Real

Written by the field. Actual torque of the screwing
operation that has been executed.

Angle_HL

Real

Highest limit of the angle. Sent by the MES system to set
a range of values for the actual Screwdriver.

Angle_LL

Real

Lowest limit of the angle. Sent by the MES system to set a
range of values for the actual Screwdriver.

CurrentBolt

DInt

Written by the field. Progressive identifier (from 1 to
NumberOfBolts value) of the bolts screwed during the
operation.

DeactivatedOn

String

Written and updated by the field. Contains the
information related to the current operation deactivated
on a specific Automation Node Instance (either by the
operator or the Screwdriver).

NumberOfBolts

DInt

Sent by the MES system. Number of total bolts to be
screwed by the actual Screwdriver.

116

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 117

Product Features
Open Protocol Tool Management

Id

Data Type

Description

Torque_HL

Real

Highest limit of the torque. Sent by the MES system to set
a range of values for the Screwdriver.

Torque_LL

Real

Lowest limit of the torque. Sent by the MES system to set
a range of values for the Screwdriver.

Status

String

State of the Screwdriver. It must be in Ready status,
otherwise the Operation is not executed (negative result
NOK) with reason Tool Not Ready.

3.11 Open Protocol Tool Management
To take advantage of the Open Protocol Tool functionality, you must have configured the Open Protocol
Service asset and installed the following Opcenter Execution Discrete Extension Apps:
• OpenProtocolDS
• BoPOPRT
• ImportOPRT
In addition, you must have deployed the Opcenter EX DS One Piece Flow Low Code UI App, in order to use
Open Protocol Tools at runtime in Opcenter Execution Discrete.
The Open Protocol Service asset provides you with the possibility to configure and monitor shop-floor Tools known
as Open Protocol Nodes, that communicate via TCP/IP protocol.
The Open Protocol Service is a Windows service that operates as a bridge between Open Protocol Nodes and the
MES System, through the exchange of Open Protocol Messages.
Open Protocol Nodes are able to receive a Program Number, execute the required actions evaluating the collected
data (including upper and lower tolerance limits), and then send back the results to the MES system.
If the Open Protocol Service asset has been properly configured, the Open Protocol Node communicates with the
Opcenter EX DS Open Protocol Tool, that is used during the execution of Work Order Operations of
type OpenProtocol. This communication between the Node and the Tool permits the user to acquire values from
the field via TCP/IP protocol and view the result of the Operation at runtime.
As a Product Engineer, you can:
• create Open Protocol Tool Definitions with logistic class OpenProtocol, that will be used to instantiate Open
Protocol Tools at runtime.
• associate Open Protocol Tool Definitions to Process Operations (these associations are known as Tool
Specifications). While creating this association, you can also set the Program Number, that represents the
identifier of the Program containing the instructions of the rundown to be executed, and the Rework Program
Number, needed in case the operation must be repaired at the Quality Gate.
• update (modify) existing Open Protocol Tool Definitions.
• delete one or more Open Protocol Tool Definitions.
As a Production Coordinator, you can:
• instantiate Open Protocol Tools from Open Protocol Tool Definitions, and then associate the Open Protocol
Node (previously created using the Open Protocol Service asset) with the Open Protocol Tool and
the Equipment (to indicate where the Open Protocol Node is located).

Opcenter Execution Discrete 2507 - Product Overview

117


## Pagina 118

Product Features
Barcode Management

• modify the Equipment (for example, Workplace or Unit) associated with the Open Protocol Tool.
As an Operator, you can:
• view and monitor values about Open Protocol Tool usage from the field, as well as the Operation result.
• view data about Open Protocol Tools in terms of completed rundowns and the values acquired for each
rundown.
• if needed, bypass an Operation.
• if needed, repair the Operation at the Quality Gate. The Operation can be repaired automatically or manually.
In addition, thanks to the integration with Opcenter Connect MOM, both the XML file for importing Master Plans and
the Output Message (Standard and JIT/JIS) include a section dedicated to Open Protocol Operations.

3.12 Barcode Management
Opcenter Execution Discrete provides the possibility of configuring Barcode Rules to validate a Barcode string.
Once created, Barcode Rules are empty containers which can be associated with Rule Parts in any combination you
deem necessary, each of them containing a regular expression which will be used to validate the Barcode string.
Whenever a Barcode string is received from a Barcode reader, the system automatically retrieves the corresponding
rule from the associated Material. If the rule is not found, the system retrieves it from the Functional Code or, as a
last option, from the rule associated to the Final Product Type.
A Default Barcode rule is also provided out-of-the-box and can be set thanks to a dedicated configuration key.
In addition, it is possible to view the History of each Barcode reading executed at runtime to know which ones are
valid or not.
For information on further functionalities provided refer to the Barcode App documentation in the Opcenter EX FN
User Manual.
As a Product Engineer or Production Coordinator, you can:
• enable the dedicated configuration key for setting a default Barcode Rule.
• create a Barcode Rule.
• configure the Rule Parts.
• associate the Barcode Rule to one or more of the following items, according to your needs:
• Material
• Functional Code
• Final Product Type
As an Operator, you can scan the Barcode to validate the Material Tracking Unit to be consumed: if it matches the
Barcode Rule, its consumption can proceed.

3.13 ID and Serial Number Generation
In product versions previous to 4.3 this functionality was provided through Identifier Templates instead of
Numbering Patterns. For more information refer to the documentation of the previous product versions.

Opcenter Execution Discrete makes it possible for you to generate identifiers based on Numbering Patterns that
you, as a Product Engineer, can configure to meet your needs.
If you are a Product Engineer or Production Coordinator, whenever you create a new Work Order, Batch or Serial
Number, Opcenter EX DS allows you to request an ID based on the Numbering Pattern specifically configured for the
particular item you are creating.

118

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 119

Product Features
Readily-Available Work Instructions and Documents

In addition, it is practically error-free, because the chance of generating two identical serial numbers or an identifier
with the wrong format is very slim.

Associate Serial Number/Batch ID at Material Tracking Unit level
You can also generate Serial Numbers or Batch IDs at the Material Tracking Unit level in the edit mode.

On-the-Fly Changes to Serial Numbers
The Serial Numbers of the Material Tracking Units produced by a Serialized or Full Serialized Work Order can be
changed during the execution of the Work Order, provided that the Work Order in question has not been verified
(that is, it must not be in Verified status). Therefore, regardless of whether the Serial Numbers associated to the
Material Tracking Units produced by the Work Order were generated from a Numbering Pattern or not, they can be
replaced with new Serial Numbers, which can be either inserted manually or generated from a Numbering Pattern.
For example, let's say that you originally wanted to use a numerical Serial Number for the Material Tracking Units
produced in your plant and created a specific Numbering Pattern of this type. Once you started executing a Work
Order, you want to adopt an alphanumerical Serial Number, perhaps because you find it more user-friendly. The
new alphanumerical Serial Number can then be used for all successive Material Tracking Units produced during the
execution of the Work Order in question.
For each Material Tracking Unit, such changes are historically traced, with indication of both the last Serial Number
used and the Serial Number that replaced it.

3.14 Readily-Available Work Instructions and Documents
Opcenter Execution Discrete offers the possibility of associating (that is, linking) Work Instructions and Documents
to crucial elements of the production process, thereby providing Operators with both necessary and supplementary
information to guide them in performing their tasks and provide them with additional insight during execution. In
the case of Work Instructions, it also provides Operators with a sure way to collect the required measurements and
values, thanks to Data Collection sections to be filled during runtime.
As a Product Engineer, you can:
• link Work Instructions to:
• Operations/Steps in the Catalog
• Process Operations/Process Steps
• Work Order Operations/Work Order Steps
• Serial Numbers
• Execution Group Phases
so that they can be followed by the Operator during execution.
• choose if the Work Instructions associated to each Work Order Operation must be shown to the Operator who is
executing an Execution Group or if they must be displayed only while executing a single Work Order.
• choose if you want to share the Work Instructions runtime values with other Work Order Operations (belonging
to the same Work Order) that will use the same Work Instruction (having also the same Association Type).
• unlink Work Instructions from the aforementioned entities.
• establish that the creation (or removal) of a link created between a Work Instruction and an Operation in the
Catalog be propagated to the Process Operation instantiated from that Operation in the Catalog.
• preview the Work Instructions that are linked to:
• Master Plan Operations and Step Catalog
• Work Order Operations and Step Catalog
• As Planned Bill of Process Operations and Step Catalog
• Operations in the Operator Landing page (legacy)/Operator Terminal (for Low Code UI Apps)
• link Documents to:

Opcenter Execution Discrete 2507 - Product Overview

119


## Pagina 120

Product Features
Readily-Available Work Instructions and Documents

• Materials
• Material Tracking Units
• Operations/Steps in the Catalog
• Tool Definitions
• Work Order Operations/Work Order Steps
• Execution Group Phases
• Non-Conformances
• Container Types
so that they can be consulted by the Operator for additional insight during execution.
• unlink one or more Documents from the associated entity.
• preview the Documents that are linked to:
• Master Plan Operations and Step Catalog
• As Planned Bill of Process Operations and Step Catalog
• Operations in the Operator Landing page (legacy)/Operator Terminal for Low Code UI Apps
• link PLMX document or any other document as specification to As Planned BOP Operations/Steps and Master
Plan Operations/Steps in case of CLM Integration.

Details regarding Non-Conformances and Documents
For what concerns Non-Conformances, as an Operator, you can:
• upload existing Documents to be linked to the Non-Conformance that is being opened.
• import Documents created on the fly to be linked to the Non-Conformance that is being opened.
As a Production Coordinator, you can:
• link and unlink Documents to/from a Non-Conformance.
• download the Documents linked to the Non-Conformance directly from the Documents tab of the NonConformances page.

Details regarding Change Packages
For what concerns Change Package requests, as an Operator, you can:
• Open a Change Package during runtime to request one of the following:
• the addition or removal of one or more Documents or Work Instructions to be used to/from a specific
Work Order Operation's or Work Order Step's execution.
• the editing of a specific Work Instruction in relation to a specific Work Order Operation's or Work Order
Step's execution.
As a Production Coordinator, against a Change Package request, you can:
• Add or remove one or more Documents or Work Instructions to be used to/from a specific Work Order
Operation's or Work Order Step's execution.
• Edit a specific Work Instruction in relation to a specific Work Order Operation's or Work Order Step's execution .
• Accept or reject the Change Package, thereby effectively applying or definitely abandoning the changes made.

File-size limitations
For both Work Instructions and Documents, there exists a limit as to the size of the file that you want to associate to
a MES entity. By default, each file must not exceed 100 MB. However, this limit can be modified: for more
information, see Modifying limits for uploading files to the Service Layer in the Opcenter Execution Foundation
Development and Configuration Guide.

Document Previewing

120

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 121

Product Features
Document Item Management

In Opcenter Execution Discrete, you can preview Documents associated to Work Order Operations to get a glimpse
of their contents. Having a general idea as to what information is contained in a Document may help you in finding
the details you need to perform your job in the best possible manner.
The Document Previewer supports the following file formats for Documents:
File Types

Supported File Formats

Non-video files with preview

• .txt
• .svg
• .jpg
• .png
• .pdf
• .plmx

Video files with preview

• .mp4
• .ogg
• .webm

Files in .doc, .csv, .xml and .zip format are not displayed by the Document Previewer, but can be
downloaded. Files in .plmx format are only displayed by the Document Previewer in the Operator Landing
Page, the High Automation Landing Page, and in the Low Code UI Apps runtime working environments.

3.15 Document Item Management
Currently, this product feature can be exploited solely if one of the following Low-Code UI Apps for
Opcenter Execution Discrete has been deployed:
• Opcenter Execution Discrete Complex Manufacturing
• Opcenter Execution Discrete Product Engineer
• Opcenter Execution Discrete Production Coordinator.
Document Items are designed to group Documents that share similar characteristics or a common purpose. In
specific contexts, when linked to a Work Order Operation (or Work Order Step), they represent an additional aid to
Operators in performing their tasks specific to the Work Order Operation (or Work Order Step) at runtime.
Revision management is contemplated for Document Items.
As a Product Engineer, you can:
• Link one or more Document Items to a Process Operation belonging to an As Planned BOP.
As a Product Engineer or Production Coordinator, you can:
• Link one or more Document Items (specifying either the current Revision or a specific one) to a Work Order
Operation (or Work Order Step).
• Unlink a Document Item from a Work Order Operation (or Work Order Step), thereby releasing both the
Document Item and the Documents they contain.
Keep in mind that unlinking is not synonymous with deletion.
As an Operator, you can:

Opcenter Execution Discrete 2507 - Product Overview

121


## Pagina 122

Product Features
Functionalities for As Planned BOP, Master Plan and Process Management

• view all Documents that belong to Document Items linked to Work Order Operations / Work Order Steps.

3.16 Functionalities for As Planned BOP, Master Plan and Process
Management
As Planned BOP, Master Plan and Process management covers an ample spectrum of possibilities for configuring
how production activities are to be executed within your production plant. As Planned BOPs, Master Plans and
Processes can be used and modified according to your needs to speed up configuration tasks and homogenize
production execution where possible.
Additionally it is possible to define Operation Folders in order to group a set of Operations in a specific Process of an
As Planned BoP or Master Plan. You can also create a nested structure having Operation Folders containing other
Operation Folders and/ or Operations. Thanks to this capability the Product Engineer can better organize the
manufacturing process flow and easily define the routing because he/she can directly connect Operation Folders
(instead of having to draw the dependency for each single Operation).
As a Product Engineer, you can create:
• A Process from scratch.
• A Process from a Catalog.
• A revision of an existing Process.
• An Operation Folder from scratch.
• An Operation Folder from a Catalog.
Likewise, as a Product Engineer, you can:
• Manually create a Process that can be either linked to existing or newly-created As Planned BOPs or Master
Plans.
• Link an existing Process to existing or newly-created As Planned BOPs or Master Plans.
• Evolve an existing As Planned BOP, to which you can introduce minor modifications (for example, by adding a
Sub-Process), while maintaining the characteristics of the original one, as well as a relationship with it.
• Clone an existing As Planned BOP to permit in-depth modification. This new As Planned BOP can then be
evolved regardless of the original one.
• Manually create an Operation Folder that can be linked to existing Process in an As Planned BOP or Master Plan
and fill its content by adding Operations or other Operation Folders of the same context.
• Manually create dependencies from/to Operation Folders and Operations in the same Process and As Planned
BOP or Master Plan.

Import of Processes in Teamcenter Manufacturing Integration Contexts
When integration with Teamcenter Manufacturing is present, the Processes (which correspond to either Master
Plans or As Planned BOPs in Discrete manufacturing) present in this particular application are prepared,
Teamcenter Manufacturing side: when they are released, this integration then creates the corresponding data in
Opcenter Execution Discrete. The resulting Processes will be handled as if their data originated directly
from Opcenter EX DS.
If changes have been made to the content (Materials, Tool Definitions, Operations and Steps) of the As Planned
BOP, depending on how you configure the system, you can generate Work Orders using the latest version of the As
Planned BOP or an out-of-date version of it.

3.17 Feature Management
The possibility of managing Bills of Features permits users to:
• specify a set of mandatory characteristics (Features) that the product to be produced must possess

122

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 123

Product Features
Product Configuration Management

• assign specific Feature Values to better customize the product according to particular needs
when generating Work Orders of different production types.
Thanks to this functionality, it is also possible to specify a set of optional characteristics (Options) for the product to
be produced.
In addition, it is possible to adopt Features when composing Qualification Criteria. Therefore, users can create their
Qualification Criteria on the basis of the content of a Bill of Features: when a Work Order is then created from a
Master Plan with this specific Qualification Criteria, the Work Order will necessarily contain those Features that
satisfy the Qualification Criteria.
As a Product Engineer or Production Coordinator, you can:
• Configure Features to be used to form Bills of Features.
• Configure Feature Values.
• Configure Options.
• Create Bills of Features.
As a Product Engineer, you can:
• use Features when composing Qualification Criteria.

3.18 Product Configuration Management
Thanks to the adoption of Product Configurations, Opcenter Execution Discrete offers the possibility of customizing
the product that you want to produce, according to your needs.
This is possible because, once created, Product Configurations can be associated with two structures, called Bill of
Features and Bill of Materials, which represent the structures to be validated in order for the Final Product Type to
be produced, and for the associated ERP Orders to be considered valid and thus scheduled.
When new items are created in the system, either inserted by the user or coming from external import data flows,
there could be the risk of the corresponding data not being valid.
For example, if a list of Bill of Materials is received without the complete list of Materials belonging to it, the final
product cannot be produced, either because the system does not have all the required information or because the
information provided is wrong.
For example:
• a BoM item refers to a Material that has not yet been imported
• two BoM items refer to the same Material (in terms of NId and Revision)
• a BoM item refers to a Material with a Unit of Measure that differs from the one of the Material.
The product makes it possible to set validity checks for the Bill of Features and Bill of Materials making up the
Product Configuration associated with the Final Product Type. Setting validity checks means freezing the structures
of that specific Product Configuration, if they are deemed valid by the system, to be used for the production of the
final product.
As a Product Engineer or Production Coordinator you can:
• create Product Configurations.
• associate Bills of Features (if necessary) and Bills of Materials.
• verify the validity of the Bill of Features and Bill of Materials associated to the Product Configuration.
As a Production Coordinator you can view the received ERP Orders associated to the Product Configuration,
provided that at least one validity check has been executed either for Bill of Features or Bill of Materials.

Opcenter Execution Discrete 2507 - Product Overview

123


## Pagina 124

Product Features
Production Flow Control Management

3.19 Production Flow Control Management
Through the Production Flow Control, Opcenter Execution Discrete makes it possible to apply a dedicated business
logic during production, through the definition of Milestones and their Transitions in relation to a specific Final
Product Type, to define and trace all the necessary steps required to produce your product.
To correctly perform a Transition, users can create Milestones and associate them with:
• Checks, preliminary conditions that must be satisfied to allow the MTU to enter a Milestone.
• Attributes, the business logic to be executed once the MTU enters a Milestone.
• Actions, non-transactional operations to be executed after the MTU has completed the transition from a
Milestone to the following one.
As a Product Engineer or Production Coordinator, you can:
• create Milestones in the Milestone Catalog.
• create Production Flow Control Diagrams.
• associate Milestones to the Diagram and define the sequence in which they must be executed.
• configure Transitions from a source Milestone to a target Milestone.
• associate the predefined Checks, Attributes or Actions to the Milestone.
• set the Diagram as Active.
During production execution, for each Material Tracking Unit associated with a specific Production Line, users can
check which Milestones of the Production Flow Control Diagram are available, to declare those to be executed
according to priorities and perform the corresponding transitions manually according to production needs.
In addition, whenever the MTU undergoes a transition from a Milestone to the other, the system automatically
tracks the outcome of Checks, Attributes and Actions executed at runtime.

3.20 Qualification Criteria Management for Master Plan Contexts
Qualification Criteria make it possible for users to single out certain elements so that they be necessarily included in
a specific Work Order created from a Master Plan.
As a Product Engineer, you can set Qualification Criteria for:
• Process Operations
• Material Specifications
• Inspection Specifications
• Setpoint Variables
• Tool Specifications
• Operation Folders.
In addition, you can use Qualification Criteria as preliminary Checks of a Milestone declaration.

3.21 Dedicated Catalogs for Reusing Processes, Operations and
Steps
Thanks to the dedicated Catalogs offered in Opcenter Execution Discrete, which respectively contain all
the Processes, Operations and Steps currently available in the system, Product Engineers can select those that are
most appropriate for use elsewhere in other contexts within a given production plant: for example, an Operation
such as "Drum Assembly" can be adopted when assembling a drum used in an industrial washing machine, but also
for smaller-scale washing machines, and thus can be used in different contexts within the same Washing Machine
production plant. Items in the Catalogs are not completely configured and act as templates to build actual
production entities.

124

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 125

Product Features
Versatile Work Order Management

3.22 Versatile Work Order Management
Opcenter Execution Discrete offers flexibility in Work Order management, particularly for what concerns how Work
Orders can be created and defined for their execution in runtime within a production plant.
Work Orders can be created in one of the following ways:
• Directly from a pre-existing Process.
• Manually on-the-fly from scratch, to satisfy needs that were not contemplated in a Process beforehand. This is
useful in the case of one-shot productions or exceptions.
• By referencing pre-existing As Planned BOPs that were created in Opcenter EX DS. This procedure allows the
creation of multiple Work Orders at the same time (for example, to produce different parts of the same item).
• By creating a Work Order Header and then merging it with a Process: especially useful to track production
requests from an ERP system.
• By using the structures defined in the Master Plan.
• From a Master Plan with Qualification Criteria rules, to include only those Work Order Operations deemed
necessary to correctly execute the Work Order. Likewise, the same can be done to include those Materials,
Quality Inspections, Setpoint Variables and/or Tools deemed necessary to correctly execute the Work Order
Operation.
• From a Master Plan based on Unit Occurrence Effectivity, to include only those elements required to produce a
certain variant of a product. These elements can be: Operations (and implicitly its Steps even if they have a
different Unit Effectivity), Operation Folders, Certifications, Equipment, Materials and Tools.
While editing a Work Order, Work Order Operations can be added from scratch or instantiated from existing Process
Operations or Master Plan Operations.
As a Product Engineer, you can:
• Create Work Orders in any of the aforementioned ways.
• Update Work Orders (in the event that a Process previously used to generate Work Orders is modified and you
want to propagate those changes to existing Work Orders, either in full or in part).
• Define Reasons for placing a Work Order (or Work Order Operation) in execution in Hold, Pause or Future Hold
status.
As a Production Coordinator, you can:
• Update Work Orders (in the event that a Process previously used to generate Work Orders is modified and you
want to propagate those changes to existing Work Orders, either in full or in part).
• (only in the Opcenter EX DS Production Coordinator App) Request the most recent As Planned BOP from
Teamcenter for updating Work Orders that were created using an out-of-date As Planned BOP.
• Update the Start and/or End times of the Work Order Operations making up a Work Order.
• Define Work Order Pre-Kitting.
• Release a Work Order to production.
• Split a Work Order, if necessary (for example, to lighten the workload if the Work Order is particularly large).
• Close flexible Work Orders before their completion.

3.23 Alternative Paths for Operation Execution
In a variety of situations, it might be useful to have more than one execution path to follow for manufacturing a
specific product: this opportunity contributes to reducing downtimes, while exploiting production-plant resources
to the best advantage.
For this purpose, in Opcenter Execution Discrete, you can adopt alternative Process Operations in place of the
Process Operations that have already been defined as part of your main execution flow for a specific Process.
Likewise, there exists the possibility of adopting alternative Work Order Operations for a specific Work Order.
Both alternatives are feasible solely for Serialized and Full Quantity production.

Opcenter Execution Discrete 2507 - Product Overview

125


## Pagina 126

Product Features
Pre-Kitting for Reserving Specific Material Tracking Units

As a Product Engineer, you can:
• define a group of Alternative Process Operations for a specific Process, establishing one of the group's elements
as the preferred Alternative Process Operation.
• define a group of Alternative Work Order Operations for a specific Work Order, establishing one of the group's
elements as the preferred Work Order Operation.
As a Production Coordinator, you can:
• change your preference of one Alternative Process Operation (or Alternative Work Order Operation) over
another.
For Alternative Work Order Operations, changing your preference is feasible provided that the Work
Order is not in use.

3.24 Pre-Kitting for Reserving Specific Material Tracking Units
The possibility of pre-kitting (reserving) specific Material Tracking Units and their respective quantities for executing
a Work Order Operation (or Work Order Step) covers both Serial Numbers and Batches. In detail, Serial Numbers
can be pre-kitted only in full, whereas Batches can be pre-kitted either in full or in part (for those cases in which
reserving only a portion of the Batch's available quantity is necessary). Pre-kitting involving multiple Batches is also
permitted.
It is possible to view the history of any pre-kitting activities that have been performed on a specific Work Order. This
particular history includes details such as:
• the Material that was pre-kitted;
• the User who performed the pre-kitting;
• the IDs of the Work Order Operations (or Work Order Steps) on which the pre-kitting was performed;
• the date and time when pre-kitting was carried out.
As a Production Coordinator, you can:
• reserve Serial Number or Batches for consumption on specific Work Order Operations (or Work Order Steps)
Pre-Kitting is not always allowed. The behavior varies depending on the status of a Work Order and its
production type. For more information, refer to the constraints in section Performing Pre-Kitting for
Work Orders of the Opcenter Execution Discrete User Manual.
• configure runtime validation for the pre-kitted Material Tracking Units
• view the History of any pre-kitting activities performed on a specific Work Order.
As an Operator, you can:
• validate the pre-kitted MTUs, if required
• replace the pre-kitted MTUs on-the-fly if they are not available for consumption.

3.25 Runtime Work Order Execution
In order for a Work Order to enter the production cycle, it must first be released by the Production Coordinator.
There exists the possibility of governing the execution of Start and Complete on Work Order Operations by
performing Interlocking Checks: for more information, see Interlocking Checks for Governing Work Order Operation
Execution.
As a Production Coordinator, you can:
• Place a Work Order in Hold or Future Hold status for a specific Reason.

126

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 127

Product Features
Result Management

• Verify the completion of a Work Order and, if necessary, freeze its configuration to prevent it from being
modified.
• View the Results declared on a Material Tracking Unit for a specific Work Order Operation, at Operation or
Activity level.
• Amend one or more Results declared on a Work Order Operation, if desired, at Operation or Activity level.
• Amend the strategy (corrective action) adopted for a declared Result, if desired, at Operation or Activity level.
• View the genealogy of a Work Order.
• Split Work Orders.
• Create a flexible Work Order and modify the quantity to be produced.
• Own and resolve Non-Conformances.
• Close flexible Work Orders before their completion.
• Add Work Order notes to Work Order Operations or at the Work Order level, as well as acknowledge them.
As an Operator, you can:
• View details related to Work Order Operations, Work Order Steps and Execution Groups prior to starting them.
• Start, pause and complete Work Order Operations.
Work Order Operations can also be started and completed automatically by Machines (or
Workcenters). The possibility of choosing whether a Work Order Operation is to be started and/or
completed automatically does not exclude the possibility that the same Work Order Operation be
started and/or completed manually by an Operator or a Team. A Work Order Operation can be
completed automatically by any member of the Team (even when the Complete by Different User
configuration option is set to NO). Once the operation is completed, the Work Order Operation is no
longer visible to other Team members.
• Start, pause and complete Execution Groups.
• Declare Work Order Step completion.
• Declare a Result regarding the execution of a specific Work Order Operation for producing one or more Serial
Numbers or Batches (Material Tracking Units), at Operation or Activity level.
• Declare the consumption of Material Tracking Units in the production process.
• Declare the consumption of Tools in the production process.
• Collect data to be entered in Work Instructions (if present).
• Add Work Order notes to Work Order Operations or at the Work Order level, as well as acknowledge them.
• Open and resolve Non-Conformances.
• Perform Quality Inspections.
• Close flexible Work Orders before their completion.
• Declare the production of Material Tracking Units for Co-Products and By-Products.
• Initiate the transfer of CNC packages and print job files.
• (In Additive Manufacturing contexts) Load Powder Batches into 3D Printers and, if necessary, replenish their
quantity.
• Upload documents.

3.26 Result Management
In Opcenter Execution Discrete, Results can be adopted to determine how a certain production of a Material
Tracking Unit will proceed after the completion of a specific Work Order Operation based on its outcome: the
execution of the Work Order Operation may be in line with what was expected - that is, with all production
requirements satisfied - or otherwise.
Shop-Floor Operators can declare a Result upon Work Order Operation completion of each Serial Number or Batch,
so that the execution of the failed activities can be re-iterated (either immediately or at a later time) until their
outcome is positive (that is, "as expected"). This is the default strategy followed by the system when Result
declaration is adopted.

Opcenter Execution Discrete 2507 - Product Overview

127


## Pagina 128

Product Features
Interlocking Checks for Governing Work Order Operation Execution

In addition to the native Result Types provided in Opcenter EX DS to declare positive and negative Results, it is
possible to configure custom Result Types that may better satisfy specific needs (such as making a clear distinction
between those Results that are considered positive or negative for a particular reason with respect to another: for
example, you could have 2 custom Result Types - "NOK_Consumption" and "NOK_Assembly" - to be used to
express distinct negative Results).
After a Result has been declared, if necessary, authorized users who possess the appropriate user rights can
override its value by performing an Amend operation.
It is also possible to amend a Result's strategy. For example, let's say that the corrective action initially associated
to a Result becomes unnecessary or is no longer valid. In this case, depending on the situation, the user can choose
to amend the Result's strategy by either:
• removing it: in this case, no corrective measure will be adopted.
• switching to a different corrective action.
The information regarding the Results declared is tracked in the MTU's history (Genealogy and As-Built screens).
To avoid continuing to work on a Material Tracking Unit with a negative Result, the system can be configured to
check, at the start of Work Order Operations, if the selected Serial Number or Batch can be started, on the basis of
the Results of all previous actions executed on that Serial Number or Batch (regardless of its position within the
production's execution path).
If the Result management is set at Activity level, the result of the Work Order Operation is partially anticipated by
performing preliminary validations on the basis of the result for the single Activities, either for the case in which
they have failed or if they have not yet been executed. The definitive result is then declared at the completion of the
Work Order Operation.

3.27 Interlocking Checks for Governing Work Order Operation
Execution
Opcenter Execution Discrete comes provided with a set of standard Interlocking Checks for governing the start and
completion of a specific Work Order Operation's execution.
It is possible to choose which Interlocking Checks can be enabled for verifying whether one or more conditions have
been satisfied in full in relation to the Work Order Operation in question: if the outcome of all these checks is
successful, the execution of the Work Order Operation will either be started (Inbound Interlocking Checks satisfied)
or completed (Outbound Interlocking Checks satisfied).
Prior to the Work Order Operation's start (or completion), the Interlocking Checks that have been enabled can be
triggered automatically.
All of the Interlocking Checks enabled on a specific Work Order Operation, be they Inbound or Outbound, are
executed in parallel. The outcome of each Interlocking Check is then traced.
In addition to the standard Inbound and Outbound Interlocking Checks, users can also implement custom Inbound
and Outbound Interlocking Checks, according to their needs. Once the required business logic is implemented and
the custom Interlocking Check is configured in Opcenter EX DS, it will be handled by the system in the same manner
as a standard Interlocking Check.
For more information on how to implement the business logic of a custom Interlocking Check, see section
How to Develop Custom Interlocking Checks of the Opcenter Execution Discrete Extensibility Guide.
For more information on how to create a Custom Interlocking Check in Opcenter EX DS and use it during
production execution, see section Configuring Custom Interlocking Checks of the Opcenter Execution
Discrete User Manual.

128

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 129

Product Features
Exchange of Messages with the Shop Floor

As a Product Engineer, you can decide which Interlocking Checks are to be performed on a certain Process
Operation or Work Order Operation, enabling and configuring them accordingly.
As an Operator, you can view which Interlocking Checks have been configured for the selected Work Order
Operation.
As a Production Coordinator, you can:
• view the outcome of both Standard and Custom Interlocking Checks from the dedicated Interlocking Check
History panel in the Operator Landing Details screen (legacy).
• view the same historical data also from the As-Built page.

3.28 Exchange of Messages with the Shop Floor
Opcenter Execution Discrete contemplates the possibility of exchanging structured messages with the Shop Floor
to automate certain activities during production execution.
By properly configuring your scenario to permit integration with Opcenter Connect MOM, you will be able to
exchange messages between the MES layer and the Shop Floor, in order to:
• Start and complete Work Order Operations automatically by Machines or Workcenters, regardless of the
Production Type.
• Automatically create and sentence Non-Conformances by Machines or Workcenters on Work Order Operations
and Material Tracking Units, in the case of Quality Non-Conformances.
• Automatically consume Material Tracking Units during the execution of Work Order Operations.
• Automatically collect Data during the execution of Work Order Operations.
• Automatically collect Quality Inspection Data of Work Order Operations.
• Automatically use Tools during the execution of Work Order Operations.
• Automatically create Work Order notes at the Work Order level.

3.29 Adoption of Execution Groups for Maximizing Productivity
In Opcenter Execution Discrete, Execution Groups and Execution Group Phases make it possible to execute sets of
Work Order Operations (typically belonging to different Work Orders) together at runtime on the same Equipment.
The benefits of this feature are:
• maximized productivity
• a considerable reduction of Equipment idle time
• Machine operation at full capacity.
If you are a Product Engineer or a Production Coordinator, you can:
• create an Execution Group while configuring the production processes.
• link additional Work Order Operations to an existing Execution Group while configuring the production
processes.
• edit the Execution Group Phase's name and link Work Instructions to the Execution Group Phase.
• unlink Work Order Operations from the Execution Group to which they are linked.
• schedule an Execution Group.
• release an Execution Group after having configured the production processes.
• abort an Execution Group, or a list of Execution Groups, if there are no Work Order Operations linked.
• (specific to Additive Manufacturing), associate Powders to Execution Group Phases.
If you are an Operator, you can:
• create an Execution Group at runtime.
• link additional Work Order Operations to an existing Execution Group at runtime.
• unlink Work Order Operations from the Execution Group to which they are linked.

Opcenter Execution Discrete 2507 - Product Overview

129


## Pagina 130

Product Features
On The Fly Management of Changes to the Production Process

• transfer the Print Job File to the Machine associated to an Execution Group.
• track Powder Material Batches used in Work Order Operations specific to Additive Manufacturing production.
• start an Execution Group to permit the execution of its Work Order Operations in parallel on the same Machine,
provided that certain requirements have been satisfied.
• pause an Execution Group. The Execution Group can be resumed once the issue that warranted the pause has
been corrected or clarified.
• complete an Execution Group, thereby indicating that all of its Work Order Operations have been executed and
that the Execution Group can no longer be launched on the Machine to which it was associated.
Regardless of their role, in runtime, from the Operator Landing Page (legacy), all users can view the list of all the
Tasks related to all the Work Order Operations associated to the Execution Groups.

3.30 On The Fly Management of Changes to the Production Process
Thanks to the possibility of opening Change Requests, Opcenter Execution Discrete can handle the most commonly
encountered situations in which changes to the production process are necessary in runtime.
As a Production Coordinator, you can:
• Introduce, repeat, re-sequence and eliminate dependencies between the Work Order Operations making up a
Work Order.
• Introduce, substitute and eliminate material to be consumed in the Work Order Operation.
• Introduce the Tools to be used in the Work Order Operation.
• Modify the quantity of material to be consumed in the Work Order Operation.
• Add a Work Instruction containing a Data Collection section designed to contain data to be entered during
runtime.

3.31 Change Package Management
Thanks to Change Packages, Operators can request that changes be made during Runtime to the Specifications
involved in the execution of a certain Work Order Operation or Work Order Step. The notes provided in a Change
Package are first-hand observations regarding deficiencies or discrepancies as to the Materials, Tools, Documents,
Work Instructions, Machines or Quality Inspections that are to be used. On the basis of this content, the Production
Coordinator may decide either in favor or against adopting the modifications suggested.
As an Operator, you can:
• open a Change Package to ask that the Production Coordinator adopt certain changes on-the-fly to the
Materials, Tools, Documents, Work Instructions, Machines or Quality Inspections to be used in the execution of a
certain Work Order Operation or Work Order Step.
As a Production Coordinator, you can:
• view the Change Packages that are active and their content.
• add or remove Materials, Tools, Documents, Work Instructions, Machines or Quality Inspections to be used from
the Work Order Operation's or Work Order Step's execution on the basis of the Change Package's content.
• accept the Change Package so that any changes that have been made become effective and are applied to the
Work Order Operation or Step.
• reject the Change Package so that none of the suggestions it contains are to be adopted: if any changes have
been made, these modifications will not be effectively applied to the Work Order Operation or Step.

3.32 Work Order Dispatching
Thanks to the Production Coordinator Dashboard, Production Coordinators can modify how production is
distributed by tweaking its dispatching. This dedicated screen displays the actual situation as to how many Work

130

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 131

Product Features
Order Work In Progress (WIP) Monitoring

Order Operations are currently active, as well as how many are queued, within a certain zone of your production
plant.
In particular, it is also possible to schedule the execution of the Work Order Operations manually.
As a Production Coordinator, you can;
• Select an Equipment Level or Machine and see the number of operations that are currently active and queued.
• View the scheduling of the Work Order Operations on the selected Equipment Level/Machine in a Gantt chart.
• Modify the current scheduling according to your needs (for example, by changing the Estimated Start and End
Times, Equipment Level/Machine, etc.).
Optionally, it is possible to associate specific pieces of Equipment to Users and/or Roles, so to filter which items are
displayed on the Production Coordinator Dashboard, and consequently the items on which a specific User is
authorized to operate.

3.33 Order Work In Progress (WIP) Monitoring
If you are a Production Coordinator or Operator, you need an accurate vision of what is actually taking place on the
shop floor, so that you can make the right decisions to streamline production; for example:
• Which Work Orders are currently being processed.
• How much of a Work Order has been completed.
• What the outcome is regarding the production of a certain product (that is, the quantities of what has been
produced and what has been scrapped).
To satisfy your customers with the best possible product in the briefest time, it is essential that you have maximum
visibility regarding work in progress.
Opcenter Execution Discrete offers a dedicated WIP screen for viewing how the Work Orders are progressing in their
execution.
The screen displays all Work Orders, with an indication of the final product being produced and their current
percentage of completion.
By selecting a specific Work Order, you can view information related to its Work Order Operations (status, as well as
produced and scrapped quantities).
If you are managing your production with Low Code UI Apps, then you can monitor Work Orders from the Work
Order Network page available in the Opcenter Execution Discrete Production Coordinator Low Code UI App.
This page provide additional capabilities. In detail, it allows you to:
• add external dependencies (only AfterEnd) to other Work Orders belonging to the same parent Batch to further
tune the production.
• display Work Order and Work Order Operation dependencies in a graphical way.
• disable the countdown.
• perform a manual refresh of the content displayed in the page.

3.34 Use of Tasks for Managing Work Order Operation/Step
Progression
The adoption of dedicated Tasks in Opcenter Execution Discrete makes it easier for users to manage the principal
elements involved in Work Order Operation/Step progression. The available Tasks listed below concern:
• Work Instruction: The Work Instructions related to the Work Order Operation's (or Work Order Step’s)
progression. They may consist in a series of steps written in html format that must be read, performed and

Opcenter Execution Discrete 2507 - Product Overview

131


## Pagina 132

Product Features
Runtime Data Collection Capabilities

acknowledged by the operator, as well as Data Collection sections into which specific measurements and values
must be entered.
• Tool Usage: The Tools to be used during the execution of a specific Serial Number or Batch during the Work
Order Operation’s (or Work Order Step’s) progression.
• Material Consumption: The Materials or Batches and the relative quantities that are to be consumed/
assembled/disassembled/tracked in order to produce a specific Serial Number or Batch.
• Quality Inspection: measurements or inspections on specific production contexts (Work Order Operations /
Steps), produced Materials and execution Equipment.
• Print Job Files: the Print Job Files and Serial Numbers that are to be transferred during Work Order Operations
execution of type Additive Manufacturing.
• Part Program Transfer: the instructions that are to be uploaded to a Machine since they are necessary to
physically perform Work Order Operations.
• Material Production: The Materials or Batches and the relative quantities that are to be produced in order to
produce a specific Serial Number or Batch.
The aforementioned Tasks are contained in the default Process Definition (called UADMProcessDefinition) and
they are carried out in parallel, but can be configured otherwise, if desired. For more information, see Speeding Up
Operator Landing Page Loading through Task Customization in the Opcenter Execution Discrete User Manual.
Furthermore, additional default Process Definitions are provided, derived from the original
UADMProcessDefinition. Each of the new defaults contains a dedicated sub-set of the runtime Tasks mentioned
above. In this manner, only those Tasks deemed necessary will be displayed at runtime in the Operator Landing
page (legacy), without the need to modify the default Process Definition.
A separate Task (Load AMPowder on 3D Printer), for loading the required Powder on the 3D Printer during Work
Order Operations specific to Additive Manufacturing, is contained in the default Process Definition
3DPrinterSetupProcessDefinition.

3.35 Runtime Data Collection Capabilities
In Opcenter Execution Discrete, thanks to the possibility of integration with Teamcenter Manufacturing,
existing Work Instructions can be imported for subsequent use.
In addition, custom Data Collection sections can be created directly inside Work Instructions in Opcenter EX
DS, operating via a dedicated page.
As a Product Engineer, you can:
• Import existing Work Instructions from Teamcenter Manufacturing.
• Create custom Data Collection sections directly inside Work Instructions in Opcenter EX DS.
• Associate Work Instructions to one or more:
• Process Operations and/or Process Steps
• Work Order Operations and/or Work Order Steps
• Serial Numbers
• Execution Group Phases
As an Operator, you can enter the requested measurements as values into the blank Data Collection sections of
your Work Instructions, so to complete them and thus permit successive evaluation.
If the system is properly configured in order to acquire values from the Automation Layer, then, as an Operator, you
will be able to decide whether to automatically retrieve the values coming from the field or enter them manually.
Data Collection values can be also calculated at runtime according to a configured formula expression. Formulas
can be created using the default Operators or relying on custom functions.
For more information on how to create custom functions, see section How To Implement Custom Functions to
Calculate Runtime Work Instruction Valuesto Work Instruction Definition Parameters of the Opcenter Execution
DiscreteExtensibility Guide.

132

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 133

Product Features
Semi-Automatic Acquisition of Values

For more information on how to manage Formulas, see section Adding Formulas to Work Instruction Definition
Parameters of the Opcenter Execution Foundation User Manual.
Finally, Data Collection values can be completely acquired from the field and no human intervention is required to
save the values in the system, if Opcenter EX DS is configured in order to exchange XML messages with the Shop
Floor. In this case, the actor is the involved piece of Equipment (Machines or Cells).

3.36 Semi-Automatic Acquisition of Values
If the system is properly configured and linked to the Shop Floor via the Opcenter Execution Foundation
Automation Gateway App, it is possible to acquire values from the field.
The Operator can acquire the values related to Data Collections, Tools/Substrates, and Material Tracking Units,
without the need to insert them manually.
The semi-automatic acquisition is possible due to the mapping of parameters with the variables coming from the
field, via the Opcenter Execution Foundation Automation Gateway App.
• For Data Collections, the field values acquired are related to Work Instruction parameters.
• For Materials, the Operator can acquire the Serial Number, Batch ID, or Quantity to be consumed during an
Assembly operation, or enter them manually.
• For Tools/Substrates, the Operator can acquire the ID of the Tool/Substrate to be used, the usage counter and
the time duration, or enter them manually.
As a Product Engineer, you can:
• Link Data Collections (for both Operations and Steps) to the Automation Node Instance Parameters.
• Link Tool/Substrate Definition Parameters to the Automation Node Instance Parameters.
• Link Material Parameters to the Automation Node Instance Parameters.
As a Production Coordinator, you can:
• View Material and Tool Definition mappings with Automation Node Instance Parameters from the Work Order
Operation configuration.
As an Operator, you can:
• Acquire Data Collection values.
• Confirm the acquired Data Collection values or edit them manually before saving.
• Acquire the ID of the Tool/Substrate to be used along with its usage counter and time duration.
• Acquire the ID of the Serial Number, Batch or Quantity to be consumed during assembling.
Information related to the acquisition from the field is traced in both the As Built and Genealogy pages.

Mapping between Data Collection Parameters and Automation Node Instance
Parameter
Opcenter EX DS maps Data Collection Parameters with Automation Node Instance Parameters according to the
following criteria:
Data Collection Parameter

Automation Node Instance Parameter

Type

Data Type

Boolean

Bool

Opcenter Execution Discrete 2507 - Product Overview

133


## Pagina 134

Product Features
Semi-Automatic Acquisition of Values

Data Collection Parameter

Automation Node Instance Parameter

Type

Data Type

Go-No Go

Bool

Pass-Fail

Bool

True-False

Bool

Yes-No

Bool

(Image)

Bool

Integer

Int

Date

DateTime

String

String

Numeric

• Real
• Lreal

Min-Max

• Int
• DInt
• LInt
• Byte
• Sint
• Uint
• UDInt
• ULInt
• Real
• Lreal

Mapping between Tool Definition/Material Parameters and Automation Node
Instance Parameter
Opcenter EX DS maps Tool Definition and Material Parameters with Automation Node Instance Parameters
according to the following criteria:
Automation Type

Automation Node Instance Parameter
Data Type

Bool

134

bool

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 135

Product Features
Runtime Behavior for Machines and Tools

Int

smallint

DInt

int

LInt

bigint

DateTime

DateTime

String

string

Byte

tinyint

SInt

smallint

UInt

int

UDInt

bigint

ULInt

decimal

Real

decimal

LReal

decimal

3.37 Runtime Behavior for Machines and Tools
In Opcenter EX DS, the runtime behavior of Machines and Tools can be driven when executing a Work Order
Operation by exchanging messages with Opcenter Connect MOM (Opcenter CN MOM).
You can configure your system in order to exchange XML messages that drive the system to do the following:
• to automatically start and complete the Work Order Operations on certain Machines.
• to automatically create and resolve Non-Conformances by Machines or Workcenters on Work Order Operations
and Material Tracking Units, in case of Non-Conformances of type Quality.
• to automatically use Tools at runtime. No human intervention is required and the activity is traced in the AsBuilt and Genealogy pages as performed by a piece of Equipment.
• to automatically consume Materials.
• to automatically collect data.
As a Product Engineer, you can:
• associate Setpoints to:
• Equipment Types and Machines.
• Tool Definitions and Tools.
• associate Automation Node Instances to Machines and Tools.
• associate Automation Node Types to Tool Definitions and Equipment Types.
• view the Setpoints associated to:

Opcenter Execution Discrete 2507 - Product Overview

135


## Pagina 136

Product Features
Non-Productive Activity Management

• Equipment Types and Machines.
• Tool Definitions and Tools.
• establish an association between Process Operations and:
• Machines with Setpoints.
• Tools with Setpoints.
As an Operator, you can:
• start Work Order Operations on Machines for which Setpoints have been defined and view the related variables.
• start Work Order Operations on Machines for which Setpoints have been defined and type a value on the fly or
choose one among those set during engineering.
• view details about the Setpoints used for Machines/Tools on specific Work Order Operations. In this case, this is
feasible from the Operator Landing page (legacy).
• use Tools at runtime, for which Setpoints have been defined.
As a Production Coordinator, you can:
• start Work Order Operations on Machines for which Setpoints have been defined and view the related variables.
• view details about the Setpoints used for Machines/Tools on specific Work Order Operations. In this case, this is
feasible from the Genealogy and As-Built pages.
• use Tools at runtime, for which Setpoints have been defined.

3.38 Non-Productive Activity Management
Although not directly involved in the production process, Non-Productive Activities are often necessary in a
manufacturing plant so that overall plant operation continues to run smoothly: examples of such activities are
accounting, training of personnel, cleaning of plant premises, etc.
As a Production Coordinator or Product Engineer, you can:
• can create a catalog of available Non-Productive Activities to satisfy your plant's needs.
• edit and modify the Activities log, in which the system tracks the time spent performing each Non-Productive
Activity.
As a User, you can:
• declare the start and end of a Non-Productive Activity, by choosing from among the previously-created activities
and, if desired, entering its context.
• declare the start and end of multiple Non-Productive Activities at the same time, provided that their contexts
differ.

3.39 Label Printing
Opcenter Execution Discrete offers the possibility of printing labels containing barcodes, text or images for:
• Work Orders
• Work Order Operations
• Material Tracking Units.

3.40 Work Order Operation Execution Using the High Automation
User Interface
Opcenter Execution Discrete uses the High Automation User Interface to monitor and control the production and
delivery of products and services. The High Automation User Interface allows the user to select a Machine instance
so that the High Automation Details User Interface will show the details of the Work Order Operation active on the

136

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 137

Product Features
Production Execution in Offline Mode

selected Machine. Once the Machine is selected, the information is saved on the database and re-used after the next
login of that user.
The High Automation User Interface uses the signals about the operations performed on the Machine, such as Start,
Complete, and Assemble and displays the correct corresponding data in real-time. The user can perform standard
functions of the Operations Details User Interface such as Adding a note, Defect, among others. The High
Automation User Interface contains all the Documents and Material to be consumed associated with the active
Work Order Operation on the selected Machine.
While configuring the system, the default layout of the High Automation Landing page can be changed to enable
the display of runtime tasks, similarly to what is done in the standard Operator Landing page (legacy). Likewise,
there also exists the possibility of determining which Header Bar fields are to be visible in the High Automation
Landing page. For this page, it is also possible to set the percentage of the overall screen's width that will be
occupied by the Document Preview therein.

3.41 Production Execution in Offline Mode
Opcenter Execution Discrete comes provided with the capability to execute production in Offline Mode (that is, in
environments without connectivity to the Opcenter EX DS server.).
In such cases, if a dedicated App is installed on mobile devices, Shop Floor Operators can manage Work Order
Operations directly from their mobile devices.
The App for managing production from mobile devices must be implemented separately according to the
customer's specific requirements.
Once selected for Offline execution, and their content is downloaded on the mobile device, Work Order Operations
remain visible in the Operator Landing page (legacy). However no actions are permitted: the Work Order
Operations remain locked until they are checked in again.
The following Actions can be performed while working offline:
• Starting Work Order Operations and Steps
• Pausing Work Order Operations
• Completing Work Order Operations and Steps
• Consuming Materials
• Using Tools
• Displaying Documents
• Collecting Data
• Uploading Documents
• Creating Quality Non-Conformances.
As an Operator, you can:
• Perform the check-out of Work Order Operations on the mobile device and thus implicitly start Offline Sessions.
• See the content of the related Offline Session (in terms of involved Work Order Operations) from the Offline
Sessions page.
• Upload production execution data from the mobile device to Opcenter Execution Discrete once the Work Order
Operations are completed, or in case you want to proceed with execution in Online mode.
• Amend the content of uploaded Offline Actions, in case of failures.
• Perform the check-in of Offline Actions and Offline Sessions to conclude production execution in Offline mode.
As a Production Coordinator, you can discard the Offline Sessions.

Opcenter Execution Discrete 2507 - Product Overview

137


## Pagina 138

Product Features
Line Side Inventory and Kanban Call Management

3.42 Line Side Inventory and Kanban Call Management
From dedicated pages it is possible to manage Line Side Positions and related Kanban requests manually,
performing the following operations:
• open a call, if no other call is active for the Line Side Position,
• cancel the call, for example if not needed anymore or opened by mistake, only if its state is Open or InProgress.
In addition, only for automatically managed Line Side Positions, it is possible to:
• update the quantity of the Materials associated with the Workplace,
• increase the priority of an existing call, only if the call is active.
Furthermore, a dedicated color code has been adopted in the user interface to allow the Operator to interpret each
Kanban request state at a glance.
When there is integration between Opcenter Execution Discrete and intraplant logistics, Kanban calls are managed
and satisfied via Opcenter Intraplant Logistics: for more information on this feature, see Integration with Intraplant
Logistics (Opcenter IPL).

3.43 Non-Conformances and Rework Codes for Runtime Quality
Management
In Opcenter Execution Discrete, for what concerns quality checks during production execution, Defects, Failures
and Non-Conformances are fully managed, with the possibility of focusing on the history of each Non-Conformance,
its lifecycle and status changes from beginning to end (that is, from when the Non-Conformance is opened to when
it is sentenced). A dedicated page displays all the Non-Conformances that have been notified, from which you can
perform various operations (including sentencing), provided you have the appropriate rights.
Quality Non-Conformances can be declared on:
• Work Order Operations
• Machines
• Material Tracking Units and Containers
• Tools.
Quality Non-Conformances can also be declared and managed automatically by Machines and/or Workcenters,
provided that there is integration with Opcenter Connect MOM.
Instead, by appropriately setting a dedicated Engineering configuration key, whenever a user detects and declares
a Failure on a Material Tracking Unit during a Quality Inspection of any type, this triggers the automatic creation of a
Quality Non-Conformance in Open status so that it can then be corrected.
Notifications for Non-Conformances are displayed to all the users currently logged in and have the rights to view
the Notification Bar.
In addition, Rework Codes can be created, associating an operation defined for reworking an item, a Defect (or a
group of Defects), a Failure (or Sub-Failures) and a Final Material.
During production, when the Operator declares a Non-Conformance on an item, the system takes into account the
Defect or Failure that has been found and the Final Material of the Work Order that is being executed and displays
the list of possible rework operations to be performed to rectify it.

Non-Conformance Management
All functionalities provided in Opcenter EX DS for managing Non-Conformances are available for use in Runtime.
As an Operator, you can:

138

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 139

Product Features
Electronic Signature and Buy-Off Management

• Create (open) a Non-Conformance with a list of Defects or Failures associated with it.
• Update a Non-Conformance.
• Link documents to a Non-Conformance when the Non-Conformance is being created.
• Filter Failures based on Material or Equipment when the Non-Conformance is being created.
As a Product Engineer, you can:
• Create custom Defect Groups and Sub-groups.
• Create Failures and Sub-Failures.
As a Production Coordinator, in addition to performing the Operator tasks listed above, you can:
• Receive notifications indicating that a Non-Conformance has been opened.
• View the history and details of a Non-Conformance.
• Link and unlink Documents to a Non-Conformance.
• Sentence a Non-Conformance (provided you possess the appropriate credentials).
• Change the status of a Non-Conformance.
• Create Rework Codes.
• Select a Rework Code to rectify a Defect (or defect group) or a Failure found in a Non-Conformance.

3.44 Electronic Signature and Buy-Off Management
In complex industries, the adoption of Electronic Signatures is essential to limiting the execution of certain actions
on a specific Work Order Operation to certain individuals.
During Engineering, through appropriate configuration, a Work Order Operation can be specifically set to require an
Electronic Signature for its start, pause or completion. Furthermore, the system takes into account whether the
user has the appropriate Role and possesses the appropriate Certification in order to work on the Work Order
Operation in question.
The Electronic Signature can also be requested while managing Work Instructions and Quality Inspections, if
properly configured.
In those contexts where more stringent restrictions are required, a particular use of the Electronic Signature can be
applied in terms of Buy-Off activities, so that during production, the produced Material Tracking Units are explicitly
signed by entitled users. While good MTUs can proceed in the production flow, the rejected MTUs are held up and
managed individually.
As a Product Engineer, you can:
• configure a Work Order Operation so that it requires an Electronic Signature when it is started, paused and/or
completed.
• configure Work Order Operations with Work Instructions or Quality Inspections that also require the Electronic
Signature while managing them.
• configure Work Order Operations with Quality Inspections specifically designed to manage Buy-Off activities.
• if entitled, carry out Buy-Off activities on the MTUs currently in production.
As an Operator, you can:
• enter an Electronic Signature so that a specific Work Order Operation can be started, paused and/or completed.
• enter an Electronic Signature while managing a Work Instruction or a Quality Inspection.
• from the Operator Terminal for Complex Manufacturing, send Buy-Off notifications and pause the Work Order
Operation with Reason Buy-Off while waiting for the Buy-Off request to be managed.
• if entitled, carry out Buy-Off activities on the MTUs currently in production.

Opcenter Execution Discrete 2507 - Product Overview

139


## Pagina 140

Product Features
Data Tracing for Production Activities

3.45 Data Tracing for Production Activities
For Production Coordinators, it is important to have a clear idea as to all the elements that come into play when a
certain production activity is performed in order to execute a specific Work Order: this makes it possible to pinpoint
critical areas in which updating and/or modifications are necessary to improve overall performance.
This information can be deduced in Opcenter Execution Discrete thanks to two distinct screens provided for this
purpose:
• The As-Built screen
• The Genealogy screen.
Likewise, Operators may need to access historical information and drill-downs similar to what is presented in the
aforementioned screens to obtain insight on what actions a specific Work Order Operation has already undergone
and what elements were involved: for example, when an Operator is acquiring data from the field regarding the
Tools involved in a Work Order Operation and wants to see the details of this particular data acquisition (such as the
quality of the acquired values, or the time-stamp of the acquisition).

The As-Built screen
The As-Built screen displays a vast range of historical data related to a selected Work Order (which must be in a
status other than New or Edit). Through this screen, you can view:
• The Work Order's essential details (for example, name, description, production type, produced material,
quantity and UoM, underlying BOP).
• Information regarding the Work Order Operations and Work Order Steps making up the selected Work Order (for
example, name, description, current status, involved Operator, Interlocking Check history).
• For Serialized Work Orders:
• The Tools used for specific Serial Numbers.
• The User who contributed to producing the Serial Numbers related to the Work Order (that is, who
started, paused or completed its execution).
• All Work Instructions, including manual acquisition, Execution Group and Execution Group Phase details, for
each Work Order Operation or Work Order Step.
• The Material Tracking Units consumed for each Work Order Operation or Work Order Step, with the identifier of
the User or the Machine who consumed them. In the case of partial disassembly, this information also
includes the target Material Tracking Unit on which the partial disassembly is performed and the respective
variations in quantity (that is, the MTU's quantity prior to partial disassembly, the quantity partially
disassembled from the MTU, the MTU's quantity after partial disassembly).
• Any related Non-Conformances.
• Any related Changes.
• A log history of all actions (activities) performed on the Work Order and its elements.
• The dependencies between the various Work Order Operations/Work Order Steps.
• The Hold history in relation to the selected Work Order.
• Any notes that have been attached to the selected Work Order's Work Order Operations.
• Any Print Job Files that have been transferred.
• Quality Inspection data.
In addition to viewing the aforementioned information, the Production Coordinator can also perform the following
operations in relation to the selected Work Order:
• Disassemble (in full or in part) the Material Tracking Units that have been consumed for each Work Order
Operation (and/or Work Order Step).
• Re-open completed Work Order Operations in order to release them for re-execution by the Operator.

The Genealogy screen

140

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 141

Product Features
Quality Inspections

The Genealogy screen provides a tree structure that displays the current status of the various Work Order
Operations (and Work Order Steps, if present) making up the selected Work Order. By expanding each node,
essential information regarding any actions that have been performed in relation to the corresponding Work Order
Operation (or Work Order Step) will be displayed:
• The type of action performed.
• Its date and time of execution.
• Who performed the activity.
In the case of Serialized Work Orders, by expanding the nodes, you will be able to view each of the Serial Numbers
that has been produced following execution. The information provided by expanding each Serial Number node
includes the Tools, as well as the date and time when it was started, paused and/or completed. The user (or the
Machine, in case of automatic operation) who started, paused or completed the action on the Serial Number is also
specified.
If the Work Order Operations contain Work Instructions (associated at the Execution Group Phase level), the
Execution Group details and the Execution Group Phase details will be displayed.
If the Work Order being viewed has consumed Material Tracking Units produced by another Work Order, the tree
structure will provide a drill-down of the Work Order that produced the Material Tracking Unit.
The contents of the Genealogy screen can also be filtered by Batch ID, Work Order ID or Serial Number.
From the Genealogy screen, it is also possible to disassemble consumed Material Tracking Units (both in full and in
part).

3.46 Quality Inspections
Quality Inspections are activities carried out at runtime to verify if the produced material conforms to specific
quality requirements or a machine is working as expected.
Typical Quality Inspections may be related to the following Quality Characteristics:
• visual defects (for example, scuff marks, paint drops)
• attributive characteristics (for example, whether a specific paint is used to paint the car or not - that is, OK/NOT
OK)
• variable characteristics (for example, any measurement with respect to allowed tolerances).
Control Methods can be defined for enabling Statistical Process Control (SPC) functionalities based on Industrydefined rules and Control Charts that will be used to evaluated the quality of the production process.
As a Product Engineer, you can:
• determine which quality characteristics are relevant for your product and configure the system accordingly.
• link the defined quality characteristics to your manufacturing process in the form of Inspection Definitions,
which determine how the Quality Characteristic must be acquired.
• configure Quality Inspections on all produced items (100 Percent) or a subset of them (Part Based) or
according to a specific interval of time (Time Based), or on a subset of produced items with a frequency
expressed in the Material Unit of Measure (Unit Based).
• specify the frequency of execution for Part Based and Unit Based inspections as either an explicit number or a
percentage of the quantity produced by the Production Order.
• configure Quality Inspections to specifically handle Buy-Off activities.
• configure Quality Inspection alerts to be displayed at runtime.
• manage Inspection Master Plans and Inspection Orders in order to perform Quality Inspections outside of
manufacturing activities.
• configure and manage Control Methods and assign them to Inspection Definitions.
As an Operator, you can:

Opcenter Execution Discrete 2507 - Product Overview

141


## Pagina 142

Product Features
Advanced Planning and Scheduling Integration (Opcenter APS)

• execute Quality Inspection tasks, based on the related Inspection Definitions.
• execute Inspection Orders.
• open Non-Conformances in case of violations.
• acquire sample size greater than 1.
• display SPC Control Charts.
• preview the Quality Inspections that are linked to:
• Master Plan Operations and Step Catalog
• As Planned Bill of Process Operations and Step Catalog
• Operations in the Operator Landing page (legacy)/Operator Terminal for Low Code UI Apps.

3.47 Advanced Planning and Scheduling Integration (Opcenter APS)
For any business, the need to make the most of its assets and resources is a strong-felt one, which calls for
integrating available MES products with APS systems. Opcenter Execution Discrete offers the possibility of
interacting with Opcenter APS, the Siemens solution for APS management, to close the gap between planning/
scheduling and execution.
In this integration, a continuous bidirectional exchange of information between Opcenter APS and Opcenter EX
DS is foreseen for what concerns Work Orders, Work Order Operations and Machines.
It is possible to schedule Execution Groups directly from the Opcenter APS environment, provided that the relative
integration is enabled and correctly configured.
If you are a user with the APS role, you can:
• Use Opcenter APS to choose the Work Orders and/or the Execution Groups that need to be planned and/or
scheduled for execution in Opcenter EX DS.
• Re-schedule any Work Orders that, for any reason, can no longer be executed according to schedule:
subsequent planning activities by Opcenter APS can re-schedule them in order to update the planning
accordingly.
• Import Work Orders, Work Order Operations and Execution Groups into Opcenter APS, schedule them according
to the APS system's capabilities and update Opcenter EX DS with the new expected start and end times and the
Machines to be used.
• Refine the production plan on the basis of Machine availability and theoretical production duration.
During these planning and scheduling activities, if changes are made to production, Opcenter EX DS side, then
Opcenter EX DS will expose data to Opcenter APS in order for corrective measures and adjustments to be adopted
to the schedule.
Virtually nothing is left to chance when the person with the APS role is planning and scheduling Work Order
Operations, because he/she will be using data related to what is actually happening on the shop floor, and not
merely making assumptions out of context.

3.48 Integration with Teamcenter and SAP
Opcenter Execution Discrete provides functionalities to integrate with Teamcenter Manufacturing. The following
three scenarios are possible:
• integration with both Teamcenter and SAP
• integration with Teamcenter only.
• integration with SAP only.

Integration with Teamcenter and SAP
Opcenter Execution Discrete provides functionalities to automatically download and release SAP and
Teamcenter production processes.

142

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 143

Product Features
Integration with Teamcenter and SAP

This makes it possible to download the following data to the Opcenter EX DS system:
• From Teamcenter:
• Bills of Processes (BOP)/Master Plans
• Materials
• Tools
• Documents
• Work Instructions
• Equipment
• Defects
• Defect Groups
• Failures
• Skills
• Human Resources
• Quality Inspections.
• From SAP:
• Production Orders
• Master Plans
• Serial Numbers.
The figure below summarizes the flow of data among Opcenter EX DS, Teamcenter and SAP.

For what concerns Documents, also 3D Files and Product Views can be associated to the Product or to the
Operations. To correctly visualize these 3D Files and Product Views, a link can be received from Teamcenter, so
that, in the Operator Terminal runtime screen, the Teamcenter EWI component embedded in the page can be
opened directly without downloading any local files to Opcenter EX DS.
In alternative, it is possible to download the Product Views converted into PLMX files. Bear in mind that, to be able
to function properly in disconnected mode from Teamcenter, the following elements must be taken into
consideration:
• Known Functional Gaps
• no videos

Opcenter Execution Discrete 2507 - Product Overview

143


## Pagina 144

Product Features
Integration with Teamcenter and SAP

• no BoM Tree selection
• no cross-section
• no mark-up
• Known Non-Functional Requirements
• maximum file storage dimension, sizing of Opcenter Database
• client performance on huge Product Views.

How Data Flows Teamcenter-side
From Teamcenter, a Product Engineer is able to create:
• Master Plans
• Processes
• Operation Folders
• Operations
• Materials
• Tools
• Data Collections
• Equipment
• Quality Inspections
• Failures
• Skills
• Human Resources
and download them to the Opcenter EX DS system (step 1).
After this action, Opcenter EX DS is capable of storing and releasing a production order created by SAP.
To do this, Opcenter EX DS can request that Teamcenter provide a specific Bill of Process that matches the
production order details (steps 3 and 4).
Thanks to the adoption of dedicated configuration keys, Opcenter EX DS is capable of verifying whether a preexisting version of a particular item is out of date and subsequently update the data contained in the system (step
4).
When an issue arises during production, Opcenter EX DS collects the data of the Non-Conformance, as well as any
documents describing the issue, and can send this information to Teamcenter (step 5). Also, Opcenter Connect
Teamcenter collects any data regarding the completion of WO and WOOP to create what is known as the the AsMaintained structure in Teamcenter.
Non-Conformance updates that take place in Teamcenter can be notified to Opcenter EX DS and viceversa.

How Data Flows SAP-side
Opcenter EX DS provides an automatic mechanism to download an ERP order and release it for production (step 2).
Upon completion of each Work Order Operation, as well as upon completion of the production order, Opcenter EX
DS issues a confirmation message to SAP (step 6).
SAP and Work Orders based on Master Plans
Creating a Work Order based on a Master Plan entails interaction with SAP. In this case, SAP sends the
production order with the list of parts to be assembled. On the basis of this information, the MES takes the
Master Plan and selects a series of Operations to create the Work Order.

Integration with Teamcenter only

144

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 145

Product Features
Integration with Generic Distributed Numerical Control (DNC) Systems

In this scenario, no production orders are downloaded from SAP. In brief, Work Order Headers are directly created
in Opcenter EX DS and then merged with suitable As Planned BOPs downloaded from Teamcenter Manufacturing.
According to system configuration, it is possible to request Teamcenter for As Planned BOP resolution and to
automatically trigger the merge of the Work Order Header with the downloaded As Planned BOP. Furthermore, the
system is also able to automatically release the resulting Work Orders to production.
In addition, in this scenario, if desired, you can configure the automatic creation of Issue Reports on the basis of
Non-Conformances declared in Opcenter Execution Discrete.
The figure below summarizes the flow of data between Opcenter EX DS and Teamcenter.

Integration with SAP only
In this scenario, it is possible to import the following data from SAP:
• Materials
• Tools
• Bills of Processes
• Documents
• Work Orders
• Serial Numbers.
After the import, data is then fully managed by Opcenter Execution Discrete.

3.49 Integration with Generic Distributed Numerical Control (DNC)
Systems
It is standard practice for production plants to employ NC machines. Opcenter Execution Discrete can interact with
DNC systems to close the gap between CNC program definition on one side and execution instructions on the other.

How you can benefit from this integration
This synergy makes it possible for you as a Product Engineer to:
• Import machines and DNC items from the DNC system, so that DNC-generated engineering data can be reutilized.
• Map machine IDs between DNC and Opcenter EX DS.
• Define the associations among imported machine-program pairs and products, so that the system will know
which CNC programs are available on which machine to work on which product.

Opcenter Execution Discrete 2507 - Product Overview

145


## Pagina 146

Product Features
Integration with Opcenter Connect MOM

Opcenter EX DS makes it possible for you to connect to a DNC system and retrieve CNC program information
available for each machine.
Connection to a DNC system requires developing a dedicated plugin: for more information, see section
Developing a Custom Plugin in the Opcenter Execution Discrete Extensibility Guide.
You can associate each CNC program to the machines on which it can run, as well as the products for which it can
be used: at this point, each association is stored and will be presented as a possible selection when working in the
context reflecting its configuration.
As an Operator, thanks to this integration, when you start a CNC operation on a machine, provided that the
dedicated flag of the operation is explicitly set to CNC, you will be presented with a list of CNC programs from which
to choose. Opcenter EX DS will display only those CNC programs that are appropriate for that particular context,
according to configuration. By narrowing down the range of choices, Opcenter EX DS simplifies selecting the right
CNC program to be used for a certain product on a certain machine. After you choose the CNC program that satisfies
your needs, the system downloads it to the selected machine.

3.50 Integration with Opcenter Connect MOM
Thanks to the possibility of integration with a product known as Opcenter Connect MOM (Opcenter CN MOM),
Opcenter Execution Discrete gives you the possibility to:
• exchange structured messages with the Shop Floor to automate certain activities during production execution.
For more information on which activities can be automated via this integration, see Exchange of Messages with
the Shop Floor.
• import and delete data. For more information on which data can be imported and deleted via this integration,
see Import Data Flows.
• send Output Messages to external systems.
• exchange Kanban Messages with the External System managing the Warehouse, with Material requests and
related responses, containing information on the state of Kanban Calls made to request the replenishment of
Materials.
• exchange messages with Opcenter Connect MOM in case of Multiplant scenario.
For more information on how to configure the integration with Opcenter CN MOM, refer to the section How to
Integrate Opcenter Execution Discrete with Opcenter Connect MOM of the Opcenter Execution Discrete Installation and
Configuration manual.

3.51 Integration with Teamcenter Share
Integration with Teamcenter Share allows you to share documents with other users or teams through a
collaborative environment.
Document sharing is achieved by uploading documents from Opcenter Execution Discrete to Teamcenter Share
into so-called Projects defined on that environment.
The Documents shared by Opcenter Execution Discrete can be related to Non-Conformances or Documents
collected during production execution.
The Projects that will contain the uploaded Documents are automatically created according to the context to which
the uploaded Documents refer.
In the case of Non-Conformances, if the context is a Work Order Operation or a produced Material Tracking Unit, the
Documents will be uploaded to a Project named as the related Word Order NId.
If the context is a production entity (for example, a Tool, a piece of Equipment or a consumed Material Tracking
Unit), the target Project will be named as the Non-Conformance NId.

146

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 147

Product Features
Integration with the Shop Floor via OPC UA

Documents collected from the shop floor will be uploaded to Projects named as the Work Order NId, similar to what
occurs for Non-Conformances on WOO or MTUs, as mentioned above.
Once the system is correctly configured and integration is also enabled on Opcenter Execution Discreteside,
entitled users can connect to Projects on Teamcenter Share via SAM authentication.
As a Production Coordinator, you can:
• from the Order As Built page: share any documents captured during production execution from the shop floor.
• from the Non-Conformances page: share any documents attached to Non-Conformances (related to Work
Order Operations, Tools, Equipment or MTUs).
For more information on how to correctly configure the system, see section Teamcenter Share Integration
Support of the Opcenter Execution Foundation Installation Guide.

3.52 Integration with the Shop Floor via OPC UA
Opcenter Execution Discrete provides a standardized way, in common with other products based on Opcenter
Execution Foundation, to manage interoperability with the Shop Floor.
This standardized way relies on so-called handshake protocols that use OPC UA tags via Automation Gateway.
These handshake protocols serve as a basis for the implementation of contracts, that are interfaces able to
exchange data between MES and the Shop Floor with the purpose of realizing business use cases.
More specifically, a contract includes:
• the definition of a message
• the behavior of the system depending on the value of the message parameters
• a direction, that can be: from MES to the Shop Floor or from the Shop Floor to MES.
Its implementation is based on:
• One or more Automation Node Types
• One or more Signal Rules
• One or more handshake commands, that manage the communication in any direction
• One or more contract commands, containing the specific business logic.
A heartbeat mechanism is available to check the connection with the automation system.
Opcenter Execution Discrete provides the following out-of-the-box contracts:
• RequestOrderInfo
• ExecuteSaveSequence
• RequestNext
• ExecuteWorkOrderOperation
• ReqMaterialConsumption
• ExecConsumeMaterials
• TrackItemLocation
• ExecuteWorkInstructionDataCollection
• ExecuteQualityInspection
Additional use cases can be implemented by following extensibility patterns and guidelines as described in section
How to Create a Custom Contract for Shop Floor Integration of the Opcenter Execution DiscreteExtensibility Guide.
Automatic/Semi-Automatic acquisition of Materials, Tools, Data Collection, and Quality Inspection data on the
Operator Terminal is possible provided that the system is properly integrated with the Shop Floor (Automation
Gateway).

Opcenter Execution Discrete 2507 - Product Overview

147


## Pagina 148

Product Features
Integration with the Shop Floor via OPC UA

3.52.1 Handshake Protocols
Handshake protocols are intended to provide reliable, consistent and configurable communication patterns.
Many handshake mechanisms are possible.
Each out-of-the-box use case provided by Opcenter Execution Discrete is based on the PLC to MES (synchronous
mode) handshake protocol. In addition, the PLC to MES (asynchronous mode) handshake protocol is also available
to be used in case of custom use cases.
Each handshake protocol is based on:
• a request tag (sequenceNo), written by the sender system, and representing a signal that some data is ready to
be processed
• a response tag (acknowledgeNo), written by the destination system, to notify that a message has been
correctly processed (that is, data has been read)
• an explicit read of the message data upon notification that a new message is ready, for consistency reasons. The
sender system is responsible for ensuring that all the requested data is ready before writing the sequenceNo
tag.
The following sections are intended to provide a general overview of each handshake, mainly focusing on the
sender and destination systems. All the intermediate layers that may be available in a scenario (such as the OPC UA
Server and the Automation Gateway) are omitted on purpose. On the PLC side, a message buffer is depicted for
description purposes, but its presence is not mandatory.
As of version 2207, the PLC-to-MES handshakes leverage the new direct read from PLC functionality. This
allows a better data consistency handling, and low acquisition cycles for most of the involved automation
parameters, with benefits for the overall system.
The suggested configurations of the Automation Node Instance Parameters involved in handshake
messages are the following:
• Setting Automation Node Instance Parameter sequenceNo to OnChange.
• Setting the acquisition mode for all the remaining parameters to a very low value (for example, 10 or 15
minutes).
As a result, the load of both the OPC Server and the PLC is kept to a minimum. Data consistency is
guaranteed by the protocol, which performs a direct Read from the device.
For more information about direct reads from the PLC see the documentation of the
AutomationReadMaxAge method ( How to Read and Write on Automation Node Parameter Values page in
the Opcenter Execution Foundation Development and Configuration Guide).

3.52.1.1 PLC to MES (synchronous mode)
This handshake protocol can be used whenever the automation system needs some information from MES which is
relevant for the production. A response is required for the automation business logic to proceed.

148

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 149

Product Features
Integration with the Shop Floor via OPC UA

3.52.1.2 From PLC to MES (asynchronous mode)
This handshake protocol can be used whenever the automation system needs to send some information to MES,
but does not require a response to proceed. The automation business logic waits for the request to be
acknowledged (message received) before proceeding.

Opcenter Execution Discrete 2507 - Product Overview

149


## Pagina 150

Product Features
Integration with Additive Manufacturing Network

3.53 Integration with Additive Manufacturing Network
Integration with Additive Manufacturing Network allows you to import Print Jobs defined in this specific
environment into Opcenter Execution Discrete, in order to streamline Shop Floor operations. A Print Job represents
a set of items to be printed together. In this integration scenario, Additive Manufacturing Network represents the
source of the production schedule for Opcenter EX DS.
A sales order, made up of several orders, is defined in Additive Manufacturing Network. These orders can then be
assigned to different Print Jobs in AM Network. Each Print Job is used to print one or more 3D Parts, considering the
quantity of each order.
Once integration between the two systems is enabled and a series of items has been configured in both
environments to establish a proper mapping, Print Jobs in Ready status can be imported and the following items
are automatically created in Opcenter EX DS:
• Work Orders with their related Work Order Operations, according to the routing template selected in Additive
Manufacturing Network, i.e. the corresponding As-Planned Process in Opcenter EX DS.
• Execution Groups, made up of the initial Operations, up to and including the printing operation (marked as AM
relevant in its Work Operation Type), belonging to the Work Orders that have been imported. The preferred
machine (the same of the corresponding Print Job) on which the Execution Group Phases should be executed
and the linked Print Job File are imported as well.
• Metadata about Print Job Files, which are linked to the related 3D Printer and Material.
• Final Material of the Work Order, which is the actual part to be printed.
For more information on the list of items to be pre-configured for the mapping, see section How to Benefit from
Integration with Siemens AM Network in the Opcenter Execution Discrete User Manual.
In addition, it is possible to import also 3D Printers and related 3D Printer Types.
When the Execution Group is started and completed from the Operator Landing page (legacy), the production
status is notified to AM Network and the Print Job state in the AM Network environment changes accordingly.
When some quantity is scrapped on the Work Orders, the total amount of failed quantity is notified to AM Network
so that the failed parts can be rescheduled in the main backlog and printed again.
In addition, when the Work Orders reach their final status, either they are completed, scrapped or aborted, AM
Network is notified as well.
As a Production Coordinator or Product Engineer, you can:
• from either the Work Orders or the Execution Groups pages: import ready Print Jobs.
• from the 3D Printers page: import 3D Printers and their related 3D Printer types.
For more information on how to correctly configure the system to enable the integration, see section How
to Integrate Opcenter Execution Discrete with Additive Manufacturing Network in the Opcenter Execution
Discrete Installation and Configuration manual.

3.54 Integration with Intraplant Logistics (Opcenter IPL)
Thanks to the possibility of integration (by way of Data Integration System) with a product known as Opcenter
Intraplant Logistics (Opcenter IPL), Opcenter Execution Discrete allows you to manage the alignment of the
Equipment Hierarchy and Kanban calls, synchronizing them between production in Opcenter EX DS and Opcenter
IPL.
In this integration, Opcenter IPL must be aligned with the default Equipment Hierarchy present in Opcenter
Execution Foundation that is used by Opcenter EX DS during production. This information is used to manage
different functionalities in Opcenter IPL, such as material stock, material requests, inventory, etc.

150

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 151

Product Features
Powder Batch Management

Another use case is the management of the Kanban calls that are triggered by Opcenter EX DS during production,
and managed in their satisfaction by Opcenter IPL. Also, when a Kanban call is cancelled by an Operator
in Opcenter EX DS, a notification in merit is sent toOpcenter IPL. Lastly, when a Kanban call is satisfied and the
material is delivered to the production line, Opcenter IPL is informed as to the quantity that reached the
destination.
High Availability and IPL
Wherever High Availability is mentioned in relation to procedures for the integration of IPL, it must be
specified that High Availability is intended for Opcenter Execution Foundation contexts, whereas Opcenter
IPL currently does not support HA.

3.55 Powder Batch Management
Powder Material Batches (also referred to as Powder Batches) represent the actual raw material to be used in a 3D
printing operation and are instantiated from Powder Materials.
At the time of creation, it is possible to set the minimum quantity allowed for the Powder Batch. In addition, you
can set a value for the maximum number of times the Powder Batch can be recycled before it becomes unavailable
for production.
With each operation, the following quantity checks are performed:
• If the current quantity reaches the minimum quantity value, the Powder Batch is set to Quarantine status and it
must be recycled before it can be mixed again.
• If, after the Powder Batch has been recycled, its current quantity is still less than the minimum quantity value,
the Powder Batch is set to Mixable status and it must be mixed with another batch in order to be used in
production.
• If the Powder Batch has been mixed with another batch with quantity equal to 0 or has reached the recycle
threshold, its status is set to Spent and the batch is no longer available for production.
• If the Powder Batch has been consumed entirely in a 3D Printing Operation and its quantity is equal to 0, its
status is set to Consumed and it is no longer available for production.
In addition, Powder Batches can be loaded in Containers which can then be connected to 3D Printers. The entire
content of the Container is moved to the 3D Printer, to be used for 3D Printing operations.
As a Production Coordinator, you can:
• instantiate Powder Batches from Powder Materials.
• preload Powder Batches in Containers.
• view historical data about Powder Batches.
As an Operator, you can:
• load Powder Batches directly into 3D Printers.
• load Powder Batches in Containers and connect the Containers to 3D Printers.
• replenish the Powder Batch quantity (this applies also to Batches loaded in Containers), which is added to the
quantity already loaded.
• (if the Barcode App provided by Opcenter Execution Foundation has been installed) type or scan a Batch ID and
view the corresponding result.
• unload the Powder Batch from the 3D Printer or from the Container, if a wrong batch has been loaded by
mistake.
• track the Powder Batch used during 3D printing operations for single Work Orders or for Execution Groups. If the
Powder Batch is inside a Container, the identifier of the used Container is tracked as well.
As a Product Engineer, in addition to loading/unloading and replenishing the Powder Batch, you can:

Opcenter Execution Discrete 2507 - Product Overview

151


## Pagina 152

Product Features
Substrate Management

• recycle Powder Batches.
• mix Powder Batches.
• amend the quantity of Powder Batches, if not aligned with the information stored in the system (for example,
due to recycling or mixing operations).
• change Powder Batches status.

3.56 Substrate Management
A substrate is the build plate upon which 3D objects are printed by using a 3D printer. Since final items are
developed upon substrates, Opcenter Execution Discrete treats substrates as specialized tools, which is why they
are created as tool definitions, and instantiated as tool entities. Substrates are configured and associated with
Work Order Operations. Additionally, Opcenter EX DS has a dedicated interface to treat and maintain substrates.
Substrates are created as tool instances. At the time of creation, it is possible to set the minimum thickness the
substrate is allowed to reach. Additionally, you can also set a value for the maximum number of times a substrate
can be treated. To monitor the substrates you configured, you can choose to be notified if a substrate has reached a
value close to the minimum thickness or the maximum treatment count.
Via a dedicated web screen, Opcenter EX DS allows for further substrate management by:
• Setting a current substrate thickness value
• Changing substrate thickness
• Changing the treatment count
With every update, thickness and treatment checks are performed:
• If the current thickness falls (manually or automatically) below the minimum thickness hold value, the substrate
is set to OnHold status and it is not available for production.
• If the current thickness of substrate falls (manually or automatically) below the minimum thickness warning
value, the substrate is set to Warning Available status and it is available for production.
• If the treatment count rises (manually or automatically) above the maximum treatment count hold value, the
substrate is set to OnHold status and it is not available for production.
• If the treatment count warning rises (manually or automatically) above the maximum treatment count warning
value, the substrate is set to Warning Available status and it is available for production.
As a Production Coordinator, you can:
• Instantiate Substrates from Tool Definitions.
• View historical data about Tools.
As an Operator, you can:
• enter values about Substrate usage manually.
• acquire values about Substrate usage from the field and then confirm them.
• view historical data about Substrate usage.
Opcenter Execution Discrete supports a specialized type of Tool, known as a Substrate. As a Product Engineer, you
can also:
• Perform substrate treatment, where specialized procedures such as machining and blasting are performed on
the Substrate with the intention of optimizing substrate surface quality.
• Reduce substrate thickness by clicking a dedicated button, without opening the Substrate in edit mode.
• Perform maintenance activities, where regular maintenance activities such as cleaning and troubleshooting are
performed to ensure that the surface-level impurities of the substrates are removed, and they perform
optimally.

152

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 153

Product Features
Print Job File Management

3.57 Print Job File Management
Print Job File management requires developing one or more dedicated plugins: for more information, see
the Opcenter Execution Discrete Extensibility Guide.

Print Job Files are designed to contain information to be used by a 3D printer to create products by means of
Additive Manufacturing processes.
Interaction with 3D printers is managed through custom plugins dedicated to:
• retrieve Print Job Files from an external repository (Import Plugins);
• download a Print Job File to a 3D printer (Transfer Plugins).
Different brands and/or models of 3D printers may require different Import and Transfer Plugins.
The system allows associating a Print Job File to a possible combination of these entities:
• Machine (3D printer), matching the 3D Printer Type.
• Process Operation (if the operation is specifically flagged as “AM-relevant”).
• Produced Material.
• Work Order Operation.
• Execution Group Phase.
Thanks to these associations, the system is able to pilot the plugins in order to:
• Retrieve the file from a Print Job File repository.
• Present the Print Job Files to the shop floor operator during operation execution.
• Download them to the correct 3D printer.
For serialized production, the system is able to link specific Serial Numbers to a Print Job File. This operation can be
performed either manually, selecting the Serial Numbers that are currently active among those associated to the
started Work Order Operation, or generating a runtime Print Job File from a Template Print Job File associated to
the Work Order Operation or Execution Group Phase.

3.58 Print Job File Pre-Transfer Management
Specific types of 3D Printers may require an intermediate Print Job File from which they will generate the final Print
Job File, to be used to complete the printing operation.
During this preliminary phase, the 3D Printer processes the received Print Job File and enriches it with additional
parameters related to the current status of the Printer itself. Consequently, the same Printer can generate different
Print Job Files in different moments.
Print Job File processing may require a huge amount of time, consequently the intermediate Print Job File must be
pre-transferred to the Printer as soon as possible, for example when the Work Order is released, to have the final
Print Job File available when the printing must start.
Since the content of the final Print Job File is strictly related to the current status of the Printer, the same Printer
can generate different Print Job Files in different moments and each file can become obsolete after a predefined
amount of time, even if all generated Print Job Files are maintained in the printer memory and can be selected
while starting the printing operation.

Example

Opcenter Execution Discrete 2507 - Product Overview

153


## Pagina 154

Product Features
Management of Intra-Plant Logistics

The Work Order requires printing 1000 clips using four 3D Printers, and each of them is able to print 50 clips
simultaneously.
As soon as the Work Order configuration is completed the user sends the same Print Job File to all involved 3D
Printers, then each printer reworks and enriches the received file generating a new one. The final files may differ
because of any temporary conditions (as for example the current temperature of each printer) but in any case each
file, after being selected at runtime, will be used by the printer that generated it, to produce exactly the same 50
clips.

3.59 Management of Intra-Plant Logistics
Opcenter Execution Discrete deals with those activities related to Transportation Management, or Intra-Plant
Logistics (IPL), for transporting items inside a production plant for either storage or packaging purposes.
As a Product Engineer, you can:
• create Logistic Classes for grouping similar Materials or Tool Definitions for logistic purposes (transportation,
packaging).
• create Buffer Definitions to be used to represent specific areas or accessories (such as wagons or carts)
allocated for storing specific types of Materials and/or Logistic Classes.
• modify and delete Buffer Definitions.
• create Revisions of a selected Buffer Definition.
As a Production Coordinator, you can:
• create, modify and delete Buffers.
• change the Buffer Status.
• add Material Tracking Units to the Buffer.
• manage Handling Units (creating them and managing their status) and subsequently loading and/or unloading
Material Tracking Units.
• declare and accept (or reject) one or more Logistic Requests at a time.
• execute Transport Operations.
As an Operator, you can:
• manage Handling Units (creating them and managing their status) and subsequently loading and/or unloading
Material Tracking Units.
• declare and accept (or reject) Logistic Requests.
• execute Transport Operations.

3.60 Monitoring of the Production Status
Monitoring production data is crucial to achieve your production targets with greater ease.
When new items are created in the system, either inserted by the user or from external data flows, the
corresponding data could be not valid.
For example, if a list of Bill of Materials is received without the complete list of Materials belonging to it, the final
product cannot be produced because the system does not have all the required information.
As a consequence, there might be the risk of having invalid ERP Orders for a specific Final Product Family, because
data is missing or not properly imported.
Conversely, if the structures imported are valid, and therefore the final product can be produced, the corresponding
ERP Orders can be considered valid and thus scheduled.

154

Opcenter Execution Discrete 2507 - Product Overview


## Pagina 155

Product Features
Quality Gate Management

Opcenter Execution Discrete makes it possible to monitor the following entities providing also predefined results
illustrated below, to have a complete overview of the production progress:
Entity

Result

Import Data Flows

• Succeeded, the data flow has been validated
• Warning, the data flow has been validated in part, for example
because data is missing
• Failed, the data flow has not been validated

ERP Orders

• Succeeded, ERP Orders are valid and consequently can be
produced
• Warning, some ERP Orders are not valid and cannot be
produced, because some data is missing or has not been properly
imported
• Failed, ERP Orders are not valid and consequently cannot be
produced

In addition the Opcenter Execution Discrete UI Application contains a page dedicated to the monitoring of
Production items, from which the user can quickly and easily verify the milestones reached by any Material Tracking
Unit with the related timestamp.

3.61 Quality Gate Management
If a Work Center or Unit has been configured as Quality Gate during the production environment configuration, the
Operator can perform additional actions on the production items being produced on the monitored Equipment.
Quality Gates monitor the Work Order Operations which are completed on the monitored Work Center or Unit with
negative results at Activity level. If the Quality Gate has been properly configured, then the failed Activities can be
repaired. The Work Order Operation started on a Work Center or Unit which is a Quality Gate will block the Work
Order production until all failed Activities are repaired (or repeated) with a positive result.
The Activities that can be repaired are related to:
• Material Consumption
• Quality Inspection
• Tool and Screwing Tool usage
• Work Instruction
If Quality Gate management has been enabled, information regarding the Quality Gates, and the pieces of
Equipment to which they are associated, as well as the Activity to which they refer will be displayed in the As Built
Order and the Genealogy pages.

Opcenter Execution Discrete 2507 - Product Overview

155
