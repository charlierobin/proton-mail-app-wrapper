# proton mail app wrapper
 
Basically just a web view in a window, with the URL set to:

`https://mail.proton.me/u/0/inbox`

So the first launch prompts the usual Proton Mail log in process, then displays the usual Proton Mail interface.

The app writes simple preferences … window position and size … so it can be restored correctly on quit/relaunch.

The only other thing it does is look for title changes in the HTML web page, and when they occur parse for Proton Mail’s standard unread messages text: the number of unread messages in brackets at the start of the title.

If found, it checks the number to see if the number of unread messages has increased, plays an alert sound if it has.

It also updates the app’s Dock icon with the number of unread messages, similar to Apple Mail.

All in all: very very simple. But sometimes it’s the simple things in life that make me happy…

