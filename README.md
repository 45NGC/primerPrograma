# primerPrograma
/*INTRODUCIR DOS FRASES DE MISMA LONGITUD Y COMPROBAR QUE CARACTERES COINCIDEN EN LA MISMA POSICION EN AMBAS FRASES*/

import java.util.Scanner;
public class CompararLetraPosicion {
	public static void main(String[] args) {
		Scanner ent=new Scanner(System.in);
		int otro=0;
		
		do {
			
			String frase1="";
			String frase2="";
			char caracter1=' ',caracter2=' ';
			int i=0;
			
			//INTRODUCIR DOS FRASES CON LA MISMA LONGITUD
			
			do {
				System.out.println("Introduza la frase 1");
				frase1=ent.nextLine().toUpperCase();
				System.out.println("Introduza la frase 2");
				frase2=ent.nextLine().toUpperCase();
			}while(frase1.length()!=frase2.length());
			
			//COMPROBAR SI LOS CARACTERES SON IGUALES Y EN QUE POSICION SE ENCUENTRAN
			
			System.out.println("FRASE 1 : "+frase1);
			System.out.println("FRASE 2 : "+frase2);
			System.out.println();
			System.out.println("CARACTER			POSICIÓN");
			
			for(i=0;i<frase1.length();i++) {
				
				caracter1=frase1.charAt(i);
				caracter2=frase2.charAt(i);
				
				if(caracter1==caracter2) {
					System.out.println(caracter1+"				"+i);
				}
			}
			
			System.out.println();
			
			//DAR OPCION DE REALIZAR OTRA OPERACION
			ent.nextLine();
			do {
				System.out.println("Realizar otra operacion(1=si/0=no)");
				otro=ent.nextInt();
			}while(otro!=1 && otro!=0);
			
				
		}while (otro==1);	
		System.out.println("FIN DEL PROGRAMA");
		ent.close();
	}
}
