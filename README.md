# linkedlist
This is my git repo with codes of linkedlist.



 /*import java.io.*; 
public class list{
    
    public static void main(String args[]){

        Node head=new Node(10);
        Node temp1=new Node(20);
        Node temp2=new Node(30);
        head.next=temp1;
        temp1.next=temp2;
        temp2.next=null;
        System.out.print(head.data + "----> " +temp1.data + "----->" + temp2.data);

    }
}
class Node{

    int data;
    Node next;
    Node(int x){
        data=x;
        next=null;
    }
}*

//traversal linked list

    import java.io.*;
     public class list{
        public static void main(String args[]){

            Node head=new Node(10);
            head.next=new Node(20);
            head.next.next=new Node(30);
            head.next.next=new Node(40);
            head.next.next.next=null;
            printlist(head);
        }
 
    public static void printlist(Node head){

        Node curr=head;
        while(curr!=null){
             System.out.println(curr.data +"--->");
             curr=curr.next;

        }
    }
}
class Node{

    int data;
    Node next;
    Node(int x){
        data=x;
        next=null;
    }
}

//1.Insert Linked list at the begining 

class Node{

    int data;
    Node next;
    Node(int data){
        this.data=data;
        next=null;
    }
}

class Linkedlist{

    Node head;

    public void insertatbegin(int data){

        Node newnode=new Node(data);
        newnode.next=head;
        head=newnode;
    } 

    public void printlist(){
        Node temp=head;
        while(temp!=null)
        {
            System.out.println(temp.data + "");
            temp=temp.next;
    }
}
}

public class list{
    public static void main(String args[]){

        Linkedlist List=new Linkedlist();
        List.insertatbegin(1);
        List.insertatbegin(2);
        List.insertatbegin(3);
        List.insertatbegin(4);
        List.insertatbegin(5);     
        List.printlist();               
            }
        }

        

        //2.Insert at end

        class Node{

            int data;
            Node next;
            Node(int data){
                this.data=data;
                next =null;
            }
        }

        class list{

            Node head;
            static Node insertatend(Node head,int data){

                Node temp=new Node(data);
                Node curr=head;

                if(head==null)return temp;
                while(curr.next!=null){
                      curr=curr.next;
                }
                curr.next=temp;
                return head;          
            }
              public static void main(String args[]){

                Node head=null;
                head=insertatend(head, 40);
                head=insertatend(head, 30);
                head=insertatend(head, 20);
                head=insertatend(head, 10);
                print(head);
              }

              public static void print(Node head){
                Node curr=head;
                while(curr!=null){
                    System.out.println(curr.data);
                    curr=curr.next;
                }

              }
        }
              

              //3.Insert At a given Position 

              class Node{
                int data;
                Node next;
                Node(int x){
                    data=x;
                    next=null;
                }
              }

              class list{

                      Node insertatposition(Node head,int x,int pos){

                        Node temp=new Node(x); 
                        if(head==null)  
                        {
                            if(pos==1)return temp;
                            else return head;
                        }
                              
                        if(pos==1) //1st position (head need to be changed)
                    {
                        temp.next=head;
                        return head;
                    }
                        Node curr=head; 
                        for(int i=1;i<pos-1;i++){
                             curr=curr.next;
                             if(curr==null){
                                System.out.println("invalid position");
                                return head;
                             }
                        }
                        temp.next=curr.next;
                        curr.next=temp;
                        return head;
                      }

                      void printlist(Node head){

                        Node curr=head;
                        while(curr!=null){
                            System.out.println(curr.data);
                            curr=curr.next;
                        }
                        System.out.println();
                      }
              public static void main(String args[]){

                Node head=new Node(10);
                head.next=new Node(20);
                head.next.next=new Node(30);
                head.next.next.next=new Node(50);
                list ll=new list();
                ll.printlist(head);
                head=ll.insertatposition(head,40,4);
                ll.printlist(head);


              }
            }


  // 4.Delete the first node of singly Linked list

  class Node{

    int data;
    Node next;
    Node(int x){
        data=x;
        next=null;
    }
  }

  class list{

    public static void main(String args[]){

        Node head=new Node(10);
        head.next=new Node(20);
        head.next.next=new Node(30);
        printlist(head);
        System.out.println("After deletion");
        head=deletehead(head); 
        printlist(head);
    }

    static Node deletehead(Node head){
        if(head==null)return null;
        else{
            return head.next;
        }
    }
    public static void printlist(Node head){

        Node curr=head;
        while(curr!=null){
            System.out.println(curr.data);
            curr=curr.next;
        }
    }
  }


 //5.Delete At the End (Singly Linked List)

class Node{

    int data;
    Node next;
    Node(int x){

        data=x;
        next=null;
    }
}

class list{

    public static void main(String args[]){
        Node head=new Node(10);
        head.next=new Node(20);
        head.next.next=new Node(30);
        head.next.next.next=new Node(40);
        head.next.next.next.next=new Node(50);
        printlist(head);
        head=deleteEnd(head);
        System.out.println("After deletion");
        printlist(head);
    }

    static Node deleteEnd(Node head){

        Node curr=head;
        if(head==null)return null;
        if(head.next==null)return null;

        while(curr.next.next!=null){
            curr=curr.next;
        }
        curr.next=null;
        return head;
    }

    public static void printlist(Node head){
         Node curr=head;
         while(curr!=null){
            System.out.println(curr.data);
            curr=curr.next;
         }
    }
}
*/

 //6. Search X in Linked List


class Node{
    int data;
    Node next;
    Node(int x){
        data=x;
        next=null;
    }
}

class list { 

public static void main(String args[]) 
{ 
    Node head=new Node(10);
    head.next=new Node(20);
    head.next.next=new Node(30);
    printlist(head);
    System.out.println("Position of element in Linked List: "+search(head,20));
    
} 

static int search(Node head, int x){
    int pos=1;
    Node curr=head;
    while(curr!=null){
        if(curr.data==x)
            return pos;
        else{
            pos++;
            curr=curr.next;
        }
    }
    return -1;
}
public static void printlist(Node head){
    Node curr=head;
    while(curr!=null){
    System.out.print(curr.data+" ");
    curr=curr.next;
}System.out.println();
}
} 
