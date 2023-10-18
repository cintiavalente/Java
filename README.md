import java.util.Scanner;

public class TheFirst {
    public static void main(String[] args) {
        //Armazenar os dados com variaveis
        String nome = "Cintia Matos";
        String tipoConta = "Corrente";
        double saldo = 150000.99;

        System.out.println("*************");
        System.out.println("\nNome do Cliente " + nome);
        System.out.println("*************");
        System.out.println("Tipo Conta " + tipoConta);
        System.out.println("Saldo " + saldo);
        System.out.println("\n*************");

        String menu = """
                ** Digite sua opcao **
                1 - Consultar Saldo
                2 - Transferir Valor
                3 - Receber Valor
                4 - Sair
                """;
        Scanner leitura = new Scanner(System.in);
        int opcao = 0;
        while (opcao != 4){
            System.out.println(menu);
            opcao = leitura.nextInt();

            if(opcao ==1){
                System.out.println("Saldo Atualizado " + saldo);
            } else if (opcao ==2){
                System.out.println("Valor a Transferir");
                double valor = leitura.nextInt();
                if (valor > saldo){
                    System.out.println("Nao ha saldo");
                } else {
                    saldo -= valor;
                    System.out.println("Novo Saldo: " + saldo);
                }
            } else if (opcao ==3) {
                System.out.println("Valor Recebido: " );
                double valor = leitura.nextInt();
                saldo += valor;
                System.out.println("Novo Saldo: " + saldo);

            } else if (opcao !=4) {
                System.out.println("Opcao Invalida2");
            }

        }
    }
}

