PROJETO_EM_C

//Testes do programa!!

CADASTRO DO CLIENTE: (teste)

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


CADASTRO DO AUTOMOVEL: (teste)

#include <stdio.h>
#include <stdlib.h>

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




//Teste "completo" do cliente e vendedor:


#include <stdio.h>
#include <string.h>
#include <stdlib.h>

typedef struct {
    int id;
    char nome[50];
    char apelido[50];
    int numtelefone;
    char sexo;
    char endereco;
    int numeroBI;
    char situacao;
} cliente;

int main() {
    
    cliente listaClientes[200];

    listaClientes[0].id = 1;
    strcpy(listaClientes[0].nome, "Joao Silva");

    printf("Clientes 1: %s \n", listaClientes[200].nome);
}

typedef struct {
    int id;
    char marca[100];
    char modelo[100];
    char cor[50];
    int classeveiculo;
    char combustivel[50];
    int ano;
    float preco;
    int vendido;
} veiculo;

void cadastrarVeiculos() {
    FILE *file = fopen(arquivo, "ab");
    if (file == NULL){
        printf("Erro ao abrir arquivo!\n")
        return 0;
    }
    veiculo; 

    printf("\n---Cadastrar Veiculo---\n")
    printf("ID: "); scanf("id%", &v.id);
    printf("Marca: "); scanf("%s", v.marca);
    printf("Modelo: "); scanf("%s", v.modelo);
    printf("Ano: "); scanf("%d", &v.ano);
    printf("Preço:"); scanf("%f", &v.preco);
    v.vendido = 0;
    
    fwrite(&v, sizeof(Veiculo), 1, file);
    fclose(file);
    printf("veiculo cadastrado com sucesso!\n");
}

void listarveiculos() {
    FILE *file = fopen(arquivo, "rb");
    if(file == NULL) {
        printf("Nenhum veiculo cadastrado.\n");
        return;
    }
veiculo v;
printf("\n---Lista de veiculos---\n");
while (fread(&v, sizeof(Veiculo), 1, file)) {
    printf("ID: %d | %s %s (%d) - R$ %.2f-%s\n",
          v.id, v.marca, v.modelo, v.ano, v.preco,
          v.vendido ? "Vendido" : "Disponivel");
    }
    fclose(file);
}

void venderVeiculos() {
    int idBusca;
    printf("\nDigite o ID do veiculo a vender: ");
    scanf("%d" , &idBusca);
    printf("Funcionalidade de venda simulada.\n");
}

int main() {
    int opsao;
    do {
        printf("\n1. Cadastrar Veiculo\n2. Listar Veiculos\n3. Vender Veiculo\n4. Sair\n0pcao: ");
        scanf("%d", &opcao);
        switch (opcao) {
            case 1: CadastrarVeiculo(); break;
            case 2: ListarVeiculos(); break;
            case 3: VenderVeiculo(); break;
            case 4: printf("Saindo...\n"); break;
            default: printf("Opcao invalida!\n");
        }
    } while (opcao ! = 4);
    return 0;
}
