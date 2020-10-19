#include <iostream>
#include <string>
using namespace std;
 
 
void draw(char*);     //declaration of functions
int win(char*);
 
int main()
{
    int insert;
    const int N = 9;
    int game = 0;
    char box[N] = { '1','2','3','4','5','6','7','8','9' };
 
 
 
    for (int i = 0; i < 9; i++)
    {
        cout << box[i];
        if (i == 2 || i == 5 || i == 8)
        {
            cout << "\n";
        }
        else
        {
            cout << "\t";
        }
 
    }
    cout << "\n";
 
 
 
 
    for (int j = 1; j > 0 ; j++)
    {
        game = win(box);
        if (game == 0)
        {
            
                if (j % 2 == 1)
                {
                    cout << "player 1, enter the box number: ";
                    cin >> insert;
                    insert = insert - 1;
                    box[insert] = 'X';
                    draw(box);
                }
 
                if (j % 2 == 0)
                {
                    cout << "player 2, enter the box number: ";
                    cin >> insert;
                    insert = insert - 1;
                    box[insert] = 'O';
                    draw(box);
 
                }
        }
        else if (game == 1)
        {
            cout <<"The game has ended! Player one has won! \n\n";
            break;
        }
        else if (game == 2)
        {
            cout << "The game has ended! Player two has won! \n\n";
            break;
        }
        else if (game == 3)
        {
            cout << "The game has ended! Player three has won! \n\n";
            break;
        }
    }
 
}
 
 
 
int win(char* boxx)
{
    
    if (boxx[0] == boxx[2] && boxx[0] == boxx[1])
    {
        if (boxx[1] == 'X')
        {
            return 1;
        }
        else
        {
 
            return 2;
        }
    }
    else if (boxx[4] == boxx[3] && boxx[3] == boxx[5])
    {
        if (boxx[3] == 'X')
        {
            return 1;
        }
        else
        {
            return 2;
        }
    }
    else if (boxx[6] == boxx[7] && boxx[8] == boxx[6])
    {
        if (boxx[6] == 'X')
        {
            return 1;
        }
        else
        {
            return 2;
        }
 
    }
    else if (boxx[6] == boxx[0] && boxx[3] == boxx[6])
    {
        if (boxx[6] == 'X')
        {
            return 1;
        }
        else
        {
            return 2;
        }
 
    }
    else if (boxx[1] == boxx[7] && boxx[4] == boxx[1])
    {
        if (boxx[1] == 'X')
        {
            return 1;
        }
        else
        {
            return 2;
        }
 
    }
    else if (boxx[2] == boxx[5] && boxx[8] == boxx[2])
    {
        if (boxx[2] == 'X')
        {
            return 1;
        }
        else
        {
            return 2;
        }
 
    }
    else if (boxx[0] == boxx[4] && boxx[8] == boxx[0])
    {
        if (boxx[0] == 'X')
        {
            return 1;
        }
        else
        {
            return 2;
        }
    }
    else if (boxx[6] == boxx[4] && boxx[2] == boxx[6])
    {
        if (boxx[6] == 'X')
        {
            return 1;
        }
        else
        {
            return 2;
        }
 
    }
    
    else if (boxx [0] != '1' && boxx[1] != '2'&& boxx[2] != '3'&& boxx[3] != '4'&& boxx[4] != '5'&& boxx[5] != '6'&& boxx[6] != '7'&& boxx[7] != '8'&&
             boxx[8] != '9')
    {
        return 3;
    }
    
    else
    {
    return 0;
    }
}
 
void draw(char* boxx)
{
    for (int i = 0; i < 9; i++)
    {
        cout << boxx[i];
        if (i == 2 || i == 5 || i == 8)
        {
            cout << "\n";
        }
        else
        {
            cout << "\t";
        }
 
    }
    /***************************
    * You can use This code to *
    * make it look nicer       *
    ***************************/
    /*
      system("cls");
    cout << "   |   |   " << endl;
    cout << " " << boxx[0] << " | " << boxx[1] << " | " << boxx[2] << endl;
    cout << "___|___|___" << endl;
    cout << "   |   |   " << endl;
    cout << " " << boxx[3] << " | " << boxx[4] << " | " << boxx[5] << endl;
    cout << "___|___|___" << endl;
    cout << "   |   |   " << endl;
    cout << " " << boxx[6] << " | " << boxx[7] << " | " << boxx[8] << endl;
    cout << "   |   |   " << endl;
    cout << "\n";
    */
    cout << "\n";
}
