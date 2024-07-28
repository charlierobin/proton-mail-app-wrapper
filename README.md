# proton mail app wrapper

## Regrettably, I've just noticed that of some point in JUly 2024, Proton have changed things so that their site is no longer loading (although it still seems happy enough in my Catalina version of Safari).

I've tried fiddling with various user agent signatures in an attempt to fool it into working, but so far no luck.

So at the moment, this is all useless. Which is a shame, as I used to use it a lot, but I just don't have the time to look into it further.

## —————
 
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

I wanted to be able to have multiple Proton Mail and GMail accounts as icons in my Dock:

<img width="171" alt="Screenshot 2023-09-18 at 13 24 30" src="https://github.com/charlierobin/proton-mail-app-wrapper/assets/10506323/252947e7-907f-4cc0-83af-938b26cbe87e">


There's more detailed information about all of this at https://github.com/charlierobin/google-mail-wrapper, which is another slightly different version of the app I built to handle GMail accounts.

[Download universal binary (Intel and ARM)](https://dl.dropboxusercontent.com/s/g05jtdmdzspl6o0/ProtonMail.zip?dl=0) for those who can’t be bothered to compile their own version from scratch.

<img width="373" alt="Screenshot 2023-09-16 at 12 36 13" src="https://github.com/charlierobin/proton-mail-app-wrapper/assets/10506323/067f3e74-0d4d-4d2e-81ca-3c20d036a43b">
