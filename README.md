# Guess-the-number
#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    std::srand(std::time(nullptr));
    
    int secret_number = std::rand() % 100 + 1;
    int user_guess = 0;
    int attempts = 0;

    std::cout << "=== GAME: GUESS THE NUMBER ===" << std::endl;
    std::cout << "I have thought of a number between 1 and 100. Try to guess it!" << std::endl;

    while (user_guess != secret_number) {
        std::cout << "Enter your guess: ";
        std::cin >> user_guess;
        attempts++;

        if (user_guess > secret_number) {
            std::cout << "Too high! Try again." << std::endl;
        } else if (user_guess < secret_number) {
            std::cout << "Too low! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed it in " << attempts << " attempts!" << std::endl;
        }
    }

    return 0;
}

## Author
Hiro Miata