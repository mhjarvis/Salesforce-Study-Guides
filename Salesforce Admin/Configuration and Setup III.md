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















# Organization Security Controls
# Apply Security Controls
# Custom Profiles and Permission Sets