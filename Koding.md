
/*
# Tugas-Kelompok-Pemrograman-Terstruktur
NAMA KELOMPOK :
PRIMA FEMINITA - 1717051059
REDA MEININGTIYAS - 1717051055
*/

#include <iostream>
#include <string.h>
#include <cstdlib>
using namespace std;
    string words, tem;
    bool cek;
    int i,j;
    char huruf[10][10]{ {'p','e','g','n','i','r','t','s','i','g'},
		 	{'o','l','b','l','l','m','l','o','s','k'},
                        {'i','k','a','s','o','o','j','k','g','q'},
			{'n','o','a','c','o','l','c','e','n','l'},
	 	        {'t','g','t','t','e','y','n','k','u','s'},
	   		{'e','u','o','c','n','i','a','k','f','t'},
			{'r','t','p','e','l','e','r','r','o','r'},
			{'c','l','a','n','r','o','o','t','r','c'},
			{'t','o','o','b','i','m','n','c','a','a'},
			{'b','b','q','a','o','u','t','p','u','t'}};
 
void reverse(string &string){
    int n = string.length();
    for (int i=0; i<n/2; i++)
    	swap(string[i], string[n-i-1]);
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
            }
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
}

bool diagonalkanan(string &words){
    int x=-9;
    for(i=9;i>=0;i--){
        tem.clear();
        for(j=i;j<=9;j++){
            tem=tem+huruf[j+x][j];
        }
        cek=check(tem,words);
	if(cek)
        return cek; x++;
    } 
    for(i=9;i>=0;i--){
        tem.clear();
        for(j=0;j<i;j++){
            tem=tem+huruf[j+x][j];
        }
        cek=check(tem,words);
	if(cek)
        return cek; x++;
    }
return false;
}

bool diagonalkiri(string &words){
    for(i=0;i<=9;i++){
    int x=i;
     	tem.clear();
        for(j=0;j<=i;j++){
            tem=tem+huruf[j][x]; x--;
        }
        cek=check(tem,words);
	if(cek)
        return cek;
    }
     for(i=1;i<=9;i++){
     int x=9;
	 tem.clear();
	 for(j=i;j<=9;j++){
	    tem=tem+huruf[j][x]; x--;
	}
	cek=check(tem,words);
	if(cek)
        return cek;
     }
return false;
}
 bool vertical(string &words){

for(i=0; i<10; i++){
    tem.clear();
    for (j=0; j<10; j++){
        tem=tem+huruf[j][i];
        }
        cek=check(tem,words);
		if(cek)
            return cek;
    }
return cek;
} 
int main(){
   for(i=0; i<10; i++){
    	for (j=0; j<10; j++)
       	cout<<huruf[i][j]<<' ';
  	cout<<endl;
 }
 
  cout<<"\n\nTulis Kata Yang Ingin Anda Cari"<<endl<<endl;
  cari:
  cin>>words;
	if (horizontal(words)){
	    cout <<"Ada (Horizontal)"<<endl<<endl;
	    goto cari;
	    }
	else if (vertical(words)){
	    cout <<"Ada (Vertikal)"<<endl<<endl;
	    goto cari;
	    }
	else if (diagonalkanan(words)){
	    cout <<"Ada (Diagonal)"<<endl<<endl;
	    goto cari;
	    }
	else if (diagonalkiri(words)){
		cout<<"Ada (Diagonal)"<<endl<<endl;
		goto cari;
		}
	else
	    cout <<"Kata yang ada cari tidak ada"<<endl<<endl;
	    goto cari;
return 0;
}

