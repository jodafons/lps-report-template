# 💠 LPS Report Template | COPPE/UFRJ


Um template LaTeX moderno, profissional e altamente customizável para relatórios técnicos do **Laboratório de Processamento de Sinais (LPS)**. Baseado nos padrões da COPPE/UFRJ, este template oferece uma estética *premium* com capas dinâmicas, gerenciamento modular de metadados e estrutura organizada para grandes projetos de pesquisa.

---

## 🚀 Destaques

- **💎 Design Premium:** Capa técnica com fundo azul profundo, logotipos institucionais e tipografia moderna.
- **🧩 Estrutura Modular:** Metadados, pacotes e capítulos separados para facilitar a manutenção.
- **📊 Gestão de Identidade:** Página de "Laboratórios e Logomarcas" automática com alinhamento vertical e controle de proporção individual.
- **📈 Automatizado:** Sumários, listas de figuras, tabelas, abreviações e símbolos gerados dinamicamente.
- **🛠️ Eficiente:** Makefile para compilação completa (BibTeX + Índices) de forma simplificada em um comando.

---

## 📂 Estrutura do Projeto

```text
├── main.tex                 # Arquivo principal (ponto de entrada)
├── Makefile                 # Automação de compilação
├── metadatas/               # Configurações do documento
│   ├── infos.tex            # Título, autores, cliente final e laboratórios (CRUD)
│   ├── packages.tex         # Pacotes LaTeX adicionais
│   ├── executive.tex        # Resumo executivo
│   ├── bibliography.bib     # Base de referências Bibliográficas
│   └── abreviations.tex     # Lista de abreviaturas/acrônimos
├── sections/                # Seções e Capítulos do relatório
│   └── 01_chapter/          # Exemplo de capítulo modular
└── template/                # Arquivos de estilo e classe
    ├── coppe.cls            # Classe principal (lógica do layout)
    └── logos/               # Logotipos institucionais padrão
```

---

## ⚙️ Como Configurar

Toda a personalização do relatório é feita de forma centralizada nos arquivos da pasta `metadatas/`.

### 1. Metadados do Projeto (`metadatas/infos.tex`)
Edite as definições para refletir os dados reais:
- `\projecttitle{...}`: Nome do projeto global.
- `\finalclient{...}`: Nome do cliente final (ex: Petrobras), exibido na folha de rosto.
- `\author{Nome}{Sobrenome}`: Autor principal do documento.
- `\coordinatorsignature{...}`: Caminho para a imagem da assinatura do coordenador (ex: `metadatas/signatures/assinatura.pdf`).
- `\authorreport{Sigla}{Nome Completo}{Título}`: Cadastro para página de assinaturas.

### 2. Gestão de Laboratórios e Logos
A página de **Laboratórios e Logomarcas** é gerada automaticamente. Você cadastra os laboratórios participantes em `metadatas/infos.tex` com o comando:
```latex
\laboratory{Nome Completo}{Sigla}{Caminho/Logo.pdf}{Proporção}
```
- **Proporção:** Um valor entre 0 e 1 (ex: `0.7`) que define a largura da imagem em relação à coluna, permitindo equilibrar visualmente logos de diferentes formatos.
- **Dica:** O template garante altura fixa de **2.2cm** e centralização total (horizontal/vertical) para um visual limpo e institucional.

### 3. Conteúdo e Fluxo
- **Resumo Executivo:** Edite `metadatas/executive.tex`.
- **Glossário:** Cadastre siglas em `metadatas/abreviations.tex`.
- **Capítulos:** Adicione novos `.tex` em `sections/` e use `\input{...}` no `main.tex`.

---

## 🛠️ Compilação

Para compilar o relatório com todas as referências cruzadas e bibliografia:

```bash
# Recomendado: Limpar e compilar do zero
make clean && make
```

Isso gera o arquivo `main.pdf` com todas as dependências resolvidas (PDFLaTeX + BibTeX + MakeIndex).

---

## 🎨 Personalização Visual

As cores institucionais do LPS são definidas na classe `coppe.cls`:
- **MyBlue:** `#0F2C4B` (Azul Profundo LPS/UFRJ)
- **MyYellow:** `#C0D700` (Destaque LPS)
- **Alert:** `#C21F30` (Avisos Críticos)

---

## 📄 Requisitos

- Distribuição LaTeX moderna (TeX Live 2022+ ou MiKTeX).
- Binários `pdflatex`, `makeindex` e `bibtex` acessíveis via terminal.

---
*Template oficial para relatórios técnicos do LPS/COPPE/UFRJ.*
