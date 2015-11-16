---

title: 'Create the database schema'
weight: 40

menu:
  main:
    name: "Create the database schema"
    identifier: "installation-guide-full-wls-database"
    parent: "installation-guide-full-wls"
    pre: "Create the database schema."

---

With the pre-packaged distribution, you can use the auto-creation function to create the necessary database tables. However, in production or QA this might not be desirable.

There are two possibilities at which the tables get created:

1. During the first startup of the engine, the engine checks and creates the tables itself automatically. This is not typically used for productive environments, as the Camunda database user needs CREATE rights for this.

2. You can manually create the tables yourself. You can find the necessary DDL scripts in the `$WLS_DISTRIBUTION\sql\create\` folder.

When you create the tables manually, then you can also configure the engine to **not** create tables at startup by setting the `databaseSchemaUpdate` property to `false` (or, in case you are using Oracle, to `noop`). In WebLogic, this is done in the `bpm-platform.xml`, located in the `$WLS_HOME\modules\camunda-oracle-weblogic-ear-$VERSION.ear\camunda-oracle-weblogic-service.jar\META-INF\` folder.

{{< note title="Heads Up!" class="info" >}}
If you have defined a specific prefix for the entities of your database, then you will have to manually adjust the `create` scripts accordingly so that the tables are created with the prefix.
{{< /note >}}