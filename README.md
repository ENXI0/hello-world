//today's HW
#ifndef THERMOSTAT_H
#define THERMOSTAT_H

#include<vector>
using std::vector;
#include<string>
using std::string;

struct Thermostat {
	std::string thermostat = "Off";
	int high = 30;
	int low = 15;
	int hy = 2;

	Thermostat() = default;
	Thermostat(int h, int l) : high(h), low(l) {};
	Thermostat(int h, int l, int y) : high(h), low(l), hy(y) {};
	Thermostat(string s);

	string GetStateAfterReading(int);
};

string ThermostatToString(const Thermostat&);

void split(const string&, vector<string>&, char);

#endif
