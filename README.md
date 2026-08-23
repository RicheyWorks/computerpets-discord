# Discord

**Discord Bot** — Companion bot linking Discord channels to pet status, away-alerts, and visit invites.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) ecosystem. Index: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. This repository ships the contract, README, and layout so implementation can start without renaming the organ later.

## Why it exists

If Rui walks away from neglect, Discord can tap you. If a friend invites a visit, it lands in a channel — not an email.

The flagship overlay already puts a living sticker on the real desktop (Rui first, 210 kinds). Discord does not replace that. It is one organ.

## Stack

TypeScript · discord.js · slash commands · Steamgate link · presence webhooks

GroupId / namespace: `com.enterprisepet.discord`  
Default listen: `3001`

## Talks to

- computerpets-visitation
- computerpets-steamgate
- computerpets-quests
- computerpets-bounty

## Contract

### Data

`Binding(discordId, steamId) · Alert(kind, channelId) · SlashAck(ephemeral)`

### Surface

- /link — bind Discord user to Steam / wallet
- /status — vitals for your active pet
- /recall — call a visiting pet home
- webhook pet.away — posted to a chosen channel

### Failure doctrine

Unlinked user → ephemeral how-to, no scan of the guild. Token leak rotation in Console. Rate limits → queue alerts 30s.

## Layout

```
computerpets-discord/
  README.md           this file
  LICENSE             MIT
  docs/CONTRACT.md    the same contract, frozen for implementers
  src/                implementation lands here
```

## Run (Windows)

PowerShell, from this folder, after the flagship helpers (Git, Node LTS 22+, JDK 21 as needed):

```powershell
cd bot; npm install; npm run start
```

You do not need this service to meet Rui. The [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md) is still the first pet.

## Ecosystem

| Organ | Repo |
| --- | --- |
| Flagship desktop + Spring | [RicheyWorks/computerpets](https://github.com/RicheyWorks/computerpets) |
| This organ | [RicheyWorks/computerpets-discord](https://github.com/RicheyWorks/computerpets-discord) |
| Full map | [RicheyWorks/computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem) |

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*
