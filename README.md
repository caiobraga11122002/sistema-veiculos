# Sistemas-veiculos
Projeto aula 12 sobre sistema de veículos

Atividade para domingo 

# 📌 Projeto: Sistema de Veículos - Desenvolvimento Colaborativo com GitHub

Este repositório contém um projeto simples de **herança em Java**, desenvolvido por uma equipe utilizando **Git e GitHub** com um fluxo estruturado de branches (`main` e `dev`).

---

## 🚀 Objetivo
- Implementar um **sistema de veículos usando herança** em Java.
- Trabalhar em equipe utilizando **GitHub Flow**.
- Utilizar **branches, pull requests e merges** corretamente.

---
## 📕 Instruções Gerais
- Formem um grupo de **três alunos**.
- Criem um repositório no GitHub e cada membro deve **clonar** o projeto.
Cada aluno será responsável por uma classe específica no projeto.
- Devem criar **branches individuais** para suas implementações e usar **pull requests** para mesclar o código na branch principal (main).
- No final, um dos membros deve rodar o código principal para validar se tudo está funcionando corretamente.

---

## 🔧 Configuração do Repositório

### 1️⃣ Criar o Repositório no GitHub
1. Um dos alunos deve criar um repositório no **GitHub**:
   - Vá para [GitHub](https://github.com).
   - Clique em **New repository**.
   - Escolha um nome (exemplo: `sistema-veiculos`).
   - Selecione **Public** ou **Private**.
   - Marque **Add a README file**.
   - Clique em **Create repository**.

2. O dono do repositório deve ir até **Settings > Collaborators** e adicionar os colegas como **colaboradores**.

---

### 2️⃣ Clonar o Repositório e Criar a Branch `dev`
1. Todos os alunos devem clonar o repositório:

   ```sh
   git clone <URL_DO_REPOSITORIO>
   cd sistema-veiculos
   
2. O aluno responsável pelo repositório **cria a branch dev** e a envia para o GitHub:

   ```sh
   git checkout -b dev
   git push origin dev
   
3. Todos os membros devem atualizar o repositório local para incluir a nova branch:

   ```sh
   git pull origin dev

Todos devem **trabalhar na branch** dev.

---
##  📚 Estrutura do projeto
   
    /projeto
     ├── src
     │   └── veiculos
     │       ├── Veiculo.java
     │       ├── Moto.java
     │       ├── Carro.java
     │   └── app
     │       ├── Main.java
   
---
## 🛠️ Implementação do Código

Cada aluno criará uma **branch individual** para sua feature e fará um pull request para dev.

### 1️⃣ Criar a Classe Veiculo (Aluno 1)

1. Criar uma nova branch:

   ```sh
   git checkout -b feature/veiculo

2. Criar o arquivo **Veiculo.java** com o seguinte código:

   ```java
   package veiculos;
   public class Veiculo {
       protected String marca;
       protected String modelo;
       protected int ano;
   
       public Veiculo(String marca, String modelo, int ano) {
           this.marca = marca;
           this.modelo = modelo;
           this.ano = ano;
       }
   
       public void exibirInfo() {
           System.out.println("Marca: " + marca + ", Modelo: " + modelo + ", Ano: " + ano);
       }
   }
   ```
3. Adicionar, commitar e enviar para o GitHub:

   ```sh
   git add src/veiculos/Veiculo.java
   git commit -m "Adiciona classe base Veiculo"
   git push origin feature/veiculo

4. Criar um **pull request para dev** no GitHub.
   - Acesse o repositório no GitHub.
   - Vá para a aba **Pull Requests**.
   - Clique no botão verde **New pull request**.
   - No campo **base**, selecione dev (a branch de destino).
   - No campo **compare**, selecione sua branch (feature/carro, feature/moto, etc.).
   - Revise as mudanças e clique em **Create pull request**.
   - Adicione um título descritivo e um comentário explicando o que foi feito.
   - Clique em **Create pull request** novamente.


### 2️⃣ Criar a Classe Carro (Aluno 2)

1. Criar uma nova branch:

   ```sh
   git checkout -b feature/carro

2. Criar o arquivo **Carro.java** com o seguinte código:

   ```java  
   package veiculos;
   public class Carro extends Veiculo {
       private int portas;
   
       public Carro(String marca, String modelo, int ano, int portas) {
           super(marca, modelo, ano);
           this.portas = portas;
       }
   
       @Override
       public void exibirInfo() {
           super.exibirInfo();
           System.out.println("Número de portas: " + portas);
       }
   }
   ```

3. Adicionar, commitar e enviar para o GitHub:

   ```sh
   git add src/veiculos/Carro.java
   git commit -m "Adiciona classe Carro"
   git push origin feature/carro

4. Criar um **pull request para dev** no GitHub.
   - Acesse o repositório no GitHub.
   - Vá para a aba **Pull Requests**.
   - Clique no botão verde **New pull request**.
   - No campo **base**, selecione dev (a branch de destino).
   - No campo **compare**, selecione sua branch (feature/carro, feature/moto, etc.).
   - Revise as mudanças e clique em **Create pull request**.
   - Adicione um título descritivo e um comentário explicando o que foi feito.
   - Clique em **Create pull request** novamente.


### 3️⃣ Criar a Classe Moto (Aluno 3)

1. Criar uma nova branch:

   ```sh
   git checkout -b feature/moto

2. Criar o arquivo **Moto.java** com o seguinte código:

   ```java
   package veiculos;
   public class Moto extends Veiculo {
       private boolean partidaEletrica;
   
       public Moto(String marca, String modelo, int ano, boolean partidaEletrica) {
           super(marca, modelo, ano);
           this.partidaEletrica = partidaEletrica;
       }
   
       @Override
       public void exibirInfo() {
           super.exibirInfo();
           System.out.println("Possui partida elétrica: " + (partidaEletrica ? "Sim" : "Não"));
       }
   }
   ```

3. Adicionar, commitar e enviar para o GitHub:

   ```sh
   git add src/veiculos/Moto.java
   git commit -m "Adiciona classe Moto"
   git push origin feature/moto

4. Criar um **pull request para dev** no GitHub.
   - Acesse o repositório no GitHub.
   - Vá para a aba **Pull Requests**.
   - Clique no botão verde **New pull request**.
   - No campo **base**, selecione dev (a branch de destino).
   - No campo **compare**, selecione sua branch (feature/carro, feature/moto, etc.).
   - Revise as mudanças e clique em **Create pull request**.
   - Adicione um título descritivo e um comentário explicando o que foi feito.
   - Clique em **Create pull request** novamente.

## ✅ Revisão e Aprovação
1. Cada aluno revisa os **pull requests** (feature/veiculo, feature/carro, feature/moto).
2. Após revisão e aprovação, fazem merge para dev, clicando em **Merge pull request**.
3. Quando **dev** estiver completo, um dos alunos cria um **pull request de dev para main** e a equipe revisa antes de aprovar o merge.

## 🚀 Criar a Classe Main e Testar

1. Criar uma nova branch:

   ```sh
   git checkout -b feature/main

2. Criar o arquivo **Main.java** com o seguinte código:

   ```java
   package app;
   import veiculos.Carro;
   import veiculos.Moto;
   public class Main {
       public static void main(String[] args) {
           Carro carro = new Carro("Toyota", "Corolla", 2022, 4);
           Moto moto = new Moto("Honda", "CB 500", 2023, true);
   
           carro.exibirInfo();
           System.out.println();
           moto.exibirInfo();
       }
   }
   ```
   
3. Adicionar, commitar e enviar para o GitHub:

   ```sh
   git add src/app/Main.java
   git commit -m "Adiciona classe Main para testes"
   git push origin feature/main

4. Criar um **pull request para dev**, revisar e mesclar.

5. Criar um **pull request de dev para main** e mesclar.

## 🏁 Rodar o Código

1. Todos os alunos devem atualizar o repositório local:

   ```sh
   git checkout main
   git pull origin main

2. Compilar e executar:

   ```sh
   javac src/app/Main.java
   javac src/veiculos/Veiculo.java
   javac src/veiculos/Carro.java
   javac src/veiculos/Moto.java
   java src/app/Main
