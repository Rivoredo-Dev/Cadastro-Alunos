# 🎓 Sistema de Cadastro de Alunos

Este é um sistema de gerenciamento acadêmico desenvolvido em Java, focado na aplicação de conceitos avançados de **Programação Orientada a Objetos (POO)** e modularidade.

O projeto utiliza interfaces para separar as responsabilidades, permitindo que a forma de armazenamento ou a interface de usuário (CLI) sejam alteradas sem afetar a lógica de negócio central. 

### 🚀 Funcionalidades
* **Persistência de Dados:** Importação e exportação de cadastros utilizando serialização de objetos (arquivos `.dat` ou binários).
* **Inserção:** Cadastro dinâmico de alunos com validação estrita de dados (Nome, Idade, RA, Curso e Semestre).
* **Remoção:** Exclusão segura de registros através do RA.
* **Listagem Avançada:** Visualização de todos os alunos cadastrados, incluindo uma opção de exibição de nomes em formato **bibliográfico**.
* **Atualização Granular:** Submenu interativo para edição de informações específicas (Nome, Idade, Curso ou Semestre) individualmente, sem a necessidade de reescrever todo o registro.
* **Validação e Tratamento de Erros:** Prevenção de quebras de sistema por entradas inválidas (como a digitação de letras onde se espera números) e controle de capacidade máxima.

### 🏗️ Estrutura de Camadas
* `App`: Classe principal que orquestra o fluxo do programa, controlando o menu inicial e o carregamento do sistema.
* `CadastroAlunos`: Coordena as operações e regras de negócio, implementando a interface `Serializable` para persistência.
* `menu.IMenu`: Interface para abstração da interação com o usuário (entradas e saídas).
* `armazenamento.IArmazenador`: Interface para abstração do local de armazenamento em memória (com suporte a listas dinâmicas ou arrays fixos).
* `salvamento.ISalvamento`: Interface responsável pela leitura e gravação dos objetos de cadastro em disco.
* `alunos.Aluno`: Entidade base que estrutura as informações acadêmicas do estudante.

### 🛠️ Tecnologias
* Java (JDK 11 ou superior)
* Ambiente de desenvolvimento: BlueJ (opcional)

### 🏁 Como Executar
1. Certifique-se de ter o Java instalado em sua máquina.
2. Compile o projeto (estando na raiz das pastas):
   ```bash
   javac App.java
