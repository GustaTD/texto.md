Introdução
Na programação, os paradigmas imperativo e declarativo representam duas abordagens distintas para resolver problemas computacionais. O paradigma imperativo é focado em como o problema deve ser resolvido, ou seja, descreve um conjunto de instruções que modificam o estado do sistema até que o objetivo seja alcançado. Já o paradigma declarativo, enfatiza o que deve ser alcançado, sem especificar como o programa deve atingir esse resultado.

Paradigma Imperativo
O paradigma imperativo segue uma abordagem sequencial de comandos, nos quais o programador especifica de forma explícita os passos necessários para alcançar um objetivo. Isso envolve controle de fluxo, manipulação de variáveis e execução de funções. Linguagens como Java, C e Python utilizam esse estilo de programação.

Paradigma Declarativo
Por outro lado, o paradigma declarativo foca em descrever a lógica ou o resultado desejado, sem se preocupar com os detalhes do controle de fluxo ou da sequência de execução. Linguagens como SQL, Haskell e Prolog são exemplos de linguagens declarativas, nas quais a programação envolve a declaração de relações e a solução do problema sem detalhar explicitamente como ela deve ser resolvida.

Comparação entre Java e Prolog
Vamos comparar dois trechos de código que resolvem o mesmo problema: verificar se um número é par.

Código Java (Paradigma Imperativo)
public class Main {
    public static void main(String[] args) {
        int numero = 4;
        if (numero % 2 == 0) {
            System.out.println("O número é par");
        } else {
            System.out.println("O número é ímpar");
        }
    }
}

Explicação do código Java:

O código em Java segue a abordagem imperativa, onde o programador define explicitamente os passos a serem seguidos.

A primeira linha declara a variável numero com o valor 4.

Em seguida, o programa verifica se o número é divisível por 2 (numero % 2 == 0). Se a condição for verdadeira, imprime que o número é par. Caso contrário, imprime que o número é ímpar.

O código descreve claramente as instruções necessárias para resolver o problema.

Código Prolog (Paradigma Declarativo)
par(X) :- X mod 2 =:= 0.

?- par(4).

Explicação do código Prolog:

O código em Prolog segue o paradigma declarativo, onde a solução é declarada em termos de fatos e regras.

A regra par(X) :- X mod 2 =:= 0. define que um número X é par se o resto da divisão de X por 2 for igual a zero. Não há necessidade de controle de fluxo ou de especificar como a verificação deve ser feita.

A consulta ?- par(4). pede ao Prolog para verificar se o número 4 é par, e a resposta será true, pois 4 é divisível por 2.

Comparação de Abordagens
Controle de Fluxo: O código Java usa uma estrutura condicional if-else para determinar se o número é par, enquanto o Prolog define uma relação entre números e a propriedade de ser par, sem especificar como a verificação deve ocorrer.

Declaração vs Instrução: No Java, o programador descreve explicitamente os passos necessários para atingir o objetivo. Em Prolog, o programador declara que a condição "ser par" é baseada em uma regra matemática (divisão por 2 sem resto) e deixa que o sistema de inferência de Prolog faça a busca pela solução.

Abstração: Prolog permite uma maior abstração ao esconder detalhes sobre o processo de execução, permitindo que o programador se concentre apenas nas relações lógicas. O Java, por ser imperativo, exige que o programador se preocupe com os detalhes da execução, como o controle de fluxo.
