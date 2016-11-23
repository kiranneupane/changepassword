# changepassword
Change password for bonitasoft 7 living application

This page will allow current logged in user to change their password. Please note No validation is done for the password match.

Login to Portal as administrator

Go to Resources and Import page-changePassLivingApp.zip
Go to Applications and import Application_Data.xml in the portal Application

Please make sure you change the following in the config file:

File: dynamic-permissions-checks.properties
Location:<Bonitahome>\setup\platform_conf\current\tenants\<tenantID>\tenant_portal

uncomment following lines

## UserPermissionRule
## Let the user access and modify only himself
GET|identity/user=[profile|Administrator, profile|Process manager, check|UserPermissionRule]
POST|identity/user=[profile|Administrator, check|UserPermissionRule]
PUT|identity/user=[profile|Administrator, profile|User, check|UserPermissionRule]

for version 7 please do setup.bat push from command prumpt to reflect changes in database and restart your engine.

