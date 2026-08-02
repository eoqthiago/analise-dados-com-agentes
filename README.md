# 🦜 Agente de Análise de Dados com IA

Assistente interativo que usa um agente [LangChain](https://www.langchain.com/) para explorar, analisar e visualizar dados de forma conversacional, direto de um app [Streamlit](https://streamlit.io/).

Basta fazer upload de um CSV e conversar com os seus dados.

---

## ✨ Funcionalidades

- 📄 **Relatório de informações gerais** — dimensões do dataset, tipos de coluna, nulos, valores `"nan"` como texto e duplicados.
- 📊 **Relatório de estatísticas descritivas** — média, desvio padrão, mínimo, máximo, outliers e sugestões de próximos passos.
- 🔎 **Perguntas em linguagem natural** — "Qual a média do tempo de entrega?", "Qual a correlação entre X e Y?".
- 📈 **Geração de gráficos automática** — peça um gráfico descrevendo o que quer ver, e o agente escreve e executa o código com `matplotlib`/`seaborn`.

---

## 🛠️ Tecnologias

| Camada | Ferramenta |
|---|---|
| Interface | [Streamlit](https://streamlit.io/) |
| Orquestração do agente | [LangChain](https://www.langchain.com/) (agente ReAct) |
| LLM | [Groq](https://groq.com/) |
| Dados | [pandas](https://pandas.pydata.org/) |
| Gráficos | [matplotlib](https://matplotlib.org/) / [seaborn](https://seaborn.pydata.org/) |

---

## 🚀 Como rodar

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/nome-do-repo.git
cd nome-do-repo
```

### 2. Crie e ative um ambiente virtual

```bash
python -m venv .venv

# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Linux / macOS
source .venv/bin/activate
```

### 3. Instale as dependências

```bash
pip install streamlit pandas python-dotenv "langchain<1.0" langchain-groq langchain-experimental langchain-community tabulate matplotlib seaborn
```

### 4. Configure sua chave da Groq

Crie um arquivo `.env` na raiz do projeto:

```env
GROQ_API_KEY=sua_chave_aqui
```

> Obtenha uma chave gratuita em [console.groq.com](https://console.groq.com/).

### 5. Rode o app

```bash
streamlit run App.py
```

O app abre automaticamente em `http://localhost:8501`.

---

## 📁 Estrutura do projeto.
├── App.py <br>
├── ferramentas.py<br>
├── .env<br>
└── .gitignore<br>

App.py           -> Interface Streamlit e orquestração do agente<br>
ferramentas.py   -> Ferramentas do agente: relatórios, estatísticas e gráficos<br>
.env             -> Chave de API (não versionado)<br>
.gitignore       -> Arquivos ignorados pelo Git<br>

