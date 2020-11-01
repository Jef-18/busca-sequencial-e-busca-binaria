#include <stdio.h>
#include <stdlib.h>
void quick(int vetor[10], int inicio, int fim);

int main(){
    
    int vetor[10] = {10,20,30,40,50,60,70,80,90,100};
    int inicio = 0, fim = 9, meio, valor =100;
    int i, it;
    
    printf("\n VETOR: [10,20,30,40,50,60,70,80,90,100]\n\n");

    printf("\n * BUSCA SEQUENCIAL * \n\n");
    printf("\n Digite o valor do vetor a ser procurado: ");
    scanf("%d", &valor);

    while(inicio <= fim){
        meio = (int)((inicio + fim) / 2);
        if(valor < vetor[meio]){
            fim = meio - 1;
        }
        else if(valor > vetor[meio]){
            inicio = meio + 1;
        }
        else{
            printf("\n Valor do vetor procurado: %d | Posição do vetor: %d ", valor, meio);
            break;
        }
   
    }   

/******************************************************************/

    printf("\n\n\n");
    
    printf("\n * QUICK SORT * \n\n");
    printf("\n Vetor Inicial: Crescente\n");
    for(int i = 0; i < 10; i++) {
        printf(" %d ", vetor[i]);
    }
    printf("\n");
    
    quick(vetor, 0, 9);
    
    printf("\n Vetor Final: Decrescente\n");
    for(int i = 0; i < 10; i++) {
        printf(" %d ", vetor[i]);
    }

/******************************************************************/

    printf("\n\n\n");
    valor = 0;

    printf("\n * BUSCA BINÁRIA * \n\n");
    printf("\n Digite o valor do vetor a ser procurado: ");
    scanf("%d", &valor);
    
    for(int i = 0; i < 10; i++){
        if(vetor[i] == valor){
            printf("\n Valor do vetor procurado: %d | Posição do vetor: %d ", valor, i);
            break;
        }
    }
    printf("\n\n Fim da pesquisa.");

} 
  
void quick(int vetor[10], int inicio, int fim){
    
    int i, j, pivo, meio, temp;
    
    i = inicio;
    j = fim;
    
    meio = (int)((i + j) /2); //converte para inteiro
    pivo = vetor[meio];
    
    do{ //Enquanto j (fim) for maior do i (início)
        
        while(vetor[i] > pivo){
            i++;
        }
        
        while(vetor[j] < pivo){
            j--;
        }
        
        if(i <= j){ //Se não tiver cruzado os valores
            temp = vetor[i];
            vetor[i] = vetor[j];
            vetor[j] = temp; //Momento da thread_local
            i++;
            j--;
        }
        
        
    }while(j > i);  //Enquanto os ponteiros não se cruzaram
    
    if(inicio < j){
        quick(vetor, inicio, j);
    }
    
    if(i < fim){
        quick(vetor, i, fim);
    }

    
}

