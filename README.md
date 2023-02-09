# Comp-11.1

import java.util.Scanner;
public class Comp111 {

    public static void main(String[] args) throws StringTooLongException{
        Scanner input = new Scanner(System.in);
        String newString = "";
        System.out.println("enter string or done when finished");
        String userInput = input.nextLine();
        while(!userInput.equalsIgnoreCase("DONE")){
        	if(userInput.length()>=20){
        		throw new StringTooLongException();
        	}
        	newString+=userInput+" \t";
        	userInput = input.nextLine();
        }
        System.out.println("The letters are :");
        System.out.print(newString);
    }
}
