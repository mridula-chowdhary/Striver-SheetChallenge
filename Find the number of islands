void dfs( int** arr,int row,int col, int n,int m,vector<vector<int>>&vis){
   vis[row][col]=1;
    int drow[]={0,+1,0,-1,+1,-1,+1,-1};
    int dcol[]={+1,0,-1,0,+1,-1,-1,+1};
   for(int i=0;i<8;i++){
      int dr=row+drow[i];
      int dc=col+dcol[i];
      
      if (dr >= 0 && dr < n && dc >= 0 && dc < m && !vis[dr][dc] &&
          arr[dr][dc]) {
        dfs(arr,dr,dc,n,m,vis);
      }
   }
}

int getTotalIslands(int** arr, int n, int m)
{
   vector<vector<int>>vis(m,vector<int>(n,0));
   int cnt=0;
   for(int i=0;i<n;i++){
      for(int j=0;j<m;j++){
         if(!vis[i][j] && arr[i][j]==1){ 
            dfs(arr,i,j,n,m,vis);
            cnt++;
         }
      }
   }
   return cnt;
}
