<div align="center">

## move a char across the screen using the arrow keys \(good for making games\)


</div>

### Description

This program (well commented) will show you the use of the arrow keys by movng a charachter across the screen. *Note* this program does not have limits so try to stay withing the screen limits. Email me if you''dlike to see boundries put on it!! and dont' forget to vote!!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[theMayor](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/themayor.md)
**Level**          |Beginner
**User Rating**    |4.2 (21 globes from 5 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Games](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/games__3-13.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/themayor-move-a-char-across-the-screen-using-the-arrow-keys-good-for-making-games__3-2109/archive/master.zip)





### Source Code

```
#include <iostream.h>
#include <stdlib.h>
#include <conio.h>
int main()
{
 int top=40;// keeps up with the top coordinate
 int side=12;// keeps up with the side coordinate
 char input;//will detect arrow keys
 char kc;//will get the players charachter
 cout << "Please Enter a Charachter!\n";
 kc=getche();// gets the user charachter
 cout << flush;
 cout << "\nNow Just press the arrow keys to move the " << kc << " across the Screen!!\n\n";
 cout << "Press any arrowkey to continue...\n";
 getch();
 system ("cls");//clears the screen
 _setcursortype(_NOCURSOR);// removes the cursor from the screen!
 gotoxy(20,24);cout << "Press The Arrow Keys to move the " << kc << " Around!!\n"<<flush;
 gotoxy(37,25);cout << "Esc to Quit\n";
 gotoxy(40,12);cout << kc <<flush;
 while (input!=27)// while the user does NOT hit escape
 {
 input=getch();//get user input
 if (input==0)// if a special key is pressed... in this case if an arrow key is pressed
 {
  input=getch();//call getch() again to get the next value
   if (input=='K')// if it's the left arrow key
   {
   gotoxy(top,side);cout << " "<< flush;// all this does is put a space where the charachter WAS
   top--;// subtract from the top coordinate
   gotoxy(top,side);cout << kc << flush; // prints the charachter at the new location
   }
  else if (input=='P')// if the down arrow key is pressed
  {
   gotoxy(top,side);cout << " " << flush;
   side++;// adds one to the top coordinate
   gotoxy (top,side);cout << kc << flush;
  }
  else if (input=='M')// if the right arrow key is pressed
  {
   gotoxy(top,side);cout << " " << flush;
   top++; //adds one to the top coordinate
   gotoxy(top,side);cout<< kc << flush;
  }
  else if (input=='H')// if the up arrow key is pressed
  {
  gotoxy(top,side);cout << " " << endl;
  side--;
  gotoxy(top,side);cout << kc << flush;
  }
 }
 }
 return 0;
}
```

