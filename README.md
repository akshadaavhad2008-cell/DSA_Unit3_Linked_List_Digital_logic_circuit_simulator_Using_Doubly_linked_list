# DSA_Unit3_Linked_List_Digital_logic_circuit_simulator_Using_Doubly_linked_list
A C++ project that simulates basic digital logic gates, including AND, OR, NOT, NAND, NOR, XOR, and XNOR. It accepts binary inputs and displays outputs to demonstrate the working of digital logic circuits.

code

#include <iostream>
using namespace std;

int main() {
    int choice, A, B, result;

    cout << "=== DIGITAL LOGIC CIRCUIT SIMULATOR ===\n";
    cout << "1. AND Gate\n";
    cout << "2. OR Gate\n";
    cout << "3. NOT Gate\n";
    cout << "4. NAND Gate\n";
    cout << "5. NOR Gate\n";
    cout << "6. XOR Gate\n";
    cout << "7. XNOR Gate\n";

    cout << "Enter your choice: ";
    cin >> choice;

    if (choice == 3) {
        cout << "Enter input A (0 or 1): ";
        cin >> A;

        if (A != 0 && A != 1) {
            cout << "Invalid input!";
            return 0;
        }

        result = !A;
        cout << "Output = " << result;
    }
    else if (choice >= 1 && choice <= 7) {
        cout << "Enter input A (0 or 1): ";
        cin >> A;
        cout << "Enter input B (0 or 1): ";
        cin >> B;

        if ((A != 0 && A != 1) ||
            (B != 0 && B != 1)) {
            cout << "Invalid input!";
            return 0;
        }

        switch (choice) {
            case 1: result = A && B; break;
            case 2: result = A || B; break;
            case 3: result = !A; break;
            case 4: result = !(A && B); break;
            case 5: result = !(A || B); break;
            case 6: result = A ^ B; break;
            case 7: result = !(A ^ B); break;
        }

        cout << "Output = " << result << endl;
    }
    else {
        cout << "Invalid choice!";
    }

    return 0;
}



   
       
       
