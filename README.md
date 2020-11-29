# discord-redirect
Cloudflare worker to open Discord links on Discord client.

## Why?
Because if you go to https://discord.com/users/461171501715161108 it will go to the website but if you go to https://discordredirect.discordsafe.com/users/461171501715161108 it will open on the client. That's it.

## Usage
`https://discordredirect.discordsafe.com/ENDPOINT`

## Examples
* Users (UserID): https://discordredirect.discordsafe.com/users/287574458963722240.
* Channels (GuildID, ChannelID): https://discordredirect.discordsafe.com/channels/374953833828319232/504679420263661588.
* DM (UserID): https://discordredirect.discordsafe.com/channels/@me/287574458963722240.
* Messages (GuildID, ChannelID, MessageID): https://discordredirect.discordsafe.com/channels/374953833828319232/504679535598501898/782614104539922493.
* Nitro Tab: https://discordredirect.discordsafe.com/store.
* Friends Tab: https://discordredirect.discordsafe.com/channels/@me.
* Library Tab: https://discordredirect.discordsafe.com/library.

## Common errors
### Not working
1. Open the same link on another tab.
2. Check site settings, allow pop-ups and redirects.
3. Try with another browser.

### The browser does not recognize the protocol or still not working
This is because the protocol is open on the last client you installed.

If you downloaded Discord Canary first, then Discord (normal) and the one you use is Discord Canary, your browser will try to open it in Discord (normal) and you won't be able to.

**Easy fix:**
1. Uninstall the client you use.
2. Install it again.

**Pro hacker fix: (on Windows)**
1. Press `Windows + X`.
2. Open `execute`.
3. Write `regedit` and open.
4. Allow admin perms.
5. Open `HKEY_CLASSES_ROOT`.
6. Search `Discord` and expand it.
7. Open `shell`.
8. Open `open`.
9.  Click and open `command`
10. Modify the `(default)` value. It will look like this `"C:\Users\USER_HERE\AppData\Local\DiscordX\app-0.0.290\DiscordX.exe" --url -- "%1"`.
11. Search your current Discord Client on `C:\Users\USER_HERE\AppData\Local`.
12. Open the folder. Example: `C:\Users\USER_HERE\AppData\Local\Discord`.
13. Open the folder with the highest value. Example: `C:\Users\USER_HERE\AppData\Local\Discord\app-0.0.308`.
14. Copy the `app...`.
15. Modify the `(default)` value replacing the path. Remind to replace Discord**X** with your client name. (leave it as only discord if it is normal). Also replace app-X with the path you saw before. `"C:\Users\USER_HERE\AppData\Local\Discord\app-X\DiscordX.exe" --url -- "%1"`
16. Save it.
17. Done!