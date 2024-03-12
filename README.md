
# Desafio backend Logcomex (Captação)

Primeiramente, obrigado pelo seu interesse em participar do nosso processo seletivo, esta vaga é para desenvolvedor backend com foco em PHP, aqui utilizamos bastante scraping/crawling para capturar dados e o teste vai seguir essa mesma linha.

# Antes de começar
- Crie um repositório no seu GitHub sem mencionar o nome da Logcomex
- Stack que pode ser utilizada:
  - **PHP**
    - Laravel
    - Symfony
    - Script
  - Banco de dados relacional
    - Mysql
    - Postgres
  - Banco de dados não relacional
    - Redis
    - MongoDB
  - Tirando essas restrições acima, o restante fica a seu critério.
- Fique a vontade para tirar qualquer dúvida com o recrutador sobre o teste.

# Objetivo
Desenvolver uma aplicação onde o será passado um código ou numero ISO 4217 (*padrão internacional que define códigos de três letras para as moedas*), e a aplicação deve realizar o crawling em uma fonte externa, os dados desta moeda.

- Fonte externa: [ISO 4217](https://pt.wikipedia.org/wiki/ISO_4217)
- A pesquisa pode ser feita com um ou mais items.
- Input de dados:  **Código ISO** valido ex: GBP ou um **número** ex: 826
```json
{  
  "code": "GBP"
}
```
OU 
```json
{  
  "code_list": ["GBP", "GEL", "HKD"]  
}
```
OU 
```json
{  
  "number": [242]  
}
```
OU
```json
{
  "number_lists": [242, 324]  
}
```
- Retorno esperado:
```json
[{  
  "code": "GBP",  
  "number": 826,  
  "decimal": 2,  
  "currency": "Libra Esterlina",  
  "currency_locations": [  
    {  
      "location": "Reuno Unido",  
      "icon": "https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Flag_of_the_United_Kingdom.svg/22px-Flag_of_the_United_Kingdom.svg.png"  
    },  
    {  
      "location": "Ilha de Man",  
      "icon": ""  
    },  
    {  
      "location": "Guernesey",  
      "icon": ""  
    },  
    {  
      "location": "Jersey",  
      "icon": ""  
    }  
  ]  
}]  
```  
> Esses valores de entrada e saída são apenas exemplos, sinta se a vontade para melhorá-los.

## Observações:

- A tabela de dados da fonte não deve ser salva por inteiro no banco de dados.
- Utilizar a versão em português da página.
- Não precisa ter autenticação

## O que será avaliado
- Documentação
- Código limpo e organizado
- Conhecimento de padrões (PSRs, design patterns, SOLID, Object Calisthenics)
- Ser consistente e saber argumentar suas escolhas
- Modelagem de Dados
- Tratamento de erros
- Arquitetura (estruturar o pensamento antes de escrever)
- Testes unitários

## O que será um diferencial
- Docker
- Caching
- Testes de mutação

## Avaliação
Após a finalização do teste, será marcado uma call para que você apresente a solução desenvolvida, explicando o porquê das suas escolhas, como, por exemplo, a stack utilizada, quais os padrões adotados, como você pensou nos testes e cenários possíveis.  
