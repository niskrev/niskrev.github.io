---
title: Save tmux sessions
layout: post
category: til
tags: [unix, tmux]
---
To detach from current session
```
ctrl+a d
```

To list existing tmux sessions:
```
tmux ls
```

To reattach to session
```
tmux attach
```

or, if there are multiple sessions
```
tmux attach -t [session number]
```

