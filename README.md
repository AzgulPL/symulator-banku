
To mój pierwszy progam w c++
(Prosty sumulator banku)

#include <iostream>
#include <windows.h>
#include <stdio.h>
#include <cstdlib>
#include <conio.h>
using namespace std;
char wybor;
string PIN;
int konto=700, wyplata=0, wplata=0;

int main()
{
    cout << "Witaj w naszym banku" << endl;
    cout<<"Podaj PIN:";
    cin>>PIN;

    if(PIN=="1729")
    {
        cout<<"Poprawny PIN"<<endl;
        cout<<"Stan twojego konta to "<<konto<<" zlotych"<<endl;
        Sleep(1000);
        cout<<"1:Wyplac pieniadze"<<endl;
        cout<<"2:Wplac pieniadze"<<endl;
        cout<<"3:Wyjscie"<<endl;
while(wybor!=3)
{

wybor=getch();
        switch(wybor)
        {
            case '1':
                {
                    cout<<"Ile chcesz wyplacic?"<<endl;
                    cin>>wyplata;
                    cout<<"Wyplacono "<<wyplata<<endl;
                    cout<<"Na koncie zostalo "<<konto-wyplata;
                    break;
                }
            case '2':
                {
                    cout<<"Ile chcesz wplacic?"<<endl;
                    cin>>wplata;
                    cout<<"Wplacono "<<wplata<<endl;
                    Sleep(1000);
                    cout<<"Na koncie jest "<<konto+wplata<<endl;
                }
            case '3':
                {
                    exit(0);
                }

        }
}
    }
    else
    {
        cout<<"Pin jest niepoprawny"<<endl;
        Sleep(1000);
        cout<<"Ze wzgledow bezpieczenstwa konto zostalo"
        " zablokowane"<<endl;


    }
    return 0;
}


