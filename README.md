# java-code
//Target sum

import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner scn=new Scanner (System.in);
		int n=scn.nextInt();
		int a[]=new int[n];
		for(int i=0;i<a.length;i++){
		    a[i]=scn.nextInt();
		}
		
			System.out.println("enter the target");
		int tar=scn.nextInt();
	
		printtargetsumSubsets(a,0," ",0,tar);
		
	}

	public static void printtargetsumSubsets(int a[],int idx,String str,int sum, int tar){
	    //base case
	    if(idx==a.length){
	        if(sum==tar){
	            System.out.println(str + " ");
	        }
	        return;
	    }
	    
	  //jab call lag kr valure add ho rhi h   
	    printtargetsumSubsets(a,idx+1,str+a[idx]+", ",sum+a[idx],tar);
	    //jab value add nhi ho rhi
	    printtargetsumSubsets(a,idx+1,str,sum,tar);
	}
    
}

