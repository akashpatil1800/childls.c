# childls.c
Child process does computation of running ls command
 
#include<stdio.h>
 
#include<stdlib.h>
 
#include<unistd.h>
 
int main()
 
{
 
//int status;
 
char *args[2];
 
args[0] = "/bin/ls";
 
args[1] = NULL;
 
if (fork() ==0)
 
execv(args[0],args);
 
//else
 
//wait( &status);
 
return 0;
 
}
 
 
