# Estagio_em_Desenvolvimento_Ribeirao_Preto
# Linguagem utilizada: JavaScript



1) Observe o trecho de código abaixo: 

     	int INDICE = 13, SOMA = 0, K = 0; 
    
     	enquanto K < INDICE faça 
    
    	{ 
    
    		K = K + 1; 
    
    		SOMA = SOMA + K; 
    
    	} 
    
     	imprimir(SOMA); 

  

Ao final do processamento, qual será o valor da variável SOMA? 
A soma dos números inteiros de 1 a 13 com o valor final igual a 91



2) Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência. 

        const  pertenceFibonacci = (numero) => {
            let a = 0;
            let b = 1;
        
            while (a <= numero) {
                if (a === numero) {
                    console.log(`${numero} pertence à sequência de Fibonacci.`);
                    return;
                }
        
                let temp = a + b;
                a = b;
                b = temp;
            }
        
            console.log(`${numero} não pertence à sequência de Fibonacci.`);
        }
        
        // Exemplo de uso
        const numeroInformado = 21; // Altere o número conforme necessário
        pertenceFibonacci(numeroInformado);



3) Descubra a lógica e complete o próximo elemento:  

   

a) 1, 3, 5, 7, ___  
A lógica aqui é: inicia-se com 1, e em seguida, o próximo número é igual ao atual somado a 2 (1, 1+2=3, 3+2=5, 5+2=7, 7+2=9).


b) 2, 4, 8, 16, 32, 64, ____  
A lógica aqui é: inicia-se com 2, e em seguida, o próximo número é igual ao atual multiplicado por 2 (2, 2*2=4, 4*2=8, 8*2=16, 16*2=32, 32*2=64, 64*2=128).
Também pode ser interpretada como: O valor atual é igual a 2 elevado a posição atual (2^1 = 2, 2^2 = 4, 2^3 = 8, 2^4 = 16, 2^5 = 32, 2^6 = 64, 2^7 = 128)

c) 0, 1, 4, 9, 16, 25, 36, ____  
A lógica aqui é: o valor da posição atual é igual a posição ao quadrado.(0^2 = 0, 1^2 = 1, 2^2 = 4, 3^2 = 9, 4^2 = 16, 5^2 = 25, 6^2 = 36, 7^2 = 49)

d) 4, 16, 36, 64, ____  
A lógica aqui é: Temos uma sequência com os números pares ao quadrado (2^2 = 4, 4^2 = 16, 6^2 = 36, 8^8 = 64, 10^2 = 100)

e) 1, 1, 2, 3, 5, 8, ____  
A lógica aqui é: Temos uma sequência de Fibonacci onde, neste caso, inicia-se com 1, 1 e  em seguida o valor atual é igual a soma dos dois valores anteriores (1, 1, 1+1 = 2, 1+2 = 3, 2+3 = 5, 3+5 = 8, 5+8 = 13);

f) 2,10, 12, 16, 17, 18, 19, ____  
Os numeros parecem crescer sem padrão fixo, então seguindo o crescimento dos ultimos valores acredito que a sequencia fique(2,10,12,16,17,18,19,20)


4) Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada.

Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?  

Primeira ida:

Ligue o primeiro interruptor por alguns minutos e depois desligue.
Ligue o segundo interruptor.
Entre na sala.
Se a lâmpada estiver acesa, você sabe qual interruptor a controla (o segundo).
Se a lâmpada estiver apagada, mas ainda quente, o primeiro interruptor a controla.
Se a lâmpada estiver apagada e fria, o terceiro interruptor a controla.

Segunda ida:

Desligue os interruptores.
Com apenas dois para identificar.
Ligue um dos interruptores que não foram identificados.
Entre em outra sala.
Se a lâmpada estiver acesa, você sabe qual interruptor a controla (o que foi ligado anteriormente).
Se a lâmpada estiver acesa, você sabe qual interruptor a controla (o não foi ligado).


5) Escreva um programa que inverta os caracteres de um string. 


IMPORTANTE: 

a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código; 

b) Evite usar funções prontas, como, por exemplo, reverse; 

    
    const  inverterString = (str) => {
        let resultado = '';
        for (let i = str.length - 1; i >= 0; i--) {
            resultado += str[i];
        }
        return resultado;
    }
    
    // Exemplo de uso:
    const minhaString = "123456789";
    const stringInvertida = inverterString(minhaString);
    console.log(stringInvertida);
