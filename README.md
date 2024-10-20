# Exp-17-Linked-List
# Aim
Write a c++ program:
1. To create a node in c++.
2. To add node in c++.
# Software Used
VS Code and c++ online compiler.
# Theory
A linked list is a linear data structure in which elements are stored in nodes that are dynamically allocated in memory. Each node contains two components: data and a pointer (or reference) to the next node in the sequence. This structure allows for efficient memory utilization and flexibility in managing data.

Each node typically contains:
Data-(The value or information stored.) ,
Pointer-(A reference to the next node in the list.)

Linked lists in C++ are a fundamental data structure that provides flexibility in memory allocation and efficient data management. They are particularly useful in scenarios requiring frequent modifications to the dataset size.

# Program Code
```
//Node

#include<iostream>
using namespace std;
class Link{
    public:
    int data ;
    Link* next;
    Link(int num){
        data = num;
        next = NULL;
    }
};
int main(){
    Link* l1 = new Link(6);
    cout << l1->data<<"   "<<l1->next;
}
```
```
//Adding node

#include<iostream>
using namespace std;
class Link{
    public:
    int data ;
    Link* next;
    Link(int num){
        data = num;
        next = NULL;
    }
};
void insert_head(Link* &head, int data){
    Link* new_node = new Link(data);
    new_node -> next= head;
    head = new_node;
}
void disp(Link*head){
    Link*temp = head;
    while (temp!= NULL){
        cout<<temp->data<<"->";
        temp = temp->next;

    }
    cout<<"NULL"<<endl;
}

int main(){
    Link*head = NULL;
    insert_head(head, 30);
    disp(head);
    insert_head(head, 32);
    disp(head);
    insert_head(head,35);
    disp(head);
}
```
# Output
### Node
![image](https://github.com/user-attachments/assets/28ffe951-d215-4665-9758-77851c337466)
### Adding node
![image](https://github.com/user-attachments/assets/2e1b7c19-092a-403c-8a91-4907cb2b7192)
# Conclusion
We learnt how to create nodes and adding nodes in c++.
