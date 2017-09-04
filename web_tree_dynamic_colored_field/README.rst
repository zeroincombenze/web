[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/web?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/web/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)

Colorize field in tree views
============================

This module aims to add support for dynamically coloring fields in tree view
according to data in the record.

It provides attributes on fields with the same syntax as the 'colors' attribute
in tree tags.

Further, it provides a ``color_field`` attribute on tree tags to use a field's
value as color.

Features

* Add attribute ``bg_color`` on fields to color background of a cell in tree view

* Add attribute ``fg_color`` on fields to change text color of a cell in tree view

* Add attribute ``color_field`` on the tree element to use as color


Installation
------------


Configuration
-------------


Usage
-----

-----

=====

* In the tree view declaration, put bg_color="red:customer==True;" attribute in the field tag::

    ...
    <field name="arch" type="xml">
        <tree string="View name">
            ...
            <field name="name" bg_color="red:customer==True;"/>
            ...
        </tree>
    </field>
    ...
    
    With this example, column which renders 'name' field will have its background colored in red.

* In the tree view declaration, put fg_color="white:customer==True;" attribute in the field tag::

    ...
    <field name="arch" type="xml">
        <tree string="View name">
            ...
            <field name="name" fg_color="white:customer==True;"/>
            ...
        </tree>
    </field>
    ...
    
    With this example, column which renders 'name' field will have its text colored in white.

* In the tree view declaration, use color_field="color" attribute in the tree tag::

    ...
    <field name="arch" type="xml">
        <tree string="View name" color_field="color">
            ...
            <field name="color" invisible="1" />
            ...
        </tree>
    </field>
    ...

    With this example, the content of the field named `color` will be used to
    populate the `color` CSS value. Use a function field to return whichever
    color you want depending on the other record values. Note that this
    overrides the `colors` attribute, and that you need the tree to load your
    field in the first place by adding it as invisible field.

Known issues / Roadmap
----------------------


Bug Tracker
-----------



Bugs are tracked on `GitHub Issues
<https://github.com/OCA/web/issues>`_. In case of trouble, please
check there if your issue has already been reported. If you spotted it first,
help us smashing it by providing a detailed and welcomed feedback.

Credits
-------



[![Odoo Italia Associazione]]


### Contributors



* Damien Crier <damien.crier@camptocamp.com>
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
