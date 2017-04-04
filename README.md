// Instructions needing to be added: (3)	A function for comparing two integers. The function CompNumbers is to be defined with two integer reference parameters, and returns true if the numbers are equal, false otherwise//

#include "stdafx.h"
#include <iostream>
using namespace std;

int main()
{
	int MaxNumbers = 0, number, AddNumbers = 0, MulNumbers = 1;
	int count = 0;
	float average;

	while (1)
	{
		cout << "Enter a number(-1 to quit): "; cin >> number;

		if (number == -1)
			break;  

		else if (number<1 || number>100)
		{
			cout << "\nOut of range.Enter between 1-100.\n"; continue;
		} 
			


		MaxNumbers = (number>MaxNumbers) ? number : MaxNumbers; 
													   
													
		AddNumbers += number;
		MulNumbers *= number;
		count++;
	}


	average = float(AddNumbers);

	cout << "\nYou entered " << count << " numbers." << endl
		<< "The Sum is : " << average << endl
		<< "Max number is : " << MaxNumbers << endl
		<< "Quotient is : " << MulNumbers << endl;

	return 0;
}
