# Phasmo Sanity and Hunt

A small companion window for **Phasmophobia** that keeps two things in view at all times: **how sane your team is** and **what the ghost is doing**. You no longer have to walk back to the truck, read the sanity monitor, squint at the activity graph, or guess whether that was a hunt.

Version 15.3 · Windows 10/11 (64-bit) · read-only

---

## What it shows

### Team sanity
- **Team average.** The same number the truck's sanity monitor shows, updated every second. It turns amber and then red as sanity drops, and pulses red below 25%.
- **One card per player, up to 4, with you first.** Each card shows:
  - the player's name;
  - their sanity;
  - the room they are in right now.
- **Low-sanity warning.** A player's card pulses red below 25%, so you know who is at risk before a hunt.
- **Dead players.** When a teammate dies, their card shows a faint ghost, **DEAD**, and the sanity they died at. They stop counting towards the team average.
- **Leavers.** A player who drops out keeps their card for 15 seconds, then the slot frees up.

### Huntatron (ghost activity)
- **Activity graph.** A live copy of the truck's **Total Activity** graph for the last 60 seconds, with the newest reading on the left like the truck. Each spike is the ghost doing something: touching, throwing, an EMF reading, a ghost event.
- **HUNT lamp.** It lights the moment a hunt starts, even if you are nowhere near the ghost.
- **Cooldown.** After a hunt ends, it counts down the time before the ghost can hunt again.

## How it helps you play
- **Know when it's safe.** Watch the team average and the activity graph without leaving the investigation.
- **Hide in time.** The HUNT lamp tells everyone at once, including the person in the truck.
- **Look after your team.** See who is low on sanity and who has died, and where everyone is in the house.
- **Plan objectives.** For "get the average sanity below 25%", watch it fall live.
- **Read the ghost's mood.** A busy graph means an active ghost; a flat one means time to provoke it.

## Getting it running
1. Install the **.NET 8 SDK** once, on the PC you build on. It's only needed to build.
2. Unzip, then double-click **BUILD-AND-RUN.cmd**.
3. When it finishes, **PhasmoSanityHunt.exe** appears next to the .cmd file. The "Ready:" line shows a size of a few tens of MB.
4. That one file is the whole program:
   - copy it anywhere, such as your desktop or a USB stick, or give it to a friend;
   - it runs on its own and doesn't need .NET installed.

Start it before or after the game. The first time it opens it may take up to a minute to find the game's data. After that it follows you from contract to contract by itself.

## Good to know
- **Read-only.** It only *reads* the game's memory:
  - it never writes to the game, injects anything or changes how the game plays;
  - closing it has no effect on the game.
- **Contracts and lobby.** It resets by itself for each contract, and shows "In the lobby" between contracts.
- **Log file.** A small log is kept in a **logs** folder next to the exe. It records when the game was found, contract start/end, hunts with their length, and errors.
- **Crashes.** If something goes wrong it shows a message, and the details are saved to **crash.txt** next to the exe.
- **Game updates.** If an update moves things around, the cards or graph may stay empty until the program is updated.
- **Fair play.** Use it where your group is happy with it. Reading another program's memory may go against a game's rules, and that is your call to make.

## Frequently asked
**The window says "Waiting for Phasmophobia".**
Start the game. The program finds it on its own.

**It says "Finding the game's player and EMF data".**
Normal on first start. Give it up to a minute.

**The graph is flat.**
The ghost isn't doing anything yet. Spikes appear as soon as it interacts with something.

**Someone's room says "Room unknown".**
They are between rooms or loading in. It fills in within a second or two.
