
int size=100;

typedef struct {
    int * arr;
    int size;
    int top;
} MyStack;


MyStack* myStackCreate() {
    MyStack* stack=(MyStack*)malloc(sizeof(MyStack));
    stack->arr=(int *)malloc(size*sizeof(int));
    stack->size = size;
    stack->top = -1;
    return stack;
}

void myStackPush(MyStack* obj, int x) {
    if(obj->top < obj->size-1){
        obj->top++;
        obj->arr[obj->top]=x;
    }
}

int myStackPop(MyStack* obj) {
    if(obj->top==-1){
        return -1;
    }
    return obj->arr[obj->top--];
}

int myStackTop(MyStack* obj) {
    if(obj->top==-1){
        return -1;
    }
    return obj->arr[obj->top];
}

bool myStackEmpty(MyStack* obj) {
    return obj->top==-1;
}

void myStackFree(MyStack* obj) {
    free(obj->arr);
    free(obj);
}

/**
 * Your MyStack struct will be instantiated and called as such:
 * MyStack* obj = myStackCreate();
 * myStackPush(obj, x);
 
 * int param_2 = myStackPop(obj);
 
 * int param_3 = myStackTop(obj);
 
 * bool param_4 = myStackEmpty(obj);
 
 * myStackFree(obj);
*/
