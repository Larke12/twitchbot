# twitchbot
Go Twitch Bot Api wrapper, with an easy to use interface.

# Example
```go
package main

import (
	"github.com/witer33/twitchbot"
)

func main() {
	bot := twitchbot.NewBot("oauth:abcdef", "mybot", []string{"channel"})

	bot.OnMessage(func(bot *twitchbot.Bot, message *twitchbot.Message) {
		if message.Message == "!ping" {
			message.Reply("pong")
			message.Delete()
		}
	})

	bot.Run()
}
```

# TODO: Migrate from python bot
* Urban Dictionary definition requests, !urban and mod only, filter words
* Standard Dictionary, !define to pull a max number of defintions (store in DB?)
* Temperature, !temp to convert xF or xC values provided
* Twitter Shoutouts, !tso obtain the given Twitch users probable twitter URL

# TODO: New
* Twitch Channel Point reactions (DB?)
