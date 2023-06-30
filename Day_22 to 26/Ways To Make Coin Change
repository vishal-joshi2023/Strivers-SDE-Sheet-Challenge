#include<bits/stdc++.h>
long solve(int *denominations, int n, int value, int index, vector<vector<long>> &dp)
{
    if(index==n)
    {
        if(value==0)
        return 1;

        else
        return 0;
    }

    if(value<0)
    return 0;

    if(dp[index][value]!=-1)
    return dp[index][value];
    else
    return dp[index][value]=long (solve(denominations, n, value-denominations[index], index, dp) +
     solve(denominations,n,value,index+1, dp));

    

}
long countWaysToMakeChange(int *denominations, int n, int value)
{
    //Write your code here
    int index =0;
    vector<vector<long>> dp(n,vector<long>(value+1,-1));
    return solve(denominations, n,value,  index, dp);
}
