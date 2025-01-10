# Desafio Backend Logcomex (Captação)

Obrigado por demonstrar interesse em fazer parte do nosso time! Este desafio foi elaborado para avaliarmos suas habilidades como desenvolvedor backend, especialmente com foco em PHP.

## Instruções Iniciais
1. Crie um repositório no GitHub para o teste. Certifique-se de **não mencionar o nome da Logcomex** no repositório.
2. Stack
    - **PHP**:
      - Laravel ou um script PHP puro
    - Banco de dados relacional:
      - MySQL ou PostgreSQL
    - Banco de dados não relacional:
      - Redis
3. Fora as tecnologias mencionadas, você está livre para utilizar quaisquer outras ferramentas, bibliotecas ou frameworks que considere úteis.
4. Caso tenha dúvidas, sinta-se à vontade para entrar em contato com o recrutador.

## Objetivo
O desafio consiste em criar uma aplicação capaz de buscar dados na [página da Wikipédia](https://pt.wikipedia.org/wiki/Lista_das_maiores_empresas_do_Brasil) que contém a lista das maiores empresas do Brasil. O objetivo é filtrar as empresas pelo lucro, com base nos parâmetros enviados na requisição.

### Detalhes do Funcionamento
Sua aplicação deve implementar:
1. Uma API que receba os seguintes parâmetros:
   ```json
   {
     "rule": "greater", // ou "smaller", ou "between"
     "billions": 15,    // valor de referência em bilhões
     "range": [10, 20]  // somente para o caso "between" (opcional)
   }
   ```
2. A API deve retornar as empresas que atendem ao critério fornecido, com a seguinte estrutura de resposta:
   ```json
   [
     {
       "company_name": "Petrobras",
       "profit": "36.47",
       "rank": 1
     },
     {
       "company_name": "Vale",
       "profit": "15.98",
       "rank": 3
     }
   ]
   ```

### Regras de Negócio
- "**greater**": Retornar empresas com lucro maior que o valor especificado.
- "**smaller**": Retornar empresas com lucro menor que o valor especificado.
- "**between**" (bônus): Retornar empresas com lucro dentro do intervalo especificado em "range".

### Requisitos Adicionais
1. Todos os retornos em "profit" devem ser em bilhões. Por exemplo, a Cosan, que obteve lucro de 228 milhões, deve ser retornada como `0.228` bilhões.
2. Deve haver alguma estratégia que evite que vários requests sobrecarreguem a fonte ao mesmo tempo ou em um curto período de tempo.
3. Os dados devem ser salvos em tabelas relacionais para guardar o histórico das informações.
4. O HTML da captura deve ser salvo para servir como prova dos dados capturados.

## Requisitos e Pontos de Avaliação
### Obrigatórios:
- **Documentação**:
  - Descreva como rodar o projeto (instalação, dependências, execução e exemplos de uso).
- **Código Limpo e Organizado**:
  - Seguir padrões de código PHP (PSRs).
  - Aplicar boas práticas de design (SOLID, design patterns, etc.).
- **Modelagem de Dados**:
  - Escolha adequada de tipos de dados e estruturação.
- **Tratamento de Erros**:
  - Validação de inputs e respostas adequadas em casos de erro.
- **Testes Unitários**:
  - Cobertura mínima das principais funcionalidades.

### Bônus:
- Implementar a funcionalidade "**between**". **NAO É OBRIGATÓRIO**
- Criar testes de integração.
- Adicionar logs para depuração.
- Utilizar containers Docker para simplificar a execução.
- Oferecer uma solução com foco em performance.

## Dicas e Observações Finais
- Estruture bem sua solução antes de iniciar a codificação.
- Demonstre consistência em suas decisões e esteja preparado para justificá-las.
- Não se esqueça de tratar cenários inesperados, como mudanças na estrutura da página da Wikipédia ou valores não numéricos.

Boa sorte! Estamos ansiosos para ver sua solução e conhecer seu potencial!

