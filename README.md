# QReaper
*Note: Discord has partially addressed the issue by adding a warning in the mobile app when you scan a QR code.*

Recently, Discord added the ability to scan a QR code with their mobile app to log in. 
It's convenient, but it has a massive flaw. Attackers have been gaining access to other people's accounts simply by
sending a login QR code but accompanying it with a message like "Scan this QR code to
redeem your Nitro gift!"

To combat these scams, someone created this Discord Bot which scans messages for QR codes and deletes any messages containing them. 

However, it, too, has a massive flaw: Not all QR codes are bad. This is fixed by checking the URL it goes to. For link shorteners, it will unshorten the URL before checking to ensure it is safe. If it's not, it will be deleted.

## How to Use
This bot has no settings and begins working as soon as it has been added to a server. It scans all attachments and embedded images.

If it fails to scan a message, you can make it re-scan the message by adding any reaction to the message.

To get this information, simply tag the bot in any channel that it can post messages to. 

## Self-hosting
These instructions assume you have created a bot account with Discord's developer portal. 
1. Download and install [Node.js](https://nodejs.org/en/)
2. Download this repository as a ZIP
3. Unzip the downloaded archive
4. In the root folder, create `env.json` and fill it with the following contents: 
```json
{
  "TOKEN": "your-bot-token-here"
}
```
5. Open a new terminal window at the root folder and run `npm install`
6. Run `node index.js` to start the bot. It will print to the console the port it's running on. Visit `localhost` to view the bot's webpage.
