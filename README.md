# Exerc-ciosClasseseObjetos

# CLASSE PAI (MAIN)


package exercíciosclasseseobjetos;


public class ExercíciosClassesEObjetos {

    
    public static void main(String[] args) {
        
         // Exercicio 1: Pessoa
        Pessoa pessoa = new Pessoa("Douglas", 25, "analista de dados");
        pessoa.exibirDetalhes();

        System.out.println("\n");

        // Exercicio 2: Conta Bancária
        ContaBancaria conta = new ContaBancaria("Dunga", "12345-6");
        conta.depositar(500);
        conta.sacar(200);
        conta.exibirSaldo();

        System.out.println("\n");

        // Exercicio 3: Carro
        Carro carro = new Carro("Fiat", "Palio", 2020);
        carro.acelerar(50);
        carro.desacelerar(20);

        System.out.println("\n");

        // Exercicio 4: Livro
        Livro livro = new Livro("O Senhor dos Anéis", "J.R.R. Tolkien", 1000, 3);
        livro.emprestar();
        livro.devolver();

        System.out.println("\n");

        // Exercicio 5: Retângulo
        Retangulo retangulo = new Retangulo(5, 7);
        System.out.println("Área: " + retangulo.calcularArea());
        System.out.println("Perímetro: " + retangulo.calcularPerimetro());

        System.out.println("\n");

        // Exercicio 6: Contador
        Contador contador = new Contador(0);
        contador.incrementar();
        contador.incrementar();
        contador.decrementar();

        System.out.println("\n");

        // Exercicio 7: Estudante
        Estudante estudante = new Estudante("Douglas", 26);
        estudante.adicionarDisciplina("Matemática");
        estudante.adicionarDisciplina("Física");
        estudante.exibirDisciplinas();
        
        
    }
    
}

#  Exercício 1: Criando uma Classe simples


package exercíciosclasseseobjetos;


public class Pessoa {
    
      String nome;
    int idade;
    String profissao;

    Pessoa(String nome, int idade, String profissao) {
        this.nome = nome;
        this.idade = idade;
        this.profissao = profissao;
    }

    void exibirDetalhes() {
        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade);
        System.out.println("Profissão: " + profissao);
    }
    
}


# Exercício 2: Conta Bancária



package exercíciosclasseseobjetos;


public class ContaBancaria {
    
     String titular;
    double saldo;
    String numeroConta;

    ContaBancaria(String titular, String numeroConta) {
        this.titular = titular;
        this.numeroConta = numeroConta;
        this.saldo = 0.0;
    }

    void depositar(double valor) {
        saldo += valor;
        System.out.println("Depósito de " + valor + " realizado. Novo saldo: " + saldo);
    }

    void sacar(double valor) {
        if (saldo >= valor) {
            saldo -= valor;
            System.out.println("Saque de " + valor + " realizado. Novo saldo: " + saldo);
        } else {
            System.out.println("Saldo insuficiente.");
        }
    }

    void exibirSaldo() {
        System.out.println("Saldo atual: " + saldo);
    }
}


# Exercício 3: Carro


package exercíciosclasseseobjetos;


public class Carro {
    
     String marca;
    String modelo;
    int ano;
    int velocidade;

    Carro(String marca, String modelo, int ano) {
        this.marca = marca;
        this.modelo = modelo;
        this.ano = ano;
        this.velocidade = 0;
    }

    void acelerar(int incremento) {
        velocidade += incremento;
        System.out.println("Acelerando. Velocidade atual: " + velocidade);
    }

    void desacelerar(int decremento) {
        if (velocidade >= decremento) {
            velocidade -= decremento;
            System.out.println("Desacelerando. Velocidade atual: " + velocidade);
        } else {
            System.out.println("Não é possível desacelerar abaixo de 0.");
        }
    }
}


# Exercício 4: Livro


package exercíciosclasseseobjetos;


public class Livro {
    
     String titulo;
    String autor;
    int numeroPaginas;
    int exemplaresDisponiveis;

    Livro(String titulo, String autor, int numeroPaginas, int exemplaresDisponiveis) {
        this.titulo = titulo;
        this.autor = autor;
        this.numeroPaginas = numeroPaginas;
        this.exemplaresDisponiveis = exemplaresDisponiveis;
    }

    void emprestar() {
        if (exemplaresDisponiveis > 0) {
            exemplaresDisponiveis--;
            System.out.println("Livro emprestado. Exemplares disponíveis: " + exemplaresDisponiveis);
        } else {
            System.out.println("Nenhum exemplar disponível para empréstimo.");
        }
    }

    void devolver() {
        exemplaresDisponiveis++;
        System.out.println("Livro devolvido. Exemplares disponíveis: " + exemplaresDisponiveis);
    }
    
}


# Exercício 5: Retângulo


package exercíciosclasseseobjetos;


public class Retangulo {
    
     double largura;
    double altura;

    Retangulo(double largura, double altura) {
        this.largura = largura;
        this.altura = altura;
    }

    double calcularArea() {
        return largura * altura;
    }

    double calcularPerimetro() {
        return 2 * (largura + altura);
    }
    
}


# Exercício 6: Contador



package exercíciosclasseseobjetos;


public class Contador {
    
     int valor;

    Contador(int valorInicial) {
        this.valor = valorInicial;
    }

    void incrementar() {
        valor++;
        System.out.println("Valor incrementado: " + valor);
    }

    void decrementar() {
        valor--;
        System.out.println("Valor decrementado: " + valor);
    } 
    
}

# Exercício 7: Estudante 



package exercíciosclasseseobjetos;

import java.util.ArrayList;


public class Estudante {
    
    String nome;
    int idade;
    ArrayList<String> disciplinas;

    Estudante(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
        this.disciplinas = new ArrayList<>();
    }

    void adicionarDisciplina(String disciplina) {
        disciplinas.add(disciplina);
        System.out.println("Disciplina " + disciplina + " adicionada.");
    }

    void exibirDisciplinas() {
        System.out.println("Disciplinas matriculadas: " + disciplinas);
    }
    
}









