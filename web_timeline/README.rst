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
    :alt: License: AGPL-3

Timeline view
=============

Define a new view displaying events in an interactive visualization chart.

The widget is based on the external library 
http://visjs.org/timeline_examples.html

Installation
------------





Configuration
-------------






You need to define a view with the tag <timeline> as base element. These are
the possible attributes for the tag:

* date_start (required): it defines the name of the field of type date that
  contains the start of the event.
* date_end (optional): it defines the name of the field of type date that
  contains the end of the event.
* date_delay (optional): it defines the name of the field of type date that
  contains the end of the event.
* default_group_by (required): it defines the name of the field that will be
  taken as default group by when accessing the view or when no other group by
  is selected.
* event_open_popup (optional): when set to true, it allows to edit the events
  in a popup. If not (default value), the record is edited changing to form
  view.
* colors (optional): it allows to set certain specific colors if the expressed
  condition (JS syntax) is met.

You also need to declare the view in an action window of the involved model.

Example:

.. code-block:: xml

    <?xml version="1.0" encoding="utf-8"?>
    <odoo>
        <record id="view_task_timeline" model="ir.ui.view">
            <field name="model">project.task</field>
            <field name="type">timeline</field>
            <field name="arch" type="xml">
                <timeline date_start="date_start"
                          date_stop="date_end"
                          string="Tasks"
                          default_group_by="user_id"
                          event_open_popup="true"
                          colors="#ec7063:user_id == false;#2ecb71:kanban_state=='done';">
                </timeline>
            </field>
        </record>

        <record id="project.action_view_task" model="ir.actions.act_window">
            <field name="view_mode">kanban,tree,form,calendar,gantt,timeline,graph</field>
        </record>
    </odoo>

Usage
-----







=====

For accessing the timeline view, you have to click on the button with the clock
icon in the view switcher. The first time you access to it, the timeline window
is zoomed to fit all the current elements, the same as when you perform a
search, filter or group by operation.

You can use the mouse scroll to zoom in or out in the timeline, and click on
any free area and drag for panning the view in that direction.

The records of your model will be shown as rectangles whose widths are the
duration of the event according our definition. You can select them clicking
on this rectangle. You can also use Ctrl or Shift keys for adding discrete
or range selections. Selected records are hightlighted with a different color
(but the difference will be more noticeable depending on the background color).
Once selected, you can drag and move the selected records across the timeline.

When a record is selected, a red cross button appears on the upper left corner
that allows to remove that record. This doesn't work for multiple records
although they were selected.

Records are grouped in different blocks depending on the group by criteria
selected (if none is specified, then the default group by is applied).
Dragging a record from one block to another change the corresponding field to
the value that represents the block. You can also click on the group name to
edit the involved record directly.

Double-click on the record to edit it. Double-click in open area to create a
new record with the group and start date linked to the area you clicked in.


.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/162/8.0

Known issues / Roadmap
----------------------






* Implement support for vis.js timeline range item addition (with Ctrl key
  pressed).
* Implement a more efficient way of refreshing timeline after a record update.

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






### Contributors






* Laurent Mignon <laurent.mignon@acsone.eu>
* Adrien Peiffer <adrien.peiffer@acsone.eu>
* Pedro M. Baeza <pedro.baeza@tecnativa.com>
* Leonardo Donelli <donelli@webmonks.it>

### Funders

### Maintainer










.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose mission is to support the collaborative development of Odoo features and promote its widespread use.

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
