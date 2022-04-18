# Vim

## Links

- [7 Tips](https://www.freecodecamp.org/news/7-vim-tips-that-changed-my-life/)
- [Python](https://www.vimfromscratch.com/articles/vim-for-python/)
- [IPython](https://pythonawesome.com/seamlessly-run-python-code-from-vim-in-ipython/#installation)

## Reminders


> C# code
 ```cs 
 void Some(){
   for(int i=0;i<10;i++){
     Console.WriteLine($"index {i}")
   }
 	
 } 
```

## Getting search in between <div>


```vim
::/\(hidden;">\)\@<=.\{-}\(\<div\)\@=
```

## Questions

- Top plugins
- Vim multiple tabs
- Tree view 
- Intelisense

## Command line syntaxis
 
 - `:!` - execute in command line
 - `%` - current file name
 - `:pu=strftime('%c')` gives date 08/01/2022 8:36:40 pm

## Set
 - `:set  number` - turn on numbers
 - `:set  nonumber` - turn off line numbers
 - `:set hlsearch` - turn on highlight on search
 - `:noh` - turn off highlight on search

## Search

 - `/`  search for something
 - `//` previous search
 - `?`  backward search
 - `:set hlsearch` - turn on highlight on search
 - `:noh` - turn off highlight on search

## Substitue

 - `:1,4s/^/#` - Add # on begining of each line from 1 to 4
 - `:s/pattern/replace/g` - find and replace in current line
 - `:%s///replace/g` - replace last search in entire file
 - `%` - serch in entire file
 - `:help :substitute`

### Vimgrep

Super awesome vim search in multiple files


## Concept 

 I think it might be a great idea to completly switch to vim
 I have couple of blind spots with vim. But the general concpt of working full in `Vim` is sort of Idea that I like I mean it is cool.

## Copy pase MS Widnows buffer

<kbd>"</kbd>+<kbd>\*</kbd>+<kbd>y</kbd> - copy

<kbd>"</kbd>+<kbd>\*</kbd>+<kbd>p</kbd> - paste 

<kbd>Ctrl</kbd>+<kbd>Q</kbd> - Visual block mode 

<kbd>Shift</kbd>+<kbd>I</kbd> -  Insert changes in visual block mode

## Navigation

<kbd>Ctrl</kbd>+<kbd>]</kbd> - Move to tag in vim help
<kbd>Ctrl</kbd>+<kbd>O</kbd> - Get to begining
<kbd>Ctrl</kbd>+<kbd>T</kbd> - Get to previous location

## Scrolling

<kbd>Ctrl</kbd>+<kbd>U</kbd> - Scroll up 
<kbd>Ctrl</kbd>+<kbd>D</kbd> - Scroll Down
<kbd>Ctrl</kbd>+<kbd>Y</kbd> - Scroll One Line up 
<kbd>Ctrl</kbd>+<kbd>E</kbd> - Scroll One Line Down

`zz` - Scroll to the screen center
`zt` - Scroll to the Top
`zb` - Scroll to the Bottom

## Plugins


### vim-plug

`~\.vimrc` - file to edit
`:source ~/.vimrc` - To reload source
`:PlugInstall` - to Install new plugins
`:PlugUpdate` - in case of update
`:PlugClean` - remove unlisted plugins


### Vim Tree-View


## Extensions

- See the file hirarchy
- Intellisens
- Documentation
- Vim MarkDown syntaxis formated

## Vimtutor

vim C:\tools\vim\vim82\tutor\tutor


