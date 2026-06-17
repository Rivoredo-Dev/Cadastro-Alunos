# 🎓 Sistema de Cadastro de Alunos

Este é um sistema de gerenciamento acadêmico desenvolvido em Java, focado na aplicação prática de conceitos de **Programação Orientada a Objetos (POO)**, encapsulamento e modularidade por meio do uso de interfaces.

O projeto adota uma arquitetura bem definida para separar as responsabilidades, garantindo que o mecanismo de armazenamento de dados ou a interface de interação com o usuário (CLI) possam ser substituídos ou modificados sem impactar a lógica de negócio central do sistema.

---

## 👨‍💻 Autores
* **Guilherme Pereira de Rivoredo**
* **João Batistella da Costa**
* **Pedro Henrique Freire Pereira**
* **Rafael Barros Infantini**

**Versão:** 1.0 (07/04/2026)  
**Ambiente Recomendado:** BlueJ ou qualquer IDE/editor com suporte ao JDK 11 ou superior.

---

## 🚀 Funcionalidades

* **Inserção com Validação Estrita:** Cadastro de alunos coletando Nome, Idade (com validação entre 1 e 120 anos), RA (Registro Acadêmico), Curso e Semestre (com validação entre 1 e 12).
* **Prevenção de Duplicidade:** O sistema impede o cadastro de mais de um aluno com o mesmo número de RA.
* **Remoção Segura:** Exclusão de registros do sistema localizando o estudante de forma única através do seu RA.
* **Listagem Avançada:** Exibição de todos os alunos armazenados, permitindo ao usuário escolher dinamicamente entre a visualização comum e a formatação de nomes no padrão **bibliográfico** (estilo citação/ABNT).
* **Atualização de Dados:** Permite alterar as informações de um aluno já existente (Nome, Idade, Curso e Semestre) localizando-o pelo seu RA.
* **Robustez e Tratamento de Erros:** Sistema totalmente protegido contra quebras por entradas inválidas no terminal (como digitação de letras em campos que esperam números) e controle estrito do limite de vagas (capacidade máxima).

---

## 🏗️ Estrutura do Projeto

O sistema é baseado em contratos (interfaces), o que reduz drasticamente o acoplamento entre os componentes:

* `App`: Classe principal que contém o método `main`. Ela gerencia o fluxo de execução, controla o laço do menu interativo e inicializa a configuração inicial do sistema.
* `CadastroAlunos`: Classe controladora responsável por coordenar as regras de negócio, loops de validação de dados e a comunicação entre a interface e o armazenamento.
* `menu.IMenu`: Interface que abstrai a camada de exibição com o usuário, isolando os métodos de leitura de teclado e escrita em tela.
* `armazenamento.IArmazenador`: Interface responsável por abstrair a manipulação e a coleção dos dados dos alunos em memória.
* `alunos.Aluno`: Classe entidade (modelo) que encapsula as propriedades de um estudante e fornece os métodos getters e setters correspondentes.

---

## 🛠️ Conceitos de POO Aplicados

* **Abstração:** Modelagem cuidadosa da entidade `Aluno` e das operações do sistema.
* **Encapsulamento:** Proteção dos atributos das classes através de modificadores de acesso privados e métodos públicos de manipulação.
* **Polimorfismo / Interfaces:** Uso intenso de referências para interfaces (`IMenu`, `IArmazenador`), permitindo que as implementações mudem de forma transparente para o restante do código.

---

## 🏁 Como Executar

### Pré-requisitos
Certifique-se de ter o **Java Development Kit (JDK 11 ou superior)** instalado na sua máquina e configurado corretamente no `PATH` do sistema.

### Compilação e Execução

1. Abra o seu terminal ou prompt de comando e navegue até a pasta raiz onde estão localizados os arquivos `.java`.
2. Compile o projeto inteiro executando o comando a partir da classe principal:
   ```bash
   javac App.java
