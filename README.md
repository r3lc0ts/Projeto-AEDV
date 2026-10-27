# Chegadas Internacionais ao Brasil (1989–2026)

Projeto desenvolvido para a disciplina de **Análise Exploratória de Dados e Visualização** (2026.2) da Escola de Matemática Aplicada da Fundação Getulio Vargas (**FGV EMAp**), ministrada pelo Prof. João Rulff.

## Integrantes do Grupo
* Artur Lacerda Pugoni [(github.com/Pugoni)]
* Guilherme da Cunha Fonseca [(github.com/14guifonseca)]
* Sarah Felix Stocler [(github.com/r3lc0ts)]

---

## Fonte dos Dados
Os dados abrangem o período de **janeiro de 1989 a agosto de 2026** e foram coletados a partir de registros administrativos de entrada e saída da Polícia Federal nos postos de fronteira, disponibilizados pelo Ministério do Turismo no Portal Brasileiro de Dados Abertos:
* **Link oficial:** [Estimativas de Chegadas de Turistas Internacionais ao Brasil - dados.gov.br](https://dados.gov.br/dados/conjuntos-dados/estimativas-de-chegadas-de-turistas-internacionais-ao-brasil)

---

## Estrutura do Repositório

```text
├── data/
│   ├── raw/                  # Tabelas brutas em CSV (ignoradas no Git via .gitignore)
│   └── processed/            # Base consolidada, padronizada e limpa (chegadas_limpo.csv)
├── notebook/
│   └── notebook_turismo.ipynb # Notebook principal estruturado em formato de artigo
├── .gitignore                # Arquivos e diretórios ignorados pelo controle de versão
├── environment.yml           # Especificação do ambiente Conda para reprodutibilidade
└── README.md                 # Documentação do projeto
```

---

## Reprodutibilidade

Para garantir que as análises e os gráficos sejam executados com exatamente as mesmas versões de Python (`3.12`) e das bibliotecas utilizadas pelo grupo (`pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`), utilizamos o gerenciador de ambientes **Conda**.

**Recrie o ambiente virtual a partir do arquivo `environment.yml`:**
Abra o **Anaconda Prompt**, navegue até a pasta do projeto e execute:
```bash
conda env create -f environment.yml
conda activate projeto_turismo
```

**Execute o Notebook:**
* **Pelo Visual Studio Code:** Abrir a pasta do projeto no VS Code, abra o arquivo `notebook/notebook_turismo.ipynb` e, no canto superior direito (*Select Kernel*), selecionar o ambiente **`projeto_turismo (Python 3.12)`**.
* **Pelo Jupyter Lab (Navegador):** Com o ambiente `projeto_turismo` ativo no Anaconda Prompt, digite `jupyter lab` e abra o arquivo `notebook/notebook_turismo.ipynb`.

> ** Solução de problemas no Windows (VS Code):** Caso ocorra o erro `"Failed to start the Kernel"` ao tentar rodar a primeira célula no Windows, executar o comando abaixo no seu Anaconda Prompt (com o ambiente `projeto_turismo` ativo) para reinstalar o comunicador do kernel e, em seguida, recarregar a janela do VS Code:
> ```bash
> pip uninstall pyzmq ipykernel tornado -y && pip install pyzmq ipykernel tornado
> ```