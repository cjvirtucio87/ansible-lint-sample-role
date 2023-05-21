# ansible-lint-sample-role
Sample role to reproduce issue with `no-role-prefix` warning.

## Steps to reproduce
1. Clone this repo.
1. Run ansible-lint:
    ```console
    ansible-lint **/*
    ```

## Expected Outcome
Only unrelated warnings about casing and unsafe file permissions.

## Actual Outcome
```txt
var-naming[no-role-prefix]: Variables names from within roles should use role_name_ as a prefix. (vars: __file__)
roles/foo/tasks/main.yml:13 Task/Handler: setup rc file

var-naming[no-role-prefix]: Variables names from within roles should use role_name_ as a prefix. (vars: __line__)
roles/foo/tasks/main.yml:13 Task/Handler: setup rc file
```
