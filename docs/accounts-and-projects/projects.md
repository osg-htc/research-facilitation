# Projects

Creating a project in OSG Connect requires three steps.

## Create the project on the portal

To create a new project using the OSGConnect.net portal, click "Create Project" button in the 
Admin panel on osgconnect.net.

Complete the provided form. You will need the following information:

```
Requester Name: 
Requester Email Address: 
Project Name (short project name): 
Display Name (descriptive project name): 
Field of Science:
PI Name: 
PI Email:
PI Organization:
Project Description:
```

Please only use [NSF-aligned Field of Sciences](https://osp.unm.edu/pi-resources/nsf-research-classifications.html) 
for the "Field of Science". 

Click "Submit" to add the new project.

## Add the user to the project

After the project file has been created, add the required users to the project. 
If you are doing this step immediately after creating the project, skip to step <<number>> below

1. Go to https://www.osgconnect.net and login
2. Click on the "Projects" tab on the Admin panel
3. Find the new project, using "Search" if desired, and open the project by clicking on the long name
4. Click on the "Add Members" and find the target user, using "Search" if desired/necessary
5. Add the user to the project by clicking the "Add Member" button next to their entry


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

Within your forked repository, go into the projects folder and create a project file. 
The project file should be named the same as the short (UNIX) project name. 
It usually makes sense to copy from another project 
file that was also created for an OSG Connect project so the 
sponsor information is already correct.  Fill in the appropriate information, including the ID number 
you got from the previous step.

In order to maintain consistancy in organization naming structure, please use the `bin/list_organizations` 
function to ensure the name you are using matches this list.

4. Commit the new project file and submit a PR. 
