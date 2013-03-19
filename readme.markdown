# HideFileExtension.tmbundle

Projects employing interpreted languages often have folders with files of solely one type. Web projects may have separate folders for css files, js files, and html files for example. Showing the file extensions in file browser in this case is redundant.

This bundle contains a command that automatically hides the extension when saving a file inside a folder where 'attr.hide-extension.enabled' scope attribute is set. This is done by applying `SetFile -A E` to the file. 

On top of that, it includes commands for 

* hiding the extension of all files inside the current folder (and its subfolders)
* unhiding the extension of current file
* unhiding the extension of all files inside the current folder (and its subfolders)

## Installation instructions (Textmate 2)

    cd ~/Library/Application Support/Avian/Pristine Copy/Bundles
    git clone git://github.com/meryn/hide-file-extension-tmbundle HideFileExtension.tmbundle

## Configuration instructions

There are two prerequisites for this to work:

1. "Show all file extensions" preference in Finder needs to be disabled. At times you want to view file extensions in Finder, you need to temporarily enable it again.
2. The file type of the files you want to hide must be known by OS X. That is, they must be registered to open with an application. Any application will do. Textmate would be an obvious choice.

Create or edit a .tm_properties file anywhere, and place the following inside:

    scopeAttributes = 'attr.hide-extension.enabled'

After that, you probably want to run the "hide extensions inside current folder" command once for each folder you'd like file extensions to be hidden in.

## Further reading

See https://github.com/textmate/textmate/issues/911 for some background information.  
See http://developer.apple.com/library/mac/#documentation/Darwin/Reference/ManPages/man1/SetFile.1.html for information on SetFile.