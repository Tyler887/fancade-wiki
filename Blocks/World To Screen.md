Given a world coordinate, outputs its screen coordinates.

[[/uploads/World_To_Screen.png]]

# Notes
This script has a bug due to a OFD (One Frame Delay). To fix this, grab an If, connect a red Get Variable to the red input on the If, grab a Set Truth, and connect True to 'Value'.

See the yellow input on the top of the Set Truth? Connect it to False and the bug is fixed!