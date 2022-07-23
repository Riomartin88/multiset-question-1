# include <bits/stdc++.h>
using namespace std;
int main() {

//taking the testcase


	int T;
	cin >> T;    
    while(T--)
	{
    
    //taking the number of bags and time in min and candies
    
    
		int n,k;
		cin >> n >> k;
		multiset<long long>b;
		for(int i=0;i<n;i++){
			long long candy;
			cin>>candy;
      
      //now inserting the candies in multiset its always be in sorted order
       
			b.insert(candy); 
		}
		long long total_candies=0;
		for(int i=0;i<k;++i)
		{
			auto last_it=(--b.end());
			long long candy=*last_it;
			total_candies+=candy;
			b.erase(last_it);
			b.insert(candy/2);

		}
		cout<<total_candies<<endl;
	}
}
