<div align="center">

## Turning Caps On And Off


</div>

### Description

This code just turns caps on and off repeatedly until you end it, it also teaches you how to use a function called, keybd_event which lets you tell windows keys are being pressed, when they aren't, I think you will like it, take a look
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[George Chunni](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/george-chunni.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/george-chunni-turning-caps-on-and-off__3-6976/archive/master.zip)





### Source Code

```
// If you look in winuser.h there is a part where there are LOTS of #defines, find all the VK defines, just replace VK_CAPITAL with the other VK's and you can emulate any other key, if you want to press A-Z, just use those letters....Have Fun
//////////////////////////////////
#include <windows.h>
int main(int argc, char *argv[])
{
HWND hwnd = FindWindow(0, argv[0]); // This finds our program window
ShowWindow(hwnd, SW_HIDE); // This hides our program window
for(;;)
{
keybd_event(VK_CAPITAL, 0, 0, 0); // This turns caps on
keybd_event(VK_CAPITAL, 0, KEYEVENTF_KEYUP, 0); // This is meant to turn caps off
}
 return 0;
}
//////////////////////////////////////////////
```

