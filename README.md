# FileReader

#include <iostream>
#include "wordcounter.cpp"
#include <string>
#include <fstream>

using namespace std;

int main()
{

//Give names to the input and output commands of the program

ifstream input;
ofstream output;

string filename;
string temp = "";
WordCounter wordcount1;
char ch;

cout << "Please enter a file name" << endl;
cin >> filename;


// Give command to program to open a text file and interate through it counting the words and unique characters


input.open(filename.c_str());
while(input.get(ch))
	{
		if(ch == ' ')
		{
			wordcount1.Addword(temp);
			temp = "";
		}
		else 
		{
			temp +=ch;
		}
}

//Close the output of the file and print the results


output.close();
cout << "test";
wordcount1.Printsummary();
return 0;
}
