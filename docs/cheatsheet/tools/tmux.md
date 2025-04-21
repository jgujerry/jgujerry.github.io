# Tmux

tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal.

Tmux has three levels of hierarchy: Session, window, and pane.

* `session`: A group of windows, plus a notion of which window is current.
* `window`: A single screen with a group of panes.
* `pane`: A rectangular part of a window that runs specific commands.

## Prefix

`Ctrl + b` is the prefix key.


## Sessions

1 - Start new session

```bash
$ tmux
$ tmux new
$ tmux new-session

$ tmux new -s mysession
```

Or use command mode,

```bash
: new
: new -s mysession
```

2- List sessions

```bash
$ tmux ls
$ tmux list-sessions
```
or, use `Ctrl + b s`

3 - Rename session

`Ctrl + b $`

4 - Detach session

`Ctrl + b d`

Or use command mode

```bash
: attach -d
```

5 - Attach session

```bash
# last session
$ tmux a
$ tmux at
$ tmux attach
$ tmux attach-session

# session with name
$ tmux a -t mysession
$ tmux at -t mysession
$ tmux attach -t mysession
$ tmux attach-session -t mysession
```

6 - Swith session

`Ctrl + b (` (move to previous session)

`Ctrl + b )` (move to next session)

7 - Kill session

```bash
# kill by name
$ tmux kill-ses -t mysession
$ tmux kill-session -t mysession

# kill all but the current
$ tmux kill-session -a

# kill all but mysession
$ tmux kill-session -a -t mysession
```


## Windows

1 - Create window

`Ctrl + b c`

2 - Switch window

`Ctrl + b p` (previous)

`Ctrl + b n` (next)

`Ctrl + b 0 ... 9` (number)

3 - Rename window

`Ctrl + b ,`

4 - Close window

`Ctrl + b &`


## Panes

1 - Split panes

`Ctrl + b %` (vertical)

`Ctrl + b "` (horizontal)

2 - Show pane numbers

`Ctrl + b q`

3 - Switch to panes

`Ctrl + b` &uarr; &darr; &rarr; &larr; (directions)

`Ctrl + b o` (next)

`Ctrl + b q 0...9` (number)

4 - Resize panes

`Ctrl + b + `&uarr; &darr; &rarr; &larr;

`Ctrl + b` - `Ctrl + `&uarr; &darr; &rarr; &larr;

5 - Toggle Zoom

`Ctrl + b z`

Toggle layout
  
`Ctrl + b Space`

6 - Move pane

`Ctrl + b {` (left)

`Ctrl + b }` (right)

7 - Convert to window

`Ctrl + b !`

8 - Kill pane

`Ctrl + b x`


## Others

1 - Enter command mode

`Ctrl + b :`

2 - Set for all sessions

```bash
: set -g OPTION
```

3 - Set for all windows

```bash
: setw -g OPTION
```

4 - Help

`Ctrl + b ?`
```bash
$ tmux info
```

## Settings

Enable mouse to scroll on pane

`Ctrol + b :`
```bash
$ set -g mouse on  # session wide
$ setw -g mouse on # window wide
```

Happy tmuxing!