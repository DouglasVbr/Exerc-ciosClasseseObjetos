# Exerc-ciosClasseseObjetos

package exercícios.classes.e.objetos;

/**
 *
 * @author Douglas Vieira
 */
public class ExercíciosClassesEObjetos {

    public static void main(String[] args) {

        Funcionario funcionario = new Funcionario("Douglas Vieira", 25, "Desenvolvedor", 5000.00);

        System.out.println(funcionario.exibirDetalhes());

        //exercicio2
        ContaBancaria minhaConta = new ContaBancaria("Douglas Vieira", 1000.00, "12345-6");

        System.out.println("Saldo inicial:" + minhaConta.getSaldo());

        minhaConta.depositar(500.00);
        minhaConta.sacar(200.00);
        minhaConta.sacar(1500.00);

        System.out.println("Saldo final:" + minhaConta.getSaldo());

        //exercicio3
        Carro meuCarro = new Carro("Toyota", "cololla", 2023);

        System.out.println("Marca" + meuCarro.getMarca());
        System.out.println("Modelo" + meuCarro.getModelo());
        System.out.println("Ano" + meuCarro.getAno());
        System.out.println("Velocidade inicial:" + meuCarro.getVelocidade() + "km/h");

        meuCarro.acelerar(50.00);
        meuCarro.acelerar(30.00);
        System.out.println("Velocidade após aceleração" + meuCarro.getVelocidade() + "km/h");

        meuCarro.desacelerar(20.00);
        System.out.println("Velocidade após desaceleração:" + meuCarro.getVelocidade() + "km/h");

        meuCarro.desacelerar(70.00);
        System.out.println("Velocidade final:" + meuCarro.getVelocidade() + "km/h");
    
    
        //exercicio4
        
    
    }

}

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package exercícios.classes.e.objetos;

/**
 *
 * @author aluno.saolucas
 */
public class ContaBancaria {

    private String titular;
    private double saldo;
    private String Nconta;

    public ContaBancaria(String titular, double saldo, String Nconta) {
        this.titular = titular;
        this.saldo = saldo;
        this.Nconta = Nconta;
    }

    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
            System.out.println("Deposito de " + valor + "realizado com sucesso!");
        } else {
            System.out.println("Valor de deposito deve ser positivo.");

        }
    }

    public void sacar(double valor) {
        if (valor > 0 && valor <= saldo) {
            saldo -= valor;
            System.out.println("Saque de " + valor + "realizado com sucesso.");
        } else if (valor > saldo) {
            System.out.println("Saldo insuficiente para realizar o saque.");
        }else{
            System.out.println("Valor do saque deve ser positivo.");
        }
    }
    
    public double getSaldo(){
        return saldo;
    }

    public String getTitular() {
        return titular;
    }

    public String getNconta() {
        return Nconta;
    }
    

}


package exercícios.classes.e.objetos;

/**
 *
 * @author aluno.saolucas
 */
public class Funcionario extends Pessoa {

    private double salario;

   public Funcionario(String nome, int idade, String Profissao, double Salario ){
       super(nome, idade, Profissao);
       this.salario = salario;
   }

    public double getSalario() {
        return salario;
    }

    public void setSalario(double salario) {
        this.salario = salario;
    }
   
   @Override
   public String exibirDetalhes(){
   
       return String.format("%s\Salário: R$%.2f", super.exibirDetalhes(), salario);
   
   }
    
}

package exercícios.classes.e.objetos;

public class Carro {

    private String marca;
    private String modelo;
    private int ano;
    private double velocidade;
    String getMarca;

    public Carro(String marca, String modelo, int ano, double velocidade) {
        this.marca = marca;
        this.modelo = modelo;
        this.ano = ano;
        this.velocidade = velocidade;
    }

    public void acelerar(double incremento) {
        if (incremento > 0) {
            velocidade += incremento;
            System.out.println("Acelerou em " + incremento + "km/h.");
        } else {
            System.out.println("Incremento de aceleração deve ser positivo.");

        }
    }

    public void desacelerar(double decremento) {
        if (decremento <= velocidade) {
            velocidade -= decremento;
            System.out.println("Desacelerou em" + decremento + "km/h.");
        } else {
            velocidade = 0;
            System.out.println("Velocidade não pode ser negativa. Carro parado. ");
        }
    }

    
    
        else{
            System.out.println("Decremento de desaceleração deve ser positivo. ");
            
         

    public double getVelocidade() {
        return velocidade;
    }

    public String getMarca() {
        return marca;
    }

    public String getModelo() {
        return modelo;
    }

    public int getAno() {
        return ano;

    }

}



package exercícios.classes.e.objetos;


public class Pessoa {
    
    private String nome;
    private int idade;
    private String Profissao;
    
    
    public Pessoa(String nome, int idade, String Profissao){
    
        this.nome = nome;
        this.idade = idade;
        this.Profissao = Profissao;
    }
    
    public String getNome(){
    return nome;
    
    }
    
    public int getIdade(){
    
        return idade;
    }
    
    public void setIdade(int idade){
    this.idade = idade;
    }
    
    public String getProfissao(){
    return Profissao;
    }
    
    public void setProfissao(String Profissao){
    this.Profissao = Profissao;
    }
    
    public String exibirDetalhes(){
    return String.format("Nome: %s\nIdade: %d\nProfissão: %s", nome, idade, Profissao);
    }
}








