# CC2

package ms;

import java.util.Scanner;
public class Ms {

   public static void main(String[] args) {
        of();
        }
     public static void of(){
Scanner sc = new Scanner(System.in);
    System.out.print("Give an odd number: ");
    int n = sc.nextInt();
     
    if (n % 2 == 0){
         System.out.println("It's an Even Number, Pls input the right number\n");
         of();
    }else{
        
    int a = n*(n*n+1)/2;
   
    System.out.println("Sum of each row or column "+a);
    
    System.out.println("\n======Magic Square======\n");
    int[][] magicSquare = new int[n][n];

    int number = 1;
    int row = 0;
    int column = n / 2;
    int curr_row;
    int curr_col;
    while (number <= n * n) {
        magicSquare[row][column] = number;
        number++;
        curr_row = row;
        curr_col = column;
        row -= 1;
        column += 1;
        
        if (row == -1) {
            row = n - 1;
        }
        if (column == n) {
            column = 0;
        }
        if (magicSquare[row][column] != 0) {
            row = curr_row + 1;
            column = curr_col;
            if (row == -1) {
                row = n - 1;
                System.out.printf("%6d ", a);
            }
        }
    }
    for (int i = 0; i < magicSquare.length; i++){
        for (int j = 0; j < magicSquare.length; j++) {
           
            System.out.printf("%6d", magicSquare[i][j]);
   
        }
        String eut = "=";
        System.out.printf("%6d",a);
        System.out.println();
        
          }
  
for(int g=0 ;g <=magicSquare.length; g++){
    System.out.printf("%6d",a);
}
   }
    
    firsst();
    }public static void firsst() {
     Scanner sc = new Scanner(System.in);
     
        System.out.println("\n\nWould you like to try again??\n"
                + "[1] Yes\n"
                + "[2] No");
        int ans = sc.nextInt();
         switch(ans){
        case 1:
            of();
        	break;
        default:
            System.out.println("Thank you have a nice day");
            System.exit(0);
        	break;
         }
             
    }
   
}
