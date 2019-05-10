# Setting up OSG repositories on GitHub

## Setting up a topology repository fork

The `topology` repository does not allow for direct commits so all changes
will need to be submitted via pull requests from personal forked repositories.
This can create challenges keeping your copy up to date with changes made to the
official repository.

1. Create a personal fork of the topology repository

To do this, visit the [repository page at https://github.com/opensciencegrid/topology/](https://github.com/opensciencegrid/topology/)
and click the "Fork" button found in the top right corner.

2. Clone the repository onto your local machine using the following command where <user_name> is your GitHub
account name or the organization name that your repository was associated with.

	git clone https://github.com/<user_name>/topology.git 
	cd topology

3. Establish the correct upstream repository

In order to pull down changes made to the main repository into yours, an upstream remote
will need to be set. From within your forked repository folder, do the following:

* List current configured remote repository for your fork:

	$ git remote -v
	origin	https://github.com/<user_name>/topology.git (fetch)
	origin	https://github.com/<user_name>/topology.git (push)

* Add a new remote `upstream` repository that will be synced with the fork:

	git remote add upstream https://github.com/opensciencegrid/topology/

* Verify the new upstream repository:

	$ git remote -v
	origin	https://github.com/<user_name>/topology.git (fetch)
	origin	https://github.com/<user_name>/topology.git (push)
	upstream	https://github.com/opensciencegrid/topology/ (fetch)
	upstream	https://github.com/opensciencegrid/topology/ (push)

## Making Changes and Creating Pull Requests

1. Pull down upstream changes

Before creating any changes, it is best to pull down upstream changes to 
avoid merge conflicts. To do this, use the command:

	git pull upstream master

2. Make changes in your local fork

Add and/or change any necessary files and commit them to your local repository.

3. Create pull request

Submit a new pull request to the official topology repository from your fork.
