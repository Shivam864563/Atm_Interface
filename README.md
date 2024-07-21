# Atm_Interface

// Task 3 ) With class And Methods . 
import java.util.*;
public class ATM_machine{ 
   static void  handleWithdraw(int amount ) { 
    Scanner sc = new Scanner(System.in) ;
       System.out.print("Enter Amount ... ") ; 
       int withdraw = sc.nextInt() ;
       if(withdraw <=100) {
       amount -= withdraw ;
       System.out.printf("You have  debit amount %d , Your Current amount is %d ." ,withdraw ,amount) ;
       }else {
           System.out.println("You cannot withdraw your amount is less than 100.") ;
       }
   }
   
   static void handleDeposit(int amount ) { 
       Scanner sc = new Scanner(System.in) ;
       System.out.println("Ensure You Deposit amount less than equal to 10000000.") ;
       System.out.print("Enter Amount ... ") ; 
       int Deposit = sc.nextInt() ;
       if(Deposit <= 1000000){
       amount += Deposit ;
     System.out.printf("You have  creaded amount %d , Your Current amount is %d ." , Deposit ,amount)  ;
       }
   } 
   
   static void handleCheckBalance(int amount ){
    System.out.printf(" Your Current amount is %d. " , amount)  ;
   }
   
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in) ;
        int amount = 500 ;
        System.out.println("STATE BANK OF INDIA");
        System.out.println("Select Transaction:");
        System.out.println("1. Withdraw");
        System.out.println("2. Deposit");
        System.out.println("3. Check Balance");
        System.out.println("4. Exit");
        int choice  = sc.nextInt() ; 
        switch(choice) {
            case 1 :
                handleWithdraw(amount) ;
                break ;
            case 2 :
                handleDeposit(amount) ;
                break ;
            case 3 :
                 handleCheckBalance(amount) ;
                break ;
            case  4:
                System.out.println(" Thank you Goodbye!") ;
                break ;
            default :
            System.out.println("Invalid Choice . Please Try Again.") ;
        }
    }
}
