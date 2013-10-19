//code for making a queue out of two stacks
#include <iostream>

using namespace std;

//stack implementation
int top = 0;
int topb = 0;
void push_a(int);
void push_b(int);
int pop_a();
int pop_b();
const int size = 10;
int integer,element,elem;
int x = 0;
int y = 0;
int temp = -1;
int a[size];
int b[size];
int store;
int final;


int main()
{

    statement: //this is the goto statement label.

    while(temp!=0)
    {

        cout<<"Enter 1 to push an element onto the queue"<<endl;
        cout<<"Enter 2 to pop an element off the queue"<<endl;
        cout<<"Enter 0 to exit"<<endl;
        cin>>temp;


    switch(temp)
    {

        case 1:
        {

            //push implementation, tests for when the queue is full.

            cout<<"Please enter the value that needs to be added to the queue"<<endl;
            cin>>integer;

            push_a(integer);
            break;
        }
         case 2:
         {  //pop implementation, tests for when the queue is empty.
           if(topb==0)
            {
                while(top!=0)
                {
                    store = pop_a();
                    push_b(store);
                }
                pop_b();
                goto statement;
            }
            if(topb!=0)
            {
                if(top==0)
                {
                    pop_b();
                    goto statement;
                }
            }
            if(topb!=0)
            {
                if(top!=0)
                {
                    pop_b();
                    goto statement;
                }
            }
           break;
         }
    }
    }
    return 0;
}

void push_a(int element)
{
        if(top!=size)
{
        a[top] = element;
        top++;
        x++;
        cout<<"The number of elements on the stack A is "<<x<<endl;

}
        else{
               cout<<"Cannot add any more elements as the stack A is full as the top is now"<<top<<endl;
        }
}

void push_b(int elem)
{
        if(topb!=size)
{
        b[topb] = elem;
        topb++;
        y++;
        //cout<<"The number of elements on the stack B is "<<y<<endl;

}
        else{
               cout<<"Cannot add any more elements as the stack B is full as the top is now"<<topb<<endl;
        }
}

int pop_a()
{
    if (top==0)
            {


            cout<<"Cannot pop any more elements as the stack A is empty and top is now "<<top<<endl;
         }
        else{
            top--;
            x--;
            element = a[top];
            //cout<<"The popped element of stack A is "<<element<<endl;
            //cout<<"The number of elements on the stack A is "<<x<<endl;
}
return element;
}

int pop_b()
{
    if (topb==0)
            {


            cout<<"Cannot pop any more elements as the stack B is empty and top is now "<<topb<<endl;
         }
        else{
            topb--;
            y--;
            elem = b[topb];
            cout<<"The popped element of stack B is "<<elem<<endl;
            //cout<<"The number of elements on the stack B is "<<y<<endl;
}
return elem;
}


