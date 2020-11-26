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
- Plan :
  ```

  ```
- Run :
  ```
  ```

# TODO

- [x] - initial code
- [ ] - run
