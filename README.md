# HW Design Directory Template Generator
Directory template generator dedicated to hardware design flow control.

## Features
* Easy development and maintenance. 
* Generic approach to generating directory tree structure allows to use this script in your own application.
* Simple, local control version mechanism provided by `BackMeUp.py` script. It creates zip archive with current design files.

## Usage: 

1. Open script `HwDirectoryTreeGenerator.py`
2. Read comments.
3. Setup client/project/tool info.
4. Run script python `HwDirectoryTreeGenerator.py`.
5. Enjoy complete directory tree for your new project.

For detailed directory tree description please check `Directory_Template_Manual.pdf` (will be generated by script).

## Modifying directory structure
Directory structure is described in `DirectoryTemplate.txt` or `DirectoryTemplateBasic.txt`. (Basic template is suggested for more experianced user, who knows where particular files should be placed. In this case, readme files will not be generated.) You can use tree available definitions:

1. `\---` - describes last directory on current depth level,
2. `+---` - describes directory on current depth level,
3. `#---` - file on current depth level.

Depth is described by amount of spaces. Increasing number of spaces by four will cause increasing depth level. It is important to keep specyfic amount of whitespaces, beacuse directory tree parsers uses them for distinguishing depth levels.

When you add new text file on any level, you have to also add content for this file. To do it, you have to add new string in specyfic place in `HwDirectoryTreeGenerator.py` script and append this string to `fileContent` structure. If something will be wrong, content of files will be misalignment between them.

## Default directory tree layout (DirectoryTemplate.txt)
```
\---_ProjectName
    #---ReadMe.txt
    +---Design Files
    |   +---_EDATool Specific Files
    |   |   +---_EDATool Integrated Library
    |   |   |   #---ReadMe.txt
    |   |   |   \---3D models
    |   |   |       #---ReadMe.txt
    |   |   \---_EDATool Templates
    |   |       #---ReadMe.txt
    |   \---_ClientName
    |       \---_ProjectName
    |           #---ReadMe.txt
    |           +---Backup
    |           |   #---ReadMe.txt
    |           #---BackMeUp.py
    |           +---Docs
    |           |   #---ReadMe.txt
    |           +---V1I1
    |           |   #---ReadMe.txt
    |           |   +---Firmware
    |           |   |   #---ReadMe.txt
    |           |   \---TODO
    |           |       #---ToDo.txt
    |           \---VxIx
    |               #---ReadMe.txt
    |               +---Firmware
    |               |   #---ReadMe.txt
    |               \---TODO
    |                   #---ToDo.txt
    +---Released Files
    |   #---!!!ImportantReadMe!!!.txt
    |   \---_ClientName
    |       \---_ProjectName
    |           #---ReadMe.txt
    |           +---V1I1
    |           |   +---3D
    |           |   |   #---ReadMe.txt
    |           |   +---Board Assembly
    |           |   |   #---ReadMe.txt
    |           |   +---Firmware
    |           |   |   #---ReadMe.txt
    |           |   +---PCB Manufacturing
    |           |   |   #---ReadMe.txt
    |           |   |   +---Gerber Output
    |           |   |   |   #---ReadMe.txt
    |           |   |   +---Layers with Highlighted Differential Pairs
    |           |   |   |   #---ReadMe.txt
    |           |   |   \---NC Drill Output
    |           |   |       #---ReadMe.txt
    |           |   +---Schematic
    |           |   |   #---ReadMe.txt
    |           |   \---Source Files
    |           |       #---ReadMe.txt
    |           \---VxIx
    |               +---3D
    |               |   #---ReadMe.txt
    |               +---Board Assembly
    |               |   #---ReadMe.txt
    |               +---Firmware
    |               |   #---ReadMe.txt
    |               +---PCB Manufacturing
    |               |   #---ReadMe.txt
    |               |   +---Gerber Output
    |               |   |   #---ReadMe.txt
    |               |   +---Layers with Highlighted Differential Pairs
    |               |   |   #---ReadMe.txt
    |               |   \---NC Drill Output
    |               |       #---ReadMe.txt
    |               +---Schematic
    |               |   #---ReadMe.txt
    |               \---Source Files
    |                   #---ReadMe.txt
    \---Work
        \---_ClientName
            \---_ProjectName
                +---V1I1
                |   +---Competition and Similar Products
                |   |   #---ReadMe.txt
                |   +---Datasheets
                |   |   #---ReadMe.txt
                |   +---Design Guides
                |   |   #---ReadMe.txt
                |   +---Development Boards
                |   |   #---ReadMe.txt
                |   +---Errata
                |   |   #---ReadMe.txt
                |   \---Software
                |       #---ReadMe.txt
                \---VxIx
                    +---Competition and Similar Products
                    |   #---ReadMe.txt
                    +---Datasheets
                    |   #---ReadMe.txt
                    +---Design Guides
                    |   #---ReadMe.txt
                    +---Development Boards
                    |   #---ReadMe.txt
                    +---Errata
                    |   #---ReadMe.txt
                    \---Software
                        #---ReadMe.txt

```
## Basic directory tree layout (DirectoryTemplateBasic.txt)
```
\---_ProjectName
    +---Design Files
    |   +---_EDATool Specific Files
    |   |   +---_EDATool Integrated Library
    |   |   |   \---3D models
    |   |   \---_EDATool Templates
    |   \---_ClientName
    |       \---_ProjectName
    |           +---Docs
    |           +---V1I1
    |               +---Firmware
    |               \---TODO
    +---Released Files
    |   \---_ClientName
    |       \---_ProjectName
    |           +---V1I1
    |               +---3D
    |               +---Board Assembly
    |               +---Firmware
    |               +---PCB Manufacturing
    |               |   +---Gerber Output
    |               |   +---Layers with Highlighted Differential Pairs
    |               |   \---NC Drill Output
    |               +---Schematic
    |               \---Source Files
    \---Work
        \---_ClientName
            \---_ProjectName
                +---V1I1
                    +---Competition and Similar Products
                    +---Datasheets
                    +---Design Guides
                    +---Development Boards
                    +---Errata
                    \---Software
```
## References
Folder structure comes from [welldone blog](http://www.fedevel.com/welldoneblog/2013/10/hardware-design-directory-template/)

