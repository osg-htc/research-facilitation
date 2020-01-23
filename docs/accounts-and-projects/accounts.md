# Accounts

## Requirements for Users

Users need to satisfy the following in order to be approved:

* Must provide an institutional email address (e.g. user@university.edu, etc.)
* Must apply with using globusid account
* Must be affiliated with a US institution or research group

## Process for Creating/Onboarding New OSG Connect Users

1. Determine correct onboarding process
2. Reply to account request to schedule engagement meeting 
3. Meeting preparation
4. Meet with the applicant
5. Complete the onboarding process

If the applicant doesn't respond to the request for the meeting, see the instructions for follow-up below. 

### Special Cases

Check to see if the account request falls under one of these special cases. If so, please follow the [Account Creation Flowchart](https://docs.google.com/spreadsheets/d/1x-ttoFxE7VlMUKyEKa_u454yd_UIdFgiLfdJj0zcBkM/edit?usp=drive_web&ouid=107104347624934509720) to route correctly.

Special cases exist for:

* UChicago (Xenon1T, South Pole Telescope)
* Duke
* CMS
* ATLAS
* Jefferson Lab
 
** OSG User School Attendees **

Individuals who attend the OSG User School in at UWMadison do not need an onboarding meeting and their account creation process can be streamlined.

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
	* Thank you for your application for an OSG Connect account. In order to understand your computational research goals and ensure that you get the most out of the Open Science Grid, we schedule a brief meeting as part of the account approval process.

		See my calendar for my availability (XXXXXXXX - note my XX time zone), and let me know what time would work well for you to meet. Our discussion should take between 30 - 45 minutes, and I can provide a teleconference link, unless you have a more preferable option.
		
		Additionally, we can streamline the upstart process by associating your account with an OSG Connect 'project'. If you intend to join an existing OSG Connect project associated with your research group, please let me know the name and PI of that project. Otherwise, we just need the below details to create a new project for you, which other members of your research group could join at a later time.
		
		* Project Title:  (representative of your research group/org’s research priorities)
		* PI Email: 
		* PI Department or Organization:
		* PI Institution:
		* Project Field of Science: (out of https://www.nsf.gov/about/research_areas.jsp)
		
		Looking forward to meeting you soon!
		
		XXSIGNATUREXX
		
* If no institutional email or Globus ID
	* We received your application to join OSG Connect.  The email you used for the account application is a XXXXX address.  Could you please re-apply and this time supply your XXXXX University email address so that we can verify your affiliation?  I will remove the current application so that you will be able to re-apply. 
	* We got your application to join OSG Connect.  In the application, the username is XXXXXXX.  This username is based on an institute provided ID, but it needs to be a GlobusID.  On our system it is difficult to create and maintain a unix account with a username other than a globusID.  Could you please re-apply with a globusID as username as outlined here: https://osgconnect.net/signup.  I will remove your current pending application so that you will be able to re-apply.
	
* If no apparent connection to US institution: 
	* We received your application for an OSG Connect account. One of the requirements to have an account on OSG Connect is that the applicant needs to have an affiliation with a US-based institution or project.  Do you have an affiliation with a US research institution (academic, government, non-profit), or US-based collaboration (if so, which collaboration)?

### Non-Responsive Applications

If someone doesn't respond to the request for a meeting, we will send one follow-up email (a week later) and then reject the account (a week later). 

1. If someone doesn't respond to the initial request, set the ticket **Type** to "on-boarding - 1 week" and close the ticket. 
2. Once it reopens send this email. 
> Let me know if you're still interested in scheduling a brief meeting to create an OSG Connect account.  See my previous email below for details. If we don't hear back from you, we'll close your account request in a few days. 
3. Set the ticket to "on-boarding - 1 week" again and close the ticket again.
4. Once it reopens, reject the person's request and send this email (optional): 
> Since we haven’t heard from you, we’ll remove your OSG Connect account request. If you decide to pursue OSG Connect in the future, just Sign Up for an account, again.

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

**Create the project:**

If the user is joining a new project, it will need to be created at this point. 
This can be completed by following the steps outlined on the [Projects documentation page]({% link docs/accounts-and-projects/projects.md %}).

**Add to their appropriate project:**

Do the following to add user to their project (new or already generated)

* Go to https://www.osgconnect.com and login as the `connect` user
* Go to Connect > My Projects in the menu
* Scroll down to the appropriate project for the user
* Click on members, and then the "Invite people to this group" link
* Search for user, and then hit the send invitation button

**Send follow-up email** 

Hi NAME OF USER,

I've authorized your account in the Globus 'osg' group (for OSG Connect, which you should receive a confirmation email for), and I invited you
to join the new "GROUPNAME" group project. You should have second email inviting you to accept this invitation to your project.

**Log In**
The last step you need to log in is submitting a public ssh key -- see [this page](https://support.opensciencegrid.org/support/solutions/articles/12000027675-generate-ssh-keys-and-activate-your-osg-login) for detailed
instructions. You should be able to log into the OSG Connect login nodes
(login.osgconnect.net) with your Globus ID (and password) within a few hours after setting
up your ssh keys.

**Submitting Jobs**
For job submission, I highly recommend looking through the latest [HTCondor User Tutorial](https://agenda.hep.wisc.edu/event/1201/other-view).
Our [OSG Connect Quickstart](https://support.opensciencegrid.org/support/solutions/articles/5000633410-osg-connect-quickstart) has a few HTCondor examples, and you'll be best off by
submitting all jobs from /local-scratch (see [Data Management](https://support.opensciencegrid.org/support/solutions/articles/12000006512-guidelines-for-data-managment-in-osg-storage-and-transfer)).

Before submitting any jobs, you’ll need to activate your project so that the required
‘ProjectName’ attribute is automatically set for future submissions. On the login node, run:
$ connect project

Let me know how things go as you submit -- you can email us at this address
(support@osgconnect.net) or reply to this thread. We're here to help!

Cheers,

STAFF MEMBER

**Ticket clean up**

* Paste notes from onboarding meeting into ticket
* If there are no outstanding issues, change the status of the ticket to "resolved" and the Type to "on-boarding X weeks".
