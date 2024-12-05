# kata-pokeapi_parser_refactoring

A kata to refactor an api parser

## Coding Challenge
You are given a list of Pokemon names.

Using the API provided at https://pokeapi.co/, list these attributes for each Pokemon:
Name
Base_experience
Species
Current level.

You can calculate their current level using their base_experience and their species' growth rate.
Example output
Given the 4 Pokemon Ivysaur, Bulbasaur, Pikachu, and Ditto, we should generate the following output:
```text
ivysaur 142 ivysaur 5
bulbasaur 64 bulbasaur 3
pikachu 112 pikachu 4
ditto 101 ditto 4
```

We already have the MVP running, you can find our code in `bin/run.php`, and you can run it with
```shell
time ./bin/run.php ivysaur bulbasaur pikachu ditto
```
or simply
```shell
time composer app
```
## TODO
1. Refactor the code so that 
   - it is easy and fast to add new features
   - we are reasonably confident that it keeps working as we evolve it
   - it is fast to go through the CI/CD pipeline
2. Add a feature:
   - when a Pokémon is of type `normal` it's printed in black
   - when a Pokémon is of type `poison` it's printed in red, and it also prints the species
   - when a Pokémon is of type `electric` it's printed in yellow, and it also prints the `move_damage_class.name` of the type
