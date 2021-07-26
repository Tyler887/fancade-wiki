Executes the scripts connected to it only on the first tick. Useful for initialization.

Output:
- On Play: Triggers if the current tick is the first tick.

[[/uploads/Playsensor.png]]

## Notes

- The Play Sensor is often described as "only executing once", but it actually can execute multiple times, if its "before" wire is connected to another block and it is triggered multiple times during the first tick.
- Likewise, if its "before" wire is connected to another block and it _doesn't_ get triggered during the first tick, the Play Sensor will _never_ trigger its "On Play" output.
