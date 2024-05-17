# Insertion-of-two-linked-list
class ListNode {
int val;
ListNode(int x){
val = x;
next = null;
   }
}
class solution {
public ListNode Intersection(ListNode HeadA,  ListNode HeadB){
ListNode tempA = HeadA;
ListNode tempB = HeadB;
int lengthA = 0, lengthB = 0;
while(tempA != null){
lengthA++;
tempA = tempA.next;
}
while(tempB != null){
lengthB++;
tempB = tempB.next;
}
tempA = HeadA;
tempB = HeadB;
if(lengthA > lengthB){
int size = lengthA - lengthB;
for(int i = 1; i <= size; i++){
tempA = tempA.next;
  }
}
else{
int size = lengthB - lengthA;
for(int i = 1; i <= size; i++){
tempB = tempB.next;
  }
}
while(tempA != tempB){
tempA = tempA.next;
tempB = tempB.next;
}
return tempA;
  }
}
