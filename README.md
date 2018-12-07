//# C-pp-screen-update


#include "pch.h"
#include <windows.h>
#include <iostream>
#include <ctime>
using namespace std;
int main()
{
	

	const int height = 20;
	const int width = 30;


	char block = '#';
	char space = ' ';
	char grid[height][width];



	//  assing
	for (int i = 0; i < height; i++) {
		for (int j = 0; j < width; j++) {

			grid[i][j] = block;


		}

	}
	while (true) {
	srand((int)time(0));
	int rh = (rand() % height) + 0;
	int rw = (rand() % width) + 0;
	grid[rh][rw] = space;
	grid[rw][rh] = space;



	//   DRAW
	for (int i = 0; i < height; i++) {
		for (int j = 0; j < width; j++) {

			

			//WriteConsoleOutput(1,  grid[i][j] , 3, 4, 5);

			cout << grid[i][j];

		}
		cout << endl;
	}

	system("cls");
}


	system("pause");
}
