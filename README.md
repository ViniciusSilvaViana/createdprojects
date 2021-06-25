# createdprojects
Projetos Criados 

#include<stdio.h>
#include<stdlib.h>
#include<locale.h>
#define NumAluno 4
#define BimestreA 4

int main(void){
	system("color E");
	setlocale(LC_ALL,"Portuguese");
	
	float NAlunos[NumAluno][BimestreA]={0};
	float MediasAlunos[NumAluno]={0};
    float media=0;
    int aluno,notas;
    
    printf(" Digite as 4 notas do aluno\n\n ");
    
    for(aluno=0;aluno<NumAluno;aluno++){
    	for(notas=0;notas<BimestreA;notas++){
    		printf("Insira a %dª nota do aluno %d = ",notas+1,aluno+1);
			scanf("%f",&NAlunos[aluno][notas]);
    		media=media+NAlunos[aluno][notas];
		}
		MediasAlunos[aluno]=media/BimestreA;
		media=0;
		printf("\n");
		printf(" - - - - - - - - - - - - -\n");
		printf("\n");
	}
    // laço só para a média
    for(aluno=0;aluno<NumAluno;aluno++){
	   printf("\n A media do aluno %d é = %.2f \n",aluno+1,MediasAlunos[aluno]);	
	}
	
	system("pause"); 	
	return 0;
}
