---
title: "OpcenterEXDS_InstallationGuide"
source_file: "SourcesMd/01 Opcenter 2507 Manuals/OpcenterEXDS_InstallationGuide.md"
project: "Brembo B-Spark - Standard Platform Documentation"
platform: "Siemens Opcenter Execution Discrete 2507"
scope: "Core_Standard_Manual"
plants: [SHARED]
---

# Opcenter Execution Discrete 2507 - Installation and Configuration Manual

> Documento sorgente: `E:\BremboDocs\01 Opcenter 2507 Manuals\OpcenterEXDS_InstallationGuide.pdf`
> Tipo: PDF - Pagine originali: 281

## Publication Information

- **Product**: Opcenter Execution Discrete
- **Version**: 2507
- **Document**: Installation and Configuration Manual
- **Publication date**: 08/2025
- **Revision**: PL20250519659659531
- **Copyright**: © Siemens AG 2025
- **Publisher**: Siemens AG, Digital Industries, Postfach 48 48, 90026 NÜRNBERG, GERMANY
- **Technical note**: Technical data subject to change

## Guidelines

This manual contains notes of varying importance that should be read with care:

- **Important**: Highlights key information on handling the product, the product itself, or a particular part of the documentation.
- **Note**: Provides supplementary information regarding handling the product, the product itself, or a specific part of the documentation.

### Trademarks

All names identified by ® are registered trademarks of Siemens AG. The remaining trademarks in this publication may be trademarks whose use by third parties for their own purposes could violate the rights of the owner.

### Disclaimer

We have reviewed the contents of this publication to ensure consistency with the hardware and software described. Since variance cannot be precluded entirely, we cannot guarantee full consistency. However, the information in this publication is reviewed regularly and any necessary corrections are included in subsequent editions.

### Cybersecurity

Siemens provides products and solutions with industrial cybersecurity functions that support the secure operation of plants, systems, machines and networks. In order to protect plants, systems, machines and networks against cyber threats, it is necessary to implement and continuously maintain a holistic, state-of-the-art industrial cybersecurity concept. Siemens products and solutions constitute one element of such a concept. Customers are responsible for preventing unauthorized access to their plants, systems, machines and networks. Such systems, machines and components should only be connected to an enterprise network or the internet if and to the extent such a connection is necessary and only when appropriate security measures (for example, firewalls and/or network segmentation) are in place. For additional information on industrial cybersecurity measures that may be implemented, please visit https://www.siemens.com/cybersecurity-industry.

Siemens products and solutions undergo continuous development to make them more secure. Siemens strongly recommends that product updates are applied as soon as they are available and that the latest product versions are used. Use of product versions that are no longer supported, and failure to apply the latest updates may increase the customer's exposure to cyber threats. To stay informed about product updates, subscribe to the Siemens Industrial Cybersecurity RSS feed at https://www.siemens.com/cert.

## Document Metadata

| Field | Value |
| --- | --- |
| ID | OpcenterEXDS_InstallationGuide |
| Title | Installation and Configuration Manual |
| Product Title | Opcenter Execution Discrete |
| Version Title | 2507 |
| Product Version | OpcenterEXDS_2507 |
| Category | Installation, Configuration, Support |
| Summary | Provides detailed information on how to install and configure Opcenter Execution Discrete. |
| Audience | System Integrator, Support Engineer, Project Engineer, Commissioning Engineer |
| Revision | PL20250519659659531 |
| State | Published |
| Author | Siemens AG |
| Language | en-US |

## Before You Start

Before you start setting up the scenario, you must:
• verify that all software and hardware prerequisites are satisfied.
• retrieve a valid license for both Opcenter Execution Foundation and Opcenter Execution Discrete and install the
PLM License Server as described in section Installing the PLM License Server in the Opcenter Execution
Foundation Installation Guide.
• design your scenario following the suggestions on how to implement security strategies so that any risks and
threats that may affect your system are successfully mitigated. For more information, see Opcenter Execution
Foundation Security Concept guide.
• set the communication protocol to https for security reasons. For more information, see section Configuring the
Opcenter Execution Foundation Service Layer Securely (HTTPS) of the Opcenter Execution Foundation Installation
Guide.
• configure RabbitMQ nodes using SSL for security reasons. For more information, see section Configuring
RabbitMQ nodes using SSL in Windows of the Opcenter Execution Foundation Installation Guide.

Notes about Licensing Configuration
The Installing the PLM License Server procedure referenced above is tailored for Opcenter Execution
Foundation, but is also valid for Opcenter Execution Discrete.
A unique license file (with .lic extension) can be generated.
The Opcenter Execution Discrete runtime host can be run even if one of the following cases occur:
• the License Server is not up and running; therefore, licenses cannot be verified because the License Server is not
responding.
• no license has been activated.
• the maximum number of seats has been reached.
• the license validity is expired.
In these cases, the system will return:
• a warning message traced with both Event Tracing for Windows (ETW) and Windows Event Viewer every 20
minutes; the current license expiration date is shown both in ETW, in verbose mode, and in Solution Studio HM
details at system start-up.
• a warning pop-up in any connected UI.

## Supported Scenarios and Prerequisites

Opcenter Execution Discrete requires Opcenter EX FN with all related Apps as a prerequisite and supports all
Opcenter EX FN scenarios and prerequisites, that are:
• stand-alone (All-In-One) scenario
• stand-alone with separated database scenario
• Distributed scenario (also in the High Availability variant).
For detailed information on those supported scenarios and prerequisites, refer to chapters Opcenter Execution
Foundation Supported Scenarios and Opcenter Execution Foundation Prerequisites in the Opcenter Execution
Foundation Installation Guide.

Examples of Opcenter Execution Discrete Complex Scenarios
When implementing a complex scenario, consider that the number of Production Servers depends on the number
of concurrent users (in general, one for every 100 concurrent users). However, the following restrictions apply in
regard to the supported number of Production Severs:
RabbitMQ Configuration Mode

Supported Number of Production Servers

Active/Standby

1, 3, 4, 5, etc.
Two is not supported.

Cluster

1, 3, 5, etc. (any odd number).

In High Availability scenarios, the minimum number of Production Servers is 3.
• If message loss is not acceptable, configure RabbitMQ in Cluster mode and provide an odd number of
Production Servers >= 3.
• If message loss is acceptable, configure RabbitMQ in Active/Standby mode.
The following complex scenarios are described below:
• Load Balancing Scenario
• High Availability Scenario

Example of Load Balancing Scenario
The first image shows how a Load Balancing scenario may be built up.

To implement this type of scenario, the following hardware requirements are recommended:
Server Type

Logical Cores/Threads

Memory

Hard Disk

Production Servers

8 vCPU

32 GB

160 GB SSD

Reverse Proxy

4 vCPU

4 GB

30 GB

Database Servers

8 vCPU * number of
Production Servers

32 GB * number of
Production
Servers

Dependent from the data
size

Example of High Availability Scenario
The second image is an example of how you can implement a High Availability scenario.

In this case, the following hardware requirements are recommended:
Server Type

Logical Cores/Threads

Memory

Hard Disk

Production Servers

8 vCPU

32 GB

160 GB SSD

Reverse Proxies

4 vCPU

4 GB

30 GB

Database Servers

8 vCPU * number of
Production Servers

32 GB * number of
Production
Servers

Dependent from the data
size

## Installing Opcenter Execution Discrete

Independently from the Scenario you have implemented, Opcenter EX DS must be installed on the Engineering
Host. In Distributed Scenarios, the installation must be performed on all Engineering Hosts.
The installation can also be run in Silent Mode. For more information, see How to Install Opcenter
Execution Discrete in Silent Mode.

Prerequisites
The installation prerequisites are fulfilled.

Procedure
1. Execute the Start.exe program located in the ISO root folder and follow the wizard instructions.
2. Accept the conditions of the license agreement and confirm the security information. Open Source and ThirdParty licenses are selected by default. Then click Next.
3. Select the required option check boxes and click Next.
4. Click Install.
5. Upon completing the wizard, restart the computer.
6. (Only for Hybrid scenarios) Install Opcenter Execution Process. For details, see Installing Opcenter Execution
Process in the Opcenter Execution Process Installation and Configuration Manual.

## How to Install Opcenter Execution Discrete in Silent Mode

You can install Opcenter Execution Discrete in Silent Mode (that is, without human interaction) simply by executing
a script. The system will install all available setup components.
This procedure is valid only in case of fresh installation.

Prerequisites
The installation prerequisites are fulfilled.

Workflow
1. Enable the RemoteSigned PowerShell script execution policy.
2. Launch the setup script.

Enabling the RemoteSigned PowerShell script execution policy
1. Run PowerShell as Administrator.
2. Enter Get-ExecutionPolicy and press ENTER, to get the currently-active policy.
3. If one of the following values is returned for the current active policy:
• Restricted
• AllSigned
• Default
• Undefined
type Set-ExecutionPolicy RemoteSigned and press ENTER to set the current policy to RemoteSigned.

Remember the original value of the execution policy, as it must be restored at the end of the environment
configuration, after all the required PowerShell scripts have been launched.
The following values for the current active policy do not require a change of the policy for correctly
running the PowerShell scripts:
• Unrestricted
• RemoteSigned.

Note Keep in mind that to properly run PowerShell, you must move away from its default directory
(%WINDIR%\system32), otherwise the script execution will fail. You can choose any folder on which you
have writing rights.

Launching the Setup Script
1. Open the SetupScripts folder available in the root of the ISO.
2. Right-click the OpcenterEX-Setup-Launcher.ps1 script and select Run with PowerShell. The system will
install Opcenter Execution Discrete according to the following parameters:
Parameter

Value

$ProcessPath

The entire path to the Start.exe file. It is set to the ISO image root
folder by default.

Parameter

Value

$ArgumentList

It is set to /qb REBOOT=Suppress by default.
Other possible values are:
• /SILENT REBOOT=Suppress, to run the script in silent
mode, without displaying any setup information.
• /qb REBOOT=Suppress, to install Opcenter EX DS in a
folder differing from the default installation directory C:
\Program Files\Siemens.
For further information on the ArgumentList parameters, see the
PEAutoInstallenUS.pdf or PEAutoInstallenUS.chm, available in the
ISO image folder Documents\Readme\English.

$SilentMode

It is set to YES by default. The script is run in silent mode.
If set to NO (with $ArgumentList set to /qb REBOOT=Suppress), a
message box showing the installation result is displayed.

The system restart is not required.

Results
• Once completed, the PowerShell window is closed and Opcenter EX DS is installed in the default installation
directory %SITUnifiedSystemRoot%.
• The script returns the following value:
• 0 = Installation completed successfully.
• 1 = Installation completed successfully. Reboot is required.
• any other value = Installation failed.
• In case of error, you can consult the LaunchInstallation_Log[Datetime].txt log file, available in
%ProgramData%\Siemens\Automation\Logfiles\Setup.
• For details on the script, open the PowerShell command shell, type get-help .\OpcenterEX-SetupLauncher.ps1 -Full and click enter. Relevant information are returned, such as parameter and log file
information.

## How to Configure Opcenter Execution Discrete

The configuration procedure of Opcenter Execution Discrete is summarized in the following workflow.

Workflow
1. (Optional) Enable Opcenter Execution Discrete Error Tracing.
2. Perform Post-Setup Configuration.
3. Define Users and User Groups.
4. (Optional) Integrate the required Opcenter Execution Foundation Apps in the Solution.
5. (Optional) Import Signal Rules.
6. (Optional) Configure Opcenter Execution Discrete in Multilanguage.
7. (Optional) Configure Runtime Screens.
8. (Optional but recommended) Configure Cleaning Rules.
9. Deploy the Opcenter Execution Discrete Solution.
10. (Mandatory if Low Code UI Apps are present in your system) Deploy Low Code UI Apps.
11. (Optional but recommended) Index the System Databases.
12. (Optional) Configure the Documentation Center.
13. (Optional) Configure the Production Resolution Common Component.
14. (Optional) Configure the PLMX-Viewer.

### Enabling Opcenter Execution Discrete Error Tracing

This procedure allows you to enable error tracing on the machines where Opcenter Execution Discrete is installed.

Enabling Error Tracing on the Engineering Host
1. On the target machine, stop the following services, if running:
• SIMATIC IT UAF Log Router
• SIMATIC IT UAF Service
2. Launch the .bat files contained in the following folders:
• C:\Program Files\Siemens\SimaticIT\Unified\VApps\UADM\Trace
• C:\Program Files\Siemens\SimaticIT\Unified\Vapps\EXAM\Trace
3. Restart the services stopped in step 1.

Enabling Error Tracing on the Runtime Hosts
1. On the target machine, stop the following services, if running:
• SIMATIC IT UAF Log Router
• SIMATIC IT UAF Service
2. Create folder C:\Program Files\Siemens\SimaticIT\Unified\VApps\UADM\Trace if it does not already exist.
3. Copy the content of folder C:\Program Files\Siemens\SimaticIT\Unified\VApps\UADM\Trace from the
Engineering Host into the folder you have just created.
4. Create folder C:\Program Files\Siemens\SimaticIT\Unified\VApps\EXAM\Trace if it does not already exist.
5. Copy the content of folder C:\Program Files\Siemens\SimaticIT\Unified\VApps\EXAM\Trace from the
Engineering Host into the folder you have just created.
6. Launch the .bat file contained in the folder you have just created.
7. Restart the services stopped in step 1.

### Performing Post-Setup Configuration

After installing the product, you need to launch the Opcenter Execution Discrete configuration tool, which
creates the Opcenter Execution Discrete manufacturing solution of interest and performs many configurations
automatically.
In particular, the tool:
• Creates one of the following manufacturing solutions and loads all the required Apps:
• U4DM, dedicated to the management of Discrete functionalities in a complex production environment
that includes also Additive Manufacturing and High Variance activities. It includes
the Siemens_SIT_UADM UI Application.
• DS, dedicated exclusively to the management of Discrete functionalities. This Solution includes includes
Additive Manufacturing, but does not include functionalities related to High Variance production
environments. It includes the Siemens_OPC_EXDSBasic UI Application.
• OnePieceFlow, dedicated to the management of Discrete functionalities in a complex production
environment that also includes High Variance activities. It includes the Siemens_OPC_EXDSAdvanced
UI Application.
• Creates User Roles (groupings of permissions) to be assigned to User Groups in order to set constraints on the
runtime operations they are allowed to perform within the manufacturing solution. For information on the User
Roles supported by Opcenter EX DS, see section Access Control through Roles and Certifications in Opcenter
Execution Discrete Product Overview.
• Associates Roles with the required Function Rights.
• Creates event subscriptions.
• Configures the worker roles on which you want to distribute the business logic making up the project.
Important Starting from version 2407, the default Worker Role is .NET instead of .NET Framework. If you want
to use the previous .NET Framework Worker Role, see note in step 1 of the procedure below.
• Configures how the business logic making up the solution is distributed over different worker roles, by assigning
worker roles to the target host.
• Creates and configures the UI application, which means creating and configuring the project-specific single
page applications as containers of UI modules.
• Deploys the UI Application, which means generating project-specific single page applications on IIS.
For Low Code UI Applications powered by Mendix, it is necessary that you perform certain procedures
for deployment manually. For details, see section Deploying Low Code UI Apps.
The tool also creates the shortcuts to the Web User Interfaces on the desktop of the production machine.
Prior to launching the Opcenter Execution Discrete Post-Setup Configuration tool, if you have changed the
default port number (http\https), it is necessary to insert the new port number editing the value of the
Http port key in the following file:
• Siemens.Opcenter.Foundation.SolutionConfigurator.exe.config, located in
%SITUnifiedVAppsRoot%\UADM, if you want to create the U4DM , DS or OnePieceFlow solution.

Procedure
1. Browse to %SITUnifiedVAppsRoot%\UADM and launch
Siemens.Opcenter.Foundation.SolutionConfigurator.exe to create the U4DM, DS or OnePieceFlow solution.
Starting from version 2407, the %SITUnifiedVAppsRoot%\UADM folder contains the xml files that
adopt the new .NET technological stack.

The xml files that adopt the previous .NET Framework Worker Role are still available in
the %SITUnifiedVAppsRoot%\UADM\NetFramework folder.
If you want to configure the solution using the previous .NET Framework Worker Role instead of the
new .NET technological stack, you can replace the xml files contained in the %SITUnifiedVAppsRoot%
\UADM folder with those contained in the %SITUnifiedVAppsRoot%\UADM\NetFramework folder.
Statistical Process Control functionalities are supported only if they are executed by a .NET worker
(not .NET Framework). The involved commands published by the WorkInstruction App are
CalculateAttributiveStatistics, CalculateVariableStatistics, CalculateVisualStatistics and
ConfirmInspectionSample.

2. In the Opcenter Execution Post-Setup Configuration dialog box, insert the credentials of the user with
administrator rights (for example, domain\user or machine\user).
Note The user to be inserted here must be authorized to work with Opcenter EX FN Solution Studio.
3. In the drop-down, select Run commands on a new installation corresponding to the appropriate solution.

4. Click Execute.
5. (Only for Hybrid scenarios) Browse to C:\Program
Files\Siemens\SimaticIT\Unified\VApps\UAPI\POSTSETUP\Hybrid and then execute
Siemens.Opcenter.Foundation.SolutionConfigurator.exe (the Opcenter Execution Process post-setup) with
option Configure Process Hybrid Solution selected.
6. (Optional and only for Hybrid scenarios) Manually install those Opcenter Execution Process Hybrid Apps and
Extension Apps that you may need and that are not included by default in the installation (for
example, PIInteroperability and ProductionHistory).

Use of deprecated Additive Manufacturing functionalities in the U4DM Solution
The U4DM solution configured through the Post-Setup includes the Additive Manufacturing functionalities
provided by the dedicated Apps.
However, the deprecated screens provided by the AppU4DM App relative to the same functionalities are
still available in the product. To properly use these screens instead of the new ones:
1. Uninstall the following Apps from the configured solution:
• PrintJobFile
• PowderMgt
• PluginMgt
2. Enable the deprecated pre-checks and post-actions within the AppU4DM App.

3. Add the deprecated modules to the solution.
For detailed information on deprecated items, see the Deprecated Functionalities and Artifacts chapter in
the Opcenter Execution Discrete Release Notes.

### Defining Users and User Groups

When installing and configuring the application, you must define Users and User Groups to be used to access
applications (such as Opcenter Execution Foundation Solution Studio), operating via User Management
Component (UMC) Web User Interface. For this purpose, you must access the User Management Component (UMC)
login page.
Users enabled to use the Electronic Signature on Work Order Operations must be associated to a group
having the same name as the role created by Opcenter Execution Discrete Post-Setup Configuration tool.
All users with the ProductionCoordinator role must be added to the group previously created, using UMC.

Accessing the UMC Login Page
1. Open a supported browser.
2. Depending on your configuration, enter the address http://<ProductionMachineName>/UMC or https://
<ProductionMachineName>/UMC.

Workflow
1. Do either of the following:
• Import Windows Active Directory Users in UMC
• Create new Users.
2. Create User Groups.
3. Associate the Users to the Groups.
4. Associate Roles to Users and Groups.
5. (only for Low Code UI Apps) Grant Low Code UI Application Rights to Roles.
6. (Optional) Generate a Security Certificate for the APS or MPP role.
Alternatively, you can directly import Windows Active Directory Groups in UMC. In this case, the Users are already
associated to Groups and they must not be created or imported.

#### Importing Windows Active Directory Users in UMC

This operation can be time-consuming and may return zero results if Active Directory administration limits
are exceeded. We strongly suggest that you perform restricted searches.
To import Active Directory users in UMC via the UMC Web User Interface:
1. Open a supported browser.
2. Depending on your configuration, enter the address http://<ProductionMachineName>/UMC or https://
<ProductionMachineName>/UMC.
3. Open the  Users page and click Import Users.
4. In the Import Domain Users dialog box, insert the search criteria and click Search. The search criteria must
contain at least three characters.
5. Select the user you want to import and click Add.
6. Click Import to import the selected Windows user into the UMC database.

Additional Details
• Windows groups associated to the imported users are not imported into the UMC database.
• For imported users, user authentication is performed against the Windows System.
• Many fields imported from Windows cannot be modified via the UMC Web UI. You can modify only the
following fields by selecting the user and then by clicking Details:
• In the General tab: Language and Data Language.
• In the Info tab: Email2 and Email3.
• In the Status tab: Enabled.
• In the Attributes tab: UMC custom attributes can be created, modified and deleted.
• In the Groups tab: For all users, this tab displays only the user group membership.
• In the Account Policy tab: User expiration date can be modified. The alert fields and the
Password expiration days field are not applicable.
All other fields must be modified in Windows and are automatically synchronized by UMC.

This procedure imports only Active Directory users. Import of local Windows users is generally not
performed in Opcenter Execution Discrete because local users authenticate only locally against Windows
on the machine where they are present. They can be used only for configuration purposes (for instance, to
be associated to the Windows services running on the machine) and they cannot be used for Opcenter EX
DS authentication.
To import local Windows users into UMC, you must use the umx command-line utility:
%ProgramFiles%\Siemens\UserManagement\BIN\umx [-x commandUserName
commandUserPassword] -I -u -w userName [-r role]

where:
• commandUserName is the string representing the name of the user who is executing the command;
• commandUserPassword is the string representing the password of the user who is executing the
command;
• userName is the string representing the user name;
• role represents the role name, it must exist in UMC;
• -x switch: the command is executed by the user given as input parameter;
• -w switch: the user to be imported is a Windows user.

#### Creating Users

Operating from the UMC Web User Interface:
1. Open a supported browser.
2. Depending on your configuration, enter the address http://<ProductionMachineName>/UMC or https://
<ProductionMachineName>/UMC
3. Open the  Users page and click Add User.
4. Insert the required user information and click Update.

#### Creating User Groups

After importing Windows users in UMC or after creating new users, you must create user groups.

Procedure

1. Operating from the UMC Web User Interface, open the  Groups page and click Add Group.
2. Insert the required user group information and click Update.

#### Associating Users to Groups

After creating user groups, you must associate the users to the groups.

Procedure
1. Open the  Groups page and select a group. Then click Details.
2. In the Members tab, insert the name of the user to be associated to the selected group and click Save.

#### Associating Roles to Users and Groups

1. In the Solution Studio Home page, click
Account > Roles section of the sidebar.
2. In the Roles page, select the role of interest.
3. Click
Assign the selected role to Users or groups.
4. Click either the Users or Groups tab, to select the users or groups, configured from the User Management
component importing a .csv file, to be associated with the selected role.
5. To assign the selected runtime role to a user or a group, select the required user/group and click Assign
Users. It is also possible to assign roles to more users or groups simultaneously.
It is mandatory to assign the AccessControlViewer system role to all users.

#### Granting Low Code UI Application Rights to Roles

When Low Code UI Apps are involved, if you have been assigned with a particular Role native in Opcenter Execution
Discrete, you must possess specific rights to be able to perform certain actions that are fundamental to using the
product. The rights that you must possess depend on the Low Code UI App involved:
Low Code UI App

Rights

Opcenter Execution Discrete One Piece Flow

• SuperUser rights, in order to select the Equipment
for the terminals.
• Operator rights, in order to see the Operator
Terminal.

Opcenter Execution Discrete Complex Manufacturing

User rights, in order to see the Operator Terminal.

Opcenter Execution Discrete Repetitive Manufacturing

User rights, in order to see the Operator Terminal.

Opcenter Execution Discrete Quality Execution

• SuperUser rights, in order to select the Equipment
for the terminals.
• Operator rights, in order to see the Operator
Terminal.

Opcenter Execution Discrete Product Engineer

User rights, in order to see the engineering UI screens.

Low Code UI App

Rights

Opcenter Execution Discrete Production Coordinator

User rights, in order to see the engineering UI screens.

Opcenter Execution Discrete System Administrator

User rights, in order to see the system UI screens.

Opcenter EX DS System

User rights, in order to see the system UI screens.

In all cases, the Low Code UI App rights must be granted to the Roles present in Opcenter Execution Discrete, by
assigning the Low Code UI App User Roles defined in the .mda package to a Role.
The engineering of the Low Code UI App User Roles is performed in the Mendix environment, whereas only
the assignment to Roles is performed from Solution Studio.

Procedure
1. Click

Account in the sidebar and then select Roles.

2. Click the tile for the user-defined role you want to assign rights to and click
.
3. In the Role Configuration page, select the Low Code UI Application User Roles tab.
4. Do either of the following:
• If no Low Code UI App User Roles are assigned, click Assign User Role.
• If any rights are already present, click

to add any available Low Code UI App User Roles. Otherwise,

to remove the association, select one or more Low Code UI App User Roles and click
5. Associate the Users to the configured Role, according to your needs.

.

##### Selecting the Equipment

As a SuperUser, you can select the Equipment for a particular client.

Procedure
1. Operating on the Operator Terminal, log in with your credentials as a SuperUser.
2. In the Equipment Selection page, select the Equipment of your choice.
3. Click

.

#### Generating and Validating Security Certificates

To enable interaction with Teamcenter Manufacturing and/or Opcenter APS, you need an X.509 standard security
certificate. A certificate represents a specific module and it can be associated with one or more authorization roles
in order to grant a subset of user rights required by that module. In this manner, a certified module can
authenticate/authorize requests without human interaction.
The certificate can be generated either with a PowerShell 5 command or an OpenSSL command.

Prerequisites
If the certificate is generated using PowerShell, the Microsoft tool New-SelfSignedCertificate must be installed on
the Web Client machine. This tool is available as part of the Windows Software Development Kit (SDK), which you
can download from the Microsoft website (https://www.microsoft.com/en-us/download/details.aspx?id=8279).

For information on New-SelfSignedCertificate, see the related documentation (https://docs.microsoft.com/en-us/
powershell/module/pkiclient/new-selfsignedcertificate?view=win10-ps).

Workflow
1. According to requirements, do either of the following:
• Request an X.509 certificate signed by a trusted Certification Authority. For more information, refer to the
instructions provided by the chosen Authority.
• Generate a self-signed X.509 certificate either using Powershell or OpenSSL.
For security reasons, it is recommended that you use self-signed certificates only for test or
custom project environments.
2. On the Web Client Machines and the Production Machines, install the certificate.
3. On the Production Machines, associate the certificate with the required role (MPP for integration with
Teamcenter Manufacturing and APS for integration with Opcenter APS).
4. In the application to be integrated, set the certificate to be used. For more information, refer to the Teamcenter
Manufacturing or Opcenter APS documentation.
Time Synchronization
Bear in mind that the machine on which you generate the certificate and the machine on which the
certificate is validated (production machine) must be synchronized. If these machines belong to the same
domain, time synchronization is guaranteed by Active Directory. If machines are not in the same domain,
you must enable the Windows Time Service properly (https://technet.microsoft.com/en-us/library/
cc773061(v=ws.10).aspx).

Generating a self-signed Certificate using Powershell
1. Invoke the Powershell 5 New-SelfSignedCertificate command and passing in the required parameters:
• -DnsName, which contains the string of the project unique identifier. In order to be a valid certificate for
Opcenter EX DS, the following value must be specified:
• For integration with Teamcenter Manufacturing "CN=T4CLMIntegration,T=SimaticIT UA
Foundation"
• For integration with Opcenter APS "CN=PreactorIntegration,T=SimaticIT UA Foundation"
• -CertStoreLocation, which must be used to specify where the file is installed (such as cert:
\LocalMachine\My).
PowerShell example (integration with Opcenter APS)
$cert = New-SelfSignedCertificate -DnsName "CN=PreactorIntegration,
T=SimaticIT UA Foundation" -CertStoreLocation "cert:\LocalMachine\My"
-KeyExportPolicy Exportable -KeySpec Signature

PowerShell example (integration with Teamcenter Manufacturing)
$cert = New-SelfSignedCertificate -DnsName "CN=T4CLMIntegration,T=SimaticIT
UA Foundation" -CertStoreLocation "cert:\LocalMachine\My" -KeyExportPolicy
Exportable -KeySpec Signature

2. Start a Powershell command prompt with a user with administrative rights.
3. Pass the required parameters, as shown in the following example, to create a .PFX container:
$psw = ConvertTo-SecureString 'password' -AsPlainText -Force
Export-PfxCertificate -Cert $cert -FilePath C:\temp\cert.pfx -Password $psw

Generating a self-signed Certificate using OpenSSL
Execute the following commands:
OpenSSL example
C:\OpenSSL\bin>openssl req -config openssl.cfg -newkey rsa:2048 -nodes -keyout
key.pem -x509 -days 365 -out certificate.pem -subj /
CN="PreactorIntegration,T=SimaticIT UA Foundation"/
C:\OpenSSL\bin>openssl pkcs12 -inkey key.pem -in certificate.pem -export -out
certificate.pfx

Installing the Certificate
The X.509 certificate must be installed on the Web Client Machines and the Production Machines, adding it to the
local machine account in the Windows certificate personal store:
1. Double-click the .PFX file containing the certificate public key.
2. In the Certificate Import Wizard, select Local Machine as store location and click Next.
3. Click Next.
4. In the Private Key Protection wizard step, input the password for the certificate and click Next.
5. In the Certificate Store wizard step, set Place all certificates in the following store and browse Personal as
certificate store (system area where the certificate is kept). Then click Next.
6. Click Finish.

Associating the Certificate with the required Role
This procedure must be performed once the Opcenter Execution Discrete solution has been deployed and
the system is up and running.
In order to enable integration, you must associate the newly-imported Certificate with the required role (MPP for
integration with Teamcenter Manufacturing and APS for integration with Opcenter APS).
1. On the Production Machines, start a Windows command prompt as a user with the required role.
2. Browse to the %situnifiedsystemroot%bin folder.
3. Execute the Importcert.exe program passing the required parameters as shown in the following examples:

importcert.exe /thumbprint:526256e0ede349bb2817800c3c8834f6aeaa954a /roles:MPP /
forcerestart
importcert.exe /thumbprint:f7b2dfe611e7522e5d64f9ba2395cbbd4573bc18 /roles:APS /
plantids:Plant001, Plant002, Plant005
importcert.exe /thumbprint:f7b2dfe611e7522e5d64f9ba2395cbbd4573bc18 /roles:MPP /
applytoallplants

Parameter

Description

/thumbprint

The thumbprint associated to the installed certificate.
Do not use the thumbprint provided in the example above. To
retrieve the correct thumbprint, if not already known:
1. Access Control Panel > Administrative Tools > Manage
computer certificates.
2. In the Certificates tree, select Personal > Certificates.
3. Double-click the installed Certificate.
4. In the Certificate window, select the Details tab.
5. Copy the Thumbprint parameter.
6. Paste the thumbprint in the importcert.exe command prompt,
removing any spaces or "?" characters that may have been added
automatically.

/roles

• MPP for integration with Teamcenter Manufacturing
• APS for integration with Opcenter APS.

/plantids

List of plants (comma separated) defined in Solution Studio. If no
plant is specified, the default plant is automatically assigned. This is
applicable only in case of Multiplant.

/applytoallplants

Flag that identifies whether the roles are to be applied to all the
defined plants or not. If set, the list of plants previously specified is
not taken into account. This is applicable only in case of Multiplant.

#### Importing Windows Active Directory Groups in UMC

Importing user groups and their associated users from Windows via the UMC Web User Interface can take a
considerable amount of time and may return zero results if administration limits are exceeded. We
strongly suggest that you perform restricted searches.
To import Active Directory groups in UMC via the UMC Web User Interface:
1. Open a supported browser.
2. Depending on your configuration, enter the address http://<ProductionMachineName>/UMC or https://
<ProductionMachineName>/UMC.
3. Open the  Groups page and click Import Groups.
4. In the Import Domain Groups dialog box, insert the search criteria and click Search.
5. Select the user group you want to import and click Add.

6. Click Import to import the selected Windows group and its associated users into the UMC database.
Additional Details
• Only direct members are imported into UMC.
• For imported users, user authentication is performed against the Windows system.
• Many imported fields cannot be modified. Group members cannot be modified and users cannot be
added/deleted to/from the group. As a consequence, users imported via Windows group cannot be
deleted.

### Integrating Opcenter Execution Foundation Apps in the Opcenter Execution Discrete Solution

In order to work properly, some functionalities provided by Opcenter EX DS require that you integrate dedicated
Opcenter Execution Foundation Apps into your Opcenter Execution Discrete Solution. These Apps concern:
• label printing
• data segregation.
The Post-Setup automatically installs a set of Opcenter Execution Foundation Apps and Extension Apps in
your Opcenter Execution Discrete Solution. For details, see Apps and Extension Apps included in the Discrete
Solution in the Opcenter Execution Discrete User Manual.
The related UI modules that are directly used by Opcenter EX DS are automatically added to the Opcenter
Execution Discrete UI Application.
If you need to integrate your system with the Automation Layer to acquire values related to Tool usage,
Material assembly and Data Collections from the field, you need to also configure your system in order to
manage Automation Nodes and connect the machines of your plant to the Automation layer. For more
information, refer to sections How to Manage Automation Nodes and How to Configure the Association
between Equipment and Automation Gateway of the Opcenter Execution Foundation User Manual.

Prerequisites
• Upon Opcenter Execution Foundation installation, you have selected the Foundation Apps check-box.
• If you intend to use the Label App, verify that the prerequisites for using the Label App have been installed as
well (Microsoft .NET Core Windows Hosting Bundle version 2.0.7).
Hybrid Scenarios and the Label App
If you have executed the post-setups for both Opcenter Execution Discrete and Opcenter Execution
Process Hybrid, you must skip installing the Label App cited at step 2 in the procedure below, as it has
already been installed by default. Then proceed with the remainder of the procedure as described.

Procedure
1. In the Solution Studio home page, click App Management on the sidebar.
2. In the Available tab, select the App to be installed according to your needs and click Install. This App will be
listed in the Installed tab.

Integrate Opcenter
EX FN App...

If you want to....

Label

Print labels containing barcodes, text or images for particular entities used
in Opcenter EX DS.

DataSegregation

Use Data Segregation tags in Opcenter EX DS.

3. In the User Interface > UI Applications page, click Add to create a new UI Application that will contain the
related UI module.
4. Provide a Name and a Title for the UI Application and select the Deployable checkbox.
5. In the UI Applications page, click the arrow icon
3.

within the tile of the UI Application created at steps 2 and

In alternative to steps 3-4, you can also associate the UI Module to the existing Opcenter Execution
Discrete default UI Applications.
6. Click
Associate UI Modules with UI Application.
7. In the Associate UI Modules page, associate the UI Module according to the integrated App, as follows:
App

UI Modules

Label

LabelManagement

DataSegregation

DataSegregationTagManagement

8. Click Associate and then click Save.
9. (optional) Repeat steps 2 through 8, should you want to install another Opcenter Execution Foundation App that
is not provided by default.
10. Stop the runtime host, if it is already running.
11. (Required for Data Segregation) Enable the following post-actions present in the AppU4DM app:

26

Command

Post-Action

CreateNonConformanceV3_1

InheritSegregationTagsFromWOOnCreateNonConform
ance

CreateWorkOrderFromProcess

InheritSegregationTagsFromBOPOnCreateWorkOrderF
romProcess

CreateWorkOrderHeader

InheritSegregationTagsFromBOPOnCreateWorkOrderH
eader

ReleaseWorkOrder

InheritSegregationTagsFromWorkOrderOnReleaseWor
kOrder

Command

Post-Action

ScrapWorkOrderQuantity

InheritSegregationTagsFromWOOnScrapWorkOrderQu
antity

ScrapWorkOrderSerialNumbers

InheritSegregationTagsFromWOOnScrapWorkOrderSer
ialNumbers

TCM2CompleteAsPlannedBOP

InheritSegregationTagsFromFinalMaterialOnTCM2Com
pleteAsPlannedBOP

UADMAcceptChangePackage

InheritSegregationTagsFromWorkOrderOnUADMAccep
tChangePackage

SentenceNonConformanceV3_1

InheritSegregationTagsFromBOPReworkOnSentenceN
onConformanceV3_1

CreateToBeUsedDocuments

InheritSegregationTagsFromWOOnCreateToBeUsedDo
cuments

12. (Required for Data Segregation) Add the subscription to the following event present in the AppU4DM:
Event: OnReleaseWorkOrder EventHandler: InheritSegregationTagsFromWOOnReleaseWorkOrder
13. In the Package Management page, click
14. In the Host Management page, click

Build to build the packages.
Deploy to deploy your Solution.

### Importing Signal Rules

If you want to have the system automatically react and send notifications in specific situations (via the Signals
App), you also need to import the pre-configured Signal Rules provided by Opcenter EX DS as described below.

Procedure
1. In the Opcenter Execution Discrete home page, select the Signal Rule Management tile and click
Import
Signal Rule.
2. Browse the installation folder %SITUnifiedSystemRoot%VApps\UADM\Signals and select the following Signal
Rules, according to your needs:
• OnBufferSpecificContentThresholdValueSignalRule, to facilitate the automatic creation of Logistic
Requests by the system if the Buffer level goes below the defined threshold for a particular Material or
Tool.
• OnTransmitEquipmentSetPointSignalRule, to transfer Setpoint variables to Machines, when a Work
Order Operation involving that Machine is started.
• OnTransmitToolSetPointSignalRule, to transfer Setpoint variables to Tools, when a Work Order
Operation involving that Tool is started.
• StartingUsingScrewingToolSignalRule, to start using Screwing Tools, when a Work Order Operation of
type Screwing involving that Tool is ready to be executed. It activates when the communication between
the system and the Automation Gateway is successful.

• UseScrewingToolSignalRule, to record values received from the Screwing Tool, when a Work Order
Operation of type Screwing involving that Tool is started, thus providing History records and operation
results.
• CompleteScrewingWOOpOnToolDeactivationSignalRule, to deactivate the Screwing Tool, when a
Work Order Operation of type Screwing involving that Tool is completed with related result.
• GetContainmentRequests, to enable import of Containment Requests from Opcenter Intelligence
Traceability Application.
• GetContainmentReleases, to enable import of Containment Request Releases from Opcenter
Intelligence Traceability Application.
3. If the Signal Rule is already imported, select the Overwrite existing rules check box.
4. Click Save.
5. Select the Signal Rule and click

Approve.

6. Select the Signal Rule and click

Deploy.

Once the Signal Rule is deployed, SignalRulesEngineer and SignalRulesViewer roles are displayed in the
Roles tab in the side bar.

### Using Opcenter Execution Discrete in Multilanguage

Opcenter Execution Discrete User Interface is displayed by default only in English, but you can:
• download and use localized packages from the Download > Additional Downloads area of the Support Center.
• create localization packages for any additional language.
Opcenter EX DS relies on Opcenter Execution Foundation for multilanguage functionalities. Refer to the section
How to Use Opcenter Execution Foundation in Multilanguage of the Opcenter Execution Foundation Development and
Configuration Guide for further info.

### How to Configure Runtime Screens

The default layout of runtime screens, such as the Operator Landing (legacy) and the High Automation Landing
pages (legacy), can be changed in order to better suit runtime needs.
For example, you can decide to filter out runtime tasks according to their statuses, or you can decide to display the
contextual command bar according to the Task type.
You can even decide to show/hide buttons from the command bar, regardless of their type (that is, be they standard
or custom buttons).
You can decide to display runtime tasks also in the High Automation Landing page (legacy), where they are not
available by default, since less interaction from Operators is expected to take place.
There also exists the possibility of determining which Header Bar fields are to be visible in the High Automation
Landing page (legacy), as well as in the Operator Landing details page (legacy).
You can set the percentage of the overall screen's width that will be occupied by the Document Preview inside the
High Automation Landing page (legacy).
You can decide to change the default behavior of the High Automation Landing page (legacy), by managing only
the visibility of the components or changing also their size and position.
For Low Code UI Apps, you can decide to customize the display of screens such as the As Built or Genealogy, as well
as the Operator Terminal's content.

Available Operations
• Enabling the Display of Runtime Tasks according to Task Statuses
• Enabling the Display of the Contextual Command Bar according to Task types
• Displaying/Hiding Standard and Custom buttons
• Customizing the Display of Header Bar fields in the Operator Landing Details page
• Displaying runtime tasks in the High Automation Landing Page
• Cloning Runtime screens
• Disabling the Configuration of Size and Positioning in the High Automation Landing Page
• Setting the Percentage of the Width Occupied by the Document Preview in the High Automation Landing Page
• Customizing the Display of Header Bar fields in the High Automation Details page
• Customizing the display of the As Built and Genealogy pages in Low Code UI Apps
• Customizing the Display of the Operator Terminal's Content in Low Code UI Apps
• Customizing the Display of the Manufacturing Operator Terminal's Content in Low Code UI Apps
• Customizing the Display of the 3D Viewer in Low Code UI Apps

Enabling the Display of Runtime Tasks according to Task Statuses
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the operatorLanding > Operator Task List UI Module.
3. Select the TaskContainer and click configuration.
4. To customize the component's visibility, type the name of the Task status to be filtered out.
Available Task statuses
are: InProgress, Error, Paused, Ready, Suspended, NotReady, Created, Failed, Aborted, Canceled, Skipped,
Completed.
In the example below, all Tasks in status Failed, Completed, Aborted, Canceled or Skipped will not be
displayed in the Operator Task Details page.
{
"HiddenTaskStatusNId": [
"Failed",
"Completed",
"Aborted",
"Canceled",
"Skipped"
]
}

5. Click Apply.
6. Click
.
7. Build and deploy your solution.

Enabling the Display of the Contextual Command Bar according to Task types
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the operatorLanding > Operator Task List UI Module.
3. Select the TaskContainer and click configuration.
4. To customize the Contextual Command Bar visibility, provide one of the following values for Visibility: Always,
Never, KnownTypes. If you want to filter according to KnownTypes, you can also the value of the Task type to
be considered.
Available Tasks
are: UADMMaterialConsumptionTask, UADMToolUsageTask, UADMWorkInstructionTask, UADMQualityInsp

ectionTask, UADMPrintJobFilesTask, UADMPartProgramTask.
In the example below, the Contextual Command Bar will not be displayed for all tasks.
{
"ContextualCommandBar": {
"Visibility": "KnownTypes",
"KnownTypes": [
"UADMMaterialConsumptionTask",
"UADMToolUsageTask",
"UADMWorkInstructionTask",
"UADMQualityInspectionTask",
"UADMPrintJobFilesTask",
"UADMPartProgramTask"
]
}
}

5. To automatically display the Task Container in the screens Operator Task List and Operator Detail Steps,
provide the OpenDocPreviewOnLoad property set to true:
{
"OpenDocPreviewOnLoad" : true
}

6. Click Apply.
7. Click
.
8. Build and deploy your solution.

Displaying/Hiding Standard and Custom buttons
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the highAutomationOpLanding > operatorDetails UI Module.
3. Select the CustomizableButtonBar UI Component and click configuration.
4. To customize the behavior of each button, update the value of the tags of interest, as follows:
• To hide a button, set visibility to "false".
The following buttons are available by default:
• in the U4DM , DS and OnePieceFlowsolutions: Start, Pause, Complete, AddDocument, Defects,
ChangeNonConformance, RequestMaterial, Notes, JoinTeam, LeaveTeam, ChangeMachine.
• in the DS4AM solution: Start, Pause, Complete, AddDocument, Defects,
ChangeNonConformance, ChangeMachine.
• To disable a button, set disabled to "false".
• To change the icon of the button, provide the path to the new icon.
• To change the alignment of the button, set align to "right".
• To add a custom button, copy the code provided for a standard button (for example, see the code
relative to the Start button in the box below) and change the values accordingly. Make sure that the
required business logic is also available and linked to the button while configuring the wiring.
{
"type": "Command",
"name": "Start",

"unauthorizedBehavior": "hide",
"label": "sit.u4dm.start",
"svgIcon": "common/icons/cmdStart24.svg",
"visibility": true,
"disabled": true,
"align": "left"
}

5. Click Apply
6. Click
.
7. Build and deploy your solution.
You can also customize the CustomizableButtonBar UI Component contained in the operatorLanding UI
Screen in the same manner.

Customizing the Display of Header Bar fields in the Operator Landing Details page
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the operatorLanding > Operator Task List UI Module.
3. Select the HeaderBar UI component and click configuration.
4. Depending on whether you want to customize the display of Header Bar fields for Work Order Operations or for
Execution Groups, go to section OperationHeaderBarFields or section ExecutionGroupHeaderBarFields,
respectively, and set property visible to either True or False for each Header Bar field that is listed to determine
whether it will be displayed or not in the Header Bar of the Operator Landing Details page.
5. Click Apply.
6. Click
.
7. Build and deploy your solution.

Displaying Runtime Tasks in the High Automation Landing Page
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the highAutomationOpLanding > operatorLanding UI Module.
3. Select the HighAutomationEquipmentList component.
4. In the redirectToScreen field, type operatorDetailsTask.
5. Click

.

6. Click
to generate the selected mashup UI module.
7. Build and deploy your solution.

Cloning Runtime Screens
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Select the operatorLanding UI Module and click
.
3. In the Copy Mashup UI Module panel, provide a new name (for example operatorLanding_XXX), title and icon
for the new module and click Save.
4. Open the newly created UI Module.
5. Open the operatorLanding UI screen and switch to the Wiring tab.
6. From the Wire List, select goToDetails, then select Output Components and maximize the panel to view the
code of the component.
7. Change the value of result in order to point to the newly created UI Module. For example:

function(input) {
var result = [];
var evtObj = input[0];
if (evtObj["isPoc"]) {
vm.isPoc = true;
}
else {
vm.isPoc = false;
}
if (vm.isPoc) {
result = ["home.U4DM_operatorLanding_XXX_operatorDetailsTask"]
;
} else {
result = ["home.U4DM_operatorLanding_XXX_operatorDetailsTask"]
;
}
return result;

8. Click OK and then Apply.
9. Click
.
10. Repeat steps 6-9 for goToDetailsClicked, goToDetailsSteps and goToDetailsStepsClicked.
11. Open the operatorDetailsTask and operatorDetailsStep UI screens and repeat steps 6-9 for goToLanding and
goToLandingPage. For these UI Screens, the value for result should be changed as follows:
function(input) {
var evtObj = input[0];
var result = [];
result.push("home.U4DM_operatorLanding_XXX_operatorLanding");
return result;
}

12. Build and deploy your solution.

Disabling the Configuration of Size and Positioning in the High Automation
Landing Page
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the highAutomationOpLanding > operatorLandingDetails or operatorDetailsTask UI screen.
3. Select the siemensSimaticitU4dmAppu4dmZerotouchcomponent UI component.
4. In the ConfigurationMode property, set one of the following values:
• Default (or empty), to apply the default behavior of the High Automation Landing page
• Visibility, to only manage the visibility of the components without impacting their size and position.
• Disabled, to neither manage the visibility nor the size and position of the components.
5. Click
.
6. Build and deploy your solution.

Setting the Percentage of the Width Occupied by the Document Preview in the
High Automation Landing Page
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.

2. Open the highAutomationOpLanding > operatorDetailsTask UI Module.
3. Select the TaskContainer UI Component and click configuration.
4. In property DocumentPreWidth, set the percentage of the width occupied by the Document Preview in which
the Document will be displayed in the High Automation Landing page. The default value (which coincides with
the minimum allowed value) for this property is 30 and the maximum allowed value is 60.
5. Click Apply.
6. Click
.
7. Build and deploy your solution.

Customizing the Display of Header Bar fields in the High Automation Details page
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the highAutomationOpLanding > operatorDetailsTask UI Module.
3. Select the HighAutomationHeaderBar UI component.
4. Go to section HeaderBarFields and set property visible to either True or False for each Header Bar field that is
listed to determine whether it will be displayed or not in the Header Bar of the High Automation Details page.
5. Click Apply.
6. Click
.
7. Build and deploy your solution.

Customizing the display of the As Built and Genealogy pages in Low Code UI Apps
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Low Code UI
Applications.
2. Select the Complex Manufacturing or Repetitive Manufacturing Low Code UI Application.
3. Click
Edit Low Code UI Application Constants.
4. For the As Built page, select the AsBuilt_OpenInNewTab constant and change its value to True if you want to
display the As Built page in a new tab in the browser. By default, the constant is set to False, and the As Built
page is displayed within the Operator Terminal working area.
5. Select the DefaultUIAppName constant and change its value with the name of the UI Application that will be
opened by default (for example Siemens_SIT_UADM).
6. For the Genealogy page, select the Genealogy_OpenInNewTab constant and change its value to True if you
want to display the Genealogy page in a new tab in the browser. By default, the constant is set to False, and the
Genealogy page is displayed within the Operator Terminal working area.
7. Click
.
8. Build and deploy your solution.

Customizing the display of the As Built and Genealogy pages in Opcenter EX DS
Manufacturing
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Low Code UI
Applications.
2. Select the Manufacturing Low Code UI Application.
3. Click
Edit Low Code UI Application Constants.
4. For the As Built page, select the AsBuilt_OpenInNewTab constant under OpcenterEXDS_OperatorLanding
Module and change its value to True if you want to display the As Built page in a new tab in the browser for
operations of Serialized, FlexibleSerialized, or FullQuantity Work Order types. By default, the constant is set
to False, and the As Built page is displayed within the Operator Terminal working area.
5. For the As Built page, select the AsBuilt_OpenInNewTab constant under
OpcenterEXDS_RPT_OperatorLanding Module and change its value to True if you want to display the As Built
page in a new tab in the browser for operations of TransferBatch or FlexibleBatch Work Order types. By

default, the constant is set to False, and the As Built page is displayed within the Operator Terminal working
area.
6. Select the DefaultUIAppName constant under OpcenterEXDS_OperatorLanding Module and change its value
with the name of the UI Application that will be opened by default (for example Siemens_SIT_UADM).
7. Select the DefaultUIAppName constant under OpcenterEXDS_RPT_OperatorLanding Module and change its
value with the name of the UI Application that will be opened by default (for example Siemens_SIT_UADM).
8. For the Genealogy page, select the Genealogy_OpenInNewTab constant
under OpcenterEXDS_OperatorLanding Module and change its value to True if you want to display the
Genealogy page in a new tab in the browser. By default, the constant is set to False, and the Genealogy page is
displayed within the Operator Terminal working area.
9. For the Genealogy page, select the Genealogy_OpenInNewTab constant
under OpcenterEXDS_RPT_OperatorLanding Module and change its value to True if you want to display the
Genealogy page in a new tab in the browser. By default, the constant is set to False, and the Genealogy page is
displayed within the Operator Terminal working area.
10. Click
.
11. Build and deploy your solution.

Customizing the Display of the Operator Terminal's Content in Low Code UI Apps
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Low Code UI
Applications.
2. Select the Complex Manufacturing or Repetitive Manufacturing Low Code UI Application.
3. Click
Edit Low Code UI Application Constants.
4. Select the ShowFullScreenContentByDefault constant and change its value to True if you want to display only
the center part, while the Operation /Step List and the Document Viewer are collapsed. By default (False), the
Operator Terminal shown the Operation /Step List, the center area and all the additional specifications content
(for example, the Documents Viewer).
In any case, you can change the display mode also at runtime by using the standard expand/collapse toggle
mechanism.
5. Select the CollapseWorkOrderOperationListByDefault constant and change its value to True if you want to
display only the center part and the Document Viewer, while the Operation /Step List is collapsed. By default
(False), the Operator Terminal shown the Operation /Step List, the center area and all the additional
specifications content (for example, the Documents Viewer).
In any case, you can change the display mode also at runtime by using the standard expand/collapse toggle
mechanism.
6. Click
.
7. Build and deploy your solution.

Customizing the Display of the Manufacturing Operator Terminal's Content in Low
Code UI Apps
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Low Code UI
Applications.
2. Select the Manufacturing Low Code UI Application.
3. Click
Edit Low Code UI Application Constants.
4. Select the ShowFullScreenContentByDefault constant under OpcenterEXDS_OperatorLanding Module and
change its value to True if you want to display only the center part, while the Operation /Step List and the
Document Viewer are collapsed. By default (False), the Operator Terminal shown the Operation /Step List, the
center area and all the additional specifications content (for example, the Documents Viewer). The Operation/
Step List will show only operations of the Serialized, FlexibleSerialized, or FullQuantity Work Order types.
In any case, you can change the display mode also at runtime by using the standard expand/collapse toggle
mechanism.

5. Select the ShowFullScreenContentByDefault constant under OpcenterEXDS_RPT_OperatorLanding Module
and change its value to True if you want to display only the center part, while the Operation /Step List and the
Document Viewer are collapsed. By default (False), the Operator Terminal shown the Operation /Step List, the
center area and all the additional specifications content (for example, the Documents Viewer). The Operation/
Step List will show only operations of the TransferBatch or FlexibleBatch Work Order types.
In any case, you can change the display mode also at runtime by using the standard expand/collapse toggle
mechanism.
6. Select the CollapseWorkOrderOperationListByDefault constant under OpcenterEXDS_OperatorLanding
Module and change its value to True if you want to display only the center part and the Document Viewer, while
the Operation /Step List is collapsed. By default (False), the Operator Terminal shown the Operation /Step List,
the center area and all the additional specifications content (for example, the Documents Viewer). The
Operation/Step List will show only operations of the Serialized, FlexibleSerialized or FullQuantity Work Order
types.
In any case, you can change the display mode also at runtime by using the standard expand/collapse toggle
mechanism.
7. Select the CollapseWorkOrderOperationListByDefault constant under
OpcenterEXDS_RPT_OperatorLanding Module and change its value to True if you want to display only the
center part and the Document Viewer, while the Operation /Step List is collapsed. By default (False), the
Operator Terminal shown the Operation /Step List, the center area and all the additional specifications content
(for example, the Documents Viewer). The Operation/Step List will show only operations of the TransferBatch
or FlexibleBatch Work Order types.
In any case, you can change the display mode also at runtime by using the standard expand/collapse toggle
mechanism.
8. Click
.
9. Build and deploy your solution.

Customizing the Display of the 3D Viewer in Low Code UI Apps
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Low Code UI
Applications.
2. Select any Low Code UI Application that needs to display a 3D file in the Document Viewer (Complex
Manufacturing or Repetitive Manufacturing or Manufacturing or Quality Execution).
3. Click Edit Low Code UI Application Constants.
4. Select LicenseToken and enter the license needed to view the new 3D viewer (If the application to which you
added the LicenseToken is already running, the token will not be recognized until you restart the application).
5. Select the Show3DViewerButton property in the EXFN_Quality section (Default value = false) set its value to
True if you want to display the Quality Inspection buttons to interact with the 3D viewer.
6. Select the Show3DViewerButton_MaterialConsumption property in the OperatorLanding section (Default
value = false) set its value to True if you want to display the To Be Consumed Material buttons to interact with
the 3D viewer.
7. Click Save.
8. Build and deploy your solution.

### Configuring Cleaning Rules

To maintain the stability of the system's level of performance over time and limit storage usage to a minimum, it is
recommended that only data required for production be maintained in the on-line Opcenter Execution Discrete
database, whereas any "consumable data" should be wiped from it.
The Data Cleaning functionality provided by Opcenter Execution Foundation uses appropriately-configured
Cleaning Rules to eliminate all entities no longer required for production from the on-line database.

In particular, data regarding certain runtime entities should be cleaned from the on-line Opcenter Execution
Discrete DB, as soon as those entities are no longer needed according to project requirements. In detail, this is
applicable to:
• Work Orders
• Material Tracking Units
• Tools
• Execution Groups.
To mark as to be cleaned Work Orders that are no longer needed, a dedicated button is available in the Work
Orders page. To mark as to be cleaned all other entities, public APIs can be invoked.
The same settings are automatically propagated by Opcenter EX FN to any child entities (in composition) and any
facets of the entities directly managed by Opcenter EX DS.
For more information and operative instructions regarding maintenance configuration, refer to How to Configure
Maintenance under section How to Manage a Manufacturing Solution in Solution Studio in the Opcenter Execution
Foundation Development and Configuration Guide.

Procedure
To enable Data Cleaning for the physical elimination of runtime data from the on-line Opcenter EX DS database:
1. Access Solution Studio and, operating from the home page, click the card with your solution.
2. Click Maintenance in the sidebar and then select Configuration.
3. In the Maintenance Configuration page, click the Rules tab.
4. In the Cleaning Rule panel, click
Create New to open the Create New Cleaning Rule pane, where you
must expand all the available panels and enter the required configuration.
5. Expand the Entities panel and select the required entity types, optionally filtering by functional block and entity
name.
Functional Block
CHR_OP

36

Entities
• RuntimeCharacteristicRepresentation
• RuntimeCharacteristicRepresentationContainer
• InspectionAcquisitionContext
• InspectionSample
• InspectionValue
• VisualDetectedFailure

MAT_OP

MaterialTrackingUnit

OP_Container

ContainerHstory

OP_ContainerExec

ContainerPartialQuantityAssociation

OP_ITLK

• ItlkCheckWOOpAssociation
• ItlkCheckWOStepAssociation
• ItlkCheckHistory

OP_Result

• Result
• ResultHistory

Functional Block
OP_Runtime

Entities
• ActualCollectedDocument
• ActualConsumedMaterial
• ActualCoProducedMaterial
• ActualProducedMaterial
• ActualUsedInspection
• ActualUsedMachine
• ActualUsedMachinePJF
• ActiveUserOnMachine
• ActualUsedTool
• Defect
• ExecutionGroup
• ExecutionGroupPhase
• ExecutionGroupPhaseWOOAssociation
• ExecutionGroupPhaseDependency
• NonConformance
• NonConformanceAttachment
• NonConformanceItem
• NonConformanceHistory
• NonConformanceResource
• ProducedMaterialItem
• ProducedMaterialUnderRework
• RuntimeCharReprRefOperationAssociation
• ToBeConsumedMaterial
• ToBeConsumedMaterialPrekit
• ToBeConsumedMaterialPrekitHistory
• ToBeCoProducedMaterial
• ToBeProducedMaterial
• ToBeUsedDocument
• ToBeUsedMachine
• ToBeUsedSetPointItemATNInstanceAssociation
• Tool
• ToBeUsedTool
• ToolHistory
• ToBeUsedInspection
• UserWorkOrderOperationAssociation
• WIDefinitionToEGPhaseAssociation
• WorkInstructionToExecutionGroupPhaseAssociatio
n
• WorkInstructionToWorkOrderOperationAssociation
• WorkInstructionToWorkOrderStepAssociation
• WIDefinitionToWOOperationAssociation
• WIDefinitionToWOStepAssociation
• WorkOrder
• WorkOrderOperation
• WorkOrderOperationSkill
• WorkOrderStepSkill
• WorkOOperationDependency
• WOOpDependencyNavigation
• WOOpDependencyNavigationMTUAssociation
• WorkOrderStep

Functional Block

Entities
• WorkOStepDependency
• WorkOrderHistory
• WorkOrderHistoryMaterialItem
• WorkOrderHumanResource

TSK_OP

• Task
• TaskContext

WI_OP

WorkInstruction

6. Expand the Cleaning Conditions panel and select the All_ToBeCleaned_Entities cleaning condition to apply to
the entity instances.
Keep in mind that, all the already deleted entities related to the Work Order marked as to be cleaned,
must be purged from the database as well. This is possible using the cleaning condition Is Logically
Deleted, which corresponds to IsDeleted equal to true. For details, see Configuring Maintenance
Cleaning Conditions in the Opcenter Execution Foundation Development and Configuration Guide. This is
applicable for the following entities in the BPF_OP Functional Block:
• WorkProcess
• WorkProcessContext
7. Expand the Schedules panel and select the schedule to apply to the entity instances.
8. Save changes.
9. Click

, to enable the configuration.

Additional cleaning rules can be configured, depending on the project's requirements and the period of
data retention on the on-line DB required by the customer processes.
The other settings of the Maintenance Configuration (such as archiving frequency or cleaning frequency)
must be configured according to customer requirements.

### Deploying the Opcenter Execution Discrete Solution

To build a deployment package and deploy it on the host:
1. From Windows Apps, in the Opcenter Execution Foundation category, click the Solution Studio link.
2. In the web page, log in to the Opcenter EX FN Solution Studio in either of the following ways:
• Insert the credentials of the user with administrator rights and click Sign In.
• Click Use your current Windows session to Log In link to access the application with the current user
credentials.
3. In the home page, click the link to your solution.
4. In the Deployment > Package Management page, click
Build. All sub-packages will be updated.
5. (Optional, only if you are using Open Protocol Tools) If the Open Protocol Service asset is installed on the host
where you are working, stop the service before performing any modification.
6. In the Host Management page, stop the host if it is started and click
package to the selected host.

Deploy to deploy the current Solution

7. Click
Update Database, to update the database.
8. If you have an Oracle database, log into its management console with a user with administrative rights and
execute the script U4DM_MS_Post_Equipment_MigrationOracle.sql found in the %ProgramData%

\Siemens\SimaticIT\Unified\Deploy\Migration\MasterData\Oracle\Post folder.
This script must not be executed when updating from a previous version.
9. (If you have updated the configuration of your solution) Depending on the database type, execute the scripts
available in the %ProgramData%
\Siemens\SimaticIT\Unified\Deploy\Migration\OperationalData\SqlServer\Post or %ProgramData%
\Siemens\SimaticIT\Unified\Deploy\Migration\OperationalData\Oracle\Post folders.
10. Click
Start to start the selected host.
11. (If you have created the DS4AM solution) Launch Siemens.OpcenterEX.AM.AM_Configuration.exe (from
%SITUnifiedVAppsRoot%\EXAM), insert the credentials of the user administrator rights, select Run database
initialization from the drop down and then click Execute.
If the Deploy has been executed during a migration and the version from which you are migrating contains
customizations regarding Order status changes upon Start/Complete of a Work Order Operation, verify
whether these customizations continue to function as expected.

Performance Issues
If you experience performance issues (for example, when accessing the runtime application), you can increase
performance by minifying the resources of the deployed solution.
For more information, see section How to Configure Solution Studio Settings in the Opcenter Execution Foundation
Development and Configuration Guide.

### Deploying Low Code UI Apps

Solution Studio includes an environment that allows you to configure Low Code UI Applications powered by
Mendix, based on a Deployment Package (.mda), to fulfill specific manufacturing needs.
Keep in mind that all prerequisites listed in page Prerequisites for Opcenter Execution Foundation Host of the
Opcenter Execution Foundation Installation Guide must be satisfied, in particular those illustrated in section
Requirements for deploying and running Low Code UI Applications powered by Mendix.

Available Low Code UI Apps
The Data Models used by the Low Code UI Apps are provided by dedicated Opcenter EX FN-based Reading Model
Apps, which must necessarily be installed. The sole exceptions are the Opcenter EX DS System and Opcenter EX DS
System Administrator apps.
In addition, all of the engineering Low Code UI Apps use the references of Opcenter Execution Foundation and
Opcenter Execution Discrete Apps.

Low Code UI App

Reading Model App

Type

Opcenter EX Apps/
Solution

Opcenter EX DS Product Engineer

RMEXDSProdEng

Engineering

• AppU4DM
• Application Log
• Barcode
• BoP
• Defect
• Document
• Equipment
• Label
• Material
• Personnel
• Reference
• System
• Work Instruction

Opcenter EX DS System

None

Engineering

Reference

Opcenter EX DS System
Administrator

None

Engineering

• Application Log
• Barcode
• Defect
• Document
• Equipment
• Label
• Material
• Personnel
• Reference
• System
• Work Instruction

Opcenter EX DS Production
Coordinator

RMEXDSProdCoord

Runtime

• AppU4DM
• Application Log
• Barcode
• Defect
• Document
• Equipment
• Label
• Material
• Personnel
• Reference
• System
• Work Instruction

Opcenter Execution Discrete One
Piece Flow

OTReadingModel

Runtime

• OnePieceFlow
• U4DM

Low Code UI App

Reading Model App

Type

Opcenter EX Apps/
Solution

Opcenter Execution Discrete
Complex Manufacturing

RMComplexManuf

Runtime

• U4DM
• DS
• OnePieceFlow

Opcenter Execution Discrete
Repetitive Manufacturing

RMRepetitiveManuf

Runtime

• U4DM
• DS
• OnePieceFlow

Opcenter Execution Discrete
Manufacturing

RMManuf

Runtime

• U4DM
• DS
• OnePieceFlow

Opcenter Execution Discrete
Quality Execution

RMQualityExecution

Runtime

• U4DM
• DS
• OnePieceFlow

Opcenter Execution Discrete
Manufacturing Planner Preview

None

Runtime

None

The Opcenter EX Apps listed in the table above are available by default according to the solution that has
been selected when performing post-setup configurations.
If you remove any of these Apps or Extension Apps, you may encounter errors during the update of the
database. For example: if you remove the Reference App or the Defect App the corresponding database
table is not created and, therefore, the creation of the related views fails.

Prerequisites
The .mda package on which you want to base the Low Code UI App is available in folder
%SITUnifiedSystemData%\Engineering\Packages\MxApps. Remember to install the dedicated Opcenter EX
FN -based Reading Model Apps that you require.
Furthermore, you will need to download the server distribution, from Mendix Marketplace, that matches Mendix
Studio Pro version used to develop the Low Code UI App that you are going to deploy. Note that before
downloading it, you have to either log in or register at the following link https://signup.mendix.com/link/signup/?
utm_medium=partners&utm_source=Siemens&utm_id=11587399. The server distribution can be found under the
Related Downloads section for the specific Mendix Studio Pro version in the Mendix Marketplace (Opcenter
Execution Foundation supports 10.24.XYZ version).
The server distribution is a tar.gz file (mendix-10.24.0.73019.tar.gz) and you will have to copy it manually on the
folder %SITUnifiedSystemData%\Engineering\Mx of each host (both Engineering and Runtime) before deploying
the Low Code UI App.

Procedure

1. In Solution Studio, in the Low Code UI Applications page, add the Low Code UI App of interest. For more
details, see chapter Configuring Low Code UI Applications powered by Mendix of the Opcenter Execution
Foundation Development and Configuration Guide.
2. (Only for Opcenter Execution Discrete Manufacturing Planner Preview) perform the following operations in the
given order:
• From %SITUnifiedSystemRoot%bin folder, start the Command Prompt and then
execute SITUASolutionConf.exe -command listmxuiapplicationports. The system displays the ports
on which Low Code UI Apps are currently running. Copy the number of the Runtime Port relative to the
Opcenter Execution Discrete Manufacturing Planner Preview App.
• In Solution Studio open the Low Code UI Applications page, select the Opcenter Execution Discrete
Manufacturing Planner Preview App and then click the
Edit Low Code UI Application Constants
button.
• Paste the previously copied runtime port relative to the Opcenter Execution Discrete Manufacturing
Planner Preview App in the PreviewReadingModel edit box related to the
OpcenterEXDS_ManufacturingPlannerPreview module, in place of 8080.
3. In the case of the Opcenter EX DS Complex Manufacturing, Opcenter EX DS Repetitive Manufacturing
and Opcenter EX DS Manufacturing Apps, to view details regarding Work Order Operations that are in
Complete or NotExecuted status, edit the related Low Code UI Application Constants, to set
constant ShowCompleteAndNotExecutedOperations to True.
4. Assign User Roles defined in the .mda package to a Role. In this way, the Role can assume both Opcenter
Execution Discrete rights and all rights related to the User Roles defined in the .mda package.
5. In the Deployment > Package Management page, click
6. In the Host Management page click

Build. All sub-packages will be updated.

Deploy to deploy the current Solution package to the selected host.

7. If needed, click
Update Database, to update the database.
8. Important: Starting from version 2401, when not explicitly listed in the table below, the scripts for the internal
views of Low Code UI Apps are automatically launched when updating the database, depending on the Low
Code UI App you have installed.
On SQL Server Database, log into the Database Management Console as a user with administrative rights and
then, depending on the Low Code UI App concerned, go to folder
%SITUnifiedVAppsRoot%\UADM\ReadingModelViews\SQLServer and execute the following scripts
contained therein in the given order after selecting the Runtime Database:
Low Code UI App
Opcenter Execution Discrete One Piece Flow

42

SQL Scripts to be executed
• Opcenter_EXDS_OTReadingModel - Utility Drop RM Views.sql: deletes the external views
with prefix RM_ previously created. Before
running this script, if customizations were made
to these external views, see Note immediately
after this table.
• Opcenter_EXDS_OTReadingModel Internal.sql: creates internal views with prefix
RMI_.
• Opcenter_EXDS_OTReadingModel.sql:
creates external views with prefix RM_.

Low Code UI App

SQL Scripts to be executed

Opcenter Execution Discrete Complex
Manufacturing

• Opcenter_EXDS_RMComplexManuf - Utility Drop RM Views.sql: deletes the external views
with prefix RM_ previously created. Before
running this script, if customizations were made
to these external views, see Note immediately
after this table.
• Opcenter_EXDS_RMComplexManuf.sql:
creates external views with prefix RM_.

Opcenter Execution Discrete Repetitive
Manufacturing

• Opcenter_EXDS_RMRepetitiveManuf Utilities - Drop RM Views.sql: deletes
the external views with prefix RM_ previously
created. Before running this script, if
customizations were made to these external
views, see the Note below.
• Opcenter_EXDS_RMRepetitiveManuf.sql: cre
ates external views with prefix RM_.

Opcenter Execution Discrete Manufacturing

• Opcenter_EXDS_RMManuf - Utilities - Drop
RM Views.sql: deletes the external views with
prefix RM_ previously created. Before running
this script, if customizations were made to
these external views, see the Note below.
• Opcenter_EXDS_RMManuf.sql: creates
external views with prefix RM_.

Opcenter Execution Discrete Quality Execution

• Opcenter_EXDS_RMQualityExecution - Utility
- Drop RM Views.sql: deletes the external views
with prefix RM_ previously created. Before
running this script, if customizations were made
to these external views, see the Note below.
• Opcenter_EXDS_RMQualityExecution.sql: cre
ates external views with prefix RM_.

Opcenter EX DS Production Coordinator

• Opcenter_EXDS_RMProductionCoord - Utility
- Drop RM Views.sql: deletes the external views
with prefix RM_ previously created. Before
running this script, if customizations were made
to these external views, see the Note below.
• Opcenter_EXDS_RMProductionCoord.sql: cre
ates external views with prefix RM_.

Customizations previously made to Low Code UI Apps
If you made customizations to external RM_ views, running this scripts will require that you reimplement the customizations once again, after running the last script that creates the external views
again. Therefore, it is suggested that you make a backup of all customized views in order to be able to
re-apply the changes you made at a later time. If you prefer not to re-create the views, you can decide
not to run this script and manually upgrade the views with the additional fields provided in the new
version.

For a complete list of the modifications made to the external RM_ views, see section Updates for
Reading Model Views for the Low Code UI Appof interest in theOpcenter EX DS Low Code UI
Personalization Guide.
For any other type of customization (for example, new modules), see section How to migrate your
customized Low Code UI App of theOpcenter EX DS Low Code UI Personalization Guide.
9. (Optional) Repeat the previous step, to run the scripts also on the Archiving Database., if you have configured
Archiving as explained in section How to Configure Archiving of the Opcenter Execution Foundation Development
and Configuration Guide.
10. If needed, click
Start to start the selected host. When the host is started, the databases of the Low Code UI
Applications powered by Mendix are created.
11. (Not valid for Opcenter Execution Discrete Manufacturing Planner Preview App, which must be opened from
Teamcenter) At the end of the deploy process, perform a log-out. You can then access the Low Code UI App
through the required URL, following the procedures explained in page Accessing the UI Application/Low Code UI
Application of the Opcenter Execution Foundation Development and Configuration Guide.

### Indexing the System Databases

After deploying the Opcenter Execution Discrete solution, it is strongly recommended that you perform the indexing
of its databases. Two different sets of scripts must be executed, depending on the database type (SQL Server or
Oracle).
Keep in mind that the indexing operation may be very time-consuming, depending on the database
parameters (size, type, server memory and so on).

Procedure
1. Log into your database administration tool (for example, SQL Server Management Studio, in the case of an SQL
Server database) with a user who possesses the proper administrative rights.
2. On the Opcenter Execution Discrete database, do either of the following:
• in case of SQL Server Database, run the script provided in the SQL Server scripts section.
• in case of Oracle Database, follow the instructions provided in the Oracle Scripts section.

SQL Server scripts
CREATE NONCLUSTERED INDEX
[IDX_WorkProcessDMMater_1832483380_IsDel_Discr_WPNid_DmMtuNid] ON [dbo].
[WorkProcessDMMater_1832483380]
(
[IsDeleted] ASC,
[Discriminator] ASC,
[WorkOrderOperationNId] ASC,
[WorkOrderStepNId] ASC
)
INCLUDE (WorkProcessNId, DM_MaterialTrackingUnitNId)
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO

CREATE NONCLUSTERED INDEX [IDX_WorkProcess_Siemen_1784161351_IsDel_Discr_Status_Id]
ON [dbo].[WorkProcess_Siemen_1784161351]
(
[IsDeleted],
[Discriminator],
[StatusNId.Status]
)
INCLUDE ([Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [IDX_WorkOrderOperation_1431095118_Id_IsDel_Discr] ON
[dbo].[WorkOrderOperation_1431095118]
(
[Id] ASC,
[IsDeleted] ASC,
[Discriminator] ASC
)
INCLUDE([NId], [WorkOrder_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX
[IDX_WorkOrderOperation_1431095118_IsDel_Discr_Stat_WoId_NId] ON [dbo].
[WorkOrderOperation_1431095118]
(
[IsDeleted] ASC,
[Discriminator] ASC,
[StatusNId.Status] ASC,
[WorkOrder_Id] ASC
)
INCLUDE([NId])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX
[IDX_ProducedMaterialIte_247001443_DmMtu_IsDel_Disc_Id_WoId] ON [dbo].
[ProducedMaterialIte_247001443]
(
[DM_MaterialTrackingUnit] ASC,
[IsDeleted] ASC,
[Discriminator] ASC
)
INCLUDE ([Id],[WorkOrder_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]

GO
CREATE NONCLUSTERED INDEX IDX_ToBeProducedMaterial_29183906_IsDel_Discr_WoosId
ON [dbo].[ToBeProducedMaterial_29183906]
(
[IsDeleted] ASC,
[Discriminator] ASC,
[WorkOrderStep_Id] ASC
)
INCLUDE ([Id], [AId], [IsFrozen], [IsLocked], [EntityType], [CreatedOn],
[LastUpdatedOn], [OptimisticVersion], [ConcurrencyVersion], [ToBeCleaned],
[Quantity], [WorkOrderOperation_Id], [DM_MaterialTrackingUnit_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX
IDX_ToBeProducedMaterial_29183906_IsDel_Discr_WooId_Qty_DmMtu
ON [dbo].[ToBeProducedMaterial_29183906]
(
[IsDeleted] ASC,
[Discriminator] ASC,
[WorkOrderOperation_Id] ASC,
[Quantity] DESC,
[DM_MaterialTrackingUnit_Id] DESC
)
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX IDX_WorkOrderStep_Siem_1809795233_IsDelDiscr_WooId ON
[dbo].[WorkOrderStep_Siem_1809795233]
(
[IsDeleted],
[Discriminator],
[WorkOrderOperation_Id]
)
INCLUDE ([Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX
IDX_ActualProducedMate_2051014940_IsDel_Discr_WosId_CQty_DmMtuId ON [dbo].
[ActualProducedMate_2051014940]
(
[IsDeleted] ASC,
[Discriminator] ASC,
[WorkOrderStep_Id] ASC,
[CompletedQuantity] DESC

)
INCLUDE ([DM_MaterialTrackingUnit_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [IDX_TemporaryApplicationIdCE_SessionId_Id_EntityType_TBC]
ON [dbo].[__TemporaryToBeCleanedItemsCE]
(
[SessionId] ASC
)
INCLUDE ([Id],[EntityType],[ToBeCleaned])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [P
RIMARY]
GO
CREATE NONCLUSTERED INDEX IDX_WorkOrderOperation_1431095118_IsDel_Discr_WoId
ON [dbo].[WorkOrderOperation_1431095118]
(
[IsDeleted]ASC,
[Discriminator] ASC,
[WorkOrder_Id] ASC
)
INCLUDE ([StatusNId.Status],[Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX IDX_MaterialTrackingUni_494706508_IsDelDisCode_Id ON [dbo].
[MaterialTrackingUni_494706508]
(
[IsDeleted],
[Discriminator],
[Code]
)
INCLUDE (Id)
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX IDX_ToBeUsedMachine_Sie_107405297_IsDelMachine ON [dbo].
[ToBeUsedMachine_Sie_107405297]
(
[IsDeleted],
[Machine]
)

WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX
IDX_ToBeProducedMaterial_29183906_IsDel_WosId_Id_Qty_WooId_DmMtuId
ON [dbo].[ToBeProducedMaterial_29183906]
(
[IsDeleted] ASC,
[WorkOrderStep_Id] ASC
)
INCLUDE ([Id],[Quantity],[WorkOrderOperation_Id],[DM_MaterialTrackingUnit_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX
[IDX_DM_MaterialTrackin_1551871669_IsDel_Discr_DM_MaterialId]
ON [dbo].[DM_MaterialTrackin_1551871669]
(
[IsDeleted],
[Discriminator],
[DM_MaterialId]
)
INCLUDE ([MaterialTrackingUnit_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX
[IDX_ToBeConsumedMateri_2105885214_IsDel_MatSpecType_Id_Group_Qty_WOO_WOS] ON [dbo].
[ToBeConsumedMateri_2105885214]
(
[IsDeleted] ASC,
[MaterialSpecificationType] ASC
)
INCLUDE ([Id], [GroupId], [Quantity], [WorkOrderOperation_Id], [WorkOrderStep_Id] )
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO

CREATE NONCLUSTERED INDEX [IDX_ToBeUsedMachine_IsDelDiscrMachine_IdWooId] ON [dbo].
[ToBeUsedMachine_Sie_107405297]
(
[IsDeleted],
[Discriminator],
[Machine]
)

INCLUDE ([Id],[WorkOrderOperation_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [IDX_Result_IsDelDiscrWooNId] ON [dbo].
[Result_Siemens_Sim_1883522939]
(
[IsDeleted],
[Discriminator],
[WorkOrderOperationNId]
)
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [IDX_Result_IsDelDiscr_WooNIdMtuNIdEquipActNIdResTypeId] ON
[dbo].[Result_Siemens_Sim_1883522939]
(
[IsDeleted],
[Discriminator]
)
INCLUDE ([WorkOrderOperationNId],[MaterialTrackingUnitNId],[EquipmentNId],
[ActivityNId],[ResultType_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [IDX_P2OpLink_IsDelDiscrMPId_IdChildOpId] ON [dbo].
[ProcessToOperation_2065129030]
(
[IsDeleted],
[Discriminator],
[MasterPlan_Id]
)
INCLUDE ([Id],[ChildOperation_Id])
WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [IDX_P2OpLink_IsDelDiscr_IdChildOpId] ON [dbo].
[ProcessToOperation_2065129030]
(
[IsDeleted],
[Discriminator]
)
INCLUDE ([Id],[ChildOperation_Id])

WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, SORT_IN_TEMPDB = OFF,
DROP_EXISTING = OFF, ONLINE = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON,
FILLFACTOR = 80) ON [PRIMARY]
GO

Oracle scripts
Before executing the following scripts, substitute the following labels with the appropriate values for the database
server:
• __SCHEMA__ (example value for default installations: U4DM)
• __TABLE_SPACE__ (example value for default installations: SIT_U4DM)
• __NUMBER_OF_CPUs__ (number of cores of the database server)

CREATE INDEX "__SCHEMA__"."IDX_WorkProcessDMMater_1832483380_IsDel_Discr_WPNid_DmMtuN
id_WpNid_DmMtuNid" ON "__SCHEMA__"."WorkProcessDMMater_1832483380"
(
"IsDeleted" ASC,
"Discriminator" ASC,
"WorkOrderOperationNId" ASC,
"WorkOrderStepNId" ASC,
"WorkProcessNId" ASC,
"DM_MaterialTrackingUnitNId" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";
CREATE INDEX "__SCHEMA__"."IDX_WorkProcess_Siemen_1784161351_IsDel_Discr_Status_Id"
ON "__SCHEMA__"."WorkProcess_Siemen_1784161351"
(
"IsDeleted" ASC,
"Discriminator" ASC,
"StatusNId.Status" ASC,
"Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";
CREATE INDEX "__SCHEMA__"."IDX_WorkOrderOperation_1431095118_Id_IsDel_Discr" ON
"__SCHEMA__"."WorkOrderOperation_1431095118"
(
"Id" ASC,
"IsDeleted" ASC,
"Discriminator" ASC,
"NId" ASC,
"WorkOrder_Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";

CREATE INDEX "__SCHEMA__"."IDX_WorkOrderOperation_1431095118_IsDel_Discr_Stat_WoId_N
Id" ON "__SCHEMA__"."WorkOrderOperation_1431095118"
(
"IsDeleted" ASC,
"Discriminator" ASC,
"StatusNId.Status" ASC,
"WorkOrder_Id" ASC,
"NId" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";
CREATE INDEX "__SCHEMA__"."IDX_ProducedMaterialIte_247001443_DmMtu_IsDel_Disc_Id_WoI
d" ON "__SCHEMA__"."ProducedMaterialIte_247001443"
(
"DM_MaterialTrackingUnit" ASC,
"IsDeleted" ASC,
"Discriminator" ASC,
"Id" ASC,
"WorkOrder_Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";

CREATE INDEX "__SCHEMA__"."IDX_ToBeProducedMaterial_29183906_IsDel_Discr_WoosId"
ON "__SCHEMA__"."ToBeProducedMaterial_29183906"
(
"IsDeleted" ASC,
"Discriminator" ASC,
"WorkOrderStep_Id" ASC,
"Id" ASC,
"AId" ASC,
"IsFrozen" ASC,
"IsLocked" ASC,
"EntityType" ASC,
"CreatedOn" ASC,
"LastUpdatedOn" ASC,
"OptimisticVersion" ASC,
"ConcurrencyVersion" ASC,
"ToBeCleaned" ASC,
"Quantity" ASC,
"WorkOrderOperation_Id" ASC,
"DM_MaterialTrackingUnit_Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";
CREATE INDEX "__SCHEMA__"."IDX_ToBeProducedMaterial_29183906_IsDel_Discr_WooId_Qty_D
mMtu"
ON "__SCHEMA__"."ToBeProducedMaterial_29183906"
(
"IsDeleted" ASC,

"Discriminator" ASC,
"WorkOrderOperation_Id" ASC,
"Quantity" DESC,
"DM_MaterialTrackingUnit_Id" DESC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";
CREATE INDEX "__SCHEMA__"."IDX_WorkOrderStep_Siem_1809795233_IsDelDiscr_WooId" ON
"__SCHEMA__"."WorkOrderStep_Siem_1809795233"
(
"IsDeleted" ASC,
"Discriminator" ASC,
"WorkOrderOperation_Id" ASC,
"Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";

CREATE INDEX "__SCHEMA__"."IDX_ActualProducedMate_2051014940_IsDel_Discr_WosId_CQty_
DmMtuId" ON "__SCHEMA__"."ActualProducedMate_2051014940"
(
"IsDeleted" ASC,
"Discriminator" ASC,
"WorkOrderStep_Id" ASC,
"CompletedQuantity" DESC,
"DM_MaterialTrackingUnit_Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";
CREATE INDEX "__SCHEMA__"."IDX_MaterialTrackingUni_494706508_IsDelDisCode_Id" ON
"__SCHEMA__"."MaterialTrackingUni_494706508"
(
"IsDeleted" ASC,
"Discriminator" ASC,
"Code" ASC,
"Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";
CREATE INDEX "__SCHEMA__"."IDX_ToBeUsedMachine_Sie_107405297_IsDelMachine" ON
"__SCHEMA__"."ToBeUsedMachine_Sie_107405297"
(
"IsDeleted" ASC,
"Machine" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";

CREATE INDEX "__SCHEMA__"."IDX_ToBeProducedMaterial_29183906_IsDel_WosId_Id_Qty_WooId
_DmMtuId"
ON "__SCHEMA__"."ToBeProducedMaterial_29183906"
(
"IsDeleted" ASC,
"WorkOrderStep_Id" ASC,
"Id" ASC,
"Quantity" ASC,
"WorkOrderOperation_Id" ASC,
"DM_MaterialTrackingUnit_Id" ASC
)
PARALLEL __NUMBER_OF_CPUs__ NOLOGGING PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE
STATISTICS TABLESPACE "__TABLE_SPACE__";

### Configuring the Documentation Center

When installing and configuring Opcenter EX DS, you can configure the Documentation Center to access user
documentation from a web-based application. The Documentation Center must be populated by loading
documentation packages.
Once loaded, the documentation packages can be viewed from within the Documentation Center or managed
according to your needs.
You may have already configured the Documentation Center during the Opcenter Execution Foundation
Configuration. In this case, the data store is already available and all documents related to Opcenter
Execution Foundation are already loaded as well. The procedure below loads all documents again and
includes those related to Opcenter Execution Discrete.

Loading Documentation Packages into Documentation Center
1. From Windows Apps, in the Opcenter Execution Foundation category, click the Opcenter EX FN Configuration
link to launch the Opcenter Execution Foundation Configuration tool.
2. Click MANAGE on the Documentation Center card.
3. Click Load Packages to create the Documentation Data Store, if not already available, and install all documents
released with your version of Opcenter EX DS: wait until a green message is displayed at the bottom of the
Monitor area, notifying you that the operation has completed successfully.

Viewing Documentation from the Documentation Center
From Windows Apps, in the Opcenter Execution Foundation category, click the Documentation Center link to
launch the Opcenter EX FN Documentation Center.

Managing Documentation Packages
The Documentation Center Administrator Tool allows you to manage the documentation packages (for example,
to add only specific documents to the Documentation Center or to remove the previously-imported documents so
that only those addressed to a specific user type remain therein).
For more information, see section Configuring the Documentation Center of the Opcenter Execution Foundation
Installation Guide.

### Configuring the Production Resolution Common Component

The Production Resolution Common Component is able to solve complex data structures and filter data by a set of
customized rules. It allows you to use the Qualification Criteria functionality to its full advantage, so that it is
possible to apply certain rules during the Work Order creation and use only the necessary operations.
This component is already included in the Opcenter EX DS setup but, if necessary, follow the steps illustrated
below.
For more information on Qualification Criteria, see:
• Qualification Criteria in the Opcenter Execution Discrete Product Overview.
• How to Configure Qualification Criteria in the Opcenter Execution Discrete User Manual.

Prerequisites
IIS ASP.NET Core 8.0.x Hosting Packet Package has been downloaded and installed.

Procedure
1. In the Internet Information Services (IIS) Manager, click Application Pools.
2. Select the following Application Pool: ProductionResolution.WebApi.
3. Right click Advanced Settings and set the .NET CLR Version parameter to No Managed Code.
4. Click OK.

### How to Configure the PLMX-Viewer

The PLMX-Viewer is a component that is used when there is integration with Teamcenter Manufacturing: its purpose
is to create a tridimensional (3D) rendering from a plmx file that can be subsequently displayed. In Opcenter
Execution Discrete, when a plmx file is attached as a Document to a business entity (for example, to a Work Order
Operation), the resulting 3D model can be displayed in the Document Previewer, which is available in the Operator
Landing page (legacy), in the High Automation Landing page (legacy), and in the Low Code UI Apps runtime
working environments.
Although included in the Opcenter EX DS setup, the PLMX-Viewer requires proper configuration so that it can be
used. The procedure that must be followed to perform this configuration depends on the target scenario: the PLMXViewer supports both Stand-alone and Distributed scenarios.

Available Procedures
• Configuring the PLMX-Viewer in a Stand-alone Scenario
• Configuring the PLMX-Viewer in a Distributed Scenario

#### Configuring the PLMX-Viewer in a Stand-alone Scenario

In a Stand-alone scenario, you will need to configure the PLMX-Viewer on the Opcenter Execution Foundation host.

Prerequisite
It is necessary that you possess a valid PLMVisWeb license.

Procedure
1. Import the PLMVisWeb license to your Opcenter License Server.

2. On the runtime host where you will install the PLMX-Viewer, create the following system environment variable:
PLMVISWEB_LICENSE_SERVER = 28000@machinename
where machinename must coincide with the name of the License Server host on which the license has been
imported.
3. Browse to %SITUnifiedVAppsRoot%\UADM\PLMX and unzip file PLMXPackage.zip under a path of your
choice (for example, %SITUnifiedVAppsRoot%\UADM\PLMX\PLMXPackage).
4. Open Command Prompt with Administrator rights where you unzipped file PLMXPackage.zip file: go to the
Scripts folder.
5. After reading the Note below, proceed to run batch file Register_Plmx_And_License_Service.bat to install
PLMX Service and License Service as Windows services.
Batch file Register_Plmx_And_License_Service.bat allows you to pass input parameters. If input
parameters are not passed, default values will be assigned.
Instead of passing the parameters to the batch file, you can also make a copy of batch file
Register_Plmx_And_License_Service.bat and modify the default values: in this case, your batch file
is customized for your scenario.
In order to modify a parameter, you must specify all those preceding the parameter you want to
change. Consult the following table to determine the exact order of the parameters:
Position

Parameter Name

Description

Default Value

1

LicenseServiceUrl

The URL to be used to access
the License Service from
clients.

/plmxLicense/api/route

2

AuthorizationServ
erUrl

The URL to be used by PLMX
Service to reach the
Introspection endpoint
provided by Opcenter EX FN to
validate the token (locally).

http://localhost/sit-auth/
oauth/introspect

3

PLMX Service Port

Port to be used for PLMX
Service.

8089

4

License Service
Port

Port to be used for License
Service.

5555

5

Protocol

Protocol used for internal
communication
between Opcenter Execution
Foundation and PLMX Service.
Only http is supported.

http

6

PlmxCacheLocatio
n

Local folder where PLMX
cached contents are stored.

%SITUnifiedVAppsRoot%
\UADM\PLMX\PLMXPackag
e\Cache

7

PlmxCacheLimit

Maximum allowed size
(expressed in MB) for the PLMX
Service cache folder.

1000 MB

Position

Parameter Name

Description

Default Value

8

Node exe Path

Local folder path
where node.exe is present.

%SITUnifiedSystemRoot%
\bin

6. Operating in Opcenter EX DS, in Configuration Keys page > Integration tab > PLMX Service URL, add the PLMX
URL to the Opcenter EX DSenvironment: enter protocol://machineName, where protocol is either http or https
(depending on how Opcenter Execution Foundation has been configured), and machineName is the machine
hosting Opcenter EX FN.
For more information, see Integration Configuration Settings in the Opcenter Execution Discrete User Manual.
HTTPS Certificates
If you have configured Opcenter EX FN in HTTPS, it is necessary that you install the Certificate
under Trusted Roots of the Opcenter EX FN Host. This is required when the Certificate is self-signed.

#### Configuring the PLMX-Viewer in a Distributed Scenario

For Distributed scenarios in which there coexist multiple hosts, you will need to configure the PLMX-Viewer on only
one Opcenter EX FN host.
In addition, you must configure the load balancer (for example, ARR) so that the PLMX calls can be routed to the
Opcenter EX FN host on which the PLMX-Viewer has been configured.
Considering that the PLMX-Viewer is configured on only one Host, high availability for PLMX is not
supported.

Prerequisite
It is necessary that you possess a valid PLMVisWeb license.

Procedure
1. Import the PLMVisWeb license to your Opcenter License Server.
2. On the runtime host where you will install the PLMX-Viewer, create the following system environment variable:
PLMVISWEB_LICENSE_SERVER = 28000@machinename
where machinename must coincide with the name of the License Server host on which the license has been
imported.
3. Browse to %SITUnifiedVAppsRoot%\UADM\PLMX and unzip file PLMXPackage.zip under a path of your
choice (for example, %SITUnifiedVAppsRoot%\UADM\PLMX\PLMXPackage).
4. Open Command Prompt with Administrator rights where you unzipped file PLMXPackage.zip file: go to the
Scripts folder.
5. After reading the Note below, proceed to run batch file Register_Plmx_And_License_Service.bat to install
PLMX Service and License Service as Windows services.
Batch file Register_Plmx_And_License_Service.bat allows you to pass input parameters. If input
parameters are not passed, default values will be assigned.
Instead of passing the parameters to the batch file, you can also make a copy of batch file
Register_Plmx_And_License_Service.bat and modify the default values: in this case, your batch file

is customized for your scenario.
In order to modify a parameter, you must specify all those preceding the parameter you want to
change. Consult the following table to determine the exact order of the parameters:
Position

Parameter Name

Description

Default Value

1

LicenseServiceUrl

The URL to be used to access
the License Service from
clients.

/plmxLicense/api/route

2

AuthorizationServ
erUrl

The URL to be used by PLMX
Service to reach the
Introspection endpoint
provided by Opcenter EX FN to
validate the token (locally).

http://localhost/sit-auth/
oauth/introspect

3

PLMX Service Port

Port to be used for PLMX
Service.

8089

4

License Service
Port

Port to be used for License
Service.

5555

5

Protocol

Protocol used for internal
communication
between Opcenter Execution
Foundation and PLMX Service.
Only http is supported.

http

6

PlmxCacheLocatio
n

Local folder where PLMX
cached contents are stored.

%SITUnifiedVAppsRoot%
\UADM\PLMX\PLMXPackag
e\Cache

7

PlmxCacheLimit

Maximum allowed size
(expressed in MB) for the PLMX
Service cache folder.

1000 MB

8

Node exe Path

Local folder path
where node.exe is present.

%SITUnifiedSystemRoot%
\bin

6. Operating in Opcenter EX DS, in Configuration Keys page > Integration tab > PLMX Service URL, add the PLMX
URL to the Opcenter EX DSenvironment: enter protocol://machineName, where protocol is either http or https
(depending on how Opcenter Execution Foundation has been configured), and machineName is the Opcenter
EX FN host on which the PLMX-Viewer is being configured.
For more information, see Integration Configuration Settings in the Opcenter Execution Discrete User Manual.

HTTPS Certificates
If you have configured Opcenter EX FN in HTTPS and the PLMX-Viewer has been configured on Host1, it
is necessary that you install the Certificate for Host1 under Trusted Roots of all the Opcenter EX FN
Hosts, including Host1. This is required when the Certificate is self-signed.

7. Configure the load balancer to route PLMX calls to the Opcenter EX FN host on which the PLMX-Viewer has been
configured. See the example below for insight in merit.

Load Balancer Configuration: Example
We have a Distributed scenario with 3 nodes, in which the PLMX-Viewer has been configured on Node1 and the load
balancer is ARR:
• Node1: Opcenter EX FN host on which the PLMX-Viewer has been configured
• Node2: Opcenter EX FN host
• Node3: Opcenter EX FN host
• VM-NODO-ARR: ARR/Load Balancer.
Operating on VM-NODO-ARR (that is, the load balancer machine):
1. In Internet Information Service (IIS) Manager, create the Server Farm with the same Address as that of the
Node1 machine.
2. Create Redirect Rule at the root level on IIS of the ARR machine and select Route to Server Farm as the Action
Type.
3. Enter ^plmx(.*) in Pattern.

## Integration with Other Systems

Opcenter Execution Discrete offers the following possibilities of integration with other systems, which can be used
either separately or in combination with one another:
• Integration with Siemens Opcenter APS
• Integration with Teamcenter Manufacturing
• Integration with Opcenter Connect MOM
• Integration with Teamcenter Share
• Integration with Additive Manufacturing Network
• Integration with Shopfloor
• Integration with Teamcenter Easy Plan
• Integration with Opcenter Intraplant Logistics (Opcenter IPL)

### How to Integrate Opcenter Execution Discrete with Opcenter APS

Integration with Opcenter APS, the Siemens solution for Advanced Planning and Scheduling, allows you to close the
gap between planning/scheduling and execution.
Thanks to the exchange of information between Opcenter Execution Discrete and Opcenter APS regarding orders,
operations and machine to be used, you will be able to:
• Schedule execution according to the APS system's capabilities.
• Refine your production plan on the basis of numerous factors (availability, setup time, theoretical production
duration, etc).
The synergy that you can create with Opcenter APS helps you to streamline execution activities in a capillary
manner, as they are scheduled for each machine within the actual context of what is currently occurring on the
shop floor.
During these planning and scheduling activities, if changes are made to production, then Opcenter EX DS will send
data to Opcenter APS via a dedicated Alerts window in order for corrective measures and tuning to be adopted to
the schedule.
Integration with Opcenter APS should be restricted solely to those Users who are fully aware of the
consequences that they may incur should they fail to implement this feature correctly.
If you are not familiar with these aspects, forego attempting integration and consult expert users.

Target User
Users with the APS role can perform this integration.

Prerequisites
• Opcenter Execution Discrete is installed and configured correctly.
• Siemens Opcenter APS 2504 is installed and configured correctly. For Opcenter APS support, see the Opcenter
APS website (https://www.plm.automation.siemens.com/global/en/products/manufacturing-operationscenter/preactor-aps.html).
• The Opcenter APS configuration package is available for installation. Refer to the Opcenter APS Technical
Support.

Workflow
Integrating Opcenter EX DS with Opcenter APS involves performing the following steps:
1. Install the Opcenter APS configuration package.

2. Generate and validate a security certificate for the APS role.
3. Enable integration with Opcenter APS in the Opcenter Execution Discrete environment.
4. Enable integration with Opcenter Execution Discrete in the Opcenter APS environment.
In case of Multiplant scenario, perform above mentioned Workflow steps for each plant. For more
information on Multiplant, see the Multiplant Management chapter in Opcenter Execution
Foundation Installation Guide.

#### Installing the Opcenter APS Configuration Package

To install the Opcenter APS configuration package, you must perform the following procedure. For more
information, refer to Opcenter APS documentation.

Prerequisite
The user who intends to install the package must possess the dbcreator role on the SQL Server instance.
To verify this, from the Microsoft SQL Server Management Studio environment > Security > Server
Roles node, right-click dbcreator in the tree view and click Properties. The Server Role Properties dialog
box displays the members of this role.

Procedure
1. Double-click the Opcenter APS Opcenter EX DS 2.1.prpkg Package File you have received from the Opcenter
APS Technical Support.
2. In the Opcenter APS Configuration Package Manager wizard, click Next.
3. In the Configuration Files and Local Reports area, set Install configuration files and local reports.
4. Take note of the path selected in the Configuration Folder field, because it will be requested while enabling
integration with Opcenter EX DS.
5. In the Database area, set Install database. Optionally modify the database name if the default name is not
appropriate. Then click Next.
6. In the SQL Server Location area, set Local Machine to create the Opcenter APS database.
7. Click Next and then click Finish. The Opcenter APS database is installed on the specified SQL Server instance.

In case of Multiplant scenario, configuration package needs to be created for each plant separately.
Therefore, perform above mentioned Procedure for each plant. For more information on Multiplant, see
the Multiplant Management chapter in Opcenter Execution Foundation Installation Guide.

#### Enabling Integration with Opcenter APS in the Opcenter Execution Discrete Environment

1. Access Opcenter EX DS web user interface. Refer to Opcenter Execution Discrete User Manual for details.
2. Click
System Configuration > Configuration Keys in the sidebar.
3. Select the Integrations tab.
4. Select the Enable APS Integration check-box, to enable the integration.
5. Set the Percentage for APS (%) field: this value (expressed in percentage of the Operation Duration) represents
the maximum allowed delta between the estimated start time and the actual start time (and the estimated end
time and the actual end time) of a Work Order Operation. If this percentage is exceeded, this value is considered

significant and Opcenter APS will receive a dedicated alert in merit. You can take this into account for your
calculations, if desired.
6. Click Save.
Additional configuration keys are provided in the same page to further customize the behavior in an
integrated scenario.

#### Enabling Integration with Opcenter Execution Discrete in the Opcenter APS Environment

To enable integration with Opcenter Execution Discrete in the Opcenter APS environment:
1. On the Opcenter APS machine, browse to the path mentioned at step 4 of the Opcenter APS Configuration
Package installation procedure and double-click the Opcenter EX DS Integration.prcdf file.
2. If you are opening the Opcenter APS Command Definition File for the first time, activate the license.
3. From the Opcenter APS environment, click Configuration > Settings in the menu list.
4. In the Settings area, click MES Integration Settings.
5. In the MES Integration Settings dialog box, set the following parameters:
Parameter

Description

Alerts Enabled

Enables the visualization of the Alerts Window in the Sequencer page.

Refresh Frequency

Defines the default time (in seconds) between each refresh of
the Alerts Window, according to the time interval between each polling
for changes in the MES system. Refreshing too frequently will cause
increased network traffic, and additional load on both Opcenter
APS and the MES system. In case you need to refresh data in the Alerts
Window, you can refresh data manually from the Sequencer page.

Target Platform

Set to Opcenter EX DS.

Service URI

http://<server name>/sit-svc/<plantId>/Application/AppU4DM/
odata.
Here, <plantId> is the plant in case of Multiplant scenario, and if no
plant is specified, then it indicates the default plant.

Certificate

The name of the security certificate you have generated and validated.

##### Using Alerts Window

The Alert functionality is based on the polling performed by Opcenter APS on the Opcenter EX DS APSAlert entity
that collects information on the following deviations of runtime activities from planned activities:
• DeviationActualResource; when a Work Order Operation or Execution Group Phase is started on a different
machine.
• DeviationActualStartTime, when a Work Order Operation or Execution Group Phase starts either earlier or
later than scheduled.

• DeviationActualEndTime, when a Work Order Operation or Execution Group Phase ends either earlier or later
than scheduled.
• SequenceChangeOnResource, when the execution sequence of the Work Order Operations or Execution Group
Phases changes on a specific machine.
After enabling the Alerts Window, you can open it and refresh the data displayed therein.

Prerequisite
The Enable APS Integration configuration key has been enabled. For more information see Integration
Configuration Settings in the Opcenter Execution Discrete User Manual.

Procedure
1. In the Opcenter APS environment, click Workspace in the menu list.
2. In the General area, click Generate Schedule.
3. In the Sequencer page, from the View menu, click Alerts Window to open the Alerts Window.

4. The system refreshes the data in the Alerts Window automatically at configurable time intervals (previously set,
when you have enabled the Alerts Window). If you want to refresh data manually, select the Alerts Window and

click View menu > Refresh Alerts.

### How to Integrate Opcenter Execution Discrete with Teamcenter Manufacturing

Opcenter Execution Discrete can be integrated with Teamcenter Manufacturing (TCM), the Siemens solution for
defining, structuring and planning your production processes, via Opcenter Connect Teamcenter.
This foresees setting up the Siemens product-to-production platform among Opcenter Execution Discrete,
Teamcenter Manufacturing and SAP, so that data can be shared and the planning and execution functions provided
by the joint adoption of the three systems can be exploited.
Opcenter Execution Discrete is compatible with Opcenter Connect EX FN and FN4T.
For more information, consult the Active Integration Compatibility Matrix available for download (under
tab Support > area Active Integration Software Certifications and Software ) at https://
www.plm.automation.siemens.com/global/en/support/certifications.html.
The workflow below provides the steps required Opcenter Execution Discrete side to integrate with Teamcenter
Manufacturing.
For a more detailed overview of all configuration steps required by all the products interacting within the context of
the Closed Loop Manufacturing solution, refer to the Configuration Guides provided for Opcenter Connect FN for
Teamcenter and Opcenter Connect FN for SAP S/4HANA, which can be downloaded from the Active Integration
section on the Siemens Support Center.

Workflow
1. Generate the security certificate for the Manufacturing Process Planner (MPP) Role.
Note The certificate must be imported to the Opcenter Connect Teamcenter machine, following the instructions
provided in the Opcenter Connect Teamcenter Installation Guide.
2. Verify the correct configuration of the required Event Subscriptions.
3. Set CLM Integration configuration keys as described in section CLM Integration Configuration Settings of the
Opcenter Execution Discrete User Manual.

### How to Integrate Opcenter Execution Discrete with Opcenter Connect MOM

Opcenter Execution Discrete releases an integration scenario configuration that after being imported into Opcenter
Connect MOM enables the integration between the two products.
After importing the released integration scenario configuration, you will be able to:
• exchange structured messages between the MES layer and the Shop Floor to automate certain activities during
production execution.
• exchange structured messages between the MES layer and the External System to import and delete data,
through dedicated XML or JSON files that must be properly configured to be validated and processed by the
system.
• receive Input Messages from the Warehouse, containing information on the state of Kanban calls made for the
replenishment of Materials.
Along with this integration scenario and a few additional configurations, you can also configure Opcenter Execution
Discrete to send Output Messages to external systems.

Prerequisites
• Opcenter Execution Foundation 2507 is installed and configured.
• Opcenter Execution Discrete 2507 is installed and configured.
• Opcenter Connect MOM 2504 is installed and configured.
• In case of Fully Distributed scenarios, the Opcenter CN MOM Connection must be configured through the ARR (or
in general Network Load Balancer) address in order to route the calls to an available Service Layer. For more
information, see How to Configure a Distributed Scenario chapter in Opcenter EX FN Installation Guide.
• An Opcenter EX DS user exists in your system and it is associated to the ShopFloorDevice user role.
• (Specific to Output Messages) Opcenter CN MOM Client Gateway is installed and configured on the Opcenter
Execution Foundation machine.
If you have localized your system (for example, in Italian), keep in mind that when implementing the use
cases, decimal values must be passed using a comma, rather than a period, as the separator. The same
concept applies also to dates (for example, the day must precede the month).
The following limitations may apply to the import of data:
• Opcenter Connect MOM usually processes files of up to 10MB at a maximum rate of 2 messages per
minute per adapter/broker (typical scenario: no mapping scripts, basic dispatch rule, messageresponse workflow, logging set to Low-Normal).
• Exceptionally, Opcenter Connect MOM may process files of up to 20MB at a maximum rate of 1
message per minute per adapter/broker. It must be noted that the processing time of files larger than
10MB increases exponentially.
• Files larger than 20MB are not recommended, since the system is not guaranteed to work properly.

Configuration Steps
The following configuration steps represent one of the possibilities provided by Opcenter CN MOM to let different
systems communicate. More specifically, the released scenario focuses on the File Adapter adoption, in order to
trigger a business logic provided by Opcenter Execution Discrete. Nothing prevents you from using other Adapters
as foreseen by Opcenter CN MOM.
Follow these configuration steps to import the configuration:

1. Import the Integration Scenario configuration.
2. Finalize the Imported Configuration.
3. If you want to exchange messages with the Shop Floor: configure the XML file specific to your Use Case.
4. If you want to automatically import (and delete) data: configure the XML or JSON file specific to the data you
want to import.
5. Reset IIS and restart the Opcenter Connect MOM Channel Adapter Host Service to activate the Use Case
configuration.
6. Verify that the configuration works properly.
If you want to configure Opcenter CN MOM to send Output Messages, see: How to Send Output Messages to
Opcenter CN MOM.

Direct Dispatch Support
Opcenter Connect MOM Direct Dispatch is supported for messages exchanged with the Shop Floor. If you want to
change the configuration in order to leverage on the Direct Dispatch, see: How to Configure Direct Dispatch for
Messages exchanged with the Shop Floor.

Multiplant Scenario
Opcenter Execution Discrete can manage a Multiplant scenario supporting multiple factories from a unique central
installation. This means that, when configuring the system, you can create more plants that are served by a
Centralized Regional Hub.
For more information on Multiplant, see the Multiplant Management chapter in the Opcenter Execution
Foundation Installation Guide.
Multiplant use cases for inbound messages are:
Use Case

Inbou
nd
Messa
ge
Flow

Plant Description

ERP →
MES

Impor
t

The Plant Id attribute is present in the ERP Message. The Plant Id is extracted from the
message to create the end point (MOM Connection + plantid attribute + restcommand
message attribute).
The MOM Connection does not have any information about the plant, as the plant is
taken from the message itself.

Shop
Floor →
MES

Shop
Floor

The Message is routed to the right end point through a dedicated MOM Connection per
plant and a dedicated File Adapter per plant.
The MOM Connection holds the information about the plant, for example: http://
myEXDSServer/sit-svc/Plant1. If the plant is not specified, the message is routed to the
default plant.
If you want to use the Direct Dispatch functionality, only one plant can be
addressed as the MOM Connection is overwritten in the Message Type itself.

Use Case

Inbou
nd
Messa
ge
Flow

Plant Description

Input
Message

Input

The Message is routed to the right end point through a dedicated MOM Connection per
plant and a dedicated File Adapter per plant.
The MOM Connection holds the information about the plant, for example: http://
myEXDSServer/sit-svc/Plant1. If the plant is not specified, the message is routed to the
default plant.

• The Shop Floor File Adapter and the Input File Adapter are configured to be plant-specific. They are linked to the
UADM_Plant MOM Connection that has the address with the plant in it, for example: http://myEXDSServer/sitsvc/Plant1.
• The Import File Adapter is linked to the UADM MOM Connection, that does not contain the information about
the plant, since it is the workflow that retrieves the Plant from the message and addresses the correct plant in
the command call. In this case, the address could be: http://myEXDSServer/sit-svc.

#### Importing the Integration Scenario Configuration

Opcenter Execution Discrete set includes preconfigured integration scenarios to be imported into Opcenter
Connect MOM to enable the integration between the two products.

Procedure
1. Access the Opcenter Connect MOM login page.
2. Log in to the Opcenter Connect MOM Web Application.
3. Select the
> Import Data command.
4. Browse the EXDS2401_OpcenterCNMOMExport.json file (available in
%SITUnifiedSystemRoot%VApps\UADM\MIOIntegration).
5. Click the Import Data button.
6. Close the Import Data dialog box.

#### How to Finalize the Imported Configuration

After importing the integration scenario configuration, it is necessary to set some parameters specific for each
project.
In particular, you must set parameters related to:
• MOM Connection, in order to properly establish the communication between Opcenter Connect MOM
and Opcenter EX DS.
• File Adapters. The imported File Adapters contain predefined settings for folders dedicated to inbound and
outbound messages, but you can modify them according to your needs. If you want to maintain the default
settings, skip the procedure for configuring the File Adapters described below and simply perform the following
operations on your machine:
• For messages from the Shop Floor, create the following folders:
• C:\UADMAutomaticShopFloor\inbound
• C:\UADMAutomaticShopFloor\outbound
• For Input Messages, create the following folders:
• C:\OpcenterEXDSInputMessage\inbound

• C:\OpcenterEXDSInputMessage\outbound
• For Import Data Flows, create the following folders:
• C:\OpcenterEXDSImport\inbound
• C:\OpcenterEXDSImport\outbound
• C:\OpcenterEXDSImport\inboundJson
• C:\OpcenterEXDSImport\outboundJson

Available Operations
• Configuring the MOM Connection
• Configuring the File Adapters.

##### Configuring the MOM Connection

The MOM Connection properly establishes the communication between Opcenter EX DS and the Opcenter Connect
MOM Web Application.

Procedure
1. In the Opcenter Connect MOM Web Application, click the General Configuration tile.
2. Click the MOM Connections tab.
3. Select the UADM MOM Connection. In case of Multiplant, select UADM_Plant MOM Connection.
4. Select Base Configuration and then click
5. Set the following properties:

.

Propert
y

Value

Address

Type the address of the machine on which Opcenter EX DS is installed, followed by /sit-svc. The
address must begin with either http or https (for example: http://myEXDSServer/sit-svc).
In case of Multiplant, the address can be, for example: http://myEXDSServer/sit-svc/MyPlant.
Here, MyPlant is the plant addressed by the MOM Connection in the multiplant use case.

User
Name

Type the name of an Opcenter EX DS user associated to the ShopFloorDevice user role.

Passwor

Type the password associated to the Opcenter EX DS user.

Authenti
cation
Address

Type the URL of the UMC authentication server: for example, http://myEXDSServer/sit-auth/
OAuth/Token.

6. Click

.

For Shop Floor and Input messages, the Multiplant can be addressed with dedicated Adapters for each
plant, along with its dedicated MOM Connection for each respective plant.
In the plant-specific MOM Connections, the address should include the plant information, for example:
http://myexdsserver/sit-svc/Plant1.

##### Configuring the File Adapters

The File Adapters contain predefined settings for folders for inbound and outbound messages and must be
configured to enable automatic data exchange.
Depending on the functionality you intend to use, the related File Adapter must be configured accordingly:
• Configure the file adapter for messages from the Shop Floor
• Configure the file adapter for automatic data import (XML File)
• Configure the file adapter for automatic data import (JSON File)
• Configure the file adapter for input messages

Configuring the File Adapter for messages from the Shop Floor
1. In the Opcenter Connect MOM Web Application, click the Adapter Configuration tile.
2. Click the File tab.
3. Select the uadmautomaticshopfloorfileadapter File Adapter.
4. Select File Adapter Configuration and click
5. Set the following parameters:

.

Parameter

Description

Inbound URI

The path to the folder where the input XML file will be placed. (By
default C:\UADMAutomaticShopFloor\inbound.)

Outbound URI

The path to the folder where the output XML file will be placed. (By
default C:\UADMAutomaticShopFloor\outbound.)

6. Click

.

Configuring the File Adapter for automatic Data Import (XML File)
1. In the Opcenter Connect MOM Web Application, click the Adapter Configuration tile.
2. Click the File tab.
3. Select the opcenterexdsimportfileadapter File Adapter.
4. Select File Adapter Configuration and click
5. Set the following parameters:

.

Parameter

Description

Inbound URI

The path to the folder where the input XML file will be placed. (By default C:
\OpcenterEXDSImport\inbound.)

Outbound
URI

The path to the folder where the output XML file will be placed. (By default C:
\OpcenterEXDSImport\outbound.)

6. Click Save

.

Configuring the File Adapter for automatic Data Import (JSON File)
1. In the Opcenter Connect MOM Web Application, click the Adapter Configuration tile.
2. Click the File tab.

3. Select the opcenterexdsimportfileadapterJson File Adapter.
4. Select File Adapter Configuration and click
5. Set the following parameters:

.

Parameter

Description

Inbound URI

The path to the folder where the input JSON file will be placed. (By default C:
\OpcenterEXDSImport\inboundJson.)

Outbound
URI

The path to the folder where the output JSON file will be placed. (By default C:
\OpcenterEXDSImport\outboundJson.)

6. Click Save

.

Configuring the File Adapter for Input Messages
1. In the Opcenter Connect MOM Web Application, click the Adapter Configuration tile.
2. Click the File tab.
3. Select the opcenterexdsinputmsgadapter File Adapter.
4. Select File Adapter Configuration and click
5. Set the following parameters:

.

Parameter

Description

Inbound URI

The path to the folder where the input XML file will be placed. (By default C:
\OpcenterEXDSInputMessage\inbound.)

Outbound
URI

The path to the folder where the input XML file will be placed. (By default C:
\OpcenterEXDSInputMessage\outbound.)

6. Click Save

.

• For Shop Floor and Input messages, the Multiplant can be addressed with dedicated File Adapters for
each plant, along with its dedicated MOM Connection for each respective plant. In the plant-specific
MOM Connections, the address should include the plant information, for example: http://
myexdsserver/sit-svc/Plant1.
• The File Adapter for each plant should have dedicated inbound and outbound folders.

#### How to Exchange Messages with the Shop Floor

Thanks to the Opcenter Connect MOM integration scenario configuration included in the Opcenter Execution
Discrete setup, messages can be exchanged between the MES layer and the Shop Floor to automate certain
activities. In detail:
• Machines or Workcenters can automatically start and complete Work Order Operations, regardless of the
Production Type.
• Work Order notes can be added automatically from Machines or Workcenters to all Work Order Operations
making up the Work Order that is currently being executed.

• Machines or Workcenters can automatically create and resolve Quality Non-Conformances on Work Order
Operations, Material Tracking Units and Machines.
• Materials can be automatically consumed during the execution of Work Order Operations.
• Tools can be automatically used during the execution of Work Order Operations.
• Work Instruction data or Quality Inspection data can be automatically collected during the execution of Work
Order Operations.
• The system can receive Input Messages from the Warehouse, containing information on the state of Kanban
calls made for the replenishment of Materials.
To attain these goals, you must create the respective XML files according to a predefined structure.
Shop Floor messages are configured out-of-the-box to rely on the Opcenter Connect MOM Broker. It is
also possible to configure them to use the Direct Dispatch functionality, in order to send messages directly
from the Adapter to Opcenter Execution Discrete. For details, see: How to Configure Direct Dispatch for
Messages Exchanged with the Shop Floor.

##### Work Order Operation Start

This use case allows you to trigger the automatic start of Work Order Operations by Machines or Workcenters.
The start will be successfully executed if no other Work Order Operations (of the same type) are queued on the
same Machine.
The start of the Work Order Operation will be traced as performed by "" (blank space indicating "no user").
The Work Order Operation NId must not be specified because it is retrieved on the basis of the Work Order
Operation type and the involved Machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Automatic Work Order Operation Start message
Here is an example of an XML message that can be used to trigger an Automatic Work Order Operation Start.
Export File
<?xml version="1.0" encoding="utf-8"?>
<WOO_START>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<TIMESTAMP>2018-10-27T16:15:00Z</TIMESTAMP>
<CATEGORY>Drilling</CATEGORY>
<PRODUCT ID="sn001" QTY="1" />
<PRODUCT ID="sn002" QTY="1" />
</WOO_START>

Here is the XSD that describes and validates the Automatic Work Order Operation Start XML message:

XSD
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="WOO_START">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="CATEGORY" maxOccurs="1" minOccurs="1"/>
<xs:element name="PRODUCT" maxOccurs="unbounded" minOccurs="1">
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="ID" use="required"/>
<xs:attribute type="xs:decimal" name="QTY" use="required"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <WOO_START> tag specifies that the scope of the message is to define an Automatic Work Order Operation
Start.
The attributes of an Automatic Work Order Operation Start are specified by the following tags:
Tag

Description

Occurre
nce

<EQUIPMENT_
NAME>

The Equipment Name that triggered the Automatic Work Order Operation Start.

Mandat
ory

<TIMESTAMP>

The Actual Start Time of the Work Order Operation.

Optiona

The timestamp must respect the UTC format: for example, yyyy-MMddThh:mm:ssZ.
<CATEGORY>

The Category of the Work Order Operation that is started.

Mandat
ory

Tag

Description

Occurre
nce

<PRODUCT>

The list of Material Tracking Units on which the Automatic Work Order
Operation Start takes place. The related Material Tracking Units are described by
the following attributes:

Mandat
ory

• ID: Either the BatchId or the SerialNumberCode of the Material Tracking Unit
on which the Automatic Start takes place.
• QTY: The quantity of either the Batch or the SerialNumber being started with
the current action.
In case of FlexibleSerialized Production Type, which has Work Order Operations
of type Dynamic, if the Serial Numbers do not exist and the Work Order is not yet
frozen, the Automatic Start creates the serial numbers automatically.
In case of FlexibleBatch Production Type, which has Work Order Operations of
type Dynamic, if the Work Order is not yet frozen, the Automatic Start
automatically updates the Batch quantity according to the quantity you set in the
XML file, if different from the Planned Target Quantity.

##### Work Order Operation Completion

The use case allows you to trigger the automatic completion of Work Order Operations by Machines or Workcenters.
The completion of the Work Order Operation will be traced as performed by "" (blank space indicating "no user").
The Work Order Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Order
Operation type and the involved Machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Automatic Complete message
Here is an example of an XML message that can be used to describe an Automatic Complete:
Export File
<WOO_COMPLETE AVOID_PAUSING_OTHER_PRODUCTS="False">
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<TIMESTAMP>2020-06-18T16:15:00Z</TIMESTAMP>
<CATEGORY>Drilling</CATEGORY>
<PRODUCT ID="sn001" QTY="1" RESULT="OK" />
<PRODUCT ID="sn002" QTY="1" RESULT="NOK" />
<PRODUCT ID="sn003" QTY="1" />
</WOO_COMPLETE>

Here is the XSD that describes and validates the Automatic Complete XML message:

XSD
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" attributeFormDefault="unqualif
ied" elementFormDefault="qualified">
<xs:element name="WOO_COMPLETE">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" />
<xs:element type="xs:dateTime" name="TIMESTAMP" />
<xs:element type="xs:string" name="CATEGORY" />
<xs:element name="PRODUCT" maxOccurs="unbounded" minOccurs="0">
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="ID" use="optional" />
<xs:attribute type="xs:byte" name="QTY" use="optional" />
<xs:attribute type="xs:string" name="RESULT" use="optional" /
>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
</xs:sequence>
<xs:attribute type="xs:string" name="AVOID_PAUSING_OTHER_PRODUCTS" use="opti
onal" />
</xs:complexType>
</xs:element>
</xs:schema>

The <WOO_COMPLETE> tag specifies that the scope of the document is to define an Automatic
Complete message.
The attributes of an Automatic Complete are specified by the following tags:

Tag

Description

Occurrence

<WOO_COMPLETE>

Root tag of the Automatic Complete message, that in addition
to defining the scope of the message, also contains the
AVOID_PAUSING_OTHER_PRODUCTS attribute. This attribute
can be used to configure the behavior of the system when
completing Material Tracking Units.
If the attribute is set to False, when an MTU is completed for a
specific Work Order Operation, the other active MTUs to be
produced are paused.
If set to True, the other MTUs remain active along with the Work
Order Operation.
This attribute is optional and only applicable for
Serialized and FlexibleSerialized production types. If
specified, this attribute overrides the value set for the
Complete Serial Number(s) without pausing other
configuration key.

<EQUIPMENT_NAME>

The Equipment Name that triggered the Automatic Complete.

Mandatory

<TIMESTAMP>

The Actual End Time of the Work Order Operation.

Optional

The timestamp must respect the UTC format: for example,
yyyy-MM-ddThh:mm:ssZ.
<CATEGORY>

The Category of the Work Order Operation that is completed.

Mandatory

<PRODUCT>

The list of Material Tracking Units on which the Automatic
Complete takes place. The related Material Tracking Units are
described by the following attributes:

Mandatory

• ID: The BatchId or SerialNumberCode of the Material
Tracking Unit on which the Automatic Complete takes place.
• QTY: The quantity of the Batch or SerialNumber that is
completed with the current action.
• RESULT (optional): String reflecting the positive or negative
result (outcome) of the Batch or SerialNumber that is
completed with the current action. Custom results are
acceptable.

##### Work Order Note Creation

The use case allows you to trigger the automatic creation of a Work Order note by Machines or Workcenters on all
the Work Order Operations making up the Work Order that is currently being executed: this can be done at runtime.
The creation of the Work Order note will be traced as performed by "" (blank space indicating "no user").
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.

The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Automatic Work Order Note Creation message
Here is an example of an XML message that can be used to trigger an Automatic Work Order Note Creation:
Export File
<WO_NOTE>
<EQUIPMENT_NAME>DrillingMachine01</EQUIPMENT_NAME>
<TIMESTAMP>2021-05-18T12:15:00Z</TIMESTAMP>
<CATEGORY>Drilling</CATEGORY>
<NOTE>My notes</NOTE>
</WO_NOTE>

Here is the XSD that describes and validates the Automatic Work Order Note Creation XML message:
XDS
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="WO_NOTE">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="CATEGORY" maxOccurs="1" minOccurs="1"/>
<xs:element type="xs:string" name="NOTE" maxOccurs="1" minOccurs="1"/>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The WO_NOTE tag specifies that the scope of the message is to define an Automatic Work Order Note Creation.
The attributes of an Automatic Work Order Note Creation are specified by the following tags:
Tag

Description

Occurrence

<EQUIPMENT_NAME>

The Equipment Name that triggered the Automatic
Work Order Note Creation.

Mandatory

Tag

Description

Occurrence

<TIMESTAMP>

The Timestamp of the Automatic Work Order Note
Creation.

Optional

The timestamp must respect the UTC format: for
example, yyyy-MM-ddThh:mm:ssZ.
<CATEGORY>

The Category of the Work Order Operation that
belongs to the Work Order for which the note is
being automatically created.

Mandatory

<NOTE>

The text of the Note that is being automatically
created.

Mandatory

##### Quality Non-Conformance Creation on Work Order Operations

The use case allows you to trigger the automatic creation of a Non-Conformance of type Quality on Work Order
Operations by Machines or Workcenters.
The creation of the Non-Conformance will be traced as performed by "" (blank space indicating "no user").
The Work Order Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Order
Operation type and the involved Machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Automatic Creation of Non-Conformance on Work Order
Operation message
Here is an example of an XML message that can be used to trigger an Automatic creation of Non-Conformance on
Work Order Operation:
Export File
<?xml version="1.0" encoding="utf-8"?>
<OPEN_NC_ON_WOO>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<TIMESTAMP>2018-10-27T16:15:00Z</TIMESTAMP>
<CATEGORY>Drilling</CATEGORY>
<DEFECT_TYPE>Scratch</DEFECT_TYPE>
<DEFECT_TYPE>Bump</DEFECT_TYPE>
<SEVERITY>High</SEVERITY>
<NOTE>Notes</NOTE>
</OPEN_NC_ON_WOO>

Here is the XSD that describes and validates an Automatic creation of Non-Conformance on Work Order
Operation:
XSD
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="OPEN_NC_ON_WOO">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="CATEGORY" maxOccurs="1" minOccurs="1"/>
<xs:element type="xs:string" name="DEFECT_TYPE" maxOccurs="unbounded"
minOccurs="0"/>
<xs:element type="xs:string" name="SEVERITY" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="NOTES" maxOccurs="1" minOccurs="0"/>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <OPEN_NC_ON_WOO> tag specifies that the scope of the message is to define an Automatic Creation of NonConformance on Work Order Operation:
The attributes of an Automatic Creation of Non-Conformance on Work Order Operation are specified by the
following tags:
Tag

Description

Occurren
ce

<EQUIPMENT_NAME>

The Equipment Name that triggered the Automatic creation of NonConformance on Work Order Operation.

Mandator
y

<TIMESTAMP>

The Timestamp of the Automatic creation of Non-Conformance on
Work Order Operation.

Optional

The timestamp must respect the UTC format: for example, yyyy-MMddThh:mm:ssZ.
<CATEGORY>

The Operation/Step Category of the Work Order Operation on which
the Non-Conformance is created.

Mandator
y

<DEFECT_TYPE>

The list of Defect Types/Failures associated to the Non-Conformance.

Optional

<SEVERITY>

The Severity of the Non-Conformance.

Optional

Tag

Description

Occurren
ce

<NOTE>

Notes associated to the Non-Conformance.

Optional

##### Quality Non-Conformance Creation on Material Tracking Units

The use case allows you to trigger the automatic creation of a Quality Non-Conformance on Material Tracking Units
by Machines or Workcenters.
The creation of the Non-Conformance will be traced as performed by "" (blank space indicating "no user").
It is then possible to associate the Non-Conformance to a Work Order Operation: for this reason, the Work Order
Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Operation and the
involved Machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Automatic Creation of Non-Conformance on Material Tracking
Units message
Here is an example of an XML message that can be used to trigger an Automatic Creation of Non-Conformance on
Material Tracking Units:
Export File
<?xml version="1.0" encoding="utf-8"?>
<OPEN_NC_ON_PRODUCT>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<TIMESTAMP>2018-10-27T16:15:00Z</TIMESTAMP>
<CATEGORY>Standard</CATEGORY>
<PRODUCT ID="sn001"/>
<PRODUCT ID="sn002"/>
<DEFECT_TYPE>Scratch</DEFECT_TYPE>
<DEFECT_TYPE>Bump</DEFECT_TYPE>
<SEVERITY>High</SEVERITY>
<NOTE>Notes</NOTE>
</OPEN_NC_ON_PRODUCT>

Here is the XSD that describes and validates the Automatic Creation of Non-Conformance on Material Tracking
Units XML message:

XSD
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="OPEN_NC_ON_PRODUCT">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="CATEGORY" maxOccurs="1" minOccurs="1"/>
<xs:element name="PRODUCT ID" maxOccurs="unbounded" minOccurs="1">
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="ID" use="required"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
<xs:element type="xs:string" name="DEFECT_TYPE" maxOccurs="unbounded"
minOccurs="0"/>
<xs:element type="xs:string" name="SEVERITY" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="NOTES" maxOccurs="1" minOccurs="0"/>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <OPEN_NC_ON_PRODUCT> tag specifies that the scope of the message is to define an Automatic Creation of
Non-Conformance on Material Tracking Units.
The attributes of an Automatic Creation of Non-Conformance on Material Tracking Units are specified by the
following tags:
Tag

Description

Occurrence

<EQUIPMENT_NAME>

The Equipment Name that triggered the Automatic Creation of
Non-Conformance on Material Tracking Units.

Mandatory

<TIMESTAMP>

The Timestamp of the Automatic Creation of Non-Conformance
on Material Tracking Units.

Optional

The timestamp must respect the UTC format: for example, yyyyMM-ddThh:mm:ssZ.
<CATEGORY>

The Operation/Step Category of the Work Order Operation to
which the Non-Conformance is optionally associated.

Optional

Tag

Description

Occurrence

<PRODUCT ID>

The list of Material Tracking Units on which the NonConformance is created.

Mandatory

The related Material Tracking Units are described by the ID
attribute that defines BatchId or SerialNumberCode of the Material
Tracking Unit on which the Non-Conformance is created.
<DEFECT_TYPE>

The list of Defect Types/Failures associated to the NonConformance.

Optional

<SEVERITY>

The Severity of the Non-Conformance.

Optional

<NOTE>

Notes associated to the Non-Conformance.

Optional

##### Quality Non-Conformance Creation on Machines

The use case allows you to trigger the automatic creation of a Non-Conformance of type Quality on Machines by
Machines or Workcenters.
The creation of the Non-Conformance will be traced as performed by "" (blank space indicating "no user").
It is then possible to associate the Non-Conformance to a Work Order Operation: for this reason, the Work Order
Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Operation and the
involved Machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Automatic Creation of Non-Conformance on Machine message
Here is an example of an XML message that can be used to trigger an Automatic Creation of Non-Conformance on
Machine:
Export File
<?xml version="1.0" encoding="utf-8"?>
<OPEN_NC_ON_EQUIPMENT>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<TIMESTAMP>2018-10-27T16:15:00Z</TIMESTAMP>
<DEFECT_TYPE>Scratch</DEFECT_TYPE>
<DEFECT_TYPE>Bump</DEFECT_TYPE>
<SEVERITY>High</SEVERITY>
<NOTE>Notes</NOTE>
</OPEN_NC_ON_EQUIPMENT>

Here is the XSD that describes and validates the Automatic Creation of Non-Conformance on Machine XML
message:
XSD
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="OPEN_NC_ON_EQUIPMENT">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="DEFECT_TYPE" maxOccurs="unbounded"
minOccurs="0"/>
<xs:element type="xs:string" name="SEVERITY" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="NOTES" maxOccurs="1" minOccurs="0"/>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <OPEN_NC_ON_EQUIPMENT> tag specifies that the scope of the message is to define an Automatic Creation
of Non-Conformance on Machine.
The attributes of an Automatic Creation of Non-Conformance on Machine are specified by the following tags:
Tag

Description

Occurrence

<EQUIPMENT_NAME>

The Equipment Name that triggered the Automatic Creation of
Non-Conformance on Machine and the Machine on which the NonConformance is created.

Mandatory

<TIMESTAMP>

The Timestamp of the Automatic Creation of Non-Conformance
on Machine.

Optional

The timestamp must respect the UTC format: for example, yyyyMM-ddThh:mm:ssZ.
<DEFECT_TYPE>

The list of Defect Types/Failures associated to the NonConformance.

Optional

<SEVERITY>

The Severity of the Non-Conformance.

Optional

<NOTE>

Notes associated to the Non-Conformance.

Optional

##### Quality Non-Conformance Sentencing

The use case allows you to trigger the automatic sentencing of a Quality Non-Conformance by Machines or
Workcenters.
Automatic sentencing can be performed on both total and partial quantities: however, just as for manual
sentencing, partial sentencing is permitted solely for contexts related to Work Order Operations. Depending on the
Work Order Production Type, the Material Tracking Units may or may not need to be specified.
The sentencing of the Non-Conformance will be traced as performed by "" (blank space indicating "no user").
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Automatic Sentencing message
Here is an example of an XML message that can be used to trigger an Automatic Sentencing:
Export File
<?xml version="1.0" encoding="utf-8"?>
<SENTENCE_NC>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<NC_NID>NCP_2018_14</NC_NID>
<TIMESTAMP>2018-07-28T16:15:00Z</TIMESTAMP>
<TARGET_STATUS>CLOSE AND RETURN TO WORK</TARGET_STATUS>
<QTY>2</QTY>
<PRODUCT ID="SNInjector45083" />
<PRODUCT ID="SNInjector45084" />
</SENTENCE_NC>

Here is the XSD that describes and validates the Automatic Sentencing XML message:
XSD
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="SENTENCE_NC">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:string" name="NC_NID" maxOccurs="1" minOccurs="1"/>
<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element type="xs:string" name="TARGET_STATUS" maxOccurs="1" minOccurs="1"
/>
<xs:element type="xs:int" name="QTY" maxOccurs="1" minOccurs="0"/>
<xs:element name="PRODUCT" maxOccurs="unbounded" minOccurs="0">

<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="ID" use="required"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <SENTENCE_NC> tag specifies that the scope of the message is to define an Automatic Sentencing.
The attributes of an Automatic Sentencing are specified by the following tags:
Tag

Description

Occurrence

<EQUIPMENT_NAME>

The Equipment Name that triggered the Automatic
Sentencing.

Mandatory

<TIMESTAMP>

The Timestamp of the Automatic Sentencing.

Optional

The timestamp must respect the UTC format: for example, yyyyMM-ddThh:mm:ssZ.
<NC_NID>

The Natural Identifier of the Non-Conformance that is
sentenced.

Mandatory

<TARGET_STATUS>

The next Status of the Non-Conformance that is sentenced.

Mandatory

<QTY>

If present, the quantity of the Batch or SerialNumber that is
sentenced with the current action.
It will contribute to defining whether the sentencing is going to
be total or partial.

Optional

<PRODUCT>

The list of Material Tracking Units on which the Automatic
Sentencing takes place. The related Material Tracking Units are
described by the ID attribute, representing the BatchId or
SerialNumberCode of the Material Tracking Unit on which the
Automatic Sentencing takes place.

Optional

##### Material Consumption

The use case allows you to trigger the automatic consumption of Materials by Machines or Workcenters for Work
Order Operations and for Work Order Steps.
As the consumption of Materials will be done by Machines automatically, no user entries are traced.

The Work Order Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Order
Operation type and the involved machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it, by creating an XML structured as the example provided below.

XML structure of an Automatic Material Consumption
Here is an example of XML message to be used to describe an Automatic Material Consumption:
Export File
<CONSUME_MI>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<CATEGORY>Standard</CATEGORY>
<TIMESTAMP>2018-07-28T16:15:00Z</TIMESTAMP>
<PRODUCT ID="sn001">
<TOBECONSUMED MATDEFID="TEST" ID="tbcsn00a" QTY="10" LOGICALPOS="X1"/>
<TOBECONSUMED QTY="20" LOGICALPOS="X2"/>
<TOBECONSUMED ID="tbcsn00c" LOGICALPOS="X3"/>
<TOBECONSUMED ID="tbcsn00d" QTY="40" />
</PRODUCT>
<PRODUCT ID="sn002">
<TOBECONSUMED ID="tbcsn00e" QTY="50" LOGICALPOS="X5"/>
<TOBECONSUMED ID="tbcsn00f" QTY="60" LOGICALPOS="X6"/>
</PRODUCT>
<PRODUCT ID="sn003">
<TOBECONSUMED ID="tbcsn00g" QTY="70" LOGICALPOS="X7"/>
<TOBECONSUMED ID="tbcsn00h" QTY="80" LOGICALPOS="X8"/>
<TOBECONSUMED ID="tbcsn00i" QTY="90" LOGICALPOS="X9"/>
</PRODUCT>
<PRODUCT ID="sn004">
</PRODUCT>
</CONSUME_MI>

Here is the XSD that describes and validates the Automatic Material Consumption XML message:
XSD
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="CONSUME_MI">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:string" name="CATEGORY" maxOccurs="1" minOccurs="1"/>

<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element name="PRODUCT" maxOccurs="unbounded" minOccurs="1" >
<xs:complexType>
<xs:sequence>
<xs:element name="TOBECONSUMED" maxOccurs="unbounded" minOccurs="1" >
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="MATDEFID"/>
<xs:attribute type="xs:string" name="ID"/>
<xs:attribute type="xs:float" name="QTY"/>
<xs:attribute type="xs:string" name="LOGICALPOS"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
</xs:sequence>
<xs:attribute type="xs:string" name="ID" use="required"/>
</xs:complexType>
</xs:element>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <CONSUME_MI> tag specifies that the scope of the document is to define an Automatic Material
Consumption message.
The attributes of an Automatic Material Consumption are specified by the following tags:
Tag

Description

Occurre
nce

<EQUIPMENT_
NAME>

Defines the Equipment Name that triggered the Automatic Material
Consumption.

Mandat
ory

<CATEGORY>

This tag defines the Work Operation Type of the Work Order Operation that is
completed.

Mandat
ory

<TIMESTAMP>

Defines the time when the automatic consumption of the Material began.

Optiona

The timestamp must respect the UTC format, for example: yyyy-MMddThh:mm:ssZ.
<PRODUCT>

This tag define the list of Final Materials created during the Automatic Material
Consumption. The related Material Tracking Units are described by the following
attribute:

Mandat
ory

ID: this attribute defines BatchId or SerialNumberCode of the Material Tracking
Unit on which the Automatic Material Consumption takes place.

Tag

Description

Occurre
nce

<TOBECONSU
MED>

This tag define a Material consumed during the Automatic Material
Consumption. The attributes of the tag are as follows:

Mandat
ory

• MATDEFID: Identifier of the Material to which the Material Tracking Unit to be
assembled/consumed belongs.
• ID: Identifier of the Material Tracking Unit (Batch or Serial Number) to be
assembled/consumed.
• QTY: The quantity of the Batch or SerialNumber that is completed with the
current action.
• LOGICALPOS: Logical Position of the Material to be assembled/consumed.

##### Tool Usage

The use case allows you to trigger the automatic usage of Tools by Machines or Workcenters.
The usage of Tools will be traced as performed by "" (blank space indicating "no user").
The Work Order Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Order
Operation type and the involved machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it, by creating an XML structured as the example provided below.

XML structure of an Automatic Tool Usage
Here is an example of XML message to be used to describe an Automatic Tool Usage:
Export File
<USE_TOOL>
<EQUIPMENT_NAME>QL-Print511</EQUIPMENT_NAME>
<CATEGORY>Standard</CATEGORY>
<TIMESTAMP>2018-10-27T16:15:00Z</TIMESTAMP>
<PRODUCT ID="SN_01">
<TOOL ID="Drill" TIMESTOBEUSED="2" USAGEDURATION="1"/>
</PRODUCT>
</USE_TOOL>

Here is the XSD that describes and validates the Automatic Tool Usage XML message:

XSD
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="USE_TOOL">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME" maxOccurs="1" minOccurs="1
"/>
<xs:element type="xs:string" name="CATEGORY" maxOccurs="1" minOccurs="1"/>
<xs:element type="xs:dateTime" name="TIMESTAMP" maxOccurs="1" minOccurs="0"/>
<xs:element name="PRODUCT" maxOccurs="unbounded" minOccurs="1" >
<xs:complexType>
<xs:sequence>
<xs:element name="TOOL" maxOccurs="unbounded" minOccurs="1" >
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="ID" use="required"/>
<xs:attribute type="xs:float" name="TIMESTOBEUSED" use="require
d"/>
<xs:attribute type="xs:byte" name="USAGEDURATION" use="required
"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
</xs:sequence>
<xs:attribute type="xs:string" name="ID" use="required"/>
</xs:complexType>
</xs:element>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <USE_TOOL> tag specifies that the scope of the document is to define an Automatic Tool Usage message.
The attributes of an Automatic Tool Usage are specified by the following tags:
Tag

Description

Occurre
nce

<EQUIPMENT_
NAME>

Defines the Equipment Name that triggered the Automatic Complete.

Mandat
ory

<CATEGORY>

This tag defines the Work Operation Type of the Work Order Operation that is
completed.

Mandat
ory

Tag

Description

Occurre
nce

<TIMESTAMP>

Defines the Actual End Time of the Work Order Operation.

Optiona

The timestamp must respect the UTC format, for example: yyyy-MMddThh:mm:ssZ.
<PRODUCT>

This tag define the list of Material Tracking Units on which the Automatic Tool
Usage takes place. The related Material Tracking Units are described by the
following attribute:

Mandat
ory

ID: this attribute defines BatchId or SerialNumberCode of the Material Tracking
Unit on which the Automatic Tool Usage takes place.
<TOOL>

This tag defines the list of Tools to be automatically used. The Tools are
described by the following attributes:

Mandat
ory

• ID: Identifier of the Tool.
• TIMESTOBEUSED: Number of times a Tool can be used.
• USAGEDURATION: duration for which a Tool can be used.

##### Data Collection

The use case allows you to trigger the automatic collection of data by Machines or Workcenters.
The Work Order Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Order
Operation type and the involved machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it, by creating an XML structured as the example provided below.

XML structure of an Automatic Collect Data
Here is an example of XML message to be used to describe an Automatic Collect Data:
Export File
<DCD_ACQUIRE>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<CATEGORY>STANDARD</CATEGORY>
<PRODUCT ID="SN_01" QTY="1"/>
<PRODUCT ID="SN_02" QTY="2"/>
<PARAMETER NAME="Temperature" VALUE="44C"/>
<PARAMETER NAME="changeDrillBit" VALUE="true"/>
</DCD_ACQUIRE>

Here is the XSD that describes and validates the Automatic Collect Data XML message:

XSD
xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:element name="DCD_ACQUIRE">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME"/>
<xs:element type="xs:string" name="WOO_TYPE"/>
<xs:element name="PRODUCT" maxOccurs="unbounded" minOccurs="1">
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="ID" use="required"/>
<xs:attribute type="xs:float" name="QTY" use="optional"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
<xs:element name="PARAMETER" maxOccurs="unbounded" minOccurs="1">
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="NAME" use="required"/>
<xs:attribute type="xs:string" name="VALUE" use="required"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <DCD_ACQUIRE> tag specifies that the scope of the document is to define an Automatic Collect
Data message.
The attributes of an Automatic Collect Data are specified by the following tags:
Tag

Description

Occurre
nce

<EQUIPMENT_
NAME>

Defines the Equipment Name that triggered the Automatic Collect Data.

Mandat
ory

<CATEGORY>

Defines the Work Operation Step Category of the Work Order Operation that
triggered the Automatic Collect Data.

Mandat
ory

Tag

Description

Occurre
nce

<PRODUCT>

Defines the list of Material Tracking Units on which the Automatic Collect Data
takes place. The related Material Tracking Units are described by the following
attribute:

Mandat
ory

ID: this attribute defines BatchId or SerialNumberCode of the Material Tracking
Unit on which the Automatic Collect Data takes place.
<PARAMETER>

Identifies the list of parameters to be automatically collected. The parameters
are described by the following attributes:

Mandat
ory

• NAME: name of the parameter that will be automatically collected and that is
used to perform the binding with the Data Collection field.
• VALUE: value of the parameter that will be automatically collected.

##### Quality Inspection Data Acquisition

The use case allows you to trigger the automatic collection of quality inspection data by Machines or Workcenters.
The Work Order Operation NId must not be explicitly specified because it is retrieved on the basis of the Work Order
Operation type and the involved machine.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it, by creating an XML structured as the example provided below.
Automatic Quality Non-Conformance Generation on MTUs and Quality Inspections
This XML also permits the automatic generation of a Quality Non-Conformance when a Failure is detected
on an MTU during an Attributive or Variable Quality Inspection: this requires that parameter FAILURE must
be set. See the table in the section below.

XML structure of an Automatic Quality Inspection Data Acquire
Here is an example of XML message to be used to describe an Automatic Quality Inspection Data Acquire.
Export File
<QI_ACQUIRE>
<EQUIPMENT_NAME>DrillingMachine</EQUIPMENT_NAME>
<CATEGORY>STANDARD</CATEGORY>
<PRODUCT ID="SN_01" QTY="1"/>
<PRODUCT ID="SN_02" QTY="2"/>
<PARAMETER NAME="VarChar_01" VALUE="44"/>

<PARAMETER NAME="VarAttributive" VALUE="false" FAILURE= "Scratch"/>
</QI_ACQUIRE>

Here is the XSD that describes and validates the Automatic Quality Inspection Data Acquire XML message:
XSD
xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:element name="QI_ACQUIRE">
<xs:complexType>
<xs:sequence>
<xs:element type="xs:string" name="EQUIPMENT_NAME"/>
<xs:element type="xs:string" name="CATEGORY"/>
<xs:element name="PRODUCT" maxOccurs="unbounded" minOccurs="0">
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="ID" use="required"/>
</xs:extension>
</xs:simpleContent>
</xs:complexType>
</xs:element>
<xs:element name="PARAMETER" maxOccurs="unbounded" minOccurs="0">
<xs:complexType>
<xs:simpleContent>
<xs:extension base="xs:string">
<xs:attribute type="xs:string" name="NAME" use="required"/>
<xs:attribute type="xs:string" name="VALUE" use="required"/>
<xs:attribute type="xs:string" name="FAILURE" use="optional"/>
</xs:extension>
</simpleContent>
</xs:complexType>
</xs:element>
</xs:sequence>
</xs:complexType>
</xs:element>
</xs:schema>

The <QI_ACQUIRE> tag specifies that the scope of the document is to define an Automatic Quality Inspection
Data Acquisition message.
The attributes of an Automatic Quality Inspection Data Acquire are specified by the following tags:
Tag

Description

Occurre
nce

<EQUIPMENT_
NAME>

Defines the Equipment Name that triggered the Automatic Quality Inspection
Data Acquire.

Mandat
ory

Tag

Description

Occurre
nce

<CATEGORY>

This tag defines the Work Operation Step Category of the Work Order
Operation that triggered the Automatic Quality Inspection Data Acquire.

Mandat
ory

<PRODUCT>

This tag defines the list of Material Tracking Units on which the Automatic
Quality Inspection Data Acquire takes place. The related Material Tracking Units
are described by the following attribute:

Optiona

ID: this attribute defines BatchId or SerialNumberCode of the Material Tracking
Unit on which the Automatic Quality Inspection Data Acquire takes place.
If the ID tag is not specified, Automatic Quality Inspection Data
Acquire is applied to all the Active Material Tracking Units.

<PARAMETER>

This tag identifies the list of parameters to be automatically collected. The
parameters are described by the following attributes:

Mandat
ory

• NAME: name of the parameter.
• VALUE: value of the parameter that will be automatically collected.
• FAILURE: identifier of the Failure.

##### Input Message related to Kanban Call

The use case allows you to trigger messages from the warehouse to receive notifications on the status of a given
Kanban call.
The use case is driven by a message exchange between Opcenter CN MOM and Opcenter EX DS.
The exchanged message is an XML file.
Once you have imported the integration scenario configuration and properly configured the MOM Connection, you
will be able to verify it by creating an XML structured as indicated in the example below.

XML structure of an Input Message
Here is an example of an XML message that can be used to trigger an Input Message:
Export File
<?xml version="1.0" encoding="utf-8"?>
<MESSAGE MSG_TYPE="KanbanMessage" MESSAGE_SCHEMA="KanbanInputMessageXSDv1.0" >
<HEADER>
<MESSAGE_INFO ID="KANBANMsg-2021-09-00000008" TYPE="New"
TRANSMISSION_TIMESTAMP="5/3/2020 1:25:43 PM +00:00" />
<MESSAGE_SENDER SENDER_ID="WHS_01" />
</HEADER>

<KANBAN_CALL KANBANID="8da05c09-a558-44db-bae9-b7f9c6ea5333" PRIORITY="2"
DELIVERED_QTY="22" DELIVERED_UOM="U" DELIVERY_POINT="LSP7" STATUS="Delivered"/>
</MESSAGE>

Here is the XSD that describes and validates the Input Message XML message:
XSD
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="
http://www.w3.org/2001/XMLSchema">
<xs:element name="MESSAGE">
<xs:complexType>
<xs:sequence>
<xs:element name="HEADER" minOccurs="1" maxOccurs="1">
<xs:complexType>
<xs:sequence>
<xs:element name="MESSAGE_INFO" minOccurs="1" maxOccurs="1">
<xs:complexType>
<xs:attribute name="ID" type="xs:string" use="required" />
<xs:attribute name="TYPE" type="xs:string" use="required" />
<xs:attribute name="TRANSMISSION_TIMESTAMP" type="xs:string" use="r
equired" />
</xs:complexType>
</xs:element>
<xs:element name="MESSAGE_SENDER" minOccurs="1" maxOccurs="1">
<xs:complexType>
<xs:attribute name="SENDER_ID" type="xs:string" use="required" />
</xs:complexType>
</xs:element>
</xs:sequence>
</xs:complexType>
</xs:element>
<xs:element name="KANBAN_CALL" minOccurs="1" maxOccurs="1">
<xs:complexType>
<xs:attribute name="KANBANID" type="xs:string" use="required" />
<xs:attribute name="PRIORITY" type="xs:integer" use="required" />
<xs:attribute name="DELIVERED_QTY" type="xs:decimal" use="required" />
<xs:attribute name="DELIVERED_UOM" type="xs:string" use="required" />
<xs:attribute name="DELIVERY_POINT" type="xs:string" use="required" />
<xs:attribute name="STATUS" type="xs:string" use="required" />
</xs:complexType>
</xs:element>
</xs:sequence>
<xs:attribute name="MSG_TYPE" type="xs:string" use="required" />
<xs:attribute name="MESSAGE_SCHEMA" type="xs:string" use="required" />
</xs:complexType>
</xs:element>
</xs:schema>

The <MESSAGE> tag specifies that the scope of the message is to define an Input Message.
The attributes of an Input Message are specified by the following tags:

Tag

Description

Occurrence

<HEADER>

Contains context information related to the response sent from
the warehouse to the Kanban call.

Mandatory

<MESSAGE_INFO>

Defines the unique identifier of the message, its type (either
New, if it is sent for the first time, or Duplicated) and its
timestamp.

Mandatory

<MESSAGE_SENDER>

Identifies the warehouse that sent the message.

Mandatory

<KANBAN_CALL>

Contains information on the Kanban call for which the message
was generated, in details:

Mandatory

• KANBANID, the identifier of the Kanban call.
• PRIORITY, the priority of the message.
• DELIVERED_QTY, the material quantity (expressed
according to the related UoM and not in Bins) that has been
sent to the DELIVERY_POINT.
• DELIVERED_UOM, the Unit of Measure of the material
quantity.
• DELIVERY_POINT, the Line Side Position where the Material
will be delivered.
• STATUS, the status of the Kanban Call (InProgress, Shipped,
Delivered or Cancelled).

##### How to Configure Direct Dispatch for Messages Exchanged with the Shop Floor

Up to Opcenter Connect MOM 2304, the Direct Dispatch was implemented by changing the inbound Message Type
and using EX FN as Direct Dispatch Type. This procedure is now deprecated. Here below the set of objects that must
be created or changed in order to achieve the same result by adopting the Web API Client Adapter.

Workflow
1. Create a Web API Client Adapter with the connection to Opcenter Execution Foundation.
2. Modify the Message Type in order to set the Direct Dispatch of Type Adapter as the main one: then adjust some
configurations for it.
3. Modify the Message Response Type name to "reply"<Message Type>. It will be seen as a new Message Type.
4. Add the new Message Response Type to the UADMAutomaticShopFloorChannel Message Channel Valid
Message Types list.
The source adapter (that is, the out-of-the-box File Adapter) must not be modified, as the destination Adapter (that
is, the Web API Client Adapter) is configured in the Message Type.
For more information on how to configure the aforementioned objects, please refer to chapter Use Case Configuration for EX FN in the Opcenter Connect MOM User Guide.
The Message flow that employs the Web API Client Adapter will be from the originally-used adapter (the out-of-thebox File Adapter) to the Web API Client adapter, which invokes Opcenter Execution Foundation and sends the

response back to the original adapter. Here is an example of the message flow considering the File Adapter as
provided out-of-the-box.

Given that the Opcenter Execution Foundation URL is stored in the Web API Client Adapter, and the Web
API Client Adapter to be used is already specified in the Message Type, it is not possible to address more
than one plant at the same time.

#### How to Automatically Import and Delete Data

Instead of creating items one by one from Opcenter Execution Discrete UI Application, you can choose to
automatically import data from external systems. This operation is driven by the exchange of properly formatted
XML files or JSON files between Opcenter Connect MOM and Opcenter Execution Discrete.
The JSON format is currently supported only for the FullWorkOrder data flow.
By default the system provides a set of Data Flows to be used to import specific data types, but you may have
defined additional data flows to satisfy your needs. The table below lists the out-of-the-box Data Flows configured
in the system:
Import Data Flow

Available in solutions

If not available, install the following
Extension App

Materials

• U4DM
• OnePieceFlow

ImportPRC

Functional Codes

• U4DM
• OnePieceFlow

ImportPRC

Suppliers

• U4DM
• OnePieceFlow

ImportPRC

Features, Feature Values,
Options

• U4DM
• OnePieceFlow

ImportPRC

Bills of Features

• U4DM
• OnePieceFlow

ImportPRC

Import Data Flow

Available in solutions

If not available, install the following
Extension App

Bills of Materials

• U4DM
• OnePieceFlow

ImportPRC

ERP Orders

• U4DM
• OnePieceFlow

ImportERP

Master Plans

• U4DM
• OnePieceFlow
• DS
• DS4AM

ImportBOP

Inspection Master Plan

• U4DM
• OnePieceFlow
• DS
• DS4AM

ImportCHR

Work Orders

• U4DM
• OnePieceFlow
• DS
• DS4AM

ImportWO

Full Work Orders

• U4DM
• OnePieceFlow
• DS
• DS4AM

ImportWO

Workflow
1. If necessary, create a custom data flow.
2. Create the XML files containing data to be imported. If you want to use one of the data flows provided by the
system, you must create the XML file according to one of the following templates:
• Materials
• Functional Codes
• Suppliers
• Features, Feature Values, Options
• Bills of Features
• Bills of Materials
• ERP Orders
• Master Plans
• Inspection Master Plan
• Work Orders (from Master Plans or As Planned BOPs)
• Full Work Orders (full Work Order structure with related Work Order Operation and Work Order Step
data).
3. From %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Xslt, copy the .xslt files in the C:\XSLT folder
of the Opcenter Connect MOM machine. They are used by Opcenter Connect MOM to verify if the XML file
contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files,

one containing the correct nodes that can be successfully imported, and one containing the wrong nodes that
must be logged. If you want to use a custom data flow, create in the same folder the EntityName.xslt file.
In the folder %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Xslt, also the
MapFullWorkOrder.xslt file is available. It is used by Opcenter Connect MOM to properly map the deserialized JSON file into the corresponding XML file.
4. Copy the XML file in the proper folder set while defining the File Adapter.
5. Verify that the configuration works properly.

##### XML File for Materials

It is possible to automatically align the Materials contained in the Opcenter Execution Discrete database with those
available in the External System. This operation can be performed through an XML file created according to the
structure below.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="MTMD" Plant="PLT01">
<Define>
<Material NId="ME-07135491500" Name="FRONT STEM REAR SUSPENSION" Description="
FRONT STEM REAR SUSPENSION" FunctionalCodeNId="FC01" UoMNId="Unit">
<Supplier SupplierNId = "SUPA400"/>
</Material>
<Material NId="ME-09135491500" Name="REAR STEM REAR SUSPENSION" Description="
REAR STEM REAR SUSPENSION" FunctionalCodeNId="FC02" UoMNId="Unit">
<Supplier SupplierNId = "SUPA120"/>
</Material>
<Material NId="ME-07972465370" Name="AUTO-GEARBOX CONTROL COMPLETE DEVICE"
Description="AUTO-GEARBOX CONTROL COMPLETE DEVICE" FunctionalCodeNId="FC04" UoMNId="U
nit">
<Supplier SupplierNId = "SUPA210"/>
</Material>
<Material NId="ME-05539265370" Name="" Description="0" FunctionalCodeNId="FC0
4" UoMNId="Unit">
<Supplier SupplierNId = "SUPA030"/>
</Material>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
MTMD (Material Master Data) data flow provided by the system and relative to a specific plant (PLT01) among
those that have been configured.
• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a
Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.

• All Materials to be imported into Opcenter Execution Discrete must be listed within the <Define> tag with the
following attributes:
• NId
• Name
• FunctionalCode
• UoM
• Supplier
• All previously imported Materials that are no more available in the External System and consequently must be
removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the <Define>
tag, specifying the related Identifiers (NId attribute).

XSLT Transformation
The Opcenter Connect MOM workflow uses the DM_Material.xslt file to verify if the XML file described above
contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>
<!-- Log Invalid Data -->
<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="Material[not(@NId) or @NId='' or
not(@Name) or @Name='' or ((not(@MaterialGroup) or @MaterialGroup='') and
(not(@FunctionalCodeNId) or @FunctionalCodeNId='')) or not(@UoMNId) or @UoMNId='' or
count(Supplier[not(@SupplierNId)]) > 0 or count(Supplier[@SupplierNId = '']) > 0]"
mode="error" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="Material[not(@NId) or @NId='']" />
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
<!-- Import Valid Data -->
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">

<xsl:apply-templates select="Material[(@NId) and @NId!='' and
(@Name) and @Name!='' and (((@MaterialGroup) and @MaterialGroup!='') or
((@FunctionalCodeNId) and @FunctionalCodeNId!='')) and (@UoMNId) and @UoMNId!='' and
count(Supplier[not(@SupplierNId)]) = 0 and count(Supplier[@SupplierNId= '']) = 0]"
mode="import" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="Material[(@NId) and @NId!='']" />
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
</CamstarCompoundMessage>
</xsl:template>
<!-- Define -->
<xsl:template match="ImportDataFlow/Define/Material" mode="error">
<xsl:if test="not(@NId) or (@NId='')">
<Material>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Material"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</Material>
</xsl:if>
<xsl:if test="not(@Name) or (@Name='')">
<Material>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12220">
<Parameters>
<Par key="Entity" value="Material"></Par>
<Par key="Property" value="Name"></Par>
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="not(@Name) or (@Name='')">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</Material>
</xsl:if>
<xsl:if test="(not(@MaterialGroup) or (@MaterialGroup='')) and
(not(@FunctionalCodeNId) or (@FunctionalCodeNId=''))">
<Material>
<xsl:copy-of select="@*[string(.)]" />

<Error Id="12220">
<Parameters>
<Par key="Entity" value="Material"></Par>
<Par key="Property" value="MaterialGroup/FunctionalCodeNId"></Par>
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="(not(@MaterialGroup) or (@MaterialGroup='')) and
(not(@FunctionalCodeNId) or (@FunctionalCodeNId=''))">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</Material>
</xsl:if>
<xsl:if test="not(@UoMNId) or (@UoMNId='')">
<Material>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12220">
<Parameters>
<Par key="Entity" value="Material"></Par>
<Par key="Property" value="UoMNId"></Par>
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="not(@UoMNId) or (@UoMNId='')">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</Material>
</xsl:if>
<xsl:for-each select="./Supplier">
<xsl:if test="not(@SupplierNId) or @SupplierNId =''">
<Material>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="SUPPLIER"></Par>
<Par key="Property" value="Supplier.SupplierNId"></Par>
</Parameters>
</Error>
</Material>
</xsl:if>
</xsl:for-each>
</xsl:template>
<xsl:template match="ImportDataFlow/Define/Material" mode="import">

<xsl:copy-of select="." />
</xsl:template>
<!-- Remove -->
<xsl:template match="ImportDataFlow/Remove/Material">
<xsl:if test="not(@NId) or @NId=''">
<Material>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Material"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</Material>
</xsl:if>
<xsl:if test="(@NId) and @NId!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
</xsl:stylesheet>

##### XML File for Functional Codes

It is possible to automatically align the Functional Codes contained in the Opcenter Execution Discrete database
with those available in the External System. This operation can be performed through an XML file created according
to the structure below.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="FCMD" Plant="PLT01">
<Define>
<FunctionalCode NId="FC01" Name="FUNCT_AREA_01" Description="GROUPING
MATERIALS 01"/>
<FunctionalCode NId="FC02" Name="FUNCT_AREA_02" Description="GROUPING
MATERIALS 02"/>
<FunctionalCode NId="FC03" Name="FUNCT_AREA_03" Description="GROUPING
MATERIALS 03"/>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
FCMD (Functional Code Master Data) data flow provided by the system and relative to a specific plant (PLT01)
among those that have been configured.
• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a
Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.
• All Functional Codes to be imported into Opcenter Execution Discretemust be listed within the <Define> tag
with the following attributes:

• NId
• Name
• Description
• All previously imported Functional Codes that are no more available in the External System and consequently
must be removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the
<Define> tag, specifying the related Identifiers (NId attribute).

XSLT Transformation
The Opcenter Connect MOM workflow uses the Functionalcode.xslt file to verify if the XML file described above
contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>
<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="FunctionalCode[not(@NId) or @NId='' or
not(@Name) or @Name='']"/>
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="FunctionalCode[not(@NId) or @NId='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="FunctionalCode[(@NId) and @NId!='' and
(@Name) and @Name!='']"/>
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="FunctionalCode[(@NId) and @NId!='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>

</CamstarCompoundMessage>
</xsl:template>
<xsl:template match="ImportDataFlow/Define/FunctionalCode">
<xsl:choose>
<xsl:when test="not(@NId) or @NId=''">
<FunctionalCode>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="FunctionalCode"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</FunctionalCode>
</xsl:when>
<xsl:when test="not(@Name) or @Name=''">
<FunctionalCode>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="FunctionalCode"></Par>
<Par key="Property" value="Name"></Par>
</Parameters>
</Error>
</FunctionalCode>
</xsl:when>
</xsl:choose>
<xsl:if test="(@NId) and @NId!='' and (@Name) and @Name!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
<xsl:template match="ImportDataFlow/Remove/FunctionalCode">
<xsl:if test="not(@NId) or @NId=''">
<FunctionalCode>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="FunctionalCode"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</FunctionalCode>
</xsl:if>
<xsl:if test="(@NId) and @NId!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
</xsl:stylesheet>

##### XML File for Suppliers

It is possible to automatically align the Suppliers contained in the Opcenter Execution Discrete database with those
available in the External System. This operation can be performed through an XML file created according to the
structure below.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="SUPMD" Plant="PLT01">
<Define>
<Supplier NId="SUPA400" Name="TOR400" Description="TOR-SUP400"/>
<Supplier NId="SUPA120" Name="TOR120" Description="TOR-SUP120"/>
<Supplier NId="SUPA700" Name="TOR700" Description="TOR-SUP700"/>
<Supplier NId="SUPA210" Name="TOR210" Description="TOR-SUP210"/>
<Supplier NId="SUPA030" Name="TOR030" Description="TOR-SUP030"/>
<Supplier NId="SUPA040" Name="TOR040" Description="TOR-SUP040"/>
<Supplier NId="SUPA560" Name="TOR560" Description="TOR-SUP560"/>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
SUPMD (Supplier Master Data) data flow provided by the system and relative to a specific plant (PLT01) among
those that have been configured.
• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a
Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.
• All Suppliers to be imported into Opcenter Execution Discrete must be listed within the <Define> tag with the
following attributes:
• NId
• Name
• Description
• All previously imported Suppliers that are no more available in the External System and consequently must be
removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the <Define>
tag, specifying the related Identifiers (NId attribute).

XSLT Transformation
The Opcenter Connect MOM workflow uses the Supplier.xslt file to verify if the XML file described above contains
logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>

<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="Supplier[not(@NId) or @NId='' or
not(@Name) or @Name='']"/>
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="Supplier[not(@NId) or @NId='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="Supplier[(@NId) and @NId!='' and (@Name)
and @Name!='']"/>
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="Supplier[(@NId) and @NId!='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
</CamstarCompoundMessage>
</xsl:template>
<xsl:template match="ImportDataFlow/Define/Supplier">
<xsl:choose>
<xsl:when test="not(@NId) or @NId=''">
<Supplier>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Supplier"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</Supplier>
</xsl:when>
<xsl:when test="not(@Name) or @Name=''">
<Supplier>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Supplier"></Par>

<Par key="Property" value="Name"></Par>
</Parameters>
</Error>
</Supplier>
</xsl:when>
</xsl:choose>
<xsl:if test="(@NId) and @NId!='' and (@Name) and @Name!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
<xsl:template match="ImportDataFlow/Remove/Supplier">
<xsl:if test="not(@NId) or @NId=''">
<Supplier>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12250">
<Parameters>
<Par key="Entity" value="Supplier"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</Supplier>
</xsl:if>
<xsl:if test="(@NId) and @NId!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
</xsl:stylesheet>

##### XML File for Features Feature Values and Options

It is possible to automatically align the Features, Feature Values and Options contained in the Opcenter Execution
Discrete database with those available in the External System. This operation can be performed through an XML file
created according to the structure below.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="FEATMD" Plant="PLT01">
<Define>
<Feature NId="F000_MDL" Name="MODEL CODE" Description="MODEL CODE" IsOption="
False">
<FeatureValue NId="F000_001" Name="GRANADIER XR" Description="GRANADIER
XR"/>
<FeatureValue NId="F000_002" Name="GRANADIER XS" Description="GRANADIER
XS"/>
</Feature>
<Feature NId="F020_BDY" Name="BODY TYPE" Description="BODY TYPE" IsOption="Fa
lse">
<FeatureValue NId="F020_001" Name="SHORT CR" Description="Short Body
Closed Roof"/>

<FeatureValue NId="F020_002" Name="LONG CR" Description="Long Body Closed
Roof"/>
<FeatureValue NId="F020_011" Name="SHORT OR" Description="Short Body Open
Roof"/>
<FeatureValue NId="F020_012" Name="LONG OR" Description="Long Body Open
Roof"/>
</Feature>
<Feature NId="OPTN_PRY" Name="AW 18 _ 5 SPOKE" Description="18 x 8J '5_alloy
wheels" IsOption="True"/>
<Feature NId="OPTN_9ZW" Name="STORAGE PACK" Description="Storage pack"
IsOption="True"/>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
FEATMD (Feature Master Data) data flow provided by the system and relative to a specific plant (PLT01) among
those that have been configured.
• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a
Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.
• All Features, Feature Values and Options to be imported into Opcenter Execution Discrete must be listed within
the <Define> tag with the following attributes:
• NId
• Name
• Description
• All previously imported Features, Feature Values and Options that are no more available in the External System
and consequently must be removed fromOpcenter Execution Discrete, must be listed within the <Remove> tag,
instead of the <Define> tag, specifying the related Identifiers (NId attribute).

XSLT Transformation
The Opcenter Connect MOM workflow uses the Feature.xslt file to verify if the XML file described above contains
logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>
<!-- Log Invalid Data -->
<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="Feature[not(@NId) or @NId='' or

not(@Name) or @Name='' or
(@IsOption='True' and
(count(FeatureValue[(@NId)]) > 0 or count(FeatureValue[@NId != '']) > 0
or count(FeatureValue[(@Name)]) > 0 or count(FeatureValue[@Name != ''])
> 0)) or
((@IsOption='False' or not(@IsOption)) and
(count(FeatureValue[not(@NId)]) > 0 or count(FeatureValue[@NId = '']) >
0
or count(FeatureValue[not(@Name)]) > 0 or count(FeatureValue[@Name =
'']) > 0))]" mode="error" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="Feature[not(@NId) or @NId='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
<!-- Import Valid Data -->
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="Feature[(@NId) and @NId!='' and
(@Name) and @Name!='' and
((@IsOption='False' or not(@IsOption)) and
(count(FeatureValue[not(@NId)]) = 0 and count(FeatureValue[@NId = ''])
= 0
and count(FeatureValue[not(@Name)]) = 0 and count(FeatureValue[@Name =
'']) = 0)) or
(@IsOption='True' and
(count(FeatureValue[(@NId)]) = 0 and count(FeatureValue[@NId != '']) =
0
and count(FeatureValue[(@Name)]) = 0 and count(FeatureValue[@Name !=
'']) = 0))]" mode="import" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="Feature[(@NId) and @NId!='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
</CamstarCompoundMessage>
</xsl:template>
<!-- Define -->
<xsl:template match="ImportDataFlow/Define/Feature" mode="error">
<xsl:choose>
<xsl:when test="not(@NId) or @NId=''">
<Feature>

<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Feature"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</Feature>
</xsl:when>
<xsl:when test="not(@Name) or @Name=''">
<Feature>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12220">
<Parameters>
<Par key="Entity" value="Feature"></Par>
<Par key="Property" value="Name"></Par>
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="not(@Name) or @Name=''">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</Feature>
</xsl:when>
<xsl:otherwise>
<Feature>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12220">
<Parameters>
<Par key="Entity" value="Feature"></Par>
<Par key="Property" value="IsOption"></Par>
<Par key="NId">
<xsl:attribute name="value">
<xsl:value-of select="@NId" />
</xsl:attribute>
</Par>
</Parameters>
</Error>
</Feature>
</xsl:otherwise>
</xsl:choose>
</xsl:template>
<xsl:template match="ImportDataFlow/Define/Feature" mode="import">
<xsl:copy-of select="." />
</xsl:template>
<!-- Remove -->
<xsl:template match="ImportDataFlow/Remove/Feature">
<xsl:if test="not(@NId) or @NId=''">

<Feature>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Feature"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</Feature>
</xsl:if>
<xsl:if test="(@NId) and @NId!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
</xsl:stylesheet>

##### XML File for Bills of Features

It is possible to automatically align the Bills of Features contained in the Opcenter Execution Discrete database with
those available in the External System. This operation can be performed through an XML file created according to
the structure below.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="LOF" Plant="PLT01" FP_TYPE = "VHL">
<Define>
<LOF Description="GRANADIER XR LONG C-ROOF RED 2.4 DS KW140 SPORT AUS"
FP_FAMILY="GXRY21LCRRPL24DS14KSPA-4C92" >
<Feature NId="F010_MYS" ValueNId="F010_002"/>
<Feature NId="F020_BDY" ValueNId="F020_002"/>
<Feature NId="F040_EXC" ValueNId="F040_004"/>
<Feature NId="OPTN_7D3" IsOption="True"/>
<Feature NId="OPTN_8UD" IsOption="True"/>
<Feature NId="OPTN_8UM" IsOption="True"/>
</LOF>
<LOF Description="GRANADIER XR LONG C-ROOF WHT 2.4 DS KW180 BUSIN CHI"
FP_FAMILY="GXRY21LCRWML24DS18KBSC-4C92" >
<Feature NId="F000_MDL" ValueNId="F000_001"/>
<Feature NId="F010_MYS" ValueNId="F010_002"/>
<Feature NId="F100_MRK" ValueNId="F100_003"/>
<Feature NId="OPTN_7D3" IsOption="True"/>
<Feature NId="OPTN_8UD" IsOption="True"/>
<Feature NId="OPTN_8UM" IsOption="True"/>
<Feature NId="OPTN_9ZW" IsOption="True"/>
</LOF>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
LOF (Bills of Features) data flow provided by the system, relative to a specific plant (PLT01) among those that
have been configured and a Final Product Type (VHL).
• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a
Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.
• All Bills of Features to be imported into Opcenter Execution Discrete must be listed within the <Define> tag
within the <LOF> tags specifying the attributes: Description and FP_FAMILY. In addition the <Features> and
<Options> tags must respectively contain the list of Features and Options to be imported within each Bill of
Feature.
• All previously imported Bills of Features that are no more available in the External System and consequently
must be removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the
<Define> tag, specifying the related Final Product Family (FP_FAMILY attribute) and the Revision, specifying
the revision to be removed. If no value is specified for the Revision attribute, revision 001 is removed.

XSLT Transformation
The Opcenter Connect MOM workflow uses the ProductConfiguration.xslt file to verify if the XML file described
above contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML
files, one containing the correct nodes that can be successfully imported, and one containing the wrong nodes that
must be logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>
<!-- Log Invalid Data -->
<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="LOF[not(@FP_FAMILY) or @FP_FAMILY='
' or count(Feature[not(@NId)]) >
0 or count(Feature[@NId = '']) > 0 or count(Feature[@ValueNId =
'']) > 0 or
(count(Feature[@NId]) != count(Feature[@ValueNId][@IsOption =
'False']) + count(Feature[@ValueNId][not(@IsOption)]) + count(Feature[not(@ValueNId)]
[@IsOption='True']))]" mode="error" />
<!-- <xsl:call-template name="ErrorTemplate" />
-->
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<!-- <xsl:call-template name="RemoveTemplateError" /> -->
<xsl:apply-templates select="LOF[not(@FP_FAMILY) or
@FP_FAMILY='']" />

</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
<!-- Import Valid Data -->
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<!-- <xsl:call-template name="WriteDataTemplate" />

--

>
<xsl:apply-templates select="LOF[(@FP_FAMILY) and @FP_FAMILY!=''
and count(Feature[not(@NId)]) = 0 and count(Feature[@NId = ''])
= 0 and
count(Feature[@ValueNId = '']) = 0 and
(count(Feature[@NId]) = count(Feature[@ValueNId][@IsOption =
'False']) + count(Feature[@ValueNId][not(@IsOption)]) + count(Feature[not(@ValueNId)]
[@IsOption='True']))
]" mode="import" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="LOF[(@FP_FAMILY) and @FP_FAMILY!
='']" />
<!-- <xsl:call-template name="RemoveTemplate" /> -->
<!-- <xsl:apply-templates select="LOF[(@FP_FAMILY) and
@FP_FAMILY!='' and not(./Feature/@NId='')]"/> -->
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
</CamstarCompoundMessage>
</xsl:template>
<!-- Define -->
<xsl:template match="ImportDataFlow/Define/LOF" mode="error">
<xsl:if test="not(@FP_FAMILY) or @FP_FAMILY=''">
<LOF>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Feature Title" />
<Par key="Property" value="FP_FAMILY" />
</Parameters>
</Error>
</LOF>
</xsl:if>
<xsl:if test="(@FP_FAMILY) and @FP_FAMILY!=''">
<xsl:for-each select="./Feature">
<xsl:if test="not(@NId) or @NId=''">
<Feature>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">

<Parameters>
<Par key="Entity" value="Feature Title" />
<Par key="Property" value="Feature NId" />
</Parameters>
</Error>
</Feature>
</xsl:if>
<xsl:if test="@NId!='' and @IsOption='True' and ((@ValueNId) or
@ValueNId!='')">
<Feature>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12220">
<Parameters>
<Par key="Entity" value="Feature Title" />
<Par key="Property" value="IsOption" />
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="@NId!='' and @IsOption='True' and
((@ValueNId) or @ValueNId!='')">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</Feature>
</xsl:if>
<xsl:if test="@NId!='' and (not(@IsOption) or @IsOption='False') and
(not(@ValueNId) or @ValueNId='')">
<Feature>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Feature Title" />
<Par key="Property" value="Feature IsOption" />
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="@NId!='' and (not(@IsOption) or
@IsOption='False') and (not(@ValueNId) or @ValueNId='')">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</Feature>
</xsl:if>
</xsl:for-each>
</xsl:if>

</xsl:template>
<xsl:template match="ImportDataFlow/Define/LOF" mode="import">
<xsl:copy-of select="." />
</xsl:template>
<!-- Remove -->
<xsl:template match="ImportDataFlow/Remove/LOF">
<xsl:choose>
<xsl:when test="not(@FP_FAMILY) or @FP_FAMILY=''">
<LOF>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="Product configuration" />
<Par key="Property" value="FP_FAMILY" />
</Parameters>
</Error>
</LOF>
</xsl:when>
<xsl:otherwise>
<xsl:copy-of select="." />
</xsl:otherwise>
</xsl:choose>
</xsl:template>
</xsl:stylesheet>

##### XML File for Bills of Materials

It is possible to automatically align the Bills of Materials contained in the Opcenter Execution Discrete database
with those available in the External System. This operation can be performed through an XML file created according
to the structure below.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="BOM" Plant="PLT01" FP_TYPE = "VHL">
<Define>
<BOM FP_FAMILY="GXRY21LCRRPL24DS14KSPA-4C92" >
<Material NId="ME-07135491500" Quantity="2" UoMNId="Unit"/>
<Material NId="ME-09135491500" Quantity="2" UoMNId="Unit"/>
<Material NId="ME-01347625500" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-39567102500" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-07023220010" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-06079220010" Quantity="1" UoMNId="Unit"/>
</BOM>
<BOM FP_FAMILY="GXRY21LCRWML24DS18KBSC-4C92" >
<Material NId="ME-09514202500" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-09845791500" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-00945791500" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-04241402500" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-30309955370" Quantity="1" UoMNId="Unit"/>
<Material NId="ME-36309955370" Quantity="1" UoMNId="Unit"/>

</BOM>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
BOM (Bill of Materials) data flow provided by the system, relative to a specific plant (PLT01) among those that
have been configured and a Final Product Type (VHL).
• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a
Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.
• Each Bill of Materials to be imported into Opcenter Execution Discrete must be listed within the <Define> tag
with the related FP_FAMILY attributes, then within each Bill of Materials it is necessary to list the related
Materials specifying the following attributes:
• NId
• Quantity
• UoM
• All previously imported Bills of Materials that are no more available in the External System and consequently
must be removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the
<Define> tag, specifying the related Final Product Family (FP_FAMILY attribute).
It is not possible to import different versions of the same Bill of Materials in the same XML file.

XSLT Transformation
The Opcenter Connect MOM workflow uses the Bom.xslt file to verify if the XML file described above contains
logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>
<!-- Log Invalid Data -->
<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="BOM[not(@FP_FAMILY) or @FP_FAMILY='
' or count(Material[not(@NId)]) > 0 or count(Material[@NId = '']) > 0 or
count(Material[not(@Quantity)]) > 0 or count(Material[@Quantity = '']) > 0 or
count(Material[not(@UoMNId)]) > 0 or count(Material[@UoMNId= '']) > 0]"
mode="error" />
</xsl:for-each>
</Define>

<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="BOM[not(@FP_FAMILY) or
@FP_FAMILY=''] " />
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
<!-- Import Valid Data -->
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="BOM[(@FP_FAMILY) and @FP_FAMILY!=''
and count(Material[not(@NId)]) = 0 and count(Material[@NId = '']) = 0 and
count(Material[not(@Quantity)]) = 0 and count(Material[@Quantity = '']) = 0 and
count(Material[not(@UoMNId)]) = 0 and count(Material[@UoMNId= '']) = 0]" mode="import
" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="BOM[(@FP_FAMILY) and @FP_FAMILY!
='']" />
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
</CamstarCompoundMessage>
</xsl:template>
<!-- Define -->
<xsl:template match="ImportDataFlow/Define/BOM" mode="error">
<xsl:if test="not(@FP_FAMILY) or @FP_FAMILY=''">
<BOM>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="BOM" />
<Par key="Property" value="FP_FAMILY" />
</Parameters>
</Error>
</BOM>
</xsl:if>
<xsl:for-each select="./Material">
<xsl:if test="not(@NId) or @NId =''">
<BOM>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="MATERIAL" />
<Par key="Property" value="Material.NId" />
</Parameters>

</Error>
</BOM>
</xsl:if>
<xsl:if test="not(@Quantity) or @Quantity =''">
<BOM>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12220">
<Parameters>
<Par key="Entity" value="MATERIAL" />
<Par key="Property" value="Quantity" />
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="not(@Quantity) or (@Quantity='')">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</BOM>
</xsl:if>
<xsl:if test="not(@UoMNId) or @UoMNId= ''">
<BOM>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12220">
<Parameters>
<Par key="Entity" value="MATERIAL" />
<Par key="Property" value="UoMNId" />
<Par key="NId">
<xsl:attribute name="value">
<xsl:choose>
<xsl:when test="not(@UoMNId) or (@UoMNId='')">
<xsl:value-of select="@NId" />
</xsl:when>
</xsl:choose>
</xsl:attribute>
</Par>
</Parameters>
</Error>
</BOM>
</xsl:if>
</xsl:for-each>
</xsl:template>
<xsl:template match="ImportDataFlow/Define/BOM" mode="import">
<xsl:copy-of select="." />
</xsl:template>
<!-- Remove -->
<xsl:template match="ImportDataFlow/Remove/BOM">
<xsl:choose>
<xsl:when test="not(@FP_FAMILY) or @FP_FAMILY=''">
<BOM>

<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="BOM" />
<Par key="Property" value="FP_FAMILY" />
</Parameters>
</Error>
</BOM>
</xsl:when>
<xsl:otherwise>
<xsl:copy-of select="." />
</xsl:otherwise>
</xsl:choose>
</xsl:template>
</xsl:stylesheet>

##### XML File for ERP Orders

It is possible to automatically align the ERP Orders contained in the Opcenter Execution Discrete database with
those available in the External System. This operation can be performed through an XML file created according to
the structure below.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="ERPLIST" Plant="PLT01" FP_TYPE = "VHL">
<Define>
<ERPOrder NId="ERPO-F0000000001" Name="ERPO-F0000000001" Description="ERPOF0000000001" FP_FAMILY="GXRY21SORBGL24DS14KBSA-4920" ProductionDate="2019-10-25T06:53
:55Z" DeliveryDate="2019-10-25T06:53:55Z" CustomerTypeNId="TRY-OUT" Sequence="1"
SerialNumber="VHL4399443999000001" MasterPlanNId="150%BOP_VHL_TCM" Quantity="2"
UoMNId="u"/>
<ERPOrder NId="ERPO-F0000000002" Name="ERPO-F0000000002" Description="ERPOF0000000002" FP_FAMILY="GXSY20LORDBL20GS11KSPE-1C1E" ProductionDate="2019-10-25T06:53
:55Z" DeliveryDate="2019-10-25T06:53:55Z" CustomerTypeNId="CRASH-TEST" Sequence="2"
SerialNumber="VHL4399443999000002" MasterPlanNId="150%BOP_VHL_TCM" Quantity="2"
UoMNId="u"/>
<ERPOrder NId="ERPO-F0000000003" Name="ERPO-F0000000003" Description="ERPOF0000000003" FP_FAMILY="GXRY21LCRWML24DS18KBSC-4C92" ProductionDate="2019-10-25T06:53
:55Z" DeliveryDate="2019-10-25T06:53:55Z" CustomerTypeNId="FAIR" Sequence="3"
SerialNumber="VHL4399443999000003" MasterPlanNId="150%BOP_VHL_TCM" Quantity="2"
UoMNId="u"/>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
ERPLIST (ERP Order List) data flow provided by the system, relative to a specific plant (PLT01) among those
that have been configured and a Final Product Type (VHL).

• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a
Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.
• All ERP Orders to be imported into Opcenter Execution Discrete must be listed within the <Define> tag with the
following attributes:
• NId
• Name
• Description
• FP_FAMILY
• Final Material
• FinalMaterialRevision
• FinalMaterialUId
• ProductionType
• ProdutionDate (in UTC format)
• DeliveryDate (in UTC format)
• CustomerTypeNId
• Sequence
• SerialNumber
• MasterPlanNId
• Quantity (default is 1)
• UoMNId (default is u)
• All previously imported ERP Orders that are no more available in the External System and consequently must be
removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the <Define>
tag, specifying the related Identifiers (NId attribute).

XSLT Transformation
The Opcenter Connect MOM workflow uses the ERPOrder.xslt file to verify if the XML file described above contains
logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>
<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="ERPOrder[(not(@NId) or @NId='') or
(not(@Name) or @Name='') or ((not(@FP_FAMILY) or @FP_FAMILY='') and
(not(@FinalMaterial) or @FinalMaterial='')) or (not(@CustomerTypeNId) or
@CustomerTypeNId='') or (not(@Sequence) or @Sequence='') or ((@BaselineUId) and
(@MasterPlanNId)) ]"/>
</xsl:for-each>
</Define>

<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="ERPOrder[not(@NId) or @NId='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select="ERPOrder[((@NId) and @NId!='') and
((@Name) and @Name!='') and (((@FP_FAMILY) and @FP_FAMILY!='') or ((@FinalMaterial)
and @FinalMaterial!='')) and ((@CustomerTypeNId) and @CustomerTypeNId!='') and
((@Sequence) and @Sequence!='') and not((@BaselineUId) and (@MasterPlanNId)) ]"/>
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="ERPOrder[(@NId) and @NId!='']"/>
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
</CamstarCompoundMessage>
</xsl:template>
<xsl:template match="ImportDataFlow/Define/ERPOrder">
<xsl:choose>
<xsl:when test="not(@NId) or @NId=''">
<ERPOrder>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="ERP Order"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</ERPOrder>
</xsl:when>
<xsl:when test="not(@Name) or @Name=''">
<ERPOrder>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="ERP Order"></Par>
<Par key="Property" value="Name"></Par>
</Parameters>
</Error>
</ERPOrder>
</xsl:when>
<xsl:when test="((not(@FP_FAMILY) or @FP_FAMILY='') and (not(@FinalMaterial) or
@FinalMaterial=''))">

<ERPOrder>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="ERP Order"></Par>
<Par key="Property" value="FP_FAMILY or FinalMaterial"></Par>
</Parameters>
</Error>
</ERPOrder>
</xsl:when>
<xsl:when test="not(@CustomerTypeNId) or @CustomerTypeNId=''">
<ERPOrder>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="ERP Order"></Par>
<Par key="Property" value="CustomerTypeNId"></Par>
</Parameters>
</Error>
</ERPOrder>
</xsl:when>
<xsl:when test="((@BaselineUId) and (@MasterPlanNId))">
<ERPOrder>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="ERP Order"></Par>
<Par key="Property" value="BaselineUId/MasterPlanNId"></Par>
</Parameters>
</Error>
</ERPOrder>
</xsl:when>
<xsl:when test="not(@Sequence) or @Sequence=''">
<ERPOrder>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="ERP Order"></Par>
<Par key="Property" value="Sequence"></Par>
</Parameters>
</Error>
</ERPOrder>
</xsl:when>
</xsl:choose>
<xsl:if test="((@NId) and @NId!='') and ((@Name) and @Name!='') and
(((@FP_FAMILY) and @FP_FAMILY!='') or ((@FinalMaterial) and @FinalMaterial!='')) and
((@CustomerTypeNId) and @CustomerTypeNId!='') and ((@Sequence) and @Sequence!='') and
not((@BaselineUId) and (@MasterPlanNId))">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
<xsl:template match="ImportDataFlow/Remove/ERPOrder">
<xsl:if test="not(@NId) or @NId=''">

<ERPOrder>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="ERP Order"></Par>
<Par key="Property" value="NId"></Par>
</Parameters>
</Error>
</ERPOrder>
</xsl:if>
<xsl:if test="(@NId) and @NId!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:template>
</xsl:stylesheet>

##### XML File for Master Plans

It is possible to automatically align the Master Plans contained in the Opcenter Execution Discrete database with
those available in the External System. This operation can be performed through an XML file created according to
the structure below.
The Open Protocol section is available only if you have installed the ImportOPRT Extension App and can
be used solely if you have configured the Open Protocol Service asset.

XML Structure
<?xml version="1.0" encoding="utf-8" ?>
<ImportDataFlow FlowName="BOP" Plant="PL01" FP_TYPE="VHL">
<Define>
<MASTER_PLAN NId="150%BOP_VHL_TCM_1" IsSpecialized="1">
<PROCESS NId="" Name="VHL_ASSEMBLY" Description="VHL_ASSEMBLY">
<PROCESS_OP NId="TRC_FC10" Name="TRACE ENGINE" Description="TRACE ENGINE"
Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG20.WP02R"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC10" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_MAT001" Name="TRACE GEARBOX" Description="TRACE GEARBOX"
Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG20.WP02R"/>
</WORKPLACES>

<TRC_SPECS>
<MAT_LIST>
<MATERIAL NId="MAT001" Quantity="1" UoMNId="u"/>
</MAT_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC17" Name="TRACE STEERING WHEEL" Description="TRACE
STEERING WHEEL" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02R"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC17" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-001" Name="CONFIRM CARPET PRESENCE" Description="CONF
IRM CARPET PRESENCE" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP99U"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-002" Name="CONFIRM VIN LABLE PRINTED" Description="CO
NFIRM VIN LABLE PRINTED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP99U"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC06" Name="TRACE FRONT CABLE" Description="TRACE FRONT
CABLE" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP02R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP02L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC06" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC07" Name="TRACE REAR CABLE" Description="TRACE REAR
CABLE" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP03R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP03L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>

<FUNCCODE NId="FC07" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-003" Name="FRONT CABLES HOOKED" Description="FRONT
CABLES HOOKED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-004" Name="REAR CABLES HOOKED" Description="REAR
CABLES HOOKED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="GDC_001" Name="GENERIC DATA COLLECTION" Description="GENERIC
DATA COLLECTION" Category="GenericDataCollection">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<GDC_SPECS>
<GDC_DEFINITION NId="GDC_001"/>
</GDC_SPECS>
</PROCESS_OP>
</PROCESS>
</MASTER_PLAN>
<MASTER_PLAN NId="150%BOP_VHL_TCM_2" IsSpecialized="1">
<PROCESS NId="VHL_ASSEMBLY" Name="VHL_ASSEMBLY" Description="VHL_ASSEMBLY">
<PROCESS_OP NId="TRC_FC10" Name="TRACE ENGINE" Description="TRACE ENGINE">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG20.WP02R"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC10" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC1M" Name="TRACE GEARBOX" Description="TRACE GEARBOX"
Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG20.WP02R"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC1M" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>

<PROCESS_OP NId="TRC_FC17" Name="TRACE STEERING WHEEL" Description="TRACE
STEERING WHEEL" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02R"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC17" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-001" Name="CONFIRM CARPET PRESENCE" Description="CONF
IRM CARPET PRESENCE" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP99U"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-002" Name="CONFIRM VIN LABLE PRINTED" Description="CO
NFIRM VIN LABLE PRINTED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP99U"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP Name="TRACE FRONT CABLE" Description="TRACE FRONT CABLE" Category="
Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP02R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP02L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC06" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC07" Name="TRACE REAR CABLE" Description="TRACE REAR
CABLE" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP03R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP03L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC07" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-003" Name="FRONT CABLES HOOKED" Description="FRONT
CABLES HOOKED" Category="MandatoryPositiveConfirmation">

<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-004" Name="REAR CABLES HOOKED" Description="REAR
CABLES HOOKED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="GDC_001" Name="GENERIC DATA COLLECTION" Description="GENERIC
DATA COLLECTION" Category="GenericDataCollection">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<GDC_SPECS>
<GDC_DEFINITION NId="GDC_001"/>
</GDC_SPECS>
</PROCESS_OP>
</PROCESS>
</MASTER_PLAN>
<MASTER_PLAN NId="150%BOP_VHL_TCM_3" IsSpecialized="1">
<PROCESS NId="VHL_ASSEMBLY" Name="VHL_ASSEMBLY" Description="VHL_ASSEMBLY">
<PROCESS_OP NId="TRC_FC10" Name="TRACE ENGINE" Description="TRACE ENGINE"
Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG20.WP02R"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC10" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC1M" Name="TRACE GEARBOX" Description="TRACE GEARBOX"
Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG20.WP02R"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC1M" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC17" Name="TRACE STEERING WHEEL" Description="TRACE
STEERING WHEEL" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02R"/>
</WORKPLACES>

<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC17" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-001" Name="CONFIRM CARPET PRESENCE" Description="CONF
IRM CARPET PRESENCE" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP99U"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-002" Name="CONFIRM VIN LABLE PRINTED" Description="CO
NFIRM VIN LABLE PRINTED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP99U"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC06" Name="TRACE FRONT CABLE" Description="TRACE FRONT
CABLE" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP02R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP02L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC06" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="TRC_FC07" Name="TRACE REAR CABLE" Description="TRACE REAR
CABLE" Category="Traceability">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP03R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP03L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<TRC_SPECS>
<FUNCCODE_LIST>
<FUNCCODE NId="FC07" Quantity="1" UoMNId="u"/>
</FUNCCODE_LIST>
</TRC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="MPB_TR-003" Name="FRONT CABLES HOOKED" Description="FRONT
CABLES HOOKED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04R"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>

<PROCESS_OP NId="MPB_TR-004" Name="REAR CABLES HOOKED" Description="REAR
CABLES HOOKED" Category="MandatoryPositiveConfirmation">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
</PROCESS_OP>
<PROCESS_OP NId="GDC_001" Name="GENERIC DATA COLLECTION" Description="GENERIC
DATA COLLECTION" Category="GenericDataCollection">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<GDC_SPECS>
<GDC_DEFINITION NId="GDC_001"/>
</GDC_SPECS>
</PROCESS_OP>
<PROCESS_OP NId="SCR_001" Name="SCREW WHEEL" Description="SCREW WHEEL"
Category="Screwing">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG10.WP04L"/>
<WORKPLACE NId="PL01.AR30.LN01.SG30.WP02L"/>
</WORKPLACES>
<SCREWING_TOOL_DEFINITIONS>
<SCREWING_TOOL_DEFINITION NId="SCR_DRIVER_001" Bolts="4" MinTorque = "20"
MaxTorque = "50" MinAngle="0" MaxAngle="300"/>
<SCREWING_TOOL_DEFINITION NId="SCR_DRIVER_002" Bolts="6" MinTorque = "10"
MaxTorque = "30" MinAngle="0" MaxAngle="360"/>
</SCREWING_TOOL_DEFINITIONS>
</PROCESS_OP>
<PROCESS_OP NId="OPT_OP60.DRV01" Revision="A" Name=" OPRT_FIX UPPER COVER"
Description="OPRT_FIX UPPER COVER" Category="OpenProtocol">
<WORKPLACES>
<WORKPLACE NId="PL01.AR30.LN01.SG20.WP02R"/>
</WORKPLACES>
<OPEN_PROTOCOL_TOOL_DEFINITIONS>
<OPEN_PROTOCOL_TOOL_DEFINITION NId="DRV01" Version="A" Pset= "10"
ReworkPset = "30"/>
<OPEN_PROTOCOL_TOOL_DEFINITION NId="DRV02" Pset= "33" />
</OPEN_PROTOCOL_TOOL_DEFINITIONS>
</PROCESS_OP>
</PROCESS>
</MASTER_PLAN>
</Define>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
BOP (Master Plan Master Data) data flow provided by the system and relative to a specific plant (PLT01) among
those that have been configured.
• In a Multiplant scenario, the Plant attribute is mandatory since it is used to route the message to the proper
plant. If the plant represents a Hierarchy (for example, PLT01.ENTERPRISE), then only the first part of the string
(PLT01) is taken as the plant to be used. Instead, if the Plant is used simply as a piece of Equipment (and not in a

Multiplant scenario), the Message Type configuration must be modified by clicking the Message Types tab,
selecting Message Attributes and removing the plantid attribute.
• All Master Plans to be imported into Opcenter Execution Discrete must be listed within the <Define> tag with
the following attributes:
• NId
• Name
• Description
• Category
• (Optional) UId: if not present, it will be automatically generated by the system.
• If the Revision of the Material to be imported is not the default 001, the related Revision attribute must be
specified within the <Define> tag.
• All previously imported Master Plans that are no more available in the External System and consequently must
be removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the <Define>
tag, specifying the related Identifiers (NId attribute). If the combination NId/UId is present, only the Master Plan
with this specific combination will be removed. If only the NId is present, then all the Master Plans with the
specified NId will be removed.

XSLT Transformation
The Opcenter Connect MOM workflow uses the Bop.xslt file to verify if the XML file described above contains logical
errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one containing the
correct nodes that can be successfully imported, and one containing the wrong nodes that must be logged.
The default content of the .xslt file is the following, but you can customize it according to your needs:
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
<xsl:output method="xml" omit-xml-declaration="no" indent="yes" />
<xsl:template match="/">
<CamstarCompoundMessage>
<!-- Log Invalid Data -->
<Message type="LogNotValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select=
"MASTER_PLAN[not(@NId) or @NId='' or count(PROCESS) >
1 or
count(PROCESS[not(@NId)]) > 0 or count(PROCESS[@NId
= '']) > 0 or
count(PROCESS[PROCESS_OP[not(@NId)]]) > 0 or
count(PROCESS[PROCESS_OP[@NId = '']]) > 0 or
count(PROCESS[PROCESS_OP[not(@Category)]]) > 0 or
count(PROCESS[PROCESS_OP[@Category = '']]) > 0 or
count(PROCESS[PROCESS_OP[GDC_SPECS[GDC_DEFINITION[not(@NId)]]]]) > 0 or
count(PROCESS[PROCESS_OP[GDC_SPECS[GDC_DEFINITION[@NId = '']]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@NId)
]]]]) > 0 or

count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@NId =
'']]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@Bolt
s)]]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@Bolts =
'']]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MinA
ngle)]]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MinAngle
= '']]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MaxA
ngle)]]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MaxAngle
= '']]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MinT
orque)]]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MinTorqu
e = '']]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MaxT
orque)]]]]) > 0 or
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MaxTorqu
e = '']]]]) > 0 or
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[not(@NId)]]]]) > 0 or
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[@NId = '']]]]) > 0 or
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[not(@Pset)]]]]) > 0 or
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[@Pset = '']]]]) > 0]"
mode="error" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="MASTER_PLAN[not(@NId) or @NId=''] " />
</xsl:for-each>
</Remove>

</ImportDataFlow>
</Message>
<!-- Import Valid Data -->
<Message type="ImportValidData">
<ImportDataFlow>
<xsl:copy-of select="ImportDataFlow/@*[string(.)]" />
<Define>
<xsl:for-each select="ImportDataFlow/Define">
<xsl:apply-templates select=
"MASTER_PLAN[(@NId) and @NId!='' and (count(PROCESS)
= 0 or count(PROCESS) = 1) and
count(PROCESS[not(@NId)]) = 0 and count(PROCESS[@NId
= '']) = 0 and
count(PROCESS[PROCESS_OP[not(@NId)]]) = 0 and
count(PROCESS[PROCESS_OP[@NId = '']]) = 0 and
count(PROCESS[PROCESS_OP[not(@Category)]]) = 0 and
count(PROCESS[PROCESS_OP[@Category = '']]) = 0 and
count(PROCESS[PROCESS_OP[GDC_SPECS[GDC_DEFINITION[not(@NId)]]]]) = 0 and
count(PROCESS[PROCESS_OP[GDC_SPECS[GDC_DEFINITION[@NId = '']]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@NId)
]]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@NId = '']
]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@Bolt
s)]]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@Bolts =
'']]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MinA
ngle)]]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MinAngle
= '']]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MaxA
ngle)]]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MaxAngle
= '']]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MinT
orque)]]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MinTorqu
e = '']]]]) = 0 and

count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[not(@MaxT
orque)]]]]) = 0 and
count(PROCESS[PROCESS_OP[SCREWING_TOOL_DEFINITIONS[SCREWING_TOOL_DEFINITION[@MaxTorqu
e = '']]]]) = 0 and
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[not(@NId)]]]]) = 0 and
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[@NId = '']]]]) = 0 and
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[not(@Pset)]]]]) = 0 and
count(PROCESS[PROCESS_OP[OPEN_PROTOCOL_TOOL_DEFINITIONS[OPEN_PROTOCOL_TOOL_DEFINITION
[@Pset = '']]]]) = 0]"
mode="import" />
</xsl:for-each>
</Define>
<Remove>
<xsl:for-each select="ImportDataFlow/Remove">
<xsl:apply-templates select="MASTER_PLAN[(@NId) and @NId!='']" />
</xsl:for-each>
</Remove>
</ImportDataFlow>
</Message>
</CamstarCompoundMessage>
</xsl:template>
<!-- Define -->
<xsl:template match="ImportDataFlow/Define/MASTER_PLAN" mode="error">
<xsl:if test="not(@NId) or @NId=''">
<MASTER_PLAN>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="MASTER_PLAN" />
<Par key="Property" value="NId" />
</Parameters>
</Error>
</MASTER_PLAN>
</xsl:if>
<xsl:if test="@NId and @NId!=''">
<MASTER_PLAN>
<xsl:copy-of select="@*[string(.)]" />
<xsl:for-each select="./PROCESS">
<xsl:if test="not(@NId) or @NId =''">
<PROCESS>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="PROCESS" />

<Par key="Property" value="PROCESS.NId" />
</Parameters>
</Error>
</PROCESS>
</xsl:if>
<xsl:if test="@NId and @NId!=''">
<PROCESS>
<xsl:copy-of select="@*[string(.)]" />
<xsl:for-each select="./PROCESS_OP">
<xsl:if test="not(@NId) or @NId =''">
<PROCESS_OP>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="PROCESS_OP" />
<Par key="Property" value="PROCESS_OP.NId" />
</Parameters>
</Error>
</PROCESS_OP>
</xsl:if>
<xsl:if test="not(@Category) or @Category =''">
<PROCESS_OP>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="PROCESS_OP" />
<Par key="Property" value="PROCESS_OP.Category" />
</Parameters>
</Error>
</PROCESS_OP>
</xsl:if>
<xsl:if test="@NId and @NId!='' and @Category and @Category!=''">
<PROCESS_OP>
<xsl:copy-of select="@*[string(.)]" />
<xsl:for-each select="./WORKPLACES">
<xsl:copy-of select="." />
</xsl:for-each>
<xsl:choose>
<xsl:when test="@Category='GenericDataCollection'">
<xsl:for-each select="./GDC_SPECS">
<GDC_SPECS>
<xsl:copy-of select="@*[string(.)]" />
<xsl:for-each select="./GDC_DEFINITION">
<xsl:if test="not(@NId) or @NId=''">
<GDC_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="GDC_DEFINITION" />
<Par key="Property" value="GDC_DEFINITION.NId"
/>
</Parameters>
</Error>

</GDC_DEFINITION>
</xsl:if>
<xsl:if test="@NId and @NId!=''">
<xsl:copy-of select="." />
</xsl:if>
</xsl:for-each>
</GDC_SPECS>
</xsl:for-each>
</xsl:when>
<xsl:when test="@Category and @Category='Screwing'">
<xsl:for-each select="./SCREWING_TOOL_DEFINITIONS">
<SCREWING_TOOL_DEFINITIONS>
<xsl:copy-of select="@*[string(.)]" />
<xsl:for-each select="./SCREWING_TOOL_DEFINITION">
<xsl:choose>
<xsl:when test="not(@NId) or @NId=''">
<SCREWING_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="SCREWING_TOOL_DEFINI
TION" />
<Par key="Property" value="SCREWING_TOOL_DEFI
NITION.NId" />
</Parameters>
</Error>
</SCREWING_TOOL_DEFINITION>
</xsl:when>
<xsl:when test="not(@Bolts) or @Bolts=''">
<SCREWING_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="SCREWING_TOOL_DEFINI
TION" />
<Par key="Property" value="SCREWING_TOOL_DEFI
NITION.Bolts" />
</Parameters>
</Error>
</SCREWING_TOOL_DEFINITION>
</xsl:when>
<xsl:when test="not(@MinTorque) or @MinTorque=''">
<SCREWING_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="SCREWING_TOOL_DEFINI
TION" />
<Par key="Property" value="SCREWING_TOOL_DEFI
NITION.MinTorque" />
</Parameters>
</Error>
</SCREWING_TOOL_DEFINITION>

</xsl:when>
<xsl:when test="not(@MaxTorque) or @MaxTorque=''">
<SCREWING_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="SCREWING_TOOL_DEFINI
TION" />
<Par key="Property" value="SCREWING_TOOL_DEFI
NITION.MaxTorque" />
</Parameters>
</Error>
</SCREWING_TOOL_DEFINITION>
</xsl:when>
<xsl:when test="not(@MinAngle) or @MinAngle=''">
<SCREWING_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="SCREWING_TOOL_DEFINI
TION" />
<Par key="Property" value="SCREWING_TOOL_DEFI
NITION.MinAngle" />
</Parameters>
</Error>
</SCREWING_TOOL_DEFINITION>
</xsl:when>
<xsl:when test="not(@MaxAngle) or @MaxAngle=''">
<SCREWING_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="SCREWING_TOOL_DEFINI
TION" />
<Par key="Property" value="SCREWING_TOOL_DEFI
NITION.MaxAngle" />
</Parameters>
</Error>
</SCREWING_TOOL_DEFINITION>
</xsl:when>
<xsl:otherwise>
<xsl:copy-of select="." />
</xsl:otherwise>
</xsl:choose>
</xsl:for-each>
</SCREWING_TOOL_DEFINITIONS>
</xsl:for-each>
</xsl:when>
<xsl:when test="@Category and @Category='OpenProtocol'">
<xsl:for-each select="./OPEN_PROTOCOL_TOOL_DEFINITIONS">
<OPEN_PROTOCOL_TOOL_DEFINITIONS>
<xsl:copy-of select="@*[string(.)]" />
<xsl:for-each select="./OPEN_PROTOCOL_TOOL_DEFINITION">

<xsl:choose>
<xsl:when test="not(@NId) or @NId=''">
<OPEN_PROTOCOL_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="OPEN_PROTOCOL_TOOL_D
EFINITION" />
<Par key="Property" value="OPEN_PROTOCOL_TOOL
_DEFINITION.NId" />
</Parameters>
</Error>
</OPEN_PROTOCOL_TOOL_DEFINITION>
</xsl:when>
<xsl:when test="not(@Pset) or @Pset=''">
<OPEN_PROTOCOL_TOOL_DEFINITION>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="OPEN_PROTOCOL_TOOL_D
EFINITION" />
<Par key="Property" value="OPEN_PROTOCOL_TOOL
_DEFINITION.Pset" />
</Parameters>
</Error>
</OPEN_PROTOCOL_TOOL_DEFINITION>
</xsl:when>
<xsl:otherwise>
<xsl:copy-of select="." />
</xsl:otherwise>
</xsl:choose>
</xsl:for-each>
</OPEN_PROTOCOL_TOOL_DEFINITIONS>
</xsl:for-each>
</xsl:when>
<xsl:otherwise>
<xsl:copy-of select="." />
</xsl:otherwise>
</xsl:choose>
</PROCESS_OP>
</xsl:if>
</xsl:for-each>
</PROCESS>
</xsl:if>
</xsl:for-each>
</MASTER_PLAN>
</xsl:if>
</xsl:template>
<xsl:template match="ImportDataFlow/Define/MASTER_PLAN" mode="import">
<xsl:copy-of select="." />
</xsl:template>
<!-- Remove -->
<xsl:template match="ImportDataFlow/Remove/MASTER_PLAN">

<xsl:choose>
<xsl:when test="not(@NId) or @NId=''">
<MASTER_PLAN>
<xsl:copy-of select="@*[string(.)]" />
<Error Id="12210">
<Parameters>
<Par key="Entity" value="MASTER_PLAN" />
<Par key="Property" value="NId" />
</Parameters>
</Error>
</MASTER_PLAN>
</xsl:when>
<xsl:otherwise>
<xsl:copy-of select="." />
</xsl:otherwise>
</xsl:choose>
</xsl:template>
</xsl:stylesheet>

##### XML File for Inspection Master Plans

It is possible to automatically align the Inspection Master Plans contained in the Opcenter Execution
Discrete database with those available in the External System. This operation can be performed through an XML file
created according to the structure below.

XML Structure
Here is an example of an XML message that can be used to import Inspection Master Plans.
<?xml version="1.0" encoding="UTF-8"?>
<ImportDataFlow FlowName="IMP" Plant="Plant1">
<Define>
<INS_MASTER_PLAN NId="IMP_GoodData" Name="IMP1" Description="Inspection
Master Plan" Revision="A">
<INS_OP NId="InsOp1" Name="Ins Op" Revision="A" Seq="22">
<INS_DEF NId="InsDefn1" Name="100PercentFrequency Ins Defn" Revision="
A" Frequency="100Percent" ScenarioNId="Scen1" CanBeSkipped="false">
<QLTY_CHARACTERISTIC NId="ATT_CHAR1" Type="Attributive"
Description="Attributive Characteristic" Revision="A" UId="ATT_CHAR1" Name="ATT_CHAR1
" Criticality="Main" Context="Process">
<STATUS_DESCRIPTION Ok="Accept" NOk="Reject"/>
</QLTY_CHARACTERISTIC>
<REF_MATERIALS>
<REF_MATERIAL NId="Mat1" Revision="A"/>
<REF_MATERIAL NId="Mat2" Revision="A"/>
</REF_MATERIALS>
<MFG_EQUIPMENT_LIST>
<MFG_EQUIPMENT NId="Unit"/>
<MFG_EQUIPMENT NId="WC"/>
</MFG_EQUIPMENT_LIST>
</INS_DEF>
</INS_OP>

<INS_OP NId="InsOp2" Name="Ins Op" Revision="A" Seq="32">
<INS_DEF NId="InsDefn2" Name="TimeBasedFrequency Ins Defn" Revision="
A" Frequency="TimeBased" TimeBasedScheduleMode="Hourly" FrequencyValue="5"
TimeBasedWarningValue="1" TimeBasedWarningUoM="hour" CanBeSkipped="false">
<QLTY_CHARACTERISTIC NId="VAR_CHAR" Type="Variable" Description="
Variable Characteristic" Revision="A" UId="VAR_CHAR" Name="VAR_CHAR" Criticality="Cri
tical" Context="Process">
<NOMINAL_VALUE UoMNId="mm" QuantityValue="10"/>
<LOWER_TOLERANCE UoMNId="mm" QuantityValue="5"/>
<UPPER_TOLERANCE UoMNId="mm" QuantityValue="15"/>
</QLTY_CHARACTERISTIC>
</INS_DEF>
</INS_OP>
<INS_OP NId="InsOp3" Name="Ins Op" Revision="A" Seq="52">
<INS_DEF NId="InsDefn3" Name="PartBasedFrequency Ins Defn" Revision="
A" Frequency="PartBased" FrequencyValue="5" CanBeSkipped="false">
<QLTY_CHARACTERISTIC NId="VISUAL_CHAR" Type="Visual" Description="
Visual Characteristic" Revision="A" UId="VISUAL_CHAR" Name="VISUAL_CHAR" Criticality="
Main" Context="Process">
<IMAGE NId="DOC1" Revision="A" SketchRows="6" SketchColumns="
10"/>
</QLTY_CHARACTERISTIC>
</INS_DEF>
</INS_OP>
<INS_OP NId="InsOp4" Name="Ins Op" Revision="A" Seq="55">
<INS_DEF NId="InsDefn4" Name="UnitBasedFrequency Ins Defn" Revision="
A" Frequency="UnitBased" FrequencyValue="4" CanBeSkipped="false">
<QLTY_CHARACTERISTIC NId="ATT_CHAR2" Type="Attributive"
Description="Attributive Characteristic 2" Revision="A" UId="ATT_CHAR2" Name="ATT_CHA
R2" Criticality="Critical" Context="Process">
<STATUS_DESCRIPTION Ok="OK" NOk="NotOK"/>
</QLTY_CHARACTERISTIC>
</INS_DEF>
</INS_OP>
</INS_MASTER_PLAN>
<INS_MASTER_PLAN NId="IMP2" Name="IMP2" Description="Inspection Master Plan"
Revision="A">
<INS_OP NId="InsOp21" Name="Ins Op" Revision="A" Seq="56">
<INS_DEF NId="" Name="100PercentFrequency Ins Defn" Revision="A"
Frequency="100Percent" CanBeSkipped="false">
<QLTY_CHARACTERISTIC NId="ATT_CHAR21" Type="Attributive"
Description="Attributive Characteristic" Revision="A" UId="ATT_CHAR21" Name="ATT_CHAR
21" Criticality="Main" Context="Process">
<STATUS_DESCRIPTION Ok="Accept" NOk="Reject"/>
</QLTY_CHARACTERISTIC>
<REF_MATERIALS>
<REF_MATERIAL NId="Mat3" Revision="A"/>
<REF_MATERIAL NId="Mat4" Revision="A"/>
</REF_MATERIALS>
<MFG_EQUIPMENT_LIST>
<MFG_EQUIPMENT NId="Unit2"/>
<MFG_EQUIPMENT NId="WC2"/>
</MFG_EQUIPMENT_LIST>

</INS_DEF>
</INS_OP>
<INS_OP NId="InsOp22" Name="Ins Op" Revision="A" Seq="58">
<INS_DEF NId="InsDefn22" Name="UnitBasedFrequency Ins Defn" Revision="
A" Frequency="UnitBased" FrequencyValue="4" CanBeSkipped="false">
<QLTY_CHARACTERISTIC NId="ATT_CHAR22" Type="Attributive"
Description="Attributive Characteristic 2" Revision="A" UId="ATT_CHAR22" Name="ATT_CH
AR22" Criticality="Critical" Context="Process">
<STATUS_DESCRIPTION Ok="OK" NOk="NotOK"/>
</QLTY_CHARACTERISTIC>
</INS_DEF>
</INS_OP>
</INS_MASTER_PLAN>
<INS_MASTER_PLAN NId="IMP3" Revision="A">
<INS_OP NId="INSOP31" Revision="A">
<INS_DEF NId="InsDefn31" Revision="A" Frequency="100Percent">
<QLTY_CHARACTERISTIC NId="ATT_CHAR31" Type="Attributive" Revision="
A" UId="ATT_CHAR31" Criticality="" Context="">
<STATUS_DESCRIPTION Ok="" NOk="Reject"/>
</QLTY_CHARACTERISTIC>
</INS_DEF>
</INS_OP>
</INS_MASTER_PLAN>
</Define>
<Remove>
<INS_MASTER_PLAN NId="IMP_Nid" Description="OK: Remove"/>
</Remove>
</ImportDataFlow>

The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the IMP
(Inspection Master Plans) data flow provided by the system, relative to a specific plant (Plant1) and a Final Product
Type (VHL), among those that have been configured. In a Multiplant scenario, the Plant attribute is mandatory
since it is used to route the message to the proper plant. If the plant represents a Hierarchy (for example,
PLT01.ENTERPRISE), then only the first part of the string (PLT01) is taken as the plant to be used. Instead, if the
Plant is used simply as a piece of Equipment (and not in a Multiplant scenario), the Message Type configuration
must be modified by clicking the Message Types tab, selecting Message Attributes and removing the plantid
attribute.
Inspection Master Plans to be imported into Opcenter Execution Discrete must be listed within the <Define> tag,
with <INS_MASTER_PLAN>, <INS_OP>, <INS_DEF>, and <QLTY_CHARACTERISTIC> tags specifying the following
attributes:
Attributes

Description

Occurrence

<INS_MASTER_PLAN> Inspection Master Plan
NId

Natural Identifier of the Master Plan.

Mandatory

Name

Name of the Inspection Master Plan.

Optional

Revision

Revision of the Inspection Master Plan.

Mandatory

Attributes

Description

Occurrence

Description

Description of the Inspection Master Plan.

Optional

NId

Natural Identifier of the Inspection Operation.

Mandatory

Name

Name of the Inspection Operation.

Optional

Revision

Revision of the Inspection Operation.

Mandatory

Seq

Sequence of the Inspection Operation.

Optional

NId

Natural Identifier of the Inspection Definition.

Mandatory

Name

Name of the Inspection Definition.

Optional

Revision

Revision of the Inspection Definition.

Mandatory

Frequency

Frequency Type of the Inspection Definition.

Mandatory

Scenario NId

Signature Scenario ID.

Optional

CanBeSkipped

Flag indicating if the Inspection Definition can be
skipped or not.

Optional

TimeBasedScheduleMode

Time Based Scheduled Mode type for the Time
Based Inspection Definition.

Mandatory

FrequencyValue

The Frequency value for all Inspection Definition
types except 100 percent.

Mandatory

TimeBasedWarningValue

The value at which a warning will be shown for
the Time Based Inspection Definition.

Mandatory

TimeBasedWarningUoM

Unit of measure for the Time Based Inspection
Definition.

Optional

<INS_OP> Inspection Operation

<INS_DEF> Inspection Definition

<REF_MATERIALS> Reference Materials

Attributes

Description

Occurrence

REF_MATERIAL

Reference Material.

Mandatory

<MFG_EQUIPMENT_LIST> Manufacturing Equipment List
MFG_EQUIPMENT

Manufacturing Equipment.

Mandatory

<QLTY_CHARACTERISTIC> Quality Characteristic
NId

Natural Identifier of the Quality Characteristic.

Mandatory

Type

Type of the Quality Characteristic.

Mandatory

Revision

Revision of the Quality Characteristic.

Mandatory

UId

Unique Identifier of the Quality Characteristic.

Mandatory

Criticality

Criticality of the Quality Characteristic.

Mandatory

Context

Context of the Quality Characteristic.

Mandatory

Description

Description of the Quality Characteristic.

Optional

Name

Name of the Quality Characteristic.

Optional

STATUS_DESCRIPTION

Status description for the Attributive
Characteristic.

Mandatory

NOMINAL_VALUE

Nominal value for the Variable Characteristic.

Mandatory

LOWER_TOLERNCE

Lower Tolerance for the Variable Characteristic.

Optional

UPPER_TOLERANCE

Upper Tolerance for the Variable Characteristic.

Optional

IMAGE

Image for the Visual Characteristic. (NId and
Revision for the Image are mandatory).

Mandatory

Reference Materials, Signature Scenarios, and Manufacturing Equipment must pre-exist in the system, otherwise
they cannot be linked to Inspection Definitions.
Similarly, Image Documents must pre-exist in the system, otherwise they cannot be linked to Quality
Characteristics.

XSLT Transformation
The Opcenter Connect MOM workflow uses the IMP.xslt file located at C:\Program
Files\Siemens\SimaticIT\Unified\VApps\UADM\MIOIntegration\Xslt to verify if the XML file described above
contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.

##### XML File for Work Orders

It is possible to automatically align the Work Orders contained in the Opcenter Execution Discrete database with
those available in the External System. This operation can be performed through an XML file created according to
the structure below.
Work Orders can be imported either from Master Plans or As Planned BOPs.

XML Structure
Here is an example of an XML message that can be used to import Work Orders:
<?xml version="1.0" encoding="UTF-8"?>
<ImportDataFlow FlowName="WorkOrder" Plant="Siemens">
<Define>
<WorkOrder MasterPlanNId="AXLE_Truck_MP" NId="AXLE_Truck_w10" ProductionType="Ser
ialized" Quantity="5" Product="Truck_AXLE" ErpOrder="" Priority="" BillOfFeature="BOF
2" BillOfMaterial="" BillFeatureRevision="A" BillOfMaterialVersion="" DueDate="202205-05T06:53:55Z" EstimatedStartTime="2022-05-05T06:53:55Z" EstimatedEndTime="2022-0505T06:53:55Z">
<Material_list>
<Material NId="mat1" Name="mat1" UoM="mm" />
<Material NId="mat2" Name="mat2" UoM="mm" />
</Material_list>
<SerialNumber_list>
<SerialNumber NId="FinalProductIdentier_1" />
<SerialNumber NId="FinalProductIdentier_2" />
</SerialNumber_list>
</WorkOrder>
<WorkOrder AsPlannedNId="Fabrication" NId="Fabrication_w10" ProductionType="Trans
ferBatch" BatchId="BatchId_001" Quantity="5" Product="Metal_Block" Status="Edit"
ErpOrder="" Priority="" BillOfFeature="" BillOfMaterial="" BillFeatureRevision=""
BillOfMaterialVersion="" DueDate="2022-05-05T06:53:55Z" EstimatedStartTime="2022-05-0
5T06:53:55Z" EstimatedEndTime="2022-05-05T06:53:55Z"></WorkOrder>
<WorkOrder UseMasterPlan="true" NId="AXLE_Car_MP_w10" ProductionType="FullQuantit
y" Quantity="5" Product="Car_AXLE" ErpOrder="" Priority="" BillOfFeature="BOF1"
BillOfMaterial="BOM1" BillFeatureRevision="A" BillOfMaterialVersion="A" DueDate="202
2-05-05T06:53:55Z" EstimatedStartTime="" EstimatedEndTime="2022-05-05T06:53:55Z"></
WorkOrder>
<WorkOrder UseMasterPlan="false" NId="Assembly_w10" ProductionType="FullSerialize
d" Quantity="5" Product="Machined_Block" Status="ReadyForScheduling" ErpOrder=""
Priority="" BillOfFeature="" BillOfMaterial="" BillFeatureRevision=""

BillOfMaterialVersion="" DueDate="" EstimatedStartTime="2022-05-05T06:53:55Z"
EstimatedEndTime="2022-05-05T06:53:55Z"></WorkOrder>
</Define>
<Remove>
<WorkOrder NId="WO_Nid" Description="Wo_NId_desc" />
</Remove>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
WorkOrder data flow provided by the system and relative to a specific plant (Plant1), among those that have
been configured.
• All Work Orders to be imported into Opcenter Execution Discrete must be listed within the <Define> tag, where
<WorkOrder>, <Material_List> and <SerialNumber_List> tags contain the following attributes:
Attributes

Description

Occurrence

MasterPlanNId

Identifier of the Master Plan to which you want to
associate the Work Order.

Optional, if AsPlannedNId
or UseMasterPlan are
present in the XML.

AsPlannedNId

Identifier of the As Planned BOP to which you want
to associate the Work Order.

Optional, if MasterPlanNId
or UseMasterPlan are
present in the XML.

UseMasterPlan

If the value of this attribute is true, then the Work
Order will be created from the Master Plan. If the
value of this attribute is false, then the Work Order
will be created from the As Planned BOP.

Optional, if MasterPlanNId
or AsPlannedNId are
present in the XML.

NId

Natural Identifier of the Work Order.

Mandatory

Attributes

Description

Occurrence

ProductionType

(Appears only after selecting a Master Plan)

Mandatory

• Serialized - Indicates that, at the time of Work
Order creation, serial numbers representing the
number of items that the Work Order is expected
to produce, must be associated to the Work
Order. Available only if the selected Master Plan
produces serialized Materials.
• FullQuantity - Indicates that the next Work
Order Operation can start only after the entire
quantity of the previous Work Order Operation
has been produced.
• FullSerialized - Indicates that the Work Order
will produce multiple Material Tracking Units of
the same type, and each of them will be
assigned with a serial number. Available only if
the selected Master Plan produces serialized
Materials.
• TransferBatch - Indicates that the next Work
Order Operation can start after a portion of the
entire material batch is completed. The
remaining portion can be moved to a successive
Work Order Operation.
• FlexibleBatch - Indicates that the Work Order
created is a flexible batch and the user can
modify the quantity to be produced based on
the plant conditions (status of the equipment,
end of shifts, and so on).
• FlexibleSerialized - Indicates that the Work
Order is created stepwise and is flexible. The
user can modify the quantity to be produced
based on the plant conditions (status of the
equipment, end of shifts, and so on).
Quantity

The quantity of Material that the Work Order is
expected to produce.

Mandatory

Plant

Opcenter Execution Foundation Plant (intended in
the multi-plant meaning) and the Enterprise or Site
where the Work Order is expected to be executed.
For more information see the bulleted list below.

Mandatory

BatchId

(Only if the Production Type is set to FullQuantity,
TransferBatch or FlexibleBatch)

Optional

The unique identifier of the Material Batch that the
Work Order is expected to produce.

Attributes

Description

Occurrence

Product

The Material that the Work Order is expected to
produce.

Mandatory

ERPOrder

Identifier of the related ERP order, if applicable.

Optional

Priority

A number identifying the order of execution of the
Work Order.

Optional

BillOfFeature

The Bill of Features containing the Features that the
user wants to be present in the Work Order being
created.

Optional

BillOfMaterial

The Bill of Materials containing the Materials that
the user wants to be present in the Work Order
being created.

Optional

DueDate

The date by which the Work Order must be
completed. The date format is: yyyy-MMddThh:mm:ssZ.

Optional

EstimatedStartTime

The date and time when the Work Order execution
is expected to start. The timestamp must respect
the UTC format: for example, yyyy-MMddThh:mm:ssZ.

Optional

EstimatedEndTime

The date and time when the Work Order execution
is expected to end. The timestamp must respect the
UTC format: for example, yyyy-MM-ddThh:mm:ssZ.

Optional

Status

The status of the Work Order. Possible values: Edit,
New, and ReadyForScheduling.

Optional

• If <Material_List> is used, then NId for Material is mandatory. If <SerialNumber_List> is used, then NId for
SerialNumber is mandatory.
• If <UseMasterPlan> value is true, then the Work Order is created from the Master Plan. If <UseMasterPlan>
value is false, then the Work Order is created from the As Planned BOP.
• If either <MasterPlanNId> or <AsPlannedNId> contain any value, then the Work Order is created either by a
Master Plan or an As Planned BOP that must have been completed and, in this case, the value of
<UseMasterPlan> is not considered.
• All previously imported Work Orders that are no more available in the External System and consequently must
be removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the <Define>
tag, specifying the related Identifiers (NId attribute).
• If the Plant contains only one piece of information (for example, PLANT01), then this piece of information is
used both as Plant Id in case of a Multiplant scenario, and as Plant field of the Work Order.

• If the Plant contains two pieces of information (for example, PLANT01.ENTERPRISE1), then the first part
(PLANT01) is used as Plant Id in case of a Multiplant scenario, while the second part (ENTERPRISE1) is used as
the Plant field of the Work Order.
• If the Plant contains more pieces of information (for example, PLANT01.ENTERPRISE1.SITE1) then the first part
(PLANT01) is used as Plant Id in case of a Multiplant scenario, while the second part (ENTERPRISE1.SITE1) is
used as the Plant field of the Work Order.

XSLT Transformation
The Opcenter Connect MOM workflow uses the WorkOrder.xslt file located at C:\Program
Files\Siemens\SimaticIT\Unified\VApps\UADM\MIOIntegration\Xslt to verify if the XML file described above
contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.

##### XML File for Full Work Orders

It is possible to automatically align the Work Orders contained in the Opcenter Execution Discrete database with
those available in the External System. This operation can be performed through an XML file created according to
the structure below.
The entire structure of the Work Order is imported along with the specifications related to its Work Order
Operations and Work Order Steps. In addition, if either a Master Plan or an As Planned BOP is indicated, the
information contained in the XML file will be merged with those contained in the Master Plan or As Planned BOP.

XML Structure
Here is an example of an XML message that can be used to import the structure of the Work Order:
<ImportDataFlow FlowName="FullWorkOrder" Plant="DefaultPlant.Plant">
<Define>
<WorkOrder NId="WO_UC1" Name="WO_UC1" MasterPlanNId="" AsPlannedNId= "" UId="
" ProductionType="Serialized" Quantity="1" BatchId="" Product="LandingGear777"
ProductRevision="A" ProductUId="LandingGear777_UId" ProductUoM="g" Status="New"
Priority="1" DueDate="2023-09-30T14:18:37.000Z" EstimatedStartTime="2023-09-26T14:19:
52.000Z" EstimatedEndTime="2023-09-28T14:19:52.000Z">
<SerialNumbers>
<SerialNumber Code="SN1"/>
</SerialNumbers>
<WorkOrderOperations>
<WorkOrderOperation NId="UC_WorkOrderOperation_1" Name="UC_WorkOrderO
peration_1" Description="UC_WorkOrderOperation_1" Sequence="10" Priority="1"
OperationStepCategoryNId="Default" WorkOperationTypeNId="Standard"
ParentWOOpFolderNId="" RequiredCertificateNId="" RequiredInspectionRole=""
ToBeCollectedDocument="false" ElectronicSignaturePause="false"
ElectronicSignatureStart="false" ElectronicSignatureComplete="false"
EstimatedStartTime="2023-09-26T14:29:52.000Z" EstimatedDuration="PT4H1M1S"
EstimatedEndTime="2023-09-27T14:25:45.000Z">
<InterlockingChecks>
<InterlockingCheck NId="AllPartsAssembled" Outbound="true"/>
<InterlockingCheck NId="AllStepsCompleted" Inbound="true"/>
</InterlockingChecks>
<Users>

<User NId="Administrator"/>
<User NId="Operator1"/>
</Users>
<Machines>
<Machine NId="Machine1"/>
<Machine NId="Machine2"/>
</Machines>
<Materials>
<Material NId="Glue" Name="Glue" Quantity="1" UoM="l"
SpecificationType="Reference" UId="Glue" Revision="A" OccurrenceId="" Sequence=""
LogicalPosition="" GroupId="" AlternativeSelected=""/>
<Material NId="LandingGear777" Name="LandingGear777" Quantity="
2" SpecificationType="NormalPart" UId="LandingGear777" Revision="A" OccurrenceId=""
Sequence="" LogicalPosition="" GroupId="" AlternativeSelected=""/>
<Material NId="Pivot" Name="Pivot" Quantity="3"
SpecificationType="RangePart" UId="Pivot" Revision="A" OccurrenceId="" Sequence=""
LogicalPosition="" GroupId="" AlternativeSelected=""/>
<Material NId="RetractableLandingGear" Name="RetractableLandi
ngGear" Quantity="4" SpecificationType="Alternative" UId="RetractableLandingGear"
Revision="A" OccurrenceId="" Sequence="" LogicalPosition="" GroupId="1"
AlternativeSelected="True"/>
<Material NId="ScrewMX" Name="ScrewMX" Quantity="5"
SpecificationType="Alternative" UId="ScrewMX" Revision="A" OccurrenceId="" Sequence="
" LogicalPosition="" GroupId="1" AlternativeSelected="False"/>
<Material NId="Wheel" Name="Wheel" Quantity="6"
SpecificationType="AsRequired" UId="Wheel" Revision="A" OccurrenceId="" Sequence=""
LogicalPosition="" GroupId="" AlternativeSelected=""/>
</Materials>
<Tools>
<Tool TimesToBeUsed="1" DefinitionNId="Hammer"/>
<Tool TimesToBeUsed="2" DefinitionNId="Wrench" Revision="A"/>
</Tools>
<WorkInstructions>
<WorkInstruction DefinitionNId="AssembleLandingGear"
AssociationType="SerialNumber"/>
<WorkInstruction DefinitionNId="AssembleWheel"
AssociationType="Operation"/>
<WorkInstruction DefinitionNId="DifferentialRotationValues"
AssociationType="SerialNumberOnDemand" Revision="A"/>
</WorkInstructions>
<QualityInspections>
<CharacteristicRepresentation NId="AssemblePivotTest"
Revision="A"/>
<CharacteristicRepresentation NId="AssembleScrewTest"
Revision="A"/>
<CharacteristicRepresentation NId="AssembleLandingGearTest"
Revision="A"/>
</QualityInspections>
<Skills>
<Skill NId="SkillDriller" Level="1"/>
<Skill NId="SkillTapping" Level="2"/>
</Skills>
<Documents>

<Document NId="AssembleInstructionsManual" Revision="A"/>
</Documents>
<HumanResources>
<HumanResource CertificationNId="DE_Driller" RequiredNumber="
1"/>
<HumanResource CertificationNId="DE_Tapping" RequiredNumber="
2"/>
</HumanResources>
<WorkOrderSteps>
<WorkOrderStep NId="UC_WorkOrderStep_1" Name="UC_WorkOrderSte
p_1" Description="Step Assembly 10" Sequence="10" Priority="1"
OperationStepCategoryNId="Default" ParentWOOpFolderNId="" RequiredCertificateNId=""
RequiredInspectionRole="" ToBeCollectedDocument="false" ElectronicSignaturePause="fal
se" ElectronicSignatureStart="false" ElectronicSignatureComplete="false"
EstimatedStartTime="2023-09-26T14:29:52.000Z" EstimatedDuration="PT4H1M1S"
EstimatedEndTime="2023-09-27T14:25:45.000Z">
<StepInterlockingChecks>
<StepInterlockingCheck NId="AllPartsAssembled"
Outbound="true"/>
<StepInterlockingCheck NId="AllStepsCompleted"
Inbound="true"/>
</StepInterlockingChecks>
<StepMaterials>
<StepMaterial NId="Glue" Name="Glue" Quantity="1" UoM="
l" SpecificationType="Reference" UId="Glue" Revision="A" OccurrenceId="" Sequence=""
LogicalPosition="" GroupId="" AlternativeSelected=""/>
<StepMaterial NId="LandingGear777" Name="LandingGear7
77" Quantity="2" SpecificationType="NormalPart" UId="LandingGear777" Revision="A"
OccurrenceId="" Sequence="" LogicalPosition="" GroupId="" AlternativeSelected=""/>
<StepMaterial NId="Pivot" Name="Pivot" Quantity="3"
SpecificationType="RangePart" UId="Pivot" Revision="A" OccurrenceId="" Sequence=""
LogicalPosition="" GroupId="" AlternativeSelected=""/>
<StepMaterial NId="RetractableLandingGear" Name="Retr
actableLandingGear" Quantity="4" SpecificationType="Alternative" UId="RetractableLand
ingGear" Revision="A" OccurrenceId="" Sequence="" LogicalPosition="" GroupId="2"
AlternativeSelected="True"/>
<StepMaterial NId="ScrewMX" Name="ScrewMX" Quantity="
5" SpecificationType="Alternative" UId="ScrewMX" Revision="A" OccurrenceId=""
Sequence="" LogicalPosition="" GroupId="2" AlternativeSelected="False"/>
<StepMaterial NId="Wheel" Name="Wheel" Quantity="6"
SpecificationType="AsRequired" UId="Wheel" Revision="A" OccurrenceId="" Sequence=""
LogicalPosition="" GroupId="" AlternativeSelected=""/>
</StepMaterials>
<StepTools>
<StepTool TimesToBeUsed="1" DefinitionNId="Hammer"/>
<StepTool TimesToBeUsed="2" DefinitionNId="Wrench"
Revision="A"/>
</StepTools>
<StepWorkInstructions>
<StepWorkInstruction DefinitionNId="AssembleLandingGe
ar" AssociationType="SerialNumber"/>
<StepWorkInstruction DefinitionNId="AssembleWheel"
AssociationType="Operation"/>

<StepWorkInstruction DefinitionNId="DifferentialRotat
ionValues" AssociationType="SerialNumberOnDemand" Revision="A"/>
</StepWorkInstructions>
<StepQualityInspections>
<StepCharacteristicRepresentation NId="AssemblePivotT
est" Revision="A"/>
<StepCharacteristicRepresentation NId="AssembleScrewT
est" Revision="A"/>
<StepCharacteristicRepresentation NId="AssembleLandin
gGearTest" Revision="A"/>
</StepQualityInspections>
<StepSkills>
<StepSkill NId="SkillDriller" Level="1"/>
<StepSkill NId="SkillTapping" Level="2"/>
</StepSkills>
<StepDocuments>
<StepDocument NId="AssembleInstructionsManual"
Revision="A"/>
</StepDocuments>
<StepHumanResources>
<StepHumanResource CertificationNId="DE_Driller"
RequiredNumber="1"/>
<StepHumanResource CertificationNId="DE_Tapping"
RequiredNumber="2"/>
</StepHumanResources>
</WorkOrderStep>
<WorkOrderStep NId="UC_WorkOrderStep_2" Name="UC_WorkOrderSte
p_2" Description="Step Assembly 20" Sequence="20" Priority="2"
OperationStepCategoryNId="Default" ParentWOOpFolderNId="" RequiredCertificateNId=""
RequiredInspectionRole="" ToBeCollectedDocument="false" ElectronicSignaturePause="fal
se" ElectronicSignatureStart="false" ElectronicSignatureComplete="false"
EstimatedStartTime="2023-09-26T14:29:52.000Z" EstimatedDuration="PT4H1M1S"
EstimatedEndTime="2023-09-27T14:25:45.000Z">
<StepInterlockingChecks/>
<StepMaterials/>
<StepTools/>
<StepWorkInstructions/>
<StepQualityInspections/>
<StepSkills/>
<StepDocuments/>
<StepHumanResources/>
</WorkOrderStep>
<WorkOrderStep NId="UC_WorkOrderStep_3" Name="UC_WorkOrderSte
p_3" Description="Step Assembly 20" Sequence="30" Priority="3"
OperationStepCategoryNId="Default" ParentWOOpFolderNId="" RequiredCertificateNId=""
RequiredInspectionRole="" ToBeCollectedDocument="false" ElectronicSignaturePause="fal
se" ElectronicSignatureStart="false" ElectronicSignatureComplete="false"
EstimatedStartTime="2023-09-26T14:29:52.000Z" EstimatedDuration="PT4H1M1S"
EstimatedEndTime="2023-09-27T14:25:45.000Z"/>
</WorkOrderSteps>
<StepDependencies>
<StepDependency From="UC_WorkOrderStep_1" To="UC_WorkOrderSte
p_2"/>

<StepDependency From="UC_WorkOrderStep_2" To="UC_WorkOrderSte
p_3"/>
</StepDependencies>
</WorkOrderOperation>
<WorkOrderOperation NId="UC_WorkOrderOperation_2" Name="UC_WorkOrderO
peration_2" Description="UC_WorkOrderOperation_2" Sequence="20" Priority="2"
OperationStepCategoryNId="Default" WorkOperationTypeNId="Standard"
ParentWOOpFolderNId="" RequiredCertificateNId="" RequiredInspectionRole=""
ToBeCollectedDocument="false" ElectronicSignaturePause="false"
ElectronicSignatureStart="false" ElectronicSignatureComplete="false"
EstimatedStartTime="2023-09-26T14:29:52.000Z" EstimatedDuration="PT4H1M1S"
EstimatedEndTime="2023-09-27T14:25:45.000Z"/>
</WorkOrderOperations>
<OperationDependencies>
<OperationDependency From="UC_WorkOrderOperation_1" Type="AfterEnd"
PartialCompleted="True" To="UC_WorkOrderOperation_2"/>
</OperationDependencies>
</WorkOrder>
<WorkOrder NId="WO_UC4" Name="WO_UC4" ProductionType="Serialized" Quantity="1
" BatchId="" Product="LandingGear777" Status="New" Priority="1" DueDate="2023-09-30T1
4:18:37.000Z" EstimatedStartTime="2023-09-26T14:19:52.000Z" EstimatedEndTime="2023-09
-28T14:19:52.000Z"/>
</Define>
<Remove>
<WorkOrder NId="WO_UC2"/>
<WorkOrder NId="WO_UC3"/>
</Remove>
</ImportDataFlow>

• The <ImportDataFlow> tag specifies that the scope of the document is to define an Import message using the
FullWorkOrder data flow provided by the system and relative to a specific plant (Plant1), among those that
have been configured.
• If the Plant contains only one piece of information (for example, PLANT01), then this is used both as
Plant Id in case of a Multiplant scenario, and as the Plant field of the Work Order.
• If the Plant contains two pieces of information (for example, PLANT01.ENTERPRISE1), then the first part
(PLANT01) is used as Plant Id in case of a Multiplant scenario, while the second part (ENTERPRISE1) is
used as the Plant field of the Work Order.
• If the Plant contains more pieces of information (for example, PLANT01.ENTERPRISE1.SITE1) then the
first part (PLANT01) is used as Plant Id in case of a Multiplant scenario, while the second part
(ENTERPRISE1.SITE1) is used as the Plant field of the Work Order.
• If either MasterPlanNId or AsPlannedNId is valorized, the UId corresponds to the field that has been valorized.
• If MasterPlanNId is valorized, the Work Order is created from the Master Plan with the information contained in
the XML file. If AsPlannedNId is valorized, the Work Order is created from the As Planned BOP with the
information contained in the XML file.
• The MasterPlanNId value of the XML file must be equal to the NId value of the MasterPlan entity.
• The AsPlannedNId value of the XML file must be equal to the PBOPIdentID value of the AsPlannedBOP entity.
• The OperationNId value (or the StepNId value) of either the Master Plan or As Planned BOP must be equal to
the NId of the <WorkOrderOperation> tag of the XML file. If the NId present in the XML is different, the
operation is not created.
• If MasterPlanNId is valorized, the Work Order is created with the Operations and Steps specified in the XML file.
The XML file is used also to resolve the Master Plan. For what concerns specifications (for example Materials,
Tools), those present in the XML file are created in the Work Order, without considering those contained in the
Master Plan. The specifications that are not present in the XML file are retrieved from the Master Plan. For

example, if the XML file contains Operation1 with Material3, and the Master Plan contains Operation1 with
Material1 and Tool1, then the Work Order is created with Operation1, Material3 and Tool1.
• If AsPlannedNId is valorized, the Work Order is created with the Operations and Steps specified in the As
Planned BOP. For what concerns specifications (for example Materials, Tools), those present in the XML file are
created in the Work Order, without considering those contained in the As Planned BOP. The specifications that
are not present in the XML file are retrieved from the As Planned BOP. For example, if the XML file contains
Operation1 with Material3, and the As Planned BOP contains Operation1 with Material1 and Tool1, then the
Work Order is created with Operation1, Material3 and Tool1.
• For what concerns dependencies between Operations and Steps:
• for the Master Plan, the dependencies present in the XML file are considered.
• for the As Planned BoP, the dependencies present in the BoP are considered. If they are not present, they
will be retrieved from the XML file.
• All Work Orders to be imported into Opcenter Execution Discrete must be listed within the <Define> tag, where
the <WorkOrder> tag specifies the attributes listed in the table below.
• All previously imported Work Orders that are no more available in the External System and consequently must
be removed from Opcenter Execution Discrete, must be listed within the <Remove> tag, instead of the <Define>
tag, specifying the related Identifiers (NId attribute).

<Define> Attributes
A description for all the attributes can be found in the related Reference Guides.
Attributes

Description

Occurrence

NId

Natural Identifier of the Work Order.

Mandatory

Attributes

Description

Occurrence

ProductionType

• Serialized - Indicates that, at the time of the
Work Order creation, serial numbers
representing the number of items that the Work
Order is expected to produce, must be
associated to the Work Order.
• FullQuantity - Indicates that the next Work
Order Operation can start only after the entire
quantity of the previous Work Order Operation
has been produced.
• FullSerialized - Indicates that the Work Order
will produce multiple Material Tracking Units of
the same type, and each of them will be assigned
with a serial number.
• TransferBatch - Indicates that the next Work
Order Operation can start after a portion of the
entire material batch is completed. The
remaining portion can be moved to a successive
Work Order Operation.
• FlexibleBatch - Indicates that the Work Order
created is a flexible batch and the user can
modify the quantity to be produced based on the
plant conditions (status of the equipment, end of
shifts, and so on).
• FlexibleSerialized - Indicates that the Work
Order is created stepwise and is flexible. The user
can modify the quantity to be produced based on
the plant conditions (status of the equipment,
end of shifts, and so on).

Mandatory

Quantity

The quantity of Material that the Work Order is
expected to produce.

Mandatory

If a Process Final Material is present, the
Work Order's Quantity will coincide with
the Quantity of the Process.

MasterPlanNId

Natural identifier of the Master Plan to which you
want to associate the Work Order.

Optional

AsPlannedNId

Natural identifier of the As Planned BOP to which
you want to associate the Work Order.

Optional

Attributes

Description

Occurrence

UId

Unique identifier of either the Master Plan or the As
Planned BOP.

Optional

Name

Name of the Work Order.

Mandatory

BatchId

(Only if the Production Type is set to
FullQuantity, TransferBatch or FlexibleBatch)

Optional

The unique identifier of the Material Batch that the
Work Order is expected to produce.
Product

The Material that the Work Order is expected to
produce.

Mandatory

ProductRevision

The Revision of the Material that the Work Order is
expected to produce. If the value is not specified, the
default Revision will be used (A).

Optional

ProductUId

The Unique Identifier of the Material that the Work
Order is expected to produce. If the value is not
specified, the default UId will be used
(ProductNId_Revision).

Optional

ProductUoM

The Unit of Measure of the Material that the Work
Order is expected to produce. If the value is not
specified, it will be used the UoM of the Material that
you want to produce.

Optional

ERPOrder

Identifier of the related ERP order, if applicable.

Optional

Priority

A number identifying the order of execution of the
Work Orders.

Optional

DueDate

The date by which the Work Order must be
completed. The date format is: yyyy-MMddThh:mm:ssZ.

Optional

EstimatedStartTime

The date and time when the Work Order execution is
expected to start. The timestamp must respect the
UTC format: for example, yyyy-MM-ddThh:mm:ssZ.

Optional

Attributes

Description

Occurrence

EstimatedEndTime

The date and time when the Work Order execution is
expected to end. The timestamp must respect the
UTC format: for example, yyyy-MM-ddThh:mm:ssZ.

Optional

Status

The status of the Work Order:

Optional

• if Edit has been set, the Work Order is created
but not released.
• if New has been set, the Work Order is created
and released.
• if ReadyForScheduling has been set, the Work
Order is created as ready to be scheduled.
If none or other values are set, the Work Order is
created in Edit status.
<Serial Numbers>

List of <SerialNumber> elements.

Optional

<OperationDependencies>

List of <OperationDependency> elements.

Optional

<WorkOrderOperations>

List of <WorkOrderOperation> elements.

Optional

Serial Number
Attributes

Occurrence

Code

Mandatory

Operation Dependency
Attributes

Occurrence

From

Mandatory

To

Mandatory

Type

Mandatory

PartialCompleted

Optional

Work Order Operation

Attributes

Occurrence

NId

Mandatory

Name

Mandatory

Sequence

Mandatory

Description

Optional

Priority

Optional

OperationStepCategoryNId

Optional

WorkOperationTypeNId

Optional

ParentWOOpFolderNId

Optional

RequiredCertificateNId

Optional

RequiredInspectionRole

Optional

ToBeCollectedDocument

Optional

ElectronicSignaturePause

Optional

ElectronicSignatureStart

Optional

ElectronicSignatureComplete

Optional

EstimatedStartTime

Optional

EstimatedDuration

Optional

EstimatedEndTime

Optional

<InterlockingChecks>

Optional

<Users>

Optional

Attributes

Occurrence

<Machines>

Optional

<Materials>

Optional

<Tools>

Optional

<WorkInstructions>

Optional

<QualityInspections>

Optional

<Skills>

Optional

<Documents>

Optional

<HumanResources>

Optional

<StepDependencies>

Optional

<WorkOrderSteps>

Optional

Interlocking Check
At least one between Inbound and Outbound must be present and its value must be set to true.
Attributes

Occurrence

NId

Mandatory

Inbound

Optional

Outbound

Optional

User
Attributes

Occurrence

NId

Mandatory

Machine

At least one between NId and EquipmentType must be present.
Attributes

Occurrence

NId

Optional

EquipmentType

Optional

PartProgram

Optional

Material
Attributes

Occurrence

NId

Mandatory

UId

Mandatory

Revision

Mandatory

Quantity

Mandatory

UoM

Optional

SpecificationType

Mandatory

Name

Optional

OccurrenceId

Optional

Sequence

Optional

LogicalPosition

Optional

GroupId

Optional

AlternativeSelected

Optional

Tool

Attributes

Occurrence

DefinitionNId

Mandatory

TimesToBeUsed

Mandatory

Revision

Optional

Work Instruction
Attributes

Occurrence

DefinitionNId

Mandatory

AssociationType

Mandatory

Revision

Optional

Characteristic Representation
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Skill
Attributes

Occurrence

NId

Mandatory

Level

Mandatory

Document
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Human Resource
Attributes

Occurrence

CertificationNId

Mandatory

RequiredNumber

Mandatory

Step Dependency
Attributes

Occurrence

From

Mandatory

To

Mandatory

WorkOrderSteps
Attributes

Occurence

NId

Mandatory

Name

Mandatory

Sequence

Mandatory

Description

Optional

Priority

Optional

OperationStepCategoryNId

Optional

ToBeCollectedDocument

Optional

ElectronicSignatureComplete

Optional

EstimatedDuration

Optional

<StepInterlockingChecks>

Optional

<StepMaterials>

Optional

Attributes

Occurence

<StepTools>

Optional

<StepWorkInstructions>

Optional

<StepQualityInspections>

Optional

<StepSkills>

Optional

<StepDocuments>

Optional

<StepHumanResources>

Optional

Step Interlocking Check
At least one between Inbound and Outbound must be present and its value must be set to true.
Attributes

Occurrence

NId

Mandatory

Inbound

Optional

Outbound

Optional

Step Material
Attributes

Occurrence

NId

Mandatory

UId

Mandatory

Revision

Mandatory

Quantity

Mandatory

SpecificationType

Mandatory

Attributes

Occurrence

Name

Optional

OccurrenceId

Optional

Sequence

Optional

LogicalPosition

Optional

GroupId

Optional

AlternativeSelected

Optional

Step Tool
Attributes

Occurrence

DefinitionNId

Mandatory

TimesToBeUsed

Mandatory

Step Work Instruction
Attributes

Occurrence

DefinitionNId

Mandatory

AssociationType

Mandatory

Step Characteristic Representation
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Step Skill

Attributes

Occurrence

NId

Mandatory

Level

Mandatory

Step Document
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Step Human Resource
Attributes

Occurrence

CertificationNId

Mandatory

RequiredNumber

Mandatory

XSLT Transformation
The Opcenter Connect MOM workflow uses the FullWorkOrder.xslt file located at C:\Program
Files\Siemens\SimaticIT\Unified\VApps\UADM\MIOIntegration\Xslt to verify if the XML file described above
contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML files, one
containing the correct nodes that can be successfully imported, and one containing the wrong nodes that must be
logged.

##### JSON File for Full Work Orders

It is possible to automatically align the Work Orders contained in the Opcenter Execution Discretedatabase with
those available in the External System. This operation can be performed through a JSON file created according to
the structure below.
The entire structure of the Work Order is imported along with all the information related to its Work Order
Operations and Work Order Steps. In addition, if either a Master Plan or an As Planned BOP is indicated, the
information contained in the JSON file will be merged with those contained in the Master Plan or As Planned BOP.

JSON Structure
Here is an example of a JSON message that can be used to import the structure of the Work Order:
{
"MessageType": "FullWorkOrderJson",
"FlowName": "FullWorkOrder",

"Plant": "DefaultPlant.Plant",
"Define": {
"WorkOrders": [
{
"NId": "WO_UC1",
"Name": "WO_UC1",
"MasterPlanNId": "",
"AsPlannedNId": "",
"UId": "",
"ProductionType": "Serialized",
"Quantity": "1",
"BatchId": "",
"Product": "LandingGear777",
"ProductRevision": "A",
"ProductUId": "LandingGear777_UId",
"ProductUoM": "g",
"Status": "New",
"Priority": "1",
"DueDate": "2023-09-30T14:18:37.000Z",
"EstimatedStartTime": "2023-09-26T14:19:52.000Z",
"EstimatedEndTime": "2023-09-28T14:19:52.000Z",
"SerialNumbers": [
{
"Code": "SN1"
}
],
"WorkOrderOperations": [
{
"NId": "UC_WorkOrderOperation_1",
"Name": "UC_WorkOrderOperation_1",
"Description": "UC_WorkOrderOperation_1",
"Sequence": "10",
"Priority": "1",
"OperationStepCategoryNId": "Default",
"WorkOperationTypeNId": "Standard",
"ParentWOOpFolderNId": "",
"RequiredCertificateNId": "",
"RequiredInspectionRole": "",
"ToBeCollectedDocument": "false",
"ElectronicSignaturePause": "false",
"ElectronicSignatureStart": "false",
"ElectronicSignatureComplete": "false",
"EstimatedStartTime": "2023-09-26T14:29:52.000Z",
"EstimatedDuration": "PT4H1M1S",
"EstimatedEndTime": "2023-09-27T14:25:45.000Z",
"InterlockingChecks": [
{
"NId": "AllPartsAssembled",
"Outbound": "true"
},
{
"NId": "AllStepsCompleted",
"Inbound": "true"

}
],
"Users": [
{
"NId": "Administrator"
},
{
"NId": "Operator1"
}
],
"Machines": [
{
"NId": "Machine1"
},
{
"NId": "Machine2"
}
],
"Materials": [
{
"NId": "Glue",
"Name": "Glue",
"Quantity": "1",
"SpecificationType": "Reference",
"UId": "Glue",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
},
{
"NId": "LandingGear777",
"Name": "LandingGear777",
"Quantity": "2",
"SpecificationType": "NormalPart",
"UId": "LandingGear777",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
},
{
"NId": "Pivot",
"Name": "Pivot",
"Quantity": "3",
"SpecificationType": "RangePart",
"UId": "Pivot",
"Revision": "A",
"OccurrenceId": "",

"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
},
{
"NId": "RetractableLandingGear",
"Name": "RetractableLandingGear",
"Quantity": "4",
"SpecificationType": "Alternative",
"UId": "RetractableLandingGear",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": "True"
},
{
"NId": "ScrewMX",
"Name": "ScrewMX",
"Quantity": "5",
"SpecificationType": "Alternative",
"UId": "ScrewMX",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": "False"
},
{
"NId": "Wheel",
"Name": "Wheel",
"Quantity": "6",
"SpecificationType": "AsRequired",
"UId": "Wheel",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
}
],
"Tools": [
{
"TimesToBeUsed": "1",
"DefinitionNId": "Hammer"
},
{
"TimesToBeUsed": "2",
"DefinitionNId": "Wrench"

}
],
"WorkInstructions": [
{
"DefinitionNId": "AssembleLandingGear",
"AssociationType": "SerialNumber"
},
{
"DefinitionNId": "AssembleWheel",
"AssociationType": "Operation"
},
{
"DefinitionNId": "DifferentialRotationValues",
"AssociationType": "SerialNumberOnDemand"
}
],
"QualityInspections": [
{
"NId": "AssemblePivotTest",
"Revision": "A"
},
{
"NId": "AssembleScrewTest",
"Revision": "A"
},
{
"NId": "AssembleLandingGearTest",
"Revision": "A"
}
],
"Skills": [
{
"NId": "SkillDriller",
"Level": "1"
},
{
"NId": "SkillTapping",
"Level": "2"
}
],
"Documents": [
{
"NId": "AssembleInstructionsManual",
"Revision": "A"
}
],
"HumanResources": [
{
"CertificationNId": "DE_Driller",
"RequiredNumber": "1"
},
{
"CertificationNId": "DE_Tapping",

"RequiredNumber": "2"
}
],
"WorkOrderSteps": [
{
"NId": "UC_WorkOrderStep_1",
"Name": "UC_WorkOrderStep_1",
"Description": "Step Assembly 10",
"Sequence": "10",
"Priority": "1",
"OperationStepCategoryNId": "Default",
"ParentWOOpFolderNId": "",
"RequiredCertificateNId": "",
"RequiredInspectionRole": "",
"ToBeCollectedDocument": "false",
"ElectronicSignaturePause": "false",
"ElectronicSignatureStart": "false",
"ElectronicSignatureComplete": "false",
"EstimatedStartTime": "2023-09-26T14:29:52.000Z",
"EstimatedDuration": "PT4H1M1S",
"EstimatedEndTime": "2023-09-27T14:25:45.000Z",
"StepInterlockingChecks": [
{
"NId": "AllPartsAssembled",
"Outbound": "true"
},
{
"NId": "AllStepsCompleted",
"Inbound": "true"
}
],
"StepMaterials": [
{
"NId": "Glue",
"Name": "Glue",
"Quantity": "1",
"SpecificationType": "Reference",
"UId": "Glue",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
},
{
"NId": "LandingGear777",
"Name": "LandingGear777",
"Quantity": "2",
"SpecificationType": "NormalPart",
"UId": "LandingGear777",
"Revision": "A",
"OccurrenceId": "",

"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
},
{
"NId": "Pivot",
"Name": "Pivot",
"Quantity": "3",
"SpecificationType": "RangePart",
"UId": "Pivot",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
},
{
"NId": "RetractableLandingGear",
"Name": "RetractableLandingGear",
"Quantity": "4",
"SpecificationType": "Alternative",
"UId": "RetractableLandingGear",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": "True"
},
{
"NId": "ScrewMX",
"Name": "ScrewMX",
"Quantity": "5",
"SpecificationType": "Alternative",
"UId": "ScrewMX",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",
"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": "False"
},
{
"NId": "Wheel",
"Name": "Wheel",
"Quantity": "6",
"SpecificationType": "AsRequired",
"UId": "Wheel",
"Revision": "A",
"OccurrenceId": "",
"Sequence": "",

"LogicalPosition": "",
"GroupId": "",
"AlternativeSelected": ""
}
],
"StepTools": [
{
"TimesToBeUsed": "1",
"DefinitionNId": "Hammer"
},
{
"TimesToBeUsed": "2",
"DefinitionNId": "Wrench"
}
],
"StepWorkInstructions": [
{
"DefinitionNId": "AssembleLandingGear",
"AssociationType": "SerialNumber"
},
{
"DefinitionNId": "AssembleWheel",
"AssociationType": "Operation"
},
{
"DefinitionNId": "DifferentialRotationValues",
"AssociationType": "SerialNumberOnDemand"
}
],
"StepQualityInspections": [
{
"NId": "AssemblePivotTest",
"Revision": "A"
},
{
"NId": "AssembleScrewTest",
"Revision": "A"
},
{
"NId": "AssembleLandingGearTest",
"Revision": "A"
}
],
"StepSkills": [
{
"NId": "SkillDriller",
"Level": "1"
},
{
"NId": "SkillTapping",
"Level": "2"
}
],

"StepDocuments": [ {
"NId": "AssembleInstructionsManual",
"Revision": "A"
}
],
"StepHumanResources": [
{
"CertificationNId": "DE_Driller",
"RequiredNumber": "1"
},
{
"CertificationNId": "DE_Tapping",
"RequiredNumber": "2"
}
]
},
{
"NId": "UC_WorkOrderStep_2",
"Name": "UC_WorkOrderStep_2",
"Description": "Step Assembly 20",
"Sequence": "20",
"Priority": "2",
"OperationStepCategoryNId": "Default",
"ParentWOOpFolderNId": "",
"RequiredCertificateNId": "",
"RequiredInspectionRole": "",
"ToBeCollectedDocument": "false",
"ElectronicSignaturePause": "false",
"ElectronicSignatureStart": "false",
"ElectronicSignatureComplete": "false",
"EstimatedStartTime": "2023-09-26T14:29:52.000Z",
"EstimatedDuration": "PT4H1M1S",
"EstimatedEndTime": "2023-09-27T14:25:45.000Z",
"StepInterlockingChecks": [],
"StepMaterials": [],
"StepTools": [],
"StepWorkInstructions": [],
"StepQualityInspections": [],
"StepSkills": [],
"StepDocuments": [],
"StepHumanResources": []
},
{
"NId": "UC_WorkOrderStep_3",
"Name": "UC_WorkOrderStep_3",
"Description": "Step Assembly 30",
"Sequence": "30",
"Priority": "3",
"OperationStepCategoryNId": "Default",
"ParentWOOpFolderNId": "",
"RequiredCertificateNId": "",
"RequiredInspectionRole": "",
"ToBeCollectedDocument": "false",

"ElectronicSignaturePause": "false",
"ElectronicSignatureStart": "false",
"ElectronicSignatureComplete": "false",
"EstimatedStartTime": "2023-09-26T14:29:52.000Z",
"EstimatedDuration": "PT4H1M1S",
"EstimatedEndTime": "2023-09-27T14:25:45.000Z"
}
],
"StepDependencies": [
{
"From": "UC_WorkOrderStep_1",
"To": "UC_WorkOrderStep_2"
},
{
"From": "UC_WorkOrderStep_2",
"To": "UC_WorkOrderStep_3"
}
]
},
{
"NId": "UC_WorkOrderOperation_2",
"Name": "UC_WorkOrderOperation_2",
"Description": "UC_WorkOrderOperation_2",
"Sequence": "20",
"Priority": "2",
"OperationStepCategoryNId": "Default",
"WorkOperationTypeNId": "Standard",
"ParentWOOpFolderNId": "",
"RequiredCertificateNId": "",
"RequiredInspectionRole": "",
"ToBeCollectedDocument": "false",
"ElectronicSignaturePause": "false",
"ElectronicSignatureStart": "false",
"ElectronicSignatureComplete": "false",
"EstimatedStartTime": "2023-09-26T14:29:52.000Z",
"EstimatedDuration": "PT4H1M1S",
"EstimatedEndTime": "2023-09-27T14:25:45.000Z"
}
],
"OperationDependencies": [
{
"From": "UC_WorkOrderOperation_1",
"Type": "AfterEnd",
"PartialCompleted": "True",
"To": "UC_WorkOrderOperation_2"
}
]
},
{
"NId": "WO_UC4",
"Name": "WO_UC4",
"ProductionType": "Serialized",
"Quantity": "1",

"BatchId": "",
"Product": "LandingGear777",
"Status": "New",
"Priority": "1",
"DueDate": "2023-09-30T14:18:37.000Z",
"EstimatedStartTime": "2023-09-26T14:19:52.000Z",
"EstimatedEndTime": "2023-09-28T14:19:52.000Z",
"SerialNumbers": []
}
]
},
"Remove": {
"WorkOrders": [
{
"NId": "WO_UC2"
},
{
"NId": "WO_UC3"
}
]
}
}

• The following fields:
• "MessageType": "FullWorkOrderJson"
• "FlowName": "FullWorkOrder"
specify that the scope of the document is to define a JSON message using the FullWorkOrder data flow
provided by the system and relative to a specific plant (Plant1), among those that have been configured.
• If the Plant contains only one piece of information (for example, PLANT01), then this is used both as Plant Id in
case of a Multiplant scenario, and as the Plant field of the Work Order.
• If the Plant contains two pieces of information (for example, PLANT01.ENTERPRISE1), then the first part
(PLANT01) is used as Plant Id in case of a Multiplant scenario, while the second part (ENTERPRISE1) is used as
the Plant field of the Work Order.
• If the Plant contains more pieces of information (for example, PLANT01.ENTERPRISE1.SITE1) then the first part
(PLANT01) is used as Plant Id in case of a Multiplant scenario, while the second part (ENTERPRISE1.SITE1) is
used as the Plant field of the Work Order.
• If either MasterPlanNId or AsPlannedNId is valorized, the UId corresponds to the field that has been valorized.
• If MasterPlanNId is valorized, the Work Order is created from the Master Plan with the information contained in
the JSON file. If AsPlannedNId is valorized, the Work Order is created from the As Planned BOP with the
information contained in the JSON file.
• The MasterPlanNId value of the JSON file must be equal to the NId value of the MasterPlan entity.
• The AsPlannedNId value of the JSON file must be equal to the PBOPIdentID value of the AsPlannedBOP entity.
• The OperationNId value (or the StepNId value) of either the Master Plan or As Planned BOP must be equal to
the NId of the <WorkOrderOperation> tag of the JSON file. If the NId present in the JSON file is different, the
operation is not created.
• If MasterPlanNId is valorized, the Work Order is created with the Operations and Steps specified in the JSON
file. The JSON file is used also to resolve the Master Plan. For what concerns specifications (for example
Materials, Tools), those present in the JSON file are created in the Work Order, without considering those
contained in the Master Plan. The specifications that are not present in the JSON file are retrieved from the
Master Plan. For example, if the JSON file contains Operation1 with Material3, and the Master Plan contains
Operation1 with Material1 and Tool1, then the Work Order is created with Operation1, Material3 and Tool1.

• If AsPlannedNId is valorized, the Work Order is created with the Operations and Steps specified in the As
Planned BOP. For what concerns specifications (for example Materials, Tools), those present in the JSON file are
created in the Work Order, without considering those contained in the As Planned BOP. The specifications that
are not present in the JSON file are retrieved from the As Planned BOP. For example, if the JSON file contains
Operation1 with Material3, and the As Planned BOP contains Operation1 with Material1 and Tool1, then the
Work Order is created with Operation1, Material3 and Tool1.
• For what concerns dependencies between Operations and Steps:
• for the Master Plan, the dependencies present in the JSON file are considered.
• for the As Planned BoP, the dependencies present in the BoP are considered. If they are not present, they
will be retrieved from the JSON file.
• All Work Orders to be imported into Opcenter Execution Discrete must be listed within the "Define" object,
where the "WorkOrders" array specifies the Work Order objects that contain the fields listed in the table below.
• All previously imported Work Orders that are no more available in the External System and consequently must
be removed from Opcenter Execution Discrete, must be listed within the "Remove" array object, instead of the
"Define" array object, specifying the related Identifiers (NId field).

Fields of the "WorkOrders" Array Object
A description for all the fields can be found in the related Reference Guides.
Field

Description

Occurrence

NId

Natural Identifier of the Work Order.

Mandatory

Field

Description

Occurrence

ProductionType

• Serialized - Indicates that, at the time of the Work
Order creation, serial numbers representing the
number of items that the Work Order is expected
to produce, must be associated to the Work
Order.
• FullQuantity - Indicates that the next Work Order
Operation can start only after the entire quantity
of the previous Work Order Operation has been
produced.
• FullSerialized - Indicates that the Work Order will
produce multiple Material Tracking Units of the
same type, and each of them will be assigned with
a serial number.
• TransferBatch - Indicates that the next Work
Order Operation can start after a portion of the
entire material batch is completed. The remaining
portion can be moved to a successive Work Order
Operation.
• FlexibleBatch - Indicates that the Work Order
created is a flexible batch and the user can modify
the quantity to be produced based on the plant
conditions (status of the equipment, end of shifts,
and so on).
• FlexibleSerialized - Indicates that the Work Order
is created stepwise and is flexible. The user can
modify the quantity to be produced based on the
plant conditions (status of the equipment, end of
shifts, and so on).

Mandatory

Quantity

The quantity of Material that the Work Order is
expected to produce.

Mandatory

MasterPlanNId

Natural identifier of the Master Plan to which you
want to associate the Work Order.

Optional

AsPlannedNId

Natural identifier of the As Planned BOP to which you
want to associate the Work Order.

Optional

UId

Unique identifier of either the Master Plan or the As
Planned BOP.

Optional

Name

Name of the Work Order.

Mandatory

Field

Description

Occurrence

BatchId

(Only if the Production Type is set to
FullQuantity, TransferBatch or FlexibleBatch)

Optional

The unique identifier of the Material Batch that the
Work Order is expected to produce.
Product

The Material that the Work Order is expected to
produce.

Mandatory

ProductRevision

The Revision of the Material that the Work Order is
expected to produce. If the value is not specified, the
default Revision will be used (A).

Optional

ProductUId

The Unique Identifier of the Material that the Work
Order is expected to produce. If the value is not
specified, the default UId will be used
(ProductNId_Revision).

Optional

ProductUoM

The Unit of Measure of the Material that the Work
Order is expected to produce. If the value is not
specified, it will be used the UoM of the Material that
you want to produce.

Optional

ERPOrder

Identifier of the related ERP order, if applicable.

Optional

Priority

A number identifying the order of execution of the
Work Orders.

Optional

DueDate

The date by which the Work Order must be
completed. The date format is: yyyy-MMddThh:mm:ssZ.

Optional

EstimatedStartTime

The date and time when the Work Order execution is
expected to start. The timestamp must respect the
UTC format: for example, yyyy-MM-ddThh:mm:ssZ.

Optional

EstimatedEndTime

The date and time when the Work Order execution is
expected to end. The timestamp must respect the
UTC format: for example, yyyy-MM-ddThh:mm:ssZ.

Optional

Field

Description

Occurrence

Status

The status of the Work Order:

Optional

• if Edit has been set, the Work Order is created but
not released.
• if New has been set, the Work Order is created
and released.
• if ReadyForScheduling has been set, the Work
Order is created as ready to be scheduled.
If none or other values are set, the Work Order is
created in Edit status.
"Serial Numbers"

Array of "SerialNumber" objects.

Optional

"OperationDependencies"

Array of "OperationDependency" objects.

Optional

"WorkOrderOperations"

Array of "WorkOrderOperation" objects.

Optional

Serial Number
Attributes

Occurrence

Code

Mandatory

Operation Dependency
Attributes

Occurrence

From

Mandatory

To

Mandatory

Type

Mandatory

PartialCompleted

Optional

Work Order Operation
Attributes

Occurrence

NId

Mandatory

Attributes

Occurrence

Name

Mandatory

Sequence

Mandatory

Description

Optional

Priority

Optional

OperationStepCategoryNId

Optional

WorkOperationTypeNId

Optional

ParentWOOpFolderNId

Optional

RequiredCertificateNId

Optional

RequiredInspectionRole

Optional

ToBeCollectedDocument

Optional

ElectronicSignaturePause

Optional

ElectronicSignatureStart

Optional

ElectronicSignatureComplete

Optional

EstimatedStartTime

Optional

EstimatedDuration

Optional

EstimatedEndTime

Optional

"InterlockingChecks"

Optional

"Users"

Optional

"Machines"

Optional

Attributes

Occurrence

"Materials"

Optional

"Tools"

Optional

"WorkInstructions"

Optional

"QualityInspections"

Optional

"Skills"

Optional

"Documents"

Optional

"HumanResources"

Optional

"StepDependencies"

Optional

"WorkOrderSteps"

Optional

Interlocking Check
At least one between Inbound and Outbound must be present and its value must be set to true.
Attributes

Occurrence

NId

Mandatory

Inbound

Optional

Outbound

Optional

User
Attributes

Occurrence

NId

Mandatory

Machine
At least one between NId and EquipmentType must be present.

Attributes

Occurrence

NId

Optional

EquipmentType

Optional

PartProgram

Optional

Material
Attributes

Occurrence

NId

Mandatory

UId

Mandatory

Revision

Mandatory

Quantity

Mandatory

UoM

Optional

SpecificationType

Mandatory

Name

Optional

OccurrenceId

Optional

Sequence

Optional

LogicalPosition

Optional

GroupId

Optional

AlternativeSelected

Optional

Tool
Attributes

Occurrence

DefinitionNId

Mandatory

Attributes

Occurrence

TimesToBeUsed

Mandatory

Revision

Optional

Work Instruction
Attributes

Occurrence

DefinitionNId

Mandatory

AssociationType

Mandatory

Revision

Optional

Characteristic Representation
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Skill
Attributes

Occurrence

NId

Mandatory

Level

Mandatory

Document
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Human Resource

Attributes

Occurrence

CertificationNId

Mandatory

RequiredNumber

Mandatory

Step Dependency
Attributes

Occurrence

From

Mandatory

To

Mandatory

WorkOrderSteps
Attributes

Occurence

NId

Mandatory

Name

Mandatory

Sequence

Mandatory

Description

Optional

Priority

Optional

OperationStepCategoryNId

Optional

ToBeCollectedDocument

Optional

ElectronicSignatureComplete

Optional

EstimatedDuration

Optional

"StepInterlockingChecks"

Optional

"StepMaterials"

Optional

"StepTools"

Optional

Attributes

Occurence

"StepWorkInstructions"

Optional

"StepQualityInspections"

Optional

"StepSkills"

Optional

"StepDocuments"

Optional

"StepHumanResources"

Optional

Step Interlocking Check
At least one between Inbound and Outbound must be present and its value must be set to true.
Attributes

Occurrence

NId

Mandatory

Inbound

Optional

Outbound

Optional

Step Material
Attributes

Occurrence

NId

Mandatory

UId

Mandatory

Revision

Mandatory

Quantity

Mandatory

SpecificationType

Mandatory

Name

Optional

Attributes

Occurrence

OccurrenceId

Optional

Sequence

Optional

LogicalPosition

Optional

GroupId

Optional

AlternativeSelected

Optional

Step Tool
Attributes

Occurrence

DefinitionNId

Mandatory

TimesToBeUsed

Mandatory

Step Work Instruction
Attributes

Occurrence

DefinitionNId

Mandatory

AssociationType

Mandatory

Step Characteristic Representation
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Step Skill
Attributes

Occurrence

NId

Mandatory

Attributes

Occurrence

Level

Mandatory

Step Document
Attributes

Occurrence

NId

Mandatory

Revision

Optional

Step Human Resource
Attributes

Occurrence

CertificationNId

Mandatory

RequiredNumber

Mandatory

XSLT Mapping
In order to allow the import of the JSON file, a transformation must be applied. The Workflow de-serializes the
JSON file and subsequently an XSLT file converts the de-serialized JSON into the corresponding XML format needed
to import data. The name of the XSLT file is MapFullWorkOrder.xslt file located at C:\Program
Files\Siemens\SimaticIT\Unified\VApps\UADM\MIOIntegration\Xslt. The transformation will result in an XML file,
structured as described here.

XSLT Transformation
The Opcenter Connect MOM workflow uses the FullWorkOrder.xslt file located at C:\Program
Files\Siemens\SimaticIT\Unified\VApps\UADM\MIOIntegration\Xslt to verify if the converted JSON file described
above contains logical errors (e.g. missing values for mandatory attributes) and to split its content into two XML
files, one containing the correct nodes that can be successfully imported, and one containing the wrong nodes that
must be logged.

#### Verifying the Use Case Configuration

After creating an XML file following the example provided for the use case of interest, you can verify if it will work
properly by following the steps below.

Procedure
1. Copy the XML file in the inbound folder specified in the File Adapter Configuration. The XML file will be
automatically processed and removed from the folder.
2. Verify if the response message is available in the outbound folder specified in the File Adapter Configuration.
3. In Opcenter EX DS, verify if the use case has been satisfied, for example, in case of Automatic Start of Work Order
Operation, check that the Work Order Operation start has been traced in the As-Built page.

You can monitor the message exchange as follows:
• for what Opcenter CN MOM concerns,
• through the History page: a diagnostic page you can access from Opcenter Connect MOM Web
Application > System Diagnostic, in which you can filter the logs (for example by message type
or by adapter).
• using the Microsoft Windows Event Viewer (Applications and Services Logs > MIO).
• for Opcenter EX DS, using the standard ETW viewer.

#### How to Send Output Messages to Opcenter CN MOM

Through a dedicated workflow, it is possible to configure the integration with Opcenter Connect MOM for Output
Messages.
The related XSD files can be found in the following folder:
%SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\XSD.
As Output Messages are created from a specific Plant execution, and it is the Message Destination that
specifies which is the destination adapter for a certain Message Definition, it is possible to target the same
destination adapter from different plants and address specific plant adapters.
All Output Messages anyway contain information about the Plant on which they have been generated, in
order to give the possibility to the recipient to read it.
The Plant information contained in Output Messages is created by the following algorithm:
• If the Message is not generated from a Workplace, then the Plant attribute in the Message will be a
Foundation Plant. For example: Plant01.
• If the Foundation Plant is the same as that of the Equipment Plant, then the Plant attribute in the
Message will contain the same Plant information. For example: Plant01.
• If the Foundation Plant is different from the Equipment Plant, then the Plant attribute in the Message
will be the concatenation of two fields. For example: Plant01.Enterprise01, where Plant01 is the
Foundation Plant and Enterprise01 is the Equipment Plant.
For additional information, refer to the Opcenter Connect MOM User Guide.

Workflow
1. Configure the Message Type.
2. Configure the Channel.
3. Define the File Adapter.
4. Configure the Client Gateway.
5. Reset IIS and restart the Opcenter Connect MOM Channel Adapter Host Service to activate the configuration.

##### Configuring the Message Types for Output Messages

The first step is to create one or more Message Types specific to Output Messages. The Message Type must match
the field Broker Message Type configured during the creation of the Output Message Destination in Opcenter
Execution Discrete.

Procedure
1. Log in to the Opcenter Connect MOM Web Application.
2. In the General Configuration tile, click the Message Types tab.

3. Click the Add Object
Object:

icon, to create a new Message Type with the following properties and then click Add

Parameter

Value

Name

(Mandatory) The name of the Output Message.

Description

Additional information on the Output Message.

Dispatch Rule

(Mandatory) fifowithpredecessors

Dispatch Type

Broker Dispatch

4. Select Content Converters and change the value of Content Converter Plugin to OriginalFormat.
5. Leave the other attributes as default (recommended) and click Save

.

##### Configuring the Channel for Output Messages

After creating the Message Type, create a Message Channel and configure it to manage the Message Type.

Procedure
1. Log in to the Opcenter Connect MOM Web Application.
2. In the General Configuration tile, click the Message Channels tab.
3. Click the Add Object
click Add Object:

icon, to create a new Message Channel with the following properties and then

Parameter

Value

Name

OpcenterEXDSOutboundChannel

Description

For example: OutboundChannelForEXDS

Is Active

Selected

Map Message

Selected

4. Select the OpcenterEXDSOutboundChannel Message Channel.
5. Select Valid Message Types and click
specific to Output Messages.

in the Valid Message Types section, to add the valid Message Types

##### Configuring the File Adapter for Output Messages

After defining the Message Channel, it is necessary to create one or more File Adapters specific to Output Messages.
The File Adapter must match the field Broker Adapter Name, which you have configured during the creation of the
Message Destination. The Adapter must be assigned to the Message Channel created before and to a proper MOM
Connection, which is one of those created for all the inbound use cases.

Procedure
1. Log in to the Opcenter Connect MOM Web Application.
2. In the Adapter Configuration tile, click the File tab.
3. Click the Add Object
Object:

icon, to create a new File Adapter with the following properties and then click Add

Parameter

Value

Name

For example: opcenterexdsoutbound
Note Lower case is mandatory.

Description

For example: File Adapter for Outbound data on
OpcenterEXDS

Channel Source

MIOChannelSource

Message Channel

OpcenterEXDSOutboundChannel

Inbound Name Format

{messagename}

Outbound Name Format

Define a file name format according to your needs (for
example, response_{messagename}).
Refer to section Appendix B: Message Name Format
Keywords of the Manufacturing Interoperability User Guide.

Is Active

Selected

4. Select the opcenterexdsoutbound File Adapter and click
.
5. Select File Adapter Configuration and configure the following parameters:
Parameter

Value

Inbound URI

(Optional, since this is an outbound adapter) The path to the folder
where the input files might be placed, for example: C:
\OpcenterEXDSOutbound\inbound

Outbound URI

The path to the folder where the output files will be placed, for
example: C:\OpcenterEXDSOutbound\outbound

6. Select Additional Configuration and then configure the following parameter:
Parameter

Value

Mom Connection Name

The name of the MOM Connection configured before.

7. Click Save

.

##### Configuring the Client Gateway for Output Messages

The Client Gateway configuration enables you to simplify outbound communications between Opcenter EX DS and
the Opcenter Connect MOM Web Application and must be assigned to a valid MOM Connection. The Client Gateway
has been previously installed on each Opcenter Execution Foundation host.

Procedure
1. Log in to the Opcenter Connect MOM Web Application.
2. In the General Configuration tile, click the Client Gateways tab.
3. Select Base Configuration, click

and then set the following parameters:

Parameter

Value

Name

The name you have assigned to the Client Gateway when you
have installed it.

Description

Exposes an interface to receive outbound messages from the
MOM applications.

Control Address

http://+:13024/ClientGateway/

Control Authentication Type

None

Message Channel

OpcenterEXDSOutboundChannel

MOM Connection Name

The name of the MOM connection created before.

Message Name Format

Define a file name format according to your needs (for
example: {messagetype}_{messagename}_{messageid})
Refer to section Appendix B: Message Name Format
Keywords of the Opcenter Connect MOM User Guide.

Client Gateway Host Name

The name of the machine where the Client Gateway is
installed.

Is Active

Selected

4. Click Save
.
5. Select Additional Configuration and check that the attribute Clear Original Contents is set to false.
6. Restart the SIMATIC IT UAF Service on the Opcenter Execution Foundation machines.
From the Opcenter Connect MOM Web Application, it is possible to check if the Client Gateway is properly
configured and communicates with the Opcenter Connect MOM server (System Diagnostics tile > System
Health). In this page, the list of all Opcenter CN MOM components is shown, including the Client Gateway.
If correctly configured, the Client Gateway State is Active.

### How to Integrate with Teamcenter Share

The integration with Teamcenter Share allows you to share documents (for example, documents attached to NonConformances) to other users connected to the same Teamcenter Share environment.
For more information, see section Teamcenter Share of the Opcenter Execution Discrete Product Overview.

Workflow
1. Configure your system in order to support the integration with Teamcenter Share, as explained in section
Teamcenter Share Integration Support of the Opcenter Execution Foundation Installation Guide.
2. Set the Enable Teamcenter Share Integration configuration key, as explained in section Integration
Configuration Settings of the Opcenter Execution Discrete User Manual.

### How to Integrate Opcenter Execution Discrete with Additive Manufacturing Network

Opcenter Execution Discrete can be integrated with Additive Manufacturing Network, the Siemens cloud-based
solution designed to optimize execution activities in a capillary manner, from sale orders to delivery, in Additive
Manufacturing contexts.
Thanks to the exchange of information between Opcenter Execution Discrete and Additive Manufacturing Network,
ready Print Jobs (which correspond to Opcenter EX DS Execution Groups) can be imported into Opcenter EX DS, as
well as 3D Printers and related Printer Types, to streamline Shop Floor operations.
During these production activities, if changes are made to production, Opcenter EX DS will send data to Additive
Manufacturing Network to automatically notify the production status.
To correctly achieve this integration, you need to perform the operations described in the Workflow below.
For additional information on Additive Manufacturing Network, see its specific documentation.

Prerequisites
• Opcenter Execution Discrete is installed and configured correctly, included the required Apps and Extension
Apps:
• AMNInt
• AppU4DMAMN
• Printer3DAMN
• A user account has been configured in Additive Manufacturing Network.
• A machine with access to Additive Manufacturing Network host is available.

Workflow
Integrating Opcenter EX DS with Additive Manufacturing Network involves performing the following steps:
1. Enable integration with Opcenter EX DS in the Additive Manufacturing Network environment.
2. Set AMN Integration configuration keys as described in page AMN Integration Configuration Settings of the
Opcenter Execution Discrete User Manual.

#### Enabling Integration with Opcenter EX DS in the AM Network Environment

To enable integration with Opcenter Execution Discrete in the Additive Manufacturing Network environment, you
must generate the Client ID and Client Secret to be copied into Opcenter EX DS dedicated configuration keys.

Keep in mind that, if the generated credentials are not saved, new credentials must be generated.

Procedure
1. In the Additive Manufacturing Network environment, click Settings > Admin Panel.
2. In the Integrations tab, click Generate New Client ID and insert the following parameters:
Parameter

Description

Application Name

Type the name of the Application for which credentials must be
generated.

Type

From the drop-down menu, select the type corresponding to
your organization. For example, Production.

Organization Name

From the drop-down menu, select the name of your organization
(previously created in the Organizations tab).

3. Click Generate to generate the Client ID and Client Secret.
4. In the pane which opens, click either Download or Copy Secret Access Key.
5. In Opcenter EX DS, copy the generated credentials in the Client ID and Client Secret fields of the AMN
Integration Configuration Keys.

### How to Integrate Opcenter Execution Discrete with the Shop Floor

Opcenter Execution Discrete can integrate with the Shop Floor leveraging on a standardized way to manage OPC UA
tags via Automation Gateway. This standardized way relies on pre-defined handshake protocols and so-called
contracts.
For more information, see section Integration with the Shop Floor via OPC UA of the Opcenter Execution Discrete
Product Overview.
Opcenter Execution Discrete provides the following out of the box contracts:
• RequestOrderInfo
• ExecuteSaveSequence
• RequestNext
• ExecuteWorkOrderOperation
• ReqMaterialConsumption
• ExecConsumeMaterials
• TrackItemLocation
• ExecuteWorkInstructionDataCollection
• ExecuteQualityInspection
To use these contracts, some configurations must be applied to your system, as indicated in the following sections.

Target User
Integration configuration is reserved for System Integrators and Product Engineers. At runtime the integration is
triggered by Machines.

Prerequisites
• Opcenter Execution Discrete is installed and configured correctly.
• Automation Gateway Host configuration and activation is done correctly.

Workflow
Integrating Opcenter EX DS with Shop Floor (OPC UA interface & Automation Gateway) involves performing the
following steps:
1. Configure and Activate Automation Gateway Channels
2. Import the Automation Node Types
3. Create the Automation Node Instances
4. Bind Automation Node Parameters with OPC Tags
5. Approve Automation Node Types and Instances
6. Activate Types and Instances
7. Import the Signal Rules.
8. Configure Heartbeat Mechanism
In order to fully use integration with the Shop Floor, it is also necessary to correctly configure your runtime
application by:
• mapping the Equipment Configurations related to Machines to Automation Node Instances
• associate these Equipment Configurations to Work Order Operations.
For more information, refer to the Opcenter Execution Discrete User Manual.

#### Configuring and Activating Automation Gateway Channels

Automation Channels, through which Automation Node Instances connect to the field, must be configured and
approved before you create the Automation Node Type and Automation Node Instance.
For more information on Configuring and Activating Automation Gateway Channels, see the Configuring Automation
Channels chapter in Opcenter Execution Foundation User Manual.

Importing the Automation Node Types
1. On the Automation Gateway Administration page, choose the Import option that suits your needs. For more
information on the available Import options, see the Importing Automation Node Master Data for Automation
Artifacts chapter in Opcenter Execution Foundation User Manual.
2. Browse the installation folder %SITUnifiedSystemRoot %VApps\UADM\AutomationConfiguration and
navigate in the folder related to the Use Case that you want to use and select the CSV file related to the
Automation Node Type for that specific use case.
3. Click Save.

Creating the Automation Node Instances
Create the Automation Node Instances from each Automation Node Type according to the project Shop Floor
environment.

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

Binding Automation Node Parameters with OPC Tags
Bind each Automation Node Instance parameter with each OPC Tag using the Smart Binding feature provided by
the Automation Gateway app. For more information on binding Automation Node Parameters with OPC Tags, see
the Setting Automation Parameter Attributes for OPC UA Automation Node Instances chapter in Opcenter Execution
Foundation User Manual.

Approving Automation Node Types and Instances
The imported Automation Node Types & Instances are set to Approved by default. For more information on
Approving Automation Node Types & Instances, see the Importing Automation Node Master Data for Automation
Artifacts chapter in Opcenter Execution Foundation User Manual.

Activating Types and Instances
1. Click

Automation Gateway Management in side menu bar and click Home.

2. In Automation Gateway Management page, click
.
3. From the drop-down list select Types and Instances and confirm the operation.
For more information on Activating Types & Instances, see the Activating Runtime Integration chapter in Opcenter
Execution Foundation User Manual.

Importing the Signal Rules
1. On the Signal Rule Management page, choose the Import option. For more information on the available
Import options, see the Importing Automation Node Master Data for Automation Artifacts chapter in Opcenter
Execution Foundation User Manual.
2. Browse the installation folder %SITUnifiedSystemData%\VApps\UADM\AutomationConfiguration\ and
navigate in the folder related to the use case that you want to use and select the .JSON file related to the signal
rule for that specific use case.
3. Click Save.
4. Click Approve. Consistency checks are automatically performed on signal rule before its status is changed to
Approved.
5. Click Deploy icon. The signal rule will now be flagged as deployed, and its runtime status will be Running.

The signal rule is the entry point for the handshake handling on Opcenter Execution Discrete, see How to
Create a Custom Contract for Shop Floor Integration chapter in Opcenter Execution Discrete Extensibility
Guide.
In case of PLC to MES handshake, to avoid risk of losing messages, the PLC may implement a retry logic if it
does not receive the acknowledge within a timeout. This means that a new notification with same
sequenceNo value is raised again.
If the contract command is not changed then contract Signal Rule must be configured by setting the
EnableRetry parameter to true. This prevents the risk of processing same message twice. The
EnableRetry can be set to false if no retry mechanism from PLC is in place, or, also, if the contract
command is unchanged. This is the case, for example, of the RequestOrderInfo command.

Configuring Heartbeat Mechanism
Heartbeat mechanism checks the status of Automation Channel to leveraging a tag which is periodically set by the
MES and reset by the automation logic.
Prerequisite for ATN Type Configuration
• Automation Gateway Administrator must be configured with ATN Type OPCHeartbeat.
• At least one ATN instance per ATN Channel must be activated.
Perform following steps for Signal Configuration:
1. On Signal Rule Management, import OPCHeartbeat signal rule.
2. Open OPCHeartbeat signal rule and set following parameters.
Parameters

Description

Start Time

Start time for the signal rule execution.

Start Date

Start date for the signal rule execution

End Time

End time for signal rule execution.

Time Zone

Time zone for specified start time.

Schedule Mode

Mode can be minute, hourly, daily or weekly.

Recurs Every

Based on schedule mode, specify value for this parameter. For example, recurs every 1
minute or 1 day.

3. Click Save and then Approve the signal.
Time period (Schedule Mode and Recurs Every) set for signal rule should be same in PLC and MES.
Signal rule will periodically execute a backend command which checks, for each configured automation node
instance, if the related heartbeat tag has been correctly reset in the period, if not, then it will raise
OPCDisconnected event to notify that the channel related to automation node instance is disconnected.

Event OPCDisconnected is available for custom implementation, if needed.

### How to integrate Opcenter Execution Discrete with Teamcenter Easy Plan

Opcenter Execution Discrete includes the Opcenter Execution Discrete Manufacturing Planner Preview Low Code UI
App dedicated to manufacturing planner users working in Teamcenter Easy Plan.
Once configured and deployed, this app provides a preview of how Teamcenter Easy Plan manufacturing data (in
details, Work Order Operations and Steps, with related Materials, Tools ad Work Instructions) will be available
to Opcenter Execution Discrete operators through the Opcenter Execution Discrete Complex Manufacturing App.
For detailed information on the Opcenter Execution Discrete Complex Manufacturing App User Interface, see the
How to Execute Work Orders in the Operator Terminal for Complex Manufacturing chapter in the Opcenter Execution
Discrete User Manual.

Procedure
1. In Teamcenter set the EP_OpenInOpcenterUrl preference to:
• If FN is configured in HTTP: http://<MachineName>/sit-ui/<PlantName>/
<SolutionName>.<DeployedMxAppname>/rest/preview/v1/loadpreview
• If FN is configured in HTTPS: https://<MachineName>:443/sit-ui/<PlantName>/
<SolutionName>.<DeployedMxAppname>/rest/preview/v1/loadpreview
where:
• <MachineName> corresponds to the name of the Environment where the Opcenter Execution
Discrete Manufacturing Planner Preview is deployed.
• <PlantName> corresponds to the name of the Plant where the Opcenter Execution Discrete
Manufacturing Planner Preview is deployed.
• <SolutionName> corresponds to the name of the Solution where the Opcenter Execution
Discrete Manufacturing Planner Preview is deployed.
• <DeployedMxAppname> corresponds to the name given to the Opcenter Execution Discrete
Manufacturing Planner Preview.
• Example: http://WIN11/sit-ui/DefaultPlant/U4DM.ManufPlannerPrev/rest/preview/v1/loadpreview
2. To open the Opcenter Execution Discrete Manufacturing Planner Preview App from Teamcenter Easy Plan, do
either of the following:
• From the Process Planning environment, select a Process and then click the
button.

View in Opcenter

• From the Work Instructions Authoring environment, select a Process and then select the
in Opcenter command.

> View

### How to Integrate Opcenter Execution Discrete with Opcenter Intraplant Logistics (Opcenter IPL)

Opcenter Execution Discrete comes provided with a dedicated dxp file for integration between Opcenter EX DS and
Opcenter IPL that, once imported into Data Integration System (DIS) and after being appropriately configured,
enables integration between the two products.
After importing the released integration scenario configuration and its appropriate configuration, you will be able
to:

• Allow Opcenter Intraplant Logistics to request the default or most recently updated Equipment Hierarchy so
that both systems are aligned in terms of plant structure.
• Send Kanban calls to Opcenter IPL for the replenishment of Materials on the production line.
• Send Kanban-call cancellation to Opcenter IPL so that they can be deleted in Opcenter IPL.
• Send Kanban-call delivery information when the Materials reach the production line so that Opcenter IPL learns
the quantity of Materials that reached the destination.
High Availability and IPL
In the following procedure and wherever High Availability is mentioned in relation to IPL, it must be
specified that High Availability is intended for Opcenter Execution Foundation contexts, whereas Opcenter
IPL currently does not support HA.

Prerequisites
• Opcenter Execution Foundation is installed and configured.
• Opcenter Execution Discrete is installed and configured.
• Data Integration System is installed and its Services have been created.
• (Only for High Availability scenario) The Microsoft ARR Load Balancer has been configured as described at
Configuring Microsoft ARR Load Balancer for WebService connectors in the DIS Data Integration System
Installation Guide.

Configuration Steps
The following configuration steps represent one of the possibilities provided by Data Integration System to create a
Project without creating all the required connectors manually.
To import and configure the scenario:
1. In Opcenter Execution Foundation Solution Studio, install and deploy:
• Extension App IPLIntegration of App AppU4DM
• App AppDIS.
2. In Data Integration System Management Console, import the IPL Integration Scenario Configuration (.dxp file).
3. Finalize the Project configuration.
4. Configure IIS to route calls from Opcenter IPL to DIS.
5. (Only for High Availability scenario) Configure IIS on the Reverse Proxy machine.
6. Configure Output Messages to reach DIS.

#### Importing the IPL Integration Scenario Configuration

Operating in DIS Management Console, you can import a DIS Project that consists of all the connectors that are
needed in the integration with Opcenter Intraplant Logistics.
This configuration is conceived for a scenario in which there is no other DIS Project existing in the system.

Procedure
For information about importing a DIS Project from DXP file, creating a DIS Database and generating a
Master Key, see the DIS Data Integration System User Manual.
To import the preconfigured Scenario:
1. In DIS Management Console, select Import from DXP File functionality.

2. Browse as Project export file EXDS_IPLIntegration_V2401.0001.dxp found under %SITUnifiedVAppsRoot%
\UADM\DIS\IPL.
3. When prompted, in the Insert Old Master Key dialog box, insert ChangeMe1! and click OK: the
EXDS_IPL_Integration DIS Project is created.
4. Create the DIS Database with the correct Database Data Source and Init Catalog.
5. Save the DIS Project.
6. Generate a New Master Key for the DIS Project.
Generating a new Master Key is not only necessary for security reasons, but is also required if you
export your DIS Project.
7. Save the DIS Project again.
8. Operating in Windows Services, restart service Opcenter Execution Foundation Aux Svc Core.

#### Finalizing the Project Configuration

Once the DIS Project has been imported, you must finalize the Project configuration.
High Availability Scenario
• In the following procedure and wherever High Availability is mentioned in relation to IPL, it must be
specified that High Availability is intended for Opcenter Execution Foundation contexts, whereas
Opcenter IPL currently does not support HA.
• In a High Availability scenario, after you have finalized your project configuration, remember to copy it
to all of the machines present in your scenario. For information, see step 6 of Main Workflow for
preparing your DIS Project provided at How to Prepare Your DIS Project in the DIS Data Integration
System User Manual.

Prerequisite
The following dlls available under folder %SITUnifiedVAppsRoot%\UADM\DIS\IPL must be copied to %DISPath%
\BIN:
• Siemens.OpcenterEX.DIS.IPLSDKResourcesHierarchy.dll
• Siemens.OpcenterEX.DIS.IPLSDKMaterialRequest.dll
In a High Availability scenario, this must be done on all of the Opcenter Execution Foundation hosts.

Procedure
1. Operating in DIS Management Console, under node SDK Connectors, double-click connector
SDKIPLResourceHierarchy.
2. In the External Processor tab, verify that:
- attribute Path is set to Siemens.OpcenterEX.DIS.IPLSDKResourcesHierarchy.dll in folder %DISPath%\BIN.
- attribute Class Name is set to Siemens.OpcenterEX.DIS.IPLSDKResourcesHierarchy.ResourcesHierarchy.
If necessary, modify these values accordingly.
3. Under node SDK Connectors, double-click connector SDKIPLMaterialRequest.
4. In the External Processor tab, verify that:
- attribute Path is set to Siemens.OpcenterEX.DIS.IPLSDKMaterialRequest.dll in folder %DISPath%\BIN.
- attribute Class Name is set to Siemens.OpcenterEX.DIS.IPLSDKMaterialRequest.MaterialRequest.
If necessary, modify these values accordingly.
5. Under node HTTP Client Connectors, double-click connector HTTPIPLResourcesHierarchy.

6. In the Configuration tab, inside area HTTP Configuration, modify attribute URL so that protocol (http/
https), hostname and plant (Multiplant concept) point to Opcenter Execution Discrete.
In a High Availability scenario, hostname must be set to localhost.

7. In the Access tab, inside area HTTP Basic Authentication, enter a valid User Name and Password to
authenticate to Opcenter Execution Discrete.
In a High Availability scenario, remember to use a Domain user who can access Opcenter Execution
Discrete.

8. Under node HTTP Client Connectors, double-click connector HTTPIPLMaterialRequestCreation.
9. In the Configuration tab, inside area HTTP Configuration, modify attribute URL so that hostname points to
the Opcenter IPL machine, as well as to the correct port.
10. Under node HTTP Client Connectors, double-click connector HTTPIPLMaterialRequestAcknowledge.
11. In the Configuration tab, inside area HTTP Configuration, modify attribute URL so that hostname points to
the Opcenter IPL machine, as well as to the correct port.
12. Under node HTTP Client Connectors, double-click connector HTTPIPLMaterialRequestCancellation.
13. In the Configuration tab, inside area HTTP Configuration, modify the URL attribute so that hostname points to
the Opcenter IPL machine, as well as to the correct port.
14. Go to Control Panel > Internet Options > Security tab >Trusted Sites > Sites button and add the modified
URL among your trusted sites.
15. Save the DIS Project.
16. Synchronize the DIS Project.

Next Step
You must proceed to Configuring IIS to Route Calls from Opcenter IPL to DIS.

#### Configuring IIS to Route Calls from Opcenter IPL to DIS

Internet Information Service (IIS) must be configured appropriately so that calls from Opcenter Intraplant Logistics
can be routed to Data Integration System. It must be possible for Opcenter IPL to address the
WSIPLResourcesHierarchy connector specifically.
High Availability scenarios and IPL
In the following procedure and wherever High Availability is mentioned in relation to IPL, it must be
specified that High Availability is intended for Opcenter Execution Foundation contexts, whereas Opcenter
IPL currently does not support HA.

Procedure
When working in a High Availability scenario, remember to perform the following procedure on each of the
Foundation Host machines.
1. In Internet Information Services (IIS) Manager, go to Default Web Site.
2. In area IIS, search for URL Rewrite and then select Add Rule(s)...: this opens a dedicated form.
3. Do as follows:

For...

Set...

field Name

IPL Resources Hierarchy

field Pattern

(.*)api/ipl/resources-hierarchy

field Rewrite
URL

http://127.0.0.1/diswebservice/WSConnector.asmx/FunctionCallJson?
ConnectorName=WSIPLResourcesHierarchy&DISServerHost=<Machine_Name>&TargetCo
nnector=&Message=&MessageType=ResourcesHierarchyToIPL&MessageSchema=Hierarchy
&RequestXSL=&ResponseXSL=&Timeout=10000
where <Machine_Name> must be substituted with the DIS Host Name.
In a High Availability scenario, the DIS Host Name must necessarily be the name of
the machine on which you are operating.

flag Stop
Processing
Subsequent
Rules

Set this flag.

4. Click Apply to confirm the settings.
5. Click Back to Rules.
6. Select the Rule you have just created: in area Inbound Rules, using the Move Up button, move the selected Rule
to the beginning of the Rule set.

#### Configuring IIS on the Reverse Proxy Machine

In a High Availability scenario, the Reverse Proxy machine functions as a router, directing the IPL calls to the
DISWEBSERVICE Web Farm in which there is an active node and the others are in stand-by.
High Availability and Resources Hierarchy Use Case
In the following procedure and wherever High Availability is mentioned in relation to IPL, it must be
specified that High Availability is intended for Opcenter Execution Foundation contexts, whereas Opcenter
IPL currently does not support HA.
For the Resources Hierarchy use case, it is necessary that the IPL Mes Gateway be configured so that it
points to the Reverse Proxy machine.
If the DIS node that is active changes, in Solution Studio (Host Monitoring), you must always verify which
node is currently active: then you must manually set the hosts of the DISWEBSERVICE Web Farm to the
new status of these servers, so that they coincide.

Procedure
1. On the Reverse Proxy machine where Microsoft ARR Load Balancer is running, access IIS (Internet Information
Services).
2. Select the machine name and double-click the URL Rewrite module.
3. In the Actions pane, click on Add Rule(s) and select Blank rule.

4. In the Edit Inbound Rule pane, enter the following settings:
Parameter

Value

Name

IPL Resources Hierarchy

Requested Url

Matches the Pattern

Using

Regular Expressions

Pattern

(.*)api/ipl/resources-hierarchy

Ignore Case

Yes

Action Type

Route to Server Farm

Scheme

Either of the following:
• http://
• https://

Server farm

DISWEBSERVICE

Path

/{R:0}

Stop processing of subsequent rules

Yes

5. Click Apply.
6. Click Back to Rules.
7. Select the Rule you have just created: in area Inbound Rules, using the Move Up button, move the selected Rule
to the beginning of the Rule set.

#### Configuring Output Messages to Reach DIS

As integration with Opcenter IPL concerns the satisfaction of Kanban calls by Opcenter IPL, the Output Message
functionality must be configured appropriately so that the Kanban calls can reach Data Integration System and
subsequently forwarded to Opcenter IPL. To this end, you must create:
• an Output Message Destination to address the DIS connector dedicated to this functionality
• an Output Message Definition for Kanban messages that reaches the aforementioned Output Message
Destination.

Procedure
1. Operating in Opcenter Execution Discrete, create an Output Message Destination, setting its attributes as
follows:

For attribute...

Do this...

Channel

Select Data Integration System.

DIS Message Type

Enter EXDSMaterialRequestToIPL.

DIS Message Schema

Enter MaterialRequest.

Json Format

Flag the checkbox.

2. Create an Output Message Definition for Kanban Message Type with the Output Message Destination created at
step 1 as its Output Message Destination.

Result
You have completed the steps for integrating Opcenter Execution Discrete with Opcenter Intraplant Logistics
(Opcenter IPL).

## Migrating from Previous Product Versions

It is possible to perform migration from all product versions starting from Opcenter Execution Discrete 3.3. The
workflows available for migrating Opcenter Execution Discrete from these versions of Opcenter EX DS are illustrated
in the Opcenter EX DS Migration Guide.
If you are using Low Code UI Applications in your system, see also section How to Migrate your Customized
Low Code UI App of the Opcenter EX DS Low Code UI Personalization Guide.

## Uninstalling Opcenter Execution Discrete

This procedure does not uninstall Opcenter Execution Foundation. If you need to perform a complete
uninstallation, see the Opcenter Execution Foundation Installation Guide.

Procedure
1. From Windows Control Panel > Programs > Program and Features > Uninstall or change a program
environment, select Opcenter Execution Foundation and run the wizard.
2. In the Please select the program features you want to uninstall step of the wizard, select the Opcenter
Execution Discrete check box and clear the Opcenter Execution Foundation check box, if selected.
3. Complete the wizard.

## Troubleshooting

• Configuration Issues
• Operator Landing Page Searching Issues (legacy)
• Manual Solution Configuration
• Manual Configuration for Integration with Opcenter CN MOM
• Manual Configuration for Integration with Opcenter IPL

### Troubleshooting - Configuration Issues

For any issues that might arise during the automatic configuration performed by the Opcenter EX DS Post-setup
configuration tool, follow these steps:
1. From Windows Apps > Opcenter Execution Foundation > Solution Studio environment, verify that
the Opcenter EX DS manufacturing solution has been created in the home page.
2. If the solution has been created, delete it.
3. Launch the Post-Setup Configuration tool again to attempt to create and configure the solution automatically.
4. If problems persist, create and configure the solution manually.

### Troubleshooting - Operator Landing page searching issues

For any issues that might arise during the automatic configuration performed by the Opcenter EX DS Post-setup
configuration tool, follow these steps:
1. From Windows Apps > Opcenter Execution Foundation > Solution Studio environment, verify that
the Opcenter EX DS manufacturing solution has been created in the home page.
2. If the solution has been created, delete it.
3. Launch the Post-Setup Configuration tool again to attempt to create and configure the solution automatically.
4. If problems persist, create and configure the solution manually.

### Troubleshooting - Manual Solution Configuration

The configuring of the application is usually performed automatically launching the Opcenter Execution Discrete
configuration tool, which creates the manufacturing solution of interest and performs many configurations
automatically.
Alternatively, you can choose to manually perform the following operations:
1. Create the Solution.
2. Configure the Solution.

#### Creating the Opcenter Execution Discrete Manufacturing Solution

The first step for configuring Opcenter Execution Discrete requires that you create a dedicated solution.

Procedure
1. Launch Opcenter Execution Foundation Solution Studio.
2. Log on to the application.
3. From the Opcenter EX FN Solution Studio home page click Create Solution.
4. In the Create Solution page, select From scratch.
5. Insert the name and the description of the Solution.
6. Click Create. The new solution is displayed in the  Solution Administration page.

7. Click the
icon on in the left-hand menu. The home page is displayed, showing the link to the created
Opcenter Execution Discrete Solution in the Quick Links area.

#### How to Configure the Opcenter Execution Discrete Solution Manually

After creating the Opcenter Execution Discrete manufacturing solution, some configurations must be executed
manually before deploying the solution and being able to access the web application.

Accessing the Solution Home Page
1. From Windows Apps, in the Opcenter Execution Foundation category, click the Solution Studio link.
2. In the web page, log in to the Opcenter EX FN Solution Studio in either of the following ways:
• Insert the credentials of the user with administrator rights and click Sign In.
• Click Use your current Windows session to Log In link to access the application with the current user
credentials.
3. In the home page, click the link to the Opcenter EX DS solution.

Workflow
1. Configure Users and Groups.
2. Configure User Roles.
3. Configure Mashups.
4. Creating Worker Roles.
5. Associate Roles to Users and Groups.
6. Associate Roles with Function Rights.
7. Configure event subscriptions.
8. (optional when integrating with Teamcenter Manufacturing) Verify the correct configuration of event
subscriptions.
9. Configure Pre-Checks and Post Actions.
10. Import the UI Application.
11. Configure the Databases and deploy the Solution.

##### Configuring User Roles

While manually configuring the Opcenter Execution Discrete manufacturing solution, you must create the user
roles. User roles (also called user rights) represent groupings of permissions to be assigned to user groups in order
to set constraints on the runtime operations they are allowed to perform within the manufacturing solution.

Retrieving the list of User Roles
The roles to be added can be manually retrieved from the following files:
• %SITUnifiedSystemRoot%Vapps\UADM\UADM_CommandList.xml, for the U4DM solution.
• %SITUnifiedSystemRoot%Vapps\EXAM\AM_CommandList.xml, for theDS4AM solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSBasic_CommandList.xml, for the DS solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSAdvanced_CommandList.xml, for theOnePieceFlow solution.
1. In the XML file, locate the <CommandList Category="CreateRoles"> section.
2. For each <Name>CreateRoleCommand</Name> item contained in this section, locate the <Body> item.
3. For each <Body> item, identify and take note of the the following parameters:
• -rn : Role Name
• -d : Role Description

Creating the User Roles
1. In the Solution Studio Home page, click

Account > Roles section of the sidebar.

2. In the Roles page, click
Add New role.
3. In the Add Role page, insert the name and description of the role and click Save.
4. Repeat steps 2-3 for each role retrieved in the previous paragraph.

##### Configuring Mashups

After creating the UI application, you must import the JSON files that describe the configuration of Mashups.

Procedure
1. Select User Interface > Mashups.
2. Click
Import UI Module.
3. In the Import UI Module panel, click Browse in the UI Module Manifest field.
4. Select one of the following:
• U4DM.operatorLanding.json file in the %SITUnifiedSystemRoot%VApps\UADM folder, for the U4DM
solution.
• DS4AM.operatorLanding.json file in the %SITUnifiedSystemRoot%VApps\EXAM folder, for the DS4AM
solution.
• DSBasic.operatorLanding.json file in the %SITUnifiedSystemRoot%VApps\UADM folder, for the DS
solution.DSBasi
• DSAdvanced.operatorLanding.json in the %SITUnifiedSystemRoot%VApps\UADM folder, for
the OnePieceFlow solution.
5. Click Save.
6. Repeat steps 2-5, selecting one of the following:
• U4DM.highAutomationOpLanding.json file in the %SITUnifiedSystemRoot%VApps\UADM folder, for
the U4DM solution.
• DS4AM.highAutomationOpLanding.json file in the %SITUnifiedSystemRoot%VApps\EXAM folder, for
the DS4AM solution.
• DSBasic.highAutomationOpLanding.json file in the %SITUnifiedSystemRoot%VApps\UADM folder,
for the DSsolution.
• DSAdvanced.highAutomationOpLanding.json file in the %SITUnifiedSystemRoot%VApps\UADM
folder, for the OnePieceFlowsolution.

##### Creating Worker Roles

Worker roles are entities that will be in charge of receiving event subscriptions and on which you want to distribute
the business logic that makes up the project. The association between subscriptions and worker roles is not unique:
different worker roles can receive the same event and execute the same logic.
Each worker role must contain the list of the commands it will receive. You can associate with a worker role
only commands defined as protected (public or not public). After this association, the command is
called published in role command. A command cannot be associated with two worker roles at the same time, it
must be first disassociated and then re-associated.
For more details, see Creating a New Worker Role in the Opcenter Execution Foundation Development and
Configuration Guide.

Retrieving the list of Worker Roles
The Worker Roles to be added can be manually retrieved from the following files:

• %SITUnifiedSystemRoot%Vapps\UADM\UADM_CommandList.xml, for the U4DM solution.
• %SITUnifiedSystemRoot%Vapps\EXAM\AM_CommandList.xml, for the DS4AM solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSBasic_CommandList.xml, for the DS solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSAdvanced_CommandList.xml, for the OnePieceFlow solution.
1. In the XML file, locate the <CommandList Category="ConfigureDefaultWorkerRole"> section.
2. For each <Command><Name>CreateRoleCommand</Name></Command> item contained in this section,
locate the <Body> item.
3. For each <Body> item, identify and take note of the the following parameters:
• "Name"
• "Description"
• "Execution Mode"
• "TargetCPU"
• "TargetRuntime"
• "RetriesNumber"
• "ExecutionMode"
• "CommandExecutionTimeout"

Creating the Worker Roles
1. In the home page of Solution Studio page, select the App of interest.
2. Select Settings > Worker Roles.
3. Click
Create New Worker Role.
4. In the Create New Worker Role panel, insert the Worker Role parameters and click Save.
5. Repeat steps 1-4 for each App and each Worker Role retrieved in the previous paragraph.

##### Associating Roles with Function Rights

After creating a user role, you must associate the role with the function rights of interest. In particular, you can:
• Associate the role with operation types:
• By invoking any runtime command.
• By firing any runtime event.
• By subscribing to any runtime event and/or signal.
• Associate the role with specific operations:
• By viewing any screen.
• By executing runtime commands.
• By raising runtime events.
• By subscribing runtime events and/or signals.
The commands can be distinguished by their prefix. In general, prefix-bearing commands expose only those
elements that are congruent with their context of use, thereby simplifying their configuration and use.
Command type

Prefix

Description

Global commands

No prefix

Commands that contain all characteristics inherent to
the general execution of the command, regardless of
its context of use.

PLM commands

PLM

Commands required for the integration with PLM
systems in order to import master data like Bills of
Processes and related entities.

Command type

Prefix

Description

UADM commands

UADM

Commands that are invoked by the default UI, but can
also be used in any case to develop custom logic.

Retrieving the lists of Function Rights
The function rights to be added can be manually retrieved from the following files:
• %SITUnifiedSystemRoot%Vapps\UADM\UADM_CommandList.xml, for the U4DM solution.
• %SITUnifiedSystemRoot%Vapps\EXAM\AM_CommandList.xml, for the DS4AM solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSBasic_CommandList.xml, for the DS solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSAdvanced_CommandList.xml, for the OnePieceFlow solution.
1. In the XML file, locate the <CommandList Category="AssociateFunctionRightsToRoles"> section.
2. For each <Command><Name>AddFunctionRightToRoleCommand</Name><Command> item contained in
this section, locate the <Body> item.
3. For each <Body> item, identify and take note of the the following parameters:
• SecurableObjectName
• SecurableCategoryName
• OperationName
• RoleName
4. Split the list grouping the items by RoleName. This creates the lists of function rights associated to each User
Role.

Associating Function Rights
For each User Role previously created, perform the following operations
1. In the Solution Studio Home page, click

Account > Roles section of the sidebar.

2. In the Roles page, select the role to which the Function Rights must be associated and click
Open.
3. According to the SecurableCategoryName parameters retrieved in the previous paragraph, select the
corresponding tab, relative to the category to which the function right must be associated (either Commands,
Events, Signals, UI Screens or Reading Functions).
4. Click Assign Rights.
5. In the Assign Rights panel, select the function right to be assigned according to the list previously created:
• SecurableObjectName corresponds to the Screen Name column
• OperationName corresponds to the Action Name column
6. Click Assign.
7. Repeat steps 4-6 for each function right to be associated.

##### Configuring Event Subscriptions

After associating roles with function rights, you must associate each event to be monitored with one or more event
handlers. This operation allows the system to execute a specific logic when the event is raised.
Any existing event subscriptions can be removed if you want to inhibit certain types of runtime behavior.

Retrieving the lists of Event Subscriptions
The event subscriptions to be added can be manually retrieved from the following files:
• %SITUnifiedSystemRoot%Vapps\UADM\UADM_CommandList.xml, for the U4DM solution.
• %SITUnifiedSystemRoot%Vapps\EXAM\AM_CommandList.xml, for the DS4AM solution.

• %SITUnifiedSystemRoot%Vapps\UADM\DSBasic_CommandList.xml, for the DS solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSAdvanced_CommandList.xml, for the OnePieceFlowsolution.
1. In the XML file, locate the <CommandList Category="CreateEventSubscriptions"> section.
2. For each <Command><Name>CreateEventSubscriptionCommand</Name><Command> item contained in
this section, locate the <Body> item.
3. For each <Body> item, identify and take note of the the following parameters:
• Name
• Description
• EventHandlerName
• SubscribedEventName
4. In the XML file, locate the <CommandList Category="ConfigureDefaultWorkerRole"> section.
5. For each <Command><Name>AddSubscriptionToWorkerRoleCommand</Name><Command> item
contained in this section, locate the <Body> item.
6. For each <Body> item, identify and take note of the the following parameters:
• SubscriptionName
• WorkerRoleName
7. Match the SubscriptionName parameter with the Name parameter retrieved in step 3 so to obtain an unique
list.

Configuring the Event Subscriptions
Perform the following operations for each installed App according to the information retrieved in the previous
paragraph:
1. In the App Management page, select the App tile and click
Open App.
2. In the App Configuration page, click on the Event Subscriptions tab: the predefined event subscriptions that
are already associated with the current worker role are displayed, but cannot be modified.
3. Click Add Event Subscription Here (or click
if an item is already present in the page).
4. In the Properties tab, insert the required parameters according to the list retrieved in the previous paragraph:
• SubscribedEventName corresponds to the Event field
• EventHandlerName corresponds to the Event Handler field.
5. In the Worker Role tab, select Select Existing and select the required worker role according to the list retrieved
in the previous paragraph.
6. Click Save.

Removing Event Subscriptions
1. In the App Management page, select the App tile and click
Open App.
2. In the App Configuration page, click on the Event Subscriptions tab: according to your needs, select the event
handlers that you want to remove and click
: a message requesting confirmation of the deletion is
displayed.
3. Click OK: the selected event handlers are removed.

##### Verifying Event Subscriptions in Integration scenarios

In case of integration with Teamcenter Manufacturing, it is possible to configure the system to trigger some
activities automatically. More specifically, this can be obtained by configuring Event Subscriptions, which makes
the system execute a specific logic when the event is raised.
The following use cases are foreseen:
• automatic merge and release of Work Orders in Opcenter Execution Discrete
• automatic creation of Issue Reports.

• automatic creation of Event Notifications.
In the first use case, you may create the Work Order Header within Opcenter EX DS and request Teamcenter
Manufacturing to download a suitable As Planned BoP. Once the As Planned BoP is available in the system, the
Work Order Header can be automatically merged with the downloaded As Planned BoP. Furthermore, the resulting
Work Order can be then automatically released for production. You can take advantage from this use case in all
scenarios that do not involve SAP.
In the second use case, Event Subscriptions can be configured to automatically create issue reports. These issue
reports are created on the basis of Non-Conformances declared in Opcenter Execution Discrete and are then sent to
Teamcenter Manufacturing.
This configuration is valid in all scenarios involving Opcenter EX DS and Teamcenter Manufacturing, regardless of
whether they are integrated or not with SAP.
The following Event Subscriptions are configured automatically during the installation, and are included in
the list created in the Configuring Event Subscriptions section. Therefore, the following instructions are
meant solely to verify the correct configuration in case of integration with Teamcenter Manufacturing.
They can be manually removed if not needed (for example because integration is not enabled).

Available Operations
• Configuring Event Subscriptions to automatically merge and release Work Orders
• Configuring Event Subscriptions to automatically create Issue Reports.
• Configuring Event Subscriptions to enable Event Notifications for Work Order and Work Order Operations
Confirmations

Configuring Event Subscriptions to automatically merge and release Work Orders
1. In the App Management page, click the AppU4DM App tile and click
.
2. In the App Configuration page, click on the Event Subscriptions tab: the predefined event subscriptions that
are already associated with the current worker role are displayed, but cannot be modified.
3. Click
.
4. In the New Subscription panel, add the following Event Subscriptions:
Event

Event Handler

OnCompleteAsPlannedBOP

OnCompleteAsPlannedBOPDefaultResolEventHandlerShell

OnCreateWorkOrderHeader

One of the following Event Handlers, depending on the scenario
(ERP/TC/OpcenterEXDS or TC/OpcenterEXDS). For more
information on the scenarios, see section Integration with
Teamcenter of the Opcenter Execution Discrete Product
Overview.
• OnCreateworkOrderHeaderERPResolutEventHandl
erShell for the ERP/TC/OpcenterEXDS scenario
• OnCreateworkOrderHeaderUADMResolutEventHan
dlerShell for the TC/OpcenterEXDS scenario

5. Assign the UADM Worker Role runtime Data Worker Role to each Event Subscription.
6. Click Save.

Configuring Event Subscriptions to automatically create Issue Reports
1. In the App Management page, click the AppU4DM App tile and click
.
2. In the App Configuration page, click on the Event Subscriptions tab: the predefined event subscriptions that
are already associated with the current worker role are displayed, but cannot be modified.
3. Click
.
4. In the New Subscription panel, add the following Event Subscriptions:
Event

Event Handler

OnCreateNonConformanceV3_1

OnCreateNonConformanceV3_1AIGIntegrationEventH
andler

OnSentenceNonConformanceV3_1

OnSentenceNonConformanceV3_1AIGIntegrationEven
tHandler

OnCreateIssueReportResult

OnCreateIssueReportResultEventHandler

5. Assign the UADM Worker Role runtime Data Worker Role to each Event Subscription.
6. Click Save.

Configuring Event Subscriptions to enable Event Notifications for Work Order and
Work Order Operations Confirmations
1. In the App Management page, click the AppU4DM App tile and click
.
2. In the App Configuration page, click on the Event Subscriptions tab: the predefined event subscriptions that
are already associated with the current worker role are displayed, but cannot be modified.
3. Click
.
4. In the New Subscription panel, add the following Event Subscriptions:
Event

Event Handler

OnCompleteWorkOrderSN

OnCompleteWorkOrderSNEventHandlerShell

OnCompleteWorkOrderOperationSN

OnCompleteWorkOrderOperationSNEventHandlerS
hell

OnCompleteWorkOrderOperationERP

OnCompleteWorkOrderOperationERPEventHandler
Shell

OnCompleteWorkOrder

OnCompleteWorkOrderEventHandlerShell

5. Assign the UADM Worker Role runtime Data Worker Role to each Event Subscription.
6. Click Save.

##### Configuring Pre-Checks and Post Actions

After creating the UI application, you must configure the Pre-Checks and the Post Actions associated to its
commands. Specifically, this means:
• enabling or disabling Pre-Checks;
• establish Pre-Checks and Post Actions execution order.

Retrieving the list of Pre-Checks
The Pre-Checks to be configured can be manually retrieved from the following files:
• %SITUnifiedSystemRoot%Vapps\UADM\UADM_CommandList.xml, for the U4DM solution.
• %SITUnifiedSystemRoot%Vapps\EXAM\AM_CommandList.xml, for the DS4AM solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSBasic_CommandList.xml, for the DS solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSAdvanced_CommandList.xml, for the OnePieceFlow solution.
1. In the XML file, locate the <CommandList Category="ConfigurePreChecksAndPostActions"> section.
2. For each <Command><Name>UpdatePreCheckConfigurationCommand</Name><Command> item
contained in this section, locate the <Body> item.
3. For each <Body>{"command"{"PreCheckConfigurationList"} item, identify and take note of the the following
parameters:
• Name
• CommandName
• Order
• Enabled

Retrieving the list of Post Actions
The Post Actions to be configured can be manually retrieved from the following files:
• %SITUnifiedSystemRoot%Vapps\UADM\UADM_CommandList.xml, for the U4DM solution.
• %SITUnifiedSystemRoot%Vapps\EXAM\AM_CommandList.xml, for the DS4AM solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSBasic_CommandList.xml, for the DS solution.
• %SITUnifiedSystemRoot%Vapps\UADM\DSAdvanced_CommandList.xml, for the OnePieceFlow solution.
1. In the XML file, locate the <CommandList Category="ConfigurePreChecksAndPostActions"> section.
2. For each <Command><Name>UpdateCommandActionConfigurationCommand</Name><Command> item
contained in this section, locate the <Body> item.
3. For each <Body>{"command"{"CommandActionConfigurationList"} item, identify and take note of the the
following parameters:
• Name
• Order.

Applying the Configuration
Perform the following operations for each installed App according to the information retrieved in the previous
paragraphs:
1. In the App Management page, select the App tile and click
Open App.
2. In the App Configuration page, click on the Commands tab: the commands that have associated Pre-Checks
and/or Post Actions are displayed with a right-pointing arrow in the first column.
3. According to the CommandName parameter of the previously retrieved Pre-Checks list, select a command with
associated Pre-Checks and/or Post Actions and click on its arrow to expand the list.
4. Click Configure.
5. In the Pre and Post Execution Configuration panel, select the Pre-Checks tab.

6. For each Pre-Check (identified according to the Name parameter of the previously retrieved Pre-Checks list),
enable or disable it according to the Enabled parameter of said list.
7. If necessary, re-order the list dragging and dropping each row in the correct position according to the
Order parameter of the previously retrieved Pre-Checks list.
8. In the Pre and Post Execution Configuration panel, select the Post-Actions tab.
9. If necessary, re-order the Post Actions (identified according to the Name parameter of the previously retrieved
Post Actions list) dragging and dropping each row in the correct position according to the Order parameter.
10. Click Save.
11. Repeat the steps from 3 to 10 for each command in the previously retrieved lists.

##### Importing the UI Application

After creating the UI application, you must import the JSON file that describes the configuration of the UI
Application.

Procedure
1. Select User Interface > UI Applications.
2. Click
Import UI Application.
3. In the Import UI Application panel, click Browse in the Ui Application Manifest field.
4. Select one of the following:
• Siemens_SIT_UADM.json file in the %SITUnifiedSystemRoot%VApps\UADM folder, to import the UI
Application included in the U4DM solution.
• Siemens_OPC_EXDS_AM.json file in the %SITUnifiedSystemRoot%VApps\EXAM folder, to import the
UI Application included in the DS4AM solution.
• Siemens_OPC_EXDS_Basic.json file in the %SITUnifiedSystemRoot%VApps\UADM folder, to import
the UI Application included in the DSsolution.
• Siemens_OPC_EXDSAdvanced.json file in the %SITUnifiedSystemRoot%VApps\UADM folder, to
import the UI Application included in the OnePieceFlow solution.
5. Click Save.

### Troubleshooting - Manual Configuration for Integration with Opcenter CN MOM

Opcenter Execution Discrete releases an integration scenario configuration that after being imported into Opcenter
Connect MOM enables the integration between the two products.
This troubleshooting section provides information on how to manually recreate the imported configurations in
order to check it in case of problems.
For details on how to create the XML messages and related XSD:
• for messages from the Shop Floor, refer to the How to Exchange Messages with the Shop Floor section.
• for automatic data import, refer to the How to Automatically Import and Delete Data section.

Workflow
1. Create the MOM Connection.
2. Import the Workflow.
3. For messages from the Shop Floor, configure the Use Case of interest.
4. For messages for data import:
• Import the Message Map.
• Configure the Message Type of interest.

• Configure the Channel.
5. Define the File Adapter.
6. Reset IIS and restart the Opcenter Connect MOM Channel Adapter Host Service, to activate the Use Case
configuration.
7. (Optional) In case of problems, tune Opcenter Connect MOM Parameters to improve performances.

#### Creating the MOM Connection

A properly-configured MOM Connection is essential to establishing communication between Opcenter EX DS and
the Opcenter Connect MOM Web Application: this communication is based on the exchange of messages.
For the Shop Floor and Input messages, the Multiplant can be addressed with dedicated Adapters for each plant
along with its dedicated MOM Connection for each respective plant.
In the plant specific MOM Connections, the address should include the plant information, for example, http://
myexdsserver/sit-svc/Plant1.
On the other hand, for the Import messages the plant is inside the XML Message itself, so a MOM Connection without
the plant information can be used.

Procedure
1. Access the Opcenter Connect MOM login page.
2. Log in to the Opcenter Connect MOM Web Application.
3. In the Opcenter Connect MOM Configuration tile, click the MOM Connections tab.
4. Click the Add Object

icon to create a new MOM Connection with the following properties:

Property

Value

Name

Type the name that identifies the new MOM connection (for example,
UADM).

Address

Type the address of the machine on which Opcenter EX DS is installed.
The address must begin with either http or https
(for example: http://myEXDSServer/sit-svc).
In case of Multiplant, the address can be, for example, http://
myEXDSServer/sit-svc/MyPlant. Here, MyPlant is the plant addressed
by the MOM Connection in the multiplant use case.

User Name

Type the name of a Opcenter EX DS user associated to the
ShopFloorDevice user role.

Password

Type the password associated to the Opcenter EX DS user.

Autentication Type

Select Oauth2.

Authentication Address

Type the URL of the UMC authentication server: for example, http://
myUADMserver/sit-auth/OAuth/Token.

Property

Value

Authentication Extension Data

Type scope=global.

5. Click Add Object.

#### Importing the Workflow

You may have already imported these Workflows in your system during previous configurations. In this
case, you can skip this step.
• The sit_ua_rest_call Workflow is specific to Shop Floor operations.
• The opcenterexds_input Workflow is specific to Input Messages.
• The opcenterexds_import Workflow is specific to data import (both for XML and JSON files).

Procedure
1. Open the Opcenter Connect MOM Workflow Designer Application.
2. In the Settings tab, configure the credentials to connect to the application server and click Save Settings
A user with Administrative rights must be entered.
3. Click
> Import File.
4. Select the file of interest (installed by default in
%SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Workflow on the Opcenter Connect
MOM machine) and click Open:
• sit_ua_rest_call.miow
• opcenterexds_input.miow
• opcenterexds_import.miow
5. In the Home tab, click Save Workflow.

.

#### Messages From the Shop Floor

After importing the Workflow, you must configure the use case of interest to exchange messages with the Shop
Floor:

Available Operations
• Work Order Operation Start
• Tool Usage
• Material Consumption
• Data Collection
• Work Order Note Creation
• Work Order Operation Completion
• Quality Inspection Data Acquisition
• Quality Non-Conformance Creation on Work Order Operations
• Quality Non-Conformance Creation on Machines
• Quality Non-Conformance Creation on Material Tracking Units
• Quality Non-Conformance Sentencing
• Input Message Receiving from the Warehouse.

##### How to Automatically Start Work Order Operations

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic start of Work Order Operations by Machines or Workcenters, in case of
integration between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the WOO_START Message Map.
2. Configure the Message Type for:
• the Automatic Work Order Operation Start call
• the Automatic Work Order Operation Start response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the WOO_START Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\WOO_START.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Work Order Operation Start call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

WOO_START

Description

Start Work Order Operation Automatically by Machines or
Workcenters

Dispatch Rule

fifowithpredecessors

3. Select the WOO_START Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

WOO_START

Message Map Revision

3

Workflow

sit_ua_rest_call

.

5. Select Message Attributes and click

to add the following Items:

Message Attribute

Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticStart
• Do Not Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Work Order Operation Start
response
1. Operating in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

WOO_STARTresponse

Description

Response for Start Work Order Operation Automatically by
Machines or Workcenters

Dispatch Rule

fifowithpredecessors

2. Select the WOO_STARTresponse Message Type created in the previous step and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

Configuring the UADMAutomaticShopFloorChannel Message Channel

The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous steps and click

.

4. Select Valid Message Types and click
• WOO_START
• WOO_STARTresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. Operating in the Message Type Functions area, in the Other Functions section, click
and insert the
following function, which is used to extract the Message Type from the XML file root node:
NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Use Tools

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic usage of Tools by Machines or Workcenters, in case of integration
between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the USE_TOOL Message Map.
2. Configure the Message Type for:
• the Automatic Tool Usage call
• the Automatic Tool Usage response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the USE_TOOL Message Map
1. Open the Opcenter Connect MOM Map Designer application.

2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\USE_TOOL.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Tool Usage call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

USE_TOOL

Description

Automatic tool usage.

Dispatch Rule

fifowithpredecessors

3. Select the USE_TOOL Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

USE_TOOL

Message Map Revision

3

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attributes
1

218

.

to add the following Items:

Parameters
• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticUseToolList
• Do Not Promote: false
• Include In Event: false

Message Attributes

Parameters

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Tool Usage response
1. Working in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

USE_TOOLresponse

Description

Response for automatic Tool usage.

Dispatch Rule

fifowithpredecessors

2. Select the USE_TOOLresponse Message Type created in the previous step and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Parameter

Value

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous steps and click

.

4. Select Valid Message Types and click
• USE_TOOL
• USE_TOOLresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function,type MessageType and

click

.

6. In Message Type Functions area, in Other Functions section, click
which is used to extract the Message Type from the XML file root node:

and insert the following function,

NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Consume Materials

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic consumption of Materials by Machines or Workcenters, in case of
integration between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the Consume_MI Message Map.
2. Configure the Message Type for:
• the Automatic Material Consumption call
• the Automatic Material Consumption response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the Consume_MI Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\Consume_MI.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Material Consumption call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

CONSUME_MI

Description

Automatic Material Consumption.

Dispatch Rule

fifowithpredecessors

3. Select the CONSUME_MI Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

CONSUME_MI

Message Map Revision

3

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attribute

.

to add the following Items:
Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticConsumeMaterialTrackingUnit
• Do Note Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Note Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Note Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Material Consumption response
1. Working in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

CONSUME_MIResponse

Description

Response for Automatic Material Consumption.

Dispatch Rule

fifowithpredecessors

2. Select the CONSUME_MIResponse Message Type created in the previous step and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous steps and click

.

4. Select Valid Message Types and click
• CONSUME_MI
• CONSUME_MIresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. In Message Type Functions area, in Other Functions section, click
which is used to extract the Message Type from the XML file root node:

and insert the following function,

NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Collect Data

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic collection of data by Machines or Workcenters, in case of integration
between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the DCD_ACQUIRE Message Map.
2. Configure the Message Type for:
• the Automatic Data Collection call
• the Automatic Data Collection response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the DCD_ACQUIRE Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\DCD_ACQUIRE.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Collect Data call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

DCD_ACQUIRE

Description

Automatic acquisition of a DCD

Dispatch Rule

fifowithpredecessors

3. Select the DCD_ACQUIRE Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:

.

Parameter

Value

Message Map

DCD_ACQUIRE

Message Map Revision

4

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attribute

to add the following Items:
Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
AutomaticCollectWorkInstruction
• Do Note Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Note Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Note Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Collect Data response
1. Working in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

DCD_ACQUIREresponse

Description

Response for Automatic acquisition of a DCD

Dispatch Rule

fifowithpredecessors

2. Select the DCD_ACQUIREresponse Message Type created in the previous step and click

.

3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for UADM Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous steps and click

.

4. Select Valid Message Types and click
• DCD_ACQUIRE
• DCD_ACQUIREresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. In Message Type Functions area, in Other Functions section, click
which is used to extract the Message Type from the XML file root node:

and insert the following function,

NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Create Work Order Notes

This page describes the configurations required to exchange messages between the MES layer and the Shop Floor,
in order to trigger the automatic creation of Work Order Notes by Machines or Workcenters on all the Work Order
Operations that belong to the Work Order currently being executed, in case of integration between Opcenter
Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the WO_NOTE Message Map.
2. Configure the Message Types for:

• the Automatic Work Order Note Creation call
• the Automatic Work Order Note Creation response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the WO_NOTE Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\WO_NOTE.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Work Order Note Creation call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

WO_NOTE

Description

Automatic creation of a Work Order note

Dispatch Rule

fifowithpredecessors

3. Select the WO_NOTE Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

WO_NOTE

Message Map Revision

1

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attribute
1

226

.

to add the following Items:
Parameters
• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticCreateSnagAndNote
• Do Not Promote: false
• Include In Event: false

Message Attribute

Parameters

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Work Order Note Creation
response
1. Working in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

WO_NOTEresponse

Description

Response for Automatic creation of a Work Order note

Dispatch Rule

fifowithpredecessors

2. Select the WO NOTEresponse Message Type created in the previous step and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Channels
tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Parameter

Value

Description

Message channel for UADM Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous steps and click

.

4. Select Valid Message Types and click
• WO_NOTE
• WO_NOTEresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. In Message Type Functions area, in Other Functions section, click
which is used to extract the Message Type from the XML file root node:

and insert the following function,

NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Complete Work Order Operations

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic completion of Work Order Operations by Machines or Workcenters, in
case of integration between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the WOO_COMPLETE Message Map.
2. Configure the Message Type for:
• the Automatic Work Order Operation Complete call
• the Automatic Work Order Operation Complete response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the WOO_COMPLETE Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\WOO_COMPLETE.miom file
and click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Work Order Operation Complete
call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

WOO_COMPLETE

Description

Complete Work Order Operation Automatically by Machines or
Workcenters

Dispatch Rule

fifowithpredecessors

3. Select the WOO_COMPLETE Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

WOO_COMPLETE

Message Map Revision

5

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attribute

.

to add the following Items:
Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticComplete
• Do Not Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

Message Attribute

Parameters

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Work Order Operation Complete
response
1. Operating in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

WOO_COMPLETEresponse

Description

Response for Complete Work Order Operation Automatically by
Machines or Workcenters

Dispatch Rule

fifowithpredecessors

2. Select the WOO_COMPLETEresponse Message Type created in the previous step and click
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

230

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Parameter

Value

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous step and click

.

4. Select Valid Message Types and click
• WOO_COMPLETE
• WOO_COMPLETEresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. Operating in the Message Type Functions area, in the Other Functions section, click
and insert the
following function, which is used to extract the Message Type from the XML file root node:
NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Acquire Quality Inspection Data

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic acquisition of quality inspection data by Machines or Workcenters, in
case of integration between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the QI_ACQUIRE Message Map.
2. Configure the Message Type for:
• the Automatic Quality Inspection Data Acquisition call
• the Automatic Quality Inspection Data Acquisition response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the QI_ACQUIRE Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\QI_ACQUIRE.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Quality Inspection Data
Acquisition call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

QI_ACQUIRE

Description

Automatic acquisition of a Quality Inspection Data.

Dispatch Rule

fifowithpredecessors

3. Select the QI_ACQUIRE Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

QI_ACQUIRE

Message Map Revision

1

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attribute

.

to add the following Items:
Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticAcquireQualityInspectionData
• Do Note Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Note Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Note Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Quality Inspection Data
Acquisition response

1. Working in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

QI_ACQUIREresponse

Description

Response for Automatic acquisition of a Quality Inspection Data.

Dispatch Rule

fifowithpredecessors

2. Select the QI_ACQUIREresponse Message Type created in the previous step and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for UADM Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous steps and click

.

4. Select Valid Message Types and click
• QI_ACQUIRE
• QI_ACQUIREresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. In Message Type Functions area, in Other Functions section, click
which is used to extract the Message Type from the XML file root node:

and insert the following function,

NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Create Non-Conformances of type Quality on Work Order Operations

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic creation of a Non-Conformance of type Quality on Work Order
Operations by Machines or Workcenters, in case of integration between Opcenter Execution Discrete and Opcenter
Connect MOM.

Workflow
1. Import the OPEN_NC_ON_WOO Message Map.
2. Configure the Message Type for:
• the Automatic creation of Non-Conformances on Work Order Operation call
• the Automatic creation of Non-Conformances on Work Order Operation response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the OPEN_NC_ON_WOO Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate
the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\OPEN_NC_ON_WOO.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic creation of Non-Conformances on
Work Order Operation call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

OPEN_NC_ON_WOO

Description

Open Automatically Non-Conformances on Work Order Operation

Dispatch Rule

fifowithpredecessors

3. Select the OPEN_NC_ON_WOO Message Type created in the previous step and click

.

4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

OPEN_NC_ON_WOO

Message Map Revision

3

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message
Attribute

to add the following Items:

Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticCreateNonConformanceOnWOOperation
• Do Not Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic creation of Non-Conformances on
Work Order Operation response
1. Working in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

OPEN_NC_ON_WOOresponse

Parameter

Value

Description

Response for Open Automatically Non-Conformances on Work
Order Operation

Dispatch Rule

fifowithpredecessors

2. Select the OPEN_NC_ON_WOOresponse Message Type created in the previous step and click
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous step and click

.

4. Select Valid Message Types and click
• OPEN_NC_ON_WOO
• OPEN_NC_ON_WOOresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. Operating in the Message Type Functions area, in the Other Functions section, click
and insert the
following function, which is used to extract the Message Type from the XML file root node:
NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Create Non-Conformances of type Quality on Machines

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic creation of a Non-Conformance of type Quality on Machines by
Machines or Workcenters, in case of integration between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the OPEN_NC_ON_EQUIPMENT Message Map.
2. Configure the Message Type for:
• the Automatic creation of Non-Conformances on Machine call
• the Automatic creation of Non-Conformances on Machine response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the OPEN_NC_ON_EQUIPMENT Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate
the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\OPEN_NC_ON_EQUIPMENT.miom fil
e and click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic creation of Non-Conformances on
Machine call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

OPEN_NC_ON_EQUIPMENT

Description

Open Automatically Non-Conformances on Machines

Dispatch Rule

fifowithpredecessors

3. Select the OPEN_NC_ON_EQUIPMENT Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

OPEN_NC_ON_EQUIPMENT

Message Map Revision

.

Parameter

Value

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attribute

to add the following Items:
Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticCreateNonConformanceOnEquipme
nt
• Do Not Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic creation of Non-Conformances on
Machine response
1. Operating in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

OPEN_NC_ON_EQUIPMENTresponse

Description

Response for Open Automatically Non-Conformances
on Machines

Dispatch Rule

fifowithpredecessors

2. Select the OPEN_NC_ON_EQUIPMENTresponse Message Type created in the previous step and click
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.

.

4. Leave the other attributes as default (recommended) and click Save

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous step and click

.

4. Select Valid Message Types and click
to add the following Items:
• OPEN_NC_ON_EQUIPMENT
• OPEN_NC_ON_EQUIPMENTresponse
5. Select Message Type Functions, click
click

to edit the Msg Type Extraction Function, type MessageType and

.

6. Operating in the Message Type Functions area, in the Other Functions section, click
and insert the
following function, which is used to extract the Message Type from the XML file root node:
NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Create Non-Conformances of type Quality on Material Tracking Units

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic creation of a Non-Conformance of type Quality on Material Tracking
Units by Machines or Workcenters, in case of integration between Opcenter Execution Discrete and Opcenter
Connect MOM.

Workflow
1. Import the OPEN_NC_ON_PRODUCT Message Map.

2. Configure the Message Type for:
• the Automatic creation of Non-Conformances on Material Tracking Unit call
• the Automatic creation of Non-Conformances on Material Tracking Unit response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the OPEN_NC_ON_PRODUCT Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate
the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\OPEN_NC_ON_PRODUCT.miom file
and click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Creation of Non-Conformance on
Material Tracking Unit call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

OPEN_NC_ON_PRODUCT

Description

Open Automatically Non-Conformances on Material Tracking
Unit

Dispatch Rule

fifowithpredecessors

3. Select the OPEN_NC_ON_PRODUCT Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

OPEN_NC_ON_PRODUCT

Message Map Revision

3

Workflow

sit_ua_rest_call

5. Select Message Attributes and click

.

to add the following Items:

Message Attribute

Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticCreateNonConformanceOnMTUList
• Do Not Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Creation of Non-Conformance on
Material Tracking Unit response
1. Operating in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

OPEN_NC_ON_PRODUCTresponse

Description

Response for Open Automatically Non-Conformances
on Material Tracking Unit

Dispatch Rule

fifowithpredecessors

2. Select the OPEN_NC_ON_PRODUCTresponse Message Type created in the previous step and click
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.

2. Click the Add Object

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous step and click

.

4. Select Valid Message Types and click
to add the following Items:
• OPEN_NC_ON_PRODUCT
• OPEN_NC_ON_PRODUCTresponse
5. Select Message Type Functions, click
click

to edit the Msg Type Extraction Function, type MessageType and

.

6. Operating in the Message Type Functions area, in the Other Functions section, click
and insert the
following function, which is used to extract the Message Type from the XML file root node:
NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Sentence Non-Conformances of Type Quality

This page describes the configurations that are necessary to exchange messages between the MES layer and the
Shop Floor, in order to trigger the automatic sentencing of a Quality Non-Conformance by Machines or
Workcenters, in case of integration between Opcenter Execution Discrete and Opcenter Connect MOM.

Workflow
1. Import the SENTENCE_NC Message Map.
2. Configure the Message Type for:
• the Automatic Sentencing call
• the Automatic Sentencing response
3. Configure the UADMAutomaticShopFloorChannel Message Channel.

Importing the SENTENCE_NC Message Map
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.

5. Locate the %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping\SENTENCE_NC.miom file and
click Open.
6. Click Save Map.

Configuring the Message Type for the Automatic Sentencing call
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message Types tab.
2. Click the Add Object

icon to create a new Message Type with the following properties:

Parameter

Value

Name

SENTENCE_NC

Description

Sentence Automatically a Non-Conformance by Machines or
Workcenters

Dispatch Rule

fifowithpredecessors

3. Select the SENTENCE_NC Message Type created in the previous step and click
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Message Map

SENTENCE_NC

Message Map Revision

2

Workflow

sit_ua_rest_call

5. Select Message Attributes and click
Message Attribute

.

to add the following Items:
Parameters

1

• Name: restcommand
• Function: equals
• Function Args: /Application/AppU4DM/odata/
UADMAutomaticSentenceNonConformance
• Do Not Promote: false
• Include In Event: false

2

• Name: httpverb
• Function: equals
• Function Args: POST
• Do Not Promote: false
• Include In Event: false

Message Attribute

Parameters

3

• Name: replacementstring
• Function: equals
• Function Args: «
• Do Not Promote: false
• Include In Event: false

6. Click Save

.

Configuring the Message Type for the Automatic Sentencing response
1. Operating in the Message Types tab, click the Add Object
following properties:

icon to create a new Message Type with the

Parameter

Value

Name

SENTENCE_NCresponse

Description

Response for Automatic Non-Conformance Sentencing by
Machines or Workcenters

Dispatch Rule

fifowithpredecessors

2. Select the SENTENCE_NCresponse Message Type created in the previous step and click
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

.

Configuring the UADMAutomaticShopFloorChannel Message Channel
The Message Channel is common to all use cases. You may have already configured it. In this case, you
need to perform only steps 3 and 4 of the procedure below.
1. In the Opcenter Connect MOM > Opcenter Connect MOM Configuration page, select the Message
Channels tab.
2. Click the Add Object

244

icon to create a new Message Channel with the following properties:

Parameter

Value

Name

UADMAutomaticShopFloorChannel

Description

Message Channel for Opcenter EX DS Shop Floor

Is Active

Selected

Parameter

Value

Map Message

Selected

3. Select the UADMAutomaticShopFloorChannel Message Channel created in the previous step and click

.

4. Select Valid Message Types and click
• SENTENCE_NC
• SENTENCE_NCresponse

to add the following Items:

5. Select Message Type Functions, click

to edit the Msg Type Extraction Function, type MessageType and

click

.

6. Operating in the Message Type Functions area, in the Other Functions section, click
and insert the
following function, which is used to extract the Message Type from the XML file root node:
NAME

FUNCTION TYPE

ARGUMENTS

MessageType

nodename

/*

7. Click Add Item.

##### How to Automatically Receive Input Messages

This page describes the configurations that are necessary to receive Input Messages from the Warehouse,
containing information on the state of Kanban calls made for the replenishment of Materials, in case of integration
between Opcenter Execution Discrete and Opcenter Connect MOM.
After importing the opcenterexds_input Workflow, you must create the Message Types for input messages.

Workflow
1. Configure the Message Type for:
• the Input Message call
• the Input Message response
2. Configure the OpcenterEXDSInputMessageChannel Message Channel.

Configuring the Message Type for the Input Message Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

InputMessage

Description

Input Message Message Type

Dispatch Rule

fifowithpredecessors

3. Select the Input Message Message Type and click
.
4. Select Additional Configuration and set the Workflow parameter to opcenterexds_input.

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

restcommand

equals

/Application/Kanban/
odata/
ReceiveXMLInputMessage

false

false

httpverb

equals

POST

false

false

replacementstrin
g

equals

«

false

false

6. Click Save

.

Configuring the Message Type for the Input Message Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

InputMessageresponse

Dispatch Rule

fifowithpredecessors

2. Select the InputMessageresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

Configuring the Message Channel for Input Messages
1. In the Opcenter Connect MOM General Configuration page, click the Message Channels tab.
2. Click the Add Object

icon, to create a new Message Channel with the following properties:

Parameter

Value

Name

OpcenterEXDSInputMessageChannel

Description

Message Channel for Input Message

Is Active

Selected

Map Message

Selected

3. Select the Message Channel you have created.

4. Select Valid Message Types and click
data you want to import and remove:

in the Valid Message Types section, to add the items relative to the

Involved Data

Items to be selected

Input Message

• InputMessage
• InputMessageresponse

5. Select Message Type Functions, click
click

to edit the Msg Type Extraction Function, type MessageType and

.

6. In the Message Type Functions area, in the Other Functions section, click
and define the following
functions, which are used to extract the Message Type from the XML file root nodes:
Name

Function Type

Arguments

MessageType

conditional

fn::IsInputMessage;InputMessage;Unknown

IsInputMessage

ifequal

fn::GetRootNodeName;MESSAGE

GetRootNodeName

nodename

/*

#### Messages for Data Import

After importing the Workflow, you must perform a series of steps to be able to automatically import and delete
data.

Workflow
1. Import the Message Map.
2. Configure the Message Type of interest.
3. Configure the Message Channel for XML files.
4. Configure the Message Channel for JSON files.

##### Importing the Message Map

One of the steps required to configure Opcenter Connect MOM to perform an automatic import of data is to import
the RemoveMessageHeader.miom Message Map file into the Opcenter Connect MOM Map Designer application.

Procedure
1. Open the Opcenter Connect MOM Map Designer application.
2. In the Opcenter CN MOM Server Settings tab, configure the credentials to connect to the application server. A
user with Administrative rights must be entered.
3. Click Save Settings.
4. Click Import Map.
5. Locate the RemoveMessageHeader.miom file (installed by default
in %SITUnifiedSystemRoot%VApps\UADM\MIOIntegration\Mapping on the Opcenter Execution
Discrete machine) and click Open.
6. Click Save Map.

##### How to Configure the Message Types

After importing the Workflow and the Message Map, you must create the Message Types for the call of the data you
want to import and delete, and for the related response.

Available Operations
• Configuring Message Types for Materials
• Configuring Message Types for Functional Codes
• Configuring Message Types for Suppliers
• Configuring Message Types for ERP Orders
• Configuring Message Types for Features
• Configuring Message Types for Bills of Features
• Configuring Message Types for Bills of Materials
• Configuring Message Types for Master Plans
• Configuring Message Types for Work Orders
• Configuring Message Types for Inspection Master Plan
• Configuring Message Types for Full Work Orders (XML File)
• Configuring Message Types for Full Work Orders (JSON File)
• Configuring Message Types for Custom Import Data Flows

9.4.4.2.1 How to Configure Message Types for Materials
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

DM_Material

Description

DM_Material Message Type

Dispatch Rule

fifowithpredecessors

3. Select the DM_Material Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportPRC_ImportMaterialLis
tFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

Enter the path of the
DM_Material.xslt
file, installed by default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

DM_Materialresponse

Dispatch Rule

fifowithpredecessors

2. Select the DM_Materialresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.2 How to Configure Message Types for Functional Codes
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call

1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

FunctionalCode

Description

FunctionalCode Message Type

Dispatch Rule

fifowithpredecessors

3. Select the FunctionalCode Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportPRC_ImportFunctional
CodeListFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

Enter the path of the
Functionalcode.xslt
file, installed by default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response

1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

FunctionalCoderesponse

Dispatch Rule

fifowithpredecessors

2. Select the FunctionalCoderesponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create paramater to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.3 How to Configure Message Types for Suppliers
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

Supplier

Description

Supplier Message Type

Dispatch Rule

fifowithpredecessors

3. Select the Supplier Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportPRC_ImportSupplierLi
stFromXML

false

false

Name

Function

Function Args

Do Not Promote

Include In Event

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

Enter the path of the
Supplier.xslt file, installed by
default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

Supplierresponse

Dispatch Rule

fifowithpredecessors

2. Select the Supplierresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.4 How to Configure Message Types for ERP Orders
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

ERPOrder

Description

ERPOrder Message Type

Dispatch Rule

fifowithpredecessors

3. Select the ERPOrder Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportERP_ImportERPOrderL
istFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

Enter the path of the
ERPOrder.xslt file, installed
by default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

Erporderresponse

Dispatch Rule

fifowithpredecessors

2. Select the Erporderresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.5 How to Configure Message Types for Features
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

Feature

Description

Feature Message Type

Dispatch Rule

fifowithpredecessors

3. Select the Feature Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

254

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportPRC_ImportFeatureLis
tFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

Name

Function

Function Args

Do Not Promote

Include In Event

xsltfile

equals

Enter the path of the
Feature.xslt file, installed by
default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

Featureresponse

Dispatch Rule

fifowithpredecessors

2. Select the Featureresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.6 How to Configure Message Types for Bills of Features
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

Bof

Description

Bill Of Feature Message Type

Parameter

Value

Dispatch Rule

fifowithpredecessors

3. Select the Bof Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportPRC_ImportBillOfFeat
ureListFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

Enter the path of the
ProductConfiguration.xslt
file, installed by default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

256

icon, to create a new Message Type with the

Parameter

Value

Name

Bofresponse

Parameter

Value

Dispatch Rule

fifowithpredecessors

2. Select the Bofresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.7 How to Configure Message Types for Bills of Materials
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

Bom

Description

Bill Of Materials Message Type

Dispatch Rule

fifowithpredecessors

3. Select the Bom Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportPRC_ImportBillOfMate
rialListFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

Name

Function

Function Args

Do Not Promote

Include In Event

xsltfile

equals

Enter the path of the
Bom.xslt file, installed by
default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

Bomresponse

Dispatch Rule

fifowithpredecessors

2. Select the Bomresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.8 How to Configure Message Types for Master Plans
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

258

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

Bop

Description

Bill Of Process Message Type

Parameter

Value

Dispatch Rule

fifowithpredecessors

3. Select the Bop Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportBOP_ImportBillOfProc
essListFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

Enter the path of the Bop.xslt
file, installed by default
in %SITUnifiedSystemRoot
%VApps\UADM\MIOIntegrati
on\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

Bopresponse

Parameter

Value

Dispatch Rule

fifowithpredecessors

2. Select the Bopresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.9 How to Configure Message Types for Work Orders
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

WorkOrder

Description

WorkOrder Message Type used in Import functionality.

Dispatch Rule

fifowithpredecessors

3. Select the WorkOrder Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

260

, to add the following Items:

Name

Function

Function Args

Do Not
Promote

Include In Event

importcomma
nd

equals

/application/ImportDataFlow/
odata/
ImportWO_ImportWorkOrderListF
romXML

false

false

logcommand

equals

/application/ImportDataFlow/
odata/LogWorkFlowFromXML

false

false

Name

Function

Function Args

Do Not
Promote

Include In Event

xsltfile

equals

Enter the path of the
WorkOrder.xslt file, installed by
default in
%SITUnifiedSystemRoot%VApps\
UADM\MIOIntegration\XSLT on
the Opcenter Execution Discrete
machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

WorkOrderresponse

Dispatch Rule

fifowithpredecessors

2. Select the WorkOrderresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.10 How to Configure Message Types for Inspection Master Plan
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

InspectionMasterPlan

Parameter

Value

Description

Message type used in Inspection Master Plan Functionality.

Dispatch Rule

fifowithpredecessors

3. Select the IMP Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportCHR_ImportInspection
PlanListFromXML

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

C:\XSLT\IMP.xslt

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:
Parameter

Value

Name

InspectionMasterPlanresponse

Dispatch Rule

fifowithpredecessors

2. Select the IMPresponse Message Type and click

icon, to create a new Message Type with the

.

3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.11 How to Configure Message Types for Full Work Orders
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

FullWorkOrder

Description

Full Work Order Message Type

Dispatch Rule

fifowithpredecessors

3. Select the FullWorkOrder Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
ImportDataFlow/odata/
ImportFullWorkOrder_Impo
rtFullWorkOrderListFromXM

false

false

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

Name

Function

Function Args

Do Not Promote

Include In Event

xsltfile

equals

Enter the path of the
FullWorkOrder.xslt
file, installed by default
in %SITUnifiedSystemRoo
t%VApps\UADM\MIOIntegr
ation\XSLT on the Opcenter
Execution Discrete
machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

FullWorkOrderresponse

Dispatch Rule

fifowithpredecessors

2. Select the FullWorkOrderresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.12 How to Configure Message Types for Full Work Orders (JSON File)
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

264

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

FullWorkOrderJson

Parameter

Value

Description

Full Work Order Json Message Type

Dispatch Rule

fifowithpredecessors

3. Select the FullWorkOrderJson Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomma
nd

equals

/application/ImportDataFlow/
odata/
ImportFullWorkOrder_ImportF
ullWorkOrderListFromXML

false

false

logcommand

equals

/application/ImportDataFlow/
odata/LogWorkFlowFromXML

false

false

xsltfile

equals

Enter the path of the
FullWorkOrder.xslt
file, installed by default
in %SITUnifiedSystemRoot%
VApps\UADM\MIOIntegration
\XSLT on the Opcenter
Execution Discrete machine.

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

xsltmapfile

equals

Enter the path of the
MapFullWorkOrder file, instal
led by default
in %SITUnifiedSystemRoot%
VApps\UADM\MIOIntegration
\XSLT on the Opcenter
Execution Discrete machine.

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

FullWorkOrderJsonresponse

Dispatch Rule

fifowithpredecessors

2. Select the FullWorkOrderJsonresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

9.4.4.2.13 How to Configure Message Types for Custom Import Data Flow
After importing the Workflow, you must create the Message Types for both the automatic call and the automatic
response.

Configuring the Message Type for the Automatic Call
1. In the Opcenter Connect MOM General Configuration page, click the Message Types tab.
2. Click the Add Object

icon, to create a new Message Type with the following properties:

Parameter

Value

Name

EntityName

Description

Entity Name Message Type

Dispatch Rule

fifowithpredecessors

3. Select the EntityName Message Type and click
.
4. Select Additional Configuration and configure the following parameters:
Parameter

Value

Workflow

opcenterexds_import

5. Select Message Attributes and click

266

, to add the following Items:

Name

Function

Function Args

Do Not Promote

Include In Event

importcomman

equals

/application/
CustomAppName/odata/
ImportEntityNameFromXML

false

false

Name

Function

Function Args

Do Not Promote

Include In Event

logcommand

equals

/application/
ImportDataFlow/odata/
LogWorkFlowFromXML

false

false

xsltfile

equals

C:\XSLT\EntityName.xslt

false

false

httpverb

equals

POST

false

false

plantid

equals

xp:://@Plant

false

false

6. Click Save

.

Configuring the Message Type for the Automatic Response
1. Working in the Message Types tab, click the Add Object
following properties:

icon, to create a new Message Type with the

Parameter

Value

Name

EntityNameresponse

Dispatch Rule

fifowithpredecessors

2. Select the EntityNameresponse Message Type and click
.
3. Select Additional Configuration and set the Outbound On Create parameter to Selected.
4. Leave the other attributes as default (recommended) and click Save

.

##### Configuring the Message Channel For XML Files

After defining the Message Types for message calls and responses, it is necessary to create a Message Channel.
The Message Channel for import and deletion is common to all import configurations. You may have
already configured it. In this case, you can skip this configuration step.

Procedure
1. In the Opcenter Connect MOM General Configuration page, click the Message Channels tab.
2. Click the Add Object

icon, to create a new Message Channel with the following properties:

Parameter

Value

Name

OpcenterEXDSImportChannel

Parameter

Value

Description

For example: Message Channel for importing data to Opcenter
Execution Discrete

Is Active

Selected

Map Message

Selected

3. Select the Message Channel you have created.
4. Select Valid Message Types and click
data you want to import and remove:

268

in the Valid Message Types section, to add the items relative to the

Materials

• DM_Material
• DM_Materialresponse

Functional Codes

• FunctionalCode
• FunctionalCoderesponse

Suppliers

• Supplier
• Supplierresponse

ERP Orders

• ERPOrder
• ERPOrderresponse

Bills of Features

• Bof
• Bofresponse

Features

• Feature
• Featureresponse

Bills of Materials

• Bom
• Bomresponse

Master Plans

• Bop
• Bopresponse

Custom Import

• EntityName
• EntityNameresponse

Work Orders

• WorkOrder
• WorkOrderresponse

Inspection Master Plan

• InspectionMasterPlan
• InspectionMasterPlanresponse

Full Work Order

• FullWorkOrder
• FullWorkOrderresponse

5. Select Message Type Functions, click

to edit the Msg Type Extraction

Function, type SupplierTypeExtract and click

.

6. In the Message Type Functions area, in the Other Functions section, click
and define the following
functions, which are used to extract the Message Type from the XML file root nodes:
Name

Function Type

Arguments

SupplierTypeExtract

conditional

fn::IsSupplier;Supplier;fn::BomExtract

BomExtract

conditional

fn::IsBom;Bom;fn::DM_MaterialExtract

DM_MaterialExtract

conditional

fn::IsDM_Material;DM_Material;fn::FunctionalCodeExtract

FunctionalCodeExtract

conditional

fn::IsFunctionalCode;FunctionalCode;fn::BopExtract

BopExtract

conditional

fn::IsBop;Bop;fn::BofExtract

BofExtract

conditional

fn::IsBof;Bof;fn::ERPOrderExtract

ERPOrderExtract

conditional

fn::IsERPOrder;ERPOrder;fn::WorkOrderExtract

FeatureExtract

conditional

fn::IsFeature;Feature;Unknown

WorkOrderExtract

conditional

fn::IsWorkOrder;WorkOrder;fn::InspectionMasterPlanExtract

InspectionMasterPlanExt
ract

conditional

fn::IsInspectionMasterPlan;InspectionMasterPlan;fn::FullWo
rkOrderExtract

FullWorkOrderExtract

conditional

fn::IsFullWorkOrder;FullWorkOrder;fn::FeatureExtract

IsSupplier

ifequal

xp:://@FlowName;SUPMD

IsBom

ifequal

xp:://@FlowName;BOM

IsBop

ifequal

xp:://@FlowName;BOP

IsDM_Material

ifequal

xp:://@FlowName;MTMD

IsFunctionalCode

ifequal

xp:://@FlowName;FCMD

IsBof

ifequal

xp:://@FlowName;LOF

Name

Function Type

Arguments

IsERPOrder

ifequal

xp:://@FlowName;ERPLIST

IsFeature

ifequal

xp:://@FlowName;FEATMD

IsWorkOrder

ifequal

xp:://@FlowName;WorkOrder

IsInspectionMasterPlan

ifequal

xp:://@FlowName;IMP

IsFullWorkOrder

ifequal

xp:://@FlowName;FullWorkOrder

7. If your import includes entities other than those foreseen by the system (for which you have created custom
XML and XSLT files), perform the following additional operations:
• For each import, create the functions:
Name

Function Type

Arguments

IsEntityName

ifequal

xp:://@FlowName;FlowIdentifier

EntityNameExtract

conditional

fn:isEntityName;fn:EntityNameNextInFlo
w

Where EntityName is the name of the entity to be imported and FlowIdentifier is the Identifier assigned to
the custom import data flow.
• Modify the Arguments of the last function in the pipeline (by default FeatureExtract) replacing
Unknown with the name of the new Extract function you have just configured.

##### Configuring the Message Channel for JSON files

After defining the Message Types for message calls and responses, it is necessary to create a Message Channel.
The Message Channel for import and deletion is common to all import configurations. You may have
already configured it. In this case, you can skip this configuration step.

Procedure
1. In the Opcenter Connect MOM General Configuration page, click the Message Channels tab.
2. Click the Add Object

270

icon, to create a new Message Channel with the following properties:

Parameter

Value

Name

For JSON files: OpcenterEXDSImportJsonChannel

Description

For example: Message Channel for importing data to Opcenter
Execution Discrete

Parameter

Value

Is Active

Selected

Map Message

Selected

3. Select the Message Channel you have created.
4. Select Valid Message Types and click
data you want to import and remove:

in the Valid Message Types section, to add the items relative to the

Involved Data

Items to be selected

Full Work Order Json

• FullWorkOrderJson
• FullWorkOrderJsonresponse

5. Select Message Type Functions, click

to edit the Msg Type Extraction

Function, type SupplierTypeExtract and click

.

6. In the Message Type Functions area, in the Other Functions section, click
and define the following
function, which is used to extract the Message Type from the JSON file root nodes:
Name

Function Type

Arguments

MessageType

ifequal

js::MessageType

#### How to Define the File Adapter

Depending on the functionality you intend to use, the related File Adapter must be defined accordingly:
• Define the file adapter for Shop Floor Operations
• Define the file adapter for data import (XML files)
• Define the file adapter for data import (JSON files)
• Define the file adapter for input messages
For the Shop Floor and Input messages, the Multiplant can be addressed with dedicated Adapters for each plant
along with its dedicated MOM Connection for each respective plant.
In the plant specific MOM Connections, the address should include the plant information, for example, http://
myexdsserver/sit-svc/Plant1.
On the other hand, for the Import messages the plant is inside the XML Message itself, so a MOM Connection without
the plant information can be used.
You may have already configured the File Adapters during previous configurations. In this case, you can
skip this step.

Defining the File Adapter for Shop Floor Operations
1. Log in to the Opcenter Connect MOM Web Application.
2. Click the Opcenter Connect MOM Adapter Configuration tile.
3. In the Opcenter Connect MOM Adapter Configuration page, click the File tab.

4. Click the Add Object

icon to create a new File Adapter with the following properties:

Parameter

Value

Name

uadmautomaticshopfloorfileadapter
Note Lower case is mandatory.

Description

File Adapter for Opcenter EX DS Shop Floor

Channel Source

miochannelsource

Message Channel

UADMAutomaticShopFloorChannel

Content Format

Inbound Name Format

{messagename}

Outbound Name Format

response_{messagename}

Is Active

Selected

5. Select the uadmautomaticshopfloorfileadapter File Adapter created in the previous step and click
6. Select File Adapter Configuration and configure the following parameters:

.

Parameter

Value

Inbound URI

Type the path to the folder where the input XML file will be placed,
for example: C:\UADMAutomaticShopFloor\inbound

Outbound URI

Type the path to the folder where the output XML file will be placed,
for example: C:\UADMAutomaticShopFloor\outbound

Is XML

Selected

7. Select Additional Configuration and configure the following parameter:
Parameter

Value

Mom Connection Name

UADM

8. Click Save

.

Defining the File Adapter for Data Import (XML Files)
1. Log in to the Opcenter Connect MOM Web Application.
2. In the Opcenter Connect MOM Adapter Configuration page, click the File tab.

3. Click the Add Object

icon, to create a new File Adapter with the following properties:

Parameter

Value

Name

For example: opcenterexdsimportfileadapter
Note Lower case is mandatory.

Description

For example: File Adapter for importing data to Opcenter
Execution Discrete

Channel Source

miochannelsource

Message Channel

OpcenterEXDSImportChannel

Content Format

Inbound Name Format

{messagename}

Outbound Name Format

Define a file name format according to your needs (for
example, response_{messagename}).
Refer to section Appendix B: Message Name Format Keywords
of the Manufacturing Interoperability User Guide.

Is Active

Selected

4. Select the opcenterexdsimportfileadapter File Adapter and click
.
5. Select File Adapter Configuration and configure the following parameters:
Parameter

Value

Inbound URI

The path to the folder where the input XML file will be placed, for
example: C:\OpcenterEXDSImport\inbound

Outbound URI

The path to the folder where the output XML file will be placed, for
example: C:\OpcenterEXDSImport\outbound

Is XML

Selected

6. Select Additional Configuration and configure the following parameter:
Parameter

Value

Mom Connection Name

The name of the MOM Connection configured before.

7. Click Save

.

Defining the File Adapter for Data Import (JSON files)
1. Log in to the Opcenter Connect MOM Web Application.
2. In the Opcenter Connect MOM Adapter Configuration page, click the File tab.
3. Click the Add Object

icon, to create a new File Adapter with the following properties:

Parameter

Value

Name

For example: opcenterexdsimportfileadapterJson
Note Lower case is mandatory.

Description

For example: File Adapter for importing data to Opcenter
Execution Discrete

Channel Source

miochannelsource

Message Channel

OpcenterEXDSImportJsonChannel

Content Format

JSON

Inbound Name Format

{messagename}

Outbound Name Format

Define a file name format according to your needs (for
example, response_{messagename}).
Refer to section Appendix B: Message Name Format Keywords
of the Manufacturing Interoperability User Guide.

Is Active

Selected

4. Select the opcenterexdsimportfileadapterJson File Adapter and click
.
5. Select File Adapter Configuration and configure the following parameters:
Parameter

Value

Inbound URI

The path to the folder where the input JSON file will be placed, for
example: C:\OpcenterEXDSImport\inboundJson

Outbound URI

The path to the folder where the output JSON file will be placed, for
example: C:\OpcenterEXDSImport\outboundJson

Is XML

False

6. Select Additional Configuration and configure the following parameter:

Parameter

Value

Mom Connection Name

The name of the MOM Connection configured before.

7. Click Save

.

Defining the File Adapter for Input Messages
1. Log in to the Opcenter Connect MOM Web Application.
2. In the Opcenter Connect MOM Adapter Configuration page, click the File tab.
3. Click the Add Object

icon, to create a new File Adapter with the following properties:

Parameter

Value

Name

For example: opcenterexdsinputmsgadapter
Note Lower case is mandatory.

Description

For example: File Adapter for Input Messages

Channel Source

miochannelsource

Message Channel

The name of the channel created before.

Content Format

Inbound Name Format

{messagename}

Outbound Name Format

Define a file name format according to your needs (for
example, response_{messagename}).
Refer to section Appendix B: Message Name Format Keywords
of the Manufacturing Interoperability User Guide.

Is Active

Selected

4. Select the opcenterexdsinputmsgadapter File Adapter and click
.
5. Select File Adapter Configuration and configure the following parameters:
Parameter

Value

Inbound URI

The path to the folder where the input XML file will be placed, for
example: C:\OpcenterEXDSInputMessage\inbound

Outbound URI

The path to the folder where the output XML file will be placed, for
example: C:\OpcenterEXDSInputMessage\outbound

Parameter

Value

Is XML

Selected

6. Select Additional Configuration and configure the following parameter:
Parameter

Value

Mom Connection Name

The name of the MOM Connection configured before.

7. Click Save

.

#### How to Tune Opcenter CN MOM Parameters to Improve Performances

During the automatic import of data, you may need to import a file containing large amounts of data or process
many files at the same time. In order to reduce the risk of having time-out errors or skipping some files, it is possible
to edit the default value of certain parameters related to Opcenter Connect MOM configuration.

Available Operations
• Edit the File Adapter Configuration Settings.
• Edit the Message Types Configuration Settings.
• Edit the Workflow Configuration Settings.
• Edit the CIO Site Configuration Settings in IIS.

Editing the File Adapter Configuration Settings
1. In the Opcenter Connect MOM Adapter Configuration page, select File Adapter Configuration.
2. Edit the default value of the Max Read Retries parameter, according to your needs. This permits processing
many files at the same time, reducing the risk of skipping some of them during the import.

Editing the Message Types Configuration Settings
1. In the Opcenter Connect MOM General Configuration page, select Dispatch Rules. Select the
fifowithprecedessors Dispatch Rule and then click Base Configuration. Edit the default value of the Max
Number Of Threads parameter. If you want to maximize the parallelism depending on the resources of your
machine, the recommended value lies between a range of 10 to 20.
2. Click Message Types, select the Message Type of interest (for example, FullWorkOrder) and then
click Additional Configuration. If the system imports thousands of messages in one-shot, it must be possible
for a message to wait for some time in the cache before it being picked up by the dispatch rule in order to start
the workflow. For this reason, edit the default value of the Time To Live (minutes) parameter, a possible value
could be 180 or even greater than this. Edit also the default values of the Max Retry Count and Min Retry
Interval (milliseconds) parameters. Possible values could be 10 for the Max Retry Count and 120.000 for Min
Retry Interval (milliseconds), if you want to cover a possible downtime of twenty minutes of the Opcenter
Execution Foundation server.

Editing the Workflow Configuration Settings
In the Workflow, assign in the rest call activities a timeout greater than the maximum execution time of the
command (for example, 1 minute could not be enough and it could be better to increase it up to 5 minutes).

Editing the CIO Site Configuration Settings in IIS
1. In the Internet Information Services (IIS) Manager, click the Sites folder and then click the CIO Site, where
you can find the tool Configuration Editor.
2. In the section system.web/httpRuntime, change the default value of either one or both parameters mentioned
below, according to your needs:
• maxRequestLength, to import large size files,
• shutdownTimeout, to avoid time-out errors during the import of large amounts of data in one file.

### Troubleshooting - Manual Configuration for Integration with Opcenter IPL

Opcenter Execution Discrete comes provided with a dedicated dxp file for integration between Opcenter EX DS and
Opcenter IPL that, once imported into Data Integration System and after being appropriately configured, enables
integration between the two products.
This troubleshooting section provides information on how to manually recreate the imported configurations in DIS.
Only the creation of a DIS Project and all its connectors used in this integration are covered here.
All the other steps that are necessary to make the integration work (for example, installing the IPLIntegration
Extension App, or creating a Message Destination in Opcenter EX DS to route Kanban Calls to DIS) remain valid and
are explained in How to Integrate Opcenter Execution Discrete with Opcenter Intraplant Logistics (Opcenter IPL).

Workflow
1. (Only if there is no pre-existing DIS Project to be enriched) Operating in DIS Management Console, create a DIS
Project manually.
2. Create all DIS Connectors Required for Integration with Opcenter IPL.
3. If you have created a new DIS Project manually, operating in Windows Services, restart service Opcenter
Execution Foundation Aux Svc Core.
Otherwise, if you are working on a pre-existing DIS Project, operating in DIS Management Console, synchronize
your DIS Project.

#### Creating a DIS Project Manually

Procedure
For information about creating a DIS Database and generating a Master Key, see the Data Integration
System User Manual.
To create a new project from scratch:
1. In DIS Management Console , select File > New Project: the New Project tab is displayed.
2. In the Project Name edit box, enter the name that you want to assign to the project you are creating (for
example, EXDS_IPL_Integration).
3. Create the DIS Database with the correct Database Data Source and Init Catalog.
4. Save the DIS Project.
5. Generate a New Master Key for the DIS Project.
6. Save the DIS Project again.
7. Operating in Windows Services, restart service Opcenter Execution Foundation Aux Svc Core.

#### Creating All DIS Connectors Required for Integration with Opcenter IPL

Here is the list of all the DIS connectors that must be created so that all use cases are covered:
• A WebService Connector for receiving calls from Opcenter IPL
• An SDK Connector for the Resources Hierarchy use case
• An SDK Connector for the Material Request use cases
• An HTTP Client Connector for querying the default Equipment Hierarchy inOpcenter Execution Discrete for the
Resources Hierarchy use case.
• Three (3) HTTP Client Connectors for invoking all the APIs provided by Opcenter IPL for the Kanban-call use
cases (creation, cancellation, delivery).
These connectors are created using DIS Management Console.

Prerequisites
• You have already created your DIS Project and configured its database.
• You have copied the following .dll files (found under folder %SITUnifiedVAppsRoot%\UADM\DIS\IPL) to
%DISPath%\BIN:
• Siemens.OpcenterEX.DIS.IPLSDKResourcesHierarchy.dll
• Siemens.OpcenterEX.DIS.IPLSDKMaterialRequest.dll.

##### Procedure

1. In DIS Management Console, operating on the Tree Structure, expand the node representing your DIS Project.
2. On node connectors, perform a right-click, select Add Connector and then select WebService.
3. In field Connector Name, enter a name (for example, WSIPLResourcesHierarchy) to be assigned to the
WebService connector you are creating.
4. On node connectors, perform a right-click, select Add Connector and then select SDK.
5. In field Connector Name, enter a name (for example, SDKIPLResourcesHierarchy) to be assigned to the SDK
connector (for the Resources Hierarchy use case) you are creating.
6. Perform the settings as specified in the table below:
In tab....

Do this...

External Processor

Set attribute Path to
Siemens.OpcenterEX.DIS.IPLSDKResourcesHierarchy.dll i
n folder %DISPath%\BIN.
Set attribute Class Name to
Siemens.OpcenterEX.DIS.IPLSDKResourcesHierarchy.Res
ourcesHierarchy.

Function Mapping

After adding a new row:
• In column Type, insert ResourcesHierarchyToIPL.
• In column Schema, insert Hierarchy.

7. On node connectors, perform a right-click, select Add Connector and then select SDK.
8. In field Connector Name, enter a name (for example, SDKIPLMaterialRequest) to be assigned to the SDK
connector (for the Material Request use cases) you are creating.

9. Perform the settings as specified in the table below:
In tab....

Do this...

External Processor

Set attribute Path to
Siemens.OpcenterEX.DIS.IPLSDKMaterialRequest.dll in
folder %DISPath%\BIN.
Set attribute Class Name to
Siemens.OpcenterEX.DIS.IPLSDKMaterialRequest.Materi
alRequest.

Notification

After adding a new row:
• In column Type, insert
EXDSMaterialRequestToIPL.
• In column Schema, insert MaterialRequest.

1. On node connectors, perform a right-click, select Add Connector and then select HTTP Client.
2. In field Connector Name, enter a name (for example, HTTPIPLResourcesHierarchy) to be assigned to the HTTP
Client connector (for querying the default Equipment Hierarchy inOpcenter Execution Discrete for the Resources
Hierarchy use case) you are creating.
3. Perform the settings as specified in the table below:
In tab....

Do this...

HTTP Request

Write the URL with a value that points to Opcenter Execution
Discrete, App AppU4DM, entity EXDSIPLResourcesHierarchy (for
example, http://MyEXDSServer/sit-svc/DefaultPlant/Application/
AppU4DM/odata/EXDSIPLResourcesHierarchy), paying attention
to protocol (http/https), hostname (MyEXDSServer in the
example) and plant (Multiplant concept, DefaultPlant in the
example).
.
Leave the value (GET) set for Method.
In area Headers, add a row with Name set to Accept and Value set
to application/json, text/plain, /

Function Mapping

After adding a new row:
• In column Type, insert
EXDSResourcesHierarchyToIPL.
• In column Schema, insert Hierarchy.

Access

Inside area HTTP Basic Authentication, enter a valid User Name
and Password for authentication to Opcenter Execution Discrete.

4. On node connectors, perform a right-click, select Add Connector and then select HTTP Client.

5. In field Connector Name, enter a name (for example, HTTPIPLMaterialRequestCreation) to be assigned to the
HTTP Client connector (for invoking the API provided by Opcenter IPL for the Kanban-call creation use case) you
are creating.
6. Perform the settings as specified in the table below:
In tab....

Do this...

HTTP Request

Write the URL with a value that points to the Opcenter IPL
Material Request API (for example, https://MyIPLServer:5201/
api/material-requests), paying attention to protocol (http/
https), hostname (MyIPLServer in the example) and port (5201
in the example)..
Change the value set for Method to POST.
In area Headers, add two rows with the following values,
respectively:
- Name set to Content-Type and Value set to application/
json;charset=UTF-8
- Name set to Accept and Value set to application/json

Function Mapping

After adding a new row:
• In column Type, insert EXDSMaterialRequestToIPL.
• In column Schema, insert MaterialRequestCreation.

7. On node connectors, perform a right-click, select Add Connector and then select HTTP Client.
8. In field Connector Name, enter a name (for example, HTTPIPLMaterialRequestAcknowledge) to be assigned
to the HTTP Client connector (for invoking the API provided by Opcenter IPL for the Kanban-call delivery use
case) you are creating.
9. Perform the settings as specified in the table below:
In tab....

Do this...

HTTP Request

Write the URL with a value that points to the Opcenter IPL Material
Request Acknowledge API (for example, https://MyIPLServer:5201/
api/material-requests/acknowledgement), paying attention to
protocol (http/https), hostname (MyIPLServer in the example)
and port (5201 in the example).
Change the value set for Method to POST.
In area Headers, add two rows with the following values,
respectively:
- Name set to Content-Type and Value set to application/
json;charset=UTF-8
- Name set to Accept and Value set to application/json.

In tab....

Do this...

Function Mapping

After adding a new row:
• In column Type, insert EXDSMaterialRequestToIPL.
• In column Schema, insert
MaterialRequestAcknowledge.

10. On node connectors, perform a right-click, select Add Connector and then select HTTP Client.
11. In field Connector Name, enter a name (for example, HTTPIPLMaterialRequestCancellation) to be assigned
to the HTTP Client connector (for invoking the API provided by Opcenter IPL for the Kanban-call cancellation)
you are creating.
12. Perform the settings as specified in the table below:
In tab....

Do this...

HTTP Request

Write the URL with a value that points to the Opcenter IPL Material
Request Cancellation API (for example, https://MyIPLServer:5201/
api/material-requests/cancellation), paying attention to protocol
(http/https), hostname (MyIPLServer in the example) and port
(5201 in the example).
Change the value set for Method to POST.
In area Headers, add two rows with the following values,
respectively:
- Name set to Content-Type and Value set to application/
json;charset=UTF-8
- Name set to Accept and Value set to application/json.

Function Mapping

After adding a new row:
• In column Type, insert EXDSMaterialRequestToIPL.
• In column Schema, insert
MaterialRequestCancellation.

13. Save the DIS Project.
14. Go to Control Panel > Internet Options > Security tab >Trusted Sites > Sites button and add both URLs to
Opcenter Execution Discrete you set for connector HTTPIPLResourcesHierarchy and the one for connector
HTTPIPLMaterialRequestCreation among your trusted sites.
