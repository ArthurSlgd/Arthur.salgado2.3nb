//MENU
package br.com.fecaf.controller;
import br.com.fecaf.model.Circulo;
import br.com.fecaf.model.Retangulo;
import br.com.fecaf.model.Triangulo;

import java.util.Scanner;

public class Menu {


    Scanner scanner = new Scanner(System.in);

    public void executarMenu() {

        boolean exit = false;
        Circulo circulo = new Circulo();
        while (!exit) {

            System.out.println("/************************/");
            System.out.println("/*      Geometria       */");
            System.out.println("/************************/");
            System.out.println("/* 1 - Circulo          */");
            System.out.println("/* 2 - Retângulo        */ ");
            System.out.println("/* 3 - Triângulo        */");
            System.out.println("/* 4 - Sair             */");
            System.out.println("/************************/");
            System.out.print("Informe a opção desejada:");

            int optionUser = scanner.nextInt();

            switch (optionUser) {
                case 1:

                    boolean exitCirculo = false;

                    boolean validaCadastro = false;

                    while (!exitCirculo) {

                        System.out.println("/*************************/");
                        System.out.println("/*        Circulo        */");
                        System.out.println("/*************************/");
                        System.out.println("/* 1 - Cadastrar Circulo */");
                        System.out.println("/* 2 - Calcular Area     */");
                        System.out.println("/* 3 -Calcular Perimetro */");
                        System.out.println("*/ 4 - Sair              */");
                        System.out.println("/*************************/");

                        System.out.print("Escolha uma opção: ");

                        int optionCirculo = scanner.nextInt();



                        switch (optionCirculo) {
                            case 1:
                                System.out.println("Cadastrando Circulo...");
                                validaCadastro = circulo.cadastrarCirculo();
                                break;
                            case 2:
                                if (validaCadastro) {
                                    System.out.println("Calculando Área");
                                    circulo.calcularArea();
                                } else {
                                    System.out.println("Cadastre um Circulo..");
                                }
                                break;
                            case 3:
                                if (validaCadastro) {
                                    System.out.println("Calculando Perimetro...");
                                    circulo.calcularPerimetro();
                                }else {
                                    System.out.println("Cadastre um Circulo..");
                                }
                                break;
                            case 4:
                                System.out.println("Voltando para Menu...");
                                exitCirculo = true;
                                break;
                            default:
                                System.out.println("Opção Inválida...");
                        }

                    }
                    break;
                case 2:
                    boolean exitRetangulo = false;
                    Retangulo retangulo = new Retangulo();
                    boolean validaRetangulo = false;

                    while (!exitRetangulo){
                        System.out.println("/*************************/");
                        System.out.println("/*      Retângulo        */");
                        System.out.println("/*************************/");
                        System.out.println("/*1 - Cadastrar Retângulo*/");
                        System.out.println("/* 2 - Calcular Area     */");
                        System.out.println("/* 3 -Calcular Perimetro */");
                        System.out.println("/* 4 - Definir Quadrado  */");
                        System.out.println("*/ 5 - Sair              */");
                        System.out.println("/*************************/");

                        System.out.print("Escolha uma opção: ");

                        int optionRetangulo = scanner.nextInt();

                        switch (optionRetangulo) {
                            case 1:
                                System.out.println("/*************************/");
                                System.out.println("/* Cadastrando Retângulo */");
                                System.out.println("/*************************/");
                                validaRetangulo = retangulo.cadastrarRetangulo();
                                System.out.println("/*************************/");

                                break;
                            case 2:
                                if (validaRetangulo) {
                                    System.out.println("Calculando Área");
                                    retangulo.calcularArea();
                                } else {
                                    System.out.println("Cadastre um Retângulo...");
                                }
                                break;
                            case 3:
                                if (validaRetangulo) {
                                    System.out.println("Calculando Perimetro...");
                                    retangulo.calcularPerimetro();
                                }else {
                                    System.out.println("Cadastre um Retângulo...");
                                }
                                break;
                            case 4:
                                System.out.println("/**  Definindo quadrado  **/");
                                if(validaRetangulo) {
                                    retangulo.validarQuadrado();
                                    }
                                break;
                            case 5:
                                System.out.println("Saindo...");
                                exitRetangulo = true;
                                break;
                            default:
                                System.out.println("Esscolha uma opção válida...");



                        }



                    }
                    break;
                case 3:
                    boolean exitTriangulo = false;
                    Triangulo triangulo = new Triangulo();
                    boolean validaTriangulo = false;

                    while (!exitTriangulo){
                        System.out.println("/*************************/");
                        System.out.println("/*      Triângulo        */");
                        System.out.println("/*************************/");
                        System.out.println("/*1 - Cadastrar Triângulo*/");
                        System.out.println("/* 2 - Calcular Area     */");
                        System.out.println("/* 3 -Calcular Perimetro */");
                        System.out.println("/* 4 - Definir Triângulo */");
                        System.out.println("/* 5 - Definir Triângulo Retângulo */");
                        System.out.println("/* 6 - Definir Triângulo 3-4-5  */");
                        System.out.println("*/ 7 - Sair              */");
                        System.out.println("/*************************/");

                        System.out.print("Escolha uma opção: ");

                        int optionTriangulo = scanner.nextInt();

                        switch (optionTriangulo) {
                            case 1:
                                System.out.println("/*************************/");
                                System.out.println("/* Cadastrando Triângulo */");
                                System.out.println("/*************************/");
                                validaTriangulo = triangulo.cadastrarTriangulo();
                                System.out.println("/*************************/");
                                break;
                            case 2:
                                if (validaTriangulo) {
                                    System.out.println("Calculando Área");
                                    triangulo.calcularArea();
                                } else {
                                    System.out.println("Cadastre um Triângulo...");
                                }
                                break;
                            case 3:
                                if (validaTriangulo) {
                                    System.out.println("Calculando Perimetro...");
                                    triangulo.calcularPerimetro();
                                } else {
                                    System.out.println("Cadastre um Triângulo...");
                                }
                                break;
                            case 4:
                                System.out.println("/**  Definindo Tipo  **/");
                                if (validaTriangulo) {
                                    triangulo.definirTipo();
                                }
                                break;
                            case 5:
                                if (validaTriangulo) {
                                    if (triangulo.ehTrianguloRetangulo()) {
                                        System.out.println("O triângulo é retângulo PORRA");
                                    } else {
                                        System.out.println("O triângulo não é retângulo PORRA");
                                    }
                                } else {
                                    System.out.println("Cadastre um Triângulo primeiro");
                                }
                                break;
                            case 6:
                                System.out.println("/* Verificando se é '3-4-5' */");
                                if (validaTriangulo) {
                                    if (triangulo.ehTriangulo345()) {
                                        System.out.println("O triângulo ta no método 3-4-5");
                                    } else {
                                        System.out.println("O triângulo NÃO ta no método 3-4-5.");
                                    }
                                } else {
                                    System.out.println("Cadastre um Triângulo primeiro...");
                                }
                                break;
                            case 7:
                                System.out.println("Saindo...");
                                exitTriangulo = true;
                                break;
                            default:
                                System.out.println("Escolha uma opção valida... ");
                        }
                    }

                    break;
                case 4:
                    System.out.println("Saindo ....");
                    exit = true;
                    break;
                default:
                    System.out.println("Opção Inválida...");
            }

        }
    }
}


//Geometria

package br.com.fecaf;

import br.com.fecaf.controller.Menu;
import br.com.fecaf.model.Circulo;
import br.com.fecaf.model.Retangulo;
import br.com.fecaf.model.Triangulo;

public class Geometria {
    public static void main(String[] args) {
        Menu menu = new Menu();
        menu.executarMenu();




    }
}



//CIRCULO

package br.com.fecaf.model;
import java.util.Scanner;

public class Circulo {
    public double raio,area, perimetro, diametro;

    Scanner scanner = new Scanner(System.in);

    public boolean cadastrarCirculo () {
        System.out.println("/***********************/");
        System.out.println("/*  Cadastro Circulo   */");
        System.out.println("/***********************/");
        System.out.println("Informe o raio: ");
        raio = scanner.nextDouble();
        System.out.println("Circulo Cadastrado com Sucesso");
        System.out.println("/***********************/");

        return true;
    }
    public void exibirCIrculo () {
        System.out.println("/***********************/");
        System.out.println("O raio do circilo é: " + raio );
        System.out.println("A area do circulo é: " + area);
        System.out.println("O perimetro do circulo é: " + perimetro);
        System.out.println("O diametro do circulo é: " + diametro);
        System.out.println("/***********************/");

    }
    public void calcularArea() {
        System.out.println("/*    Calculando Area    */");
        area = Math.PI * Math.pow(raio, 2);
        System.out.println(area);



    }
    public void calcularPerimetro () {
        System.out.println("/*    Calculando Perimetro    */");
        perimetro = 2 * Math.PI * raio;


    }
}

// RETANGULo


package br.com.fecaf.model;

import java.util.Scanner;

public class Retangulo {
    public double lado1, lado2, area, perimetro;

    Scanner scanner = new Scanner(System.in);

    public boolean cadastrarRetangulo () {
        System.out.println("/************************/");
        System.out.println("/*  Cadastro Retangulo  */");
        System.out.println("/************************/");
        System.out.println("Informe o lado 1: ");
        lado1 = scanner.nextDouble();
        System.out.println("Informe o lado 2: ");
        lado2 = scanner.nextDouble();
        System.out.println("/************************/");
        return true;

    }

    public void exibirRetangulo () {
        System.out.println("/*** Exibir Retangulo ***/");
        System.out.println("O lado 1 é: " + lado1);
        System.out.println("O lado 2 é: " + lado2);
        System.out.println("A area é: " + area);
        System.out.println("O perimetro é: " + perimetro);


    }

    public void calcularArea () {
        System.out.println("/*** Calculando Area ***/");
        area = lado1 * lado2;
        System.out.println("A area é: " + area);




    }
    public void calcularPerimetro () {
        System.out.println("/*** Calculando Perimetro ***/");
        perimetro = 2 * lado1 + 2 * lado2;
        System.out.println("O perimetro é: " + perimetro);






    }
    public boolean validarQuadrado () {
        System.out.println("/* Definindo se é quadrado */");

        if (lado1 == lado2) {
            System.out.println("é um quadrado!");
            return true;

        }
        return false;




    }





}


// TRIANGULo


package br.com.fecaf.model;
import java.util.Arrays;
import java.util.Scanner;

public class Triangulo {
    public double base, altura, lado2, lado3, area, perimetro;

    Scanner scanner = new Scanner(System.in);

    public boolean cadastrarTriangulo (){
        System.out.println("/**************************/");
        System.out.println("/**  Cadastrar Triângulo **/");
        System.out.println("/**************************/");
        System.out.println("/* Informe a Base:        */");
        base = scanner.nextDouble();
        System.out.println("/* Informe o Lado 2:      */");
        lado2 = scanner.nextDouble();
        System.out.println("/* Informe o Lado 3:      */");
        lado3 = scanner.nextDouble();
        System.out.println("/* Informe a Altura:      */");
        altura = scanner.nextDouble();

        return true;

    }



    public void calcularArea() {
        System.out.println("/**************************/");
        System.out.println("/**     Calculando  Area **/");
        System.out.println("/**************************/");

        area = (base * altura) / 2;
        System.out.println("A area é: " + area);
        System.out.println("/**************************/");

    }

    public void calcularPerimetro () {
        System.out.println("/**************************/");
        System.out.println("/*  Calculando Parimetro  */");
        System.out.println("/**************************/");
        perimetro = base + lado2 + lado3;
        System.out.println("Seu perimetro é " + perimetro);
        System.out.println("/**************************/");

    }


    // equilatero escaleno isosceles

    public void definirTipo () {
        System.out.println("/**************************/");
        System.out.println("/*Definindo Tipo Triangulo*/");
        System.out.println("/**************************/");

        if (base == lado2 && base == lado3) {
            System.out.println("Esse triângulo é equilatero...");
        } else if (base != lado2 &&  base != lado3 && lado2 != lado3) {
            System.out.println("Esse Triângulo é Escaleno...");
        } else {
            System.out.println("Esse Triângulo é Isosceles");
        }


    }
    // depois dessa linha eu tive que pesquisar bastante coisa pq tudo que eu tentava dava errado - então vou explicar oq eu entendi

    // antes de tudo importei a bliblioteca de array do java
    // depois eu criei uma array que serve pra organizar os itens em ordem crescente
    // dessa forma cateto1 sempre sera a base, c2 sempre sera o lado2 e hipotenusa sempre sera o lado3
    // e por ultimo o calculo padrão da hipotenusa q é A^2 + B^2 = C^2

    public boolean ehTrianguloRetangulo() {
        double[] lados = {base, lado2, lado3};
        Arrays.sort(lados);
        double cateto1 = lados[0], cateto2 = lados[1], hipotenusa = lados[2];
        return (cateto1 * cateto1 + cateto2 * cateto2) == (hipotenusa * hipotenusa);
    }

    //eu fiquei tentando tantas coisas e no fim é um bgl tão facil que eu fiquei com vontade de atravessar o monitor com meu braço

        // aq eu fiz a mesma coisa doq a de cima, criei a arrays pra organizar em ordem crescente
        // depois disso vem o calculo que mais uma vez era simples mas faz parecer dificil pra quebrar a cabeça
        // fazendo a diferença em ordem decrescente o metodo sempre vai dar certo, se for 3-4-5 -> 5-4=1 | 4-3=1 -> verdadeiro
        // e a mesma coisa com tudo q entrar, a diferença é que caso chegue por exemplo:  5-6-9 -> 9-6=3 | 6-5=1 -> falso
        // o sistema vai reconhecer como false e retorna que n é um triangulo 3-4-5

    public boolean ehTriangulo345() {
        double[] lados = {base, lado2, lado3};
        java.util.Arrays.sort(lados);
        double diferenca1 = lados[1] - lados[0], diferenca2 = lados[2] - lados[1];
        return diferenca1 == diferenca2;
    }
}
