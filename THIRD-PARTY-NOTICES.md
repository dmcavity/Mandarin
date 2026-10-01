# Third-party notices

汉字卡 HSK Flashcards is built on the following work. The same list appears in the app under **Settings → About → Credits & licences**.

| Component | Used for | Licence |
|---|---|---|
| [Hanzi Writer](https://github.com/chanind/hanzi-writer) v3.7.3, © 2014 David Chanin | Drawing characters and animating stroke order. Bundled inside `index.html`, with its full licence notice. | MIT |
| [hanzi-writer-data](https://github.com/chanind/hanzi-writer-data) 2.0.1, from [Make Me a Hanzi](https://github.com/skishore/makemeahanzi), derived from the fonts AR PL KaitiM GB and AR PL UKai, © 1999 Arphic Technology Co., Ltd. | Stroke data, in `strokes.json`. **Modified September 2026:** only the characters this app uses are included, combined into one file, with each character's `radStrokes` field removed. Stroke outlines and medians are exactly as published. | Arphic Public License — see [`ARPHICPL.TXT`](ARPHICPL.TXT) |
| [Make Me a Hanzi](https://github.com/skishore/makemeahanzi) dictionary data, derived from Unicode Unihan and CJKlib | Character components, radicals, meanings and etymology hints. A trimmed copy is inside `index.html`. | [GNU LGPL v3 or later](https://www.gnu.org/licenses/lgpl-3.0.html) |
| [CC-CEDICT](https://www.mdbg.net/chinese/dictionary?page=cc-cedict), maintained by MDBG, continuing CEDICT by Paul Denisowski | Dictionary meanings. A selected, reformatted subset is in `dict.json`, which is shared under the same licence. | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
| [hsk-vocabulary](https://github.com/clem109/hsk-vocabulary) by clem109 (data from gigacool/hanyu-shuiping-kaoshi); [complete-hsk-vocabulary](https://github.com/drkameleon/complete-hsk-vocabulary) by Yanis Zafirópulos | HSK 2.0 level assignments, then checked and corrected by hand. | MIT |
| SUBTLEX-CH — Cai, Q. & Brysbaert, M. (2010). *SUBTLEX-CH: Chinese word and character frequencies based on film subtitles.* PLoS ONE 5(6): e10729. | Choosing which dictionary entries to include. | Cited |
| [MyMemory](https://mymemory.translated.net) by Translated | Optional online lookups for words not in the dictionary. | Web service |

Built with the help of Claude, by [Anthropic](https://www.anthropic.com), which wrote much of the code and the example sentences.
