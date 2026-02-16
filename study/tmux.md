# とりあえず、これだけ
起動
```
tmux
```

分割
```
Ctrl+b → %
Ctrl+b → "
```

ペイン移動
```
Ctrl+b → 矢印
```

ペイン閉じる
```
exit
```

デタッチ / 再接続
```
Ctrl+b → d
tmux attach
```

リサイズ
~/.tmux.conf
```
bind -r H resize-pane -L 1
bind -r L resize-pane -R 1
bind -r K resize-pane -U 1
bind -r J resize-pane -D 1
set -g mouse on
```

反映
```
tmux source-file ~/.tmux.conf
```
