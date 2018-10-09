# gitedit

## What is this project about?
There are a lot of people working collaboratively on text for some purpose, which are not tech savvy.
There are some people working collaboratively on text, which are. 
Both run into the same problem when doing so, namely versioning, ways to communicate where and why they changed stuff, communicating their thoughts about passages without changing them and so on.
The tech savvy people built tools that help with these problems: A myriad of collaborative text editors and document formats, git, github and so on.
The non tech savvy people don't know how to use these tools.
This project is there to bridge this gap.

## What is needed to work on text collaboratively over distances?
Feel free to ammend this list if you think something is missing:

* Automatic versioning: Keeping track of changes, showing what was changed, giving names to changes
* Branching: Like git does: One group works on one part, while the other group works on another part? give them a way to make a brach and merge when finished.
* Handling change: Enable people to comment on why they changed what part, not only show the change
* Comment on text: Comment on specific parts in the text as a feature in a chat system that is integrated into the editor
* Transparency: Show who changed what, make sure that only authorized people have access to the text, make sure that changes attributed to some contributer really are from that contributer
* Automatic backup: Make sure that if the tool is used properly for its intended purpose, no data is lost ever without the user taking care of it
* Easy conversion: Keep the text in one format, enable users to export to many formats
* Giving context: Including media in order to give context to a point (newspaper article, video on youtube, website etc.)

## What are tools already available for this?

* git: Can be used for versioning, backup, showing who changed what, showing changes, assigning changes to contributors (gpg keys). what may be needed additionally: comments on specific changes, chat (protocoll for adressing text, folder in repo for chat?). think about what pull requests are for, how they can be used and how to integrate them.
* markdown: great tool for storing text easily, lots of available infrastructure for converting (no way to store comments (-> chat?), some text features maybe not available (footnotes, citations etc)).
* gpg & ssh: enabling authentication and making sure access only for the right people.

## What is needed?

The most important thing needed is a gui that takes care of most of the command line stuff to do this. This gui is basically a WYSIWYG text editor limited to the features of markdown, with added funcionality:

* A chat bar, where you can chat about the text using the authentication already in place for the git repo (gpg & ssh), as well as being able to reference parts in the text you are commenting on (hover & highlight)
* A git gui, for pulling changes, commiting and pushing them, adding comments to changes, making a branch and merging it, showing a diff.
