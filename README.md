# cypress-downloadfile

[![npm version](https://badge.fury.io/js/cypress-downloadfile.svg)](https://badge.fury.io/js/cypress-downloadfile)
 
This is a Cypress custom file download command.

This repository is not maintained by the Cypress developers. 

## Installation

Install the module.

```shell
npm install cypress-downloadfile
```

Add the following line to `cypress/support/commands.js`.

```javascript
require('cypress-downloadfile/lib/downloadFileCommand')
```

Add the following lines to `cypress/plugins/index.js`.

```javascript
const {downloadFile} = require('cypress-downloadfile/lib/addPlugin')
module.exports = (on, config) => {
  on('task', {downloadFile})
}
```

If autocompletion does not work out of the box you can add the following line above your testfile

```javascript
/// <reference types="cypress-downloadfile"/>
```


## Example of command
```javascript
cy.downloadFile('https://library.concordia.ca/help/technology/recovering_saved_files.pdf','mydownloads','demo.pdf')
```

