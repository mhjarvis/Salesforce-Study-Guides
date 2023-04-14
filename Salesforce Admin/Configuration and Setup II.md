<h1 style="text-align: center; font-size: 40px">Configuration and Setup II</h1>

# UI Features: UI Settings

## UI Features: UI Settings
There are two ways to set a default record page view at the org level:
* ```Full View``` - data-dense, focuses on details and related lists and puts all info on the same page.
* ```Group View``` - divides records info into groupings across multiple regions and tabs.

Found in ```Setup -> Record Page Settings```.

To ```override``` a default view, a ```custom``` Lightning record page can be created for a specified object and activated in ```Lightning App Builder```. Custom ```Lightning record pages``` can be activated selectively by Lightning app, record type, or profile.      

## User Interface Settings
User Interface settings are modified via ```User Interface``` in Settings. Here you can find a list of ```features that can be enabled or disabled```. These include:

    - Enable Hover Details
    - Related List Hover Links
    - Inline Editing in Lightning Experience - pencil icon appears if editable
    
    - Disable Navigation Bar Personalization in Lightning Experience
    - Enable Printaable List Views - button enable when in list view
    - Enable Salesforce Notification Banner

## Lightning Experience Navigation Bar
The lightning experience nav bar can contain most of the following: standard/custom objects, lightning component tabs, web tabs, utilities like lightning voice, lightning page tabs, canvaas apps, visualforce tabs.

Each app in Lightning Experience has a horizontal navigation bar. This is used to access the items and finctionality in the app. It can be customized to fit user needs. 

- Apps can be created and customized via the ```App Manager in Setup```.
- The Navigation Items can be rearanged and picked; a utility bar can be enabled as well.
- The Interface / ```color and logo can be customized``` for each app.
- These apps can be ```assigned to user profiles```.

The ```App Manager``` is used to ```view, create, and customize``` apps in the organization. Salesforce apps can be personalized to match aspects of their companies' branding (logo, hightlight colors). 

The ```Utility Bar``` allows easy ```access to common productivity tools``` such as Notes, History, Calculator, and Omnichannel.

```Temporary tabs``` are opened when a user clicks an item that ```does not have a parent object``` placed in the navigation bar. These are visible when you click on a nav bar item (look for the '+') These can be used to access relevant items from the nav bar. Can be set as a permanent 'tab'.

## Lightning Experience App Launcher
The App Launcher allows users to ```switch between apps```. The apps that appear in the app launcher can be changed via ```App Menu in Setup```. Users can ```open or search for``` an app after clicking on the App Launcher icon. The apps visible in the App Launcher depend on ```each app's visibility settings and user permissions```. These can be addressed via profil and permission sets. App tiles can be dragged and sorted. Apps show as ```large tiles under 'All Apps' ```; custom objects, tasks, events, and the feed show up ```under 'All Items'```. 

The ```App Menu``` in Settings can be used to show the visibility in the App Launcher. 

## Lightning Experience Themes
Custom images and themes are availabe. Admins can choose from ```build-in themes``` ('Lightning Blue' is the default theme). Themes don't apply to mobile apps. Custom themes can be created to include brand logo, brand colors, background, and banner images. Themes apply to the entire org and can only have 1 active at a time. Apps can override a ```custom theme's brand image and nav bar color```. 

Custom themes can be ```created, previewed, and activated``` from the Setup page. Other options for customization include ```Background, banner, and default avatar imaes```. 

## In-App Guidance
Can be used to create hands-on ```interactive tour``` to guide users with ```step-by-step-prompts```. These can be placed on ```Object record pages, Support setup pages, List view dropdown menu, Record tabs and subtabs, etc```. 

Found in ```In-App Guidance``` under ```User Engagement``` in Setup.

The ```Manage Prompts``` permission is needed. A ```myTrailhead``` subscription is required so users can be assigned the permission to view ```more than three custom walktrhoughs```.

There are three prompt types: ```floating```, ```docked```, and ```targeted```. Where on the page the prompt appear is also a option. You can also add still images and animated .gifs. Existing in-app guidance can be assigned to a specific rcord type.

It is also possible to create ```direct links``` to prompts and walkthroughs. The URL can also be attached to the help menu or help documents. Note that if the API name of the guidance is changed, the URL will also change. The link can be found either from ```the Settings from inide the In-App Guidance Builder on the Details dialog``` or ```from the row-level action menu on the In-App Guidance Setup page```.

## Guidance Center
The ```Guidance Center``` guies admins in setting up and enhancing the Salesforce org and provides ```recommendations``` tailored for the org and the admin's level of experience. The Guidance Center can be accessed next to your profile picture with the 'trail' looking buttons that has mountains.

# UI Features: Search Settings

## Seach Overview
Admins can configure the search results of ```global search``` and ```lookup search```.

- Global Search Results - the results that appear when searching the global search bar at the top.
- Lookup Search Results - results when using the search on the lookup fields of a record

Each search type searches a unique set of fields for each object. Encrypted, formula, and lookup fields cannot be searched. Field-level security if enforced when users search for records. Search results do not override field-level security. Data in restricted fields do not return in the results. ```Records in search results depend on whether that the objects type and fields are accessible```. Lists of records can also be searched using the ```list view search bar```.

## Global Search
The global search box ```displays a list of auto-suggested records``` for multiple object types as it is typed into. This provides instant results ```before performing a full search```. You can also get ```recently viewed items``` that match the search term when a user clicks into the search box.

The ```Suggested Records``` lists ```up to five records``` with name matches. ```Full search``` searches ```across searchable objects``` and takes the user to the 'Top Results' page. ```Full Object-Specific Search``` searches ```within the current object``` and takes the user to the object's search results page. The ```Limit search to``` option can be selected to ```limit the search to an object``` entered in the search box.

## Lookup Search
Lookup Search allows a user to search for a record of an object and associate it to a record of another object using a lookup field. This can be found for example, when adding a record and looking for an account name to add - the auto populated info is using lookup search.

- Lookup Fields - used to ```associate two records``` together in a relationship.
- Instant Results - when they type in a lookup field, you see a ```dynamic list of suggested matches instantly```.
- Search Term - instant results match to the records name, but a full search can be performed.
- Secondary Field - if configured, a secondary field is displayed under the primary record name that provides more contextual info.

```Lookup Filters``` and ```dependent lookups``` can be configured to make the lookup search results more relevant.

- Lookup Filters - ```restrict the valid values and lookup dialog results``` for relationship fields.
- Dependent Lookups - A lookup field that ```includes a lookup filter that references fields``` on the source object record.

## List View Search
```ONLY the first 2000 records are searched```. To get around this, use more specific terms or change the filters / sorting order.

Federated Search - configuring this will allow users to ```search data stored in extrnal repositories``` from the Salesforce interface.

- External Search - users can use global search to see external results.
- Partner Providers - Salesforce has partnered services to make it easy to connect to external search providers.
- Setup In Experience Cloud Sites - Federated search can be configured in ```Experience Cloud sites```.

## Search Layouts
The ```Search Layout``` dtermines which fields users can ```view, filter on, and sort by``` on the search results page for global / lookup search. 

- Setup - Search Layout of an object can be configured to select the fields that should be shown as columns on the search results page.
- Secondary Field - Secondary field is always the related account for contacts and opportunities.
- Object-specific Layout - Search layouts can be created for individual objects.

Search layout allows the following to be customized: fields in a ```record's instant results``` preview, fields that can be ```filtered```, fields shown in a ```recommended result```, and ```secondary fields``` in instant results.

Search layout cann be configured from ```Setup Menu``` or ```Object Manager```.

Record search results columns are displayed and arranged ```according to the object search layout``` assigned to a user profile.

## Einstein Search [Trailhead Link](https://trailhead.salesforce.com/content/learn/modules/einstein-search-increased-productivity)
Enabled by default and provides features like ```search personalization, natural language search, and instant actionable results```. 

- Search Personalization - search results are based on records most relevant to the user, the records they use most. Results are reordered to be most relevant to you.
- Instant Actionable Results - suggested searches and record previews are immediately seen. Hovering over these instant results also provides previews of these records. Actions buttons also show up to let you follow or edit these accounts from the search.
- Natural Language Search (NLS) - common words / phrases can be used as search terms which are turned into usable search filters.

```Search Manager``` can be accessed in Setup to ```view all searchable objects``` and the ```search status of each field```. 

EINSTEING DOES NOT discard results or filter them away.

Personalization is currently available on Accounts, Cases, Contacts, Leads, and Opportunities. 
Natural language search currently works on Accounts, Cases, Contacts, Opportunities, and Leads.

# UI Features: List Views

Summary of records can be displayed in a single view on that objects home page. To do this, we have ```List Views``` (a list or summary of records that meet a defined criteria) and ```Kanban View``` (shows a graphical view of records in a list view). 

## UI Features: List Views
Salesforce groups data by object types, such as Contacts or Cases. An object tab contains a data table and a toolbar of action buttons - this is the list view. Rows begin to fill in as new data is added to the org. You can also customize the views which provides a lot of power. Other users can be given the ability to ```create public list views```. The user needs the ```Manage Public List views``` permission.

Remember that sharing rules apply to list views as well. List views can show any field associated with the object. You can pin the list view that you use the most often (this affects your instance only). Certain list views let you do different things (e.g. in Contacts you can send emails to selected contacts). 

The default view shows up to 50 records. Scrolling will show more. Up to 15 different fields can be displayed. To apply a bulk action to every record in a list (even those not seen), click the bulk action button without selecting any records. To apply bulk action to all records in the current view, check the table header checkbox. For specific records, click on the individual boxes.

The default pinned list for all objects is ```Recently Viewed```. Any view can be pinned as the default. The send email action is available for Contacts, Leads, and Compaign. 

Users can switch list view display to split view. This will allow users to ```efficiently work with multiple records from a list``` without going back and forth to the list view page. 

    Q. What's the first step to take to create a list view? 
    A. Open the List View Controls menu.

    Q. To take bulk actions on all records in a list view, you click the bulk action button without selecting any records. 
    A. True.

    Q. True or False: A list view can be shred?
    A. True.
    
List Views have the followwing features:
1. List View Search Bar
2. Show Charts - display data as a chart
3. Charts - can be added to a list view
4. Kanban View
5. Inline Editing
6. Filters
7. Import
8. List Email - send emails

In ```Settings``` under ```List View Button Layout```, you can add buttons and actions to the ```List View Search Layout``` so that they appear in the objects list views.

To Create a custom list view:
1. Create and name a new list view or clone an existing list view. 
2. Select the List View sharing.
3. Add List View filters.
4. Select the fields to display.
5. Opionally create a list view chart.
6. Use Sharing Settings to adjust visibility if required. 

## UI Features: Kanban View
The Kanban view is aa list view presented as a ```visual summary for a selection of records```. 

- List View - records are based on the selected list view.
- Record Type - records are separated based on record type.
- Fields - fields on which columns and summaries should be created.
- Search Bar - search records
- Availability - available for most objects in Lightning Experience.

Opportunity deal change highlights can be used to show recent changes to amounts and close dates in the Kanban view. This feature is also available in list views. Feature can be turned on or off from the Opportunity Settings page in Setup. Text colors and arrows can indicate amounts and close dates that changed during the last 7 days. Users can hover over an arrow to view details.This feature is only available in Lightning Experience in Unlimited Edition.

# UI Features: Lightning App Builder
## Lightning App Builder [Trailhead Link](https://trailhead.salesforce.com/content/learn/modules/lightning_app_builder)
The Lightningn App Builder is a one-stop shop, point and click tool that can be used to customize Lightning Apps. It allows you to customize apps with custom components based on need. Lightning App Builder can be used to manage Lightning app settings such as branding, navigation, options, and the Lightning pages assigned to that app.

Standard, custom, and third-party components (e.g. AppExchange) can be added to a Lightning page using the ```Lightning App Builder```. Some components are only available based on the Lightning page type. For example, the Record Detail component can only be added to Lightning Record Pages. 

Lightning App Builder can be used to customize:

- Lightning Apps
- Lightning Pages
- Visibility Rules - Lightning app, home, and record pages can be made dynamic by setting visibility rules for components. Related fieldss and other objects can be included in visibility rules.
- Component Visibility - can be based on standard or custom user permissions.
- Collapsible Sections - components can be groouped into collapsible sections using the Accordion component. There can be up to 25 sections.
- Pinned Regions - can be created for console apps. These remain displayed as a user navigatees to subtabs in Lightning console app.

Some additional notes:
- The ‘Pages’ menucan be used to navigate and edit the pages of a Lightning app.
- Component visibility rules can be set for app, record, and home pages by defining filters.
- A page can be made dynamic by configuring the component visibility filters based on the permissions of the person viewing the page.
- Components can be grouped into collapsible sections using the ‘Accordion’ component.
- Pinned region pages can be created for Console Apps.

## Dynamic Interactions
Dynamic Interactions enable Lightning web components (source) to ```communicate with other custom Lightning components (target) that exist on the same Lightning App page. Programmatic customiztion is required for configuring a Lightning web componenet as a source, Lightning App Builder is used to specifying target components. 

When a (source) component has been configured for dynamic interactions, an Interactions tab will appear in its properties panel in Lightning App Builder. This tab lists the interactions, or available events, “exposed” by the source component. To target a component for a specific event, the Add Interaction button is clicked. Clicking on the ```Add Interactions``` button opens up the Interaction Details tab for the selected event. The Interaction Details tab is used to define the target component and data (property values) that will be communicated in the interaction. It also shows the name of the source component and event, as well as the type of interaction between the source and target components.A static value or an expression can be used to define the value of the property. 

## UI Features: Homepage Layouts
This is the first page displayed to a user and can be customized using the ```Lightning App Builder```. A home page layout can be set as the org default or it can be customized and assigned to app or app and profile combos. 

## UI Features: Creating a Lightning Home Page
The Lightning App Builder is used to create a new Home Page. The steps include:

1. Create a new Home page or clone and exisiting Home page.
2. Select a standard or custom template.
3. Add componenets to the layout.
4. Optionally set component visibility. 
5. Activate the Home page.
6. Set as default for Org, App or App/Profile combo.

Visibility filters can be set for components on Lightning app and home pages to make them dynamic. For example, component visibility filter can be based on a field on the User object, such as 'Country'. Custom labels can be localized. The expression {!$Label.customLabelName} allows users to see labels in a chosen language, if a translation is created for that label in that language. Dynamic Actions can be used to dynamically control the visibility of Action buttons on a record page based on the values on the record. It helps in keeping the record page neat and streamlined.

When you edit a page for the first time, Salesforce makes a copy of the standard page. This copy is what you can customize in the Lightning App Builder. Custom home pages can be assigned as org default, app default, or per app and profile combinations. The Standard Home page can be restored by selecting the System Default.

## Lightning Page Performance
Helps with monitoring adoption metrics and page performance. You can see ```daily user activity data``` and ```browser usage and page performance data```.

The ```Lightning page analysis tool``` in the App Builder calculates the page performance of a Lightning Record Page. It also identifies the components that have the most impact on page load time. You can analyze performance based on Desktop/Phone. It will show the page load time. If possible, you can see which componenets take longest to load which thus should be moved to non-default taabs, or in an accordion (to improve page performance).

When a custom Lightning component is added to a Lightning Record Page, the analysis tool may provideinsights and recommendations related to the custom componentto improve page performance.

# UI Features: App Menu
## App Menu
Each app has a horizontal navigation bar to access items and functionality in the app. The navigation bar can be customized to include custom colors and branding. It can be used to access lightning apps containing lightning components. More nav items can be added to the menu and items can be reordered by draggiing the tabs around where you want them. 

Users can rename / remove navigation items except for the ones added by the Admin by default. This accomplished in the ```app navigation items edit page```.

## App Manager
All apps in an org can be viewed and managed in the App Manager, including the app menu configuration. The App Manager is found under ```Settings -> App Manager```. A tab must exit for a Lightning component or page in order to add it to an app in Salesforce or the navigation menu. This is automatically creeated when a Lighhtning page is built and activated using the Lightning App Builder.

Lightning apps can be configured to support desktop, phone, or both devices. They can be personalized depending on the navigation style. Utility items can also be added here. You can also add additional navigation items and assign the app to user profiles.

# Global Actions

There are a number of different kinds of actions available in Salesforce:

- Global Actions - actions that are available in places like the home page; allow action types such as create a record and log a call.
- Object-Specific Actions - allow creating a record that is related to the object.
- Action Layout Editor - fields can be added, removed, or reordered using the action layout editor for an object-specific action.

## Quick Action Overview
Actions are availble on the Salesforce mobil app landing page as well as different objects. Types include:
1. Standard Publisher Actions - actions automatically included when Chatter is enabled (e.g. Post, File, Link). Standard actions require enabling of feed tracking per object.
2. Cutsom Action - ones you've created. Can be global or object-specific. Can also invoke lightning components, flows, VF pages, or canvas app. 
3. Default Actions - ```predefined by Salesforce``` per object (New Contact, New Task, etc.). 
4. Mobile Smart Actions - ```preconfigured just like Default actions```. 
5. Productivity Actions - ```predefined by Salesforce and attached to a limited set of objects (e.g. Send Email, Log a Call, View Website). 

Types of Quick Actions:

Global:
- have ```no automatic``` relationship with any record.
- can be found on the (+) icon in the Salesforce header. 
- e.g. Create Actions, Log a Call, Custom Actions

Object-Specific:
- ```Automatically associated``` with related records.
- can be found on the ```record detail page``` of a specific object.
- e.g. Create Actions, Log a Call, Update Actions, Custom Actions.

## Global Actions
These actions can be added to any page that supports actions. Some notes:
- Record Creation - allows creation of object records.
- Configuration - defined in ```Setup > Global Action```.
- Object Relationship - there is ```no automatic relationship``` between records that's created and any other record.
- Accessibility - available from the ```home``` page, ```Chatter tab```, Chatter groups, ```object pages```, and custom ```Lightning app pages```. 

Actions types include:
- Create a Record
- Send Email
- Log a Call
- Custom Visualforce
- Custom Canvas
- Lightning Component

Global Actions can be accessed by clicking on the ```Global Actions Menu``` which i the '+' icon in the Salesforce Header (near your profile icon). In mobile, it can be accessed in the ```action bar``` on the ```Feed``` and ```People``` pages.

Global Actions can be created to perform any of the following: Create standard object, create custom object, log a call, send an email, display vp page, display custom canvaas, launch a lightning component.

‘Create a Record’ action can be used by users to create supported object records without leaving the page they are on.

Global actions have layouts of their own called global publisher layouts. A global publisher layout is not associated to any object. If an object page layout is not customized with actions, the actions on those object record pages are inherited from the global publisher layout.

Global Publisher Layouts - position nof the actions can be customized from: Setup, User Interface, Global Actions, Publisher Layouts. Global Publisher Layouts can be assigned by profile. 

After a Mass Quick Action is set up, up to 100 records can be selected in a list view and perform mass updates in Lightning Experience. Mass quick actions cannot be performed on a Recently Viewed list.

## Dynamic Actions
Dynamic Actions can be used to dynamically control the visibility of Action buttons on a record page, based on the values on the record. Actions can thus be set to only appear when values of fields match a certain critria.

## Object-Specific Actions
Object-specific actions are used to quickly create or update records, log calls, etc. in regards to a particular object. The location of actions for the mobile app can be customized in the object's ```page layout editor```. The layout of an action determines the fields that will be displayed. 

When a action is created, there is always a ```corresponding layout``` that can be customized based on requirements. Fields can be added, removed, or reordered on the action layout. In order to display the action in the user interface, it needs to be added to the Publisher Actions section of the objects’ page layout.

The ‘Override global publisher layout’ option must be ticked when adding new object-specific actions for the first time on an object’s page layout. This option will allow the users to set a customized list of actions on Lightning Experience and mobile app pages.

Object-Specific actions layout can be configured from: Setup, Object Manager, (Object), Buttons, Links, and Actions.

## Scenarios & Solutions

SCENARIO: Support reps need to be able to launch a Visualforce page created by a developer from their home page.
SOLUTION: A global actioncan be created for this use case. The action type can be set as ‘Custom Visualforce’. The action can be added to the publisher layout to make it appear on the home page.

SCENARIO: When creating a related case from the account feed using the ‘New Case’ object-specific action, support reps should be able to enter only certain required fields.
SOLUTION: The action layoutfor the object-specific action can be edited for this use case. The fields can be added, reordered or removed according to requirements.

SCENARIO: A support representative should be able to send an email from the Chatter feed on the home page.
SOLUTION: 
- A global action with the action type 'Send an Email' can be created for this use case.
- This action can be added to the global publisher layout to ensure that it appears on the Chatter feed of the home page.

SCENARIO: An account manager who is using Salesforce mobile app when not in office is creating a new child account directly from an account record page. She wants to auto-populate fields such as ‘Website’ and ‘Account Number’ upon the click of a button.
SOLUTION: Create a new quick action called “New Child Account” where the predefined value for the Parent Account field of the target record is the Account ID of the source record. The ‘Website and ‘Account Number’ field values can be predefined according to the parent record.

# UI Features: Sandbox & Change Sets
## Sandboxes
A Sandbox is a copy of a production org and is linked to it. Initally, Sanboxes only contain metadata (but some can contain data records). They are used to develop and test in a safe environment. This ensures nothing affects the production environment. They type of sandbox will differ by storage limit, initial data, and refresh interval. Refreshing a sandbox happens when an existing sandbox is replaced with a new copy from production. This creates a new sandbox, but retains the original name. There is a limit on how often you can refresh.

There are 4 types of sandboxes:
1. Developer - used for development, configuration, and testing new functionality.
2. Developer Pro - development in which larger amounts of data are needed to test functionality; Integration from multiple developer sandboxes; quality assurance and user training.
3. Partial Copy - testing / training where a subset of the data is sufficient.
4. Full Copy - performance testing, load testing, and staging in an enviornment that is identical to production.

The type of sandbox can be elected when creating or refreshing a sandbox. 

Type                    Storage Limit                    Initial Data                      Refresh

Developer               200MB Data Storage              Configuration Only                  1 Day
                        200MB File Storage       

Developer Pro           1GB Data Storage                Configuration Only                  1 Day
                        1GB File Storage

Partial Copy            5GB Data Storage                Subset of data determined           5 Days
                        File Storage same               by template
                        as production

Full Copy               Same as Production              All data, but subset of             29 days
                                                        can be copied through a
                                                        sandbox template

Sandbox templates are required in partial copy sandboxes to specify which data to copy over.

## Deployment Options














## Change Sets