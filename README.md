
    #include <stdio.h>
    #include <stdlib.h>
    #include <time.h>
    
    
    int main(){
        system ("clear");
        srand((unsigned)time(NULL));
        int numeroSorteado = rand() % 11;
        int num;
        int tentativas = 1;
        int chances = 5;
      
      
      do{
          printf("\nAdvinhe o número aleatório! \n");
          printf("Número: ");
          scanf("%d", &num);
          
          if(numeroSorteado > num){
              printf("Número sorteado é maior! \n");
          }
          else if(numeroSorteado < num){
              printf("Número sorteado é menor! \n");
          }
              
          tentativas = tentativas + 1;
          /*printf("Quantidade de tentativas %d. \n", tentativas);*/
          
          chances --;
          printf("Você tem %d chances! \n", chances);    
              
      }while(numeroSorteado != num && tentativas <= 5 );
      
          
      if(tentativas > 5){
          printf("\nVocê excedeu a quantidade de chances!");
      }else if(numeroSorteado == num){
          printf("\nVocê acertou o número %d \n", numeroSorteado);
      }    
      
      
  
      return 0;
  }
