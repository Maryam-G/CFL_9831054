#include <stdio.h>

char t[3][5];
int cnt=1;

int finish(){
    if(((t[0][0]==t[0][2])&&(t[0][2]==t[0][4])&&(t[0][4]!=' '))||((t[1][0]==t[1][2])&&(t[1][2]==t[1][4])&&(t[1][4]!=' '))||((t[2][0]==t[2][2])&&(t[2][2]==t[2][4])&&(t[2][4]!=' '))||((t[0][0]==t[1][0])&&(t[1][0]==t[2][0])&&(t[2][0]!=' '))||((t[0][2]==t[1][2])&&(t[1][2]==t[2][2])&&(t[2][2]!=' '))||((t[0][4]==t[1][4])&&(t[1][4]==t[2][4])&&(t[2][4]!=' '))||((t[0][0]==t[1][2])&&(t[1][2]==t[2][4])&&(t[2][4]!=' '))||((t[2][0]==t[1][2])&&(t[1][2]==t[0][4])&&(t[0][4]!=' '))){
        return 0;
    }else{
        if(cnt<9){
            return 1;
        }else{
            return 2;
        }
    }
}

int main(){
    char first_player,second_player,p;
    int n;
    t[0][1]=t[0][3]=t[1][1]=t[1][3]=t[2][1]=t[2][3]='|';
    t[0][0]=t[0][2]=t[0][4]=t[1][0]=t[1][2]=t[1][4]=t[2][0]=t[2][2]=t[2][4]=' ';
    printf("please enter first player(X or O):\n");
    scanf("%c",&first_player);
    if((first_player!='X')&&(first_player!='O')){
        printf("your input is invalid\n");
        return 0;
    }
    if(first_player=='X'){
        second_player='O';
    }else{
        second_player='X';
    }
	return 0;
}