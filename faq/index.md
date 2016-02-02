---
layout: default
title: FAQ
description: frequently asked questions
keywords: faq, questions, problems, solutions
---

# Frequently Asked Questions

[Which Standard Does PyWPS Support?](#which-standard-does-pywps-support)

[What is PyWPS-4 About?](#what-is-pywps-4-about)

[Which Version of PyWPS Should I Use?](#which-version-of-pywps-should-i-use)

[How do I Debug PyWPS Processes?](#how-do-i-debug-pywps-processes)

[How do I Run Command Line Commands?](#how-do-i-run-command-line-commands)

[How do I Run GRASS commands?](#how-do-i-run-grass-commands)

[Where Can I Find Documentation on Process Writing in General?](#where-can-i-find-documentation-on-process-writing-in-general)

[How do I Cite PyWPS Software?](#how-do-i-cite-pywps-software)


## Which Standard Does PyWPS Support?

PyWPS (any version) supports the OGC WPS 1.0.0 standard.

PyWPS < 4 does not currently support 2.0.0 version.

PyWPS 4 will support OGC:WPS 2.0.0 and contains partial features in support of OGC WPS 2.0.0.

## What is PyWPS-4 About?

PyWPS-4 is a complete rewrite in support of the OGC WPS standard.  It has a completely different codebase compared to previous (3.x) versions.

PyWPS-4 supports both Python 2.x and Python 3.x versions.  It uses Flask, lxml and other modern libraries for web application development.  The processes are not backwards compatible, but the code should be easy to port (the philosophy remains the same).

## Which Version of PyWPS Should I Use?

As a general rule, use the latest stable version.  Older versions (1.0.0, 2.0.x) are no longer supported.

Current stable means PyWPS 3.2 or the master branch in the PyWPS repository.

PyWPS-4 is under heavy development, the OGC WPS standard is not fully implemented yet.

## How do I Debug PyWPS Processes?

- Run PyWPS from command line directly from command line:

```bash
./wps.py "&service=wps&version=0.4.0&request=execute&datainputs=input1,value1,input2,value2,..."
```

- Inspect the web server's error log:

```bash
tail -f /var/log/apache/error.log |sed -e "s/\[.*\] //g"
PyWPS GCmd: r.rescale out=kat_dop_k_2004_1188372842 in=dop_k_2004_1188372842\
        to=0,255 to kat_dop_k_2004_1188372842[0,255]
PyWPS GCmd: r.support map=dop_k_2004_1188372842 title="drasil2"
PyWPS GCmd: r.support map=kat_dop_k_2004_1188372842 title="drasil2"
PyWPS ERROR: Could not perform command:
        r.support map=kat_dop_k_2004_1188372842 title="drasil2"
        in process K2O, method execute() /home/bnhelp/pfwps/wps.py:
            79: DeprecationWarning:
                Non-ASCII character '\xc2' in file
                /usr/home/bnhelp/pfwps/pywps/processes/pf_interpolate_grass.py
                on line 51, but no encoding declared;
        see http://www.python.org/peps/pep-0263.html for details
from pywps.processes import *
PyWPS GCmd: g.region rast=mask2004@medlov res=5 1>&2
```

- See the log file, which you have set in the configuration file, in the `[server]` section

## How do I Run Command Line Commands?

Use the built-in `cmd()` method of the process:

```python
self.cmd(['ogr2ogr','output','input'])
```
## How do I Run GRASS Commands?

The same way, like normal commands:

```python
self.cmd(['g.region','rast=raster'])
```

## Where Can I Find Documentation on Process Writing in General?

Of course, there is Documentation, but it does not contain modules documentation yet. To get this, try:

```bash
pydoc pywps/Process/Process.py
pydoc pywps/Process/InputsAndOutputs.py
```

## How do I Cite PyWPS Software?

- PyWPS Development Team, 2009. Python Web Processing Service (PyWPS)
  - Software, Version XXXX. <http://pywps.org>

- Cepicky, J. (2007): PyWPS 2.0.0: The presence and the future.
  - Proceedings Geoinformatics FCE CTU 2007,Prague, Czech Republic, 19th Sept. 2007, Electronic document PDF: <https://ojs.cvut.cz/ojs/index.php/gi/article/download/gi.2.8/2583>

- Cepicky, J., and Becchi, L., 2007, Geospatial Processing via
  - Internet on Remote Servers – PyWPS. OSGeo Journal, 1, 39-42. <http://www.osgeo.org/journal>
