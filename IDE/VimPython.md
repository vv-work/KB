# Vim for python

## Questions

- IPython
- Python-mode

### Inoke code within CLI

Run current file
``vim
:!python %
:w !python
```

Execute one line of code
```vim
:py3 print("Hello")
```
> Hello

## IPython

![GithubLink](https://github.com/hanschen/vim-ipython-cell)
```vim
Plug 'jpalardy/vim-slime', { 'for': 'python' }
Plug 'hanschen/vim-ipython-cell', { 'for': 'python' }
```
#### Status

I was trying to set up this thing. 
But i faced an issue to make it work I need to understand
`vim-slime` and to understand it I need to set output window
`tmux` to display output but it dosen't present in windows 
`cygwin` and to make ubuntu software run I need to get cygwin 

At that point I decided to give it up... 

## Python-mode

