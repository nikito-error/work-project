#include <iostream>
#include <stdlib.h>
#include <time.h>
using namespace std;
#define N 30 
int A[N], n, i;

void inputkeyboard() 
{ do  
 { cout<<"\n Razmer na masiva: "; 
     cin>>n;
 }
while (n<0 || n>N);
for (i=0; i<n; i++)
    { cout<<"\n A["<<i+1<<"] = "; 
      do
      {cin>>A[i];
      }
	  while (A[i]<100 || A[i]>999); 
    }
}
void inputrandom()
{
    srand(time(0)); 
       do
 {
     cout<<"\n Razmer na masiva: ";
     cin>>n;
 }
 while (n<0 || n>N);
for (i=0;i<n;i++)
    {
    A[i] =100+rand()%900; 
    }
 for (i=0;i<n;i++)
    {
        cout<<"\n A["<<i+1<<"] = "<<A[i];
    }
}
int array[] = { 151,152,123,694,255,956,427,218,769,320 }; 
int count = sizeof(array) / sizeof(int);
int first(int an_array[],int  members) 
{
int a, j, b, *T; 
  T = new int [members];
         for (a = 0, j = 0; a < members; a++) 
         {
                 b = an_array[a]; 
                 if (b % 2) 
                        T[j++] = b;
         }
for (a = 0; a < members; a++)
         {
                 b = an_array[a]; 
                 if (!(b % 2))
                        T[j++] = b;
         }
cout << "\n\nIztinskiqt masiv e:\n";
         for (a=0;a<members; a++)
                 cout << an_array[a] << " ";
 cout << "\n\nV nachaloto sa nechetnite a sled tqh chetnite:\n"; 
         for (a=0;a<members;a++)
                 cout << T[a] << " ";
         cout << endl; 
         delete [] T; 
}
int arr[] = { 151,152,123,694,255,956,427,218,769,320 }; 
int counnt= sizeof(arr) / sizeof(int); 
int sort(int an_arr[], int members) 
{
int a, j, b, *T; 
int p[1000];
  T= new int [members];
         for (j = 100; j < 1000; p[j++] = 0) 
        ;
for (a = 0; a < members; p[an_arr[a++]]++)
        ; 
for (j = 100, a = 0; j < 1000; j++)
         {
		 b = p[j];
                 while (b--)
                        T[a++] = j;
         }
         cout << "\n\nIztinskiqt masiv e:\n"; 
         for (a = 0; a < members; a++)
                 cout << an_arr[a] << " ";
cout << "\n\nSortiran vuv vuzhodqsht red e:\n"; 
         for (a = 0; a < members; a++)
                 cout << T[a] << " ";
         cout << endl;
         delete [] T; 
}
int main() 
{
    inputrandom();
    int P[10] = {}; 
    int p, max;
    for (i=0;i<n;i++) 
    {
        P[A[i]%10]++; 
        p= A[i]/10;
        P[p%10]++;
        P[p/10]++;
    }
max = -1;
    for (i=0;i<10; i++) 
        if (P[i]>max) 
            max=P[i];
    for (i=0; i<10; i++)
        if (P[i]==max) 
            cout <<"\n Nai-chesto sreshtanata cifra e " << i << "  " << max << " broia\n"; 
    first(array,count); 
          sort(arr,counnt);	
			       system("pause"); 
          return 0;
} 
t
