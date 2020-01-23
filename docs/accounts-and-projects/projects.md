# Projects

Creating a project in OSG Connect requires three steps.

## Create the project using gosync

The email received 
in Freshdesk entails the the information needed to create a group. Copy the 
information, e.g. 

```
Your Name: 
Your Email Address: 
Project Name: 
Short Project Name: 
Field of Science: Evolutionary 
Field of Science (if Other): 
PI Name: 
PI Email:
PI Organization:
PI Department:
Join Date: 
Sponsor: 
OSG Sponsor Contact: 
Project Contact: 
Project Contact Email: 
Telephone Number: 
Project Description:
```

into a text file. Note: the fields are freeform and do not need to be formatted in any specific
way

This text file can then be passed to `./add_connect_group.py` 
in `gosync3`. Do this on login03.osgconnect.net under `/usr/local/gosync3/`.

Using the the project information text file, the group can be added to the 
by running 

```
./add_connect_group.py --projectfile /path/to/file --parent <parent_group>
```

The "parent_group" is usually `osg`.

## Add the user to the project

After the project file has been created, 
add the required users to the project. 

* Go to https://www.osgconnect.com and login as the connect user
* Go to Connect > My Projects in the menu
* Click on "Groups" on the left and scroll down to the project that was just generated
* Click on members, and then the "Invite others to join" link
* Search for user, and then hit the send invitation button

The "invite" will **automatically add** the user 
to the project group; they won't need to accept anything. 

Additionally, the project requestor or 
another designated user needs to be made a "Manager" in Globus.

## Add the project to `topology`

The project will also need to be added to the OSG topology at 

https://github.com/opensciencegrid/topology/tree/master/projects

1. Clone the topology repository and `cd` into it.
```
git clone https://github.com/opensciencegrid/topology
cd topology
```

2. Run the "next project id" script in the bin/ directory:
```
bin/next_project_id
```
That will give you the ID number for the new project.  

3. To add a new project file, you will need to ensure you are working
within your own (forked) version of the repository. If you have not already
done so, fork the topology repository by visiting https://github.com/opensciencegrid/topology, 
clicking "Fork". Detailed information for setting up and maintaining your fork can be found
in the [GitHub documentation page]({% link docs/documentation/github.md %}).

Within your forked repository, go into the projects folder and create a project 
 file. It usually makes sense to copy from another project 
 file that was also created for an OSG Connect project so the 
 sponsor information is already correct.  Fill in the appropriate information, including the ID number 
 you got from the previous step. 

4. Commit the new project file and submit a PR. 
