# Leitor-Automatizado-de-Notas-Fiscais-XML-e-PDF-
Este projeto em Python foi desenvolvido para automatizar a extração, processamento e estruturação de dados de Notas Fiscais Eletrônicas (NF-e) e Notas Fiscais de Serviços (NFS-e) a partir de arquivos nos formatos XML e PDF


# 📄 Leitor e Extrator de Notas Fiscais (NF-e & NFS-e)

Este projeto em Python realiza a leitura, parsing e estruturação automatizada de dados provenientes de Notas Fiscais Eletrónicas (NF-e) e Notas Fiscais de Serviços (NFS-e), suportando ficheiros nos formatos XML e PDF.

A ferramenta é capaz de identificar automaticamente o tipo de documento fiscal, extrair campos chave (como dados do emitente, destinatário, valores totais e detalhamento de itens) e exportar as informações consolidadas para tabelas em Excel (`.xlsx`) ou estruturas de dados reutilizáveis.

---

## 🚀 Funcionalidades

- **Processamento em Lote:** Varredura automática de diretórios para processar múltiplos ficheiros XML e PDF.
- **Suporte Multi-Formato Fiscal:**
  - **NF-e (Produtos):** Extração de dados da chave de acesso, emitente, comprador, impostos (ICMS, IPI, PIS, COFINS) e lista individualizada de produtos.
  - **NFS-e (Serviços):** Identificação e extração de notas de serviço municipais (como a Nota Carioca).
- **Tratamento de Exceções:** Validação da estrutura XML para ignorar ficheiros incompatíveis ou corrompidos sem interromper a execução.
- **Exportação de Dados:** Conversão direta de listas de produtos e informações da nota em DataFrames do `pandas` e exportação para ficheiros Excel.

---

## 🛠️ Tecnologias Utilizadas

- **[Python](https://www.python.org/)** (v3.x)
- **[pandas](https://pandas.pydata.org/)** — Manipulação e estruturação de dados.
- **[xmltodict](https://github.com/martinblech/xmltodict)** — Conversão de documentos XML em dicionários nativos do Python.
- **[openpyxl](https://openpyxl.readthedocs.io/)** — Suporte para geração e exportação de ficheiros `.xlsx`.
- **[Jupyter Notebook](https://jupyter.org/)** — Ambiente de desenvolvimento e execução interativa (`main.ipynb`).

---

## 📂 Estrutura do Repositório

```text
.
├── DANFEBrota.pdf          # Exemplo de DANFE em PDF
├── DANFEBrota.xml          # Exemplo de NF-e em XML
├── DANFENespresso.pdf      # Exemplo de DANFE em PDF
├── DANFENespresso.xml      # Exemplo de NF-e em XML
├── NotaCariocaHashtag.pdf  # Exemplo de NFS-e em PDF
├── NotaCariocaHashtag.xml  # Exemplo de NFS-e em XML
├── main.ipynb              # Notebook principal com o código de extração
└── README.md               # Documentação do projeto
