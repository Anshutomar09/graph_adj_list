# graph_adj_list
/******************************************************************************

                              Online C++ Compiler.
               Code, Compile, Run and Debug C++ program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <bits/stdc++.h>
using namespace std;

void addn(vector<vector<int>>&ad, int u, int v){
    ad[u].push_back(v);
    ad[v].push_back(u);
}
void print(int v, vector<vector<int>>&ad){
    for(int i=0;i<v;i++){
        cout<<i<<" -> ";
        for(auto am:ad[i]){
            cout<<am<<" ";
        }
        cout<<endl;
    }
}
int main()
{
    int v=5;
    vector<vector<int>>ad(v);
    addn(ad, 0, 1);
    addn(ad, 0, 2);
    addn(ad, 1, 2);
    
    print(v, ad);
    return 0;
}
