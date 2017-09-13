[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/web?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/web/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)

.. image:: https://img.shields.io/badge/licence-AGPL--3-blue.svg
================================================================
   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
   :alt: License: AGPL-3

More completion options for datetime fields

This module was written to extend the offers shown to the user when starting
to fill in a date. In standard odoo, the only offer is the date at 00:00:00
hours, while it can be convenient for the user to have other options, too.
When searching for the end of a period, ``23:59:59`` would come to mind, and
there also might be domain specific times that make sense.

Installation
------------



Configuration
-------------




If you do nothing, only the time ``23:59:59`` is added to the completion
dropdown.

In your code, you can add an options dictionary with a key
``completion_options`` which contains a list if dictionaries detailing the
offsets that should be added to the parsed date, like::

<field name="my_datetime_field" options="{'completion_options': [{'hours': 12, 'minutes': 30, 'seconds': 0}]}" />

which would offer to search for the date at half past twelve. Note that when
you set ``completion_options``, you have to list all options you want to see,
as the standard options will be replaced with your list.

Usage
-----

-----

-----

=====

Start filling in your date in a search field and choose one of the additional
options offered.

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/162/8.0

Known issues / Roadmap
----------------------



Bug Tracker
-----------




Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and
welcomed feedback
`here <https://github.com/OCA/web/issues/new?body=module:%20
web_search_datetime_completion%0Aversion:%20
8.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Credits
-------




[![Odoo Italia Associazione]]



### Contributors




* Holger Brunn <hbrunn@therp.nl>

### Funders

### Maintainer






.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

To contribute to this module, please visit https://odoo-community.org.

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
