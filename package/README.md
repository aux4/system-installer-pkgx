# system-installer-pkgx

The [aux4 system installer](/r/public/packages/aux4/pkger/commands/aux4/pkger/system) is used to manage packages by another package system. It is used to install and uninstall system packages.

```json
{
  "scope": "<scope>",
  "name": "<name>",
  "version": "<version>",
  ...
  "system": [
    ["pkgx:aws"],
    ["pkgx:jq"]
  ],
  "profiles": [
    ...
  ]
}
```

In this case when the *aux4 package is installed*, it will install the `aws` and `jq` packages using the `pkgx` package manager.

```sh
> pkgx install aws
```
```sh
> pkgx install jq
```

In the same way, when the *aux4 package is uninstalled*, it will uninstall `aws` and `jq` packages using the `pkgx` package manager (only if they are not used by another aux4 package).

```sh
> pkgx uninstall aws
```
```sh
> pkgx uninstall jq
```

Check out the [aux4 pkger system pkgx](commands/aux4/pkger/system/pkgx) command for more information.

