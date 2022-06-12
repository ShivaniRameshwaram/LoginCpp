#include<iostream>
#include<fstream>
#include<string>
using namespace std;
bool IsLoggedin()
{
    string username, password, un, pw;
    cout<<"Enter username: "; cin>>username;
    cout<<"Enter password: "; cin>>password;
    ifstream read(username+".txt");
    getline(read,un);
    getline(read,pw);
    if (un==username && pw==password)
    {
        return true;
    }
    else
       return false;
}
int main()
{
    string username,password;
    int choice;
    cout<<"\n1.Register\n2.Login \nEnter your choice: "; cin>>choice;
    if (choice==1)
    {
        cout<<"Select username: "; cin>>username;
        cout<<"Select password: "; cin>>password;
        ofstream file;
        file.open(username+".txt");
        file<<username<<endl<<password;
        file.close();
        main();

    } 
    else if (choice==2)
    {
        bool status=IsLoggedin();
        if (!status)
        {
            cout<<"False Login!";
            system("PAUSE");
            return 0;
        }
        else{
            cout<<"Successfully Logged in!";
            system("PAUSE");
            return 1;
        }
    }
}
