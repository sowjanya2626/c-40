# c-40
ceaser cipher codes
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
	char text[100];
	int key,i;
	printf("enter the text:");
	fgets(text,sizeof(text),stdin);
	printf("enter the shift value:");
	scanf("%d", &key);
	for(i=0; text[i]!= '\0'; i++){
		char ch=text[i];
		if(isalpha(ch)){
			char base=isupper(ch)?'A':'a';
			text[i]=(ch-base+key)%26+base;
		}
	}
	printf("cipher code:%s",text);
	return 0;
}                                                                                                                                                                                                                
