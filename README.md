#include <stdio.h>
#include <string.h>

typedef struct {
    int id;
    char nome[50];
    char apelido[50];
    int numtelefone;
    char sexo;
    char endereco;
    int numeroCPF;
    char situacao;
} cliente;

int main() {
    
    cliente listaClientes[200];

    listaClientes[0].id = 1;
    strcpy(listaClientes[0].nome, "Joao silva");

    printf("Clientes 1: %s \n", listaClientes[200].nome);
}

struct automovel {

    int clienteid;
    char marca[100];
    char modelo[100];
    char matricula[17];
    int classeveiculo;
    char cor[50];
    char combustivel[50];
    int ano;
}
iobjsbuj
