3.1 编写打印出一个单链表的所有元素的程序
```
void printList(List L)     //L为链表的头节点
{
  Position P;
  P = L->next;
  if(p->next!=NULL)
  {
    print(P->data);
    P = P->next;
  }
}
```
3.2 写出过程PrintLots(L,P),只使用表的基本操作。
```
void PrintLots(L,P)  // L,P均为两个链表，打印出链表L中P链表位置的元素。L,P均为以升序排列的整数
{
  Position H1,H2;   
  H1 = L->next,H2 = P->next;
  int i;
  while(H2->next!=NULL)
  {
    i = H2->data;
    while(H1->next!=NULL&&i>0)       //定义变量i来确定在L中的位置
    {
      print(H1->data);
      H1 = H1->next;
      --i;
    }
  }
}
```
3.3 通过只调整指针（而不是数据）来交换两个相邻的元素
```
void switch(L,l1,l2)    //单链表
{
  Position p,h;
  h = l2->next;
  p = findprevious(L,l1);
  l1->next = h;
  l2->next = l1;
  p ->next = l2;
  return;
}

void switch(L,l1,l2)     //双链表
{
  Position p,h,q;
  p = l1 ->next;
  q = l1 ->pres;
  l1->next = l2 ->next;
  l2->next->pres = l1;
  l1->pres->next = l2;
  l2->pres = q;
  l2->next = l1;
  l1->pres = l2;
  return;
}
```
