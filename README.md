import java.util.Scanner;

public class SistemaEscolar {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double[] notas = new double[8];
        double media1Bimestre, media2Bimestre, media3Bimestre, media4Bimestre;
        double media1Semestre, media2Semestre, mediaFinal;

        System.out.println("=== SISTEMA ESCOLAR ===");
        System.out.println("Digite as 8 notas anuais:");

        // Entrada das 8 notas
        for (int i = 0; i < 8; i++) {
            System.out.print("Nota " + (i + 1) + ": ");
            notas[i] = entrada.nextDouble();
        }

        // Cálculo das médias bimestrais
        media1Bimestre = (notas[0] + notas[1]) / 2;
        media2Bimestre = (notas[2] + notas[3]) / 2;
        media3Bimestre = (notas[4] + notas[5]) / 2;
        media4Bimestre = (notas[6] + notas[7]) / 2;

        // Cálculo das médias semestrais
        media1Semestre = (media1Bimestre + media2Bimestre) / 2;
        media2Semestre = (media3Bimestre + media4Bimestre) / 2;

        // Cálculo da média final
        mediaFinal = (media1Semestre + media2Semestre) / 2;

        // Saída formatada dos resultados
        System.out.println("\n=== RESULTADOS ===");
        System.out.printf("1º Bimestre: %.1f%n", media1Bimestre);
        System.out.printf("2º Bimestre: %.1f%n", media2Bimestre);
        System.out.printf("1º Semestre: %.1f%n", media1Semestre);
        System.out.println("----------------------");
        System.out.printf("3º Bimestre: %.1f%n", media3Bimestre);
        System.out.printf("4º Bimestre: %.1f%n", media4Bimestre);
        System.out.printf("2º Semestre: %.1f%n", media2Semestre);
        System.out.println("----------------------");
        System.out.printf("Média Final: %.1f%n", mediaFinal);

        entrada.close();
    }
}
