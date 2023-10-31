# Palindrome

package fr.gouv.finances.exo;

import java.util.Arrays;
import java.util.Scanner;

public class exercicePalindrome {

    public static void main(String[] args) {
	String maPhrase;
	int i;
	int j;
	Scanner saisie = new Scanner(System.in);
	maPhrase = saisie.nextLine();
	char[] palin = new char[maPhrase.length()];

	for (i = 0; i < maPhrase.length(); i++) { // Opération pour inverser la chaine de notre phrase.
	    palin[palin.length - 1 - i] = maPhrase.charAt(i); // TROUVER l'emplacement de nos chaines de caractères.

	}

	for (i = 0; i < maPhrase.length(); i++) {
	    if (palin[i] != maPhrase.charAt(i)) {
		System.out.println("Ce n'est pas un palin");
		break;
	    }

	}
	if (i == maPhrase.length()) {
	    System.out.println("C'est un palin");
	}

	System.out.println("Affichez le contenu du tableau " + Arrays.toString(palin) + "\nLa phrase : " + maPhrase);
	saisie.close();

    }
}
