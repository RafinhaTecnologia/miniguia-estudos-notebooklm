# 📚 Guia Definitivo de Bancos de Dados: Caderno Temático com NotebookLM

Este repositório apresenta o desenvolvimento de um Caderno Temático inteligente estruturado no **NotebookLM**, utilizando Inteligência Artificial como ferramenta de aprendizagem ativa para dominar o universo de Bancos de Dados relacionais do absoluto zero, unindo teoria acadêmica e aplicação prática em sistemas de gestão.

---

## 🎯 1. Contexto e Objetivos

* **Assunto Escolhido:** Modelagem de Dados Relacional, Arquitetura de Bancos de Dados e Linguagem SQL (com foco prático no desenvolvimento de sistemas de gestão empresarial, como o *Rafinha Tecnologia*).
* **Objetivos de Estudo:** 
  * Compreender os fundamentos teóricos e práticos de modelagem de dados (Entidades, Atributos, Relacionamentos, MER/DER).
  * Aprender a estruturação lógica e física de tabelas relacionais, aplicando com rigor Chaves Primárias (PK) e Estrangeiras (FK).
  * Dominar os comandos iniciais de SQL (DDL e DML) conectando a teoria a cenários reais de negócio (como controle de comandas para restaurantes e gestão de estoque).
  * Consolidar o uso de fontes acadêmicas e técnicas confiáveis com rigor de citação.

---

## 🔍 2. Curadoria de Fontes

Fontes abertas e documentações técnicas selecionadas e carregadas no NotebookLM para fundamentar os estudos:

| # | Título | Tipo | Link / Referência |
|---|--------|------|-------------------|
| 1 | Database Design for Mere Mortals (Michael J. Hernandez) | Livro / PDF | Referência teórica para projeto lógico e estruturação de dados |
| 2 | Database System Concepts (Abraham Silberschatz et al.) | Livro / PDF | Fundamentos teóricos e propriedades ACID de bancos de dados |
| 3 | Documentação Oficial PostgreSQL (SQL Reference) | Web / Documentação | [PostgreSQL SQL Documentation](https://www.postgresql.org/docs/current/sql.html) |
| 4 | W3Schools SQL Tutorial & Reference | Web / Guia Prático | [W3Schools SQL Tutorial](https://www.w3schools.com/sql/) |
| 5 | Stanford Online: Databases (Modeling and Theory) | Curso / Referência | [Stanford Databases Course](https://online.stanford.edu/courses/soe-ydatabases0003-databases-modeling-and-theory) |

---

## ⚙️ 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Durante a construção do ambiente de estudos no NotebookLM, foram testadas diferentes abordagens de prompts para garantir que a IA atuasse estritamente como um professor sênior de engenharia de dados, sem dispersar para áreas de lógica de programação pura ou front-end.

### 🔄 Evolução e Testes de Prompts

* **Prompt Inicial (Genérico):** Focava excessivamente em lógica genérica e linguagens de back-end (C#/Python), o que gerava desvios do núcleo central em bancos de dados.
* **Prompt Ajustado (Definitivo):** O prompt foi refinado e fixado nas instruções do notebook para isolar o ecossistema de dados, exigindo rigor técnico, modelagem voltada a negócios reais (restaurantes e lojas) e obrigatoriedade de citação nas respostas da IA.

> **Exemplo de Prompt Utilizado no NotebookLM:**
> *"Atue como um Professor Sênior de Engenharia de Dados e Bancos de Dados particular. Meu objetivo é dominar Banco de Dados do absoluto zero, absorvendo o máximo de conhecimento técnico e teórico das fontes fornecidas neste notebook. Explique com rigor técnico e didático como estruturar tabelas, normalização e transformar um diagrama (DER/MER) em um modelo físico relacional robusto."*

### 🛠️ Desafios Encontrados (Cicatrizes do Processo)
* **Restrições de Importação por URL:** Diversos links web (como páginas do LeetCode, Beecrowd e biografias acadêmicas da ACM) apresentaram barreiras de segurança anti-bot ou restrições de fonte do NotebookLM (*"Não foi possível importar esta página da Web devido a restrições de fonte"*).
* **Solução Adotada:** Substituição gradual das URLs problemáticas por documentações abertas em texto plano, guias oficiais de SQL compatíveis e priorização de materiais consolidados em PDF e referências acadêmicas diretas.

---

## 📖 4. Miniguia de Estudo (Entrega Final)

### 📌 Resumos Estruturados
1. **Modelagem Conceitual:** Extração de requisitos do mundo real definindo **Entidades** (ex: `Mesa`, `Comanda`, `Produto`), seus **Atributos** e a cardinalidade dos **Relacionamentos** (1:N e N:N, resolvidos com tabelas associativas como `ItemComanda`).
2. **Modelagem Lógica:** Mapeamento conceitual para tabelas bidimensionais através de **Chaves Primárias (PK)** para unicidade de registros e **Chaves Estrangeiras (FK)** para garantia de integridade referencial.
3. **Criação de Estruturas (DDL):** Aplicação prática de comandos SQL para a criação de tabelas e restrições de integridade. Exemplo prático estruturado durante os estudos:

```sql
-- 1. Criação da tabela de Mesas
CREATE TABLE Mesa (
    id_mesa INT PRIMARY KEY,
    numero INT NOT NULL,
    capacidade INT NOT NULL
);

-- 2. Criação da tabela de Comandas com integridade referencial
CREATE TABLE Comanda (
    id_comanda INT PRIMARY KEY,
    data_hora DATETIME NOT NULL,
    status VARCHAR(20) NOT NULL,
    id_mesa INT NOT NULL,
    FOREIGN KEY (id_mesa) REFERENCES Mesa(id_mesa)
);