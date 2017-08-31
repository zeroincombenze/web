[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=7.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=7.0)](https://coveralls.io/github/zeroincombenze/web?branch=7.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/7.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/7.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-7.svg)](https://github.com/OCA/web/tree/7.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-7.svg)](http://erp7.zeroincombenze.it)


[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

.. image:: https://img.shields.io/badge/licence-AGPL--3-blue.svg
================================================================
    :alt: License: AGPL-3

Raise warning when saving

This module was written to extend the functionality of saving a record in the web interface.

/!\\/!\\/!\\

In no way this module stops the save of the record. You must consider this as a warning displayed 
to the user AFTER save completed.

/!\\/!\\/!\\

If you don't want Odoo to save the record, you should use constraints.

Installation
------------

Configuration
-------------

Usage
-----

=====

To use this module, you need to:

* write a method called 'check_warning_on_save' which will make some checks and return a string

example :

.. code:: python

    def check_warning_on_save(self, cr, uid, id, context=None):
        """
            @param: int: record_id
            @return: string: message that should be displayed to the user
        """
        res = ""

        record = self.browse(cr, uid, id, context=context)
        # ... make some checks

        return res

For further information, please visit:

* https://www.odoo.com/forum/help-1


Known issues / Roadmap
----------------------

Bug Tracker
-----------


Bugs are tracked on `GitHub Issues <https://github.com/OCA/{project_repo}/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/web/issues/new?body=module:%20web_warning_on_save%0Aversion:%207.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.


Credits
-------


[![Odoo Italia Associazione]]

### Contributors


* Damien Crier <damien.crier@camptocamp.com>
* Vincent Renaville <vincent.renaville@camptocamp.com>

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
