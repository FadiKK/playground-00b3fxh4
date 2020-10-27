# Welcome!

This C++ template lets you get started quickly with a simple one-page playground.

```C++ runnable
#include <iostream>
#include <vector>
#include <string>

int main() 
{
  string user;
  char selection;
  vector<string> users;
  do
  {
    std::cout << "--------------------------------------------" << std::endl;

    std::cout << "a - add a user" << std::endl;
    std::cout << "d - display all users" << std::endl;
    std::cout << "q - quit" << std::endl;

    std::cout << "please pick a selection";
    std::cin >> selection;

    if (selection == 'a' or selection == 'A')
    {
      std::cout << "please type the users name";
      std::cin >> user;

      users.push_back(user);

      std::cout << "the user was succesfully added" << std::endl;
    }

    else if (selection == 'd' or selection == 'D')
    {
      std::cout << "here are all of the users: " << std::endl;

      for (auto use: *users.data())
      {
        std::cout << use << std::endl;
      }
    }

    else if (selection == 'q' or selection == 'Q')
    {
      std::cout << "goodbye" << std::endl;
    }

    else
      std::cout << "hmmmm, I do not recognize that command" << std::endl;

  } while(selection != 'q' and selection != 'Q')
  
  return 0;
}
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced C++ template](https://tech.io/select-repo/598)
