# Sumarização de Texto com Hugging Face Transformers

Este projeto demonstra a capacidade de um modelo de linguagem pré-treinado para realizar a sumarização de texto. Utilizando a biblioteca `transformers` da Hugging Face, o projeto permite gerar resumos concisos a partir de textos mais longos, destacando as informações mais relevantes.

## Visão Geral

A sumarização de texto é uma tarefa fundamental no Processamento de Linguagem Natural (PLN) que visa criar uma versão mais curta e coerente de um documento, mantendo seu significado principal. Este projeto utiliza o modelo `sshleifer/distilbart-cnn-12-6`, que é uma versão otimizada do BART, projetada especificamente para tarefas de sumarização. O modelo é capaz de realizar sumarização **abstrativa**, ou seja, ele pode gerar novas frases e reformular informações, em vez de apenas extrair frases existentes do texto original.

## Estrutura do Projeto

* `Resumo.ipynb`: O notebook Jupyter que contém todo o código para configurar o ambiente, carregar o modelo e gerar resumos.

## Tecnologias Utilizadas

* **Python 3**
* **Hugging Face `transformers` library**: Para acesso e utilização do modelo de sumarização.
* **Jupyter Notebook**: Para execução e demonstração interativa do código.
* **Modelo**: `sshleifer/distilbart-cnn-12-6` (modelo pré-treinado para sumarização).

## Exemplo de Uso

No notebook, você pode substituir o `texto` de exemplo por qualquer outro texto que deseje resumir. Os parâmetros `max_length` e `min_length` controlam o comprimento do resumo gerado.

```python
texto_para_resumir = """
[Cole seu texto longo aqui. Pode ser um artigo, um parágrafo grande, etc.]
"""

resumo_gerado = resumir(texto_para_resumir, max_length=150, min_length=80)
print(resumo_gerado[0]['summary_text'])
