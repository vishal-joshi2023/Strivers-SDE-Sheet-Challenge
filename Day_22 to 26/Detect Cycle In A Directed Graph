#include<bits/stdc++.h>
bool dfs(int i,vector<int>& vis,vector<int>& pathvis,vector<list<int>>& adj)
{
  vis[i]=1;
  pathvis[i] = 1;

  for(auto nb:adj[i])
  {
    if (vis[nb] == 0) {
      if (dfs(nb, vis, pathvis, adj) == true)
        return true;
    }

    else if (pathvis[nb] == 1)
      return true;
  }
  pathvis[i] = 0;
  return false;
}
int detectCycleInDirectedGraph(int n, vector < pair < int, int >> & edges) {
  // Write your code here.
  vector<list<int>> adj(n+1);

  for(int i=0;i<edges.size();i++)
  {
    int u = edges[i].first;
    int v = edges[i].second;

    adj[u].push_back(v);
  }

  vector<int> vis(n+1,0);
  vector<int>pathvis(n+1,0);

  for(int i=1;i<=n;i++)
  {
    //pathvis={0};
    if (vis[i] == 0) {
      if (dfs(i, vis, pathvis, adj))
        return 1;
    }
  }
  return 0;
}
