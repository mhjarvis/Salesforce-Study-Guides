<h1 style="text-align: center; font-size: 40px">Configuration and Setup III</h1>

# Setup and Maintenance of Users
Each Salesforce user has their own user record where personalized settings are established. The assigned profile determines their access to objects in addition to what privileges they have. On these user records, user licenses are assigned. Feature licences can be assigned for items such as Marketing, Knowledge, or Mobile User. Users are permanent records that ```cannot be deleted```. Instead, you can ```deactivate``` or ```freeze``` a user.

Key Words:
- User Details - last name, email, username, user license, and profile are required.
- User License - determines the level of access to the org and what profile can be selected for a particular user. 
- Feature License - provides access to additional features not included in a user license.
- Resetting Password - done by user or admin.
- Unlocking User Accounts - unlocked by admin.
- Localization - locale settings like language, time zone, and currency can be specified on a user's record.

## User Creation
Creating a new user includes the following components: user details, user license, feature license, role, profile, localization. Each user is uniquely identified by the information added when the user is setup. This includes a unique username, which is unique across all Salesforce orgs and cannot be reused. Usernames must be in email format, but do not need to be a valid email. User role is marked as required, but ```does not need to be selected``` to create a new user.

To complete the setup process, the following steps need to be done:
    An account verification link sent via email is clicked -> new password created -> security question created.

New user required fields include:
- Last Name
- Alias
- Nickname
- Email
- Username
- User License
- Profile

The email domains in a user's email field can be restricted. ```Email Domain Allowlist``` can be enabled via ```User Management Settings``` in Setup. This allows you to restrict the allowed email domains. 

The account verification link sent to new users will expire after 7 days (by default). When clicked on, a new user will be prompted to set a new password. If not done, the process will need to be repeated. Before an admin-initiated email update is approved, a user is required to reset their password even if the ‘Generate new password and notify user immediately’ setting is not enabled, to ensure the security of the org. A password reset link is sent to the new email address to activate the new email address. 

Multiple users (up to 10) can be added at one time. The ```Add Multiple Users``` button is available from the Manage Users Screen. When this is done, all users will have the same license assigned. The ```username will be the same as the email address``` when adding users this way. These records will need to be edited after user creation for individual details. 

Users can also be created in ```batch``` using the Data Loader application. Required fields should be included in the import file. The Insert operation will need to be used. Proper picklist values should be used. 

## License
There are three types of licenses: user license, feature license, permission set license. The user license must be selected to determine the level of access to the org and which profiles can be selected. Feature license allow for additional access. Permission set licenses can be used to assign users specific settings and permissions to use various tools and functions. 

Locale settings are set via the company profile and can be overridden on the user record: locale, time zone, language, currency. 

## User Maintenance
The ```Login History``` page provides information on past login attempts. It providess the following information: 
- Login Status - will indicate success or reason for failure to login.
- List View - can be viewed as a related list.
- Maximum Record Size - ```shows up to 20,000 login records for the past 6 months```.
- Saved File Format - can be downloaded as a ```CSV or GZIP file```.
- Troubleshooting - can be used to troubleshoot why a user cannot login.
- API Access Record - API access logins will be included in All Logins option.

Multiple passwords can be reset at a time if needed.

Admins can see in the ```User detail section``` how many ```failed login attempts``` a user has. If the max is reached, they are locked out. Admins can unlock and unfreeze accounts from a user's details page. A user's account is frozen after too many login attempts. The ```freeze``` feature can also be used to ```prevent user access``` to the org. This is an immediate action that prevents them from logging in and having access. No emails/alerts are sent. The license is not released when a account is frozen. To release a license, the user must be deactivated.

** Users ```cannot be deactivated``` if they are the sole recipient of a Workflow Email Alert, Customer Portal Administrator, or User selected in a Custom Hierarchy Field.

A user can ```Self Deactivation``` if enabled to allow external Community and Chatter users deactivate their own accounts.

The System Admin can ```delegate certain admin tasks``` to delegated admins. A ```delegated group``` controls what ```admin privileges``` are granted. This is done by:
    Create delegated group -> Add users -> Assign capabilities

Users in a delegated group can: manage users (create and edit users in specific roles), assign profiles, unlock and reset passwords (for users in certain roles), manage permission sets, create public groups and assign users to specified public groups, and manage custom objects.

System Admins can ```log in as any user``` in the Setup menu under ```Login Access```. This feature can be turned on and off in: ```Setup -> Security Controls -> Login Access Policies```. If this setting is not enabled, each user needs to ```Grant Login Access``` from the ```Personal Setup menu```. 

Common issues that occur when loging in:
- Password is case sensitive
- Login hours are setup and user is outside of those times
- Inaccurate username
- Incorrect domain
- MyDomain policy
- Profile based IP restriction
- Unverified account
- Locked out

## Scenarios & Solutions

SCENARIO: A new Salesforce Administrator is required to create a user record for a sales representative in Salesforce. He needs to get all the necessary details from the user to create the record, but he is not sure which details he should ask the user to provide.
SOLUTION: To create a new user record, the required fields are Last Name, Alias, Nickname, Email, Username, User License, and Profile. The administrator should get the user’s full name, email address, unique username, alias, and nickname. The user license and profile should be selected based on what the user should be able to do in Salesforce. A role can be selected if a role hierarchy has been defined in Salesforce.


SCENARIO: A user in the marketing department of Cosmic Solutions recently started using Salesforce. She is able to view campaigns, but she also needs the ability to create, edit, and delete campaign records in Salesforce.
SOLUTION: The administrator of the company should edit the user record of the user and select the ‘Marketing User’ checkbox to assign a feature license to the user that would allow her to create, edit, and delete Campaign records. A feature license is assigned to provide access to additional features that are not available via the user license.


SCENARIO: A support agent who uses Salesforce wants to see the text of standards tabs and fields in Italian. In addition, he would like to see the Event Start/End Time in calendar entries and events based on the Italian time zone instead of the default Eastern Standard Time.
SOLUTION: The user record of the support agent can be edited for this requirement. In the Locale Settings section, the Language and Time Zone can be changed according to his requirement.


SCENARIO: A sales rep of Cosmic Electronics has sent a message to the company’s system administrator saying that she sees an error while trying to log in. The administrator would like to view her past login attempts to determine the reason.
SOLUTION The administrator can navigate to the ‘Login History’ page in Setup to view the sales rep’s past login attempts. The ‘Status’ of the recent login attempts should be checked to determine why she sees an error while trying to log in.


SCENARIO: A support rep of Cosmic Service Solutions has been locked out of Salesforce due to too many failed login attempts. The administrator of the company needs to allow her to access Salesforce using a new password.
SOLUTION: The administrator should unlock the user’s account by navigating to the user detail page and clicking the ‘Unlock’ button. To allow the user to set a new password, the ‘Reset Password’ button should be clicked, which sends an email to the user with a link to set a new password.

SCENARIO: A Salesforce developer of Cosmic Solutions who regularly uses multiple Salesforce orgs, including test and production environments, is unable to access the company’s production org. He is certain that he’s using the correct username and password, which he has used several times in the past.
SOLUTION: Since the developer accesses multiple Salesforce orgs, it is possible that he is using test.salesforce.com instead of login.salesforce.com to access the company’s production org. The administrator should inform the developer about this possibility. If the company is using My Domain, the link should be shared with the user.

# Organization Security Controls
Salesforce provides several ways to control org access. There are 4 levels of Security:
1. Organization Security Controls - login hours, ip restrictions, password policies.
2. Objects - profiles, permission sets.
3. Object Record - org-wide defaults, role hierarchy, sharing, teams.
4. Fields on a Record - field-level security, page layouts.

## Setup Audit Trail
The ```View Setup Audit Trail``` screen is located in Setup. This helps track setup changes that admins have made to the org, which helps if there are multiple admins. If a delegated user makes a setup change, the ```Delegate User column``` shows their username. This shows the ```20 most recent setup changes``` and stores audit trail history for the last 6 months. This can be ```downloaded for the last 6 months``` (excel csv).

Changes tracked include who made those changes, date of change, and what was changed. Some things trackd include:
- Amin-related changes such as Company info, defult settings, roles, users, permission sets, etc.
- Customization changes such as workflow rules, approval processes, flows, page layouts, custom objects, etc.
- Groups and Sharing such as changes to public groups, sharing rules, org-wide settings, etc.
- Data Management changes such as use of Data Import Wizard, exporting data, deletion of records, etc.
- Email Deliverability and Delivery changes such as access level, PIN length, inactivity timeout, email relay, etc.
- Delegated Admin setup changes.
- Notification types delivery setting changes.
- Apex changes such as class creation, triggers, VF pages, lightning pages, etc.
- Lightning Component changes (create, change, delete components).

## Passwords
### Passwords
Each user has a unique username/password. The admin can ensure these are strong and secure through password policies, password expiration, password resets, and Login Attempts / Lockout Periods. 

Password Policies govern ```login and password specifications```. Passwords cannot contain a user's username and cant match their first or last name. Password restrictions and lockout policies can be changed as needed and can apply at the org level or profile level. Changes to org-wide password policies do not affect profile-specific password policies. 

There are default password reqs for new orgs that can be modified except for the Personal Edition. These include a minimum length of ```at least eight characters, including one alphabetic character and one number```, the security question answer cannot contain the password, and a user cannot reuse their last 3 passwords. Password expiration time an also be set. The default for this is ```90 days```, but it can be set to 30, 60, 90, 180, 1 year, or never expires.

Password Policies can specify login attempts and lockout periods. For invalid login attempts, you can set it to 3, 5, 10, or no limit. The length a user is locked out can also be set to 15 minutes, 30 minutes, 60 minutes, or forever.

Password setting modification can improve security:
- Password question requirement - can be set to not contain password.
- Obscure secret answer for password resets - this hides the text when the user types security answer.
- Password complexity requirement - enforce a certain combination of characters.
- Minimum password length - can be set between 5 and 50 characters.
- Require a minimum 1 day password lifetime - users are not allowed to change password more than once a day.
- Enfoce password history - number of passwords remembered (none to 24). 

There are some things to consider when resetting passswords:
- When email is changed, the password is also reset.
- Reset Password on the 'Users' page can reset all or select passwords.
- A automatic email is generated when there is a password reset.
- ```Reseting a locked account user's password automatically unlocks the account.```

### User Authentication
There are several ways to authenticate users:

- Single Sign-On. Allows users in the org to login with other applications ```using single user credentials``` with an external provider. This removes the need to login to every single application every time. Only one password is needed this way. Can be used to standardize authentication. Federated Authentication or Delegated Authentication can be used. Increases use and efficiency. Also reduces risk of numerous logins.
    
    - Federated Authentication. Allows affiliated but unrelated service providers to share authentication data using SAML assertions. Salesforce can be the identity provider, service provider, or both. Automatically enabled for an org.
    - Delegated Authentication. Allows authentication using credentials from an external authentication provider wrapped in a web service. Uses a strong form of user authentication and makes the login page private and accessible only behind a corporate firewall. Enabled via ```Setup -> Single Sign-On Settings```. 
    
- Multi-Factor Authentication. Increases an Org's security. Can be service-based or policy-based. Second factor may be the mobile authenticator app, or they can use WebAuthn or U2F security keys. Some considerations:

    - Users who log in through an authentication provider that supports Single Sign-On are not subject to multi-factor authentication by default.
    - MFA can be enforced (Session Security Level Required at Login = High Assurance).
    - Salesforce support users, partner support users, and subscribers with high-assurance sessions can log in asother users without triggering the multi-factor authentication (MFA) challenge. The Multi-Factor Authentication for UI Logins During Log In As setting is disabled by default.
    - Multi-factor authentication (MFA) can be enabled for all the users in an org by selecting a setting. This org-wide setting is the quickest way of satisfying the MFA requirement and will be used by Salesforce to automatically enable and enforce MFA in the future.
    - To enable MFA for all the users, Require multi-factor authentication (MFA) for all direct UI logins to your Salesforce org can be enabled on the Identity Verification or Session Settings page in Setup.
    - To enforce MFA challenges for users, Session Security Level Required at Login can be set to High Assurance in their profile
    - An administrator must ensure that Multi-Factor Authentication is in the High Assurance column on the Session Settings page in Setup.

## Session Settings
You can configure the ```session connection type, timeout restrictions, and IP address ranges``` in Setup. The Session Security Settings can be configured at the org and profile level. Profile settings over-ride org-wide settings. Session Settings will be available in a user profile if using the enghanced profile interface. 

At the Org-Wide Session Settings, you can set the ```session timeout``` to happen after a set amount of time. You can also disable the session timeout warning popup. It is also possible to force logout on session timeout. User sessions can be locked to the IP address from where they originated or the domain in which they were first used. Salesforce requires HTTPS for connections to third-party domains. POST requests can be used for cross-domain sessions. Login IP ranges can be enforced on every request. Some other notes:

    - Secure and persistent browser caching can be enabled to improve performance.Caching and autocomplete on the login pagecan also be enabled. CDN can be enabled for theLightning Component Framework
    - Protection against clickjacking, also called UI redress attack, can be enabled for customVisualforce pageswithstandard headersand withheaders disabled.
    - XSSandContent Sniffing protection can be enabled. Thesite’s URL can be hidden from other websites in the referred header. Users can be warned before they’re redirected outside Salesforce.
    - Access to certain types of resources can be restricted based on thesecurity level (Standard or High Assurance) associated with theauthentication method, such as Username and Password
    - Policies can be set to requireHigh Assurance security level forreports,dashboards, andconnected apps. If the session isn’t High Assurance, access can beblockedorthesession level can be raised.
    - The Logout URL can be specified to redirect users to a certain page after they log out. The expiration timecan be selected for theaccount verification link in welcome emails to new users. All expired tabs can be redirected to a custom logout URL.

Session-based access control can be done using a permission set. If multiple permission sets need to be assigned for an activated user session, a permission set group can be assigned to users instead.

## IP Restrictions
Control org access via IP addresses, which can be set at the org-level or profile level. When enabled, logins from other IP addresses will deny access. For profiles, this option is found in the ```profile overview page```. When denied, the user is shown the same error message as when someone enters the wrong username/password. You can enforce login IP ranges on every request via the Session Settings. 

You can add trusted IP adresses at the org-level via Network Access in Setup. This allows users to login without receiving a login challenge (verifying their idenity). If login from outside this IP range, they are sent a activation code. An activation code is sent eveery time a user logs in from a device or browser that Salesforce does not recognize, regardless of IP address. If cookies have been deleted, they will be asked to verify their idenity. 

## Login Hours
Login hours can be set at the profile level, but not at he org-wide level. You can set the days and hours a profile can log in. The same error message is seen as when a user enters the wrong username/password. To prohibit users from logging in on a specific day, set ```'Start Time' to 12 AM and 'End Time' to End of Day (12AM)```. 

## Device Activation & Identity Verification
Device activation is another security layer. This is invoked when logging in from a unknown device and/or outside a trusted IP range. This is all based on browser cookies. They will be required to reactivate if cookies are deleted. Verification is done via ```the highest priority verification method available```, in the following order: 

    1. Salesforce Auth. Mobile App
    2. Built-in Authenticator
    3. U2f Security Key
    4. One-Time Password Generator
    5. SMS Text Message
    6. Email

A user is able to ```register a Built-In Authenticator such as Touch ID, Face ID, or Windows Hello``` to their account/mobile device. These use biometric data for identification. You can switch back to another verification mode (click on 'Having Trouble'). 

## Additional Security Controls
You can monitor login behavior and information using ```Login Forensics```. This is helpful when there is:
    - suspicious login activity
    - more than average number of logins
    - logins during non-business hours
    - logins using suspicious IP ranges

There is no user interface with Login Forensics. Track events using API objects LoginEvent and Platform Event Metrics. Login Forensics can be enabled in the ```Event Manager``` page in Setup. 

Security Health Check is another tool that can help identify and fix potential vulnerabilities in key areas of security settings. This can be found in 'Health Check' in Setup. Grades and scores are provided to meassure org security. Recommended actions are provided as are additional options.

### My Domain
My Domain is a feature that allows the creation of subdomains. Allows highlighting the brand of the company and making the org more secure. Helps manage login/authentication. It also allows you to add your brand to the domain name. This is also required for certain features such as SSO. 

My Domain can be routed through the Salesforce Edge Network to improve download times and org performance. 

## GDPR
GDPR is a data protection law defining how personal information of EU individuals needs to be handled. It regulates the processing, collection, storage, transfer, and usage of personal data about EU individuals. It is meant to carry high penalties, give people more control on how their data is collected, used, and stored, applies if an org contracts with someone in the EU (regardless of physical presence in the EU), applies to personal/sensitive data, and orgs should minimize what info is needed and stored. 

Data Protection - include encryption, data masking, event monitoring, sharing settings, field level security and session settings.
Data Classification Fields - owwner, field usage, data sensitivity and compliance categorization levels.
Data Retention - used to clasify and define how long data should be retained. 
Data Model - can be made compliant using data privacy objects and custom objects as needed.
Personal Data - any data that can identify an individual.
Sensitive Data - subcategory of personal data and needs higher protection.

GDPR Terms:
    Data Processor - processes data upon behalf of the data controller (This is Salesforce). 
    Data Controller - Salesforce customer that is responsible for managing customer ddata. 
    Data Subject - An individual data collected relates to. 

Key data must be handled according to these key principals:
1. Legitimate purpose - limited, explicit, an for a specific purpose.
2. Data deletion - delete if not required.
3. Secure - prevent access, disclosure, loss, destruction, or alteration.
4. Consent - freely given, can be revoked.
5. Accurate - accurate and up to date.
6. Accountable - record keeping and reporting on compliance.

Rights under GDPR:
1. Right of access.
2. Right of rectification - inaccurate or incomplete data must be rectified.
3. Right to be informed.
4. Right to erasure.
5. Right to restrict processing.
6. Right to data portability.
7. Right to object.
8. Rights of automated decision-making and profiling.

# Apply Security Control
Access to records is determined by access to the objects themselves (and then access to individual records). 



## Object Access




















## Record Access
## Field Access
## Role Hierarchy
## Manager Group Access
## Sharing Rules
## Manual Sharing
## Manual User Sharing
## Record Sharing Hierarchy
## Report and Dashboard Folders
## Other Sharing Options
## Scenarios


































# Custom Profiles and Permission Sets