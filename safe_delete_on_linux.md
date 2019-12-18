Add function to .zshrc.

```shell
# safe rm
alias rm=del
function del {
    local F
    for F; do
        mv -- "$F" ~/.trash/"$F-$(exec date '+%F-%T')"
    done
}

function cleardel {
    /bin/rm -rf ~/.trash/*
}
```
