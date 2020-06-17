## Android focus will not trigger soft keyboard

I've created this sample repo to reproduce an issue (or intended behavior?) related to input focus when a webview is served from Android.

This sample app contains a single text input (type number) that receives focus after 3000 ms using setTimeout. On iOS this runs as I would expect. They input field receives focus and the OS soft keyboard is shown.

However, on Android although the input field receives focus the keyboard is not triggered. Focus is received as it is both visible with a blinking caret as well as confirmed by document.activeElement.

If the user interacts with the page canvas (just tap anywhere else but the input itself) before the 3000 ms has elapsed, the input receives focus and the keyboard is triggered.

On iOS it seems this behavior can be controlled with the KeyboardDisplayRequiresUserAction configuration. But I haven't been able to figure out how to do something similar for Android.

I know I can trigger the keyboard manually using the Capacitor keyboard plugin, but that way the input type (here number) will no be respected and the regular keyboard is shown.

Is this is expected behavior and if so is there anything we can do to override this?
