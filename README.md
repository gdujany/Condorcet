# Condorcet [![Build status](https://travis-ci.org/gdujany/Condorcet.svg?branch=master)](http://travis-ci.org/gdujany/Condorcet)

Condorcet is a web application for voting.

⚠️ **Note** ⚠️ This repository is archived. It has been superseeded by the [new implementation hosted on CERN's GitLab instance](https://gitlab.cern.ch/lhcb/condorcet).

Set up
---

The application uses the [Flask](http://flask.pocoo.org/) web framework and [SQLAlchemy](http://www.sqlalchemy.org/) database management packages.
To get up and running, run the setup which makes sure the correct Python version
is used, installs the dependencies, initialises the database and gets a copy of the [Flup](http://www.saddi.com/software/flup/)
Python module, which is used as a
[WSGI](http://en.wikipedia.org/wiki/Web_Server_Gateway_Interface) bridge.
Moreover it assumes you are setting up the website
[in a folder on AFS](https://espace2013.cern.ch/webservices-help/websitemanagement/ManagingWebsitesAtCERN/Pages/WebsitecreationandmanagementatCERN.aspx)
so it also makes the database writable by the AFS web server. For more details
on the commands run read the setup file.

```bash
$ git clone git@github.com:gdujany/Condorcet.git
$ cd Condorcet
$ chmod 755 setup.sh
$ ./setup.sh
```

Adapt  Condorcet/config.py to your needs, in particular change `APPLICATION_ROOT`.

Go to the [CERN AFS web configuration page](https://webservices.web.cern.ch/webservices/Tools/SiteConfiguration/) and enable CGI execution.

