[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/web?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/web/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)

Dashboard Tiles
===============

Adds a dashboard where you can configure tiles from any view and add them as short cut.

By default, the tile displays items count of a given model restricted to a given domain.

Optionally, the tile can display the result of a function on a field.

- Function is one of `sum`, `avg`, `min`, `max` or `median`.
- Field must be integer or float.

Tile can be:

- Displayed only for a user.
- Global for all users.
- Restricted to some groups.

*Note: The tile will be hidden if the current user doesn't have access to the given model.*

Installation
------------



Configuration
-------------



Usage
-----

-----

-----

=====

* Dashboad sample, displaying Sale Orders to invoice:

.. image:: ./static/src/img/screenshot_dashboard.png

* Tree view displayed when user click on the tile:

.. image:: ./static/src/img/screenshot_action_click.png

Known issues
* Can not edit tile from dashboard (color, sequence, function, ...).
* Original context is ignored.
* Original domain and filter are not restored.
* To preserve a relative date domain, you have to manually edit the tile's domain from `Configuration > User Interface > Dashboard Tile`. You can use the same variables available in filters (`uid`, `context_today()`, `current_date`, `time`, `datetime`, `relativedelta`).

Roadmap
* Add icons.
* Support client side action (like inbox).
* Restore original Domain + Filter when an action is set.
* Posibility to hide the tile based on a field expression.
* Posibility to set the background color based on a field expression.

Known issues / Roadmap
----------------------



Bug Tracker
-----------




Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/web/issues/new?body=module:%20web_dashboard_tile%0Aversion:%208.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.


Credits
-------




[![Odoo Italia Associazione]]



### Contributors




* Markus Schneider <markus.schneider at initos.com>
* Sylvain Le Gal (https://twitter.com/legalsylvain)
* Iván Todorovich <ivan.todorovich@gmail.com>

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
