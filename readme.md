Art by [Artcobain](https://www.deviantart.com/artcobain)
#  __Introduction__
Run fully automated encounters with `!map` using AMIMO!

AMIMO fully automates monster movement and attacks in initiative. It is seamlessly integrated with [Map Utilities (`!map`)](https://avrae.io/dashboard/workshop/5f6a4623f4c89c324d6a5cd3) and [OTFBM](http://docs.otfbm.com/#/).
It is expected that AMIMO will be used alongside `!map`.


AMIMO will do its best to detect a monster's speed, attacks, and multiattacks. It works best with simple monsters, and is not intended for use with something like an Adult Red Dragon.

**AMIMO is still in alpha. Bugs will likely arise, and many limitations still exist. Report any bugs you find to @mehmango.**

**__Commands__**
`!amimo` - Automates the current and following monsters' movements and attacks.
`!ally [target1] [target2]...` - Toggles the allied status of a monster. *(Eg: `!ally GO1 go2 Ba1`)*
`!ghost [target1] [target2]...` - Toggles the ghost status of a combatant (Ghosts are untargetable). *(Eg: `!ghost Player1 "Player 2"`)*
`!amimo help` - Shows the help menu.


**__Usage__**
Follow the steps below to use AMIMO
- Make sure you have the `!map` alias added. Check it out [here](https://avrae.io/dashboard/workshop/5f6a4623f4c89c324d6a5cd3)
- Start init with `!init begin`
- Add a DM for `!map` with `!init add 0 DM -p 99`
- Set up the map. *(Eg: `!map -mapsize 20x20`)*
- Add monsters to the map with `!map -t <monster name>|<location> [-t <monster_name>|<location>]...`. *(Eg: `!map -t GO1|A1 -t GO2|B10`)*
- When it is the monster's turn, run `!amimo` to automate it and the following monsters' movements and attacks.


**__Limitations__**
There are currently some limitations to the alias. The main ones being:
- **No Spells.** AMIMO does not know how to use spells unless they are listed as a regular attack by Avrae attack automation. So it will probably work poorly on any monsters that use spells.
- **Non-attack Actions.** In a similar vein to spells, any abilities the monster has, like Dragon Breath, that are not listed as attacks by Avrae attack automation will not be properly recognised.
- **Monster Speed.** While AMIMO can get a monster's base walking and flying speed, it does not account for any other speeds. This will affect some monsters more than others.
- **Obstacles and Terrain.** While monsters will avoid standing in occupied spaces, AMIMO currently doesn't account for obstacles on the map (including other combatants) or different types of terrain when moving. It is unlikely this will be supported in the future for performance reasons.
- **Flight/Height.** AMIMO currently doesn't account for the third dimension, so any height differences between combatants is ignored.
- **Map Size.** Due to limitations that Avrae places on aliases, a map that is too large can cause AMIMO to fail. A safe size I have found is 30x30.
- **Multiattack Bugs.** AMIMO *does* support multiattack. However, it may not always work. Most simple monsters should work fine, but there may be rare cases where the multiattacking bugs out.


**__Show Your Support__**
Support AMIMO on [Ko-Fi](https://ko-fi.com/mehmango)
Support Map Utilities (`!map`) on [Ko-Fi](https://ko-fi.com/croebh)
Support OTFBM on [Patreon](https://www.patreon.com/otfbm)