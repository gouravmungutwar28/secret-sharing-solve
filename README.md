Secret Sharing Solution
This repository contains a C++ solution for a secret sharing problem. The program can reconstruct a secret from a set of shares and identify corrupt shares if they exist. It is designed to handle different JSON input formats and number bases.

Prerequisites
You need a C++ compiler (like g++) and the nlohmann/json header-only library.

File Structure
secret_sharing.cpp: The main C++ source code file.

json.hpp: The header file for the nlohmann/json library.

test_case_1.json: A sample input file with a corrupt share.

test_case_2.json: A sample input file with large numbers in different bases.

Compilation
Place secret_sharing.cpp and json.hpp in the same directory. Then, compile the code using the following command in your terminal:

g++ -std=c++17 -o secret_sharing secret_sharing.cpp

How to Run
The program reads a JSON input from standard input (stdin). You can provide a test case using input redirection.

To run Test Case 1:
./secret_sharing < test_case_1.json

Expected Output:

the secret is:120
the wrong secret is:150
participant 5 is corrupt

To run Test Case 2:
./secret_sharing < test_case_2.json

Expected Output:

The reconstructed secret is: -6290016743746469796
