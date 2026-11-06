# Galaxy Games

Twelve free learning games for kids aged 5–15. Every game is a single HTML file with no build step, no frameworks. The site is supported by Google AdSense ads (see Ads below). Open `index.html` in a browser, or host the folder on any static host.

## Games

### Ages 5–8
| Game | Folder | Skills |
|---|---|---|
| Star Catcher | `star-catcher/` | Adding, taking away, times tables to 5 |
| Memory Match | `memory-match/` | Memory, animal names |
| Spelling Bubbles | `spelling-bubbles/` | Spelling 3, 4 and 5-letter words |
| Counting Garden | `counting-garden/` | Counting to 5, 10 or 20 |
| Shape Sorter | `shape-sorter/` | Shapes and colours |
| Color Echo | `color-echo/` | Memory and focus (ages 5+) |

### Ages 9–15
| Game | Folder | Skills |
|---|---|---|
| Galaxy Defenders | `galaxy-defenders/` | Math, science, geography, English, logic |
| Word Forge | `word-forge/` | Vocabulary (Wordle-style, daily word) |
| Code Quest | `code-quest/` | Coding basics with command blocks |
| Typing Rocket | `typing-rocket/` | Typing speed and accuracy |
| Lemonade Tycoon | `lemonade-tycoon/` | Money, profit and business decisions |
| Logic Lights | `logic-lights/` | Logic puzzles |

## Run locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765.

## Host for free

- **GitHub Pages:** Settings → Pages → deploy from the `main` branch, root folder.
- **Netlify:** drag this folder onto https://app.netlify.com/drop.

## Customise

- Each game has its settings (speeds, round lengths, word lists) near the top of its `<script>`.
- Galaxy Defenders questions live in the `QUESTION BANK` section, one per line: `Question|Right answer|Wrong 1|Wrong 2|Wrong 3|Why`.
- Word Forge words live in `WORDS_TEXT`, one per line: `WORD|clue`.

## Ads

Every page loads Google AdSense **Auto ads**; you choose where ads appear in AdSense → Ads → By site. Ads are requested as non-personalised because the players are children.

To go live, replace the placeholder publisher ID `XXXXXXXXXXXXXXXX` with your own (the digits after `ca-pub-`) in every page and in `ads.txt`:

```bash
grep -rl XXXXXXXXXXXXXXXX . | xargs sed -i '' 's/XXXXXXXXXXXXXXXX/1234567890123456/g'
```

`ads.txt` must be served from the root of your domain (for example `https://example.com/ads.txt`).

## Privacy

No sign-up and no chat. Scores and progress are saved only in the browser's local storage on the device. Google AdSense may use cookies to serve and measure ads.
