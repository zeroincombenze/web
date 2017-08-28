[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/web?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/web/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)


[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
================================================================
   :alt: License: AGPL-3

Formulas in Float Fields

This module allows the use of simple math formulas in integer/float fields 
(e.g. "=45 + 4/3 - 5 * (2 + 1)").

* Only supports parentheses, decimal points, thousands separators, and the 
  operators "+", "-", "*", and "/"
* Will use the decimal point and thousands separator characters associated 
  with your language
* If the formula is valid, the result will be computed and displayed, and the 
  formula will be stored for editing
* If the formula is not valid, it's retained in the field as text

**Technical Details**

* Overloads web.form_widgets.FieldFloat (so it works for fields.integer & 
  fields.float)
* Uses the eval() JS function to evaluate the formula
* Does not do any rounding (this is handled elsewhere)
* Avoids code injection by applying strict regex to formula prior to eval() 
  (e.g. "=alert('security')" would not get evaluated)

Installation
------------


To install this module, simply follow the standard install process.

Configuration
-------------


No configuration is needed or possible.

Usage
-----

=====

Install and enjoy. A short demo video can be found at 
http://www.youtube.com/watch?v=jQGdD34WYrA.

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/162/9.0

Known Issues / Roadmap

Known issues / Roadmap
----------------------

Bug Tracker
-----------


Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smash it by providing detailed and welcomed 
feedback.

Credits
-------


[![Odoo Italia Associazione]]

### Contributors


* Sylvain Le Gal (https://twitter.com/legalsylvain)
* Oleg Bulkin <o.bulkin@gmail.com>

### Funders

### Maintainer


.. image:: http://odoo-community.org/logo.png 
   :alt: Odoo Community Association
   :target: http://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose 
mission is to support the collaborative development of Odoo features and 
promote its widespread use.

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
