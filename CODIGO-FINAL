#include <stdio.h>
#include <string.h>



int main(){
    int opcao;
    char frase[100];
    char l; 
    long int chave1, chave2, i, c;



//MENU
while (opcao != 1 && opcao != 2 && opcao != 3)
        {printf("Seja bem vindo ao programa de Cifra de Cesar\n");
        printf("O que voce deseja fazer hoje?\n"
                "[1]Criptografar\n"
                "[2]Descriptografar\n"
                "[3]Sair\n"
                "Opcao: ");
        fflush(stdin);
        //__fpurge(stdin); //CASO VÁ USAR LINUX
        scanf("%d", &opcao);}
    


    switch (opcao)
    {

//Criptografia
        case 1:
        printf("Digite sua frase: \n");
        fflush(stdin);                                                  
        //__fpurge(stdin); //CASO VÁ USAR LINUX
        scanf("%[^\n]s", frase);
        printf("Digite a rotacao: \n");
        scanf("%ld", &chave2);
        chave1 = chave2;

        if (chave2 < 0) //Verifico se a chave é negativa
            {chave2 = -chave2;} //Se for, torno positiva

        while (chave2 > 26) //Verifica se o número de rotações é maior que 26
            {chave2 = chave2 - 26;} //Enquanto for maior ou igual, ele vai subtraindo até ser menor que 26

//Código de Criptografia
        if (chave1 >= 0)
            {for (i = 0; frase[i] != '\0'; i ++)
                {l = frase[i]; //Atribui letra por letra ao L
                if (l >= 'a' && l <= 'z') //Verifica se L está entre A e Z
                    {
                    if (l + chave2 > 'z') //Verifica se a soma de L com a Rotação é maior que Z
                        {l = l - 26 + chave2;} //Se for verdadeiro, ele subrtrai de 26 (Uma volta no alfabeto) e soma a Chave
                    else {l = l + chave2;} //Se não, soma da rotação
                    frase[i] = l;} //Devolve o valor da letra já com a mudança de chave
                else if (l >= 'A' && l <= 'Z')
                    if (l + chave2 > 'Z')
                        {l = l - 26 + chave2;}
                    else {l = l + chave2;}
                    frase[i] = l;}  
                printf("Mensagem criptografada: %s \n", frase);
                printf("Numero de rotacoes: %ld\n", chave1);
                printf("Muito Obrigado!\n");
                break;}   
        else{  //Se a chave for negativa, repito o código de descriptografia     
            for (i = 0; frase[i] != '\0'; i ++)
            {l = frase[i];
            if (l >= 'a' && l <= 'z')
                {
                if (l - chave2 < 'a')
                    {l = l + 26 - chave2;} 
                else {l = l - chave2;}
                frase[i] = l;}  
            else if (l >= 'A' && l <= 'Z')
                if (l - chave2 < 'A')
                    {l = l + 26 - chave2;}
                else {l = l - chave2;}
                frase[i] = l;}
                printf("Mensagem descriptografada: %s \n", frase);
                printf("Numero de rotacoes: %ld\n", chave1);
                printf("Muito Obrigado!\n");
                break;}        






//Descriptografia
        case 2: 
        printf("Digite sua frase: \n");
        fflush(stdin);
        //__fpurge(stdin); //CASO VÁ USAR LINUX
        scanf("%[^\n]s", frase);
        printf("Digite a rotacao: \n");
        scanf("%ld", &chave2);    
        chave1 = chave2;

        if (chave2 < 0) //Verifico se a chave é negativa
            {chave2 = -chave2;} //Se for, torno positiva

        while (chave2 > 26) //Verifica se o número de rotações é maior que 26
            {chave2 = chave2 - 26;} //Enquanto for maior ou igual, ele vai subtraindo até ser menor que 26

//Código de Descriptografia
        if(chave1 >=0)
            {for (i = 0; frase[i] != '\0'; i ++)
                {l = frase[i]; //Atribui letra por letra ao L
                if (l >= 'a' && l <= 'z') //Verifica se L está entre A e Z
                    {
                    if (l - chave2 < 'a') //Verifica se a diferença de L com a Rotação é menor que A
                        {l = l + 26 - chave2;} //Se for verdadeiro, ele adciona 26 (Valor de 1 volta no alfabeto) e subtrai a Chave
                    else {l = l - chave2;} //Se não, subtrai da rotação
                    frase[i] = l;}  //Devolve o valor da letra já com a mudança de chave
                else if (l >= 'A' && l <= 'Z')
                    if (l - chave2 < 'A')
                        {l = l + 26 - chave2;}
                    else {l = l - chave2;}
                    frase[i] = l;}
            printf("Mensagem descriptografada: %s \n", frase);
            printf("Numero de rotacoes: %ld\n", chave1);
            printf("Muito Obrigado!\n");
            break;}
        else{ //Se a chave for negativa, repito o código de criptografia  
            for (i = 0; frase[i] != '\0'; i ++)
                {l = frase[i]; //Atribui letra por letra ao L
                if (l >= 'a' && l <= 'z') //Verifica se L está entre A e Z
                    {
                    if (l + chave2 > 'z') //Verifica se a soma de L com a Rotação é maior que Z
                        {l = l - 26 + chave2;} //Se for verdadeiro, ele subrtrai de 26 (Uma volta no alfabeto) e soma a Chave
                    else {l = l + chave2;} //Se não, soma da rotação
                    frase[i] = l;} //Devolve o valor da letra já com a mudança de chave
                else if (l >= 'A' && l <= 'Z')
                    if (l + chave2 > 'Z')
                        {l = l - 26 + chave2;}
                    else {l = l + chave2;}
                    frase[i] = l;} 
                printf("Mensagem criptografada: %s \n", frase);
                printf("Numero de rotacoes: %ld\n", chave1);
                printf("Muito Obrigado!\n");
                break;}

//Saída do Programa
    case 3:
        printf("Muito Obrigado!\n");
        break;
    }
}
