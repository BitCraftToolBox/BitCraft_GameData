BitCraft game data
------------------

This repository houses a copy of the static data ("desc tables") for BitCraft online. These can be used for developing tools (calculators, planners, etc) that don't need a live connection to the database.

The data is currently available in two formats, available via branches in this repository:

* [Serialized C# SDK JSON](https://github.com/BitCraftToolBox/BitCraft_GameData/tree/cereal/cs): This is the result of decoding the native binary format (BSATN) with the C# SpacetimeDB SDK and generated bindings, and then serializing it to JSON. Generally recommended for use as it is more readable for both humans and code.
* [SATS-JSON](https://github.com/BitCraftToolBox/BitCraft_GameData/tree/sats-json): A much more verbose format that preserves the full structure (SumTypes, etc) of the data. Official documentation on the format is available on the [SpacetimeDB docs](https://spacetimedb.com/docs/sats-json).

The static data is also available for offline use in the native binary format: [BitCraft BSATN Data](https://github.com/BitCraftToolBox/BitCraft_BSATN_Data)

For applications that need a live connection to the database, bindings are available in all the languages SpacetimeDB supports via SDKs: [BitCraft Bindings](https://github.com/BitCraftToolBox/BitCraft_Bindings)

Alternatively, raw websocket connections can be used, though this is currently less well documented. An example can be seen [here](https://github.com/BitCraftToolBox/automata/blob/main/scripts/sats-json/gamedata-sats-json.py) (one of the scripts that generates this repository).
