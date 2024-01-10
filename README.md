package projetoecommerce;

import java.util.Scanner;

public class Main {
	    public static void main(String[] args) {
	        Scanner scanner = new Scanner(System.in);
	        funcionario funcionario = null;

	        while (true) {
	            exibirMenu();

	            int opcao = scanner.nextInt();
	            scanner.nextLine(); // Consumir a quebra de linha

	            switch (opcao) {
	                case 1:
	                    System.out.print("Digite o nome do funcionário: ");
	                    String nome = scanner.nextLine();

	                    System.out.print("Digite o salário por hora: ");
	                    double salarioPorHora = scanner.nextDouble();

	                    System.out.print("Digite as horas trabalhadas: ");
	                    int horasTrabalhadas = scanner.nextInt();

	                    funcionario = new funcionariohorista(nome, salarioPorHora, horasTrabalhadas);
	                    break;

	                case 2:
	                    if (funcionario != null) {
	                        funcionario.calcularSalario();
	                        funcionario.exibirDetalhes();
	                    } else {
	                        System.out.println("Crie um funcionário primeiro.");
	                    }
	                    break;

	                case 3:
	                    System.out.println("Saindo do programa. Até logo!");
	                    System.exit(0);
	                    break;

	                default:
	                    System.out.println("Opção inválida. Tente novamente.");
	                    break;
	            }
	        }
	    }

	    private static void exibirMenu() {
	        System.out.println("\n===== Menu Principal =====");
	        System.out.println("1. Criar Funcionário");
	        System.out.println("2. Calcular Salário");
	        System.out.println("3. Sair");
	        System.out.print("Escolha uma opção: ");
	    }
	

	
		
}


