# BemaniPatcher
A tool to easily apply known hex edits to any binary, with examples for Bemani games.

Should work on most modern browsers.

Live version hosted as part of [linux arcade guide](https://nixac.codeberg.page/patcher/).

Repository contains additional experimental patches, that aim to support running these games through wine.

## Asking about new patches
If you would like new hex edits, make them yourself and make a pull request!

## Patch rules
- acceptable quality (doesn't cause obvious clashes with other patch or is marked in some way if so)
- while this fork accepts any patches for listed titles, you may prefer to submit your patch to [mon's BemaniPatcher](https://github.com/mon/BemaniPatcher/) instead, this fork pulls changes from upstream periodically, so your changes should be reflected here as well (unless patch here supersedes the one in upstream repository)

## Submitting a new game
Here is your checklist:
- Add the new game html, it is easiest to copy an existing game and modify it.
  The html should be named `[game][release].html` except IIDX because they just
  happen to be `[release].html` only...
- Modify the `<title>` tag and the `<h1>` tag to the name of the new game.
- Modify the patcher for the new DLL names/patches.
- Keep consistent indentation for the new patches. I will have to fix your PR if
  it contains poor formatting, which will delay the merging process.
- Modify `index.html` to add the new game. Sorting: alphabetical by game series,
  then in release order per game.
- Add a game image. 128x128px PNG files, please. Any blank space should be
  either white or transparent.

If your pull request is a single commit, I will rebase and merge. If it is
multiple commits, I will squash and merge.

Please do not worry about submitting "bad" PRs. If there is something wrong, I
will tell you how to fix it or I will fix it myself before merging.
