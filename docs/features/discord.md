# Discord

A Discord client built into Quartz — log in, browse your servers and DMs, read and send messages, and join voice chat, all without leaving the game.

## Where to find it

Open the Quartz menu in-game and select **Discord** from the sidebar.

## Logging in

- **Log In with QR** shows a QR code — open Discord on your phone, go to **Settings → Scan QR Code**, and point your camera at it.
- Or paste a **Discord token** into the field and press **Log In**.
- Once you're logged in with a saved token, **Forget Saved Token** signs you out and clears it.

!!! warning "About tokens"
    Pasting a token gives Quartz full access to your account, and third-party clients that use one this way are against Discord's terms of service. The QR login doesn't have this problem.

## Browsing and messaging

The left rail lists your servers and **Direct Messages**, each with its own icon; picking one loads its channel list beside it. Locked channels show a lock icon and can't be opened. Select a channel to load its recent messages, then type in the box at the bottom and press **Send** (or Enter) to post. Channels created, renamed, or deleted while you're looking at a server are picked up as they happen, and the lists keep their scroll position when the page redraws.

Messages are rendered the way Discord shows them: profile pictures, standard and custom server emoji as pictures, and the usual formatting — bold, italics, underline, strikethrough, headings, subtext, bullet lists, quotes, spoilers, inline code and code blocks, and links shown by their label. Mentions of people and channels show their names, and timestamps are converted to your local time; typing `@name` in the composer turns it back into a real mention when you send. Several messages in a row from the same person are grouped under one name and timestamp.

Pictures come through too: image attachments, linked media, and embed images render inline — up to four per message — while embeds show their title and description and any other attachment appears as a file line with its name.

!!! note
    Animated emoji are drawn as a still frame.

## Voice chat

Open a voice channel and press **Join Voice** in the bar above the chat to connect; the same button becomes **Disconnect** once you're in. While connected, **Mute**/**Unmute** toggles your microphone, and the status line shows the end-to-end encryption state along with live sent/received/dropped audio frame counts.

Voice needs a small native runtime that isn't bundled with Quartz. You don't have to fetch it yourself — the first time you join a call, Quartz downloads and installs it, with progress on the status line.

!!! note "Not available on every platform"
    If no voice runtime is published for your platform, voice chat isn't available, and the status line says so when you try to join.
