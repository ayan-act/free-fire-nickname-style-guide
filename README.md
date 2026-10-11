# Unicode nickname compatibility guide

Unicode nickname styling is often called a “font”, but copied names are text characters. This guide explains what changes when letters, symbols, and emoji are added to a gaming nickname. It includes a small local character inspector for checking the text you intend to paste.

For creating a name, use the [FF Name Style generator by FF Bio Code](https://ffbiocodes.com/ff-name-style/). This repository is a companion reference, not a mirror of that page or an official Free Fire guide.

## Why a short name may still fail

There are several ways to measure text:

| Measure | Example: `A✿` | What it tells you |
| --- | --- | --- |
| UTF-16 code units | 2 | JavaScript string storage length |
| Unicode code points | 2 | Number of encoded characters |
| Grapheme clusters | 2 | Approximate user-perceived characters |

These numbers can differ. For example, `👨‍👩‍👧` appears as one family emoji but contains multiple code points joined together. Combining marks can also make one visible character from more than one code point. A game's actual limit and permitted character set are determined by the current game client and server, so no local counter can promise acceptance.

## Practical checks

1. Start with a readable base name. Add one decorative element at a time.
2. Use the [character inspector](unicode-inspector.html) to see code points and invisible or combining characters in a draft.
3. Paste the result into the game's name field. Check rendering, accepted length, and availability there before completing a name change.
4. If the name is rejected, remove an emoji, joiner, invisible space, or elaborate frame and retry.

The inspector runs locally in the browser. It does not upload your text or connect to a game account. It reports text structure only; it does not validate Free Fire names.

## Examples

| Draft | Observation |
| --- | --- |
| `NOVA` | Simple Latin letters are easiest to read across devices. |
| `ɴᴏᴠᴀ` | Small-cap-like characters are distinct Unicode code points. |
| `༺NOVA༻` | Frames add characters that may count toward a limit. |
| `NO​VA` | This example contains a zero-width space between `O` and `V`; the inspector exposes it. |

Compatibility varies by platform and may change. This repository intentionally avoids claiming that a particular name or symbol is guaranteed to work.

## Attribution

Created as a companion resource for [FF Bio Code](https://ffbiocodes.com/ff-name-style/). Fan-made educational content; no affiliation with or endorsement by Garena or Free Fire.

