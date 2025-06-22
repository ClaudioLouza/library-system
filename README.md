# Sistema de Gerenciamento de Biblioteca

Este projeto implementa um sistema de biblioteca em Java, baseado em Programação Orientada a Objetos, com interface gráfica via `JOptionPane` e persistência de dados em arquivo.

## 📝 Visão Geral
O sistema permite gerenciar livros, autores, usuários e operações de empréstimo e devolução, garantindo controle de disponibilidade e histórico de movimentações.

## ✅ Funcionalidades Principais
- **CRUD de Livros**: adicionar, listar e remover livros.
- **CRUD de Autores**: adicionar, listar e remover autores.
- **CRUD de Usuários**: adicionar, listar e remover usuários.
- **Empréstimos**: registrar empréstimos de livros, decrementando quantidade disponível e gerando prazo de devolução de 14 dias.
- **Devoluções**: registrar devoluções, atualizando data de devolução e incrementando disponibilidade.
- **Persistência**: todos os dados são armazenados em `dados_biblioteca.dat` via serialização Java.

## 📋 Requisitos Funcionais
1. Cadastrar livros com título, editora, ano de publicação, quantidade e lista de autores.
2. Cadastrar autores com nome e nacionalidade.
3. Cadastrar usuários com nome, email e telefone.
4. Registrar empréstimo, verificando disponibilidade e gerando data prevista de devolução.
5. Registrar devolução, atualizando data de devolução e disponibilidade.
6. Impedir remoção de livros ou usuários com empréstimos ativos.
7. Listar entidades (livros, autores, usuários, empréstimos ativos e todos empréstimos).

## ⚙️ Requisitos Não Funcionais
- Interface gráfica simples, intuitiva e baseada em `JOptionPane`.
- Validação de entradas e tratamento de exceções para formatos inválidos.
- Persistência de dados confiável, com tratamento de I/O.
- Código organizado em pacotes e classes seguindo princípios de POO.

## 🚀 Como Compilar e Executar
```bash
# Pré-requisitos:
# - JDK 11 ou superior instalado
# - Variável JAVA_HOME configurada

# Compilar:
javac -d bin src/entities/*.java src/main/Main.java

# Executar:
java -cp bin main.Main
```

## 📄 Persistência de Dados
Todos os objetos são serializados em um único arquivo `dados_biblioteca.dat`. Ao iniciar, o sistema carrega os dados existentes; ao sair, grava o estado atual.
