# tmux guide

## Shortcuts

`CTRL + b` called prefix

### Sessions Management

| keys                                            |                                   actions |
| :---------------------------------------------- | ----------------------------------------: |
| `tmux`                                          |       create new session (default name 0) |
| `tmux new -s <session_name>`                    |              create new session with name |
| `prefix` + `d`                                  | Detach (tmux still running in background) |
| `tmux ls`                                       |                          List of sessions |
| `tmux a`                                        |                     Open recently session |
| `exit` or `tmux kill-session -t <session_name>` |                             close session |

---

### Panes Management

| keys                 |                 actions |
| :------------------- | ----------------------: |
| `prefix` `%`         |      divided left-right |
| `prefix` `"`         |      divided top-bottom |
| `prefix` `arrow`     |          focus sessions |
| `prefix` `z`         |                    zoom |
| `exit` or `CTRL + d` | close currently session |
