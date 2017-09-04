[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/web?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/web/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)

Add Tiles to Dashboard
======================

module to give you a dashboard where you can configure tile from any view
and add them as short cut.

* Tile can be:
    * displayed only for a user;
    * global for all users (In that case, some tiles will be hidden if
      the current user doesn't have access to the given model);
* The tile displays items count of a given model restricted to a given domain;
* Optionnaly, the tile can display the result of a function of a field;
    * Function is one of sum/avg/min/max/median;
    * Field must be integer or float;

Installation
------------


Configuration
-------------


Usage
-----

-----

=====

* Dashboad sample, displaying Sale Orders to invoice:
.. image:: /web_dashboard_tile/static/src/img/screenshot_dashboard.png
* Tree view displayed when user click on the tile:
.. image:: /web_dashboard_tile/static/src/img/screenshot_action_click.png

Known issues / Roadmap
----------------------



* Can not edit tile from dashboard (color, sequence, function, ...);
* Context are ignored;
* Date filter can not be relative;
* Combine domain of menue and filter so can not restore origin filter;
* Support context_today;
* Add icons;
* Support client side action (like inbox);

Bug Tracker
-----------



Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/
web/issues/new?body=module:%20
web_dashboard_tile%0Aversion:%20
8.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.


Credits
-------



[![Odoo Italia Associazione]]


### Contributors



* Markus Schneider <markus.schneider at initos.com>
* Sylvain Le Gal (https://twitter.com/legalsylvain)

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
