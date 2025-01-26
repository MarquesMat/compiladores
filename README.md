
# Compilador para MiniJava+

Este repositório contém o desenvolvimento de um compilador para a linguagem **MiniJava+**, implementado como parte do Trabalho I para a disciplina de Compiladores na Universidade Federal Fluminense.

## 📋 Descrição do Projeto

O compilador foi desenvolvido em etapas progressivas, cobrindo desde a análise léxica e sintática até a geração de código para a arquitetura MIPS. As principais etapas do projeto incluem:

1. **Scanner (Analisador Léxico)**:
   - Processa o código-fonte e identifica tokens utilizando expressões regulares.
   - Gera uma tabela de tokens que é consumida nas próximas etapas.

2. **Parser (Analisador Sintático)**:
   - Constrói a árvore sintática utilizando uma abordagem top-down.
   - Ajusta gramáticas eliminando recursões à esquerda para melhorar eficiência.

3. **Análise Semântica**:
   - Utiliza uma tabela de símbolos para garantir que o código segue as regras semânticas da linguagem.
   - Realiza verificações como declaração de variáveis antes do uso e validação de parâmetros em chamadas de funções.

4. **Geração de Código Intermediário**:
   - Converte a árvore sintática abstrata (AST) para uma representação de código intermediário, facilitando a tradução para MIPS.

5. **Otimização**:
   - Realiza otimizações locais, como propagação de cópias e eliminação de redundâncias.

6. **Geração de Código MIPS**:
   - Traduz o código intermediário para instruções compatíveis com a arquitetura MIPS.

## 🛠️ Estrutura do Projeto

- **`main.py`**: Arquivo principal que coordena todas as etapas do compilador.
- **`scanner.py`**: Realiza a análise léxica do código.
- **`parser.py`**: Constrói a árvore sintática e verifica a conformidade com as regras da linguagem.
- **`ast.py`**: Gera a árvore sintática abstrata (AST) para facilitar a geração de código intermediário.
- **`optimizer.py`**: Aplica otimizações locais no código intermediário.
- **`mips.py`**: Realiza a tradução do código otimizado para MIPS.

## 🔧 Tecnologias Utilizadas

- **Python**: Linguagem principal para o desenvolvimento do compilador.
- **Graphviz**: Para visualização da árvore sintática.
- **Regex (`re`)**: Para identificação de padrões no código-fonte.

## 🖥️ Execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/MarquesMat/compiladores.git
   cd compiladores
   ```

2. Execute o compilador com o comando:
   ```bash
   python3 main.py ./minijava/ex1.java
   ```

## ✍️ Autores

- **Lucas Silveira Serrano**
- **Matheus Marques Barros**

---

