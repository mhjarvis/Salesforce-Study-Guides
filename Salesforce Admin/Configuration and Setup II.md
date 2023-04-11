<h1 style="text-align: center; font-size: 40px">Configuration and Setup II</h1>

# UI Features: UI Settings

## UI Settings
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



# UI Features: List Views

# UI Features: Lightning App Builder

# UI Features: App Menu

# UI Features: Sandbox & Change Sets



