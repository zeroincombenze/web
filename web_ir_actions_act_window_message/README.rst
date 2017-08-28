[![Build Status](https://travis-ci.org/zeroincombenze/web.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/web)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/web/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/web?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/web/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/web/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/web/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)


[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

Client side message boxes
=========================

This module allows to show a message popup on the client side as result of a button.

Installation
------------

Configuration
-------------

Usage
-----

=====

Depend on this module and return

.. code:: python

    {
        'type': 'ir.actions.act_window.message',
        'title': _('My title'),
        'message': _('My message'),
        # optional title of the close button, if not set, will be _('Close')
        # if set False, no close button will be shown
        # you can create your own close button with an action of type
        # ir.actions.act_window_close
        'close_button_title': 'Make this window go away',
        # Use HTML instead of text
        'is_html_message': True,
        # this is an optional list of buttons to show
        'buttons': [
            # a button can be any action (also ir.actions.report.xml et al)
            {
                'type': 'ir.actions.act_window',
                'name': 'All customers',
                'res_model': 'res.partner',
                'view_mode': 'form',
                'views': [[False, 'list'], [False, 'form']],
                'domain': [('customer', '=', True)],
            },
            # or if type == method, you need to pass a model, a method name and
            # parameters
            {
                'type': 'method',
                'name': _('Yes, do it'),
                'model': self._name,
                'method': 'myfunction',
                # list of arguments to pass positionally
                'args': [self.ids],
                # dictionary of keyword arguments
                'kwargs': {'force': True},
                # button style
                'classes': 'btn-primary',
            }
        ]
    }

You are responsible for translating the messages.

Known issues / Roadmap
----------------------


* add `message_type` to differenciate between warnings, errors, etc.
* have one `message_type` to show a nonmodal warning on top right


Bug Tracker
-----------


Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed feedback
`here <https://github.com/OCA/web/issues/new?body=module:%20web_ir_actions_act_window_message%0Aversion:%208.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.


Credits
-------


[![Odoo Italia Associazione]]

### Contributors


* Holger Brunn <hbrunn@therp.nl>
* Zakaria Makrelouf (ACSONE SA/NV) <z.makrelouf@gmail.com>
* Benjamin Willig (ACSONE SA/NV) <benjamin.willig@acsone.eu>

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
