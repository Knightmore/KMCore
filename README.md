



# KMCore (Proof of Concept)
Being bored and fed up with all those plugins that depend on x other plugins, LUA scripts and plugins that have high maintenance because their devs hardcode everything, I began to work on a framework based on Dalamud. 

I don't know if/when I will release it to the public as this is/was just a private hobby project, so this is just a showcase for now. Tending to feature creep and forgetting some other WIP modules, the following list isn't complete.

*All included module names are (based on) ingame achievements or titles as I'm horrible with naming projects...*

## DisHonest Gillionaire *(Marketboard)*
- [x] Code
- [ ] GUI

Everything done for basic efficient marketboard needs... 

- Undercutting
- Relisting
- Ignoring own retainer
- And some other things

But the GUI is still a WIP mess and venture handling has to be outsourced to its own module , so nothing clean to show here. It's fully working, but with a typical backend dev UI..

## Date With Destiny *(Fates)*

| Content           | Status | ToDo  | 
|----------------|---------------|---------------|
| Fates | <li>[x] Code</li><li>[x] GUI</li> | <li>More refactor (moving commonly used fuctions outside of plugin)</li><li>Adding Relic Atma and Relic Resistance farming </li>
| Eureka   | <li>[ ] Code</li><li>[ ] GUI</li>  | Begin after finishing ***I Traded That/Nothing Ventured Nothing Gained***
| Bozja   | <li>[ ] Code</li><li>[ ] GUI</li>  |  Begin after finishing Eureka module

**Fates:**
All done and working. 

 - [x] Removed Escort fates, as they are just annoying and mostly useless.
 - [x] Gemstone trade-in  (see **I Traded That** ).
 - [x] Added using the local mender NPC (see **Mapping The Realm**) to repair equipment for characters which don't level all needed crafting classes.
 - [x] Added Statistic and advanced logging.
 - [x] Multiboxing party farming mode through local IPC (windows only)
 - [ ] Maybe some advanced party mode outside of multiboxing through relay server communication 

<img src="https://raw.githubusercontent.com/Knightmore/KMCore/refs/heads/main/images/DWD%20Statistics.png" width="500" />



**Eureka:**
WIP (see table)

**Bozja:**
WIP (see table)

## Mapping The Realm *(Navigation Database)*
- [x] Code

Not really much to show here, as this is mostly just an API for the other included modules to handle any needed target location, shop inventory, etc. (straight from ingame data/not hardcoded so should work for every gameversion if Dalamud/Lumina is updated). (*[VNavmesh](https://github.com/awgil/ffxiv_navmesh/tree/master) is needed for actual movement*). 

Basically it can be used to find and use any shop NPC, mender or a direct way to any given destination (across territories) either through positional data or just using the map flag.

Includes:
- Aetherytes and their connections.
- Connections between territories 
- Vendor locations and their shop list
- Mender locations
- Whatever the other modules need

## On Your Mark *(Daily Hunt Marks)*
- [ ] Code
- [ ] GUI

Code is mostly done, still undecided on how to set up the GUI, as there is not really much needed. Just enable and wait for it to be done.

## I Traded That *(Collectable, Gem-/Tomestone, Hunt Mark Trade-In)*
- [x] Code
- [ ] GUI

Code is done for Gem-, Tomestones and GCs. Hunt Marks will be done when **On Your Mark** is complete. Collectables will be done last. It's the easiest one, but cba right now to deal with gathering/crafting to test it. 
GUI will be complete with it too. Still undecided if there should be added more like Gil/Tribal/whatever shops.

<img src="https://raw.githubusercontent.com/Knightmore/KMCore/refs/heads/main/images/ITradedThat.png" width="500" />

## Out of Sight *(Sightseeing Log)*
- [ ] Code
- [ ] GUI

WIP and not really a priority now. Lots of them are a pain in the ass, especially when it's depending on a good player connection and framerate like jump puzzles. Doable and things like Kugane Tower/lamppost are working already... but oof... 

## Nothing Ventured Nothing Gained *(Retainer Ventures)*
- [ ] Code
- [ ] GUI

Not really much done yet. Only quick ventures and resend included in **DisHonest Gillionaire** that has to moved into its own module. 

# Mammeteer *(Scheduler)*
- [ ] Code
- [ ] GUI

Code and GUI are partially done, but I'm not happy with it yet. You can set up tasks for the whole day in minimum 30 minute parts and just go AFK to let it do its thing, but until the other modules are done this will be a WIP.

# Experimental Stuff and Utilities
Includes things like FC Chest sorting, Auto Re-/Login, Configuration of all modules per character or accountwide.
