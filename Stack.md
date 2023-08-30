Stack 
It is a liner data structure in which the insertion and removal of a new element and removal of existing element  takes places at the same end represented as the top of the stack 

It follows LIFO principle. Real life example will be pile of plates

Basic operations of stack

PUSH
Algorithms
begin 
if stack is full 
   return
endif
else
    increment top
    stack[top] assign value
end else
end procedure


POP
Algorithm
if stack is empty
  return 
endif
else
  store value of stack[top]
  return value
end else
end procudure


TOP
Algorithm

begin
return stack[top]
end procedure

isEmpty
Algorithm

begin
if top < 1
  return true
else
   return false


Types of stack
1. Fixed size stack
2. Dynamic size stack


Applications of stack
1. Infix to postfix / prefix conversion
2. redo-undo features at many places like editors , photoshop.
3. forward and backward features in web browser
4. string reversal
5. stack helps in implementing function call in computers. The last called function is always completed first.
