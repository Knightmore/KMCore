# KMCore 
Being bored and fed up with all those plugins that depend on x other plugins, LUA scripts and plugins that have high maintenance because their devs hardcode everything, I began to work on a framework based on Dalamud. 

I don't know if/when I will release it to the public as this is/was just a private hobby project, so this is just a showcase for now. Tending to feature creep and forgetting some other WIP modules, the following list isn't complete.

*All/most included module names are (based on) ingame achievements or titles as I'm horrible with naming projects...*

## DisHonest Gillionaire *(Marketboard)*
- [x] Code
- [ ] GUI

Everything done for basic efficient marketboard needs... 

- Undercutting
- Relisting
- Ignoring own retainer
- And some other things

But the GUI is still a WIP mess, so nothing clean to show here. It's fully working, but with a typical backend dev UI..

## Date With Destiny *(Fates)*

| Content           | Status | ToDo  | 
|----------------|---------------|---------------|
| Fates | <li>[x] Code</li><li>[x] GUI</li> | Adding Relic Resistance farming
| Eureka   | <li>[ ] Code</li><li>[ ] GUI</li>  | Begin after finishing ***I Traded That/Nothing Ventured Nothing Gained***
| Bozja   | <li>[ ] Code</li><li>[ ] GUI</li>  |  Begin after finishing Eureka module

**Fates:**
All done and working. 

 - [x] Removed Escort fates, as they are just annoying and mostly useless.
 - [x] Gemstone trade-in  (see **I Traded That** ).
 - [x] Added using the local mender NPC (see **Mapping The Realm**) to repair equipment for characters which don't level all needed crafting classes.
 - [x] Added Statistic and advanced logging.
 - [x] Multiboxing party farming mode through local IPC (windows only)
 - [x] Added Atma Farming (will maybe make a standalone relic plugin too)
 - [ ] Maybe some advanced party mode outside of multiboxing through relay server communication (still undecided as I don't really like the possibility to create botting groups with other people)

<img src="https://raw.githubusercontent.com/Knightmore/KMCore/refs/heads/main/images/DWD%20Statistics.png" width="500" />

**Eureka:**
WIP (see table)

**Bozja:**
WIP (see table)

## Mapping The Realm *(Navigation Database)*
- [x] Code

Not really much to show here, as this is mostly just an API for the other included modules to handle any needed target location, shop inventory, etc. (straight from ingame data, so should work for every gameversion if Dalamud/Lumina is updated and there are not again heavily breaking changes like with Lumina 5 *blegh*). (*[VNavmesh](https://github.com/awgil/ffxiv_navmesh/tree/master) is needed for actual movement*). 

Basically it can be used to find and use any shop NPC, mender or a direct way to any given destination (across territories) either through positional data or just using the map flag.

Includes:
- Aetherytes and their connections.
- Connections between territories 
- Vendor locations and their shop list
- Mender locations
- Whatever the other modules need

## On Your Mark *(Daily Hunt Marks)*
- [X] Code
- [ ] GUI

Still undecided on its GUI. Maybe just an overview table of the current status (open/finished).
Just enable and wait for it to be done.

## I Traded That *(Collectable, Gem-/Tomestone, Hunt Mark Trade-In)*
- [x] Code
- [X] GUI

Includes: 
- Bicolor Gemstones (and Vouchers)
- Tomestones
- Company Seals (GC)
- Hunt Currency (Allied/Centrurio Seals, Sack of Nuts)

Going to add gil shop soon (and update the preview picture below) as all needed stuff is already finished in *Mapping The Realm* and I am just to lazy to properly test different gil vendors.

<img src="https://raw.githubusercontent.com/Knightmore/KMCore/refs/heads/main/images/ITradedThat.png" width="500" />

## Nothing Ventured Nothing Gained *(Retainer Ventures)*
- [X] Code
- [ ] GUI

Code is mostly done for the basics like sending out on selected ventures, tracking retainers and moving to prefered or nearest summoning bell to resend.
I will have to add another module to also automate submarines (there are still only lua scripts and no proper plugins around...)  and make all of this work for sublords. Time to fire up some FCs and join their ranks I guess!?

## Voyager *(Submersibles)*
- [X] Code
- [ ] GUI (Mostly only for preparatory options. 

Includes:
- Leveling and unlocking until OJ farm
- Automatic repair and component swap for SSSS -> SSUS -> SSUC (or WSUC if preferred)
- Stock up of Ceruleum Tanks if below set threshold.
- Statistics (gil/voyage, avg. duration, etc.)

## Out of Hiding *(Player/Retainer Database)*
- [X] Code
- [ ] GUI (Webservice?)

Tracking all players with their alt characters and retainers. Why? Because f***'em, that's why... also nice to keep track of market bot alts and their main account or toxic players and their other characters.

## Mammeteer *(Scheduler)*
- [ ] Code
- [ ] GUI

Code and GUI are partially done, but I'm not happy with it yet. You can set up tasks for the whole day in minimum 30 minute parts and just go AFK to let it do its thing, but until the other modules are done this will be a WIP.

## Experimental Stuff and Utilities
Includes things like 
- FC Chest sorting
- Auto Re-/Login
- A4N Undersync farm/mass exchange (together with *I Traded That* and mostly for stockpiling Ceruleum Tanks. See *Voyager*)
- Configuration of all modules per character or accountwide.
