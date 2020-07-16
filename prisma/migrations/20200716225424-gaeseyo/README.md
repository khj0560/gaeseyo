# Migration `20200716225424-gaeseyo`

This migration has been generated at 7/16/2020, 10:54:24 PM.
You can check out the [state of the schema](./schema.prisma) after the migration.

## Database Steps

```sql
CREATE TABLE "gaeseyo_dev"."User" (
"id" SERIAL,
"userId" text  NOT NULL ,
    PRIMARY KEY ("id"))

CREATE UNIQUE INDEX "User.userId" ON "gaeseyo_dev"."User"("userId")
```

## Changes

```diff
diff --git schema.prisma schema.prisma
migration ..20200716225424-gaeseyo
--- datamodel.dml
+++ datamodel.dml
@@ -1,0 +1,13 @@
+datasource db {
+  provider = "postgresql"
+  url = "***"
+}
+
+generator client {
+  provider = "prisma-client-js"
+}
+
+model User {
+  id Int @id @default(autoincrement())
+  userId String @unique
+}
```


