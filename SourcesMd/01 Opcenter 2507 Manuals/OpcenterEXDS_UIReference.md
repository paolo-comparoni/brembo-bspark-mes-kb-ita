# OpcenterEXDS_UIReference

> Documento sorgente: `E:\BremboDocs\01 Opcenter 2507 Manuals\OpcenterEXDS_UIReference.pdf`  
> Tipo: PDF · Pagine: 83


## Pagina 1

Opcenter Execution Discrete 2507.0001

UI Reference and Customization Manual

10/2025
PL20250808636629882


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

PL20250808636629882

Copyright © Siemens AG 2025

Digital Industries

20251024_141854

Technical data subject to change

Postfach 48 48
90026 NÜRNBERG
GERMANY


## Pagina 3

Table of Contents
1

Essentials to Approaching UI Customization in Opcenter Execution Discrete ..7

2

How to Create a Custom Application ...................................................................9

3

How to Customize the User Interface.................................................................11

3.1

Identifying the Customizable Providers...................................................................................11

3.2

Customizing the Item Collection Viewers ................................................................................12

3.2.1 Item Collector Viewer Service .................................................................................................................................13

3.3

Customizing the Property Grids ...............................................................................................13

3.3.1 Property Grid Service ..............................................................................................................................................14

3.4

Customizing the Command Bars..............................................................................................19

3.5

Customizing the Menu Buttons ................................................................................................21

3.6

Customizing the Tab Controls ..................................................................................................21

3.7

Customizing oData Queries and Backend Commands ...........................................................22

3.8

Customizing the Icons...............................................................................................................25

3.9

Customizing the Default UI Configuration...............................................................................26

3.10 Customizing the UI Module Initialization.................................................................................26

4

Opcenter Execution Discrete UI Modules...........................................................28

4.1

CLM Resource Management UI Module ...................................................................................29

4.2

Configuration Keys UI Module ..................................................................................................29

4.3

DCD Engineering UI Module......................................................................................................30

4.4

Defect Type Management UI Module .......................................................................................31

4.5

Document Management UI Module .........................................................................................32

4.6

Genealogy UI Module ................................................................................................................32

4.7

High Automation Mashup UI Module .......................................................................................33

4.7.1 High Automation Details Screen.............................................................................................................................34
4.7.2 High Automation Operator Landing Screen...........................................................................................................35
4.7.3 High Automation Operator Task List Screen..........................................................................................................35

4.8

Labor Tracking Management UI Module..................................................................................35

4.9

Non-Conformance Lifecycle UI Module ...................................................................................36

4.10 Non-Conformance Notification Management UI Module .......................................................38
4.11 Non-Conformance Supervisor Management UI Module .........................................................38
4.12 Operation/Step Category UI Module........................................................................................40

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

iii


## Pagina 4

4.13 Operator Landing Mashup UI Module ......................................................................................41
4.13.1 Operator Detail Screen............................................................................................................................................42
4.13.2 Operator Detail Steps Screen..................................................................................................................................42
4.13.3 Operator Landing Task List Screen.........................................................................................................................43
4.13.4 Operator Landing Home Screen .............................................................................................................................43

4.14 Order Work In Progress UI Module ...........................................................................................43
4.15 PowderGenealogy UI Module ...................................................................................................44
4.16 Process Catalog Management UI Module (Deprecated) .........................................................45
4.17 Team Management UI Module .................................................................................................45
4.18 Transport Operation Landing UI Module .................................................................................46
4.19 Users and Skills UI Module........................................................................................................47
4.20 Work Order As Built UI Module .................................................................................................48
4.21 Work Order As Planned BOP UI Module ...................................................................................50
4.22 Work Order Status UI Module (Deprecated) ............................................................................51

5

Opcenter Execution Discrete UI Components ...................................................53

5.1

Button Bar UI Component ........................................................................................................53

5.2

Bill of Materials UI Component.................................................................................................56

5.3

Customizable Button Bar UI Component ................................................................................58

5.4

High Automation Header Bar UI Component ..........................................................................59

5.5

Declare Defect UI Component ..................................................................................................60

5.6

Document Preview UI Component...........................................................................................61

5.7

Execution Group Details UI Component ..................................................................................63

5.8

Execution Groups Document Preview UI Component ............................................................64

5.9

Execution Groups Header Bar UI Component .........................................................................65

5.10 High Automation Equipment List UI Component....................................................................66
5.11 Load Powder UI Component ....................................................................................................66
5.12 Material Production UI Component .........................................................................................67
5.13 Material Tracking UI Component .............................................................................................68
5.14 Operation Header Bar UI Component......................................................................................68
5.15 Operation List UI Component...................................................................................................69
5.16 Part Program UI Component ....................................................................................................71
5.17 Print Job File UI Component ....................................................................................................72
5.18 Quality Inspection UI Component............................................................................................72

iv

Opcenter Execution Discrete2507.0001 - UI Reference and Customization Manual


## Pagina 5

5.19 Step List UI Component ............................................................................................................73
5.20 Task Details UI Component (Deprecated) ...............................................................................74
5.21 Task Container UI Component .................................................................................................77
5.22 Task Viewer UI Component ......................................................................................................80
5.23 Tracking AM Powder UI Component ........................................................................................81
5.24 Work Order Routing UI Component .........................................................................................82
5.25 Zero Touch Component UI Component...................................................................................82

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

v


## Pagina 6

6

ID

OpcenterEXDS_UIReference

Title

UI Reference and Customization Manual

Product Title

Opcenter Execution Discrete

Version Title

2507.0001

Product Version

OpcenterEXDS_2507.0001

Category

Development, Support

Summary

Provides information on how to customize the UI provided by Opcenter Execution Discrete

Audience

System Integrator, Support Engineer, Project Engineer, Commissioning Engineer, Developer

Revision

PL20250808636629882

State

Published

Author

Siemens AG

Language

en-US

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 7

Essentials to Approaching UI Customization in Opcenter Execution Discrete

1 Essentials to Approaching UI Customization in Opcenter
Execution Discrete
Customization is necessary whenever what is provided by default in Opcenter Execution Discrete does not
completely satisfy your project's requirements.
Depending on your needs, you can choose to:
Customize the UI provided in the Opcenter EX DS application without the need of writing additional code,
except for the code needed to wire together the components. This can be achieved by using the Mashup Editor
to combine UI Components to form new UI Modules to be added to your UI application. This new UI application
is not so much a revamped layout from a graphical standpoint, but rather a new way of presenting runtime data,
establishing relationships between its various elements according to your needs.
Create a custom UI application writing additional Javascript code which will be processed alternatively to the
standard code. The range of available customizations extends from basic changes to the user interface (for
example, changing icons or grid appearances) to complex interactions with the data model.
Extend Model-Driven UI Modules, as explained in section How to Extend User Interfaces in an Extension App of the
Opcenter Execution Foundation Development and Configuration Guide.
Extend Custom Actions in Model-Driven UI Modules, as explained in section How to Customize the User
Interface.

User Interface Terminology
Term

Definition

Page

Graphical layout displayed by a browser.

Screen

Root page which is the entry point of a particular concept.
Every module can contain one or more screens.

State

An Angular UI.Router state corresponds to a "place" in the application in terms of the overall UI and
navigation.
A state describes (via the controller / template / view properties) what the UI looks like and does at
that place.

Module

Collection of related user interface screens, which may be deployed using Solution Studio.
A Module can navigate to other Modules using States.

Compon
ent

AngularJS directive that can be used in the Mashup Editor of Solution Studio.

Controll
er

Angular object which "controls" data and the view used to show it.

Service

Function or object that is available for an Angular application. A Service can be used across
different Controllers in a consistent manner.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

7


## Pagina 8

Essentials to Approaching UI Customization in Opcenter Execution Discrete

Term

Definition

Provider

Term which groups Services and Angular Factories (all the customizable Angular objects).

How are Standard and Custom UI Codes Processed?
When a Opcenter EX DS page is loaded, the customization service checks if custom Angular Providers are present. If
a custom Provider is found, it is called when needed. Inside a custom Provider, it is possible to customize one or
more functions.
A custom Angular Provider or function has the same name of its corresponding standard version, plus
the _custom suffix. For example:
standard icons service: u4dm.services.icons
custom icons service: u4dm.services.icons_custom
Checking for custom Angular Providers is performed according to the following workflow:

8

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 9

How to Create a Custom Application

2 How to Create a Custom Application
Customizing Opcenter Execution Discrete is required whenever you need to extend the data model and/or the
related business logic. This may be for example:
new properties of Opcenter EX DS entities
new project entities
new commands
new events
new signals
new UIs (components, modules, screens).
The recommended way to customize Opcenter EX DS is developing an Extension App. The advantage of this
approach, compared to creating a Custom Application from scratch, is that:
it allows you to take advantage of the existing Public Object Model and its relationships
it allows you to extend Model Driven UIs provided by Opcenter EX DS.
For information about the creation of Extension Apps in Opcenter Execution Foundation , refer to How to Develop an
Extension App in the Opcenter Execution Foundation Development and Configuration Guide.
The following workflow represents an example of a complete customization to extend an Opcenter EX DS entity
imported into a Custom Functional Block. Steps needed only for customizing the User Interface are highlighted.
The instructions provided in the following workflow are based on the extension of the AppU4DM App, but
are valid for any other App that you want to extend in your solution.

Workflow

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

9


## Pagina 10

How to Create a Custom Application

1. In Project Studio:
Create a Custom Functional Block.
Create the commands to interact with.
Compile the Custom Functional Block.
Create an Extension App based on the AppU4DM App.
In the Extension App, reference the previously created Custom Functional Block.
Define the navigation property between the Custom Functional Block entity and the standard entities.
Customize the User Interface, if you have created Composite Commands.
Compile the Extension App.
2. In Solution Studio:
In the Opcenter EX DS solution, add the Extension App to the AppU4DM App .
Associate any custom Command to a master or runtime worker.
Build and deploy the Solution.

10

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 11

How to Customize the User Interface
Identifying the Customizable Providers

3 How to Customize the User Interface
Customizing the User Interface is generally required while creating a Custom Application, in order to implement the
desired modifications to the graphical layout and/or to the data model.
If you want to customize a Model-driven UI module in general, refer to How to Extend User Interfaces in an Extension
App in the Opcenter Execution Foundation Development and Configuration Guide.
The following workflow and instructions refer to the customization of standard UI Modules and the
extension of Custom Actions, specific to Opcenter EX DS, available in Model Driven UI Modules.
Bear in mind that for Custom Actions you can only extend:
Item Collection Viewers
Property Grids
OData Queries
Backend Calls.
The examples provided in the following sections are based on the extension of the AppU4DM App, but are
valid for any other App to want to extend in your solution.

Workflow
In order to create one or more custom Angular Providers, perform the following steps:
1. Identify the Provider you need to customize.
2. Write the custom code of the Provider in one or more Javascript files.
3. Name the Provider object_custom as explained above in the Naming Convention paragraph.
4. Reference the code in the Angular module 'Siemens.SimaticIT.U4DM.AppU4DM.services.customServices'
which is already defined and included in the Opcenter EX DS application.
5. Repeat steps 1-4 for each Angular Provider.
6. Create a custom UI Module and add it to the UI Application where you want to apply your customizations.

If the purpose of the UI Module is only to include the customizations, it can be set as hidden in the
containing UI Application.

Examples
Item Collection Viewers
Property Grids
Command Bars
Menu Buttons
Tab Controls
oData queries and Backend calls
Icons
Default UI configuration
UI Module Initialization

3.1 Identifying the Customizable Providers
While customizing the User Interface, you need to identify which Angular Providers (UI Modules, UI Components or
Services) are called when the page is displayed, and to do this you can examine the console log available in the
Developer Tools of the web browser.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

11


## Pagina 12

How to Customize the User Interface
Customizing the Item Collection Viewers

Procedure
1. In one of the supported Web Browsers, click F12 to enter Developer Tools mode.
2. In the Developer Tools, click the Console tab.
3. Access the Opcenter EX DS page you want to customize. In the Developer Tools Console, the Opcenter EX DS log
is displayed.
4. Make sure that the displayed items are filtered according to at least Info level.
5. Browse the log and take note of the rows starting with [UADM][CUSTOMIZATOR].

Log Structure
Each row has the following structure:
[UADM] [CUSTOMIZATOR] Searching for providerName_custom : FOUND/NOT FOUND
Row Section

Description

providerName_custom

Name of the custom Angular Provider expected by the page

FOUND/NOT FOUND

FOUND: providerName_custom is present and it has been loaded after the
standard one;
NOT FOUND: providerName_custom is not present, therefore only the standard
providerName has been loaded.

3.2 Customizing the Item Collection Viewers
This example of User Interface customization allows you to add or remove fields from the Item Collection Viewers of
the application.

Procedure
1. Create a .js file into a custom folder of your custom App.
2. Create a service called [controller_name]_custom into
the Siemens.SimaticIT.U4DM.AppU4DM.services.customServices module.
3. Create a function called icvConfig inside the service.
var controllerName = 'yourControllerName';
function configureWOIcv() {
var options = u4dmSvc.icv.configureIcvByEntity("WorkOrder", 'm', getAllWOs,
selectionChanged, 'workorder-status-list');
//insert here custom page management of standard options, if needed
vm.icvConfig = u4dmSvc.customizator.customizeICV(controllerName, options);
}

12

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 13

How to Customize the User Interface
Customizing the Property Grids

3.2.1 Item Collector Viewer Service
While customizing the Item Collector Viewers, you can use the Item Collector Viewer Service to set a standard ICV
configuration for each entity.

ICV Service API Functions
API Function

Description

Example

addFieldInGrid

Adds a field object in the grid mode at the last
position or in the given position.

options.addFieldInGrid(newfields
.RecycleCount,6);
options.addFieldInGrid(newfields
.MaxRecycleCount,7);
options.addFieldInGrid(newfields
.MinQuantity,8);

addFieldInTileP
ropertyList

Adds a field object in the tile property grid at
the last position or in the given position.

options.addFieldInTilePropertyLi
st(newfields.qty);
options.addFieldInTilePropertyLi
st(newfields.status);
options.addFieldInTilePropertyLi
st(newfields.RecycleCount);

removeFieldFro
mGrid

Removes a field from the grid and returns the
field id.

options.removeFieldFromGrid('IsR
eserved');
options.removeFieldFromGrid('Ser
ialNumberCode');

removeFieldFro
mTilePropertie
s

Removes a field from the tile properties and
returns the field id.

options.removeFieldInTilePropert
yList(newfields.qty);
options.removeFieldInTilePropert
yList(newfields.status);
options.removeFieldInTilePropert
yList(newfields.RecycleCount);

3.3 Customizing the Property Grids
This example of User Interface customization allows you to customize the behavior of Property Grids, which is
essential for viewing and modifying custom field values.

Procedure
1. Create a .js file into a custom folder of your custom App.
2. Create a service called [Controller Name]_custom into
the Siemens.SimaticIT.U4DM.AppU4DM.services.customServices module.
3. Create a function called propertyGridConfig inside the service to customize the retrieval function. If you have
more than one Property Grid on the page, you need to create corresponding functions with different names.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

13


## Pagina 14

How to Customize the User Interface
Customizing the Property Grids

var mod = angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices')
.service('workOrderStatus_workOrderAdd_Ctrl_custom ', ['u4dm.services',
workOrderStatus_workOrderAdd_Ctrl_custom ]);

function workOrderStatus_workOrderAdd_Ctrl_custom () {
this.configureFromProcessPg = pgConfig;
function pgConfig(propGridMgr, currentEntity) {
//CREATE NEW FIELD WITH PG MANAGER
propGridMgr.createTextProperty({
id: newField,
labelKey: newFieldDisplayText,
value: currentEntity[newField]
});
//REDEFINE THE GET VALUE FUNCTION
propGridMgr.getValues = function (item, standardGetValues) {
//REUSE THE STANDARD FUNCTION
standardGetValues(item);
//ADD THE NEW FIELD
item[newField] = propGridMgr[newField].value;
};
return propGridMgr;
}
}

3.3.1 Property Grid Service
While customizing the Property Grids, you can use the Property Grid Service to provide an interface to configure the
Property Grid widget. The Property Grid Service acts as a constructor function for the Property Grid.

Property Grid Methods and Examples
Method

Example

createTextProperty(con
fig)

pgFields.lorem = propertyGrid.createTextProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: "ipsum",
read_only: false,
required: true,
invisible: false,
checkSpecialChars: true,
onChange: function(oldVal, newVal, form){...},
customValidation: function(val, model){...}
});

14

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 15

How to Customize the User Interface
Customizing the Property Grids

Method

Example

createTextPropertyWith
Button(config)

pgFields.lorem = propertyGrid.createTextPropertywithButton({
..., //widgetspecific attributes
onClick: callbackFn,
buttonDisabled: vm.currentItem.GenerateDisabled,
buttonIcon: icon.plus,
buttonText: "Generate",
showButtonInViewMode: true //if button has to be displayed in
view mode
});

createTextAreaProperty
(config)

pgFields.lorem = propertyGrid.createTextAreaProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: "ipsum",
read_only: true,
});

createTextAreaProperty
WithButton(config)

pgFields.lorem = propertyGrid.createTextAreaPropertywithButton({
..., //widgetspecific attributes
onClick: callbackFn,
buttonDisabled: vm.currentItem.GenerateDisabled,
buttonIcon: icon.plus,
buttonText: "Generate",
showButtonInViewMode: true //if button has to be displayed in
view mode
});

createNumericProperty
(config)

pgFields.lorem = propertyGrid.createNumericProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: "ipsum",
read_only: true,
onChange: function(oldVal, newVal, form){...},
required: true,
invisible: false,
minVal: vm.currentItem.QuantityMin,
maxVal: vm.currentItem.QuantityMax,
validationCallback: function(val, model) {...}
});

createNumericProperty
WithButton(config)

pgFields.lorem = propertyGrid.createNumericPropertywithButton({
..., //widgetspecific attributes
onClick: callbackFn,
buttonDisabled: vm.currentItem.GenerateDisabled,
buttonIcon: icon.plus,
buttonText: "Generate",
showButtonInViewMode: true //if button has to be displayed in
view mode
});

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

15


## Pagina 16

How to Customize the User Interface
Customizing the Property Grids

Method

Example

createEntityPickerProp
erty(config)

pfFields.lorem = propertyGrid.createEntityPickerProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: vm.ipsum,
required: vm.lorem,
dataSource: vm.productionTypeList // Array or a Promise,
displayProperty: 'NId',
onChange: function(oldVal, newVal){...} //For selection
change,
pickerOptions:
u4dmSvc.icv.configureIcvByEntity("MaterialDefinition", null, null
, null, controllerName, '')
});
/*datasource configured as promise*/
pgManager.createEntityPickerProperty({
id: 'powderMaterial',
value: vm.currentItem.selectedPowder,
labelKey: 'sit.u4dm.genealogy.labels.powder-batch',
dataSource: getPowderMaterials(), // returns a promise
displayProperty: 'NId',
pickerOptions: pickerOptions,
onChange: materialChange,
resolveEntityPickerValue: function (result) {
return _(result.value).find(function (matItem)
{ return matItem.Id == selectedMaterialId }); //custom logic to
return selected object
}
});
function getPowderMaterials() {
if (vm.materials) return materials;
else return u4dmSvc.api.am.powder.getAll().then(function (resul
t) {
vm.materials = result.value;
//in case pgGrid is
refreshed multiple times then we can cache data to avoid multiple
hits to the server
return result;
}, u4dmSvc.ui.overlay.showBackendError);
}
/*datasource configured as object for lazy loading*/
pfFields.lorem = propertyGrid.createEntityPickerProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: vm.ipsum,
required: vm.lorem,
dataSource:{
getAll: function (options, hasFilter),
searchField: 'Name' //required in case if the
displayProperty is a custom property
} // Array or a Promise,
displayProperty: 'NId',

16

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 17

How to Customize the User Interface
Customizing the Property Grids

Method

Example
onChange: function(oldVal, newVal){...} //For selection
change,
pickerOptions:
u4dmSvc.icv.configureIcvByEntity("MaterialDefinition", null, null
, null, controllerName, '')
});

createEntityPickerProp
ertyWithButton(config)

pgFields.lorem =
propertyGrid.createEntityPickerPropertywithButton({
..., //widgetspecific attributes
onClick: callbackFn,
buttonDisabled: vm.currentItem.GenerateDisabled,
buttonIcon: icon.plus,
buttonText: "Generate",
showButtonInViewMode: true //if button has to be displayed in
view mode
});

createDateTimePropert
y(config)

pgFields.lorem = propertyGrid.createDateTimeProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
dateValue: vm.currentItem.ED,
timeValue: vm.currentItem.ET,
validationCallback: endDateValidationFn
});

createCheckboxPropert
y(config)

pgFields.lorem = propertyGrid.createCheckboxProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
read_only: true,
invisble: false,
options: vm.options // [{labelKey: 'sit.u4dm.ipsum', checked:
false}, ...]
});

createComboBoxPrope
rty(config)

pfFields.lorem = propertyGrid.createComboBoxProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: vm.ipsum,
required: vm.lorem,
dataSource: vm.optionsList,
displayProperty: 'NId',
valueProperty: 'Id'
onChange: onChangeCallback //For selection change
});

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

17


## Pagina 18

How to Customize the User Interface
Customizing the Property Grids

Method

Example

createNumericProperty
WithReadOnlyText(conf
ig)

pgFields.lorem =
propertyGrid.createNumericPropertyWithReadOnlyText({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: "ipsum",
read_only: true,
onChange: function(oldVal, newVal, form){...},
required: true,
invisible: false,
minVal: vm.currentItem.QuantityMin,
maxVal: vm.currentItem.QuantityMax,
validationCallback: function(val, model) {...},
textValue: "someText" //To set the value of the read-only text
field.
});

createDurationTimePro
perty(config)

pgFields.lorem = propertyGrid.createDurationTimeProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: "ipsum",
read_only: true,
onChange: function(oldVal, newVal, form){...},
required: true,
invisible: false,
format: 'd:h:m:s', // default is 'h:m:s' and it supports any
momentjs duration supported format (https://momentjs.com/docs/#/
durations/)
value: vm.currentItem.someValue, // value can be ticks,
moment.duration object or a plain JS object with structure
{seconds: s, minutes: m, hours: h},
displayValue: "someText"//To set the value in readOnly mode.
})

18

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 19

How to Customize the User Interface
Customizing the Command Bars

Method

Example

createNumericProperty
WithEntityPicker(config
)

pfFields.lorem = propertyGrid.createEntityPickerProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: vm.ipsum // if number than it will be assigned to
numeric field else if array then 0-index value will be assigned
to Numeric Field and 1-index value will be assigned to
EntityPicker
required: vm.lorem,
read_only: true,
dataSource: vm.productionTypeList,
displayProperty: 'NId',
disablePicker: true, //If only entity picker needs to be
disabled
pickerValue: vm.ipsum,
onChange: function(oldVal, newVal){...} //For selection
change,
pickerOptions:
u4dmSvc.icv.configureIcvByEntity("MaterialDefinition", 'm', null
, null, controllerName, '')
});

createPasswordPropert
y(config)

pgFields.lorem = propertyGrid.createPasswordProperty({
id: 'lorem',
labelKey: 'sit.u4dm.lorem',
value: "ipsum",
read_only: true
});

createPasswordPropert
yWithButton(config)

pgFields.lorem = propertyGrid.createPasswordPropertywithButton({
..., //widgetspecific attributes
onClick: callbackFn,
buttonDisabled: vm.currentItem.GenerateDisabled,
buttonIcon: icon.plus,
buttonText: "Generate",
showButtonInViewMode: true //if button has to be displayed in
view mode
});

3.4 Customizing the Command Bars
This example of User Interface customization allows you to change the behavior of every Command Bar in the
application.

Procedure

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

19


## Pagina 20

How to Customize the User Interface
Customizing the Command Bars

1. Create a .js file into a custom folder of your custom App.
2. Create a service called [controller Name]_custom into
the Siemens.SimaticIT.U4DM.AppU4DM.services.customServices module.
3. Create a function called commandBarConfig inside the service.
var mod =
angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices')
.service('workOrderStatus_workOrderList_Ctrl_custom', ['$state',
workOrderStatus_workOrderList_Ctrl_custom]);
function workOrderStatus_workOrderList_Ctrl_custom($state) {
var button = {
type: 'Command',
name: 'name',
image: 'fa-sitemap',
label: 'Custom Button',
onClickCallback: function () {
$state.go('home.Siemens_SimaticIT_U4DM_AppU4DM_workOrder.customadd')
},
visibility: false
};
//CUSTOMIZE ICV
this.icvConfig = function (standardConfig) {
var newColumn = {
field: newField,
displayNameKey: newFieldDisplayText,
type: 'string'
};
standardConfig.gridConfig.columnDefs.unshift(newColumn);
var newColumn2 = {
field: newDTField,
displayNameKey: newDTFieldDisplayText,
type: 'string'
};
standardConfig.gridConfig.columnDefs.unshift(newColumn2);
var newColumn3 = {
field: "ProcessNId",
displayNameKey: "Process NId",
type: 'string'
};
standardConfig.gridConfig.columnDefs.unshift(newColumn3);
standardConfig.mediumTileTemplate = mediumTileTemplate;
var oldsc = standardConfig.onSelectionChangeCallback;
standardConfig.onSelectionChangeCallback = function (selected) {
oldsc(selected);
if (selected && selected.length > 0) {
button.visibility = true;
} else {
button.visibility = false;
}
}
return standardConfig;

20

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 21

How to Customize the User Interface
Customizing the Menu Buttons

};
this.commandBarConfig = function (standardConfig) {
standardConfig.bar.push(button);
return standardConfig;
}
}

3.5 Customizing the Menu Buttons
This example of User Interface customization allows you to modify the behavior of the Menu Buttons of the
application.

Procedure
1. Create a .js file into a custom folder of your custom App.
2. Create a service called [Controller Name]_custom into
the Siemens.SimaticIT.U4DM.AppU4DM.services.customServices module.
3. Create a function called menuButtonConfig inside the service.
var mod = angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices')
.service('workOrderStatus_workOrderList_Ctrl_custom',
[workOrderStatus_workOrderList_Ctrl_custom]);
function workOrderStatus_workOrderList_Ctrl_custom() {
//CUSTOMIZE ICV
this.menuButtonConfig = function (standardConfig) {
standardConfig.menuItems.push({
label: "Test",
name:
"Siemens.SimaticIT.U4DM.MsExt.FB_OP_EXT.OEModel.Commands.CreateWorkOrderFromProcess",
onClickCallback: function () {}
});
return standardConfig;
};
}

3.6 Customizing the Tab Controls
This example of User Interface customization allows you to add or remove tabs in the Tab Controls of the
application.
Task Details UI Component Customization
For information on how to customize the Task Details UI Component tab, see Task Details UI Component
(Deprecated).

Procedure
1. Create a .js file inside a custom folder of your custom App.
2. Create a service called [Controller Name]_custom inside
the Siemens.SimaticIT.U4DM.AppU4DM.services.customServices module.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

21


## Pagina 22

How to Customize the User Interface
Customizing oData Queries and Backend Commands

3. Create a function called tabsConfig inside the service.

Example for Work Orders Page
var mod =
angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices')
.service('workOrderStatus_workOrderStatusSelect_Ctrl_custom', ['u4dm.services',
workOrderStatus_workOrderStatusSelect_Ctrl_custom]);
function workOrderStatus_workOrderStatusSelect_Ctrl_custom() {
this.tabsConfig = function (tabs) {
tabs.push({
heading: 'CUSTOMTAB',
route:
'home.Siemens_SimaticIT_U4DM_AppU4DM_workOrder.select.customtab',
active: false
});
return tabs;
};
}

3.7 Customizing oData Queries and Backend Commands
This example of User Interface customization shows how you can override oData queries and Backend Commands
called by the User Interface through the API services. This allows you to retrieve custom data.
Every module must have a dedicated service containing the logic of the module, as well as all the calls to the
backend.

Procedure via Angular Factory
1. In a custom folder of your custom App, create a .js file.
2. In module Siemens.SimaticIT.U4DM.AppU4DM.services.customServices, create a factory called [App
Name].[Service Name]_custom.
3. In section Config of the module, add the App name and service name.
4. Create a javascript function that will return an object containing your custom function.
5. In the service, create a function having the same name as the function that you want to customize.
6. Do either of the following:
Create a function that will overwrite the behavior of the standard function.
Create a function that will call the standard function through service
customizator.standardMethodCache, using the following syntax:
customizator.standardMethodCache['[Service Name]'].[Name of function]([list of parameter]);

Example for Angular Factory procedure

//1) Create a javascript file in a custom folder of your custom App
var mod =
angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices');

22

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 23

How to Customize the User Interface
Customizing oData Queries and Backend Commands

//2) Create a factory called [App Name].[Service Name]_custom in module
Siemens.SimaticIT.U4DM.AppU4DM.services.customServices.
mod.factory('AppU4DM.lazyConsumeMaterial.service_custom', ['u4dm.services',
'uadm.services.customizator',
consumeMaterialService
]);
mod.config([
'CONFIG',
function (CONFIG) {
//3) add the App name and service name in section Config of the module
CONFIG.addCustomizedFunction("AppU4DM",
"lazyConsumeMaterial.service_custom");
}]);

function consumeMaterialService(u4dmSvc, customizator) {
//4) Create a javascript function that will return an object containing your
custom function
return {
getToBeConsumedMaterialFromView
:
getToBeConsumedMaterialFromView,
getMTUsAndContainersWithConsumptionStatus :
getMTUsAndContainersWithConsumptionStatus
};
// example of overwriting the standard function
function getToBeConsumedMaterialFromView(woop, wos){
return u4dmSvc.api.workOrder.getAll("$select=Id eq"+woop.Id);
}
// example of calling the standard function
function getMTUsAndContainersWithConsumptionStatus(woop, wos, eqNId, top,
skip, mtunid) {
var result =
customizator.standardMethodCache['lazyConsumeMaterial.service'].getMTUsAndContainersW
ithConsumptionStatus(woop, wos, eqNId, top, skip, mtunid);
return result;
}
}

Procedure via Angular Service
1. In a custom folder of your custom App, create a .js file.
2. In module Siemens.SimaticIT.U4DM.AppU4DM.services.customServices, create a service called [App
Name].[Service Name]_custom.
3. Operating inside the service, do either of the following:
Create a function called getAll to customize the data-retrieval function.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

23


## Pagina 24

How to Customize the User Interface
Customizing oData Queries and Backend Commands

Create a function called getAll_inject to customize the data-retrieval function using the standard
function provided by Opcenter EX DS (passed as a parameter).
4. Operating inside the service, do either of the following:
Create a function called [Command Name] to customize the function as desired.
Create a function called [Command Name]_inject to customize the function using the standard
Opcenter EX DS function (passed as a parameter).

Example for Angular Service procedure

var mod = angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices')
.service('AppU4DM.workOrderStatus_Svc_custom ', ['u4dm.services', '$q',
'$timeout', workOrderStatus_Svc_custom ]);
mod.config([
'CONFIG',
function (CONFIG) {
CONFIG.addCustomizedFunction("AppU4DM", "workOrderStatus_Svc_custom ");
}]);
function workOrderStatus_Svc_custom (u4dmSvc, $q, $timeout) {
var workOrderOptions =
'$expand=ProducedMaterialItems($expand=MaterialItem),FinalMaterial($select=NId,
Name,Revision),ProductionType($select=NId),WorkOrderOperations';
//OVERRIDE getAll function of the original workOrderStatusService service
this.getAll = function (options) {
var query = u4dmSvc.api.tools.chainQuery(options, workOrderOptions);
return u4dmSvc.api.workOrder.getAll(query).then(function (result) {
//ADD FAKE VALUE
result.value.forEach(function (wo) {
wo[newField] = wo.NId + '_custom';
});
return result;
});
};
//OVERRIDE getAll function of the original workOrderStatus_Svc service
injection mode example
this.getAll_inject = function (standard) {
function myGetAll(options) {
return standard(options).then(function (result) {
//ADD FAKE VALUE
result.value.forEach(function (wo) {
wo[newField] = wo.NId + '_custom';
});
return result;
});
}
return myGetAll;
};

24

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 25

How to Customize the User Interface
Customizing the Icons

this.createFromProcess = function (item) {
var payload = createPayload(item);
var deferred = $q.defer();
//FAKE ASYNC CALL
$timeout(function () {
deferred.resolve(true);
}, 100);
return deferred.promise;
};
function createPayload(data) {
var payload = {};
///ADD CUSTOM DATA MANAGEMENT HERE
payload[newField] = 'newValue';
return payload;
}
this.updateWorkOrder = function (item) {
var payload = createPayload(item);
var deferred = $q.defer();
//FAKE ASYNC CALL
$timeout(function () {
deferred.resolve(true);
}, 100);
return deferred.promise;
};
}

3.8 Customizing the Icons
This example of User Interface customization allows you to change the icon of every page in the whole application.

Procedure
1. Create a .js file into a custom folder of your custom App.
2. Create a service called u4dm.services.icons_custom into
the Siemens.SimaticIT.U4DM.AppU4DM.services.customServices module.
3. Create a function called customizeIcons inside the service.
(function () {
'use strict';
var mod =
angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices');
mod.service('u4dm.services.icons_custom', [
myIconsService
]);
function myIconsService(customizator) {
this.customizeIcons = function (icons) {
//modify the collection

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

25


## Pagina 26

How to Customize the User Interface
Customizing the Default UI Configuration

return icons;
}
}
})();

3.9 Customizing the Default UI Configuration
This example of User Interface customization allows you to modify the default configuration of the User Interface.
For example, it allows you to change how the grids are displayed, their pagination options, which filters are active,
and so on.

Procedure
1. Create a .js file into a custom folder of your custom App.
2. Create a service called u4dm.ui.configuration_custom into
the Siemens.SimaticIT.U4DM.AppU4DM.services.customServices module.
3. Create a function called customizeUIDefaults inside the service.
(function () {
'use strict';
var mod =
angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices');
mod.service('u4dm.ui.configuration_custom', [
u4dmUIConfiguration
]);
function u4dmUIConfiguration(customizator) {
this.customizeUIDefaults = function (uiConfiguration) {
//change the UI Defaults
uiConfiguration.icv.defaultOptions.viewMode = 'g';
return uiConfiguration;
}
}
})();

3.10 Customizing the UI Module Initialization
If your custom Module is using services related to an App or an Ext App, it is necessary to indicate this dependency
as described below.

Procedure
1. Edit the main module.js file, generated by Project Studio when you create a new App or Ext App.
2. Indicate the required dependency app ( or module ) as shown in the following example:
(function () {
'use strict';
angular.module(MyCustomApp', ['DependentModule']);

26

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 27

How to Customize the User Interface
Customizing the UI Module Initialization

})();

3. Save the module.js file.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

27


## Pagina 28

Opcenter Execution Discrete UI Modules
Customizing the UI Module Initialization

4 Opcenter Execution Discrete UI Modules
User Interface Modules used by Opcenter Execution Discrete are of three types:
Standard UI Modules, created with Javascript code;
Mashup UI Modules, created with Opcenter Execution Foundation Mashup Editor;
Model-driven UI Modules, created without writing code, starting from the implemented data model and
business logic.
The Standard UI Modules and Mashup UI Modules listed below are all related to the AppU4DM App.
All other Opcenter Execution Discrete Apps and Extension Apps only contain Model-driven UI Modules.
To retrieve the list of all Model-driven UI modules by App/Extension App, log in to Opcenter EX FN
Solution Studio as explained in section Model-driven UI Modules.

Standard UI Modules
CLM Resource Management
Configuration Keys
DCD Engineering
Defect Type Management
Document Management
Genealogy
Labor Tracking Management
Non-Conformance Lifecycle
Non-Conformance Notification Management
Non-Conformance Supervisor Management
Operation/Step Category
Order Work In Progress
PowderGenealogy
Process Catalog Management (Deprecated)
Team Management
Transport Operation Landing UI Module
Users and Skills
Work Order As Built
Work Order As Planned BOP
Work Order Status (Deprecated)

Mashup UI Modules and related Screens
High Automation
High Automation Details Screen
High Automation Operator Landing Screen
Operator Landing
Operator Detail Screen
Operator Detail Steps Screen
Operator Landing Task List Screen
Operator Landing Home Screen

Model-driven UI Modules
To retrieve the list of Model-driven UI Modules:
1. From Windows Apps, in the Siemens Automation category, click the Opcenter EX FN Solution Studio link.
2. In the web page, log in to the Opcenter EX FN Solution Studio in either of the following ways:

28

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 29

Opcenter Execution Discrete UI Modules
CLM Resource Management UI Module

Insert the credentials of the user with administrator rights and click Sign In.
Click Use your current Windows session to Log In link to access the application with the current user
credentials.
3. In the home page, click the link to the Opcenter EX DS solution.
4. In the User Interface > UI Applications page, select the Opcenter EX DS solution and click
Open.
5. The Model-driven UI Modules are those indicated with ModelDriven in the UI Module Type column.

4.1 CLM Resource Management UI Module
This UI module manages features related to the CLM Resources.

Name
Siemens.SimaticIT.U4DM.AppU4DM.CLMResourceMgt

Screens and Angular States
Screen

Angular State

CLM Resource Management

home.Siemens_SimaticIT_U4DM_AppU4DM_CLMResourceMgt

Angular Controllers related to the Module
Name

File Name

clmResourceMgt_list_Ctrl

clm-resource-mgt-list-ctrl.js

Services related to the Module
Name

File Name

clmResourceMgt_Svc

clm-resource-mgt-srv.js

4.2 Configuration Keys UI Module
This UI module manages the Configuration Keys used to customize the application behavior.

Name
Siemens.SimaticIT.U4DM.AppU4DM.configKeys

Screens and Angular States
Screen

Angular State

Configuration Keys

home.Siemens_SimaticIT_U4DM_AppU4DM_configKeys

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

29


## Pagina 30

Opcenter Execution Discrete UI Modules
DCD Engineering UI Module

Angular Controllers related to the Module
Name

File Name

configKeys_list_Ctrl

configKeys-list-ctrl.js

commandsCtrl

commands.js

Services related to the Module
Name

File Name

configKeys_Svc

configKeys-srv.js

4.3 DCD Engineering UI Module
This UI module manages features related to Data Collections.

Name
Siemens.SimaticIT.U4DM.AppU4DM.workInstruction

Screens and Angular States
Screen

Angular State

DCD Engineering

home.Siemens_SimaticIT_U4DM_AppU4DM_altengineering

PMI2ALT

home.Siemens_SimaticIT_U4DM_AppU4DM_workInstruction_pmi2alt

Angular Controllers related to the Module
Name

File Name

pmi2altCtrl

pmi2alt-ctrl.js

workInstruction_altEng_Ctrl

workInstruction-alteng-ctrl.js

workInstruction_altRuntime_Ctrl

workInstruction-altruntime-ctrl.js

workInstruction_list_Ctrl

workInstruction-list-ctrl.js

Services related to the Module

30

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 31

Opcenter Execution Discrete UI Modules
Defect Type Management UI Module

Name

File Name

workInstruction_Svc

workInstruction-srv.js

4.4 Defect Type Management UI Module
This UI module manages features related to the Defect Types.

Name
Siemens.SimaticIT.U4DM.AppU4DM.defectTypeMgt

Screens and Angular States
Screen

Angular State

Defect Type Management

home.Siemens_SimaticIT_U4DM_AppU4DM_defectMgt_Type_Defects

Angular Controllers related to the Module
Name

File Name

defectTypeMgt_add_Ctrl

defectTypeMgt-add-ctrl.js

defectTypeMgt_addMachine_Ctrl

defectTypeMgt-add-machine-ctrl.js

defectTypeMgt_addMaterial_Ctrl

defectTypeMgt-add-materials-ctrl.js

defectTypeMgt_addGroup_Ctrl

defectTypeMgt-group-list-ctrl.js

defectTypeMgt_groups_Ctrl

defectTypeMgt-groups-ctrl

defectTypeMgt_groupsList_Ctrl

defectTypeMgt-groups-list-ctrl.js

defectTypeMgt_list_Ctrl

defectTypeMgt-list-ctrl.js

defectTypeMgt_list_edit_Ctrl

defectTypeMgt-list-edit-ctrl.js

defectTypeMgt_select_Ctrl

defectTypeMgt-select-ctrl.js

defectTypeMgt_selectDetails_Ctrl

defectTypeMgt-select-details-ctrl.js

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

31


## Pagina 32

Opcenter Execution Discrete UI Modules
Document Management UI Module

Name

File Name

defectTypeMgt_selectMachines_Ctrl

defectTypeMgt-select-machine-ctrl.js

defectTypeMgt_selectMaterials_Ctrl

defectTypeMgt-select-materials.js

Services related to the Module
Name

File Name

defectTypeMgt_Svc

defectTypeMgt-srv.js

4.5 Document Management UI Module
This UI module manages features related to Documents.

Name
Siemens.SimaticIT.U4DM.AppU4DM.document

Screens and Angular States
Screen

Angular State

Document Management

home.Siemens_SimaticIT_U4DM_AppU4DM_document

Angular Controllers related to the Module
Name

File Name

document_download_Ctrl

document-download-ctrl.js

document_list_Ctrl

document-list-ctrl.js

Services related to the Module
Name

File Name

documentsvc

document-srv.js

4.6 Genealogy UI Module
This UI module manages features related to Item Genealogy.

32

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 33

Opcenter Execution Discrete UI Modules
High Automation Mashup UI Module

Name
Siemens.SimaticIT.U4DM.AppU4DM.Genealogy

Screens and Angular States
Screen

Angular State

Genealogy

home.Siemens_SimaticIT_U4DM_AppU4DM_genealogy

Angular Controllers related to the Module
Name

File Name

genealogy_Ctrl

genealogy-ctrl.js

genealogy_materialNote_Ctrl

genealogy-disassemble-material-note-ctrl.js

genealogy_powderGenealogy_Ctrl

powderGenealogy-ctrl.js (Deprecated, use the PowderGenealogy UI
Module instead)

Services related to the Module
Name

File Name

genealogy_Svc

genealogy-svc.js

genealogy_Tree_Svc

genealogy-tree-svc.js

4.7 High Automation Mashup UI Module
This UI Module manages the features related to the High Automation Operator Landing Page.

Name
Siemens.SimaticIT.U4DM.AppU4DM.highAutomationOpLanding

Screens and Angular States
Screen

Angular State

High Automation Operator Landing Screen

home.UADM_highAutomationOpLanding_operatorLanding

High Automation Details Screen

home.UADM_highAutomationOpLanding_operatorDetails

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

33


## Pagina 34

Opcenter Execution Discrete UI Modules
High Automation Mashup UI Module

Screen

Angular State

High Automation Operator Task List Screen

home.U4DM_highAutomationOpLanding_operatorDetailsTask

Angular Controllers related to the Module
Name

File Name

UADM.highAutomationOpLanding

mashup-module.js

Services related to the Module
Name

File Name

u4dm.services.runtime

u4dm-runtime-service.js

u4dm.services.runtime.wooperations

uadm-runtime-wo-operations.js

u4dm.services.runtime.utils

uadm-runtime-utils-service.js

4.7.1 High Automation Details Screen
This Screen belonging to the High Automation Mashup UI Module allows Operators to monitor production and track
material consumption.

Name
Siemens.SimaticIT.U4DM.AppU4DM.highAutomation.operatorDetails

Angular Controllers related to the Screen
Name

File Name

UADM.highAutomationOpLanding

mashup-module.js

UI Components related to the Screen
High Automation Header Bar
Material Tracking
Document Preview
Customizable Button Bar

34

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 35

Opcenter Execution Discrete UI Modules
Labor Tracking Management UI Module

4.7.2 High Automation Operator Landing Screen
This Screen belonging to the High Automation Mashup UI Module allows Operator to browse and select a piece of
Equipment where to monitor production.

Name
Siemens.SimaticIT.U4DM.AppU4DM.highAutomation.operatorLanding

Angular Controllers related to the Screen
Name

File Name

UADM.highAutomationOpLanding.operatorLanding

mashup-module.js

UI Components related to the Screen
High Automation Equipment List
Customizable Button Bar

4.7.3 High Automation Operator Task List Screen
This Screen belonging to the the High Automation Mashup UI Module allows Operators to monitor production and
perform the activities required by the available runtime tasks.

Name
operatorDetailsTask

Angular Controllers related to the Screen
Name

File Name

UADM.highAutomationOpLanding

mashup-module.js

UI Components related to the Screen
High Automation Header Bar
Task Container
Customizable Button Bar

4.8 Labor Tracking Management UI Module
This UI module implements features related to manual management of Labor Tracking.

Name
Siemens.SimaticIT.U4DM.AppU4DM.laborTrackingMgt

Screens and Angular States

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

35


## Pagina 36

Opcenter Execution Discrete UI Modules
Non-Conformance Lifecycle UI Module

Screen

Angular State

Production Coordinator Dashboard

home.Siemens_SimaticIT_U4DM_AppU4DM_pc_dashboard

Production Coordinator Time Update

home.Siemens_SimaticIT_U4DM_AppU4DM_pc_time_update

Angular Controllers related to the Module
Name

File Name

laborTrackingMgt_pcDashboardChangeWorkplace_Ctrl

pc-dashboard-changewp-ctrl.js

laborTrackingMgt_pcDashboardEditView_Ctrl

pc-dashboard-edit-ctrl.js

laborTrackingMgt_pcDashboardListView_Ctrl

pc-dashboard-list-ctrl.js

laborTrackingMgt_pcDashboardSelectView_Ctrl

pc-dashboard-select-ctrl.js

laborTrackingMgt_pcTimeUpdateListView_Ctrl

pc-time-update-list-ctrl.js

laborTrackingMgt_pcTimeUpdateSelectView_Ctrl

pc-time-update-select-ctrl.js

laborTrackingMgt_pcTimeUpdateSelectHistoryAdd_Ctrl

pc-time-update-select-history-add-ctrl.js

laborTrackingMgt_pcTimeUpdateSelectHistoryEditView_Ctrl

pc-time-update-select-history-edit-ctrl.js

laborTrackingMgt_pcTimeUpdateHistory_Ctrl

pc-time-update-select-history-list-ctrl.js

laborTrackingMgt_pcTimeUpdadeSelectOperationEdit_Ctrl

pc-time-update-select-operations-edit-ctrl.js

laborTrackingMgt_pcTimeUpdateSelectOperations_Ctrl

pc-time-update-select-operations-list-ctrl

Services related to the Module
Name

File Name

laborTrackingMgt_Svc

labor-tracking-svc.js

4.9 Non-Conformance Lifecycle UI Module
This UI module manages features related to the lifecycles of Non-Conformances.

36

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 37

Opcenter Execution Discrete UI Modules
Non-Conformance Lifecycle UI Module

Name
Siemens.SimaticIT.U4DM.AppU4DM.NCLifecycleMgt

Screens and Angular States
Screen

Angular State

Non Conformance Lifecycle

home.Siemens_SimaticIT_U4DM_AppU4DM_NCLifeCycleMgt

Angular Controllers related to the Module
Name

File Name

NCLlifecycle_AddEdit_Ctrl

nc-lifecycle-mgt-lifecycle-add.js

NCLlifecycle_list_Ctrl

nc-lifecycle-mgt-list-ctrl.js

NCLlifecycle_TransitionDtails_Ctrl

nc-lifecycle-mgt-select-details.js

NCLlifecycle_States_Edit_Ctrl

nc-lifecycle-mgt-select-states-edit.js

NCLlifecycle_States_Ctrl

nc-lifecycle-mgt-select-states.js

NCLlifecycle_TransitionAddEdit_Ctrl

nc-lifecycle-mgt-select-transition-add.js

NCLlifecycle_Transition_Graph

nc-lifecycle-mgt-select-transition-flow.js

NCLlifecycle_AssignNotificationOnTransition_Ctrl

nc-lifecycle-mgt-select-transition-notification

NCLlifecycle_AssignRoleToTransition_Ctrl

nc-lifecycle-mgt-select-transition-roles.js

NCLlifecycle_TransitionList_Ctrl

nc-lifecycle-mgt-select-transition.js

NCLlifecycle_SelectLifecycle_Ctrl

nc-lifecycle-mgt-select.js

NCLlifecycle_StatusAdd_Ctrl

nc-lifecycle-mgt-status-add.js

NCLlifecycle_SelectState_Ctrl

nc-lifecycle-mgt-status.js

Services related to the Module

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

37


## Pagina 38

Opcenter Execution Discrete UI Modules
Non-Conformance Notification Management UI Module

Name

File Name

ncLifecycle_Svc

nc-lifecycle-mgt-srv.js

4.10 Non-Conformance Notification Management UI Module
This UI module manages features related to the notification of the various Non-Conformance messages.

Name
Siemens.SimaticIT.U4DM.AppU4DM.NCNotificationMgt

Screens and Angular States
Screen

Angular State

Non Conformance Notification Management

home.Siemens_SimaticIT_U4DM_AppU4DM_NCNotificationMgt

Angular Controllers related to the Module
Name

File Name

NCNotificationMgt_ncNotificationMgtAccept_Ctrl

nc-notification-mgt-accept-ctrl.js

NCNotificationMgt_ncNotificationMgt_Ctrl

nc-notification-mgt-list-ctrl.js

NCNotification_ncNotificationMgtReject_Ctrl

nc-notification-mgt-reject-ctrl.js

NCNotificationMgt_ncNotificationMgtselect_Ctrl

nc-notification-mgt-select-ctrl.js

Services related to the Module
Name

File Name

ncNotificationMgt_Svc

nc-notification-mgt-srv.js

4.11 Non-Conformance Supervisor Management UI Module
This UI module implements the operations that the Production Coordinator can perform on the various NonConformances.

Name
Siemens.SimaticIT.U4DM.AppU4DM.NCSupervisor

38

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 39

Opcenter Execution Discrete UI Modules
Non-Conformance Supervisor Management UI Module

Screens and Angular States
Screen

Angular State

Non Conformance Supervisor Management

home.Siemens_SimaticIT_U4DM_AppU4DM_NCSupervisor

Non Conformance Change Management

home.Siemens_SimaticIT_U4DM_AppU4DM_NCChange

Angular Controllers related to the Module
Name

File Name

ncSupervisor_ncChangeAccept_Ctrl

nc-change-accept.js

ncSupervisor_ncChangeAdd_Ctrl

nc-change-add.js

ncSupervisor_ncChangeList_Ctrl

nc-change-list-ctrl.js

ncSupervisor_ncChangeReject_Ctrl

nc-change-reject-ctrl.js

ncSupervisor_ncChangeSelect_View

nc-change-select-ctrl.js

ncSuperVisor_ncChangeSelectDetails_Ctrl

nc-change-select-details-ctrl.js

ncSupervisor_addDefect_Ctrl

nc-supervisor-add-defect-ctrl.js

ncSupervisor_changeStatus_Ctrl

nc-supervisor-changestatus-ctrl.js

ncSupervisor_list_Ctrl

nc-supervisor-list-ctrl.js

ncSupervisor_select_Ctrl

nc-supervisor-select-ctrl.js

ncSupervisor_selectDefects_Ctrl

nc-supervisor-select-defects-ctrl.js

ncSupervisor_selectDetails_Ctrl

nc.js-supervisor-select-details-ctrl

ncSupervisor_selectDocuments_Ctrl

nc-supervisor-select-documents-ctrl.js

ncSupervisor_selectHistory_Ctrl

nc-supervisor-select-history-ctrl.js

ncSupervisor_selectMachines_Ctrl

nc-supervisor-select-machines-ctrl.js

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

39


## Pagina 40

Opcenter Execution Discrete UI Modules
Operation/Step Category UI Module

Name

File Name

ncSupervisor_selectMaterialItems_Ctrl

nc-supervisor-select-materials-ctrl.js

ncSupervisor_selectTools_Ctrl

nc-supervisor-select-tools-ctrl.js

Services related to the Module
Name

File Name

ncSupervisor_Svc

nc-supervisor-srv.js

4.12 Operation/Step Category UI Module
This UI module implements features related to Operation/Step Category management.

Name
Siemens.SimaticIT.U4DM.AppU4DM.OperationStepCategory

Screens and Angular States
Screen

Angular State

Operation/Step Categories

home.Siemens_SimaticIT_U4DM_AppU4DM_operationStepCategory

Angular Controllers related to the Module
Name

File Name

operationStepCategory_select_Ctrl

operation-step-category-select-ctrl.js

operationStepCategory_selectDetails_Ctrl

operation-step-category-select-details-ctrl.js

operationStepCategory_selectAssociations_add_Ctrl

operation-step-category-select-associations-add-ctrl.js

operationStepCategory_selectAssociations_Ctrl

operation-step-category-select-associations-ctrl.js

operationStepCategory_selectInterlocking_Ctrl

operation-step-category-select-interlocking-ctrl.js

Services related to the Module

40

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 41

Opcenter Execution Discrete UI Modules
Operator Landing Mashup UI Module

Name

File Name

operationStepCategory_Svc

operation-step-category-srv.js

4.13 Operator Landing Mashup UI Module
This UI Module manages the features related to the Operator Landing Page.

Name
Siemens.SimaticIT.U4DM.AppU4DM.operatorLanding

Screens and Angular States
Screen

Angular State

Operator Landing Home Screen

home.U4DM_operatorLanding_operatorLanding

Operator Detail Screen

home.U4DM_operatorLanding_operatorDetails

Operator Detail Steps Screen

home.U4DM_operatorLanding_operatorDetailSteps

Operator Exec Group Details Screen

home.UADM_operatorLanding_execGroupDetails

Angular Controllers related to the Module
Name

File Name

UADM.operatorLanding

mashup-module.js

Services related to the Module
Name

File Name

u4dm.services.runtime

u4dm-runtime-service.js

u4dm.services.runtime.wooperations

uadm-runtime-wo-operations.js

u4dm.services.runtime.utils

uadm-runtime-utils-service.js

u4dm.services.runtime.wosteps

uadm-runtime-wo-steps.js

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

41


## Pagina 42

Opcenter Execution Discrete UI Modules
Operator Landing Mashup UI Module

Name

File Name

u4dm.services.runtime.dcd

u4dm-dcd-service.js

u4dm.services.runtime.qms

u4dm-runtime-qms.js

u4dm.services.runtime.execution-group-details-integration

u4dm-execution-group-details-integration.js

4.13.1 Operator Detail Screen
This Screen belonging to the Operator Landing Mashup UI Module manages the features related to the details of the
Operator.

Name
operatorDetails

Angular Controllers related to the Screen
Name

File Name

UADM.operatorLanding

mashup-module.js

UI Components related to the Screen
Operation Header Bar
Task Details
Document Preview
Button Bar

4.13.2 Operator Detail Steps Screen
This Screen belonging to the Operator Landing Mashup UI Module manages the features related to the Work Order
Operation steps in the Operator Landing Page.

Name
operatorDetailsStep

Angular Controllers related to the Screen
Name

File Name

UADM.operatorLanding

mashup-module.js

UI Components related to the Screen

42

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 43

Opcenter Execution Discrete UI Modules
Order Work In Progress UI Module

Operation Header Bar
Step List
Task Container
Button Bar

4.13.3 Operator Landing Task List Screen
This Screen belonging to the the Operator Landing Mashup UI Module manages the features related to the different
available Task.

Name
operatorDetailsTask

Angular Controllers related to the Screen
Name

File Name

UADM.operatorLanding

mashup-module.js

UI Components related to the Screen
Operation Header Bar
Task Container
Button Bar

4.13.4 Operator Landing Home Screen
This Screen belonging to the the Operator Landing Mashup UI Module manages the main features of the Operator
Landing page.

Name
operatorLanding

Angular Controllers related to the Screen
Name

File Name

UADM.operatorLanding

mashup-module.js

UI Components related to the Screen
Operation List
Button Bar
Work Order Routing

4.14 Order Work In Progress UI Module
This UI module manages the features needed to monitor the progress of the current Work Order execution.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

43


## Pagina 44

Opcenter Execution Discrete UI Modules
PowderGenealogy UI Module

Name
Siemens.SimaticIT.U4DM.AppU4DM.WIP

Screens and Angular States
Screen

Angular State

Order Work In Progress

home.Siemens_SimaticIT_U4DM_AppU4DM_orderWIP

Angular Controllers related to the Module
Name

File Name

wip_list_Ctrl

Order-wip-list-ctrl.js

wip_operationList_Ctrl

OrderOperation-wip-list-ctrl.js

Services related to the Module
Name

File Name

wip_Svc

Order-wip-srv.js

4.15 PowderGenealogy UI Module
This UI module manages features related to Powder Genealogy.

Name
Siemens.OpcenterEX.AM.PowderMgt.PowderGenealogy

Screens and Angular States
Screen

Angular State

PowderGenealogy

home.Siemens_OpcenterEX_AM_PowderMgt_PowderGenealogy

Angular Controllers related to the Module
Name

File Name

PowderGenealogy_powderGenealogy_Ctrl

powderGenealogy-ctrl.js

44

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 45

Opcenter Execution Discrete UI Modules
Process Catalog Management UI Module (Deprecated)

Services related to the Module
Name

File Name

powder_Svc

powder-srv.js

4.16 Process Catalog Management UI Module (Deprecated)
This UI module manages features related to the Process Catalog.
This UI module is deprecated. Use Siemens.OpcenterEX.DS.BoP.ProcessCatalog.mdui UI Module
available in the BoP App instead.

Name
Siemens.SimaticIT.U4DM.AppU4DM.catalogMgt

Screens and Angular States
Screen

Angular State

Process Catalog Management

home.Siemens_SimaticIT_U4DM_AppU4DM.catalogMgt

Angular Controllers related to the Module
Name

File Name

process_catalog_add_ctrl

process-catalog-add-ctrl.js

process_catalog_edit_ctrl

process-catalog-edit-ctrl.js

Services related to the Module
Name

File Name

catalog_Svc

catalog-srv.js

process_catalog_svc

process-catalog-svc.js

4.17 Team Management UI Module
This UI module implements features related to management of Teams.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

45


## Pagina 46

Opcenter Execution Discrete UI Modules
Transport Operation Landing UI Module

Name
Siemens.SimaticIT.U4DM.AppU4DM.teamMgt

Screens and Angular States
Screen

Angular State

Teams

home.Siemens_SimaticIT_U4DM_AppU4DM_teamMgt

Angular Controllers related to the Module
Name

File Name

teamMgt_selectUsersAdd_Ctrl

teamMgt-select-users-add-ctrl.js

Services related to the Module
Name

File Name

teamMgt_Svc

teamMgt-srv.js

4.18 Transport Operation Landing UI Module
This UI module manages the features related to the execution of Transport Operations.

Name
Siemens.SimaticIT.U4DM.AppU4DM.transportOperationExecution

Screens and Angular States
Screen

Angular State

Transport Operation Execution

home.Siemens_SimaticIT_U4DM_AppU4DM_transportOperationLanding

Angular Controllers related to the Module
Name

File Name

transport_operation_buffer_details_Ctrl

transport-operation-buffer-details-ctrl.js

transport_order_details_ctrl

transport-operation-details-ctrl.js

46

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 47

Opcenter Execution Discrete UI Modules
Users and Skills UI Module

Name

File Name

transport_order_handling_unit_ctrl

transport-operation-handling-unit-ctrl.js

transport_operation_handling_unit_materials_add_c
trl

transport-operation-handling-unit-materials-addctrl.js

transport_order_landing_ctrl

transport-operation-landing-ctrl.js

transport_order_details_select_buffer_ctrl

transport-operation-select-item-ctrl.js

Services related to the Module
Name

File Name

transport_operation_srv

transport-operation-srv.js

4.19 Users and Skills UI Module
This UI module manages the features related to Users and Skills.

Name
Siemens.SimaticIT.U4DM.AppU4DM.users

Screens and Angular States
Screen

Angular State

Users

home.Siemens_SimaticIT_U4DM_AppU4DM_users

Skills

home.Siemens_SimaticIT_U4DM_AppU4DM_skills

Angular Controllers related to the Module
Name

File Name

userMgt_skillAdd_Controller

skills-add-ctrl.js

usersMgt_skillsList_Ctrl

skills-list-ctrl.js

usersMgt_skillSelect_Ctrl

skills-select-ctrl.js

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

47


## Pagina 48

Opcenter Execution Discrete UI Modules
Work Order As Built UI Module

Name

File Name

usersMgt_skillSelectDetails_Ctrl

skills-select-details-ctrl.js

usersMgt_usersList_Ctrl

users-list-ctrl.js

usersMgt_select_Ctrl

users-select-ctrl.js

usersMgt_selectDetails_Ctrl

users-select-details-ctrl.js

usersMgt_selectNpa_Ctrl

users-select-npa-ctrl.js

Services related to the Module
Name

File Name

users_Svc

users-srv.js

skills_Svc

skills-srv.js

4.20 Work Order As Built UI Module
This UI module manages the features related to historical data of Work Orders.

Name
Siemens.SimaticIT.U4DM.AppU4DM.asBuilt

Screens and Angular States
Screen

Angular State

Work Order As Built

home.Siemens_SimaticIT_U4DM_AppU4DM_workOrder.asBuilt

Angular Controllers related to the Module
Name

File Name

asBuilt_activHistory_Ctrl

asBuilt-activity-history-ctrl.js

userTeamAssociationHistoryCtrl

asBuilt-activity-history-team-ctrl.js

48

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 49

Opcenter Execution Discrete UI Modules
Work Order As Built UI Module

Name

File Name

asBuilt_change_Ctrl

asBuilt-change-ctrl.js

asBuilt_dataCollection_Ctrl

asBuilt-datacollection-ctrl.js

asBuilt_dependencies_Ctrl

asBuilt-dependencies-ctrl.js

asBuilt_details_Ctrl

asBuilt-details-ctrl.js

asBuilt_dncDetails_Ctrl

asBuilt-dnc-details-ctrl.js

asBuilt_documents_Ctrl

asBuilt-document-ctrl.js

asBuilt_documents_runtime_Ctrl

asBuilt-document-runtime-ctrl.js

asBuilt_hold_Ctrl

asBuilt-hold-ctrl.js

asBuilt_main_Ctrl

asBuilt-main-ctrl.js

asBuilt_material_Ctrl

asBuilt-material-ctrl.js

asBuilt_material_history_Ctrl

asBuilt-material-history-ctrl.js

asBuilt_materialNote_Ctrl

asBuilt-material-note-ctrl.js

asBuilt_nonConformance_buyoff_Ctrl

asBuilt-nonconformance-buyoff-ctrl.js

asBuilt_nonConformance_Ctrl

asBuilt-nonconformance-ctrl.js

asBuilt_notes_Ctrl

asBuilt-note-ctrl.js

asBuilt_operation_Ctrl

asBuilt-operation-ctrl.js

asBuilt-operation-setpoints-ctrl

asBuilt-operation-setpoints-ctrl.js

asBuilt_Pjf_Ctrl

asBuilt-pjf-ctrl.js

asBuilt_qualityInspection_Ctrl

asBuilt-qualityinspection-ctrl.js

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

49


## Pagina 50

Opcenter Execution Discrete UI Modules
Work Order As Planned BOP UI Module

Name

File Name

asBuilt_reopenBatch_Ctrl

asBuilt-reopen-batch-srv.js

asBuilt_reopenSerialize_Ctrl

asBuilt-reopen-serialize-ctrl.js

asBuilt_rework_Ctrl

asBuilt-rework-ctrl.js

asBuilt_serialNumber_Ctrl

asBuilt-serialnumber-ctrl.js

asBuilt_step_Ctrl

asBuilt-step-ctrl.js

asBuilt_subtrates_Ctrl

asBuilt-substrate-ctrl.js

asBuilt_tools_Ctrl

asBuilt-tool-ctrl.js

asBuilt-tool-setpoints-ctrl

asBuilt-tool-setpoints-ctrl.js

asBuilt_workInstruction_automationNodeDetails_Ctrl

asBuilt-workinstruction-automationNodeDetails-ctrl.js

asBuilt_workInstruction_Ctrl

asBuilt-workinstruction-ctrl.js

Services related to the Module
Name

File Name

asBuilt_Svc

asBuilt-srv.js

4.21 Work Order As Planned BOP UI Module
This UI module manages the features related to historical data of Bills Of Processes.

Name
Siemens.SimaticIT.U4DM.AppU4DM.asPlannedBOP

Screens and Angular States
Screen

Angular State

Work Order As Planned BOP

home.Siemens_SimaticIT_U4DM_AppU4DM_asPlannedBOP_workOrder

50

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 51

Opcenter Execution Discrete UI Modules
Work Order Status UI Module (Deprecated)

Angular Controllers related to the Module
Name

File Name

asPlannedBOP_List_Ctrl

asPlannedBOP-list-ctrl.js

asPlannedBOP_Select_Ctrl

asPlannedBOP-select-ctrl.js

Services related to the Module
Name

File Name

asPlannedBOP_Svc

asPlannedBOP-srv.js

4.22 Work Order Status UI Module (Deprecated)
This UI module manages several features, primarily related to pre-kitting.
This UI module is deprecated. Use
Siemens.SimaticIT.U4DM.AppU4DM.WorkOrderPreKitting.mdui MDUI Module available in
AppU4DM instead.

Name
Siemens.SimaticIT.U4DM.AppU4DM.workOrderStatus

Screen and Angular States
Screen

Angular State

Work Order Prekit

home.Siemens_SimaticIT_U4DM_AppU4DM_workOrder_prekit

Angular Controllers related to the Module
Name

File Name

skillsSelectionAddToWorkOrderOperationCtrl

workorder-operation-skill-add-ctrl.js

workOrderStatus_MasterPlanOperationAdd_Ctrl

workorder-mp-operation-add-ctrl.js

workOrderStatus_workOrderAdd_Ctrl

workorder-add-ctrl.js

workOrderStatus_workOrderAddSerialNumber_Ctrl

workorder-select-serialnumber-add-ctrl.js

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

51


## Pagina 52

Opcenter Execution Discrete UI Modules
Work Order Status UI Module (Deprecated)

Name

File Name

workOrderStatus_workOrderAlternativeOperationsGroupAd
d_Ctrl

workorder-select-alternative-operations-addctrl.js

workOrderStatus_workOrderAlternativeOperationsGroupEdi
t_Ctrl

workorder-select-alternative-operations-editctrl.js

workOrderStatus_workOrderMerge_Ctrl

workorder-merge-ctrl.js

workOrderStatus_workOrderOperationAdd_Ctrl

workorder-operation-add-ctrl.js

workOrderStatus_workOrderOperationSelectDependencies_
Ctrl

workorder-select-operations-dependencies.js

workOrderStatus_workOrderOperationSelectDetails_Ctrl

workorder-operation-select-details-ctrl.js

workOrderStatus_workOrderPrekitDetails_Ctrl

workorder-prekit-details-ctrl.js

workOrderStatus_workOrderPrekitEditView_Ctrl

workorder-prekit-edit-ctrl.js

workOrderStatus_workOrderPrekitList_Ctrl

workorder-prekit-list-ctrl.js

workOrderStatus_workOrderStatusPrekitSerialNumberSearc
h_Ctrl

workorder-prekit-snsearch-list-ctrl.js

Services related to the Module
Name

File Name

workOrderStatus_Svc

workorder-status-srv.js

52

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 53

Opcenter Execution Discrete UI Components
Button Bar UI Component

5 Opcenter Execution Discrete UI Components
User Interface Components are objects which can be deployed on a page to create a graphical interface for an
application.
Opcenter Execution Discrete provides you with a set of UI Components dedicated to the management of its internal
functionalities.

Available UI Components
Button Bar
Bill of Materials
Customizable Button Bar
High Automation Header Bar
Declare Defect
Document Preview
Execution Group Details
Execution Groups Document Preview
Execution Groups Header Bar
High Automation Equipment List UI Component
Load Powder
Material Production
Material Tracking
Operation Header Bar
Operation List
Part Program
Print Job File
Quality Inspection
Step List
Task Details (Deprecated)
Task Container
Task Viewer
Tracking AM Powder
Work Order Routing
Zero Touch Component Manager

5.1 Button Bar UI Component
This User Interface component displays the Button Bar User Interface Component.

Name
siemensSimaticitU4dmAppu4dmButtonbar

Layout
Size

Rows

Columns

Default

1

12

Min

1

1

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

53


## Pagina 54

Opcenter Execution Discrete UI Components
Button Bar UI Component

Size

Rows

Columns

Max

12

12

Destination Methods
Destination Method

Description

Parameters

setStartVisible

Changes visibility of the Start button.

visible (boolean)

setPauseVisible

Changes visibility of the Pause button.

visible (boolean)

setSkipVisible

Changes visibility of the Skip button.

visible (boolean)

setCompleteVisible

Changes visibility of the Complete button.

visible (boolean)

setCompleteStepsVisible

Changes visibility of the Complete Steps button.

visible (boolean)

setGoToDetailVisible

Changes visibility of the Go To Detail button.

visible (boolean)

initialize

Initializes buttons in the bar.

buttonStatus (object)

setCurrentOperationId

Sets the current Work Order Operation Id.

wooId (number)

setActionVisible

Sets visibility of menu items in Action button.

selectedOperations (object)

updateButtonVisibility

Updates the visibilty of a button.

id (string)

updateButtonsStates

Sets multiple buttons states (enable or disable).

buttonStates (array)

Source Events
Source Event

Description

start

User clicked Start

pause

User clicked Pause

skip

User clicked Skip

complete

User clicked Complete

54

Parameters

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 55

Opcenter Execution Discrete UI Components
Button Bar UI Component

Source Event

Description

Parameters

completeSteps

User clicked Complete Steps

goToDetail

User clicked Go To Detail

goToDetailSteps

User clicked Go To Detail and steps exist

goToExecutionGroupDetails

User clicked go to detail and execution group exist

execGroupPhaseId (string)

setContextProperty_mode

Sets the mode context property.

mode (string)

setContextProperty_isPoc

Set the isPoc context property.

goToDeclareDefect

Opens the Declare Defect mashup.

setContextProperty_wooId

Sets Work Order Operation Id to context.

wooId (number)

team

Manages team configuration.

teamId (string)

buttonClicked

The user wants to click the custom button

startSteps

User started a step.

id(string)
data(Object)

Customization
The following customizations on the ButtonBar UI Component are possible:
hide standard buttons
add custom buttons, with related custom business logic.
The following buttons are available by default:
Start
Pause
Skip
Complete
StepComplete
AddDocument
goToInterlocking
Notes
Defects
ChangeNonConformance
Travelling
ExecutionGroupLink
RequestMaterial
JoinTeam

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

55


## Pagina 56

Opcenter Execution Discrete UI Components
Bill of Materials UI Component

leaveTeam
showDocumentPreview
labelPrinting
goToChangeSerialNumbers
goToGenealogyLink
freezeTargetQuantity
woAbruptClosure
To customize the ButtonBar UI Component:
1. In the Opcenter Execution Foundation Solution Studio environment, select User Interface > Mashups.
2. Open the OperatorLanding > operatorDetailsTask UI Screen.
You can also customize the ButtonBar UI Component contained in the operatorLanding
and operatorDetailsStep UI Screens in the same manner.
3. Select the ButtonBar UI Component and click configuration.
4. To customize the behavior of each button, update the value of the tags of interest, as follows:
To hide a button, set visibility to "false".
To disable a button, set disabled to "false".
To change the icon of the button, provide the path to the new icon.
To change the alignment of the button, set align to "right".
To add a custom button, copy the code provided for a standard button (see for example the code relative
to the Start button in the box below) and change the values accordingly. Make sure that the required
business logic is also available and linked to the button while configuring the wiring.
{
"type": "Command",
"id": "start",
"name":
"Siemens.SimaticIT.U4DM.AppU4DM.AppU4DM.DMPOMModel.Commands.UADMStartOperati
on",
"unauthorizedBehavior": "hide",
"svgIcon": "common/icons/cmdStart24.svg",
"label": "sit.u4dm.start",
"visibility": true,
"disabled": true,
"align": "left"
},

5. Click Apply

5.2 Bill of Materials UI Component
This User Interface component displays the Bill of Materials to provide information for the list of raw Materials.

Name
siemensSimaticitU4dmAppu4dmBillofmaterials

Layout

56

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 57

Opcenter Execution Discrete UI Components
Bill of Materials UI Component

Size

Rows

Columns

Default

10

10

Min

1

1

Max

12

12

Destination Methods
Destination Method

Description

Parameters

Type

initializeBOM

Displays the item list as pet the given final material.

finalMaterialId

string

Source Events
Destination Method

Description

Parameters

Type

onBoMDocClick

This event will send the material Id to the Document Preview
component.

materialId

string

UI Component Properties
Source
Event

Description

Default

Type

CustomVie
w

The view that contains the entity which displays the Bill of Materials. The
column names used in the CustomView are listed below:

vEXDSB
oM

strin
g

DocumentId
MaterialId
Material
Description
UoM
Quantity
showTrace
ability

The option to display the traceability indicator. If you want to display this
option, you need to set the field as true.

false

bool
ean

isRowExpa
nded

The option to display the grouped items in expanded form by default.

true

bool
ean

groupRowB
y

The column name by which the items will be grouped.

Materia
l

strin
g

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

57


## Pagina 58

Opcenter Execution Discrete UI Components
Customizable Button Bar UI Component

Source
Event

Description

Default

Type

parentBOM
Key

The items grouped together based on the parent BOM which is listed in the
View.

Parent
Bom

strin
g

5.3 Customizable Button Bar UI Component
This User Interface component displays the Customizable Button Bar User Interface Component.

Name
siemensSimaticitU4dmAppu4dmCustomizablebuttonbar

Layout
Size

Rows

Columns

Default

2

12

Min

2

2

Max

4

12

Destination Methods
Destination Method

Description

Parameters

updateButtonVisibility

Updates the visibility of the Button

configureButtonBar

Configures the Button Bar

config(Object)

updateButtonsStates

Sets multiple buttons states (enable or disable)

buttonStates(Array)

id(string)
visibility(Boolean)
disabled(Boolean)

Source Events
Source Event

Description

buttonClicked

The user wants to click the custom button

58

Parameters
id(string)
data(Object
)

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 59

Opcenter Execution Discrete UI Components
High Automation Header Bar UI Component

Source Event

Description

workOrderOperationStartByUser

The user wants to start the Work Operation

workOrderOperationPauseByUser

The user wants to Pause the Work Operation

workOrderOperationCompleteByUser

The user wants to complete the Work Operation

manageTeam

Manages the team configuration

changeMachine

User wants to change the machine

toggleDocumentPreview

User wants to toggle the visibility of the
Document Previewer

Parameters

teamId(string)

Customization
The following customizations on the CustomizableButtonBar UI Component are possible:
hide standard buttons
add custom buttons, with related custom business logic.
The following buttons are available by default:
Start
Pause
Complete
AddDocument
Defects
ChangeNonConformance
RequestMaterial
Notes
JoinTeam
leaveTeam
ChangeMachine.
For more information, see section Configuring Runtime Screens of the Opcenter Execution Discrete Installation and
Configuration Manual.

5.4 High Automation Header Bar UI Component
This User Interface component displays a high automation Header Bar with summary information for a Work Order
Operation.

Name
siemensSimaticitU4dmAppu4dmHighautomationheaderbar

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

59


## Pagina 60

Opcenter Execution Discrete UI Components
Declare Defect UI Component

Layout
Size

Rows

Columns

Default

2

12

Min

1

12

Max

2

12

Destination Methods
Destination Method

Description

Parameters

setWorkOrderOperat
ion

Sets the Work Order Operation the component is
showing information about.

workOrderOperationId(n
umber)

setParentState

Sets a value identifying the parent state.

parent (string)

initialize

Initializes the header bar.

workCenter(object)

Source Event

Description

Parameters

goToParent

Goes to mashup defined as parent of this one.

stateId (string)

sendFinalMaterialDeta
ils

This event will send the final material details to the BOM
component.

FinalMaterialDetails
(string)

Source Events

5.5 Declare Defect UI Component
This User Interface component allows to declare and update Defects and Non-Conformances.

Name
siemensSimaticitU4dmAppu4dmDeclaredefect

Layout
Size

Rows

Columns

Default

6

6

60

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 61

Opcenter Execution Discrete UI Components
Document Preview UI Component

Size

Rows

Columns

Min

6

6

Max

12

12

Destination Methods
Destination Method

Description

Parameters

initialize

Initializes the component.

param (string)

Source Events
Source Event

Description

goToDetail

Goes to the parent Detail mashup

Parameters

5.6 Document Preview UI Component
This User Interface component displays a list of Documents and allows you to preview them.

Name
siemensSimaticitU4dmAppu4dmDocumentpreview

Layout
Size

Rows

Columns

Default

8

4

Min

6

3

Max

10

6

Destination Methods
Destination Method

Description

initializeDocuments

Initialize the document list.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

Parameters
wooId (number)
wosId (number)

61


## Pagina 62

Opcenter Execution Discrete UI Components
Document Preview UI Component

Source Events
Source Event

Description

Parameters

docClick

Fires when a document is clicked.

docId (string)

UI Component Properties
Sectio
n

Propert
y

Description

Default

Ty
pe

Docu
ment
Viewe
r

title

The Title of the document viewer to be displayed. The title will be
localized only if the translation keys are present in the resource file,
or else the title will be displayed as it is entered.

sit.u4dm.do
cuments

stri
ng

autoSel
ectFirst
Docume
nt

An option to prevent the default selection of the documents.

true

bo
ole
an

mode

The specific mode for the viewer. The available options are as
follows:

display

stri
ng

viewer

stri
ng

display: It will display the category tabset field and viewer.
details: It will display the tabs in the expanded mode.
fullScre
enMode

An option to configure the full screen preview. The available
options are as follows:
viewer: The document is displayed in the fullscreen mode when
you click on the document from the viewer.
toolbar: A fullscreen button is displayed in the sit-documentviewer toolbar, so as to open the full screen mode.

PDF
Plugin

62

isFitPag
eWidth

An option to display the PDF in full page width.

false

bo
ole
an

isSingle
Page

An option to display the PDF in single page view or multi page view
based on the container width.

false

bo
ole
an

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 63

Opcenter Execution Discrete UI Components
Execution Group Details UI Component

Sectio
n

Propert
y

Description

Default

Ty
pe

Notes
Config
uratio
n

sqlView
ForNote
s

The textual information can be represented as Notes in the
Document Viewer by creating an SQL View and updating the
Message field.

vEXDSSnag
AndNote

stri
ng

If you want to differentiate the data provided in Notes as Header
and Paragraphs, then you need to add the html tags while creating
the Notes. For Headers you can use the </h3> tags and for
Paragraphs you can use the <span> tags. Below listed are some
examples to create Notes in the Document Viewer:
Product Notes: Operations can also be started and completed
automatically by Machines.
Order Notes: Operations can be completed automatically by any
member of the Team.
Use combination of </h3> tag and <span> tag while you save your
data in the database.
</h3>Product Notes</h3>
<span>Operations can also be started and completed
automatically by Machines.<span>

The
maximum
limit of
characters
allowed in
Notes is
255. If the
limit
exceeds,
you will
receive a
Validation
error popup message.

</h3>Order Notes</h3>
<span>Operations can be completed automatically by any
member of the Team.<span>
If there are no Notes available for Work Order operation,
then the Notes tab in the Document Viewer will not be
visible.
The SQL View should be created with the same column names. The
column names are as follows:
WorkOrderOperation
Message

5.7 Execution Group Details UI Component
This User Interface component displays a series of tabs to show the details of Execution Groups.

Name
siemensSimaticitU4dmAppu4dmExecgroupdetails

Layout

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

63


## Pagina 64

Opcenter Execution Discrete UI Components
Execution Groups Document Preview UI Component

Size

Rows

Columns

Default

8

8

Min

6

4

Max

12

12

Destination Methods
Destination Method

Description

Parameters

loadDetails

Loads the Details screen.

startExecutionGroupPhaseOperat
ions

Starts all selected execution Group
phases.

completeExecutionGroupPhase

Completes all selected execution
Group phases.

pauseExecutionGroupPhase

Pauses all selected execution Group
phases.

execGroupPhaseNId
(string)
currentTabId (string)

Source Events
Source Event

Description

Parameters

refresh

Fires when starting operations.

executionGroupPhaseId (string)

5.8 Execution Groups Document Preview UI Component
This User Interface component displays a list of Documents to be shown during execution of Execution Groups and
allows you to preview them.

Name
siemensSimaticitU4dmAppu4dmExecgroupdocumentpreview

Layout

64

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 65

Opcenter Execution Discrete UI Components
Execution Groups Header Bar UI Component

Size

Rows

Columns

Default

8

4

Min

6

3

Max

12

12

Destination Methods
Destination Method

Description

Parameters

refreshDocuments

Refreshes the component showing tabs available for the exec
group current phase.

execGroupId
(number)

5.9 Execution Groups Header Bar UI Component
This User Interface component displays a Header Bar with summary information for an Execution Group.

Name
siemensSimaticitU4dmAppu4dmExecgroupheaderbar

Layout
Size

Rows

Columns

Default

2

12

Min

1

1

Max

12

12

Destination Methods
Destination Method

Description

Parameters

getExecutionGroupPhaseDetai
ls

Retrieves details about the selected Execution
Group Phase.

execGroupPhaseId
(string)

setParentState

Sets a value identifying the parent state.

parent (string)

Source Events

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

65


## Pagina 66

Opcenter Execution Discrete UI Components
High Automation Equipment List UI Component

Source Event

Description

Parameters

goToParent

Same as clicking the back button.

5.10 High Automation Equipment List UI Component
This User Interface component displays a list of Equipments inside the High Automation Landing Page.

Name
siemensSimaticitU4dmAppu4dmHighautomationequipmentlist

Layout
Size

Rows

Columns

Default

6

12

Min

3

3

Max

12

12

Destination Methods
Destination Method

Description

setMachineAsWorkplace

Sets selected Machine or Workcentre as
orkplace

Parameters

Source Events
Source Event

Description

Parameters

EquipmentSelectionChanged

Fired when an equipment selection is changed.

data (object)

EquipmentSelected

Fired when an equipment is selected as the work
center.

EquipmentNId
(string)
StateId (string)

5.11 Load Powder UI Component
This User Interface component displays the Task to manage the loading of Powder into the 3D Printer during
production execution.

66

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 67

Opcenter Execution Discrete UI Components
Material Production UI Component

Name
siemensOpcenterexAmRuntimeampowderintSetup3dprintercomponent

Layout
Size

Rows

Columns

Default

6

6

Min

6

6

Max

6

6

Destination Methods
None.

Source Events
None.

5.12 Material Production UI Component
This User Interface component keeps track of production of co-products and by-products.

Name
siemensSimaticitU4dmAppu4dmMaterialproductioncomponent

Layout
Size

Rows

Columns

Default

6

6

Min

3

1

Max

12

12

Destination Methods
None.

Source Events
None.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

67


## Pagina 68

Opcenter Execution Discrete UI Components
Material Tracking UI Component

5.13 Material Tracking UI Component
This User Interface component displays the Material Tracking User Interface component.

Name
siemensSimaticitU4dmAppu4dmMaterialtracking

Layout
Size

Rows

Columns

Default

6

6

Min

3

3

Max

12

12

Destination Methods
Destination Method

Description

initializeMaterialTracker

Initializes material tracker
component.

Parameters
WorkOrderOperation
(number)
WorkOrderStep (number)
serialNumberList (Array)

Source Events
None.

5.14 Operation Header Bar UI Component
This User Interface component displays a Header Bar with summary information for a Work Order Operation.

Name
siemensSimaticitU4dmAppu4dmOperationheaderbar

Layout
Size

Rows

Columns

Default

2

12

Min

1

1

68

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 69

Opcenter Execution Discrete UI Components
Operation List UI Component

Size

Rows

Columns

Max

12

12

Destination Methods
Destination Method

Description

Parameters

goToParent

Same as clicking the Back button.

setWorkOrderOperatio
n

Sets the Work Order Operation the component is
showing information about

workOrderOperationId
(number)

setParentState

Sets a value identifying the parent state

parent (string)

Source Events
Source Event

Description

Parameters

nextWorkOrderOperation

User wants to work on the next Work Order
Operation

currentWOO
(object)
nextWOO (object)

previousWorkOrderOperati
on

User wants to work on the previous Work Order
Operation

currentWOO
(object)
previousWOO
(object)

goToParent

Goes to mashup defined as parent of this one.

stateId (string)

operationDetailsLoaded

Notifies other components that details are loaded.

operation (object)

setContextProperty_wooId

Sets the wooId context property.

wooId (number)

setContextProperty_isPoc

Sets the isPoc context property.

isPoc (string)

5.15 Operation List UI Component
This User Interface component displays the list of Work Order Operations.

Name
siemensSimaticitU4dmAppu4dmOperationlist

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

69


## Pagina 70

Opcenter Execution Discrete UI Components
Operation List UI Component

Layout
Size

Rows

Columns

Default

9

3

Min

1

1

Max

12

12

Destination Methods
Destination Method

Description

startOperations

Starts all selected operations.

pauseOperations

Pauses all selected operations.

skipOperations

Skips all selected operations.

completeOperations

Completes all selected operations.

manageTeam

Manages user-team relations.

Parameters

teamAssociationId (string)

Source Events
Source Event

Description

operationSelectionC
hanged

User selected/unselected an operation

allCanBeStartedChan
ged

Whether or not all of the selected work order operations
can be started has changed

allCanBeStarted
(boolean)

allCanBePausedChan
ged

Whether or not all of the selected work order operations
can be started has changed

allCanBePaused
(boolean)

allCanBeSkippedCha
nged

Whether or not all of the selected work order operations
can be started has changed

allCanBeSkipped
(boolean)

70

Parameters
selections (object)
firstSelectedWooId
(string)

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 71

Opcenter Execution Discrete UI Components
Part Program UI Component

Source Event

Description

Parameters

allCanBeCompletedC
hanged

Whether or not all of the selected work order operations
can be started has changed

allCanBeCompleted
(boolean)

goToDetails

Opens the details state

detailsStateName
(string)

goToDetailsSteps

Opens the details with steps state

detailsStateName
(string)

canGoToDetailChang
ed

Whether or not the user can go to the operator detail state

canGoToDetail
(boolean)

setContextProperty_
mode

Sets the mode context property

mode (string)

goToGenealogyLink

Opens the Genealogy state

5.16 Part Program UI Component
This User Interface component manages the transfer of Part Programs to DNC Machines.

Name
siemensSimaticitU4dmAppu4dmPartprogramcomponent

Layout
Size

Rows

Columns

Default

3

3

Min

2

3

Max

4

4

Destination Methods
None.

Source Events
None.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

71


## Pagina 72

Opcenter Execution Discrete UI Components
Print Job File UI Component

5.17 Print Job File UI Component
This User Interface component displays the Print Job File Transfer Component.

Name
siemensSimaticitU4dmAppu4dmPrintjobfileComponent

Layout
Size

Rows

Columns

Default

3

3

Min

2

3

Max

4

4

Destination Methods
None.

Source Events
None.

5.18 Quality Inspection UI Component
This User Interface component manages the interface for Quality Inspections.

Name
siemensSimaticitU4dmAppu4dmQualityinspectioncomponent

Layout
Size

Rows

Columns

Default

3

3

Min

2

3

Max

4

4

Destination Methods
None.

72

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 73

Opcenter Execution Discrete UI Components
Step List UI Component

Source Events
None.

5.19 Step List UI Component
This User Interface component displays the list of Work Order Operation steps.

Name
siemensSimaticitU4dmAppu4dmSteplist

Layout
Size

Rows

Columns

Default

8

2

Min

1

1

Max

12

12

Destination Methods
Destination Method

Description

Parameters

initialize

Initial settings for the step list

wooId (number)

complete

Completes all selected steps.

refreshTree

Refreshes the data.

wooId (number)
refresh (boolean)

Source Events
Source Event

Description

stepSelectionChanged

A new step is selected.

allStepsCanBeCompletedCh
anged

Checks if one or more steps that can be
completed have changed.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

Parameters
selectedSteps (object)
clickedStep (object)
wooId (number)
wosId (number)
selectedOperations (object)
allStepsCanBeCompleted
(boolean)

73


## Pagina 74

Opcenter Execution Discrete UI Components
Task Details UI Component (Deprecated)

5.20 Task Details UI Component (Deprecated)
This User Interface component displays the details of a task in a set of tabs.
This UI Component is deprecated. Use the Task Container UI Component instead.

Name
siemensSimaticitU4dmAppu4dmTaskdetails

Layout
Size

Rows

Columns

Default

8

4

Min

6

4

Max

12

8

Destination Methods
Destination Method

Description

initializeTaskDetails

Initializes the component

completeOperation

Completes the work order operation

pauseOperation

Pauses the work order operation

skipOperation

Skips the work order operation

startOperation

Starts the work order operation

Parameters
wooId (number)
wosId (number)

Source Events
Source Event

Description

Parameters

operationCompleted

Work Order Operation has been successfully completed

wooId (number)

operationPaused

Work Order Operation has been successfully paused

wooId (number)

74

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 75

Opcenter Execution Discrete UI Components
Task Details UI Component (Deprecated)

Source Event

Description

Parameters

operationSkipped

Work Order Operation has been successfully skipped

wooId (number)

operationStarted

Work Order Operation has been successfully started

wooId (number)

canBeStartedChanged

Notifies if operation can be started

canStart (boolean)

canBePausedChanged

Notifies if operation can be paused

canPause (boolean)

canBeCompletedChanged

Notifies if operation can be completed

canComplete
(boolean)

operationStatusChanged

Notifies that the status of current operation changed

selections (object)

Customization
Here is an example of how to create a Custom Tab containing a Widget. Your starting point is a custom tab that
displays the NId of the Work Order Operation or Step in Runtime. The value displayed changes dynamically,
depending on which Work Order Operation or Step is selected.
Here are the contents of the sitTestStep widget for what concerns sitTestStep.html:
<div>{{vm.teststep}}</div>

Here are the contents of the sitTestStep widget for what concerns sitTestStep.js:
(function () {
'use strict';
var controllerName = 'sitTestStep';
angular.module('Siemens.SimaticIT.U4DM.AppU4DM.widgets').directive(controllerName,
toSeeStepOpNid);
function toSeeStepOpNid() {
return {
restrict: 'E',
scope: {},
bindToController: {
workOrderStep: '=?sitWorkOrderStep',
workOrderOperation: '=?sitWorkOrderOperation'
},
controller: toSeeStepOpNidCtrl,
controllerAs: 'vm',
templateUrl: 'Siemens.SimaticIT.U4DM.AppU4DM/widgets/testWidGet/
testWidGet.html'
};
}

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

75


## Pagina 76

Opcenter Execution Discrete UI Components
Task Details UI Component (Deprecated)

toSeeStepOpNidCtrl.$inject = ['u4dm.services.runtime', 'u4dm.services', '$q',
'$state', '$scope', '$timeout', '$window', 'u4dm.constants'];
function toSeeStepOpNidCtrl(u4dmRuntimeSvc, u4dmSvc, $q, $state, $scope,
$timeout, $window, u4dmConstants) {
var vm = this;
vm.teststep = 'null';
init();
function init() {
setWatches();

$timeout(function () {
// trick ICV to resize after side panel open.
bind to 'resize', so this should work
angular.element($window).trigger('resize');
});
}

ICV uses jqLite to

function setWatches() {
$scope.$watch("vm.workOrderStep", refreshWithSignals);
$scope.$watch("vm.workOrderOperation", refreshWithSignals);
}
function refreshWithSignals() {
if (vm.workOrderStep)
{ vm.teststep = vm.workOrderStep.NId; }
else
{
vm.teststep = vm.workOrderOperation.NId;
}
}
}
})();

Here is the sitTaskDetails component customization:
(function () {
'use strict';
var mod =angular.module('Siemens.SimaticIT.U4DM.AppU4DM.services.customServices');
mod.service('sitTaskDetail_custom', ['u4dm.services', sitTaskDetail_custom]);
function sitTaskDetail_custom() {
this.tabsConfig = function (tabs) {
tabs.push({
heading: 'CUSTOMTAB',
route: 'home.Siemens_SimaticIT_U4DM_AppU4DM_workOrder.select.customtab',
active: true,
visible: true,
content: '<sit-test-step sit-work-order-step="vm.workOrderStep" sit-work-orderoperation="vm.workOrderOperation"></sit-test-step>'

76

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 77

Opcenter Execution Discrete UI Components
Task Container UI Component

});
return tabs;
};
}})();

5.21 Task Container UI Component
This User Interface component displays the list of available Tasks to be managed during production execution.
The default Tasks are:
UADMMaterialConsumptionTask
UADMToolUsageTask
UADMWorkInstructionTask
UADMQualityInspectionTask
UADMPrintJobFilesTask
UADMPartProgramTask
For more information on how these tasks are used at runtime, see section Managing Tasks for Work Order Operation
or Step Progression of the Opcenter Execution Discrete User Manual.

Name
siemensSimaticitU4dmAppu4dmTaskcontainer

Layout
Size

Rows

Columns

Default

8

4

6

4

12

12

Max

Destination Methods
Destination
Method

Description

initializeTaskDet
ailsForSteps

Initializes the Task Container UI Component
for the Work Order Steps.

Parameters

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

wooId (String that identifies the Id of
the Work Order Operation)
wosId (String that identifies the Id of
the Work Order Step)
executionGroupId (String that
identifies the Id of the Execution
Group).

77


## Pagina 78

Opcenter Execution Discrete UI Components
Task Container UI Component

Destination
Method

Description

Parameters

initializeTaskDet
ailsForTasks

Initialized the Task Container UI Component
for the selected Work Order Operation.

completeOperati
on

Completes the selected Work Order
Operation.

pauseOperation

Pauses the selected Work Order Operation.

skipOperation

Skips the selected Work Order Operation.

startOperation

Starts the selected Work Order Operation.

startStep

Starts the selected Work Order Step.

id (String that identifies the Id of the
Work Order Operation)
executionGroupId (String that
identifies the Id of the Execution
Group).

Source Events
Source Event

Description

Parameters

operationCompl
eted

Work Order Operation has been
successfully completed.

wooId (String that identifies the Id of the
Work Order Operation)

operationPause
d

Work Order Operation has been
successfully paused.

wooId (String that identifies the Id of the
Work Order Operation)

operationSkippe
d

Work Order Operation has been
successfully skipped.

wooId (String that identifies the Id of the
Work Order Operation)

operationStarte
d

Work Order Operation has been
successfully started.

wooId (String that identifies the Id of the
Work Order Operation)

canBeStartedCh
anged

Notifies if the Work Order Operation can
be started.

canStart (boolean)

canBePausedCh
anged

Notifies if the Work Order Operation can
be paused.

canPause (boolean)

78

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 79

Opcenter Execution Discrete UI Components
Task Container UI Component

Source Event

Description

Parameters

canBeSkippedCh
anged

Notifies if the Work Order Operation can
be skipped.

canSkip (boolean)

canBeCompleted
Changed

Notifies if the Work Order Operation can
be skipped.

canComplete (boolean)

operationStatus
Changed

Notifies that the status of the current Work
Order Operation has changed.

selections (object)

stepStarted

Work Order Step has been successfully
started.

wooId (number)

stepCompleted

Work Order Step has been successfully
completed.

wooId (number)

UI Component Properties
Secti
on

Propert
y

Description

Defaul
t

Ty
pe

Confi
gurat
ion

configu
ration

The configuration for different behaviors for High Automation Landing
Page. The various configurations that can be preformed are as follows:

object

obj
ect

Docu
ment
View
er

title

The Title of the document viewer to be displayed. The title will be localized
only if the translation keys are present in the resource file, or else the title
will be displayed as it is entered.

sit.u4d
m.doc
ument
s

stri
ng

autoSel
ectFirst
Docum
ent

An option to prevent the default selection of the documents.

true

bo
ole
an

HiddenTaskStatusNId: It displays the Task listed status in HALP. The
available options for status are Failed, Completed, Aborted, Canceled
and Skipped. If the Task is in the listed, in the above mentioned status,
then the Task will not be displayed.
ContextualCommandBar: The list of the type of Task than can be
displayed in the HALP.
OpenDocPreviewOnLoad: An option to display the Document Preview
on HALP. The Document Preview will be displayed in the HALP on load,
when the OpenDocPreviewOnLoad is set as True.
DocumentPreWidth: The percentage of width, the Document Preview
will acquire on loading. The default value is 30 and the maximum value
is 60.

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

79


## Pagina 80

Opcenter Execution Discrete UI Components
Task Viewer UI Component

Secti
on

Propert
y

Description

Defaul
t

Ty
pe

mode

The specific mode for the viewer. The available options are as follows:

displa
y

stri
ng

viewer

stri
ng

display: It will display the category tabset field and viewer.
details: It will display the tabs in the expanded mode.
fullScre
enMode

An option to configure the full screen preview. The available options are as
follows:
viewer: The document is displayed in the fullscreen mode when you
click on the document from the viewer.
toolbar: A fullscreen button is displayed in the sit-document-viewer
toolbar, so as to open the full screen mode.

PDF
Plugi
n

isFitPa
geWidt
h

An option to display the PDF in full page width.

false

bo
ole
an

isSingle
Page

An option to display the PDF in single page view or multi page view based
on the container width.

false

bo
ole
an

All these UI component properties can be configured to the Document Preview inside the Task Container
component and not in the Document Preview component.

Customization
The following customizations on the Task Container UI Component are possible:
customization of the component's visibility according to the status of the Task. Available statuses for Tasks
are: InProgress, Error, Paused, Ready, Suspended, NotReady, Created, Failed, Aborted, Canceled, Skipped
, Completed.
customization of the Contextual Command bar's visibility depending on the Task type. Available Tasks
are: UADMMaterialConsumptionTask, UADMToolUsageTask, UADMWorkInstructionTask, UADMQualityInsp
ectionTask, UADMPrintJobFilesTask, UADMPartProgramTask.
For more information, see section Configuring Runtime Screens of the Opcenter Execution Discrete Installation and
Configuration Manual.

5.22 Task Viewer UI Component
This User Interface component displays a single Task to be managed during production execution.
For more information on how these tasks are used at runtime, see section Managing Tasks for Work Order Operation
or Step Progression of the Opcenter Execution Discrete User Manual.

Name

80

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 81

Opcenter Execution Discrete UI Components
Tracking AM Powder UI Component

siemensSimaticitU4dmAppu4dmTaskviewer

Layout
Size

Rows

Columns

Default

6

2

Min

6

2

Max

6

12

Destination Methods
Destination Method

Description

Parameters

setWooId

Identifier of the Work Order Operation to which the step belongs.

id (string)

Source Events
Source Event

Description

Parameters

onSelectedItem

Fires when the task is selected.

item (string)

5.23 Tracking AM Powder UI Component
This User Interface component displays the Task to manage the tracking of Powder Batches, previously loaded into
3D Printers, used for printing operations in Additive Manufacturing production.

Name
siemensOpcenterexAmRuntimeampowderintTrackingampowdercomponent

Layout
Size

Rows

Columns

Default

8

4

Min

6

4

Max

12

8

Destination Methods

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

81


## Pagina 82

Opcenter Execution Discrete UI Components
Work Order Routing UI Component

None.

Source Events
None.

5.24 Work Order Routing UI Component
This User Interface component displays the Routing of Work Order Operations or Steps.

Name
siemensSimaticitU4dmAppu4dmWorkorderrouting

Layout
Size

Rows

Columns

Default

6

6

Min

2

2

Max

12

12

Destination Methods
Destination Method

Description

Parameters

SetOperationRouting

Shows routing of Work Order Operations or Steps.

selections (object)

Source Events
None.

5.25 Zero Touch Component UI Component
This User Interface component displays the Zero Touch Component User Interface component.

Name
siemensSimaticitU4dmAppu4dmZerotouchcomponent

Layout
Size

Rows

Columns

Default

1

1

82

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual


## Pagina 83

Opcenter Execution Discrete UI Components
Zero Touch Component UI Component

Size

Rows

Columns

Min

1

1

Max

6

6

Destination Methods
Destination Method

Description

Parameters

workOrderOperationStartByUser

Starts the Work Order Operation manually

workOrderOperationCompleteByUser

Completes the Work Order Operation
manually

parent (string)

workOrderOperationPauseByUser

Pauses the Work Order Operation
manually

workCenter(obje
ct)

manageTeam

Manages user-team relations

team(string)

changeMachine

Changes the selected machine

Source Events
Source Event

Description

onWorkOrderOperationStartedBy
Machine

Fired when a Work Order Operation is
automatically started by a machine

workOrderOpera
tionId (Number)
materialList(Arra
y)

onWorkOrderOperationCompleted

Notifies other components that details are
loaded

operation (object)
work order
operation(Object)

onWorkOrderOperationAssembled

Fired when a work order operation is
assembled

workOrderOpera
tionId(Number)
mater(string)

initialized

Fired when a component is initialized

machineContext(Obj
ect)

onMachineDeselected

Fired when work-center change is clicked

StateId(string)

Opcenter Execution Discrete 2507.0001 - UI Reference and Customization Manual

Parameters

83
