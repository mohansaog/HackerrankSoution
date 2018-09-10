# HackerrankSoution
//Apples and Orange
#include <bits/stdc++.h>

using namespace std;

vector<string> split_string(string);

// Complete the countApplesAndOranges function below.
void countApplesAndOranges(int s, int t, int a, int b, vector<int> apples, vector<int> oranges) {

    int n1=apples.size();
    int count1=0,count2=0;
    int n2=oranges.size();
    for(int i=0;i<n1;i++)
        apples[i]=a+apples[i];
    for(int i=0;i<n2;i++)
        oranges[i]=b+oranges[i];
    for(int i=0;i<n1;i++)
    {
        if(apples[i]>=s && apples[i]<=t)
            count1++;
    }
    for(int i=0;i<n2;i++)
    {
        if(oranges[i]>=s && oranges[i]<=t)
            count2++;
    }
    cout<<count1<<"\n"<<count2<<endl;
}
