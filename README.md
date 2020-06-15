## Motivação

Pensando na construção um sistema de informações para auxiliar na tomada de decisões para gestores públicos e agentes de saúde,
vamos elaborar um banco de dados para registrar o avanço do COVID-19 pelo Brasil. 
Para isso, a tabela REGISTRO_DIARIO_COVID19 irá armazenar o número de pessoas infectadas, à óbito e curadas de um determinado dia e cidade.

### 1ª Etapa Criação da Estrutura

![Modelo](modelo.png)

Algumas dicas importantes:

● A chave primária das tabelas podem ser auto incrementadas pelo SGBD;

● Os atributos com prefixo QTD_ devem ser, obrigatoriamente, do tipo INTEGER;

● O atributo chamado DATA deve ser do tipo DATE.

### 2.Etapa) Criação dos Dados 

● 10 estados. Obrigatório que esteja na lista: São Paulo, Rio de Janeiro e Amazonas;

● 20 cidades (relacionado entre os estados). Obrigatório que esteja na lista: São Paulo, Rio de
Janeiro e Manaus;

● 60 registros diários de COVID, para diferentes dias e cidades. Mantenha algumas cidades sem registros (pelo menos duas).
Dica: Para informar um valor válido para o campo DATA, utilize a seguinte sintaxe no MySQL: AAAA-MM-DD. 

Exemplo:
```
INSERT INTO EXEMPLO(DATA) VALUES ('2020- 05 - 22');
```

### 3ª Etapa Consultas


1. Retornar o nome das cidades de um determinado estado, ordenado pela quantidade da
    população;
2. Retornar o nome dos estados que comecem com a letra S:
3. Informar quando houve o início da doença, ou seja, a data mais antiga registrada na tabela
    REGISTRO_DIARIO_COVID19:
4. Listar o nome da cidade e a sigla do estado cujo tamanho do município seja maior que 1000
    quilômetros quadrados:
5. Retornar a soma da quantidade de casos de uma determinada cidade:
6. Retornar a soma de óbitos ocorridos desde ontem para o estado de São Paulo:
7. Listar a data, a quantidade de casos e a quantidade de óbitos do estado do Rio de Janeiro a partir
    do dia 1º de maio, ordenando pela data:
8. Listar as cidades que ainda não possuem nenhum registro de COVID-19:
9. Informar a soma da quantidade de pessoas atualmente enfermas na cidade de Manaus. Para isso,
    utilize o cálculo: QTD_CASOS - QTD_OBITOS - QTD_RECUPERADOS:
10. Liste o nome da cidade e a taxa de mortalidade, obtida a partir do seguinte cálculo: QTD_OBITOS
    / QTD_CASOS * 100:
11. Informe o nome da cidade, a quantidade da população e a porcentagem no número de infectados
    do município que possui mais casos confirmados. Para calcular a porcentagem, utilize o seguinte
    cálculo: QTD_CASOS / QTD_POPULACAO * 100:
