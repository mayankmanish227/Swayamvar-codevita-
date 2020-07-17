# Swayamvar-codevita-
using linked list


import java.util.*;
import java.io.*;
public class Hello
{
  public static void main(String[] args)
  {
    Scanner sc=new Scanner(System.in);
    int n=sc.nextInt();
    sc.nextLine();
    String br=sc.next();
   
    String gr=sc.next();
 
    System.out.println(check(br,gr,n));
  }
  static int check(String br,String gr,int n)
  {
    
    int count=0;
    LinkedList<Character> li=new LinkedList<>();
    
    for(int i=0;i<n;i++)
    {
      li.add(gr.charAt(i));
 
    }
    
   for(int i=0;i<br.length();i++)
   {
     
     if(li.contains(br.charAt(i)))
         {
           li.removeFirstOccurrence(br.charAt(i));
           count++;
         }
      else if(!li.contains(br.charAt(i)))
         {
        	break;
         }
                 
    }
    return br.length()-count;
  }      
}
