


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
| Fates | <li>[x] Code</li><li>[x] GUI</li> | <li>Maybe refactor (less memory allocation)</li><li>Maybe adding some logic for Relic Atma farming </li>
| Eureka   | <li>[ ] Code</li><li>[ ] GUI</li>  | Begin after finishing ***I Traded That/Nothing Ventured Nothing Gained***
| Bozja   | <li>[ ] Code</li><li>[ ] GUI</li>  |  Begin after finishing Eureka module

**Fates:**
All done and working with every type. A bit wonky with Escort fates, but maybe I'll just remove and skip them completely as the time/gemstone ratio is horrible and who does them anyway, right? 
Settings GUI could need a little revamp but well...

Gemstone trade-in is handled in **I Traded That** and will be triggered once the set threshold is reached.

**Eureka:**
WIP (see table)

**Bozja:**
WIP (see table)

## Mapping The Realm *(Navigation Database)*
- [x] Code

Not really much to show here, as this is mostly just an API for the other included modules to handle any needed target location, shop inventory, etc. (straight from ingame data/not hardcoded so should work for every gameversion if Dalamud/Lumina is updated). (*[VNavmesh](https://github.com/awgil/ffxiv_navmesh/tree/master) is needed for actual movement*). 

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

Code is done for Gem- and Tomestones. Hunt Marks will be done when **On Your Mark** is complete. Collectables will be done last. It's the easiest one, but cba right now to deal with gathering/crafting to test it. 
GUI will be complete with it too. Still undecided if there should be added more like Gil/Tribal/whatever shops.

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
