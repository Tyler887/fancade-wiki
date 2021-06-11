Fancade has a hard script limit. After a certain number of scripts in the editor, adding anything else will cause a "Too many scripts" error, and the game will refuse to run, as long as the extra scripts are not removed. Games that do not optimise scripts, that affect multiple objects, into loops are most likely to run into this issue.
![Too many scripts!](https://cdn.discordapp.com/attachments/852037487987392529/852037576935211018/Too_many_scripts.png)

# History
Script limit has been a mystery for a long time. An elusive upper limit that creators randomly hit, and are forced to scrap their ambitious project. Fancade 1.2 significantly improved the scenario by introducing Advanced Inspect blocks. Those blocks, when enabled, showed how much of the script limit has the game consumed already.
![Advanced Inspect](https://cdn.discordapp.com/attachments/852037487987392529/852039104958824478/Screenshot_20210609-094759_Fancade.png)

# Technical Details
The introduction of advanced inspect allowed for more robust testing, which helped in discovering some key insights regarding the elusive script limit. Among those, Andrew Clark's discoveries were crucial for our current understanding of it.

## Current Understanding
The limit is 4096. The value doesn't matter as much as how you decide to use them. There are three things that consume the script limit.

* Script Blocks
* [Wire Splits](https://www.fancade.com/wiki/Script/Wire%20Splits.md)
* Pointer Dereferencing
