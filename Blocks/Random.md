A number randomizer.

[[/uploads/Random.png]]

Inputs:

- Min: The minimum amount the block chooses from.
- Max: The maximum amount the block chooses from.

Outputs:

- Random: The randomly selected [[number]].

## Notes
- The Min input is included while the Max input is excluded, meaning: I put 0 into the Min input and put 5 into the Max input, the block will still select 0 or any number lower than 5 but not 5.
- The random block will not stop selecting numbers unless you wire a [[Play Sensor]] block.
- Note that the output would be in decimal, to avoid this use [[floor]], [[ceiling]], or [[round]] operators.

## Examples

[[uploads/random_ex01.jpg]]