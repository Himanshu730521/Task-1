#include <iostream>
#include <cstdlib>   // for rand() and srand()
#include <ctime>     // for time()

using namespace std;

int main() {
    srand(static_cast<unsigned int>(time(0)));  // seed the random number generator
    
    int secretNumber = rand() % 100 + 1;  //  we have to generate a random number between 1 and 100
    int guess;
    
    cout << "Welcome to the Number Guessing Game!\n";
    
    do {
        cout << "Guess the number (between 1 and 100): ";
        cin >> guess;
        
        if (guess < secretNumber) {
            cout << "Too low! Try again.\n";
        } else if (guess > secretNumber) {
            cout << "Too high! Try again.\n";
        } else {
            cout << "Congratulations! You guessed the number " << secretNumber << " correctly!\n";
        }
        
    } while (guess != secretNumber);
    
    return 0;
}
