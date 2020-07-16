# Migration `20200716232319-test`

This migration has been generated at 7/16/2020, 11:23:19 PM.
You can check out the [state of the schema](./schema.prisma) after the migration.

## Database Steps

```sql
ALTER TABLE "gaeseyo_dev"."User" ADD COLUMN "address" text  NOT NULL ,
ADD COLUMN "shortAddress" text  NOT NULL ;
```

## Changes

```diff
diff --git schema.prisma schema.prisma
migration 20200716225424-gaeseyo..20200716232319-test
--- datamodel.dml
+++ datamodel.dml
@@ -1,7 +1,7 @@
 datasource db {
   provider = "postgresql"
-  url = "***"
+  url = "***"
 }
 generator client {
   provider = "prisma-client-js"
@@ -9,5 +9,7 @@
 model User {
   id Int @id @default(autoincrement())
   userId String @unique
+  address String
+  shortAddress String
 }
```


