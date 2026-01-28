#include <stdio.h>
<br>
#include <stdlib.h>  
<br>
#include <time.h>    
<br>
int main() {
<br>
	int player;
	<br>
	/* 0-->snake
	   1-->water
	   2-->gun*/
	   <br>
	printf("enter 0 for snake ,1 for water ,2 for gun:");
	<br>
	scanf("%d",&player);
	<br>
	if(player < 0 || player > 2){
    	printf("Invalid input\n");
    	return 1;
	}
	<br>
    srand(time(0));  
	<br>
    int computer = rand() % 3; 
	<br>
    printf("Random number: %d\n", computer);
	<br>
    if(player == computer)
	<br>
    	printf("Draw");
		<br>
	else if((player == 0 && computer == 1) ||
        (player == 1 && computer == 2) ||
        (player == 2 && computer == 0))
    	printf("Player wins");
	else
    printf("Computer wins");
    return 0;
}


