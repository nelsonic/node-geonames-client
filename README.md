node-geonames
=============

[Geonames] (http://www.geonames.org) API client for NodeJs

create your geonames [user account](http://www.geonames.org/login):

#Install

npm install node-geonames-client

#Tests

Before running your test you've to set the NGN_USERNAME environment variable to your geonames.org username,
or pass a commandline param --username={yourusername}

    var opts = {
        'username': argh.argv.username || process.env.NGN_USERNAME
    };


# Trouble Shooting

Ensure that you have enabled the "Free Web Service" for your Geonames account:

Go to: http://www.geonames.org/manageaccount and scroll to the bottom of the page
![geonames-manageaccount-enable-free-web-services](https://cloud.githubusercontent.com/assets/194400/14138582/d8d31c58-f665-11e5-953a-82f272b1b53b.png)
you will see a link "[Click here to enable](http://www.geonames.org/enablefreewebservice)" click it.

Once enabled you should see a confirmation message:
![geonames-free-webservice-enabled](https://cloud.githubusercontent.com/assets/194400/14138588/e3e6aed4-f665-11e5-91ca-555c7c684325.png)

Now everything should work as expected.
