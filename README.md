# praktikum8


##Latihan.cpp

**Alur Algoritma**
1. mulai program
2. masukan rumus untuk mencari maxmin bilangan 
3. masukan rumus untuk mencari nilai modus dari matrix
4. masukan rumus untuk mencari kedua matrikx
5. masukan semua kedalam satu program dengan intuksi awal int
6. run .
7. end

**Peseudecode**
```
int maxmin
{
for(a<--1 to baris do)
cin >> a;
if[a] < (min);
return 0;
}
HitungStatistik
void hitung_modus;
int a, a[20], f[11];
{
for(int i<--0; i<20 to do)
hitung_modus;
}
jumlah_matriks(input matrik1, matrik2: matriks; baris,
kolom: integer): matriks
jumlah: matriks
for x ? 1 to baris do
for y ? 1 to kolom do
jumlah[x,y] ? matrik1[x,y] + matrik2[x,y]
jumlah_matriks ? jumlah

cout << matrix transponse
{
for(x<--0; to do)
}
{
for(y<--0; to do)
}
fugsi utama
int main()
{
int maxmin();
HitungStatistik();
matrik_1();
matrik_2();
transpose_m();
hasil();

return 0;
}
```

**Code Program**
```#include <iostream>
#include <conio.h>
using namespace std;
int maxmin()
{
    int nilai[3],a,min,maks;
    for(a=1;a<=5;a++){
   cout<<"Masukkan nilai ke-"<<a<<":";
   cin>>nilai[a];
    }
   min = nilai[1];
   maks = nilai[1];
   for(a=1;a<=5;a++){
   if(nilai[a] < min){
   min = nilai[a];
   } else if(nilai[a] > maks){
   maks = nilai[a];
   }
   }
   cout<<"nilai minimum adalah : "<<min<<endl;
   cout<<"nilai maksimum adalah : "<<maks<<endl;

getch();
return 0;
}
class HitungStatistik {
friend ostream& operator<<(ostream&, HitungStatistik&);
friend istream& operator>>(istream&, HitungStatistik&);
public:
HitungStatistik();
void hitung_modus();
private:
void maksimum();
void frekuensi();
int maks, item;
int n;
int A[20];
int f[11];
};

HitungStatistik::HitungStatistik()
{ for (int i=0; i<20; i++) f[i] = 0; }

istream& operator>>(istream& in, HitungStatistik& a) {
cout << "Banyaknya data : ";
cin >> a.n;
for (int i = 0; i < a.n; i++) {
cout << "Data ke- : " << i+1 << " > ";
cin >> a.A[i];
}
return in;
}

void HitungStatistik::maksimum()
{
maks = f[0];
item = 1;
for (int i=0; i<n; i++)
if (f[i] > maks) {
maks = f[i];
item = i;
}
cout << "Modus = " << item;
}

void HitungStatistik::frekuensi()
{
for (int i=1; i<n; i++) ++f[A[i]];
}

void HitungStatistik::hitung_modus() {
cout << "Frekuensi running\n";
frekuensi();
maksimum();
}

ostream& operator<<(ostream& out, HitungStatistik& a) {
cout << "Mulai ...\n";
a.hitung_modus();
cout << "Nilai modus : " << a.item;
return out;
}

int matrik1[2][2];
int matrik2[2][2];
int matrik3[2][2];
int temp;

//input matrik pertama
void matrik_1(){

int matrik1[2][2];
int matrik2[2][2];
int matrik3[2][2];
int temp;

for (int x = 0;x<2;x++){
for (int y =0;y<2;y++){
cout <<"masukan nilai matrik pertama baris ke-"<<(x+1)<<" kolom ke-"<<(y+1)<<" : ";
cin>>matrik1[x][y];
}
}

cout<<endl;
//output matrik pertama
cout<<"Matrik Pertama :"<<endl;
for (int x = 0;x<2;x++){
for (int y =0;y<2;y++){
cout <<matrik1[x][y]<<"   ";
}
cout<<endl;
}
}

void matrik_2(){
int matrik1[2][2];
int matrik2[2][2];
int matrik3[2][2];
int temp;


//input matrik kedua
for (int x = 0;x<2;x++){
for (int y =0;y<2;y++){
cout <<"masukan nilai matrik kedua baris ke-"<<(x+1)<<" kolom ke-"<<(y+1)<<" : ";
cin>>matrik2[x][y];
}
}
cout<<endl;
//output matrik kedua
cout<<"Matrik Kedua :"<<endl;
for (int x = 0;x<2;x++){
for (int y =0;y<2;y++){
cout <<matrik2[x][y]<<"   ";
}
cout<<endl;
}
}

void hasil(){
int matrik1[2][2];
int matrik2[2][2];
int matrik3[2][2];
int temp;

for (int x = 0;x<2;x++){
for (int y =0;y<2;y++){
matrik3[x][y]=0;
for (int z =0;z<2;z++){
temp=matrik1[x][z]*matrik2[z][y];
matrik3[x][y]=matrik3[x][y]+temp;
}
}
}
cout<<endl;
cout<<"Matrik hasil perkalian :"<<endl;
for (int x = 0;x<2;x++){
for (int y =0;y<2;y++){
cout <<matrik3[x][y]<<"   ";
}
cout<<endl;
}
}

int transpose_m()
{

int A[10][10],b,c,baris,kolom;
char pil;
cout<<"Jumlah Baris : ";
cin>>baris;
cout<<"Jumlah Kolom : ";
cin>>kolom;
cout<<endl;
for (b=0;b<baris;b++)
{
for (c=0;c<kolom;c++)
{
cout<<" Matriks ["<<b+1<<","<<c+1<<"] =";
cin>>A[b][c];
}
}

cout<<endl<<endl;
cout<<"Matriks Pertama :"<<endl<<endl;
for (b=0;b<baris;b++)
{
for (c=0;c<kolom;c++)
{
cout<<" " <<A[b][c]<<" " ;
}
cout<<endl<<endl;
}

cout<<"Matriks Transpose :"<<endl<<endl;
for (b=0;b<kolom;b++)
{
for (c=0;c<baris;c++)
{
cout<<" "<<A[c][b]<< " ";
}
}
}


int main()
{
int maxmin();
HitungStatistik();
matrik_1();
matrik_2();
transpose_m();
hasil();

return 0;
}
```
**Hasil**
![Hasil](https://raw.githubusercontent.com/sofianadi/praktikum8/master/program/latihan/screenshot%20hasil.png)