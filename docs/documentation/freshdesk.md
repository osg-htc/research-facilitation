# Managing Documentation in Freshdesk

Brief overview: source for the documentation is in markdown files 
in the documentation repository.  "Empty" articles are created and 
organized in categories in Freshdesk. Each article has a numeric 
identifier.  The `freshpush.ini` file maps 
the markdown documents in the repository to the appropriate numeric 
identifier so that the content gets pushed into that article in Freshdesk. 

For more details, see [this page](https://support.opensciencegrid.org/a/solutions/articles/5000641634-how-knowledge-base-synchronization-works-technical-reference-).

Relevant links: 
* Documentation repository: https://github.com/OSGConnect/connectbook
* Freshdesk solutions: https://support.opensciencegrid.org/a/solutions/
* Rendered Docs: https://support.opensciencegrid.org/support/home
* Style guide: https://opensciencegrid.org/technology/documentation/style-guide/ 

## Adding a Document

* Clone the documentation repository if you haven't already. 
    git clone --recursive https://github.com/OSGConnect/connectbook.git
* Create a markdown file and add content. 
* Create empty article in Freshdesk. 
* Add entry to `update/freshpush.ini` in the connectbook `repository`
* Commit change and push changes
    git commit -a -m "commit message"
    git push origin master

## Reorganizing Content

Manage folders and article hierarchy in Freshdesk.

Have to update organization in markdown files in `connectbook` 
repository manually; however, we like to do this to make it 
easier to find the appropriate markdown file to make changes.  

## Editing a Document

Online OR on own computer

https://support.opensciencegrid.org/support/solutions/articles/5000641843-editing-content-topics-

## Archiving or Removing a Document

* Clone the documentation repository if you haven't already. 
    git clone --recursive https://github.com/OSGConnect/connectbook.git
* Move the file to the `archive` folder.
    git mv document.md archive
    git commit -a -m "archiving document"
* Remove that document's entry from `update/freshpush.ini`
* In Freshdesk, delete the corresponding article. 
