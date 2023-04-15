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

















## User Maintenance
## Scenarios & Solutions
























# Organization Security Controls
# Apply Security Controls
# Custom Profiles and Permission Sets