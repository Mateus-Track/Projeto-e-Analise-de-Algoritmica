int main(){
    char palavra[20];
    char palavra2[20];

    printf("Escreva palavra 1: ");
    scanf("%s", palavra);
    printf("Escreva palavra 2: ");
    scanf("%s", palavra2);
    int tamanho1 = strlen(palavra);
    printf("tamanho da palavra 1 = %i\n", tamanho1);
    int tamanho2 = strlen(palavra2);
    printf("tamanho da palavra 2 = %i\n", tamanho2);
    //for(int i = tamanho1; i >0; i--){

    //}

    int tabela[tamanho1 + 1][tamanho2 + 1];
    for(int i = 0; i< tamanho1+1; i++){
        tabela[i][0] = 0;
    }
    for(int j = 0; j< tamanho2+1; j++){
        tabela[0][j] = 0;
    }


    for(int i = 0; i<tamanho1+1; i++){
        for(int j = 0; j<tamanho2+1; j++){
            printf("%i ", tabela[i][j]);
        }
        printf("\n");
    }

    printf("\n\ncabooo\n\n");


    for(int m = 0; m<tamanho1; m++){
        for(int n = 0; n<tamanho2; n++){
            if(palavra[m] == palavra2[n]){
                tabela[m+1][n+1] = tabela[m][n] + 1;


            }else{
                if(tabela[m+1][n] > tabela[m][n+1]){
                    tabela[m+1][n+1] = tabela[m+1][n];
                }else{
                    tabela[m+1][n+1] = tabela[m][n+1];
                }
            }
        }
    }

    for(int i = 0; i<tamanho1+1;i++){
        for(int j = 0; j<tamanho2+1; j++){
            printf("%2i ", tabela[i][j]);
        }
        printf("\n");
    }


    printf("Tamanho da LCS= %i\n", tabela[tamanho1][tamanho2]);

    int tamanhoLCS = tabela[tamanho1][tamanho2];
    char sub[tamanhoLCS];
    int percorre = tamanho1;
    int percorre2 = tamanho2;
    while(percorre2> 0 && percorre > 0){
        if((tabela[percorre][percorre2] != tabela[percorre -1][percorre2]) && (tabela[percorre][percorre2] != tabela[percorre][percorre2-1] )){
            sub[tamanhoLCS-1] = palavra[percorre - 1];
            //printf("\nletra igual = %c\n", palavra[percorre - 1]);
            tamanhoLCS--;
            percorre--;
            percorre2--;
        }
        else{
            if(tabela[percorre][percorre2] == tabela[percorre -1][percorre2]){
                percorre--;
            }else{
                percorre2--;
            }
        }
    }


    printf("LCS = %s", sub);
    return 0;
}
