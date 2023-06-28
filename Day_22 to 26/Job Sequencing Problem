#include <bits/stdc++.h> 
#include<algorithm>
bool comp(vector <int> a,vector<int> b)
{
     return a[1]>b[1];
     }
int jobScheduling(vector<vector<int>> &jobs)
{
    sort(jobs.begin(),jobs.end(),comp);
    int n=jobs.size();
    int maxdead=INT_MIN;
    for (int i=0;i<n;i++)
     maxdead=max(jobs[i][0],maxdead);
     int profit=0;
     vector<int> ans(maxdead+1,-1);     //why maxdead +1 soze is needed  ans 1 indexing is used
     for (int i=0;i<n;i++)
     {
         int currdead=jobs[i][0];
         int currprofit=jobs[i][1];
         for (int k=currdead;k>0;k--)
         {
             if(ans[k]==-1)
             {
                 profit+=currprofit;
                 ans[k]=1;
                 break;
             }
         }
     }
    return profit;
}
