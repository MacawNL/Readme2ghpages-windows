# Readme2ghpages-windows

A Windows PowerShell script for GitHub users to convert the README.md in the master branch to an index.html file in the gh-pages branch using http://www.DocumentUp.com.

The gh-pages branch in a GitHub repository can contain documentation pages. The pages are published as a web site if the **gh-pages** branch is available. This web site is available under the URL **http://<your-name>.github.com/<your-repository>**.

This repository contains a single script: **PublishDocumentation.ps1**.
This script with make a gh-pages branch if it does not exist yet. All files are removed from the repository, and the script creates a single file called **index.html**.

NOTA BENE: Every time the script runs it will remove all files except **index.html**.

## How to use it

* Add the **PublishDocumentation.ps1** script to the root of your repository, next to README.md.

* Run **PublishDocumentation.ps1** in the PowerShell **Git Shell** (I assume you installed [GitHub for Windows](http://windows.github.com/)). We assume you are in the same directory as script **PublishDocumentation.ps1** itself.

The documentation is generated with http://www.DocumentUp.com. The generated html content is written to the file **index.html**.

You can rerun the script as often as you want,

## Tips and tricks

* The **PublishDocumentation.ps1** script does commit the README.md file first, so no need to do this after editing the documentation.

* Keep images in the master branch, and reference the images in the documentation using its full path. I use the folder DocumentationImages. You can find the path to the image by open it on the GitHub side and selecting the raw view. In the address bar you will see the full path to the image. Example of such a path: https://raw.github.com/MacawNL/WebMatrix.Executer/master/DocumentationImages/ErrorsAndWarningsPane.png
