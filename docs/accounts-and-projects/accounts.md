# New Accounts

## Requirements for Users

Users need to satisfy the following in order to be approved:

* Must provide an institutional email address (e.g. user@university.edu, etc.)
* Must be affiliated with a US institution or research group

## Process for Creating/Onboarding New OSG Connect Users

1. Determine correct onboarding process
2. Reply to account request to schedule engagement meeting 
3. Meet with the applicant
4. Approve account and add to a login node/project
5. Follow-up

If the applicant doesn't respond to the request for the meeting, see the instructions for follow-up below. 

### 1. Determine Correct Onboarding Process

Check to see if the account request falls under one of these special cases. If so, please follow the [Account Creation Flowchart](https://docs.google.com/spreadsheets/d/1x-ttoFxE7VlMUKyEKa_u454yd_UIdFgiLfdJj0zcBkM/edit?usp=drive_web&ouid=107104347624934509720) to route correctly.

**Special Cases**

* UChicago (Xenon1T, South Pole Telescope)
* Duke
* CMS
* ATLAS
* Jefferson Lab
 
**OSG User School Attendees**

Individuals who attend the OSG User School in at UWMadison do not need an onboarding meeting and their account creation process can be streamlined.

### 2. Reply to Account Request to Schedule Engagement Meeting

**Ticket changes**

Copy and paste the user's information from the ["Pending Members" page](https://www.osgconnect.net/groups/root.osg/members-requests) 
into the ticket as a note. 

**Initial Response**

* Do they have US institutional email?
* Standard response (also in the User Support's Canned Responses "New Account Request - schedule initial meeting")
	
> Thank you for your application for an OSG Connect account. In order to understand your computational research goals and ensure that you get the most out of the Open Science Grid, we schedule a brief meeting as part of the account approval process.
>	
> See my calendar for my availability (XXXXXXXX - note my XX time zone), and let me know what time would work well for you to meet. Our discussion should take between 30 - 45 minutes, and I can provide a teleconference link, unless you have a more preferable option.
>	
> Additionally, we can streamline the upstart process by associating your account with an OSG Connect 'project'. If you intend to join an existing OSG Connect project associated with your research group, please let me know the name and PI of that project. Otherwise, we just need the below details to create a new project for you, which other members of your research group could join at a later time.
>
> * PI Email: 	
> * PI Department or Organization:
> * PI Institution:
> * Project Field of Science: (out of https://www.nsf.gov/about/research_areas.jsp)
> 
> Looking forward to meeting you soon!
>	 
> XXSIGNATUREXX
	
* If no institutional email (Canned Responses: "New Account Request - non-institutional email")
	
> We received your application to join OSG Connect. A requirement for using OSG Connect is that you be affiliated with a United States academic, non-profit, or government organization. One way that we verify this affiliation is through an institutional/university email address. 
>	
> Can you please re-apply using your institutional email in the E-mail address field? ??It may require logging out of the osgconnect.net web portal and logging in again with your institutional credentials.  On the login page, where it says ???Use your existing organizational login,??? please select your institution from the drop-down menu and then ???continue.???  Please let me know if your institution is not listed.  I will remove your current application so that you will be able to re-apply.  
	
* If no apparent connection to US institution (Canned Responses: "New Account Request - non US") 
	
>We received your application for an OSG Connect account. One of the requirements to have an account on OSG Connect is that the applicant needs to have an affiliation with a US-based institution or project.  Do you have an affiliation with a US research institution (academic, government, non-profit), or US-based collaboration (if so, which collaboration)?

**Non-Responsive Applications**

If someone doesn't respond to the request for a meeting, we will send one follow-up email (a week later) and then reject the account (a week later). 

1. If someone doesn't respond to the initial request, set the ticket **Type** to "on-boarding - 1 week" and close the ticket. 
2. Once it reopens send this email (Canned Responses: "New Account Request - no response, pinging")
> Let me know if you're still interested in scheduling a brief meeting to create an OSG Connect account.  See my previous email below for details. If we don't hear back from you, we'll close your account request in a few days. 
3. Set the ticket to "on-boarding - 1 week" again and close the ticket again.
4. Once it reopens, reject the person's request and send this email (optional, Canned Responses: "New Account Request - no response, closing""): 
> Since we haven???t heard from you, we???ll remove your OSG Connect account request. If you decide to pursue OSG Connect in the future, just Sign Up for an account, again.


### 3. Meet with the Applicant

The goal of this meeting is to determine if the applicant's science problem is a good 
fit for high throughput computing + OSG, to tell them about the OSG (and how it may be 
similar or different from their previous experiences), and talk about concrete next 
steps for getting started. 

Sample onboarding discussion outline:

* Tell me about your research in general
* How does computing fit in? 
* Short term and long term priorities
* What does computing look like (dimensions) for short term goals? 
* One program run or many (how many)
* For one program run - how long? How much memory? Input/output? Can the workflow be split? Software?
* If the workflow isn???t OSG friendly -> refer to other computing resources
* At this point describe HTC (vs HPC if they have previous familiarity) and then OSG
* How OSG ???affects??? their software, file transfer and job submission

### 4. Finish Account Setup

**Request approval from PI**

To create new projects with a PI different than the requested user, to join existing projects, send an email to the PI to verify their approval. 


**Approve to enter the osg group:**

Go to the "[Pending Members](https://www.osgconnect.net/groups/root.osg/members-requests)" page of the OSG project and click the "Approve" button 
for the user. 

**Create a project:**

If the user is joining a new project, it will need to be created at this point. 
This can be completed by following the steps outlined on the [Projects documentation page](projects.md).

**Add to their appropriate project:**

1. Search for the project (pre-existing or newly-created) under the [OSG Projects tab](https://www.osgconnect.net/groups) and click on the project name. 
2. Click on the "Add Members" tab
3. Search for the user and add them to the login node. 

**Add to a login node**

1. Go to the [Login Nodes tab](https://www.osgconnect.net/login-nodes)
2. Choose a login node for the user. If someone has joined an existing group, look 
up one of their group members and try to put them on the same login node. If they are 
the first of their group, choose `login05`. 
3. Click the "Add User" button for that submit node. 
4. Search for the user and add them to the login node. 

### 5. Follow-Up

**Send follow-up email** 

Send the following email to the new user (Canned Responses: "New Account Request - welcome email")

> Hi NAME OF USER,
>
> I've authorized your login account for OSG Connect and added you to the "GROUPNAME" project in OSG (which you can use to run jobs on OSG from any submit point). You should have separate emails confirming these actions.
>
>
>**Log In**
>
> The last step you need to log in is submitting a public ssh key -- see [this page](https://support.opensciencegrid.org/support/solutions/articles/12000027675-generate-ssh-keys-and-activate-your-osg-login) for detailed instructions. You should be able to log into your designated OSG Connect login node within a few hours after setting up your ssh key.
>
>
>**Submitting Jobs**
>
> For job submission, we highly recommend looking through the latest [HTCondor Job Submission Tutorial] presentation(https://agenda.hep.wisc.edu/event/1325/session/0/contribution/19/material/slides/0.pdf).  Our [OSG Connect Quickstart](https://support.opensciencegrid.org/support/solutions/articles/5000633410-osg-connect-quickstart) has a few HTCondor examples, and the [Data Management](https://support.opensciencegrid.org/support/solutions/articles/12000002985-introduction-to-data-management-on-osg) guide discusses where and how to stage your data on the login node for for running jobs. 
>
> Before submitting any jobs on OSG Connect, you???ll want to activate your 'default' submission project so that the required ???ProjectName??? option is automatically set for future submissions. On the login node, run:
>
> $ connect project
>
> Let me know how things go as you submit -- you can email us at this address (support@osgconnect.net) or reply to this thread.  We're here to help!
>
> Cheers,
>
> STAFF MEMBER

**Ticket clean up**

* Paste notes from onboarding meeting into ticket
* If there are no outstanding issues, change the status of the ticket to "closed" and the Type to "on-boarding X weeks". When it re-opens, send a check-in email. If there is 
no response, mark the ticket as "resolved".
