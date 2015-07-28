
# Alfred Password Generator #

Generate secure random passwords from Alfred.

Offers multiple generators, including based on real words and pronounceable pseudo-words generated with Markov chains.

Shows the strength of each generated password.


## Usage ##

- `pwgen [<length>]` — Generate passwords of length `<length>`. Default length is 30 characters.
- `pwconf` — View and edit workflow settings.

**Note:** Word-based generators may provide passwords that are slightly longer than `<length>`.


## Password strength ##

Each password has its strength in the result subtitle. This is in bits of entropy.

As a rule of thumb, your passwords should have the following strengths for the following applications:

|   Application   | Strength (bits of entropy) |
|-----------------|----------------------------|
| Online password |                         30 |
| Encrpytion keys |                        128 |

The default password length of 30 characters should provide very secure passwords, though you may need to increase this if you're making a new 1Password master key using one of the word-based generators.

Passwords of the same length (or even the self-same password) generated using different techniques have different strengths because the strength is determined by the permutations in the algorithm and the password length.

For example, the single-digit password `1` has an entropy of 3.32 bits when generated by the Numeric algorithm because it is one of only 10 possible one-digit passwords. The same password generated by the ASCII algorithm has an entropy of 5.95 bits because it is one of 62 possible one-character passwords.

See [Password strength on Wikipedia](https://en.wikipedia.org/wiki/Password_strength#Random_passwords) for more information.
