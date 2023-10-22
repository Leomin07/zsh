```
if [[ $TERM = dumb ]]; then
    unset zle_bracketed_paste
fi
# Use bash-completion, if available
[[ $PS1 && -f /usr/share/bash-completion/bash_completion ]] && \
    . /usr/share/bash-completion/bash_completion

```
