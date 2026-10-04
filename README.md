# 汉字卡 HSK Flashcards

A Mandarin flashcard app for reading and writing the 1,208 words of HSK levels 1–4. It runs in the browser, installs on a phone like a native app, and works offline.

**Open the app:** https://dmcavity.github.io/Mandarin/

## Features

- **Two drills for every word.**
  - **Reading 认:** see the characters, recall the pinyin and meaning, then flip the card to check.
  - **Writing 写:** see the pinyin and meaning, write the characters from memory on the screen, then reveal the answer or watch the stroke order animate.
- **Three ratings.** Each answer is rated **Solid**, **Tentative** or **Not learned**, separately for reading and writing. Each deck can be studied in full or filtered to one rating. In a Tentative or Not learned pass, words you already know in the other mode come first.
- **Words for review.** A short daily selection of Solid words. It favours words you have had to relearn and words you haven't seen for a while, and passes over words you have recalled correctly many times running. You set the number per deck.
- **Initial scheduled reviews.** A word that has just become Solid comes back after a set number of days (1, 3 and 6 by default) to fix it in long-term memory before it joins the daily review.
- **Progress.** A chart of how long your Solid words are remembered, grouped by each word's longest recall: the longest gap between reviews after which you still recalled it. A list shows words that have gone past their longest recall. Tap any part of the chart to review those words.
- **Your own lists and words.** Make lists for a textbook chapter, a topic or anything else, and add words that aren't in HSK 1–4. Progress on a word is shared between your list and its HSK deck.
- **Add words from other apps** (Android). Share a word from Google Translate, a browser or any other app to the app, or copy it and use the **Paste** button on the add-word screen. If only English text arrives, the app looks up the Chinese.
- **Search** by English or pinyin.
- **Pronunciation** using the Chinese voices installed on your device.
- **Character breakdowns** show each part of a character with its pinyin and meaning, and whether it gives the character its meaning or its sound. Breakdowns cover about 9,500 characters, including those in words you add.
- **Example sentences** for HSK words.
- **Offline.** Everything except the optional online lookups is stored in the app.

## Install

**Android (Chrome):** open the link above, tap ⋮, then **Install app** or **Add to Home screen**. Sharing words from other apps only works once the app is installed.

**iPhone or iPad (Safari):** open the link, tap Share, then **Add to Home Screen**. Sharing from other apps isn't available on iOS; use the Paste button instead.

**Desktop:** the app also runs in any modern browser. Chrome and Edge offer an install button in the address bar.

New versions load automatically the next time the app is opened with a connection.

## Your data

- **Progress stays on your device.** It is stored in the browser's local storage, and the review history in IndexedDB. Nothing is sent to a server.
- **Back up regularly:** **Settings → Data → Back up progress** saves a dated file with every rating, review date and the review history. Clearing the browser's site data, or uninstalling the app, erases progress that hasn't been backed up.
- **Restore** from a backup file through **Settings → Data → Restore from backup**. This is also how to move progress to another device.
- **Online lookups** are optional and can be turned off in Settings. When used, the word is sent to the MyMemory translation service. Stroke data for a character outside the bundled set is fetched from the jsDelivr CDN.

## Files

| File | Contents |
|---|---|
| `index.html` | The whole app: code, styles, HSK vocabulary, example sentences, character data and the bundled Hanzi Writer library |
| `sw.js` | Service worker for offline use and updates |
| `manifest.json` | App name, icons, and the share target that lets other apps send words to it |
| `dict.json` | Dictionary used to look up words you add (from CC-CEDICT) |
| `chars.json` | Character breakdowns for characters outside HSK 1–4, loaded when a breakdown needs one (from Make Me a Hanzi and CC-CEDICT) |
| `strokes.json` | Stroke outlines for the 1,073 characters in the app (from hanzi-writer-data) |
| `icon-192.png`, `icon-512.png` | App icons |
| `THIRD-PARTY-NOTICES.md`, `ARPHICPL.TXT` | Credits and licences for the components below |

There is no build step. The files are served as they are.

## Hosting your own copy

1. Fork this repository.
2. In the fork's **Settings → Pages**, publish from the `main` branch, root folder.
3. In `manifest.json`, change `share_target.action` to your own Pages address, e.g. `https://<your-username>.github.io/<repo-name>/`.

## Credits and licences

The app builds on:

- [Hanzi Writer](https://github.com/chanind/hanzi-writer) (MIT);
- stroke data from [hanzi-writer-data](https://github.com/chanind/hanzi-writer-data) and [Make Me a Hanzi](https://github.com/skishore/makemeahanzi) (Arphic Public License);
- Make Me a Hanzi dictionary data (LGPL v3 or later);
- [CC-CEDICT](https://www.mdbg.net/chinese/dictionary?page=cc-cedict) (CC BY-SA 4.0);
- HSK word lists by [clem109](https://github.com/clem109/hsk-vocabulary) and [drkameleon](https://github.com/drkameleon/complete-hsk-vocabulary) (MIT);
- word frequencies from SUBTLEX-CH (Cai & Brysbaert, 2010).

Full details, including how the stroke data was modified, are in [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md). The same list appears in the app under **Settings → About → Credits & licences**.

`dict.json` is derived from CC-CEDICT and is shared under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). `chars.json` is derived from Make Me a Hanzi and CC-CEDICT and is shared under their licences (LGPL v3 or later; CC BY-SA 4.0).

Built with the help of [Claude](https://www.anthropic.com), by Anthropic.
