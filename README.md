#include <stdio.h>
#include <stdlib.h>  
#include <time.h>    

int main() {
	int player;
	/* 0-->snake
	   1-->water
	   2-->gun*/
	printf("enter 0 for snake ,1 for water ,2 for gun:");
	scanf("%d",&player);
	if(player < 0 || player > 2){
    	printf("Invalid input\n");
    	return 1;
	}
    srand(time(0));         
    int computer = rand() % 3;   
    printf("Random number: %d\n", computer);
    if(player == computer)
    	printf("Draw");
	else if((player == 0 && computer == 1) ||
        (player == 1 && computer == 2) ||
        (player == 2 && computer == 0))
    	printf("Player wins");
	else
    printf("Computer wins");
    return 0;
}


