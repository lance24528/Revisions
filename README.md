# Revisions

#include <stdio.h>
#include <iostream>
using namespace std;

float studentAverage;
int studentSum;
float total;

int main() {
	int StudentMarks[5];
	cout << "Enter your grades from 0-100" << endl;
	for (int i = 0; i < 5; i++) {

		cin >> StudentMarks[i];

	}
	cout << endl;
	for (int i = 0; i < 5; i++) {
		//cout << StudentMarks[i] << endl;
		total = total + StudentMarks[i];
	}
	studentAverage = total / 5;
	studentSum = int(total);
	cout << "The student's Average is:" << studentAverage << endl;
	cout << "The student's grade sum is:" << studentSum;
	return 0;
}
                                                     //
#include <stdio.h>
#include <iostream>
using namespace std;

float studentAverage;
int studentSum;
float total;

int main()
{
	int StudentMarks[5];
	cout << "Enter your grades from 0-100" << endl;
	for (int i = 0; i < 5; i++) {
		try
		{
			cin >> StudentMarks[i];
			if ((StudentMarks[i] <= 100) && (StudentMarks[i] > 0))
				cout << "Subject " << i + 1 << " entered: " << StudentMarks[i] << endl;


			else throw StudentMarks[i];
		}
		catch (int err){
			cout << "\n!INVALID! Please enter from 0 to 100" << endl;
			cout << endl;
			i--;
		}
	}
	cout << endl;
	for (int i = 0; i < 5; i++) {
		//cout << StudentMarks[i] << endl;
		total = total + StudentMarks[i];
	}
	studentAverage = total / 5;
	studentSum = int(total);
	cout << "The student's Average is:" << studentAverage << endl;
	cout << "The student's grade sum is:" << studentSum;
	return 0;
}
                                                     //
#include <iostream>
using namespace std;
int main()
{
	int userAge;
	string response;

	cout << "Enter your age above 10." << endl;
	cin >> userAge;
	try {
		if ((userAge <= 12) && (userAge >= 10)){
			response = "Preteen age";
		}
		else if ((userAge <= 19) && (userAge >= 13)){
			response = "Teen-age";
		}
		else if ((userAge <= 29) && (userAge >= 20)){
			response = "Twenties";
		}
		else if ((userAge <= 39) && (userAge >= 30)){
			response = "Thirties";
		}
		else if ((userAge <= 49) && (userAge >= 40)){
			response = "Forties";
		}
		else if ((userAge <= 59) && (userAge >= 50)){
			response = "Fifties";
		}
		else if (userAge >= 60){
			response = "Sixties or above";
		}
		else throw userAge;
	}
	catch (int err){
		cout << "Invalid! Enter a correct number! ";
	}
	cout << response;
	return 0;
}
