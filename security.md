# High-Level Security Model

Overview of the high level roles required for the DevOps toolchains and other roles that would be recommended across the set of tools in place or to-be implemented.

### Authentication

The configuration and management of users should be done outside of the individual tools and done at the Active Directory level. 

This model relies on using Active Directory as a LDAP provider.

### Roles

As a starting point, these are the general point of authorization of levels of access. These are a basic set that can be applied in almost all cases and provide a good starting point.


 * Administrator - Tool Owner and Administrators
 * Team/Project lead - Implementors that required updates/add/deletes
 * Developer - Perform day to day activities
 * Observer/Auditor


These map directly to groups that we want to exist in the corporate directory.

### Team Management

For the future of supporting multiple teams and provide a separation of duties, ownership, and general isolation. For a fairly flat organization like eBiz this is not required day one, so we can defer this level of detail for now and implement these as the need arises, more likely when we look to implement a separation of duties in a deployment tool.
