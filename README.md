# analysis_project

#include <iostream>
#include <string>
#include <fstream>

using namespace std;

int BF_Matching(string text, string pattern){
    
    int n = text.length();
    int m = pattern.length();
    
    for (int i = 0; i < n-m; i++) {
        int j = 0;
        while (j < m && pattern[j] == text[i+j]) {
            j = j + 1;
        }
        if(j == m) return i;
    }
     return -1;
}

    string pattern;
    ifstream myfile("/Users/refaatabououkal/Desktop/pattern.txt");
    if (myfile.is_open())
    {
        getline (myfile,pattern);
      myfile.close();
    }
   cout << pattern << endl;
    
    string text1;
    ifstream File1("/Users/refaatabououkal/Desktop/File1.txt");
    if (File1.is_open())
    {
        getline (File1,text1);
         myfile.close();
    }
    cout << text1 << endl;
       
       
 
   return 0;
}
