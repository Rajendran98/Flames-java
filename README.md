import java.io.*;

import java.util.*;

public class Main
{

 public static void main(String[] args) {
 
    Scanner sc = new Scanner(System.in); 
    
    System.out.println("ENTER YOUR NAME:");
    String name1 = sc.nextLine();
    System.out.println("ENTER YOUR PARTNER NAME");
    String name2 = sc.nextLine();
    for (int i = 0; i < name1.length(); i++) {
        for (int j = 0; j < name2.length(); j++) {
            if (name1.charAt(i) == name2.charAt(j)) {
            name1 = name1.replaceFirst(String.valueOf(name1.charAt(i)), "#");
            name2 = name2.replaceFirst(String.valueOf(name2.charAt(j)), "#");
            }
        }
    }
   
    String result = name1 + name2;
    
    result = result.replaceAll("#", "");
    
    int resultLength = result.length();

    String baseInput = "flames";
    int temp;
    temp =   resultLength % baseInput.length();
    System.out.println("Relation Between you and your partner is:");

    switch (temp) {
        case 1:
            System.out.println("friendship");
            break;
        case 2:
            System.out.println("Lovers");
            break;
        case 3:
            System.out.println("Affection");
            break;
        case 4:
            System.out.println("Marriage");
            break;
        case 5:
            System.out.println("Enemity");
            break;
        case 6:
            System.out.println("Siblings");
            break;
        default:
            System.out.println("Last varai kum nee single tha");
            break;
    }
}

}
