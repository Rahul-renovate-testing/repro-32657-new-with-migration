File Config

```js
...
  allowPostUpgradeCommandTemplating: true,
  allowedPostUpgradeCommands: ['echo modified > file.txt'],
```

Result for `pnpm config-validator`

```
$ pnpm config-validator

> renovate@0.0.0-semantic-release config-validator C:\Users\Acer\Desktop\renovate
> ts-node lib/config-validator.ts

 INFO: Validating renovate.json
 WARN: config.js needs migrating
       "originalConfig": {
         "token": "***********",
         "repositories": ["Rahul-renovate-testing/repro-32657-new-no-migration"],
         "allowPostUpgradeCommandTemplating": true,
         "allowedPostUpgradeCommands": ["echo modified > file.txt"],
         "repositoryCache": "disabled",
         "forkProcessing": "enabled",
         "binarySource": "global",
         "prHourlyLimit": 0,
         "prConcurrentLimit": 0
       },
       "migratedConfig": {
         "token": "***********",
         "repositories": ["Rahul-renovate-testing/repro-32657-new-no-migration"],
         "allowCommandTemplating": true,
         "allowedCommands": ["echo modified > file.txt"],
         "repositoryCache": "disabled",
         "forkProcessing": "enabled",
         "binarySource": "global",
         "prHourlyLimit": 0,
         "prConcurrentLimit": 0
       }
 INFO: Validating config.js
 INFO: Config validated successfully
```
