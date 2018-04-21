# Tugas-Kelompok-Pemrograman-Terstruktur

#include <iostream>
#include <string.h>
#include <bits/stdc++.h>
using namespace std;
    string words, tem;
    bool cek;
    char huruf[10][10]{ {'p','e','a','c','d','v','q','w','f','g'},
		 	{'o','c','b','n','j','m','l','o','c','k'},
                        {'i','k','o','s','o','y','j','k','a','q'},
			{'n','d','o','m','w','i','r','e','w','l'},
	 	        {'t','g','t','n','p','v','b','m','n','o'},
	   		{'e','e','x','c','n','u','l','k','s','h'},
			{'r','t','i','e','n','j','t','b','d','n'},
			{'c','l','i','c','k','q','n','e','k','p'},
			{'s','z','m','t','e','q','j','s','r','b'},
			{'b','b','q','p','w','h','f','b','m','k'}};
 
 
 
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
