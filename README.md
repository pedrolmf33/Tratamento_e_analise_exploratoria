# Python - Tratamento e Análise Exploratória de Dados

Este projeto faz parte de uma capacitação em Ciência de Dados e tem como objetivo principal demonstrar técnicas fundamentais de **limpeza, tratamento de dados corrompidos e análise exploratória (EDA)** utilizando a linguagem Python e bibliotecas do ecossistema de dados.

## 📋 Descrição do Projeto

O projeto utiliza um conjunto de dados simulado de uma cadeia de suprimentos (*Campe Supply Corrompido*), que intencionalmente contém diversos problemas comuns em cenários reais de engenharia e análise de dados, tais como:
* Colunas e dados corrompidos / irrelevantes.
* Valores ausentes (nulos) espalhados por quase todo o dataset.
* Inconsistências e erros de digitação em colunas categóricas (como *Setor*, *Produto*, *Vendedor*, *Região*, *Estado* e *Cliente*).
* Atributos numéricos armazenados incorretamente como texto.
* Presença de *outliers* extremos (valores discrepantes) nas colunas de *Faturamento* e *Lucro*.

A partir desse cenário desafiador, o fluxo do projeto percorre desde a inspeção inicial até o tratamento robusto dos dados e a geração de visualizações analíticas para extração de insights de vendas.

---

## 🚀 Tecnologias Utilizadas

O projeto foi desenvolvido em ambiente Jupyter Notebook utilizando as seguintes bibliotecas:
* **Python** (versão 3.x)
* **Pandas**: Para manipulação, limpeza e tratamento do DataFrame.
* **NumPy**: Para operações numéricas de suporte.
* **Matplotlib**: Para construção de gráficos base.
* **Seaborn**: Para visualizações estatísticas avançadas (como boxplots e gráficos de distribuição).

---

## 🗂️ Estrutura do Repositório

```text
├── Python_tratamento_e_analise_exploratoria.ipynb  # Notebook principal contendo todo o código e análises
├── Campe_Supply_Corrompido.csv                     # Dataset original corrompido (base de entrada)
├── Campe_Supply_Tratado.xlsx                       # Dataset final limpo e processado
└── README.md                                       # Documentação do projeto
```

---

## ⚙️ Pré-requisitos e Instalação

Para executar este projeto em sua máquina local, certifique-se de ter o Python instalado juntamente com o gerenciador de pacotes pip.

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```
   
2. Instale as bibliotecas necessárias executando o comando no terminal:
   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl
   ```

3. Abra o Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
   Abra o arquivo `Python_tratamento_e_analise_exploratoria.ipynb` e execute as células sequencialmente.

---

## 🔍 Etapas do Desenvolvimento

1. **Importação de Bibliotecas e Carga dos Dados:** Leitura inicial do arquivo CSV com o Pandas.
2. **Análise Exploratória Inicial (Inspeção):**
   * Verificação de dimensões (`shape`), tipos de dados (`info()`) e contagem de nulos.
   * Identificação de colunas lixo/inúteis (`Sem nome`, `Inutil1`, `Inutil2`).
   * Inspeção detalhada de colunas categóricas para mapear variações e erros de digitação.
3. **Tratamento de Dados:**
   * Exclusão de colunas irrelevantes.
   * Padronização de datas para o formato brasileiro.
   * Tratamento de erros de digitação em variáveis categóricas utilizando correspondência por aproximação (`difflib.get_close_matches`).
   * Tratamento de valores nulos (preenchimento via interpolação/propagação temporal e uso de moda/mediana).
   * Conversão de colunas monetárias/numéricas de string para float.
4. **Tratamento de Outliers:**
   * Utilização de *Boxplots* para detecção visual de valores extremos em *Faturamento* e *Lucro*.
   * Filtragem e remoção de registros anômalos que distorciam as métricas.
5. **Análises e Visualizações:**
   * Gráficos comparativos de faturamento por setor.
   * Análise de faturamento por produto e por vendedor.
   * Distribuição regional das vendas (gráfico de pizza).
   * Avaliação da correlação entre Faturamento e Lucro por meio de gráfico de dispersão (*scatter plot*).

---

## 👤 Autor

Desenvolvido por **[Seu Nome / Membro da Empresa Júnior]**  
*Projeto desenvolvido como parte da capacitação em Ciência de Dados.*