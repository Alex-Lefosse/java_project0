import java.util.Scanner;

public class Vigenere {
    Scanner in = new Scanner(System.in);
    String clear_text = "";
    String verme = "";

    public void insert() {
        Boolean controllo = false;
        System.out.println("insert clear text --> ");
        clear_text = in.nextLine();
        System.out.println("insert verme");
        verme = in.next();
        in.nextLine();
        while (controllo == false) {
            for (int i = 0; i < clear_text.length(); i++) {
                if ((int) clear_text.charAt(i) < 97 || (int) clear_text.charAt(i) > 122) {
                    System.out.println("caratteri validi per il testo in chiaro a-z minuscolo reinserisci testo --> ");
                    clear_text = in.nextLine();
                    i = 0;
                }

            }
            for (int i = 0; i < verme.length(); i++) {
                if ((int) verme.charAt(i) < 97 || (int) verme.charAt(i) > 122) {
                    System.out.println("caratteri validi per il verme a-z minuscolo reinserisci verme --> ");
                    verme = in.next();
                    i = 0;
                }
            }
            controllo = true;
            if (verme.length() > clear_text.length()) {
                System.out.println("verme più lungo della frase in chiaro, reinserire il verme --> ");
                verme = in.next();
                controllo = false;
            }
        }
    }

    public void Cifrario(){
        char temp;
        char temp1;
        String cifrata="";
        for(int i=0; i<clear_text.length(); i++)
        {
            temp=clear_text.charAt(i);
            temp1=verme.charAt(i%(verme.length()-1));
            if((int) temp + (int) temp1 <97 || (int) temp + (int) temp1 >122 ){
                jump=25;
            }
        }
    }
}
