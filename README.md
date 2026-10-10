# Telescope Bot

**A free Telegram bot that monitors public channels for your keywords and notifies you the instant a post matches.**

[![Telegram](https://img.shields.io/badge/Telegram-@telescope__one__bot-2CA5E0?style=flat&logo=telegram)](https://t.me/telescope_one_bot)
[![Website](https://img.shields.io/badge/Website-nomad4.tech%2Ftelescope-2196f3?style=flat)](https://nomad4.tech/telescope)
[![Java](https://img.shields.io/badge/Java-17+-ED8B00?style=flat&logo=openjdk)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=flat&logo=springboot)](https://spring.io/projects/spring-boot)
[![telegrambot4j](https://img.shields.io/badge/lib-telegrambot4j-blue?style=flat)](https://github.com/nomad4tech/telegrambot4j)
[![heartbeat4j](https://img.shields.io/badge/lib-heartbeat4j-blue?style=flat)](https://github.com/nomad4tech/heartbeat4j)
[![Status](https://img.shields.io/badge/status-live-brightgreen?style=flat)]()

[Try it now: @telescope_one_bot](https://t.me/telescope_one_bot) · [Website](https://nomad4.tech/telescope)

![Demo](assets/demo.gif)

------

## Quick facts

| | |
| --- | --- |
| Platform | Telegram (works in any Telegram client - iOS, Android, Web, Desktop) |
| Price | Free · Premium tier coming soon |
| Free tier limits | 2 channels, 50 keywords per user |
| Check interval | Every minute |
| Languages | English, Russian |
| Channel type | Public channels only (no private channels or DMs) |
| Data stored | Telegram user ID, your channel list, your keywords - no message content |

------

## What is this?

Telescope is a Telegram bot that watches public channels for you and sends a notification the moment a keyword appears in a new post.

Looking for a way to monitor Telegram channels for keywords, track mentions across Telegram, get alerts from public chats, or follow a topic without reading every post yourself? That's exactly what Telescope does.

Set it up once - never miss a relevant post again.

**Use cases:**

- Track mentions of your brand, product, or competitor
- Monitor job postings or apartment listings in niche channels
- Follow specific topics across news channels
- Get alerts on keywords in communities you don't want to read manually
- OSINT / open-source monitoring of public Telegram activity
- Keep an eye on channels without joining or reading them yourself

------

- ## Features

  - 🔔 **Real-time monitoring** - new posts checked every minute

  - 🔑 **Smart keyword matching**
    - Single word -> prefix match (`football` matches `footballer`)
    - Number -> exact match (`2026` won't match `20261`)
    - Phrase -> full phrase match (`rent apartment`)

  - 🚫 **Exclude keywords** - filter out noisy matches with keywords you want the bot to ignore

  - 📡 **Multiple input formats** - add channels by `@username`, `t.me/` link, or web Telegram URL

    ![Add channel](assets/add_chanel.gif)

  - 🔑 **Keyword management** - add, view, and remove keywords on the fly

    ![Add keywords](assets/add_keywords.gif)

  - 🌐 **Two languages** - English and Russian

    ![Language switch](assets/language_change.gif)

  - 💬 **In-app feedback** - report a bug or leave feedback right from the bot menu, no need to leave the chat

  - 🗑️ **Full data deletion** - `/deletedata` removes everything, no questions asked

------

## FAQ

**Is there a bot that notifies me when a keyword appears in a Telegram channel?**
Yes - Telescope does exactly this. Add a channel, add a keyword, get an instant notification when it matches.

**How do I track mentions of my brand or product on Telegram?**
Add the channels you care about and your brand name as a keyword - Telescope checks new posts every minute and notifies you the moment it matches.

**What's included in the free tier?**
Up to 2 channels and 50 keywords per user, checked every minute. A Premium tier is planned: higher limits, per-channel keyword filters, priority sweeps, and webhooks/API to send matches into your own apps (Slack, Notion, your own service).

**Can I monitor a Telegram channel without joining it?**
Yes - Telescope only needs the channel to be public; you don't have to join or be a member.

**Can I monitor private channels or groups?**
No - only public channels, the kind anyone can read without an invite. This is the same restriction every Telegram bot has.

**Can I exclude certain words from matching?**
Yes - add exclude keywords to filter out matches you don't want, without having to drop the main keyword entirely.

**How fast are alerts?**
The bot checks channels every minute, so you'll typically see a matching post in your DMs within 60-120 seconds of it going live.

**Are keywords case-sensitive?**
No. Matching ignores case and works across English, Russian, and other Unicode scripts.

**Do you store the posts?**
No - only enough to avoid sending you the same match twice. Post text is checked against your keywords and not kept.

**How do I delete my data?**
Send `/deletedata` in the bot - everything tied to your account is removed immediately.

**Does this work for apartment listings, job postings, or niche marketplace channels?**
Yes - any use case where you want an instant alert on a keyword in a public channel works: real estate, jobs, deals, brand mentions, news topics, and more.

------

## Plans

|                             | Free         | Premium *(coming soon)* |
| --------------------------- | ------------ | ------------------------ |
| Channels                    | 3            | More                    |
| Keywords                    | 50           | More                    |
| Check interval              | Every minute | Priority                |
| Per-channel keyword filters | —            | ✓                        |
| Webhooks / API              | —            | ✓                        |

------

## Commands

| Command       | Description              |
| ------------- | ------------------------ |
| `/start`      | Main menu                |
| `/help`       | Guide and keyword syntax |
| `/language`   | Switch language (ru/en)  |
| `/deletedata` | Delete all your data     |

------

## What's new

Changes are tracked in [CHANGELOG.md](CHANGELOG.md). A shorter, user-facing version of the same updates is also shown on the [website](https://nomad4.tech/telescope).

------

## Tech

Built with:

- **Java 17** + **Spring Boot**
- **PostgreSQL** - user data and channel state
- **[telegrambot4j](https://github.com/nomad4tech/telegrambot4j)** - my own open-source Java library for Telegram bots
- **[heartbeat4j](https://github.com/nomad4tech/heartbeat4j)** - my own open-source health-check library, used to catch background monitoring loops that silently stop ticking
- Custom Telegram API layer for channel monitoring

> The code is closed-source, but `telegrambot4j` and `heartbeat4j` - the libraries powering this - are open and available on GitHub

------

## Privacy

The bot stores only: your Telegram user ID, your entered list of channels, and your keywords. No message content is stored. Use `/deletedata` to remove everything at any time.

[Full privacy policy](https://telegra.ph/Politika-konfidencialnosti---Telescope-Bot-05-03)

------

## Support

Found a bug or have a feature request? Use the **💬 Contact support** button right in the bot, or reach out directly: [@nomad4tech](https://t.me/nomad4tech)

------

<div align="center">

Made by [@nomad4tech](https://github.com/nomad4tech) · Powered by [telegrambot4j](https://github.com/nomad4tech/telegrambot4j) and [heartbeat4j](https://github.com/nomad4tech/heartbeat4j)