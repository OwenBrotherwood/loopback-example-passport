# loopback-example-passport


WITH LDAP :)
- Or at least one can be authenticated
- The whole subject of authorization is yet to be checked.
- I note that on rendering of auth/account, the banner partial has an undefined for user.username
- Linked accounts...Needed? The LDAP is for internal access such that one can control access without depending on local accounts

Notes:
passport-configurator.js: the version in the root of this repo is changed from the presently available version
providers.json.template: contains an example config for LDAP
Anonymous Bind and not allowed: some Microsoft AD Installations do not allow anonymous bind
Bind: if the Bind credentials are wrong, no log so watch out
SearchFilter: is important.

br Owen Brotherwood
 
All credit for getting the basics done too https://github.com/PierreGambarotto


LoopBack example for [loopback-passport](https://github.com/strongloop/loopback-passport) module. It demonstrates how to use
LoopBack's user/userIdentity/userCredential models and [passport](http://passportjs.org) to interact with other auth providers.

- Log in or sign up to LoopBack using third party providers (aka social logins)
- Link third party accounts with a LoopBack user (for example, a LoopBack user can have associated facebook/google accounts to retrieve pictures).

# How to run the application

```
git clone git@github.com:strongloop/loopback-example-passport.git
cd loopback-example-passport
npm install
```

## Get your client ids/secrets from facebook & google

- https://developers.facebook.com/apps
- https://console.developers.google.com/project

## Create providers.json

- Copy providers.json.template to providers.json
- Update providers.json with your own values for clientID/clientSecret

## Run the application

```
node . 
```

Open your browser to http://127.0.0.1:3000

