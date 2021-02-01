Ansible Role: RethinkDB
=========

This role is for you to install **RethinkDB**.  

If you want this role to support more applications, you can [**submit Issues**](https://github.com/websoft9dev/role_rethinkdb/issues/new/choose) for us.

## Requirements

Make sure these requirements need before the installation:

| **Items**      | **Details** |
| ------------------| ------------------|
| Operating system | CentOS7.x Ubuntu18.04 |
| Python version | Python2, Python3  |

## Related roles

This Role does not depend on other role variables in syntax, but it depend on other role before:

```
roles:
  - { role: role_common }
```

## Variables

The main variables of this Role and how to use them are as follows:

| **Items**      | **Details** | **Format**  | **Need to assignment** |
| ------------------| ------------------|-----|-----|
| rethinkdb_admin_username | e.g  admin | String | No |
| rethinkdb_admin_password | e.g  admin | String | No |


## Example

```
rethinkdb_admin_username: "admin"
```

## Resources

* [Documentation](https://support.websoft9.com/docs/rethinkdb)
* [Deploy by Image](https://apps.websoft9.com/rethinkdb)
* [Deploy by Script](https://github.com/websoft9/ansible-rethinkdb)

## License

[LGPL-3.0](/License.md), Additional Terms: It is not allowed to publish free or paid image based on this repository in any Cloud platform's Marketplace.

Copyright (c) 2016-present, Websoft9

## FAQ

#### Is there any web-based GUI tool for RethinkDB?

Yes, the RethinkDB have web-based GUI by default