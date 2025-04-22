# Métodos Numéricos - UFRJ (Notebooks)

Este repositório contém Jupyter Notebooks com implementações e exemplos de algoritmos estudados na disciplina de Métodos Numéricos, provavelmente da UFRJ.

## Conteúdo do Repositório

Os notebooks abordam diferentes problemas e métodos:

*   **`1.ipynb`**:
    *   Análise da solução de sistemas lineares `Ax = b` usando a matriz de Hilbert (conhecida por ser mal condicionada).
    *   Cálculo do número de condicionamento da matriz de Hilbert para diferentes dimensões (`n`).
    *   Comparação da solução obtida por `numpy.linalg.solve` com a solução exata, mostrando o aumento do erro relativo com o aumento do número de condicionamento.
    *   Implementação e aplicação do Método dos Gradientes Conjugados (CG) para resolver o sistema.
    *   Aplicação do Refinamento Iterativo para melhorar a solução obtida pelo CG.

*   **`2.ipynb`**:
    *   Modelação do perfil da montanha Fitz Roy a partir de uma imagem.
    *   Seleção de pontos de controle sobre a imagem da montanha.
    *   Aplicação de Interpolação por Spline Cúbica (`scipy.interpolate.CubicSpline`) aos pontos selecionados.
    *   Implementação e aplicação de Curvas de Bézier Paramétricas para ajustar segmentos do perfil.
    *   Visualização dos pontos, da spline e das curvas de Bézier sobrepostas à imagem original.

*   **`3.ipynb`**:
    *   Aplicação do Método dos Mínimos Quadrados (MMQ) para ajustar um polinômio de grau 2 (quadrático) a dados de notificações de dengue ao longo de bimestres (2017-2020).
    *   Construção da tabela com os somatórios necessários para as equações normais do MMQ Quadrático.
    *   Resolução do sistema linear resultante (`numpy.linalg.solve`) para encontrar os coeficientes do polinômio.
    *   Cálculo de um índice sazonal (`ei`) comparando os dados reais com os valores previstos pelo modelo quadrático.

## Tópicos Abordados

*   Resolução de Sistemas Lineares (Métodos Diretos e Iterativos)
*   Matriz de Hilbert
*   Número de Condicionamento
*   Erro Numérico e Estabilidade
*   Método dos Gradientes Conjugados
*   Refinamento Iterativo
*   Interpolação (Spline Cúbica)
*   Ajuste de Curvas (Curve Fitting)
*   Curvas Paramétricas
*   Curvas de Bézier
*   Método dos Mínimos Quadrados (MMQ)
*   Regressão Polinomial (Quadrática)
*   Análise de Dados Temporais (Dengue)

## Tecnologias Utilizadas

*   Python 3
*   Jupyter Notebook
*   NumPy
*   Pandas
*   Matplotlib
*   SciPy (principalmente `interpolate`)
*   Pillow (PIL) (para manipulação de imagens em `2.ipynb`)

## Como Utilizar

1.  **Clone o Repositório:**
    ```
    git clone https://github.com/BayesTheory/MetNum.git
    cd MetNum
    ```
2.  **Crie um Ambiente Virtual (Recomendado):**
    *   Usando `venv`:
        ```
        python -m venv venv
        source venv/bin/activate # Linux/Mac
        # venv\Scripts\activate # Windows
        ```
    *   Usando `conda`:
        ```
        conda create -n metnum python=3.9 # Ou outra versão
        conda activate metnum
        ```
3.  **Instale as Dependências:**
    *   É recomendável criar um arquivo `requirements.txt` com as bibliotecas.
    *   Instale as bibliotecas principais:
        ```
        pip install numpy pandas matplotlib scipy Pillow openpyxl jupyterlab # ou jupyter
        ```
        ou via `conda`:
        ```
        conda install numpy pandas matplotlib scipy Pillow openpyxl jupyterlab # ou jupyter
        ```
4.  **Execute o Jupyter:**
    ```
    jupyter lab
    ```
    ou
    ```
    jupyter notebook
    ```
5.  **Abra os Notebooks:** Navegue pelos arquivos `.ipynb` no seu navegador e execute as células. Certifique-se de que quaisquer arquivos de dados necessários (como imagens ou planilhas, se não carregados via URL) estejam no local esperado.


