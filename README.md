# Rationale #

* Steps that describe the workflow of migration 3 databases in 3 diferent operating systems, in outdated file formats. 
* In the [Bibliography.md](https://bitbucket.org/imhicihu/winisis-migration/src/328d9c2b9649caa3a4e65e57399dbfc817f40717/Bibliography.md?at=master&fileviewer=file-view-default) there are some _insights_ about the original database created, maintained, curated in the 90's. 
* _Goal_: generate an unique database compatible with the most current file format specifications.
![2235980529-terrae.png](https://bitbucket.org/repo/Kr5x8n6/images/3748228110-2235980529-terrae.png)

### What is this repository for? ###

* Quick summary
     - Workflow with a focus in the steps (mandatory) to migrate some older database (_circa_ 1990's) to current file format specifications. 
* Version 1.0
![bothdatabases.jpg](https://bitbucket.org/repo/Kr5x8n6/images/1785054149-bothdatabases.jpg)

### How do I get set up? ###

* Summary of set-up
     - Check our [WinIsis operating system test](https://bitbucket.org/imhicihu/winisis-migration/issues/1/software-winisis-compatibility-test)
     - [Windows 7 iso](https://www.microsoft.com/en-us/software-download/windows7)
          + once installed Windows 7 ISO _via_ VirtualBox, install [Windows Virtual PC](https://www.microsoft.com/es-ar/download/details.aspx?id=3702) and then [Windows XP Mode for Windows 7](https://www.microsoft.com/es-ar/download/details.aspx?id=8002). This will create a virtual environment, mandatory in this case because compatibilities issues. WinIsis runs _natively_ on 32 bits, so all the operating systems must follow this requisite, at this point, *essential*. 
	 - [WinIsis](http://biblio1.mdp.edu.ar/index2.php?pagina=recursos/wisis/winisis.php)
     - [VirtualBox](https://www.virtualbox.org/) (software that create a custom virtual environment) plus [VirtualBox Extension Pack](https://www.virtualbox.org/wiki/Downloads)
     - [Docker](https://www.docker.com/)
     - [Google Spreadsheet](http://spreadsheets.google.com/)
     - db3iso
     - [Beautiful Soap](https://www.crummy.com/software/BeautifulSoup/#Download): unencoding of unicode text to UTF-8 format specification. A kind of swiss-army knife of encoding-unencoding text files. 

* Configuration
     - _In the making_
* Dependencies
     - The less, the better (avoid steps prone to error). _In the making._
* Database configuration
     - _In the making_
* How to run tests
     - _In the making_
* Deployment instructions
     - _In the making_

### Issues ###

* Check them on [here](https://bitbucket.org/imhicihu/winisis-migration/issues)

### Who do I talk to? ###

* Repo owner or admin
     - Contact `imhicihu` at `gmail` dot `com` or our [Board](https://bitbucket.org/imhicihu/win-isis-migration/addon/trello/trello-board). (You need a [Trello](https://trello.com/) account)