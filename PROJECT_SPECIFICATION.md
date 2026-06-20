# ESPECIFICAÇÃO DO PROJETO ECO-GESTÃO

## VISÃO GERAL

O ECO-Gestão é um sistema financeiro e gerencial offline desenvolvido para controle interno de duas empresas do mesmo grupo empresarial:

* **ECOVIVA BRASIL TRADING**
* **ECOVIVA BRASIL LOJA**

O sistema deve funcionar como um **ERP financeiro simplificado**, com foco em controle de resultados mensais, lucratividade, vendas e despesas operacionais.

Ele será utilizado pela gestão financeira para análise de desempenho, fechamento mensal e tomada de decisão estratégica.

---

## PRINCÍPIO FUNDAMENTAL DO SISTEMA

O sistema não é um CRM nem um sistema de estoque.

**O foco é exclusivamente financeiro e gerencial.**

Toda operação deve refletir em:

* Receita
* Despesa
* Lucro
* Indicadores por vendedor
* Resultado mensal consolidado

---

## ESTRUTURA MULTIEMPRESA

O sistema possui duas empresas totalmente independentes.

### Regras obrigatórias:

* Nenhum dado pode ser compartilhado entre empresas
* Cada empresa possui seu próprio caixa, relatórios e histórico
* Todos os módulos devem ser filtrados por empresa ativa
* O usuário escolhe a empresa antes de operar

---

## FLUXO FINANCEIRO DO SISTEMA

O sistema trabalha com fluxo simples:

### RECEITAS

Entradas de dinheiro acontecem apenas por:

* Vendas de scooters
* Vendas de peças
* Outras receitas eventuais (se houver)

**Toda venda entra imediatamente no caixa.**

---

### DESPESAS

Saídas de dinheiro acontecem por:

* Garantias
* Salários
* Comissões de vendedores
* Contas a pagar
* Despesas gerais

**Toda despesa impacta diretamente o resultado do mês.**

---

## REGRA DE FECHAMENTO MENSAL

O sistema funciona por ciclo mensal.

Ao final de cada mês:

1. Todos os dados do mês são consolidados
2. Um relatório gerencial completo é gerado automaticamente em PDF
3. O mês é arquivado permanentemente
4. Um novo ciclo mensal é iniciado
5. Nenhum dado do mês anterior pode ser alterado após fechamento (modo auditoria)

---

## REGRA DE COMISSIONAMENTO (MUITO IMPORTANTE)

As comissões são calculadas automaticamente com base no volume de vendas de scooters por vendedor no mês.

### Faixas de Comissão:

* **1 a 50 scooters** → 3%
* **51 a 170 scooters** → 4%
* **171 ou mais** → 4,5%

### Regras adicionais:

* O cálculo é feito no fechamento do mês
* A base de cálculo é o valor total de vendas do vendedor no mês
* A comissão vira uma obrigação financeira (despesa futura)
* Quando paga, vira despesa efetiva
* O sistema deve mostrar:
  * Comissão gerada
  * Comissão pendente
  * Comissão paga

---

## GARANTIAS

Garantias representam custos operacionais.

### Regras:

* Toda garantia é uma despesa direta
* Impacta imediatamente o resultado do mês
* Deve ser registrada por mês, não por item individual

---

## MODELO DE VENDAS

### Vendas de Scooters

* Registradas por mês
* Associadas a vendedor
* Geram receita imediata

### Vendas de Peças

* Registradas por mês
* Associadas a vendedor
* Geram receita imediata

---

## INDICADORES GERENCIAIS

O sistema deve fornecer visão executiva com:

* Receita total mensal
* Despesa total mensal
* Lucro líquido
* Ranking de vendedores
* Volume de vendas por vendedor
* Evolução mensal
* Comparativo histórico

---

## RELATÓRIO GERENCIAL MENSAL (CORE DO SISTEMA)

Todo mês o sistema deve gerar automaticamente um relatório executivo contendo:

### RECEITAS

* Scooters
* Peças
* Total geral

### DESPESAS

* Garantias
* Salários
* Comissões
* Contas a pagar
* Despesas gerais

### RESULTADO

* Receita total
* Despesa total
* Lucro líquido

### ANÁLISE EXECUTIVA

* Melhor vendedor do mês
* Ranking de vendas
* Evolução mensal
* Tendência de crescimento

**O relatório deve ser exportado em PDF com layout executivo profissional.**

---

## HISTÓRICO MENSAL

* Cada mês é armazenado como um "snapshot fechado"
* Não pode ser alterado após fechamento
* Deve ser possível consultar qualquer mês anterior
* Deve ser possível reimprimir relatórios

---

## REQUISITOS TÉCNICOS DO SISTEMA

* **Funcionar 100% offline**
* **Banco de dados local** (SQLite)
* **Aplicação desktop** (preferencialmente Electron)
* **Exportação PDF** profissional
* **Interface moderna** e executiva
* **Suporte a modo claro e escuro**
* **Suporte a português e chinês simplificado**

---

## OBJETIVO FINAL

O ECO-Gestão deve funcionar como um sistema de controle gerencial executivo capaz de responder:

* **Quanto entrou**
* **Quanto saiu**
* **Quanto sobrou**
* **Quem vendeu mais**
* **Qual empresa performou melhor**
* **Qual mês foi mais lucrativo**

Com total rastreabilidade mensal e histórico confiável para gestão empresarial.

---

## STACK TECNOLÓGICO RECOMENDADO

* **Frontend**: React / Electron
* **Backend**: Node.js / Python
* **Banco de Dados**: SQLite
* **Geração de PDF**: PDFKit / ReportLab
* **Linguagem**: JavaScript/TypeScript
* **Versionamento**: Git

---

## STATUS DO PROJETO

🔄 Em desenvolvimento
