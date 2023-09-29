#include <iostream>
#include <ctime>
using namespace std;

int main()
{
   int guess ,random; 
    int numofattempts=0;
    
    srand(time(0));
    random = (rand()%100)+1;
       cout<<"I am thinking of a number between 1 to 100 "<<endl;
    cout<<"can you guess what it is?"<<endl;
     
    do { 
        
     
    cout<<"enter your guess: ";
    cin>>guess;
        if (guess>100|| guess<0)
        cout<<"please choose a number between 0 to 100"<<endl;
       else if (guess==random)
        cout<<"Congrats! Right guess after "<<numofattempts<<" guesses"<<endl;
        else if(guess<random){
        cout<<"You enterd a lower number.Try again!"<<endl;
        numofattempts++;}
         else if(guess>random){
         cout<<"You enterd a higher number.Try again!"<<endl;
         numofattempts++;}
        
    }while(guess!=random);
    
    
    return 0;
}