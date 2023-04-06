# Configuration and Setup

## Company Settings

### Locale
Locale controls how different values are displayed (e.g. data dn time, address, currency, name, and number fields). The ```Company Information Page``` controls company-wide defaults and new users will use these default settings. However, users can OVERRIDE company default settings via ```Language and Time Zone settings``` in user's personal settings.

### Language Settings
Language settings define the ```default language``` of the org and the languages the user will be able to use in their personal settings. There are 3 levels of language support: fully supported, end user, and platform languages. The default language is set on the Company Info page and applies to new users. The ```Translation Workbench``` allows translations to be applied to custom fields, labels, etc.

1. Fully Supported - mean all Salesforce featuers, including User Interface, Setup, and Help will display in that language. Total 18 supported.
2. End User - languages will have translations for all standard object field labels and pages, but not Setup and Help. Total 17.
3. Platform - Possible to provide translations for customizationss and standard fields. Fallback is English is translations are not provided. Total +100.

The ```Default Language``` will be the language used in the org.

User can change their display language via -> my settings -> personal -> language & time zone. 

If you want other languages enabled, they must be enabled in ```Language Settings``` before they can be selected.

### Organization ID
The Org ID is a 15 character identifier that uniquely identifies each Salesforce org. It is found in the ```Company Information``` page. It will be different accross enviornments (e.g. Dev, Test, Production). 

### Licenses
Licenses (type) define what features/services are available to an org. There are three different license types:

1. ```User Licenses``` - define the baseline of features available to a user; each user needs a license.
2. ```Feature Licenses``` - grant access to additional features not included in standard licenses (e.g. Marketing, Knowledge, CRM content).
3. ```Permission Set Licenses``` - gradually grant users access to select features not included in their user license.

License information can be found on the ```Company Information``` page.

### Salesforce API
Abbreviation for Application Programmin Interface. This allows access to Salesforce programmatically (e.g. data loader, Informatica, integrations with other systems). There are limits to the number of requests that can be made in a 24 hour time period and is based on the edition and number of user licenses. Available for Enterprise, Unlimited, Developer, and Performance editions.

### Time Zone
The time and date fields will display based on the time zone settings. The Org's time zone is set on the ```Company Information page``` and is used as the default for new users. Users can set their own time zone and override the org's settings.

### Currencies
Orgs can have a single currency or multiple currencies. 

Single Currencies:
- set for the organization via the ```Company Information``` page using the ```Currency Locale```.
- this also controls the currency symbol.
- this is the default

Multiple Currencies:
- adds the ability to record amounts in different currencies on the records.
- must be enabled on the ```Company Information``` page.
- in multi-currency orgs, the corporate currency is ```defined```.

Multiple Currencies is enabled by the System Admin. Currencies must be made active to be used. Reporting and forcating can be done in the ```record currency``` and ```corporate currency```. Users can also set their individual currency in the ```Personal Information``` page. These can be used in reports, quotes, forecaasts, and other records that use currency amounts. Exchange rates can be set on the ```Manage Currencies``` page. Dated exchange ratees can be used by enabling ```Advanced Currency Management```. This allows for the tracking of the exchange rate at the ```date opportunities close```.

Reports also support multiple currencies, classified as primary or secondary currency. The primary currency reflects either the default corporate currencyor the currency selected for the record. They secondary currency reflects the personal default currency of the user or the currency specified in the report criteria.

MULTIPLE CURRENCIES CANNOT BE DISABLED AFTER BEING ENABLED. Enabling can increase the compile size of formulas.

### Business Hours and Holidays
Business hours determine when users are available to support customers and are the basis for computing the support processes hours. ```Multiple Business Hours``` can be defined with one as the default. These can be specified in a case record to define when the support team is available to help customers. Holidays will be excluded from the time used when calculating a case escalation. 

Found under:
    Company Settings -> Business Hours

### Fiscal Year
The ```Fiscal year``` defines the ```business year of the company``` and can be ```Standard``` or ```Custom```. The standard fiscal year follows the ```Gregorian calendar``` and can be configured to start on the first day of ```any month``` and can be named for the starting or ending year. The custom fiscal year can use ```custom periods``` and can be bassed on existing template or an exiting template can be modified. Fiscal year can be based on either the starting or ending month of the period.

Custom Fiscal Year Templates include adding 4 quarters per year, 13 weeks per quarter, or 13 periods per year. Using custom fiscal years will impact ```forecasting, reports, and quotas```. 

IF A CUSTOM FISCAL YEAR IS ENABLED, IT CANNOT BE REVERTED BACK TO STANDARD. However, standard fiscal years can be replicated by choosing the Gregorian calendar.

Custom Fiscal Year editing occurs in the ```Fiscal Year``` page under Setup. After picking a fiscal year structure, you can enter the start date, name, description, week start day. Additional customization can be done by ```adding or removing fiscal periods``` and by ```changing the length of a fiscal week```. Templates can also be reset by selecting a different structure base. It can be previewed before saving.

Enabling / defining custom fiscal years impacts ```forecasts```, ```reports```, and ```quotas```.

Custom fiscal year ranges appear in ```report filters```.


- Storage
- Fiscal Year