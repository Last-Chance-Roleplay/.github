# Last Chance Roleplay

Last Chance Roleplay is a serious roleplay community on FiveM. We focus on character-driven stories, fair play, and a server where every choice has weight. You only get one shot at it, so make it count.

## Connecting

1. Install [FiveM](https://fivem.net) and sign in with your Cfx.re account.
2. Join our [Discord](https://discord.gg/lcrp5m) and read the rules before you hop in.
3. Open FiveM, press `F8`, and run:

```
connect play.lcrp5m.net
```

You can also search for **Last Chance Roleplay** in the FiveM server browser.

| | |
|---|---|
| Server address | `play.lcrp5m.net` |
| Discord | [discord.gg/lcrp5m](https://discord.gg/lcrp5m) |
| Website | [lcrp5m.net](https://lcrp5m.net) |

## Requirements

- A legal copy of GTA V on PC
- FiveM client, up to date
- A working microphone (push-to-talk is required in city)
- A linked Discord account
- Be 18 or older

## Getting Started

New to the city? Here's the short version:

1. **Join the Discord** and verify your account.
2. **Read the rules** in the Discord. Not knowing them isn't an excuse.
3. **Submit an application** if you want to join a whitelisted department.
4. **Create your character.** Give them a name, a backstory, and a reason to be in the city.
5. **Play it out.** Stay in character, give others good RP, and let the story happen.

## Departments and Jobs

### Whitelisted

| Department | How to join |
|---|---|
| Police | Application in Discord |
| EMS / Fire | Application in Discord |
| Department of Justice | Application in Discord |
| Gangs and organizations | Contact staff with a group proposal |

### Civilian

Mechanic, tow, taxi, trucking, fishing, mining, real estate, and more. Civilian jobs are open to everyone. Some businesses can be owned and run by players.

## Staff

| | Name | Role | Discord |
|---|---|---|---|
| <img src="img/Henz.png" width="64" height="64"> | T. Bradford (A-1) | Owner | `bhens84` |
| <img src="img/Barfield.png" width="64" height="64"> | K. Barfield (A-2) | Owner | `kennyb_14` |
| <img src="img/Ron.png" width="64" height="64"> | R. Wick (A-3) | Owner & Development Director | `sa1tie8` |
| <img src="img/turner.png" width="64" height="64"> | K. Turner | Staff Team & Developer | `onyximpulsion` |
| <img src="img/baumann.png" width="64" height="64"> | L. Baumann | Staff Team & Developer | `lb2234` |
| <img src="img/larry.png" width="64" height="64"> | A. Larry | Staff Team | `larry.j` |
| <img src="img/brayden.png" width="64" height="64"> | B. Herrell | Developer | `i_ambrayden` |

Need help? Open a ticket in Discord. Don't DM staff directly for support.

## Ban Appeals

Appeals are submitted through the `#ban-appeals` channel or the form on [our website](https://lcrp5m.net). Be honest about what happened. Appeals that dodge responsibility get denied.

## For Developers

This section is for anyone working on the server itself.

### Stack

- **Server:** FXServer managed through txAdmin
- **Framework:** [Qbox](https://qbox.re)
- **Database:** MariaDB / MySQL with oxmysql
- **Library:** ox_lib
- **Voice:** pma-voice

### Local Setup

1. Download the latest recommended [FXServer artifacts](https://runtime.fivem.net/artifacts/fivem/).
2. Clone this repository into your server data folder.
3. Copy `server.cfg.example` to `server.cfg` and fill in your license key and database connection string.
4. Import the database schema:

```bash
mysql -u <user> -p <database> < sql/schema.sql
```

5. Start the server:

```bash
./run.sh +exec server.cfg
```

On Windows, run `FXServer.exe +exec server.cfg` instead.

### Structure

```
resources/
├── [core]        Framework and essential dependencies
├── [standalone]  Self-contained scripts
├── [jobs]        Job and department resources
├── [maps]        MLOs and map edits
├── [vehicles]    Vehicle add-ons
└── [ui]          HUD, phone, and menus
server.cfg        Server configuration (not committed)
sql/              Database schema and migrations
```

### Contributing

- Branch off `main` and open a pull request when you're ready for review.
- Test changes on the dev server before they go to live.
- Keep secrets out of the repo. License keys, webhooks, and database credentials go in `server.cfg` only.
- Respect resource licenses. Don't commit paid or escrowed resources.

## Links

- Discord: [discord.gg/lcrp5m](https://discord.gg/lcrp5m)
- Website: [lcrp5m.net](https://lcrp5m.net)

---

Last Chance Roleplay is not affiliated with or endorsed by Rockstar Games, Take-Two Interactive, or Cfx.re.
