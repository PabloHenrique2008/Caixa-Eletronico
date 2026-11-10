#include <stdio.h>
int main() {
int saldo = 1000;
int saque;
int inicia_operacao = 1;
while(inicia_operacao == 1){
printf("Digite valor do saque: ");
scanf("%d", &saque);
if (saque > saldo) {
printf("Saldo insuficiente\n");
}else if (saque <= 0) {
printf("Valor invalido");
}else if (saque % 5 != 0) {
printf("Tem quer ser multiplo de 5");
}else{
saldo = saldo - saque;
int n100 = saque / 100;
saque = saque % 100;
int n50 = saque / 50;
saque = saque % 50;
int n20 = saque / 20;
saque = saque % 20;
int n10 = saque / 10;
saque = saque % 10;
int n5 = saque / 5;
saque = saque % 5;
printf("Notas de 100: %d\n", n100);
printf("Notas de 50: %d\n", n50);
printf("Notas de 20: %d\n", n20);
printf("Notas de 10: %d\n", n10);
printf("Notas de 5: %d\n", n5);
printf("Novo saldo: %d\n", saldo);
}
if (saldo <= 0){
printf("Você não tem mais saldo");
break;
}else{
printf("\nDeseja realizar outro saque? (1 - Sim / 0 - Nao): ");
if (scanf("%d", &inicia_operacao) != 1) {
while (getchar() != '\n');
inicia_operacao = 0; 
}
}
} 
return 0;
}