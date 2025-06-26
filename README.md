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

Na parte inferior esquerda há opções selecionáveis para que faça a importação conforme as notas específicas:

- ```NFe - Notas Fiscais Eletrônicas```
- ```CTe - Conhecimento de Transporte Eletrônicos```

E por fim, selecione o botão **IMPORTAR**, aguarde o processo e feche o painel!

Essas extrações são as notas contra a ferro que teoricamente irão ser entregues conforme já citado no 1.1,  e ficaram disponíveis para consulta no sistema até que entrem as notas das mercadorias.

--------

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

--------

#### 1.3 - MERCADO LIVRE (FULL)

As notas são emitidas pela própria plataforma e o departamento fiscal apenas baixa os xmls e importa ao sistema Prisma.

As vendas do Mercado Livre Full são emitidas as notas diretamente do ML, já saindo da Ferro para o cliente. E em contra partida o ML emite uma nota de retorno para o estoque da Ferro para que compute essa saída Nat.Operação - Outras Entradas - Retorno Simbólico de Deposito Temporário.

**Importação das notas do Mercado Livre FULL**

> ![image](https://github.com/user-attachments/assets/525ec123-7a1e-4621-b42c-70cbd3ebfa41)

Nota de venda (Saída) - Familia financeira - 513 

> ![image](https://github.com/user-attachments/assets/e8379995-b61b-4326-abc6-1d24d20b6dee)

A nota emitida pelo Mercado Livre Full de Outras Entradas - Retorno Simbólico de Depósito Temporário, é para entrada ao estoque da Ferro Ferramentas - E-commerce para que seja efetuada a venda on line, e a nota emitida de Venda para o cliente é a saída, o qual é necessário realizar o desdobramento com a forma de pagamento 186 - Mercado Livre.

--------

#### 1.4 - Série da NF-e

> **SÉRIE 001** - Utilizada pela Ferro Industria (Antiga) em suas emissões

> **SÉRIE 002** - Utilizada atualmente pela Ferro Ferramantas (E-commerce - ML | TIK TOK ! LEROY MERLIN | FERRO STORE)

> **SÉRIE 003** - Utilizada na emissão das notas pelo Mercado Livre Full (E.bazar)

--------

### 2. Quais são as empresas da Ferro? E suas operações?

☑️**FERRO STORE LTDA - CNPJ 59.217.616/0001-61 (CD)** 

- **Emite Nota Fiscal**

➡️Ferro indústria ```(Venda)```

➡️Ferro Ferramentas ```(E-commerce)```

Para abastecer o estoque, sendo apenas para realizar a venda efetivada em uma das plataformas, fazendo a entrada no sistema e a saída (Venda) para o cliente.

➡️Ferro Store - Filial ```(Transferência) ```

--------

☑️**FERRO STORE LTDA - CNPJ 59.217.616/0002-42 (FERRO LOJA - FILIAL)**

- **Emite Nota Fiscal**

➡️Faturamento para todos os clientes balcão dentro da cidade

➡️Ferro indústria ```(Venda)```

➡️Ferro Store - CD ```(Transferência)```

--------

☑️**FERRO FERRAMENTAS - CNPJ 25.003.733/0001-00 (E-COMMERCE)**

- **Emite Nota Fiscal**

➡️```Faturamento para fora do estado ou mercado interno (SP)```

--------

☑️**FERRO EQUIPAMENTO INDUSTRIAL - CNPJ 15.797.607/0001-11 (FERRO INDUSTRIA)**

- **Emite Nota Fiscal**

➡️Ferro Store - Filial ```(Remessa p/conserto)```

--------

☑️**FERRO EQUIPAMENTO INDUSTRIAL - CNPJ 15.797.607/0002-00 (FERRO LOJA ANTIGA)**

- **Emite Nota Fiscal**

➡️Ferro Store (CD) ```(Venda)``` 

➡️Ferro Store - Filial ```(Venda)```

A decisão de onde será destinada a mercadoria fica por conta do Gerente Carlinhos da Ferro Store - Filial (Loja), pois ainda existem pedidos de compras que estão sendo faturados pela Empresa Antiga.

--------

### 3. Sistemas internos

**Prisma**

> ![image](https://github.com/user-attachments/assets/64a60b8b-92a9-4529-90c7-17b9e668baae)

**Super Soft**

> ![image](https://github.com/user-attachments/assets/251f3a11-9237-4d73-9894-ace1b8a83708)


### 4. Legendas

Formas utilizadas para identificação da operação interna:

| Sigla | Legenda |
|---------|----------|
| AC | Aviso de compra |
| AF | Ativo fixo |
| AT | Aviso de transferência |
| MC | Mercadoria de uso e consumo |
| MR | Mercadoria de Revenda |
| MT | Material de terceiro |
| PC | Pedido de compra |
| PV | Pedido de Venda |
| SV | Nota de Serviço |


--------

### 5. Portaria | Ricms SP

#### 5.1 Portarias

📑**Portarias**:

> ➡️[Acesse - Ferramentas](https://legislacao.fazenda.sp.gov.br/Paginas/Portaria-SRE-14-de-2023.aspx)

> ➡️[Acesse - Auto Peças](https://legislacao.fazenda.sp.gov.br/Paginas/Portaria-SRE-16-de-2023.aspx)

> ➡️[Acesse - Materiais Elétricos](https://legislacao.fazenda.sp.gov.br/Paginas/Portaria-SRE-86-de-2024.aspx)

> ➡️[Acesse - máquinas, aparelhos e equipamentos industrias](https://legislacao.fazenda.sp.gov.br/Paginas/resf041998.aspx)

#### 5.2 RICMS

📑**Alíquotas**: 

> ➡️[SEÇÃO II - DA ALÍQUOTA](https://legislacao.fazenda.sp.gov.br/Paginas/art052.aspx)

--------

📑**Reduções**: 

> ➡️[Artigo 65 (CARROCERIAS SOBRE CHASSI, VAGÕES FERROVIÁRIOS DE CARGA, CARROCERIAS PARA VEÍCULOS AUTOMÓVEIS, REBOQUES E SEMIRREBOQUES)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art065.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

> ➡️[Artigo 12 (MÁQUINAS INDUSTRIAIS E IMPLEMENTOS AGRÍCOLAS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art012.aspx) 

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 48,89%	| 18,00%	| 8,80% |
| 46,67%	| 12,00%	| 5,60% |

> ➡️[Artigo 36 (AUTOPEÇAS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art036.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

> ➡️[Artigo 30 (PRODUTOS DE COURO, SAPATOS, BOLSAS, CINTOS, CARTEIRAS E OUTROS ACESSÓRIOS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art030.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

> ➡️[Artigo 52 (PRODUTOS TÊXTEIS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art052.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

--------

📑**Convênio e Protocolo**: 

> ➡️[ANEXO VI - SUBSTITUIÇÃO TRIBUTÁRIA EM OPERAÇÕES OU PRESTAÇÕES INTERESTADUAIS - ESTADOS SIGNATÁRIOS DE ACORDOS](https://legislacao.fazenda.sp.gov.br/Paginas/textoricms.aspx#l6an6.aspx)

> ➡️[Convênio 142/18 - Regime de substituição tributária](https://www.confaz.fazenda.gov.br/legislacao/convenios/2018/CV142_18)

--------

📑**Isenção**: 

> ➡️[ANEXO I - ISENÇÕES](https://legislacao.fazenda.sp.gov.br/Paginas/textoricms.aspx#an1art001.aspx)

---------

📑**Partilha ICMS - Consumidor Final Interestadual**: 

> ➡️[Partilha ICMS](https://www.confaz.fazenda.gov.br/legislacao/convenios/2015/CV093_15)

> Para ocorrer a divisão de ICMS é obrigatório que duas condições estejam presentes. A primeira é a operação ser interestadual, ou seja: o remetente da mercadoria está em um estado e o destinatário em outro. Já a segunda condição obrigatória é a mercadoria se destinar ao consumo final. 

---------

#### 5.3 Resposta à consulta

---------

### 6. Cálculo substituição tributária (MVA / Redução / IPI)

**Exemplo de cálculo operação interestadual:**

> ![image](https://github.com/user-attachments/assets/85b209f0-e225-4625-b7e4-65f80208b45d)

- Total de Produtos: 1699,90
- Frete: 79,00
- IPI: 85,00
- MVA 70%
- Redução 48,89% (Carga tributária 8,80%)

**Base de ICMS:** (1699,90 + 79,00) * 48,89% = 869,70
**Valor de ICMS:** (869,70 * 18%) = 156,55

**Base de ICMS ST:** (1699,90 + 79,00 + 85) * 70% = 3168,63
**Base de ICMS ST c/redução:** 3168,63 * 48,89% = 1549,14

**Valor de ICMS ST:** 278,85 - 156,55 = 122,30

---------

### 7. Pedidos devolvidos por cliente - Ferro Store (Devolução)

Para a conferência e identificação das devoluções é preciso antes extrair o relatório de "Pedidos Devolvidos" e relacionar qual o período que gostaria de realizar a análise. Abaixo o caminho para realizar essa consulta:

> ![image](https://github.com/user-attachments/assets/df934d83-c6ab-498d-813c-4c44fa46a31b)

➡️**Passo a Passo:**

#### 7.1. Faturamento / Vendas / Nota Fiscal / Consulta

- Relacione em consulta o nome do cliente e preencha em movimento o nº da nota de devolução (1.102 | 1.411) devido ser uma venda a consumidor final (Tributada(00 | 20 | 40) ou ST Recolhida anteriormente - 60), Modelo 55, Série 1.
- Ao abrir na tela, em **Relação de Notas referenciadas** pegue a chave de acesso e faça a consulta da Nota Fiscal Consumidor Eletrônica (NFC-e) para verificar o número do cupom e se esta autorizado.
- Ainda em Faturamento / Vendas altere o modelo para 65 e informe o número da NFC-e e verifique a venda realizada ao cliente.

#### 7.2. Faturamento / Vendas / Consultar Cupom

- Com o relatório extraído faça a consulta em Nº Pedido do Pedido de venda para verificar a saída feita para o cliente.
- E também em Nº Pedido faça a consulta da Devolução para verificar se os lançamentos estão de acordo com a nota emitida de devolução.
- Pedido de Venda (Sequencial do número de venda).
- Nº Devolução é a solicitação do cliente, ou seja, o sequencial da ordem de devolução.

> ![image](https://github.com/user-attachments/assets/d5cc9748-1914-4d84-bc5a-e97d211f61b5)

#### 7.3. Conferência e validação das informações

- Faça a conferência dos campos próprios (ICMS) se estão em conformidade, dados do cliente, Total da nota, itens (CP), quantidade, Valor, dados fiscais (NCM, CFOP, CST, PIS/COFINS).
- Validar se a Nota de devolução esta conforme Pedido de devolução (Nº Devolução).


### 8. Sugestões de melhorias

Quando tiver uma operação interestadual de compra de mercadoria onde não há convênio/protocolo entre os estados e fica a cargo da Ferro realizar o recolhimento ST, seria interessante amarrar em um campo o percentual MVA a se utilizar na operação, no caso se ajustado ou original nos casos onde a carga tributária do estado remetente seja a mesma do destinatário.

E para que fique ainda mais eficiente, trazer as portaria mais utilizadas na indústria com NCM, CEST e MVA para deixar programado ao sistema e todas as compras que tiverem esse tipo de operação com substiruição tributária em SP já ser realizado o cálculo do valor a recolher via DARE.

**Como fazer isso?**

> Se tiver na seção de alíquotas amparadas com percentual de 12% - Artigo 54, a aplicação da MVA será considerada como o ORIGINAl devido a carga tributária da operação interestadual ser a mesma da interna.

> E nos casos onde a carga tributária interna seja maior que a da operação interestadual, será necessário o ajuste sendo considerada a MVA Ajustada.

**Alguns cenários nas operações:**

| Alíquota interestadual | Alíquota Interna | Ajustado |
|------------|------------|--------------|
| 4% | 18% | ☑️ SIM |
| 12% | 18% | ☑️ SIM |
| 4% | 12% | ☑️ SIM |
| 4% | 7% | ☑️ SIM |
| 12% | 12% | ❌ NÃO |
