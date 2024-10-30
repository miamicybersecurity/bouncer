# bouncer

Bouncer is a Discord authentication bot tailored specifically for university
clubs. Initially developed for the Miami University Cyber Security Club
(MUCSC), Bouncer facilitates autonomous verification through email,
streamlining the membership verification process.

To begin using Bouncer, please refer to the quick start guide provided below.
To generate the authentication prompt, utilize the command
`/verification create <#channel>`.

## Quick Start Guide

This repository includes pre-built Docker images available via GitHub releases,
designed to simplify deployment on containerized servers. To get started, you
will need two essential components:

1. **Discord Bot and Token:**  
   Set up a Discord bot and retrieve its token. While there are many tutorials available, a commonly recommended resource is the [discord.py tutorial](https://discordpy.readthedocs.io/en/stable/discord.html).

2. **Google Application for Gmail API:**  
   Create a Google application to access the Gmail API. You can follow the official [Google tutorial](https://developers.google.com/gmail/api/quickstart/python#enable_the_api) for guidance.

Once both the Discord bot and Google application have been created, compile all
application secrets into a configuration file. The refresh token for the Gmail
API can be generated by running bouncer locally with the `-v` option, which
will display the token after completing the OAuth flow.

Below is an example configuration file:

```env
DISCORD_TOKEN=<Your Discord bot token>
GOOGLE_CLIENT_ID=<Your Google application client ID>
GOOGLE_CLIENT_SECRET=<Your Google application client secret>
GOOGLE_REFRESH_TOKEN=<Your Google refresh token>
```

This file should be securely stored and will be required for proper application
deployment.
