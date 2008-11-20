CSS: style.css
LaTeX preamble: preamble.tex

[rosetta]: http://en.wikipedia.org/wiki/Rosetta_Stone
[this_html]: http://media.build-doctor.com/rosetta-stone
[this_pdf]: http://media.build-doctor.com/rosetta-stone/stone.pdf

Build Rosetta Stone
===================

Introduction
------------
The original Rosetta stone was discovered in Egypt in 1799, and controversially brought back to Europe in 1802.  The stone led to a breakthrough in the decipherment of Hieroglyphic writing. It now resides in the British Museum in London and is well worth a visit. [Wikipedia link][rosetta]

What's on this stone?  Major tasks and commands from several build languages.

Most build tools deal with a very similar problem in a familiar way.  So if you know one build tool, you probably don't want gory details on how to write a buld file - you just want to know about that task.   You know, that task? I know what it is in Ant ...   

This document is available in  [HTML][this_html] and [PDF][this_pdf].

File Tasks
----------

|Ant|Nant|MsBuild|Rake|Desc|
|---|-----|-------|------|---|
|Basename|.|.|.|Identify the last element of a path|
|BUnzip2|.|.|.|Extract a Bzip2 archive|
|BZip2|.|.|.|Make a Bzip2 archive|
|Checksum|.|.|.|Calculate the message digest checksum of a file|
|Chmod|attrib|.|.|Change permission bits on a file|
|Concat|.|.|.|Concatenate files|
|Copy|copy|Copy|cp|Copy files or directories|
|Delete|delete|Delete,RemoveDir|rm, rm_r_|Remove files or directories|
|Dirname|.|.|.|Identify the directories that make up a path|
|FixCRLF|.|.|.|Change the line ending of a file|
|Filter|.|.|.|Replace tokens in files|
|GUnzip|gunzip|.|.|Uncompress a GZip archive|
|GZip|.|.|.|Make a GZip archive \[surely nant has this?\|
|LoadFile|loadfile|.|.|read a file into a property|
|Mkdir|.|MakeDir|.|Make a new directory|
|Move|move|.|.|Move files and directories|
|Replace|.|.|.|Replace a token in a file or group of files|
|Tar|tar|.|.|Make or extract a tar archive|
|Tempfile|.|.|.|Make a unique temporary directory|
|Touch|touch|Touch|touch|Update timestamp on a file|
|Unzip|.|.|.|Extract a Zip archive file|
|Zip|zip|.|.|Make a Zip archive file|


Compilation, Linking etc.
-------------------------


|Ant|Nant|MsBuild|Desc|
|---|-----|-------|------|
|.|al|AL|.|Assembly Linker|
|.|cl|.|Compile C/C++ code|
|.|csc|Csc|Compile C# code|
|javadoc|ndoc|.|Generate Documentation|
|Java|.|.|Run Java Code
|Javac|.|.|Compile Java Code|
|.|vbc|Vbc|Compile Visual Basic Code|
|.|jsc|.|Compile Jscript.NET code|
|.|vjc|.|Compile J# code|
|junit [^optional]|nunit2|.|.|
|Rmic|.|.|run the RMIC compiler for a single class|


Packaging Tasks
------------------


|Ant|Nant|MsBuild|Rake|
|---|-----|-------|------|
|.|ASMInfo|AssemblyInfo|.|
|Ear|.|.|.|
|Jar|.|.|.|
|Manifest|.|.|.|
|ManifestClassPath|.|.|.|
|Unjar|.|.|.|
|Untar|.|.|.|
|Unwar|.|.|.|
|War|.|.|.|

Version Control System Tasks
----------------------------


|Ant|Nant|MsBuild|Rake|
|---|-----|-------|------|
|Cvs|cvs|.|.|
|CvsChangeLog|cvs-changelog|.|.|
|CvsVersion|.|.|.|
|CVSPass|cvs-pass|.|.|
|CvsTagDiff|.|.|.|

Other Tasks
------------------
|Ant|Nant|MsBuild|Rake|
|---|-----|-------|------|
|Ant|Nant|MsBuild|.|
|AntCall|NantCall|CallTarget|.|
|AntStructure|NantSchema|.|.|
|Apply|.|.|.|
|Available|.|.|.|
|BuildNumber|.|.|.|
|Condition|if|.|.|
|Defaultexcludes|.|.|.|
|Description|Description|.|.|
|Dependset|.|.|.|
|Diagnostics|.|.|.|
|Echo|echo|Message|puts|
|EchoXML|.|.|.|
|Exec|Exec|Exec|.|
|Fail|fail|.|.|
|.|Foreach|.|.
|GenKey|.|.|.|
|Get|Get|.|.|
|Import|include|.|.|
|Input|.|.|.|
|Length|.|.|.|
|LoadProperties|.|.|.|
|LoadResource|.|.|.|
|MakeURL|.|.|.|
|Mail|mail|.|.|
|Macrodef|.|.|.|
|Nice|.|.|.|
|Parallel|.|.|.|
|Patch|.|.|.|
|PathConvert|.|.|.|
|PreSetDef|.|.|.|
|Property|property|.|property|
|Record|.|.|.|
|ResourceCount|.|.|.|
|script,scriptdef[^optional]|script|.|.|
|Sequential|.|.|.|
|.|servicecontroller|.|.|
|SignJar|.|.|.|
|Sleep|sleep.|.|.|
|Sql|.|.|.|
|Subant|.|.|.|
|Sync|.|.|.|
|Taskdef|loadtasks|.|require|
|TStamp|tstamp|.|.|
|Typedef|.|.|.|
|Uptodate|.|.|.|
|Waitfor|.|.|.|
|.|.|Warning|.|
|WhichResource|.|.|.|
|XmlProperty|.|.|.|
|XSLT/Style|style|.|.|

[^optional]: This task has additional library dependencies

Notes
-----
Deprecated tasks are not included.


Author
------

Julian Simpson

<http://www.build-doctor.com>

<medic@build-doctor.com>

![BD Logo](logo.jpg)

![CC Logo](license.png)

This work is licenced under the Creative Commons Attribution-Non-Commercial-Share Alike 2.0 UK: England & Wales License. To view a copy of this licence, visit http://creativecommons.org/licenses/by-nc-sa/2.0/uk/ or send a letter to Creative Commons, 171 Second Street, Suite 300, San Francisco, California 94105, USA.
