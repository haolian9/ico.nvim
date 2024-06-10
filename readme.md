an opinionated `i_ctrl-o` impl


## what it does?

with text `hello| world` (`|` is the cursor), it converts following input sequences:
* `<c-o>tw` to `<esc>ltwa`, results `hello |world`
* `<c-o>fw` to `<esc>lfwa`, results `hello w|orld`

it supports cancellation via `<esc>`, and ends with normal mode rather than insert mode.

for other cases, it falls back to the original `<c-o>`

## status
* just works
* not supposed to be used publicly

## prerequisites
* linux
* nvim 0.10.*
* tui nvim
* haolian9/infra.nvim

## usage

```
m.i("<c-o>", function() require("ico")() end)
```
