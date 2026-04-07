# 🎓 Sistema de Cadastro de Alunos

Este é um sistema de gerenciamento acadêmico desenvolvido em Java, focado na aplicação de conceitos avançados de **Programação Orientada a Objetos (POO)** e modularidade.

O projeto utiliza interfaces para separar as responsabilidades, permitindo que a forma de armazenamento ou a interface de usuário (CLI) sejam alteradas sem afetar a lógica de negócio central.

### 🚀 Funcionalidades
* **Inserção:** Cadastro de alunos com validação de dados (Nome, Idade, RA, Curso e Semestre).
* **Remoção:** Exclusão de registros através do RA.
* **Listagem:** Visualização de todos os alunos cadastrados.
* **Atualização:** Edição de informações de alunos já existentes.
* **Validação:** Tratamento de erros para entradas inválidas e controle de capacidade máxima.

### 🏗️ Estrutura de Camadas
* `App`: Classe principal que orquestra o fluxo do programa.
* `CadastroAlunos`: Coordena as operações e regras de negócio.
* `menu.IMenu`: Interface para abstração da interação com o usuário.
* `armazenamento.IArmazenador`: Interface para abstração do local de salvamento dos dados.

### 🛠️ Tecnologias
* Java (JDK 11 ou superior)
* Ambiente de desenvolvimento: BlueJ (opcional)

### 🏁 Como Executar
1. Certifique-se de ter o Java instalado em sua máquina.
2. Compile o projeto (estando na raiz das pastas):
   ```bash
   javac App.java
