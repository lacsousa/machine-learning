# Machine Learning - Estudos e Práticas (Alura)

Repositório contendo exercícios e projetos de Machine Learning desenvolvidos a partir dos cursos da Alura, com foco em algoritmos de classificação, preparação de dados, métricas de validação e visualização gráfica.

---

## 📁 Estrutura do Repositório

```text
machine-learning/
├── alura/
│   ├── Dados/                          # Datasets utilizados nos cursos
│   │   ├── precos.csv
│   │   ├── projects.csv
│   │   └── tracking.csv
│   └── codigo/                         # Notebooks Jupyter e códigos das aulas
│       ├── Introd-Classif-video_1_3.ipynb
│       ├── Introd-Classif-video_1_4.ipynb
│       ├── Introd-Classif-video_2_1.ipynb
│       ├── Introd-Classif-video_2_2.ipynb
│       ├── Introd-Classif-video_3_1.ipynb
│       ├── Introd-Classif-video_3_2.ipynb
│       ├── Introd-Classif-video_4_1.ipynb
│       ├── Introd-Classif-video_5_1.ipynb
│       ├── Introd-Classif-video_5_2.ipynb
│       └── Introd-Classif-video_5_3.ipynb
├── .gitignore                          # Arquivos e pastas ignorados pelo Git (.venv, etc.)
└── README.md                           # Documentação do projeto
```

---

## 🛠️ Tecnologias e Bibliotecas

- **[Python 3.12](https://www.python.org/)**
- **[uv](https://github.com/astral-sh/uv)**: Gerenciador de ambientes e pacotes Python de alta performance
- **[scikit-learn](https://scikit-learn.org/)**: Algoritmos de Machine Learning (`LinearSVC`, `SVC`, `DummyClassifier`, `train_test_split`, `accuracy_score`, `StandardScaler`, etc.)
- **[pandas](https://pandas.pydata.org/)** e **[numpy](https://numpy.org/)**: Carga, manipulação e tratamento de dados
- **[matplotlib](https://matplotlib.org/)** e **[seaborn](https://seaborn.pydata.org/)**: Visualização de dados e gráficos estatísticos
- **[graphviz](https://graphviz.org/)**: Renderização de árvores de decisão
- **[ipykernel](https://ipython.org/)**: Execução dos notebooks interativos no Jupyter / VS Code

---

## 🚀 Configuração do Ambiente com `uv`

Para garantir reprodutibilidade e isolamento, o projeto utiliza um ambiente virtual (`.venv`) gerenciado pelo `uv`.

### 1. Pré-requisito
Certifique-se de ter o `uv` instalado na máquina:
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### 2. Criação do Ambiente Virtual
Na raiz do repositório, crie o ambiente virtual:
```bash
uv venv --python 3.12
```

### 3. Instalação das Dependências
Instale todos os pacotes necessários utilizando o `uv pip`:
```bash
uv pip install scikit-learn pandas numpy matplotlib seaborn graphviz ipykernel
```

### 4. Registro do Kernel no Jupyter (Opcional, mas recomendado)
Para disponibilizar o ambiente no seletor de kernels do VS Code e Jupyter:
```bash
.venv/bin/python -m ipykernel install --user --name machine-learning --display-name "Python (machine-learning .venv)"
```

---

## ▶️ Como Rodar os Arquivos do Projeto

### Opção 1: Executar pelo VS Code / Antigravity IDE (Recomendado)
1. Abra qualquer notebook na pasta `alura/codigo/` (por exemplo: `alura/codigo/Introd-Classif-video_1_3.ipynb`).
2. No canto superior direito do editor do notebook, clique em **Select Kernel**.
3. Escolha **Python Environments...** e selecione o ambiente local **`.venv`** (ou selecione **`Python (machine-learning .venv)`** na lista de Jupyter Kernels).
4. Execute as células sequencialmente (`Shift + Enter` ou o botão **Run All**).

### Opção 2: Executar no Terminal usando `uv run`
Se converter ou rodar scripts Python diretamente:
```bash
# Ativando o ambiente virtual:
source .venv/bin/activate
python alura/codigo/<seu_arquivo>.py

# Ou diretamente com o uv sem precisar ativar o shell:
uv run python alura/codigo/<seu_arquivo>.py
```

### Opção 3: Iniciar o Jupyter Lab / Notebook via Web
Se preferir utilizar a interface web do Jupyter:
```bash
source .venv/bin/activate
uv pip install jupyterlab
jupyter lab
```
Navegue até a pasta `alura/codigo/` e abra o notebook desejado.
