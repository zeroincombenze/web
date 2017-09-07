[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=7.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=7.0)](https://coveralls.io/github/zeroincombenze/web?branch=7.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/7.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/7.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-7.svg)](https://github.com/OCA/web/tree/7.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-7.svg)](http://erp7.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)

.. image:: https://img.shields.io/badge/licence-AGPL--3-blue.svg
================================================================
   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
   :alt: License: AGPL-3

Web Duplicate Visibility

This module allows to manage the visibility of duplicate button from the form
view declaration.

Installation
------------


Configuration
-------------


Usage
-----

-----

=====

While the default behavior of odoo is to display the duplicate button when user 
is allowed to create a new object. You are now able to remove duplicate button 
explicitly even if you are able to create new object::

   <record id="view_form_id" model="ir.ui.view">
      <field name="name">view name</field>
      <field name="model">my.model</field>
      <field name="priority" eval="10"/>
      <field name="arch" type="xml">
         <form string="..." duplicate="0">
         ...
         </form>
      </field>
    </record>

or by extending an existing view::

     <field name="arch" type="xml">
         <xpath expr="//form" position="attributes">
             <attribute name="duplicate">0</attribute>
         </xpath>
     </field>
     
Note that admin user has always access to Duplicate

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/repo/github-com-oca-web-162


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



Images

* Odoo Community Association: `Icon <https://github.com/OCA/maintainer-tools/blob/master/template/module/static/description/icon.svg>`_.

[![Odoo Italia Associazione]]


### Contributors



* Pierre Verkest <pverkest@anybox.fr>
* Christophe Combelles <ccomb@anybox.fr>
* Simon André <sandre@anybox.fr>
* Denis Roussel <denis.roussel@acsone.eu>

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
