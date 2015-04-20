# loopback-example-passport
This repo is a fork of https://github.com/strongloop/loopback-example-passport

The purpose of this fork is to test implementation of a passport that supports LDAP.

Currently the passport strategi used is https://github.com/vesse/passport-ldapauth

All credit for getting the basics done too https://github.com/PierreGambarotto
- https://github.com/strongloop/loopback-component-passport/pull/44

Current work is that there is identified at least two use case for LDAP

Authentication against OpenLDAP and Microsoft AD (via LDAP).

In order to ensure a clean testing ground, the included providers.json.template has two definitions, ms-ad and openldap.

In order to ensure that there is the greatest flexibility in testing, the two definitions for ms-ad and openldap have different provider values

providerType (a normalised provider from the provider.json) is available to create a switch from if nesessary.

Status:
- ms-ad authentication works for Owen
- openldap works for Pierre
- The whole subject of authorization is yet to be checked.
- Linked accounts...Needed? The LDAP is for internal access such that one can control access without depending on local accounts

WARNING:
- the package.json includes a forked version of loopback-component-passport: https://github.com/OwenBrotherwood/loopback-component-passport

Notes:
- providers.json.template: contains an example config for LDAP
- Anonymous Bind and not allowed: some Microsoft AD Installations do not allow anonymous bind
- Bind: if the Bind credentials are wrong, no log so watch out
