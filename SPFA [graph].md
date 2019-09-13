# SPFA [graph]

1. `vis[i]`代表`queue`中已经有`i`存在，此时只需要更新`dis[i]`，而不需要` push(i)`
2. 当`dis[i]`更新后，说明后续节点也可以更新，` push(i)`

```c++
SPFA
void Spfa()
{
    for (int i(0); i<num_town; ++i)//初始化
    {
        dis[i] = MAX;
        visited[i] = false;    
    }
    queue<int> Q;
    dis[start] = 0;
    visited[start] = true;
    Q.push(start);
    while (!Q.empty()){
        int temp = Q.front();
        Q.pop();
        for (int i(0); i<num_town; ++i)
        {
            if (dis[temp] + road[temp][i] < dis[i])//存在负权的话，就需要创建一个COUNT数组，当某点的入队次数超过V(顶点数)返回。
            {
                dis[i] = dis[temp] + road[temp][i];
                if (!visited[i])
                {
                    Q.push(i);
                    visited[i] = true;    
                }        
            }            
        }
        visited[temp] = false;            
    }    
}
```

[Reference][https://www.cnblogs.com/devtang/archive/2011/08/25/SPFA.html]