# CP-THEORY-
#include <iostream>
#include<conio.h>
using namespace std;
// Function to convert Temperature in Celsius to Temperature in Fahrenheit
double CelsiusToFahrenheit(double celsius) {
	return (celsius * 9 / 5) + 32;
}
// Function to convert Temperature in Fahrenheit to Temperature in Celsius
double FahrenheitToCelsius(double fahrenheit) {
	return (fahrenheit - 32) * 5 / 9;
}
// Function to convert Temperature in Celsius to Temperature in Kelvin
double CelsiusToKelvin(double celsius) {
	return celsius + 273.15;
}
// Function to convert Temperature in Kelvin to Temperature in Celsius
double KelvinToCelsius(double kelvin) {
	return kelvin - 273.15;
}
// Function to convert Temperature in Fahrenheit to Temperature in Kelvin
double FahrenheitToKelvin(double fahrenheit) {
	return (fahrenheit + 459.67) * 5 / 9;
}
// Function to convert Temperature in Kelvin to Temperature in Fahrenheit
double KelvinToFahrenheit(double kelvin) {
	return kelvin * 9 / 5 - 459.67;
}
int main() {
	// Choice is for switch case
	char choice;
	//double is because input temperature can be in decimal
	double temperature;
	cout << "Covert Temperatures:\n";
	cout << "--------------------\n";
	while (true) {
		// Enter the choice for what you are going to convert your temperature in C, F and K
		cout << "Choose the conversion:\n";
		cout << "a) Celsius to Fahrenheit\n";
		cout << "b) Fahrenheit to Celsius\n";
		cout << "c) Celsius to Kelvin\n";
		cout << "d) Kelvin to Celsius\n";
		cout << "e) Fahrenheit to Kelvin\n";
		cout << "f) Kelvin to Fahrenheit\n";
		cout << "Enter your choice (a, b, c, d, e, or f): ";
		cin >> choice;
		// Switch case
		switch (choice) {
		case 'a':
			cout << "Enter the Temperature in Celcius:\t";
			cin >> temperature;
			cout << temperature << " Celsius is equal to " <<
				CelsiusToFahrenheit(temperature) << " Fahrenheit\n";
			break;

		case 'b':
			cout << "Enter the Temperature in Fahrenheit:\t";
			cin >> temperature;
			cout << temperature << " Fahrenheit is equal to " <<
				FahrenheitToCelsius(temperature) << " Celsius\n";
			break;
		case 'c':
			cout << "Enter the Temperature in Celcius:\t";
			cin >> temperature;
			cout << temperature << " Celsius is equal to " <<
				CelsiusToKelvin(temperature) << " Kelvin\n";
			break;
		case 'd':
			cout << "Enter the Temperature in Kelvin:\t";
			cin >> temperature;
			cout << temperature << " Kelvin is equal to " <<
				KelvinToCelsius(temperature) << " Celsius\n";
			break;
		case 'e':
			cout << "Enter the Temperature in Fahrenheit:\t";
			cin >> temperature;
			cout << temperature << " Fahrenheit is equal to " <<
				FahrenheitToKelvin(temperature) << " Kelvin\n";
			break;
		case 'f':
			cout << "Enter the Temperature in Kelvin:\t";
			cin >> temperature;
			cout << temperature << " Kelvin is equal to " <<
				KelvinToFahrenheit(temperature) << " Fahrenheit\n";
			break;
		default:
			cout << "Invalid choice\n";
		}
		// Chose yes if you are going to perform another conversion
		string ans;
		cout << "Do you want to perform another conversion? (yes/no): ";
		cin >> ans;
		if (ans != "yes") {
			break;
		}
	}
	cout << "\n_______________________________________________________________________________________________________________________\n";
	return 0;
}
