# proton mail app wrapper
 
Basically just a web view in a window, with the URL set to:

`https://mail.proton.me/u/0/inbox`

So the first launch prompts the usual Proton Mail log in process, then displays the usual Proton Mail interface.

The app writes simple preferences … window position and size … so it can be restored correctly on quit/relaunch.

The only other thing it does is look for title changes in the HTML web page, and when they occur parse for Proton Mail’s standard unread messages text: the number of unread messages in brackets at the start of the title.

`(1) Inbox | emailaddress@proton.me | Proton Mail` -> there’s one unread message

If found, it checks the number to see if the number of unread messages has increased, plays an alert sound if it has.

It also updates the app’s Dock icon with the number of unread messages, similar to Apple Mail.

If there are no unread messages, the dock icon is cleared.

All in all: very very simple. But sometimes it’s the simple things in life that make me happy…

I created this app because I wanted to work with Proton Mail separately from my usual web browser (because I'm frequently clearing cookies/web data etc, and it was getting to be a real pain constantly reauthenticating). I also wanted to be able to have a separate app for each Proton Mail account.

There's more detailed information about all of this at https://github.com/charlierobin/google-mail-wrapper, which is another slightly different version of the app I built to handle GMail accounts.

[Download universal binary (Intel and ARM)](https://dl.dropboxusercontent.com/s/g05jtdmdzspl6o0/ProtonMail.zip?dl=0) for those who can’t be bothered to compile their own version from scratch.

