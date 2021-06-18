Fancade has a hard script limit. After a certain number of scripts in the editor, adding anything else will cause a "Too many scripts" error, and the game will refuse to run, as long as the extra scripts are not removed. Games that do not optimise scripts, that affect multiple objects, into loops are most likely to run into this issue.
![Too many scripts!](https://cdn.discordapp.com/attachments/852037487987392529/852037576935211018/Too_many_scripts.png)

# History
Script limit has been a mystery for a long time. An elusive upper limit that creators randomly hit, and are forced to scrap their ambitious project. Fancade 1.2 significantly improved the scenario by introducing Advanced Inspect blocks. Those blocks, when enabled, showed how much of the script limit has the game consumed already.
![Advanced Inspect](https://cdn.discordapp.com/attachments/852037487987392529/852039104958824478/Screenshot_20210609-094759_Fancade.png)

# Technical Details
The introduction of advanced inspect allowed for more robust testing, which helped in discovering some key insights regarding the elusive script limit. Among those, Andrew Clark's discoveries were crucial for our current understanding of it.

## Current Understanding
The limit is 4096. The value doesn't matter as much as how you decide to use them. There are three things that consume the script limit.

* [Script Blocks](https://www.fancade.com/wiki/Script/Script%20Limit.md#script-blocks)
* [Wire Splits](https://www.fancade.com/wiki/Script/Script%20Limit.md#wire-splits)
* [Pointer Dereferencing](https://www.fancade.com/wiki/Script/Script%20Limit.md#pointer-dereferencing)

### Script Blocks
Every script block counts as 1 script towards the total limit. It does not matter which script block it is, as long as it is an inbuilt script block, it adds 1 to the counter. The attached image has 4 script blocks, thus the script consumption is 4/4096 or 0.1%.
![4 Script Blocks](https://cdn.discordapp.com/attachments/852037487987392529/855423620397662238/Screenshot_20210618-113130_Fancade.png)

### Wire Splits
A wire split counts as 1 script towards the limit. Thus the script in image A adds 4 scripts (3 script blocks + 1 wire split) to the counter.
![A - Wire Splitting](https://cdn.discordapp.com/attachments/852037487987392529/855423620692443156/Screenshot_20210618-113313_Fancade.png)

But wire splits are defined as "n to 1" and "1 to n". This basically means, no matter how large the split is, it will add only 1 to the counter. The script in image B adds 10 scripts (9 script blocks + 1 wire split) to the counter.
![B - Wire Splitting](https://cdn.discordapp.com/attachments/852037487987392529/855423621173739530/Screenshot_20210618-113424_Fancade.png)

The same applies in case of joining. The script in image C counts as 4, whereas the script in image D counts as 10.
![C - Wire Splitting](https://cdn.discordapp.com/attachments/852037487987392529/855423621433393172/Screenshot_20210618-113611_Fancade.png)
![D - Wire Splitting](https://cdn.discordapp.com/attachments/852037487987392529/855423621639569408/Screenshot_20210618-113747_Fancade.png)

### Pointer Dereferencing
This section will be easier to understand if you are somewhat familiar with the concept of pointers. If you are not, you can think of them as an address to somewhere a value is stored.
When a pointer is dereferenced, i.e. converted to value, it counts as one script. In image E, the Get Variable block outputs a pointer, which is then derefernced to a value for the Negate block. Thus the script adds 3 (2 script blocks + 1 pointer dereferencing) to the counter.
![E - Pointer Dereferencing](https://cdn.discordapp.com/attachments/852037487987392529/855423621933301760/Screenshot_20210618-113952_Fancade.png)

This behaviour, when combined with wire splitting, results in a peculiar quirk where adding another script block can actually consume less script limit than without that block. In the following picture, case 1 adds 8 (4 script blocks + 1 wire splitting + 3 pointer dereferencing) scripts to the counter. Almost half of them are just from dereferencing. To avoid that, in case 2 another script block is added to dereference the pointer before the split. Thus case 2 only adds 7 (5 script blocks + 1 wire split + 1 pointer dereference) scripts to the counter.
![Pointer Dereferencing](https://cdn.discordapp.com/attachments/852037487987392529/855440742431064094/Screenshot_20210618-130458_Fancade.png)

Known script blocks that output a pointer are all the Get Variable and List Element blocks.
![Pointer out](https://cdn.discordapp.com/attachments/852037487987392529/855444701309829170/Screenshot_20210618-192013_Fancade.png)

Known script blocks that accept a pointer as input are the Variable inputs of the List Element blocks and the Variable input of the Menu Item block.
![Pointer in](https://cdn.discordapp.com/attachments/852037487987392529/855444701561094211/Screenshot_20210618-192112_Fancade.png)

## Tips
Here are some general tips to conserve the limit as much as possible.

* Use wire splits whenever possible.
* Do not use variables unless absolutely needed.
* If a pointer is dereferenced at least three times, dereference it before the split.
* Comments do not count towards any limits. Use them as much as possible.
