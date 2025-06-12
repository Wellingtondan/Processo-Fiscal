# Processo Fiscal

### PLATAFORMAS, PROCESSOS FISCAIS, CONFERÊNCIAS E CUSTO

Nesse repositório contém algumas orientações e passo a passo para entradas de notas, consultas, conferências, extrações base de XML de vendas.

### 1. Plataformas (Notas Fiscais)
   
#### 1.1 - QIVE

Pelo ```ARQUIVEI``` são realizadas as consultas das notas emitidas pelos fornecedores para a Ferro, e são estraídos os xmls para importação do sistema Prisma apenas para consulta.

As notas que não tiveram entradas de acordo com a entrega do fornecedor, precisa ser repassadas ao compras conforme a data de emissão para manter o controle de emissões contra a Ferro e assim cobrem seus fornecedores para o envio e entrada ao estoque da mercadoria.

Conforme a chegada da mercadoria e entrada ao sistema, as notas vão sendo liberadas nas consultas de notas pendentes de recebimento e deixando de aparecer no painel.

##### 1.1.1 - Importação Prisma

Pela manhã são realizadas as consultas completas da NF-e e CT-e e são extraídos os xmls e salvos no caminho ```Y:\Publico\Fiscal\XML``` onde será capturados pelo  sistema.

- **Empresas:**

```diff
- FERRO STORE LTDA - CD
- FERRO STORE LTDA - FILIAL
- FERRO INDUSTRIA ANTIGA
```

> O Caminho no sistema para a importação: ➡️ Estoque / Compras ➡️ Importar Notas Fiscais

Após a extração irá subir os xmls para o sistema para a importação, conforme ilustração abaixo:

> ![image](https://github.com/user-attachments/assets/e9162d2a-f2a8-444b-bc00-f9da0ce70887)

Na parte inferior esquerda há as opções selecionáveis para que faça a importação conforme as notas específicas:

- ```NFe - Notas Fiscais Eletrônicas```
- ```CTe - Conhecimento de Transporte Eletrônicos```

E por fim, selecione o botão **IMPORTAR**, aguarde o processo e feche o painel!

Essas extrações são as notas contra a ferro que teoricamente irão ser entregues conforme já citado no 1.1,  e ficaram disponíveis para consulta no sistema até que entrem as notas das mercadorias.

#### 1.2 - BLING

Abaixo são todas as plataformas de vendas do e-commerce nas quais as notas são emitidas pelo Bling:

- Leroy Merlin
- Mercado Livre
- Tik Tok Shop
- Ferro Ferramentas

São realizadas conferências diárias do sequencial das notas para não ocorrer nenhuma inconsistência ou pular a ordem dos números nas emissões na qual são emitidas e importadas ao sistema Prisma pelo departamento do E-commerce. 

**Conferência**

Para assegurar que as notas estão sendo emitidas com os dados tributários corretos, será necessário fazer um filtro nas notas do dia e consultar se NCM, CST e CFOP estão de acordo com o produto vendido.

> ![image](https://github.com/user-attachments/assets/ec790430-5fbd-4fa9-a11f-32a97fa31f07)


**Notas Canceladas**

Acho importante também realizar a consulta no Portal NFe se houve de fato o cancelamento das notas canceladas no BLING.

> ![image](https://github.com/user-attachments/assets/b512990a-e675-43d1-917b-e5eab26f5d97)

> Caminho no site: ➡️ Vendas / Notas Fiscais de saída ➡️ Importar Notas Fiscais

#### 1.3 - MERCADO LIVRE (FULL)

As notas são emitidas pela própria plataforma e o departamento fiscal apenas baixa os xmls e importa ao sistema Prisma.


### 2. Empresas

☑️**FERRO STORE LTDA - CNPJ 59.217.616/0001-61 (CD)** 

**Emite Nota Fiscal**

➡️Ferro indústria ```(Venda)```

➡️Ferro Ferramentas ```(E-commerce para abastecer o estoque)```

➡️Ferro Store - Filial ```(Transferência) ```

--------

☑️**FERRO STORE LTDA - CNPJ 59.217.616/0002-42 (FERRO LOJA - FILIAL)**

**Emite Nota Fiscal**

➡️Faturamento para todos os clientes balcão dentro da cidade

➡️Ferro indústria ```(Venda)```

➡️Ferro Store - CD ```(Transferência)```

--------

☑️**FERRO FERRAMENTAS - CNPJ 25.003.733/0001-00 (E-COMMERCE)**

**Emite Nota Fiscal**

➡️```Faturamento para fora do estado ou mercado interno (SP)```

--------

☑️**FERRO EQUIPAMENTO INDUSTRIAL - CNPJ 15.797.607/0001-11 (FERRO INDUSTRIA)**

☑️**FERRO EQUIPAMENTO INDUSTRIAL - CNPJ 15.797.607/0002-00 (FERRO LOJA ANTIGA)**


### 3. Sistemas internos

Prisma

Super Soft


### 4. Portaria | Ricms SP

4.1 Portaria

📑**Ferramentas**: [Acesse](https://legislacao.fazenda.sp.gov.br/Paginas/Portaria-SRE-14-de-2023.aspx)

4.2 RICMS

📑**Alíquotas**: 




Material desenvolvido para NFS-e com informações dos códigos de Serviços

[Acesse conteúdo](https://github.com/Wellingtondan/Codigos-de-Servicos-Tomador.git)

```Acessarmos o sistema :```
