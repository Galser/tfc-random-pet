# tfc-random-pet
Random Pet repo for a separate testing in TFC (for test later in remote state)

Follow-up repo for the skills map

# Main code

We prepare in this repo the code and then run state, to reference it in the next Lab task
- Code in [main.tf](main.tf)
  ```terraform
  resource "random_pet" "demo" { }

  output "demo" {
    value = "${random_pet.demo.id}"
  }
  ```
- Run :

  ```
  Terraform v0.13.5
  Initializing plugins and modules...
  random_pet.demo: Creating...
  random_pet.demo: Creation complete after 0s [id=ample-baboon]

  Warning: Interpolation-only expressions are deprecated

    on maint.tf line 4, in output "demo":
     4:   value = "${random_pet.demo.id}"

  Terraform 0.11 and earlier required all non-constant expressions to be
  provided via interpolation syntax, but this pattern is now deprecated. To
  silence this warning, remove the "${ sequence from the start and the }"
  sequence from the end of this expression, leaving just the inner expression.

  Template interpolation syntax is still used to construct strings from
  expressions when the template includes multiple interpolation sequences or a
  mixture of literal strings and interpolations. This deprecation applies only
  to templates that consist entirely of a single interpolation sequence.


  Apply complete! Resources: 1 added, 0 changed, 0 destroyed.

  Outputs:

  demo = ample-baboon
    
  ```

# TODO

- [x] - initial code
- [x] - run
