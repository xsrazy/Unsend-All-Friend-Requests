# Unsend All Friend Requests

A tiny browser console script that cancels all your sent Facebook friend requests at once, from a PC or laptop. No installation, no password or token needed.

![Screenshot](screenshot.png)

## About

Unsend All Friend Requests cleans up your outgoing Facebook friend requests in one go. If you have sent requests that were never accepted, the pending list keeps piling up, and cancelling them one by one takes forever. This script withdraws every loaded request for you in seconds.

It runs entirely in your own browser through the developer console. The script finds every Cancel Request button loaded on the page and clicks them one by one. It only acts on buttons that are already on your screen, and it never asks for your password, token, or any account access.

## Features

- Cancels all sent (outgoing) Facebook friend requests loaded on the page at once
- Runs in the browser developer console (F12), no extensions or software to install
- No password, token, or account access needed, and no data leaves the page
- The whole script is four lines of plain JavaScript, easy to read before you run it

## How It Works

The entire script:

```js
var inputs = document.getElementsByClassName('_54k8 _52jg _56bs _26vk _2b4n _56bt');
for (var i = 0; i != inputs.length; i++) {
  inputs[i].click();
}
```

It collects every element carrying that class combination, which is how the Cancel Request buttons are marked in Facebook's mobile web layout, and clicks them one by one. It makes no network calls of its own: the cancellations are the same clicks you would make by hand, just automated.

## Requirements

- A PC or laptop with a desktop browser that has a developer console (Chrome, Edge, Firefox, and similar)
- The mobile Facebook site (m.facebook.com), which is where the request list and its buttons appear

## How to Use

1. Open your outgoing requests page: https://m.facebook.com/friends/center/requests/outgoing/#friends_center_main
2. Scroll down until the list stops loading
3. Press F12 to open the developer console
4. Paste the script from [script.txt](https://github.com/xsrazy/Unsend-All-Friend-Requests/blob/main/script.txt) into the console, then press Enter
5. Done. Every loaded request is cancelled

## Notes

- Only requests that have been scrolled into view get cancelled, so scroll until the full list has loaded first if you have many pending requests
- The script finds the Cancel Request buttons by their page classes in Facebook's mobile layout, so if Facebook changes its layout, the selector in the script may need an update

## License

MIT License. See [LICENSE](LICENSE) for details.

<a href="https://www.buymeacoffee.com/xsrazy" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
