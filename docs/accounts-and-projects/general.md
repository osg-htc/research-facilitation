# OSG User Support Internal Documentation

## Creating Accounts in OSG Connect. 

The account creation workflow for OSG Connect follows a fairly straightforward 
workflow:

1. Users enter through one of the Connect websites, e.g. www.osgconnect.net
2. The default should be that they sign in via CILogon, using their institutional identity. 
If they don't have an institution that's part of CILogon, they should use Globus. 
3. Completing the login steps will generate a profile that is "pending" in the osg group 
(which represents all accounts on OSG Connect)
4. An e-mail gets sent to "Manager"s and "Admin"s of the top-level connect project 
and a ticket gets created in FreshDesk
5. At this point, a member of the OSG support team steps in and follows the steps 
listed in the [guide on creating new accounts](../accounts)
6. After the account has been approved, a login node assigned, and an ssh key uploaded, 
the person's account should be generated on the appropriate login node within 30 minutes. 

## Updating Accounts in OSG Connect

The only updates that need to be made to a user account are:

1. Change SSH key

Changing the user SSH key needs to be performed by the user by going to
https://www.osgconnect.net/profile, clicking on "Edit Profile" and then 
adding or changing their ssh key. 

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