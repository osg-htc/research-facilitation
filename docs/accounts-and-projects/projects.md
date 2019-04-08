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

into a text file. This text file can then be passed to `./add_connect_group.py` 
in `gosync3`. Do this on login03.osgconnect.net under `/usr/local/gosync3/`.

Using the the project information text file, the group can be added to the 
by running 

```
./add_connect_group.py --projectfile /path/to/file --parent <parent_group>
```

## Add the user to the project

After the project file has been created, log into Globus using the `connect` user and
add the required users to the project. The groups are listed on the left, 
find the appropriate group and then click on "invite others" or a similar
command. Search for the user and send them an invitation -- if they're
a member of the parent group, the "invite" will **automatically add** them 
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

3. Then, go into the projects folder and create a project 
 file. It usually makes sense to copy from another project 
 file that was also created for an OSG Connect project so the 
 sponsor information is already correct.  Fill in the appropriate information, including the ID number 
 you got from the previous step. 

4. Commit the new project file and submit a PR. 
