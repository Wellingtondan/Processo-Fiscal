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

5.1 Portaria

📑**Ferramentas**:

--------

[Acesse](https://legislacao.fazenda.sp.gov.br/Paginas/Portaria-SRE-14-de-2023.aspx)

5.2 RICMS

📑**Alíquotas**: 

[SEÇÃO II - DA ALÍQUOTA](https://legislacao.fazenda.sp.gov.br/Paginas/art052.aspx)

--------

📑**Reduções**: 

> [Artigo 65 (CARROCERIAS SOBRE CHASSI, VAGÕES FERROVIÁRIOS DE CARGA, CARROCERIAS PARA VEÍCULOS AUTOMÓVEIS, REBOQUES E SEMIRREBOQUES)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art065.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

> [Artigo 12 (MÁQUINAS INDUSTRIAIS E IMPLEMENTOS AGRÍCOLAS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art012.aspx) 

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 48,89%	| 18,00%	| 8,80% |
| 46,67%	| 12,00%	| 5,60% |

> [Artigo 36 (AUTOPEÇAS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art036.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

> [Artigo 30 (PRODUTOS DE COURO, SAPATOS, BOLSAS, CINTOS, CARTEIRAS E OUTROS ACESSÓRIOS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art030.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

> [Artigo 52 (PRODUTOS TÊXTEIS)](https://legislacao.fazenda.sp.gov.br/Paginas/an2art052.aspx)

| Redução | Alíquota | Carga tributária |
|-------|-----------|------------|
| 66,67%	| 18,00%	| 12,00% |

--------

📑**cONVÊNIO E PROTOCOLO**: 

[ANEXO VI - SUBSTITUIÇÃO TRIBUTÁRIA EM OPERAÇÕES OU PRESTAÇÕES INTERESTADUAIS - ESTADOS SIGNATÁRIOS DE ACORDOS](https://legislacao.fazenda.sp.gov.br/Paginas/textoricms.aspx#l6an6.aspx)

--------

📑**Isenção**: 


---------

### 6. Cálculo subsituição tributária (MVA | Redução | IPI)

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



### 4. Sugestões de melhorias

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


Alíquotas 18%

Ferramentas

https://legislacao.fazenda.sp.gov.br/Paginas/Portaria-SRE-14-de-2023.aspx

Auto Peças

https://legislacao.fazenda.sp.gov.br/Paginas/Portaria-SRE-16-de-2023.aspx


https://legislacao.fazenda.sp.gov.br/Paginas/resf041998.aspx




### Pedidos devolvidos por cliente - Ferro Store (Devolução)

Para a conferência e identificação das devoluções é preciso antes extrair o relatório de "Pedidos Devolvidos" e relacionar qual o período que gostaria de realizar a análise. Abaixo o caminho para realizar essa consulta:

> ![image](https://github.com/user-attachments/assets/df934d83-c6ab-498d-813c-4c44fa46a31b)

Passo a Passo:

## 1. Faturamento / Vendas / Nota Fiscal / Consulta

- Relacione em consulta o nome do cliente e preencha em movimento o nº da nota de devolução (1.102) devido ser uma venda a consumidor final, Modelo 55, Série 1.
- Ao abrir na tela, em **Relação de Notas referenciadas** pegue a chave de acesso e faça a consulta da Nota Fiscal Consumidor Eletrônica (NFC-e) para verificar o número do cupom e se esta autorizado.
- Ainda em Faturamento / Vendas altere o modelo para 65 e informe o número da NFC-e e verifique a venda realizada ao cliente.

## 2. Faturamento / Vendas / Consultar Cupom

- Com o relatório extraído faça a consulta em Nº Pedido do Pedido de venda para verificar a saída feita para o cliente.
- E também em Nº Pedido faça a consulta da Devolução para verificar se os lançamentos estão de acordo com a nota emitida de devolução.
- Pedido de Venda (Sequencial do número de venda).
- Nº Devolução é a solicitação do cliente, ou seja, o sequencial da ordem de devolução.

> ![image](https://github.com/user-attachments/assets/d5cc9748-1914-4d84-bc5a-e97d211f61b5)

## 3. Conferência e validação das informações

- Faça a conferência dos campos próprios (ICMS) se estão em conformidade, dados do cliente, Total da nota, itens (CP), quantidade, Valor, dados fiscais (NCM, CFOP, CST, PIS/COFINS).
- Validar se a Nota de devolução conforme Pedido de devolução (Nº Devolução).

### Transferência entre estabelecimentos da mesma empresa

- Ferro STORE (LOJA) ↔️ Ferro STORE (CD)
  
Operação lançada com CFOP 1.152 na entrada e 5.152 na saída. Não gera direito a crédito de PIS/COFINS, uma vez que se trata de movimentação de estoque entre estabelecimentos da mesma empresa, sem envolvimento financeiro.

**Dados**

- **CFOP:** 1.152 (Entrada)

- **CST PIS/COFINS:** 70 – Operação sem direito a crédito

- **Crédito de PIS/COFINS:** Não se aplica

- **Justificativa:** Operação de transferência de mercadorias entre estabelecimentos do mesmo titular, sem geração de receita ou valor financeiro. Portanto, não gera direito a crédito de PIS/COFINS, conforme previsto na legislação das contribuições.

- **Dados para emissão de nota com a base legal:** Operação de simples transferência entre estabelecimentos da mesma empresa, sem geração de receita, conforme arts. 3º, §2º, II da Lei 10.637/2002 (PIS) e Lei 10.833/2003 (COFINS), art. 3º, §1º da Lei 9.718/1998 e arts. 166 e 167 da IN RFB 1.911/2019. CST 70 – operação sem direito a crédito.

   - Nota fiscal referente à transferência de mercadoria entre filiais da mesma empresa, sem fins comerciais. Operação sem direito a crédito de PIS/COFINS.
 

| TIPO   | CFOP | CST PIS/COFINS | OBSERVAÇÃO |
|---------|----------|---------|----------|
| Entrada | 1.152 | 70 | Operação sem direiro a crédito |
| Saída | 5.152 | 04 | Operação sem incidência (Não tributada) |


## Devolução de fornecedores

### 1. Devolução sem Substituição Tributária (ICMS próprio destacado - TRIBUTADO)

- Devolução de mercadoria recebida como Tributado.

**Dados**

- **CFOP:** 5.102 (Devolução de compra de mercadoria)

- **CST PIS/COFINS:** 010 – Operação tributável com crédito (ou outro conforme caso)

- **Crédito de PIS/COFINS:** Normalmente não gera crédito, pois é operação de devolução.

- **Tratamento do ICMS:** Deve ser destacado o ICMS próprio nos campos próprios da NF-e, com base e valor iguais à operação original.

- **Justificativa:**

   - Devolução que anula operação anterior, conforme art. 57 do RICMS/2000 e Convênio ICMS 54/2000.

   - ICMS próprio destacado normalmente para permitir o estorno do crédito.

- **Base legal:**

   - Art. 57 do RICMS/2000

   - Convênio ICMS 54/2000

   - Arts. 3º, §§ 1º e 2º das Leis 10.637/2002 (PIS) e 10.833/2003 (COFINS)

   - IN RFB 1.911/2019

| TIPO   | CFOP | CST PIS/COFINS | OBSERVAÇÃO |
|---------|----------|---------|----------|
| Saída |	5.102 - 6.102	| 49	| Devolução **sem ICMS-ST**; ICMS próprio destacado no campo próprio da NF-e; sem crédito PIS/COFINS |
| Entrada | 1.102 - 2.102 | 70 | Recebimento da devolução sem direito a crédito de PIS/COFINS, pois não houve geração de receita |

### 2. Devolução com Substituição Tributária (ST)

- Devolução de mercadoria recebida com ICMS-ST.

**Dados**

- **CFOP:** 5.411 (Devolução de compra de mercadoria com ICMS-ST)

- **CST PIS/COFINS:** 010 – Operação tributável com crédito (ou conforme caso)

- **Crédito de PIS/COFINS:** Geralmente não gera crédito, por não ser operação geradora de receita.

- **Tratamento do ICMS e ICMS-ST:**

   - ICMS próprio destacado normalmente no campo próprio da NF-e.

   - ICMS-ST **não deve ser destacado no campo próprio do ICMS da NF-e na devolução**.

   - Base de cálculo e valor do ICMS-ST devem ser informados no campo **“Informações Adicionais de Interesse do Fisco (infAdFisco)”**.

   - Valor do ICMS-ST registrado no campo **“Outras despesas acessórias (vOutro)”** para validação do documento fiscal.

- **Justificativa:**

   - Devolução que anula operação anterior com ST, conforme art. 127, §5º e art. 274, §3º do RICMS/SP e cláusula primeira do Convênio ICMS 54/2000.

   - Necessário informar ICMS-ST nos campos indicados para evitar rejeição pela NF-e.

- **Base legal:**

   - Art. 127, §5º e art. 274, §3º do RICMS/SP

   - Cláusula primeira do Convênio ICMS 54/2000

   - Arts. 3º, §§ 1º e 2º das Leis 10.637/2002 (PIS) e 10.833/2003 (COFINS)

   - IN RFB 1.911/2019

| TIPO   | CFOP | CST PIS/COFINS | OBSERVAÇÃO |
|---------|----------|---------|----------|
| Saída |	5.411 - 6.411	| 49	| Devolução com ICMS-ST; ICMS próprio destacado no campo próprio; valor do ICMS-ST informado em “Outras Despesas Acessórias” e detalhado em “Informações Adicionais”; sem crédito de PIS/COFINS |
| Entrada | 1.411 - 2.411 | 70 | Recebimento da devolução com ICMS-ST; operação sem direito a crédito de PIS/COFINS |

> Exemplo para campo Informações Adicionais (infAdFisco):

```
Devolução referente à NF nº 12345, série 1, de 10/06/2025.
Base de cálculo do ICMS-ST: R$ 5.000,00. Valor do ICMS-ST: R$ 850,00.
Informações conforme art. 127, §5º e art. 274, §3º do RICMS/SP e cláusula primeira do Convênio ICMS 54/2000.
ICMS-ST informado em “Outras Despesas Acessórias” (vOutro), conforme regras da NF-e.
```


### 3. 📄 Resposta à Consulta Tributária 30001/2024 (SP)

**Assunto:** Devolução de mercadoria – Substituição tributária (ICMS-ST) – Documento fiscal – Direito ao crédito

> 🔗 [Resposta à consulta](https://legislacao.fazenda.sp.gov.br/Paginas/RC30001_2024.aspx)

---

#### 4. ✅ Pontos principais:

**🔹 Competência Interestadual**  

O Estado de São Paulo **não regula** a forma de emissão de NF-e por contribuintes de outros Estados, como o Paraná. Portanto, **não opina** sobre a vedação do destaque do ICMS-ST na devolução conforme regras locais.

**🔹 Obrigatoriedade do Destaque (SP)**  

Para que o contribuinte paulista tenha **direito ao crédito do ICMS**, o imposto deve estar **destacado em documento fiscal hábil**, mesmo quando se trata de devolução de mercadoria sujeita à substituição tributária.

**🔹 ICMS Próprio e ST na Devolução**

- O **ICMS próprio** deve ser **destacado nos campos próprios** da NF-e.
- O **ICMS-ST** **não é destacado**, mas deve ser:
  - Informado no campo **"Informações Adicionais de Interesse do Fisco"** (`infAdFisco`), com **base de cálculo e valor**.
  - Lançado no campo **`vOutro` (Outras Despesas Acessórias)** para que o **valor total da NF-e seja validado** pelo sistema.

---

#### 5. 📚 Fundamento Legal:

- **RICMS/SP**:  
  - Art. 127, §5º  
  - Art. 274, §3º  
  - Art. 57  
  - Art. 59, §1º, item 2

- **Convênio ICMS 54/2000**  
- **Decisão Normativa CAT 04/2010**


---

#### 6. ⚠️ Consequência:

Caso o **ICMS próprio não esteja destacado** na NF-e da devolução, **não será permitido o crédito** 
