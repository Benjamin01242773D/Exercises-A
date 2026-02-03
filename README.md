#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    // Seed the random number generator
    srand(time(0));
    
    // Generate a secret number between 1 and 100
    int secretNumber = rand() % 100 + 1;
    int playerGuess = 0;

    cout << "Welcome to the Number Guessing Game!" << endl;

    while (true) {
        cout << "Enter your guess (1-100): ";
        cin >> playerGuess;

        if (playerGuess == secretNumber) {
            cout << "Congratulations! You guessed the secret number!" << endl;
            break;
        } else if (playerGuess > secretNumber) {
            cout << "Too High! Try again." << endl;
        } else {
            cout << "Too Low! Try again." << endl;
        }
    }

    return 0;
}
