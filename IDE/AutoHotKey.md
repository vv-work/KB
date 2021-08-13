# AutoHotKey


## Sleep

```AutoHotKey
^j::


Send, "some"
Sleep 500
send, "input"

return
```

## Kyeys

`^` - `CTRL`
`+` - `Shift`
`#` - `Win`
`!` - `Win`

## Loops
```AutoHotKey
Loop, 3
{
    MsgBox, Iteration number is %A_Index%.  ; A_Index will be 1, 2, then 3
    Sleep, 100
}
```

