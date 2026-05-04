# Telescope Bot

**Monitor public Telegram channels for keywords. Get notified instantly.**

[![Telegram](https://img.shields.io/badge/Telegram-@telescope__one__bot-2CA5E0?style=flat&logo=telegram)](https://t.me/telescope_one_bot)
[![Java](https://img.shields.io/badge/Java-17+-ED8B00?style=flat&logo=openjdk)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=flat&logo=springboot)](https://spring.io/projects/spring-boot)
[![telegrambot4j](https://img.shields.io/badge/lib-telegrambot4j-blue?style=flat)](https://github.com/nomad4tech/telegrambot4j)
[![Status](https://img.shields.io/badge/status-live-brightgreen?style=flat)]()

[Try it now: @telescope_one_bot](https://t.me/telescope_one_bot)

------

## What is this?

Telescope is a Telegram bot that watches public channels for you and sends a notification the moment a keyword appears in a new post.

Set it up once - never miss a relevant post again

**Use cases:**

- Track mentions of your brand, product, or competitor
- Monitor job postings or apartment listings in niche channels
- Follow specific topics across news channels
- Get alerts on keywords in communities you don't want to read manually

------

## Features

- 🔔 **Real-time monitoring** - new posts checked every minute
- 🔑 **Smart keyword matching**
  - Single word -> prefix match (`football` matches `footballer`)
  - Number  -> exact match (`2026` won't match `20261`)
  - Phrase -> full phrase match (`rent apartment`)
- 📡 **Multiple input formats** - add channels by `@username`, `t.me/` link, or web Telegram URL
- 🌐 **Two languages** - English and Russian (`/language`)
- 🗑️ **Full data deletion** - `/deletedata` removes everything, no questions asked

------

## Plans

|                             | Free         | Premium *(coming soon)* |
| --------------------------- | ------------ | ----------------------- |
| Channels                    | 2            | More                    |
| Keywords                    | 10           | More                    |
| Check interval              | Every minute | Priority                |
| Per-channel keyword filters | —            | ✓                       |
| Advanced search filters     | —            | ✓                       |
| Webhooks                    | —            | ✓                       |

------

## Commands

| Command       | Description              |
| ------------- | ------------------------ |
| `/start`      | Main menu                |
| `/help`       | Guide and keyword syntax |
| `/language`   | Switch language (ru/en)  |
| `/deletedata` | Delete all your data     |

------

## Tech

Built with:

- **Java 17** + **Spring Boot**
- **PostgreSQL** - user data and channel state
- **[telegrambot4j](https://github.com/nomad4tech/telegrambot4j)** - my own open-source Java library for Telegram bots
- Custom Telegram API layer for channel monitoring

> The code is closed-source, but `telegrambot4j` - the bot framework powering this - is open and available on GitHub

------

## Privacy

The bot stores only: your Telegram user ID, your entered list of channels, and your keywords. No message content is stored. Use `/deletedata` to remove everything at any time.

[Full privacy policy](https://telegra.ph/Politika-konfidencialnosti---Telescope-Bot-05-03)

------

## Support

Found a bug or have a feature request? Contact: [@nomad4tech](https://t.me/nomad4tech)

------

<div align="center">

Made by [@nomad4tech](https://github.com/nomad4tech) · Powered by [telegrambot4j](https://github.com/nomad4tech/telegrambot4j)
