# 💠 LPS Report Template | COPPE/UFRJ

[![LaTeX](https://img.shields.io/badge/LaTeX-Project-blue?style=for-the-badge&logo=latex)](https://www.latex-project.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://opensource.org/licenses/MIT)

Um template LaTeX moderno, profissional e altamente customizável para relatórios técnicos do **Laboratório de Processamento de Sinais (LPS)**. Baseado nos padrões da COPPE/UFRJ, este template oferece uma estética *premium* com capas dinâmicas, gerenciamento modular de metadados e estrutura organizada para grandes projetos de pesquisa.

---

## 🚀 Destaques

- **💎 Design Premium:** Capa técnica com fundo azul profundo, logotipos institucionais e tipografia moderna.
- **🧩 Estrutura Modular:** Metadados, pacotes e capítulos separados para facilitar a manutenção.
- **📈 Automatizado:** Sumário, lista de figuras, tabelas, abreviações e símbolos gerados automaticamente.
- **🛠️ Pronto para Uso:** Inclui `Makefile` para compilação completa (BibTeX + Índices).

---

## 📂 Estrutura do Projeto

```text
├── main.tex                 # Arquivo principal (ponto de entrada)
├── Makefile                 # Automação de compilação
├── metadatas/               # Configurações do documento
│   ├── infos.tex            # Título, autores, coordenadores, etc.
│   ├── packages.tex         # Pacotes LaTeX adicionais
│   ├── executive.tex        # Resumo executivo
│   ├── bibliography.bib     # Base de referências Bibliográficas
│   └── abreviations.tex     # Lista de abreviaturas
├── sections/                # Seções e Capítulos do relatório
│   └── 01_chapter/          # Exemplo de capítulo modular
└── template/                # Arquivos de estilo e classe
    ├── coppe.cls            # Classe principal do relatório
    └── logos/               # Logotipos (LPS, UFRJ, etc.)
```

---

## ⚙️ Como Configurar

Toda a personalização do relatório é feita de forma centralizada na pasta `metadatas/`.

### 1. Informações do Projeto (`metadatas/infos.tex`)
Edite este arquivo para definir os dados principais:
- `\projecttitle{...}`: Título principal do projeto.
- `\title{...}`: Título específico deste relatório.
- `\author{Nome}{Sobrenome}`: Autor principal.
- `\authorreport{...}`: Lista completa de autores para a página de assinaturas.
- `\cooperationterm{...}`: Número do Termo de Cooperação.
- `\reportversion{1.0}`: Versão atual do documento.

### 2. Pacotes e Dependências (`metadatas/packages.tex`)
Adicione qualquer pacote extra que seu documento necessite (ex: `tcolorbox`, `amsmath`, etc).

### 3. Conteúdo (`sections/`)
Crie novas pastas ou arquivos dentro de `sections/` e use `\input{...}` no seu `main.tex` para manter o projeto organizado.

---

## 🛠️ Compilação

Para compilar o relatório com todas as referências e índices, utilize o comando `make` no terminal:

```bash
# Limpar arquivos temporários antigos
make clean

# Compilar o relatório completo (gera o main.pdf)
make
```

O `Makefile` cuidará de todas as passagens necessárias (`pdflatex`, `bibtex`, `makeindex`).

---

## 🎨 Personalização Visual

As cores principais são definidas em `template/coppe.cls`:
- **MyBlue:** `#0F2C4B` (Azul Profundo LPS)
- **MyYellow:** `#C0D700` (Verde/Amarelo destaque)
- **Alert:** `#C21F30` (Vermelho para avisos)

Você pode ajustar essas definições diretamente na classe se precisar seguir uma nova identidade visual.

---

## 📄 Requisitos

- Distribuição LaTeX completa (TeX Live 2022+ ou MiKTeX).
- Binário `pdflatex` no PATH.
- Ferramentas `makeindex` e `bibtex` (inclusas na maioria das distribuições).

---
*Desenvolvido para pesquisadores do LPS/COPPE/UFRJ.*
