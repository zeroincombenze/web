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
    :alt: License: AGPL-3

Support branding

If you run an Odoo support company and you support customers without an OPW,
you can brand the Odoo instance accordingly using this module. This module will
add a line `Supported by $yourcompany` in the menu footer and add a button to
mail exception messages to your support email address.


Installation
------------



Configuration
-------------




This module is controlled by config parameters:

support_branding.company_name
    Your company's name

support_branding.company_url
    Your company's website

support_branding.company_color
    The color to show your company's name in (CSS syntax)

support_branding.support_email
    The (optional) mailaddress to contact for support

support_branding.release
    The (optional) version number of your deployment

You probably want to depend on this module in your customer specific module and
add the following XML::

  <record id="support_branding.config_parameter_company_name" model="ir.config_parameter">
      <field name="value">Your company</field>
  </record>
  <record id="support_branding.config_parameter_company_url" model="ir.config_parameter">
      <field name="value">https://yourwebsite.com</field>
  </record>
  <record id="support_branding.config_parameter_company_color" model="ir.config_parameter">
      <field name="value">#000</field>
  </record>
  <record id="support_branding.config_parameter_support_email" model="ir.config_parameter">
      <field name="value">support@yourwebsite.com</field>
  </record>
  <record id="config_parameter_release" model="ir.config_parameter">
      <field name="value">42</field>
  </record>Configuration

Note that the email button is only visible if you configure an email address,
the default is empty!

Usage
-----

-----

-----

Known issues / Roadmap
----------------------



Bug Tracker
-----------




Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/web/issues/new?body=module:%20support_branding%0Aversion:%208.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.


Credits
-------




[![Odoo Italia Associazione]]



### Contributors




* Holger Brunn <hbrunn@therp.nl>
* Stefan Rijnhart <srijnhart@therp.nl>

Icon
----

* https://commons.wikimedia.org/wiki/File:Crystal_Clear_app_khelpcenter.png

### Funders

### Maintainer






.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

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
