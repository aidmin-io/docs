# Security Overview

In order for Aidmin to help you manage your database, we require that you share your database credentials with us. That means we have a great deal of responsibility to keep you safe, and we take this responsibility very seriously.

We only store data you provide to us to help you manage Aidmin, which is your users, data sources, and roles. Your database schema is stored in an in-memory cache (never stored at rest), and we never store any data, even in a cache, that is queried from your database.

## Full encryption

Whenever your data are in transit between you and us, everything is encrypted, and sent using HTTPS. Within our firewalled private networks, data may be transferred unencrypted.

All connections to databases that support encryption are always encrypted.

All data we store is encrypted at rest.

## We protect your credentials

Your database credentials (and any generated SSH private keys) are encrypted in our database with a key that is unique to each workspace. This information is also encrypted again when stored at rest. If an attacker was to get a copy of the full database, they would be unable to to see your database connection details.

Only users with the "Owner" role have permission to view your connection details decrypted in the connection editor.

## Abstractions over querying

When a user on Aidmin sends a query to your database, we first build an [AST](https://en.wikipedia.org/wiki/Abstract_syntax_tree) that describes the changes, then validate that the user has permission to make those changes, and then convert that AST into a query that is suited for the type of database you are using.

This layer of abstraction allows us to be confident that there can be no [SQL Injections](https://en.wikipedia.org/wiki/SQL_injection) and that the user can only perform actions they are allowed to.

## Physical Security

Our servers are hosted on Amazon Web Services, located in US data centers that are SOC 1, SOC 2 and ISO 27001 certified. Read more about [AWS Data Center Controls](https://aws.amazon.com/compliance/data-center/controls/).
