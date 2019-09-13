# *p

```c++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;
struct NODE{
    NODE *next;
    int val;
    NODE(int x){
        this->val=x;
        this->next=NULL;
    }
}*root;
void modify1(NODE* &node){
    node=NULL;
}
void modify2(NODE* &node){
    node=node->next;
}
void travasal(NODE *node){
    while(node!=NULL){
        printf(" %d",node->val);
        node=node->next;
    }
    printf("\n");
}
int main(){
    root=new NODE(1);
    root->next=new NODE(2);
    root->next->next=new NODE(3);
    root->next->next->next=new NODE(4);
    
    travasal(root);
    //modify1(root->next->next);
    
    //travasal(root);
    
    NODE * a=root->next;
    modify2(a);
    travasal(a);
    travasal(root->next);
    return 0;
}

```

