# Create database and user

In the `mongo` container, run the following commands:

```sh
mongosh mongodb://<USERNAME>:<PASSWORD>@localhost
# dropped in the mongosh shell
use <DATABASE_NAME>  # the user will be "bound" to this database
db.createUser({user: "<NEW_USER>", pwd: "<PASSWORD>", roles: [{ role: "readWrite", db: "<DATABASE_NAME>" }]})
```
