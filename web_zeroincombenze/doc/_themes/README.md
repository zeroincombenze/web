[![Build Status](https://travis-ci.org/zeroincombenze/_themes.svg?branch=7.0)](https://travis-ci.org/zeroincombenze/_themes)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/_themes/badge.svg?branch=7.0)](https://coveralls.io/github/zeroincombenze/_themes?branch=7.0)
[![codecov](https://codecov.io/gh/zeroincombenze/_themes/branch/7.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/_themes/branch/7.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-7.svg)](https://github.com/OCA/_themes/tree/7.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-7.svg)](http://wiki.zeroincombenze.org/en/Odoo/7.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-7.svg)](http://erp7.zeroincombenze.it)


[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

Flask Sphinx Styles
===================

This repository contains sphinx styles for Flask and Flask related
projects.  To use this style in your Sphinx documentation, follow
this guide:

1. put this folder as _themes into your docs folder.  Alternatively
   you can also use git submodules to check out the contents there.
2. add this to your conf.py:

   sys.path.append(os.path.abspath('_themes'))
   html_theme_path = ['_themes']
   html_theme = 'flask'

The following themes exist:

- 'flask' - the standard flask documentation theme for large
  projects
- 'flask_small' - small one-page theme.  Intended to be used by
  very small addon libraries for flask.

The following options exist for the flask_small theme:

   [options]
   index_logo = ''              filename of a picture in _static
                                to be used as replacement for the
                                h1 in the index.rst file.
   index_logo_height = 120px    height of the index logo
   github_fork = ''             repository name on github for the
                                "fork me" badge

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
