node-geonames
=============

[![codecov.io](https://codecov.io/github/nelsonic/node-geonames-client/coverage.svg?branch=master)](https://codecov.io/github/nelsonic/node-geonames-client?branch=master)


[Geonames.org] (http://www.geonames.org) API client for NodeJs

#Install

npm install node-geonames-client

#Required Environment Variable

Before running your test you've to set the NGN_USERNAME environment variable to your geonames.org username,
or pass a commandline param --username={yourusername}

    var opts = {
        'username': argh.argv.username || process.env.NGN_USERNAME
    };

To export your username as an environment variable:

    export NGN_USERNAME=yourusername

# Usage

```js
var opts = {
    'username': argh.argv.username || process.env.NGN_USERNAME
};

var geonames = require('node-geonames-client')({username: opts.username});
geonames.postalCodeLookup({postalCode : '3580', countryCode : 'BE', maxRows : 20}, function (err, res) {
  // handle the err
  // use the res (response data)
});
```

# Geonames Account Setup

First ensure that you have signed up for a Geonames account:
[http://www.geonames.org/login](http://www.geonames.org/login)

Next, ensure that you have enabled the "***Free Web Service***" for your Geonames account:

Go to: http://www.geonames.org/manageaccount and scroll to the bottom of the page
![geonames-manageaccount-enable-free-web-services](https://cloud.githubusercontent.com/assets/194400/14138582/d8d31c58-f665-11e5-953a-82f272b1b53b.png)
you will see a link "[Click here to enable](http://www.geonames.org/enablefreewebservice)" click it.

Once enabled you should see a confirmation message:
![geonames-free-webservice-enabled](https://cloud.githubusercontent.com/assets/194400/14138588/e3e6aed4-f665-11e5-91ca-555c7c684325.png)

Now everything should work as expected.

# Tests

to run the tests for this project execute the following command in your terminal:

```sh
npm test
```
