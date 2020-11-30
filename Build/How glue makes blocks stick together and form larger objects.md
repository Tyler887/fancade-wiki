Blocks placed next to each other automatically group into a single larger object. This is great for static things, such as a level, which will get nice shading (ambient occlusion) and draw efficiently to keep your game running smoothly.

For moving things, you probably do *not* want them to glue to nearby blocks. E.g. if you use script to move a character, and it has glued to the level, the entire level will move too! So you want to remove the glue from the character block's sides. Select the block, tap the Pencil button ✏️ and then tap on a LEGO brick button. See those white dots? Just tap on them and they will disappear, making blocks around unable to stick to your custom block.

Removing glue dots requires editing the block. In case you have complex moving shapes, and do not want to make a lot of custom blocks with various glue sides, another method is to build the whole moving object off to the side, so its blocks don't directly touch e.g. the level blocks. Then use script to move it into place on Play, it'll happen before the first frame is drawn, so completely unnoticeable to the player.

<<Video("/uploads/20190726_001748.mp4")>>