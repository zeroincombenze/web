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


Timepicker widget in form views

This module provides a timepicker widget for float fields.
It can be used as a replacement for the standard float_time widget in form views.


|picker|


The widget has the following default timepicker options:

* the possible selection is based on 15 minute interval (step: 15)
* 24 hour mode in H:i format (timeFormat: 'H:i')
* scroll selection starts at current time (scrollDefault: 'now')


|formview|


Installation
------------

Configuration
-------------

Usage
-----

=====

In the form view declaration, put widget='timepicker' attribute in the field tag::

    ...
    <field name="arch" type="xml">
        <form string="View name">
            ...
            <field name="name"/>
            <field name="mytimefieldname" widget="timepicker"/>
            ...
        </form>
    </field>
    ...

Additional jquery-timepicker plugin options can be specified by an options attribute::

    ...
    <field name="mytimefieldname" widget="timepicker" options="{'step': '30', 'disableTextInput': false}"/>
    ...

See the available options at `jquery-timepicker <https://github.com//jonthornton//jquery-timepicker#timepicker-plugin-for-jquery>`_.

.. |picker| image:: ./images/picker.png
.. |formview| image:: ./images/form_view.png


Known issues / Roadmap
----------------------


* No validation on options.


Bug Tracker
-----------

Credits
-------


* The module uses the `jquery-timepicker <https://cdnjs.com//libraries//jquery-timepicker>`_ plugin by Jon Thornton. This software is made available under the open source MIT License. © 2014 Jon Thornton and contributors

* Odoo Community Association (OCA)


[![Odoo Italia Associazione]]

### Contributors


* Michael Fried <Michael.Fried@vividlab.de>

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
