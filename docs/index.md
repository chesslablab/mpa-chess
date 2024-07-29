# Website

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Contributing](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/dwyl/esta/issues)

Chess developers and business owners can now run their own open-source based platform more easily than ever before because the ChesslaBlab website is super-duper simple to install and set up. To give you an idea of its simplicity, the [assets/js](https://github.com/chesslablab/website/tree/main/assets/js) folder contains less than 3,000 lines of JavaScript code.

```text
cloc assets/js
      80 text files.
      80 unique files.                              
       0 files ignored.

github.com/AlDanial/cloc v 1.90  T=0.05 s (1474.8 files/s, 59028.2 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
JavaScript                      80            311             33           2858
-------------------------------------------------------------------------------
SUM:                            80            311             33           2858
-------------------------------------------------------------------------------
```

This is made possible with object-oriented programming (OOP) using [JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#importing_modules_using_import_maps). Now you can get rid of libraries and frameworks like React, Vue, Next.js, as well as transpilers, bundlers and so on. The ChesslaBlab website is written using OOP and the DOM.

## Standard Mode

The following repositories are required to run a complete chess platform using your own resources in standard mode:

- [Website](https://github.com/chesslablab/website)
- [PHP Chess Server](https://github.com/chesslablab/chess-server)
- [PHP Chess API](https://github.com/chesslablab/chess-api)
- [Chess Data](https://github.com/chesslablab/chess-data)

It is recommended to run the platform using four different servers on production, one per repository, especially if your site is expected to hit a significant amount of visits. However, everything can be run on a humble machine. In fact, the documentation examples are run in a development environment using these ports for each of the repositories, respectively.

- 443
- 8443
- 9443
- 3306

Remember, this is because multiple applications can't listen on the same port on the same host.

## Decentralized Mode

Decentralized mode allows to run a complete chess platform using one repository only:

- [Website](https://github.com/chesslablab/website)

Make sure to add at least one API endpoint as well as a WebSocket host from the ChesslaBlab node list in your `assets/env.js` file.