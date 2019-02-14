# Accounts

## Requirements for Users

Users need to satisfy the following in order to be approved:

* Must provide an institutional email address (e.g. user@university.edu, etc.)
* Must apply with using globusid account
* Must be affiliated with a US institution or research group

## Process for Creating/Onboarding New OSG Connect Users

1. Reply to account request to schedule engagement meeting 
2. Meeting preparation
3. Meet with the applicant
4. Complete the onboarding process

### Reply to Account Request to Schedule Engagement Meeting

**Ticket changes**

Copy and paste the user's "Member Info" into a note in the account application ticket:

* Go to https://www.osgconnect.net and sign in.
* Go to Connect > My Projects and click on the osg group.
* On the "About" tab, select the name of the applicant and then click on "Member Info"
* Copy and paste the fields (Username, Full Name, E-mail Address, etc...) into the ticket as a note

**Initial Response**

* Does it look like they are a member of one of the special projects / Connect groups (Duke, Chicago, etc.) 
* Do they have a Globus ID and a US institutional email?
* Standard response
	* TBD
* If no institutional email or Globus ID
	* We received your application to join OSG Connect.  The email you used for the account application is a XXXXX address.  Could you please re-apply and this time supply your XXXXX University email address so that we can verify your affiliation?  I will remove the current application so that you will be able to re-apply. 
	* We got your application to join OSG Connect.  In the application, the username is XXXXXXX.  This username is based on an institute provided ID, but it needs to be a GlobusID.  On our system it is difficult to create and maintain a unix account with a username other than a globusID.  Could you please re-apply with a globusID as username as outlined here: https://osgconnect.net/signup.  I will remove your current pending application so that you will be able to re-apply.
* If no apparent connection to US institution: 
	* We received your application for an OSG Connect account. One of the requirements to have an account on OSG Connect is that the applicant needs to have an affiliation with  a US Institution.  Do you have an affiliation with a U.S. institution, organization, or project that was not listed on your application?

**No response**

* If someone has not responded, send a follow-up email after one-week
	* TBD
* If they don't respond to the second email: 
	* Reject request in OSG Connect
	* Change ticket to `resolved`

### Before the meeting

Generate the project: https://opensciencegrid.org/campus-research/accounts-and-projects/projects/ 

### During meeting

Onboarding discussion outline:

* Tell me about your research in general
* How does computing fit in
* Short term and Long term priorities
* What does computing look like (dimensions) for short term goals
* One program run or many (how many)
* For one program run - how long? How much memory? Input/output? Can the workflow be split? Software?
* If the workflow isn’t OSG friendly -> refer to other computing resources
* At this point describe HTC (vs HPC if they have previous familiarity) and then OSG
* How OSG “affects” their software, file transfer and job submission

### After the meeting

**Approve to enter the osg group:**

Do the following to add user to the newly created project

* Go to https://www.osgconnect.net and login as the `connect` user
* Go to Connect > My Projects in the menu
* Go to osg group or relevant group if applying to another group
* Click on members and click on pencil icon next to user
* Click on Approve button

**Add to their appropriate project:**

Do the following to add user to their project (new or already generated)

* Go to https://www.osgconnect.com and login as the `connect` user
* Go to Connect > My Projects in the menu
* Scroll down to the appropriate project for the user
* Click on members, and then the "Invite people to this group" link
* Search for user, and then hit the send invitation button

**Send follow-up email** 

TBD

**Ticket clean up**

* Paste notes from onboarding meeting into ticket
* If there are no outstanding issues, change the status of the ticket to "resolved" and the Type to "on-boarding X weeks".
