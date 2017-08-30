[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/web?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/web/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)


[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

Search for x2x records in advanced search
=========================================

Standard behavior in advanced search for one2many, many2many and many2one fields is to do a `name_search`. This often is not satisfactionary as you might want to search for other properties. There might also be cases where you don't exactly know what you're searching for, then a list of possible options is necessary too. This module enables you to have a full search view to select the record in question, and either select specific records or select them using a search query of its own.

Installation
------------

Configuration
-------------

Usage
-----

=====

To use this module, you need to:

* open the advanced search options in a search view
* select a one2many, many2many or many2one field
* select operator `is equal to` or `is not equal to`
* the textfield changes to a many2one selection field where you can search for the record in question

To search for properties of linked records (ie invoices for customers with a credit limit higher than X):

* open the advanced search options in a search view
* select a one2many, many2many or many2one field
* select operator `is in selection`
* in the search view that pops up, select the criteria
* click `Use criteria`
* if you're only interested in certain records, mark them en click `Select`
* if you want to change your selection afterwards, click the search symbol right of the selection term

In both cases, don't forget to click `Apply` to actually execute the search.

Note that you can stack searching for properties: Simply add another advanced search in the selection search window. You can do this indefinetely, so it is possible to search for moves belonging to a journal which has a user who is member of a certain group etc.

For further information, please visit:

* https://www.odoo.com/forum/help-1

Known issues / Roadmap
----------------------

Bug Tracker
-----------

Credits
-------


[![Odoo Italia Associazione]]

### Contributors


* Holger Brunn <hbrunn@therp.nl>

### Funders

### Maintainer


.. image:: http://odoo-community.org/logo.png
    :alt: Odoo Community Association
    :target: http://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose mission is to support the collaborative development of Odoo features and promote its widespread use.

To contribute to this module, please visit http://odoo-community.org.

[//]: # (copyright)

----

**Odoo** is a trademark of [Odoo S.A.](https://www.odoo.com/) (formerly OpenERP, formerly TinyERP)

**OCA**, or the [Odoo Community Association](http://odoo-community.org/), is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

**zeroincombenze®** is a trademark of [SHS-AV s.r.l.](http://www.shs-av.com/)
which distributes and promotes **Odoo** ready-to-use on its own cloud infrastructure.
[Zeroincombenze® distribution](http://wiki.zeroincombenze.org/en/Odoo)
is mainly designed for Italian law and markeplace.
Everytime, every Odoo DB and customized code can be deployed on local server too.

[//]: # (end copyright)

[//]: # (addons)

[//]: # (end addons)

[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
