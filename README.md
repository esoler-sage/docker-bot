# docker-bot

Template for developing bot with Docker and Bot Framework Emulator

# How to use

With Docker installed, run `docker-compose up`. Then navigate to [http://localhost:3000/](http://localhost:3000/).

## Development

Modify your bot code at [packages/bot](https://github.com/compulim/docker-bot/tree/master/packages/bot).

## Ports

| Port | Exposed | Image | Description | Incoming connection from |
| - | - | - | - | - |
| 3000 | Yes | `web-server` | Static page for Web Chat | Browser |
| 3978 | No | `bot-server` | Bot.js hosted on Restify | `bot-emulator` |
| 5000 | Yes | `bot-emulator` | Emulated Direct Line server | Browser and `bot-server` |

# Roadmap

* Bot.js
   * Create some responses that fire Redux actions
* Web server
   * Use Web Chat from NPM, instead of CDN
   * Add Redux
   * For activity with `{ event: 'redux' }`, pump it into Redux directly

# Contributions

Like us? [Star](https://github.com/compulim/docker-bot/stargazers) us.

Want to make it better? [File](https://github.com/compulim/docker-bot/issues) us an issue.

Don't like something you see? [Submit](https://github.com/compulim/docker-bot/pulls) a pull request.
