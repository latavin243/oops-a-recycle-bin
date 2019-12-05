```bash
find . -name "*cb*" | fzf | xargs -I{} xclip -selection clipboard -t image/png -i {}
```

## Bash function
```bash
ii ()
{
    local cli=`baseff file $* | xargs echo -n`;
    if [[ "${cli}" = ~ ".png" ]]; then
        echo -n ${cli} | xargs -I{} xclip -selection clipboard -t image/png -i {};
        echo "${cli} => clipboard";
    fi
}
```

## My custom function
```
function ffc {
    local cli=`fd $* | fzf | xargs echo -n`;
    case "${cli##*.}" in
        "png")
            echo -n ${cli} | xargs -I{} xclip -selection clipboard -t image/png -i {}
            ;;
        "py")
            echo -n ${cli} | xargs -I{} xclip -selection clipboard -i {}
            ;;
        "go")
            echo -n ${cli} | xargs -I{} xclip -selection clipboard -i {}
            ;;
        "yaml")
            echo -n ${cli} | xargs -I{} xclip -selection clipboard -i {}
            ;;
        "yml")
            echo -n ${cli} | xargs -I{} xclip -selection clipboard -i {}
            ;;
        *)
            echo "unsupported type"
    esac
}
```
