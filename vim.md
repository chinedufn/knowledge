## Highlight long lines of text

http://vim.wikia.com/wiki/Highlight_long_lines

- I use this when writing a tutorial to split up any code block lines that will cause an overflow

## Scratch Buffers

I wanted to map keys to run `node` on the tape test file and show the output in a new buffer within vim.

Needed to set local options onto `new` so that that buffer would close when we hit `:q`.
Otherwise we get an error that explains that there are unsaved writes to an open buffer.

```viml
function! s:node_test_current()
    execute 'new | setlocal nobuflisted buftype=nofile bufhidden=wipe noswapfile | 0read ! node' expand('%')
endfunction
command! NodeTestCurrent execute s:node_test_current()
nmap <leader>tn :NodeTestCurrent<CR>
```

https://stackoverflow.com/a/31935734
