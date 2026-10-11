# spotify-deck

A Spotify control for the [Omarchy](https://omarchy.org/) top bar.

A Spotify logo sits in the bar. Click it for a panel with album art, a seek
bar, previous / play-pause / next, shuffle, repeat and volume. Right-click
focuses the Spotify window, or launches Spotify when it is closed.

It only talks to Spotify over MPRIS, so other players (browser tabs, mpv)
never take over the controls.

## Install

```bash
cp -r plugins/aaditya.spotify ~/.config/omarchy/plugins/
omarchy-shell shell rescanPlugins
omarchy plugin enable aaditya.spotify --section right --index 0
```

After editing the widget, run `omarchy restart shell` to load the change.

## Options

```bash
omarchy bar set aaditya.spotify showControls true --json   # inline prev / play / next
omarchy bar set aaditya.spotify showLabel true --json      # track and artist in the bar
omarchy bar set aaditya.spotify maxLabelWidth 300 --json   # label width, default 220
```

`shell.json` is a snapshot of the bar layout this was built for.
