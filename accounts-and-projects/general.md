# OSG User Support Internal Documentation

## Creating Accounts in OSG Connect

The account creation workflow for OSG Connect follows a fairly straightforward 
workflow:

1. Users enter through one of the Connect websites, e.g. www.osgconnect.net
2. The user creates a Globus ID
3. User applies for membership in the respective top-level connect project, 
e.g. `osg` for OSG Connect *with their Globus ID*
4. E-mail gets sent to "Manager"s and "Admin"s of the top-level connect project 
and a ticket gets created in FreshDesk
5. A designated OSG user support staff member contacts the user
6. The designated OSG user support staff member approves the user adds the 
user to the required project, e.g. osg.Biograph for members of Alex Feltus'
group at Clemson
7. If there is no sub-project available, the user will have request a project
to be created
8. Once every hour the user and project list is synced from Globus to a `json`
file on `service.ci-connect.net`
9. Puppet/heira will check the `json` file and creat missing users and groups 
as needed.

## Updating Accounts in OSG Connect

The only updates that need to be made to a user account are:

1. Change SSH key

Changing the user SSH key needs to be performed by the user by going to
https://portal.osgconnect.net/globus-app/account and add/remove the SSH key
in the "Manage SSH and X.509 keys" window.

2. Change project membership

To add a user to a project, either the user can request being added to the 
project, or have a "Manager"/"Admin" invite the user to the project. If the 
user is a member of the top-level project, e.g. `osg`, a "Manager"/"Admin" can 
"invite" the user and the user is added to the group automatically. If the user 
is not a member of the top-level project, the user can request membership in an 
project or a a "Manager"/"Admin" can "invite" the user. If the user is invited, 
the user will receive and email and have to accept the invitation. 

3. Delete user

To delete a user, the "Manager"/"Admin" can simply remove the user from the 
project.

In all these cases, the synchronization step will propagate the changes from 
Globus through the `json` file to puppet and ultimately the servers. 


## Known Issues

### Username during Sign up procedure

One issue that appears in about 1/3 of user sign ups is that the user uses 
a non-Globus ID to request membership in the respective top-level project. This 
is caused by the fact that the user link their institutional credentials to 
their Globus ID or never create a Globus ID. The former is much more frequent 
than the latter. 

If the user has a Globus ID, one can invite them to the group with that. The 
user will receive an email that they need to accept. This step also allows one 
to check whether the user has a Globus ID.


### OSG Stash Globus Endpoint

If the user does not have the Globus ID as their primary ID, e.g. their 
institutional ID or their GMail, the setup of the Globus endpoint for OSG Stash 
will not work. This has to do with using the Globus MyProxy server as the 
source for authentication. Without having the Globus ID as the primary, this 
will not work. 