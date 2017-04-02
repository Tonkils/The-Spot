# The-Spot
/*Enter n (to print primes from 3 to n): 3 is a prime number.
5 is a prime number.
7 is a prime number.
11 is a prime number.
*/
#include<iostream>
#include <cstdlib>

using namespace std;

int main()

{
	int N;
	//N represents the number of primes you would like to be printed
	int prime = 3;
	//prime represents the number being tested for whether or not it is prime
	int prime_divisor;
	//prime_divisor represents the number that will test if the number is prime
	int next;
	//This will hold the value of the upcoming prime
	int count = 0;
	//Count will keep track of how many values have been printed
	int displayCount = 0;
	const int displayMax = 4;
	cout << "Enter a number, and I will display all of the" << endl;
	cout << "prime numbers from 0 to that number: ";
	cin >> N;

	while (count != N && prime < N){
		prime_divisor = 2;
		if (prime%2 == 0){
			prime++;
		}
		else
		{
		while((prime%prime_divisor) != 0){
			prime_divisor++;
			if (prime_divisor == prime){
				count++;
				displayCount++;
				next = prime;
				cout << next << "\t";
				if (displayCount%displayMax == 0)
					cout << endl;
			}
		}
			prime++;
		}
	}
	return 0;
}
