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

For "PI Organization", visit the [project organizations list](https://topology.opensciencegrid.org/organizations)
to see if the organization is already used in another project.  If so, be sure to use the same spelling
and punctuation in your own entry, so we don't have duplicate organizations with different spellings.

Note: the convention for "Project Name" for non-XSEDE projects is `<SHORT INSTITUTION>_<PI LAST NAME>`
where `<SHORT INSTITUTION>` is an abbreviation or short version of the organization name.
For example, abbreviate "University of Wisconsin-Madison" as "UWMadison".
The "Project Prefix" column in the [project organizations list](https://topology.opensciencegrid.org/organizations)
contains what you should use for `<SHORT INSTITUTION>` for that organization.  If the organization is not
there, or the Project Prefix column is blank, pick something appropriate; you should later add it to the
[project/institution mappings file](https://github.com/opensciencegrid/topology/blob/master/mappings/project_institution.yaml).
when you register the project in Topology.

Click "Submit" to add the new project.

## Add the user to the project

After the project file has been created, add the required users to the project. 
If you are doing this step immediately after creating the project, skip to step 4 below

1. Go to https://www.osgconnect.net and login
2. Click on the "Projects" tab on the Admin panel
3. Find the new project, using "Search" if desired, and open the project by clicking on the long name
4. Click on the "Add Members" and find the target user, using "Search" if desired/necessary
5. Add the user to the project by clicking the "Add Member" button next to their entry


## Add the project to OSG Topology

The project will also need to be added to the OSG Topology repo at 

<https://github.com/opensciencegrid/topology/tree/master/projects>

1.  Clone the topology repository and `cd` into it.

        git clone https://github.com/opensciencegrid/topology
        cd topology

2.  To add a new project file, you will need to ensure you are working
    within your own (forked) version of the repository. If you have not already
    done so, fork the topology repository by visiting <https://github.com/opensciencegrid/topology>,
    clicking "Fork". Detailed information for setting up and maintaining your fork can be found
    in the [GitHub documentation page](../documentation/github.md).

    Within your forked repository, copy `template-project.yaml` into a new project file in the
    `projects` folder.
    The project file should be named the same as the short (UNIX) project name.
    Fill in the appropriate information.

    If you made the project for a new organization, or an organization that didn't have a
    "Project Prefix" in the [project organizations list page](https://topology.opensciencegrid.org/organizations),
    edit the [project/institution mappings file](https://github.com/opensciencegrid/topology/blob/master/mappings/project_institution.yaml),
    and add the mapping for the prefix you used.

    (You can skip this for XSEDE projects.)

3.  Commit the new project file and, if modified, the project/institution mappings file, and submit a PR. 
