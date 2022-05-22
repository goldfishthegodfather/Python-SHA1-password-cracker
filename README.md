![Badge tracking project size](https://img.shields.io/github/repo-size/Preffet/Python-SHA1-password-cracker?color=%2377009e)![Badge tracking code size](https://img.shields.io/github/languages/code-size/Preffet/Python-SHA1-password-cracker?color=%2335009e)![Badge tracking last commit](https://img.shields.io/github/last-commit/Preffet/Python-SHA1-password-cracker?color=%2300379e)

-----------------------------------------------------------------------------

![banner](https://user-images.githubusercontent.com/84241003/161397143-e73a7976-972a-46d6-9274-1524a95abaee.png)

-----------------------------------------------------------------------------

### Description

Passwords should never be stored in plain text. They should be stored as hashes, just in case the password list is discovered. However, not all hashes are created equal.

crack_sha1_hash function takes in a SHA-1 hash of a password and returns the password if it is one of the top 10,000 passwords used, if it is not, it returns "PASSWORD NOT IN DATABASE".

The function hashes each password from `top-10000-passwords.txt` and compares it to the hash passed into the function. It also takes an optional second argument named `use_salts`. If set to true, each salt string from the file `known-salts.txt` is appended AND prepended to each password from `top-10000-passwords.txt` before hashing and before comparing it to the hash passed into the function.

-----------------------------------------------------------------------------

### Some password hashes to test the application

* `b305921a3723cd5d70a375cd21a61e60aabb84ec` should return "sammy123"
* `c7ab388a5ebefbf4d550652f1eb4d833e5316e3e` should return "abacab"
* `5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8` should return "password"

Here are some hashed passwords to test the function with when `use_salts` is set to `True`:

* `53d8b3dc9d39f0184144674e310185e41a87ffd5` should return "superman"
* `da5a4e8cf89539e66097acd2f8af128acae2f8ae` should return "q1w2e3r4t5"
* `ea3f62d498e3b98557f9f9cd0d905028b3b019e1` should return "bubbles1"

-----------------------------------------------------------------------------

### Testing

The unit tests for this project are in `test_module.py`. They are imported from `test_module.py` to `main.py` and will run automatically whenever you run the project.
