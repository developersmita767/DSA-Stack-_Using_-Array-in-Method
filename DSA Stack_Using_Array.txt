//stack using array
import java.util.*;
class MyStack
{
	int top,max;
	int arr[];
	MyStack(int max)
	{
	  top=-1;
	  this.max=max;
	  arr=new int[max];
	}
	void push(int ele)
	{
	  if(top==max-1)
	  {
	     System.out.println("stack overflow");
	     return;

	  }
	  top++;
	  arr[top]=ele;
	  System.out.println(ele+" insert");
	}
	void pop()
	{
	  if(top==-1)
	  {
	     System.out.println("stack underflow or no element");
	     return;
	  }
	    System.out.println("delete element= " + arr[top]);
	    top=top-1;

	}
	void peek()
	{
	   if(top==-1)
	   {
	     System.out.println("stack underflow or no element");
	     return;
	   }
	   System.out.println("top elemment="+ arr[top]);
	}
	 void disp()
	 {
	    if(top==-1)
	   {
	     System.out.println("stack underflow or no element");
	     return;
	   }
	   System.out.println(" elemment are");
	   int i=top;
	   while(i>=0)
	   {
	     System.out.println(arr[i]);
	     i--;
	   }
	}

	 
}


//drivenclass
class Test
{
	public static void main(String[] args)
	{
       Scanner sc = new Scanner(System.in);
       MyStack m=new MyStack(5);
       int ch;
       while(true)
       {
         System.out.println("enter your choice\n1.push\n2.pop\n3.peek\n4.disp\n5.exit");
         ch=sc.nextInt();
         switch(ch)
         {
          case 1:
          System.out.println("enter a element to push");
          m.push(sc.nextInt());
          break;
          case 2:
          m.pop();
          break;
          case 3:
          m.peek();
          break;
          case 4:
          m.disp();
          break;
          case 5:
          System.exit(0);
          default:System.out.println("invalid choice ");

         }
       }	
	}
}