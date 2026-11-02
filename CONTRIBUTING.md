# Contributing

Thanks for taking an interest in this little Middle-earth world for **Pilgrimage**! :3

This is essentially a fun side project and an experiment, not something I'm actively maintaining as a major project. That said, **pull requests are absolutely welcome**. If you want to improve or expand the world, feel free to fork the repo, make your changes, and open a PR against `master` for me to look at and potentially merge.

## What I'd love contributions for

In particular, I'd welcome things like:

- **Better ASCII art.** Some of the current creature art is pretty shitty, so improvements are very welcome.
- **More detail and lore** for creatures, plants, historical figures, and locations.
- **More regional fun facts**, descriptions, and other little pieces of worldbuilding.
- **Additional or improved regions, species, plants, and historical details** that make the world feel more alive.
- **Corrections and cleanup**, including mistakes in the existing data or things that don't quite make sense.

This is a starting point for a living, alternate-history simulation of Middle-earth, not an attempt to recreate Tolkien's world perfectly. Once Pilgrimage starts simulating it, things are going to go in their own directions anyway.

## Where to find the schemas

The `.block` schemas are **included with the game Pilgrimage**, not repackaged in this repository.

You'll need to **download Pilgrimage** to see them. Look in the game's `blocks/schemas` files for documentation on how the world, creatures, plants, regions, historical figures, and other blocks are structured.

You can get the game here: https://untrustedlife.itch.io/pilgrimage

A couple of particularly important things when editing the world:

- **Species and individuals are different things.** `GeneratedCreatures` contains reusable **species templates**, not one species for each named character. Named individuals belong in `HistoricalFigures` or `DeadHistoricalFigures`, with their individual names in `preferredName`.
- Species starting stats should be defined through `DefaultSkills` and `AttributeModifiers`. Don't populate a species template's `skillsAttributesBlock` with an individual's actual stats.
- Try to preserve existing IDs and historical event references, since changing them can break the world's history.
- If possible, test that the edited world still imports and works in Pilgrimage before submitting a PR. The format can change between game versions.

## A note about pull requests

**I probably won't be keeping a close eye on this repository.** This is just something I'm doing for fun alongside developing Pilgrimage itself, so please don't be surprised if a PR sits for a while before I notice or review it.

I appreciate contributions, but I can't promise quick reviews, regular updates, or that every PR will be merged.

## Use it as a modding reference!

I also hope this repository is useful as a **reference point for your own Pilgrimage modding projects**. Feel free to explore how the world is put together, learn from it, and use it as a starting point for making your own worlds. The game schemas are the better source of truth for the format, but a complete world save can be a useful real-world example.

Have fun making weird fantasy simulations! :3
