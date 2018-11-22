# museum-infinity

This is an unconventional Minecraft modpack set in a mysterious, abandoned structure - the titular Infinite Museum.

## Naming conventions

To avoid namespace collisions, all structures and lists will be named in a hierarchical fashion, beginning with the author's name in ALL CAPS and seperated with underscores. Names will denote when structures or lists are sub-parts or variants of another one. Room names will be in PascalCase and sub-component names will be in camelCase. For instance, a door mechanism for Room 1, variety 1, made by Blueturtle1134 will be named `BLUETURTLE1134_Room1_variety1_door`

The `COMMON` namespace has components used for internal functioning of the modpack and contains the following:

+ `COMMON_Nodeshell` is a structure created for an "unfilled" room. This structure contains commands to detect if players are nearby, and if they are, to fill in this room and generate nodeshells to all open spaces around this room.
+ `COMMON_Node` is a structure that "fills" the room, by picking a random splitup and generating it.
+ `COMMON_Splits` is a list that enumerates all possible "splittings" of a full 42x42x14 room and contains all the items in `SPLITS`

The `SPLITS` namespace fills out a room with possible splittings

+ `SPLITS_Full` means a full 42x42x14 room
+ `SPLITS_HalfNS` splits into north and south halfs
+ `SPLITS_HalfEW` splits into east and west halfs
+ `SPLITS_Flat` splits into up and down halfs, both of which are 42x42x7
+ `SPLITS_QuadNS` splits into 42x21x7 blocks with long axis running NS
+ `SPLITS_QuadEQ` splits into 42x21x7 blocks with long axis running EW
+ `SPLITS_Tall` splits into 21x21x14
+ `SPLITS_Small` splits by eighths, into a 21x21x7 space

All these also have lists that are not in any namespace; i.e. if you've made a room that takes up a "flat" space you'd add it to the `Flat` list.