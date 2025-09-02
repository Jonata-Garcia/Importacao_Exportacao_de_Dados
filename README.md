# 📊 Importação e Manipulação de Arquivos no Google Colab com Python

Este projeto demonstra como **importar, visualizar e manipular arquivos** dentro do **Google Colab**, utilizando a biblioteca **Pandas** e o módulo `files` do próprio Colab.  
O código está dividido em três partes principais: **upload de arquivos**, **leitura de planilhas Excel** e **visualização dos dados**.

---

## 1️⃣ Upload de arquivos para o Colab
O primeiro trecho de código utiliza o módulo `files.upload()` para enviar arquivos do computador para o ambiente do Colab.  

```python
from google.colab import files

uploaded = files.upload()

for fn in uploaded.keys():
    print('Arquivo "{name}" com tamanho de {length} bytes'.format(
        name=fn, length=len(uploaded[fn])))


## 2️⃣ Leitura de planilhas e listagem de arquivos
Na segunda parte, o código mostra como ler arquivos Excel diretamente com a função pd.read_excel(), armazenando os dados em um DataFrame do Pandas.
import pandas as pd

Dados1 = pd.read_excel('20Nomes (1).xlsx')

print(Dados1)         # Exibe todos os dados
print(Dados1.shape)   # Mostra quantidade de linhas e colunas

!ls  # Lista todos os arquivos no diretório do Colab


## 3️⃣ Visualização parcial dos dados
Por fim, o código lê outra planilha Excel e usa funções do Pandas para inspecionar rapidamente os dados:

Dados2 = pd.read_excel('20Nomes.xlsx')

print(Dados2.head())   # Mostra as 5 primeiras linhas
print(Dados2.shape)   # Mostra linhas e colunas

