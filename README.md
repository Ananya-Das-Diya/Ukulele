//Ukulele Chord Diagram App
#include <iostream>
#include <map>
#include <string>


void displayChordDiagram(const std::string& chord) {

    std::cout << "Chord Diagram for " << chord << ":\n";

    std::cout << "   G\n";
    std::cout << "   |---|\n";
    std::cout << "   | | |\n";
    std::cout << "   |---|\n";
    std::cout << "   | | |\n";
    std::cout << "C  |---|  E\n";
    std::cout << "   | | |\n";
    std::cout << "   |---|\n\n";
}

int main() {
    std::map<std::string, std::string> chordMap;

    chordMap["C"] = "0003";
    chordMap["G"] = "0232";
    chordMap["Am"] = "2000";


    std::cout << "Welcome to the Ukulele Chord Diagram App!\n";


    std::string userChord;
    std::cout << "Enter a ukulele chord name (e.g., C, G, Am): ";
    std::cin >> userChord;

    auto it = chordMap.find(userChord);
    if (it != chordMap.end()) {

        displayChordDiagram(userChord);
    } else {
        std::cout << "Chord not found. Please enter a valid ukulele chord.\n";
    }

    return 0;
}
