# Discord contract

Do not implement against folklore. Implement against this file.

## Identity

- Product: **Discord**
- Repo: `computerpets-discord`
- Category: Integrations
- Idea: Discord Bot
- Port / surface: `3001`

## Must

- Stay canon with 210 species. No illegal hybrids. No swapped voices.
- Treat the desktop overlay as the main quest. This organ is optional until wired.
- Fail soft: the overlay keeps walking if this service is down, unless this *is* the overlay.
- No PII in public artifacts (Steam id, wallet, home path, webcam frames).

## Data

Binding(discordId, steamId) · Alert(kind, channelId) · SlashAck(ephemeral)

## Surface

- /link — bind Discord user to Steam / wallet
- /status — vitals for your active pet
- /recall — call a visiting pet home
- webhook pet.away — posted to a chosen channel

## Neighbors

- computerpets-visitation
- computerpets-steamgate
- computerpets-quests
- computerpets-bounty

## Failure doctrine

Unlinked user → ephemeral how-to, no scan of the guild. Token leak rotation in Console. Rate limits → queue alerts 30s.

## Stack

TypeScript · discord.js · slash commands · Steamgate link · presence webhooks
