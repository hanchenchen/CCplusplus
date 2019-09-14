# 欧拉路径_[euler path]

##### iteration

```c++
 stack<int> st;
    vector<int> ans;
    st.push(1);
    while(!st.empty()){
        int x=st.top(),i;
        for(i=0;i<g[x].size();i++){
            if(!vis[x][g[x][i]]){
                vis[x][g[x][i]]=vis[g[x][i]][x]=true;
                st.push(g[x][i]);
                break;
            }
        }
        if(i==(int)g[x].size()){
            st.pop();
            ans.insert(ans.begin(),x);
        }
    }
    for(int i=0;i<ans.size();i++){
        if(i!=0)cout<<" ";
        cout<<ans[i];
    }
```

##### dfs



##### fleury