#include<stdio.h>

void decimaltohexadecimal(int decimal){
    char hex[100];
    int i = 0;
    
    if (decimal == 0){
        printf("hexadecimal  :");
        return;
        
    }
    while(decimal != 0){
        int remainder = decimal % 16;
        
        if (remainder < 10){
            hex[i] = remainder + '0';
        }else{
            hex[i] = remainder - 10 + 'A';
        }
        i++;
        decimal /= 16;
        
    }
    printf("hexadecimal :");
    for(int j = i-1;j>=0;j--){
        printf("%c",hex[j]);
    }
    printf("\n");
}
int main(){
    int decimal;
    
    printf("enter a decimal number : ");
    scanf("%d",&decimal);
    
    decimaltohexadecimal(decimal);
    
    return 0;
}
