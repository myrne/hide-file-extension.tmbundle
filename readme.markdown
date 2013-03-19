# HideFileExtension.tmbundle

Projects employing interpreted languages often have directories with files of solely one type. Web projects may have separate directories for css files, js files, and html files for example. Showing the file extensions in file browser in this case is redundant.

This bundle automatically hides file extension for files in directories where 'attr.hide-extension.enabled' scope attribute is set. This is done by setting the E attribute on the file. Additionally, you may show a file extension again.

## Installation instructions (Textmate 2)

    cd ~/Library/Application Support/Avian/Pristine Copy/Bundles
    git clone git://github.com/meryn/hide-file-extension-tmbundle HideFileExtension.tmbundle

## Configuration instructions

There are two prerequisites for this to work:

1. "Show all file extensions" preference in Finder needs to be disabled. At times you want to view file extensions in Finder, you need to temporarily enable it again.
2. The file type of the files you want to hide must be known by OS X. That is, they must be registered to open with an application. Any application will do. Textmate would be an obvious choice.

Create or edit a .tm_properties file anywhere, and place the following inside:

    scopeAttributes = 'attr.hide-extension.enabled'

## Further reading

See https://github.com/textmate/textmate/issues/911 for some background information.