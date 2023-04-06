## Configuration and Setup

### Company Settings

#### Locale
Locale controls how different values are displayed (e.g. data dn time, address, currency, name, and number fields). The ```Company Information Page``` controls company-wide defaults and new users will use these default settings. However, users can OVERRIDE company default settings via ```Language and Time Zone settings``` in user's personal settings.

#### Language Settings
Language settings define the ```default language``` of the org and the languages the user will be able to use in their personal settings. There are 3 levels of language support: fully supported, end user, and platform languages. The default language is set on the Company Info page and applies to new users. The ```Translation Workbench``` allows translations to be applied to custom fields, labels, etc.

    1. Fully Supported - mean all Salesforce featuers, including User Interface, Setup, and Help will display in that language. Total 18 supported.
    2. End User - languages will have translations for all standard object field labels and pages, but not Setup and Help. Total 17.
    3. Possible to provide translations for customizationss and standard fields. Fallback is English is translations are not provided. Total +100.

The ```Default Language``` will be the language used in the org.

User can change their display language via -> my settings -> personal -> language & time zone. 

If you want other languages enabled, they must be enabled in ```Language Settings``` before they can be selected.


- Time Zone
- Currencies
- Business Hours and Holidays
- Organization ID
- Licenses
- Storage
- Fiscal Year