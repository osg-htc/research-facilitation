# Projects

Creating a project in OSG Connect is fairly straightforward. The email received 
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

into a text file. This text file can then be past to `./add_connect_group.py` 
in `gosync3`. Do this on login03.osgconnect.net under `/usr/local/gosync3/`.

Using the the project information text file, the group can be added to the 
by running 

```
./add_connect_group.py --projectfile /path/to/file --parent <parent_group>
```

After the project file has been created, log into Globus using `connect` user and
add the required users to the project. Additionally, the project requestor or 
another designated user needs to be made a "Manager" in Globus.

The project will also need to be added to the OSG topology at 

https://github.com/opensciencegrid/topology/tree/master/projects

