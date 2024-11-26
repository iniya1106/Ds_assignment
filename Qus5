typedef struct{
    int val;
    struct Node* next;
}Node;
bool dfs(Node* graph[],bool visited[],int current,int destination);

bool validPath(int n, int** edges, int edgesSize, int* edgesColSize, int source, int destination) {
Node* graph[n];
for(int i=0;i<n;i++){
    graph[i]=NULL;
}
for(int i=0;i<edgesSize;i++){
    Node* node=(Node*)malloc(sizeof(Node));
    node->val=edges[i][1];
    node->next=graph[edges[i][0]];
    graph[edges[i][0]]=node;
    node=(Node*)malloc(sizeof(Node));
    node->val=edges[i][0];
    node->next=graph[edges[i][1]];
    graph[edges[i][1]]=node;
}
bool visited[n];
for(int i=0;i<n;i++){
    visited[i]=false;
}
return dfs(graph,visited,source,destination);
}
bool dfs(Node* graph[],bool visited[],int current,int destination){
    if(current==destination){
        return true;
    }
    visited[current]=true;
    for(Node* node=graph[current];node;node=node->next){
        if(!visited[node->val]){
            if(dfs(graph,visited,node->val,destination)){
                return true;
            }
        }
    }
    return false;
}
