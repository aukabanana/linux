# tmux guide

## Shortcuts

### Sessions Management

| keys                                            |                                   actions |
| :---------------------------------------------- | ----------------------------------------: |
| `tmux`                                          |       create new session (default name 0) |
| `tmux new -s <session_name>`                    |              create new session with name |
| `Ctrl + b` + `d`                                | Detach (tmux still running in background) |
| `tmux ls`                                       |                          List of sessions |
| `tmux a`                                        |                     Open recently session |
| `exit` or `tmux kill-session -t <session_name>` |                             close session |

