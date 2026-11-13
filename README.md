# Lore

Language-learning video and book library that runs **locally in your browser**.
Your library and progress stay on your own computer.

<!-- Add one or two screenshots here, e.g.:  ![Lore home page](docs/home.png) -->

## What it does

- Build a library of videos (YouTube channels and playlists) and study with subtitles
- Look up words while you watch or read, and keep vocabulary sets per language
- Podcast page: audio episodes with transcripts
- Study time, streaks and goals; automatic local backups
- Interface in English, French and Japanese
- Optional Japanese word analysis (readings, base forms)

## Install

You need **Python 3.9 or newer** and [pipx](https://pipx.pypa.io/).

1. Open the [latest release](https://github.com/tiagozero/Lore/releases/latest).
2. Under **Assets**, right-click the `.whl` file and choose **Copy link address**.
3. Install it:

   ```
   pipx install --force "PASTE_THE_LINK_HERE"
   ```

4. Start Lore and open the address it prints (normally <http://localhost:8765/>):

   ```
   lore
   ```

Check your version with `lore --version`.

## Update

Stop Lore (Ctrl+C), install the newer `.whl` the same way as above, start Lore again and
refresh the page with Ctrl+Shift+R. Your progress is kept: it lives in your data folder, not
in the program.

Screen-only updates can come as a small *UI pack*:

```
lore update-ui lore-ui-X.Y.Z.zip      # install
lore reset-ui                         # go back to the screens inside the installed version
```

## Where your data is

| System  | Folder                                  |
|---------|-----------------------------------------|
| Linux   | `~/.local/share/lore`                   |
| macOS   | `~/Library/Application Support/lore`    |
| Windows | `%APPDATA%\lore`                        |

Set the `LORE_HOME` environment variable to use another folder (for example an external drive).

## Optional: Japanese analysis

```
pipx inject lore sudachipy sudachidict_small
```

## Podcast audio

The audio files are large and are **not** part of the program. Download them separately and
unzip them into `<data folder>/ui/` so that you get `ui/Podcast/<Language>/<Show>/...`.
<!-- Add the link to your audio release here. -->

## Privacy

Lore runs on your computer and only listens on `localhost`. Videos play through YouTube's
embedded player, so YouTube sees that playback, and dictionary look-ups open the dictionary
sites you choose.

## License

<!-- Choose one and add a LICENSE file, for example MIT. Until you do, nobody else may legally reuse the code. -->
