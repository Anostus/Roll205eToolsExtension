# Beyond20 5e.tools Experimental Build

This repository contains an experimental Beyond20 build with additional 5e.tools support.

Use the browser-specific zip files for local developer-mode installation. The source zip and patch are included for review, diffing, or rebuilding from source.

## Files

| File | Purpose |
| --- | --- |
| `Beyond20-5etools-reference-chrome-unpacked.zip` | Chrome / Chromium unpacked extension build |
| `Beyond20-5etools-reference-firefox-unpacked.zip` | Firefox temporary add-on unpacked build |
| `Beyond20-5etools-reference-source.zip` | Modified source tree |
| `Beyond20-5etools-reference-support.patch` | Patch from the previous 5e.tools expanded build |

## What this build adds

This build keeps Beyond20's existing functionality intact and adds experimental 5e.tools support for:

- Bestiary / monsters, including legendary creatures
- Monster actions, traits, attacks, saves, skills, initiative, HP, and damage dice
- Spells, including spell cards and damage dice
- Magic items
- Classes and selected subclasses
- Races
- Feats
- Backgrounds

Supported 5e.tools page families include:

- `bestiary.html`
- `spells.html`
- `items.html`
- `classes.html`
- `races.html`
- `feats.html`
- `backgrounds.html`

## Install in Chrome or Chromium browsers

These steps also generally apply to Chromium-based browsers such as Edge, Brave, Vivaldi, and Opera, though labels may vary slightly.

1. Download `Beyond20-5etools-reference-chrome-unpacked.zip`.
2. Unzip it somewhere permanent, for example:
   - macOS/Linux: `~/Extensions/Beyond20-5etools/`
   - Windows: `Documents\Extensions\Beyond20-5etools\`
3. Open Chrome and go to `chrome://extensions`.
4. Turn on **Developer mode**.
5. Click **Load unpacked**.
6. Select the extracted folder that contains `manifest.json`.
7. Keep the extracted folder in place. Chrome loads the extension from that folder, so deleting or moving it can break the install.
8. Optional: pin Beyond20 from the puzzle-piece extensions menu.

### Updating Chrome

1. Download and unzip the newer Chrome build.
2. Either replace the old extracted folder with the new one, or load the new folder separately.
3. Go to `chrome://extensions` and click **Reload** on the Beyond20 card.
4. Refresh any open Roll20, Foundry, D&D Beyond, or 5e.tools tabs.

## Install in Firefox Developer Mode / Temporary Add-on mode

Firefox loads unpacked local extensions as temporary add-ons for testing. Temporary add-ons are removed when Firefox restarts, so you will need to reload the extension after restarting Firefox.

1. Download `Beyond20-5etools-reference-firefox-unpacked.zip`.
2. Unzip it somewhere convenient.
3. Open Firefox and go to `about:debugging#/runtime/this-firefox`.
4. Click **Load Temporary Add-on...**.
5. In the extracted folder, select `manifest.json`.
6. Beyond20 should appear under temporary extensions.
7. Refresh any open Roll20, Foundry, D&D Beyond, or 5e.tools tabs.

### Updating Firefox

1. Download and unzip the newer Firefox build.
2. Go to `about:debugging#/runtime/this-firefox`.
3. Remove the older temporary Beyond20 add-on if it is still loaded.
4. Click **Load Temporary Add-on...** again and select the new build's `manifest.json`.
5. Refresh your VTT and 5e.tools tabs.

## Basic testing checklist

After installing the extension:

1. Open your VTT in one tab, such as Roll20 or Foundry VTT.
2. Open a supported 5e.tools page in another tab.
3. Confirm Beyond20's page buttons appear.
4. Try a few rolls:
   - Monster attack roll
   - Monster damage roll
   - Legendary action or trait display
   - Spell card display
   - Spell damage roll
   - Race, feat, background, class, or subclass feature display
5. If buttons do not appear, refresh the 5e.tools page after the page content fully loads.
6. If rolls do not reach the VTT, refresh both the VTT tab and the 5e.tools tab.

## Known limitations

- This is a local/developer-mode build, not a Chrome Web Store or Firefox Add-ons release.
- Firefox temporary add-ons do not persist after Firefox restarts.
- 5e.tools pages are dynamic and often update content after navigation or hash changes. Refreshing the 5e.tools tab may be necessary after switching entries.
- This build was validated with static page samples and package checks, but it has not been fully end-to-end tested against every VTT/page combination.

## Checksums

SHA-256 checksums for the included build artifacts:

```text
ce2afb473695775b5e1c86d79d9f2ee3f632f57072037ed62719dc925e74ad0c  Beyond20-5etools-reference-chrome-unpacked.zip
2b9cc0f7b8f36a7f4c6e31516a11a05405ff0332fdcd6059faf67ebf924d0f25  Beyond20-5etools-reference-firefox-unpacked.zip
79f34f34a8ac2822849cf80471aba5c5a84422bc0ab379957955d76e741fcf27  Beyond20-5etools-reference-source.zip
1fd1421f5a44aa6fe0cbb28870f3ef84712ef67791237e2fbae3e30ccd96acbc  Beyond20-5etools-reference-support.patch
```

## Official browser references

- Chrome unpacked extension loading: https://developer.chrome.com/docs/extensions/get-started/tutorial/hello-world#load-unpacked
- Chrome admin/testing instructions for unpacked extensions: https://support.google.com/chrome/a/answer/2714278
- Firefox temporary extension loading: https://extensionworkshop.com/documentation/develop/temporary-installation-in-firefox/
- Firefox `about:debugging`: https://firefox-source-docs.mozilla.org/devtools-user/about_colon_debugging/index.html
