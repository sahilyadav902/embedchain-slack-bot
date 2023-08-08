## Setup Slack Bot
- Fork the replit template for the Slack bot.
- Create a workspace on Slack if you don't have one already by clicking [here](https://slack.com/intl/en-in/).
- Create a new App on your Slack account by going [here](https://api.slack.com/apps).
- Select "From Scratch" and then enter the Bot Name and select your new or existing workspace.
- On the `Basic Information` page copy the `Signing Secret` and set it in your secrets as `SLACK_SIGNING_SECRET`.
- On the left Sidebar, go to `OAuth and Permissions` and add the following scopes under `Bot Token Scopes`: app_mentions:read, channels:history, channels:read, chat:write.
- Now select the option `Install to Workspace` and after it's done, copy the `Bot User OAuth Token` and set it in your secrets as `SLACK_BOT_TOKEN`.
- Set your `OPENAI_API_KEY` in your secrets.
- Start your replit container now by clicking on `Run`.
- On the Slack API website go to `Event Subscriptions` on the left Sidebar and turn on `Enable Events`.
- Copy the generated server URL in replit, append `/chat` at its end and paste it in `Request URL` box.
- After it gets Verified, click on `Subscribe to bot events`, add `message.channels` Bot User Event and click on `Save Changes`.
- Now go to your workspace, click on the bot name in the Sidebar and then add the bot to any channel you want.

## Usage
- Go to the channel where you have added your bot.
- To add data sources to the bot, use the command:
```text
add <data_type> <url_or_text>
```
- To ask queries from the bot, use the command:
```text
query <question>
```