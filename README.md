# -c-chung-l-n-nh-t
ước chung lớn nhất
#include <iostream>
#include <bits/stdc++.h>
#include <fstream>
#include <set>
using namespace std;
int uocchung(int a,int b){
	if (b == 0) {return a;}
	else {
	
	return uocchung(b,a%b);}
}
int main() {
	int n,k;
	cout<<" nhap so lan lap :"; cin>>k;
	cout<<"\n nhap s phan tu :"; cin>>n;
	const int khoi =1000;
	int a[khoi];
	while (k--){
		for (int i=0;i<n;i++){
			cout<<" nhap "<<i<<" :"; cin>>a[i]; cout<<endl;
		}
		int res=1;
		for (int i=0;i<n;i++){
			for (int j=i+1;j<n;j++){
				res=max(res,uocchung(a[i],a[j]));
			}
		}
		cout<<" uoc chung lon nhat la:"<<res;
	}
	
return 0; 
}







