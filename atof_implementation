#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#define SIZE 250
float myAtof(char *string, char *error);

int main()
{
    char string[SIZE];            // Array declaration.
    float fnum1;
    char errorState=0;

    printf("Enter a number:\n");
    gets(string);

    fnum1=myAtof(string,&errorState);

    if (errorState==0){
        printf("Your number is: %.2f \n", fnum1);
    }else if (errorState==1){
        printf("Error has been occurred due to inappropriate input!\n");
    }

    return 0;
}

float myAtof(char* string, char* error){      

    float value = 0;
    int check = 1;
    int whereispoint;
    float afterpointvalue = 0;

    for (int i = 0; string[i] !='\0'; i++)
    {
        if (string[i] >= 48 && string[i] <= 57)
        {
            if(check) {
                    value = value * 10 + (string[i]-48);
            }
            else{
                    value += ((string[i]-48) * pow(10,whereispoint-i));
            }
        }
        else if (string[i] == 46 ) 
        {
            check = 0;
            whereispoint = i;
        }
        else{
            *error = 1;
            return 0;
        }
    
    }
    return value;

}
