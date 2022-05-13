# Snake-Game-using-C-
Snake game is one of the most famous and oldest games that could be played on a device. I thought it would be a good fit for my first beginner friendly project.

# 1.INTRODUCTION 

# 1.1 What is Snake Game? 

➤Snake is the common name for a video game concept where the player  maneuvers a line(snake) which grows in length, with the line itself being a  primary obstacle. The concept originated in the 1976 two-player arcade game Blockade from Gremlin Industries, and the ease of implementing Snake has led  to many variations. (some of which have the word snake or worm in the title) 
It being one of the most famous games in the history of humans has a demand  for being simple and playable. The objective of this game is to eat as many  fruits as possible to increase your score and avoid the in game obstacles plus  the snake itself as touching either of them will lead to the game being over. 
Catching a fruit will give your score 10 increments. If your score is above 50  and below 100 you’ll achieve the title of “BRONZE”. Similarly if your score is  between 100 and 150 you’ll achieve “SILVER” and finally if you manage to  score more than 150 you’ll achieve the title of “SNAKE MASTER”. 
# 1.2 What’s the twist ? 
➤The twist in our snake game project is that it’s different from other  versions as we have a special feature we have implemented in this  game in which every time you eat a fruit (F), the head of the snake  gets teleported through a portal denoted by purple ‘?’ and the rest of  the body follows it. This leads to a more interesting game and one  has to be careful on how to approach the fruit as there are more  chances of colliding with the obstacle and snake itself after this  special trait.
# ➤Approach
# 2.1 How was the idea originated ? 
As I have an interest in gaming I wanted to  implement something different in this, and using the concepts  of OOPS such as inheritance, polymorphism and classes I  could make my interest into this project. I chose a simple  game and added our own idea in it of teleportation so the  game is more interesting and original. 
# 2.2 Prototype development 
The prototype development started with keeping these things  in mind: 
● The snake is represented with a 0(zero) symbol. 
● The fruit is represented with an F symbol. 
● The snake can move in any direction according to the user with the help  of the keyboard (W, A, S, D keys). 
● When the snake eats a fruit the score will increase by 10 points. ● The fruit will generate automatically within the boundaries. 
● Whenever the snake will touch itself or obstacle the game is over. 
First the body of snake was implemented using a array so it’s  easier to increase snake’s length
Snake(){ //Constructor 
 size = 1; // default size 
 cell[0] = new Point(20,20); // 20,20 is default position  for( int i=1; i<MAXSNAKESIZE; i++){ 
 cell[i] = NULL; 
 } 
 void AddCell(int x, int y){ //increases size of snake by 1 on eating  fruit 
 cell[size++] = new Point(x,y); 
 } 
Next movement of snake was implemented 

if(kbhit()){ //keeps track of last pressed key 
 op = getch(); 
 } 
 switch(op){ 
 case 'w': 
 case 'W': 
 snake.TurnUp(); 
 break; 
  
 case 's': 
 case 'S': 
 snake.TurnDown(); 
 break; 
  
 case 'a': 
 case 'A': 
 snake.TurnLeft(); 
 break; 
  
 case 'd': 
 case 'D': 
 snake.TurnRight();
 break; 
 } 
 snake.Move(); 
Next interaction of the snake with objects such as fruit or  obstacles was implemented. 
if( SelfCollision() ) 
 state = 0;  
 if(Collision()) 
 state =0; 
  
 // Collision with fruit 
  
 if( fruit.GetX() == cell[0]->GetX() && fruit.GetY() == cell[0]- >GetY()){ 
 AddCell(0,0); 
 score=score+10; 
 cell[0] = new Point(fruit2.GetX(),fruit2.GetY());
 fruit.SetPoint(rand()%MAXFRAMEX, rand()%MAXFRAMEY);
 fruit2.SetPoint(rand()%MAXFRAMEX, rand()%MAXFRAMEY);
 Obstacle.SetPoint(rand()%MAXFRAMEX, rand()%MAXFRAMEY); 
 Obstacle.SetPoint(5,6); 
 } 
This was the basic prototype of the game. The other functions  will be seen in the main function. 
# 3. SOFTWARE TOOLS USED
# 3.1 C++ 
C++ is a general-purpose programming language created by Bjarne Stroustrup as an  extension of the C programming language, or "C with Classes". The language has  expanded significantly over time, and modern C++ now has object-oriented, generic,  and functional features in addition to facilities for low-level memory manipulation. It is almost always implemented as a compiled language, and many vendors provide C++  compilers, including the Free Software Foundation, LLVM, Microsoft, Intel, Oracle,  and IBM, so it is available on many platforms.
Inbuilt header files used: 
<vector> 
<iostream> 
<conio.h 
<time.h> 
<dos.h> 
Imported header file: 
<color.hpp> 
Inbuilt functions used: 
SetconsoleCursorPoistion() 
rand() 
system(“cls”) 
getch() 
Sleep() 
setcursor() 
kbhit() 
Classes and functions made: 
Classes: 
Snake 
Point
Functions: 
gotoxy() 
SetPoint() 
GetX(),GetY() 
MoveUp(),MoveDown(),MoveLeft(),MoveRight() Draw(),DrawFruit,DrawObstacle 
Erase() 
CopyPos() 
IsEqual() 
AddCell() 
Move() 
SelfCollision() 
Collision()
# 4.The outputs and screenshots can be found in snakegame.pdf
