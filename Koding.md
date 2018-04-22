# Tugas-Kelompok-Pemrograman-Terstruktur

#include <iostream>
#include <string.h>
#include <bits/stdc++.h>
using namespace std;
    string words, tem;
    bool cek;
    char huruf[10][10]{ {'p','e','s','t','r','i','n','g','f','g'},
		 	{'o','c','b','n','j','m','l','o','u','k'},
                        {'i','k','o','s','o','y','j','k','n','q'},
			{'n','d','a','t','o','l','r','e','g','l'},
	 	        {'t','g','t','n','s','v','b','m','s','o'},
	   		{'e','e','o','c','n','t','l','k','i','b'},
			{'r','t','i','e','n','j','r','b','o','j'},
			{'c','l','a','s','s','k','q','c','e','e'},
			{'r','e','f','e','r','e','n','c','a','c'},
			{'b','b','q','a','r','r','a','y','m','t'}};
 
 
 
 void reverse(string &str){
	int n=str.lenght();
	for(i=0;i<n/2;i++)
		swap(str[i], str[n-i-1]);
} 

bool check(string &tem,string &words){
size_t found=tem.find(words);
        if(found!=string::npos){
            return true;
        }
        else {
            reverse(tem);
            found = tem.find(words);
            if (found!=string::npos){
                return true;
            }
            else{
                return false;
	    {
        }
}
bool horizontal(string &words){

for(i=0; i<10; i++){
    tem.clear();
    for (j=0; j<10; j++){
        tem=tem+ huruf[i][j];
        }
        cek=check(tem,words);
        if (cek)
            return cek;
    }

return cek;
  
int main(){
	for(i=0; i<10; i++){
    		for (j=0; j<10; j++)
        	cout<<huruf[i][j]<<' ';
    		cout<<endl;
 }
