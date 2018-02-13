# terraform-shell-resource

This module runs a command as a `null_resource` and makes the stdout, stderr and exit status available as outputs (with temporary files stored in the module).

## Usage

See [test/main.tf](test/main.tf)

```
$ cd test
$ terraform init
$ terraform apply
  Apply complete! Resources: 2 added, 0 changed, 0 destroyed.

  Outputs:

  error = {
    exitstatus = 127

    stderr = /bin/sh: /bin/false: No such file or directory

    stdout =
  }
  stdout = {
    exitstatus = 0

    stderr =
    stdout = hello stdout

  }
```