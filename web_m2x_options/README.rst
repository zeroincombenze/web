[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=7.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=7.0)](https://coveralls.io/github/zeroincombenze/web?branch=7.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/7.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/7.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-7.svg)](https://github.com/OCA/web/tree/7.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-7.svg)](http://erp7.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)

==================================
==================================
Add new options for many2one field
==================================


Description

This module changes "many2one" and "many2manytags" form widgets, so as to
add some new display control options.

** New: support many2manytags widget ! **

** New: support global option management with ir.config_parameter ! **

The options provided include the possibility to remove "Create..." and/or
"Create and Edit..." entries from many2one and many2many drop down lists. You
can also change the default number of entries appearing in the drop-down, or
prevent the dialog box popping in case of validation error occurring.

If not specified, the module will avoid proposing any of the create options
if the current user have no permission rights to create the related object.


Requirements

Was tested on openerp v7.0


New option

``create`` *boolean* (Default: depends if user have create rights)

  Whether to display the "Create..." entry in dropdown panel.

``create_edit`` *boolean* (Default: depends if user have create rights)

  Whether to display "Create and Edit..." entry in dropdown panel

``m2o_dialog`` *boolean* (Default: depends if user have create rights)

  Whether to display the many2one dialog in case of validation error.

``limit`` *int* (Default: openerp default value is ``7``)

  Number of displayed record in drop-down panel

``search_more`` *boolean* 

  Used to force disable/enable search more button.
  
``field_color`` *string*

  A string to define the field used to define color.
  This option has to be used with colors.
  
``colors`` *dictionary*

  A dictionary to link field value with a HTML color.
  This option has to be used with field_color.
  



ir.config_parameter options

Now you can disable "Create..." and "Create and Edit..." entry for all widgets in the odoo instance.
If you disable one option, you can enable it for particular field by setting "create: True" option directly on the field definition.

``web_m2x_options.create`` *boolean* (Default: depends if user have create rights)

  Whether to display the "Create..." entry in dropdown panel for all fields in the odoo instance.

``web_m2x_options.create_edit`` *boolean* (Default: depends if user have create rights)

  Whether to display "Create and Edit..." entry in dropdown panel for all fields in the odoo instance.

``web_m2x_options.m2o_dialog`` *boolean* (Default: depends if user have create rights)

  Whether to display the many2one dialog in case of validation error for all fields in the odoo instance.

``web_m2x_options.limit`` *int* (Default: openerp default value is ``7``)

  Number of displayed records in drop-down panel for all fields in the odoo instance

``web_m2x_options.search_more`` *boolean* (Default: default value is ``False``)

  Whether the field should always show "Search more..." entry or not.

To add these parameters go to Configuration -> Technical -> Parameters -> System Parameters and add new parameters like:

- web_m2x_options.create: False
- web_m2x_options.create_edit: False
- web_m2x_options.m2o_dialog: False
- web_m2x_options.limit: 10
- web_m2x_options.search_more: True


ir.actions.act_window context options

The following options can be specified in the ``context`` field of an
``ir.actions.act_window`` to provide the same functionality at the form level:

``create`` *boolean* (Default: depends if user have create rights)

  Whether to display the "Create..." entry in dropdown panels.

``create_edit`` *boolean* (Default: depends if user have create rights)

  Whether to display the "Create and Edit..." entry in dropdown panels.

``m2o_dialog`` *boolean* (Default: depends if user have create rights)

  Whether to display the many2one dialog in case of validation error.

``limit`` *int* (Default: openerp default value is ``7``)

  Number of displayed records in drop-down panels.

``search_more`` *boolean*

  Whether to always display the "Search More..." entry in dropdown panels.


Example

Your XML form view definition could contain::

    ...
    <field name="partner_id" options="{'limit': 10, 'create': false, 'create_edit': false, 'search_more': true, 'field_color': 'state', 'colors': {'active':'green'}}"/>
    ...

Note
----

Double check that you have no inherited view that remote ``options`` you set on a field ! 
If nothing work, add a debugger in the first line of ``get_search_result`` method and enable debug mode in Odoo. When you write something in a many2one field, javascript debugger should pause. If not verify your installation.

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
