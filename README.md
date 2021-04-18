# Aidmin - Your database helper.

Welcome to the temporary homepage for Aidmin.

https://user-images.githubusercontent.com/882228/115136839-3d4a5a00-9fd7-11eb-9dfa-567cf5d13f9b.mp4

[Higher Quality Demo](https://www.loom.com/share/961636d33578410baec67582cffb3411)

## Beta

The beta version of Aidmin can be found here: https://app.aidmin.io.

Aidmin is still in early development, and we'd love to get your feedback on which features are important to you. If you come across any bugs, please open an [issue](https://github.com/aidmin-io/aidmin/issues) against this repository and we'll be sure to address them in a timely manner. Similarly, if you'd like to submit a feature suggestion or have other ideas, please post in the [Discussion](https://github.com/aidmin-io/aidmin/discussions/categories/ideas) board.

## What problems does Aidmin solve?

Give's your organization access to the database. Every early stage startup has certain actions only developers can perform, because it is often the case that only they have access to the database. Aidmin provides a simple spreadsheet like interface that anyone can use, granular role based access, and a full audit log.

**Other features:**

- Make multiple changes to a table (including adding and deleting rows), preview the SQL it is going to run, and then execute it.
- Access to the database via SSO (Google only right now). Each user doesn't have to deal with connecting via a bastion host or having database credentials, and administrators don't have to worry about onboarding / offboarding access to bastion hosts and the databases themselves.
- You can have well defined roles (Support, Product, etc) with very granular access:
  - The Product team can toggle features, but not add or remove them.
  - The Support team can view your change data capture tables but only the metadata.
  - The Finance team can override billing details.
- Get a detailed log of queries that are run against your database. We tell you what kind of action was performed, who performed it, how long it took, along with relevant contextual data.
- Send deep links to filtered information inside a table.

**Coming soon:**

- Shared queries that will adapt to the role the user has.
- Talk to us about your needs at product@aidmin.io.

## Legal

- [Privacy Policy](https://github.com/aidmin-io/docs/blob/main/legal/privacy-policy.md)
- [Terms of Service](https://github.com/aidmin-io/docs/blob/main/legal/terms-of-service.md)

## Security

- [Security Overview](https://github.com/aidmin-io/docs/blob/main/security-overview.md)

## Documentation

- [SSH Tunneling](https://github.com/aidmin-io/docs/blob/main/docs/ssh-tunneling.md)
