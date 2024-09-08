EX 13
#include <stdio.h>

// Função principal
int main() {
    char operacao;
    float num1, num2, resultado;

    // Solicita ao usuário que escolha a operação
    printf("Escolha a operação (+, -, *, /): ");
    scanf(" %c", &operacao);

    // Solicita ao usuário que insira os dois números
    printf("Digite o primeiro número: ");
    scanf("%f", &num1);

    printf("Digite o segundo número: ");
    scanf("%f", &num2);

    // Realiza a operação selecionada
    switch (operacao) {
        case '+':
            resultado = num1 + num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case '-':
            resultado = num1 - num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case '*':
            resultado = num1 * num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case '/':
            if (num2 != 0) {
                resultado = num1 / num2;
                printf("Resultado: %.2f\n", resultado);
            } else {
                printf("Erro: Divisão por zero não é permitida.\n");
            }
            break;
        default:
            printf("Erro: Operação não reconhecida.\n");
            break;
    }

    return 0;
}
