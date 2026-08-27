# Rental DB

# Como Identificar Requisitos Funcionais e Não Funcionais

## 1. Entenda o problema

Leia o enunciado e identifique:

* Qual problema o sistema deve resolver?
* Quem vai utilizar o sistema?
* O que os usuários precisam fazer?

---

## 2. Identifique as ações

Procure os **verbos** do enunciado, como:

* Cadastrar
* Consultar
* Editar
* Excluir
* Registrar
* Calcular
* Gerar
* Enviar

Essas ações geralmente indicam **Requisitos Funcionais**.

---

## 3. Identifique os Requisitos Funcionais (RF)

Os requisitos funcionais descrevem **o que o sistema deve fazer**.

### Exemplos:

* **RF01** — O sistema deve permitir cadastrar usuários.
* **RF02** — O sistema deve permitir consultar produtos.
* **RF03** — O sistema deve gerar relatórios.
* **RF04** — O sistema deve calcular o valor da compra.

### Dica:

> **RF = O QUE o sistema faz.**

---

## 4. Identifique os Requisitos Não Funcionais (RNF)

Os requisitos não funcionais descrevem **como o sistema deve funcionar**, suas características e restrições.

### Exemplos:

* **RNF01** — O sistema deve responder às consultas em até 2 segundos.
* **RNF02** — O sistema deve proteger os dados dos usuários.
* **RNF03** — O sistema deve funcionar em dispositivos móveis.
* **RNF04** — O sistema deve realizar backups diariamente.

### Dica:

> **RNF = COMO o sistema deve funcionar.**

---

## 5. Classifique os RNFs

Os requisitos não funcionais podem envolver:

* 🔐 **Segurança** — proteção dos dados e controle de acesso.
* ⚡ **Desempenho** — velocidade e tempo de resposta.
* 🖥️ **Usabilidade** — facilidade de utilização.
* 📱 **Compatibilidade** — funcionamento em diferentes dispositivos.
* 💾 **Confiabilidade** — disponibilidade, backup e recuperação.

---

## 6. Verifique os requisitos

Um bom requisito deve ser:

* Claro;
* Específico;
* Testável;
* Necessário;
* Sem ambiguidades.

### ❌ Ruim

> O sistema deve ser rápido.

### ✅ Melhor

> O sistema deve responder às consultas em até 2 segundos.

---

## 7. Priorize

Depois de identificar os requisitos, defina sua importância:

* 🔴 **Essencial** — necessário para o sistema funcionar.
* 🟡 **Importante** — necessário, mas pode ser implementado depois.
* 🟢 **Desejável** — pode ficar para uma etapa futura.

---

# 🧠 Resumo

```text
Entender o problema
        ↓
Identificar os usuários
        ↓
Identificar as ações
        ↓
Ações → Requisitos Funcionais
        ↓
Características e restrições → Requisitos Não Funcionais
        ↓
Verificar e priorizar
```

> **RF = O QUE o sistema faz.**
> **RNF = COMO o sistema deve funcionar.**


---

# 🔎 Identificação do problema

## Principais problemas encontrados

1. **Controle feito em planilhas**
   As informações podem ficar desorganizadas e dificultar o acompanhamento dos equipamentos.

2. **Dupla locação de equipamentos**
   Sem um controle adequado, o mesmo equipamento pode ser disponibilizado para mais de um cliente na mesma data.

3. **Equipamentos danificados**
   Equipamentos devolvidos com problemas precisam ser registrados para que possam ser identificados como indisponíveis.

4. **Falta de rastreabilidade**
   É necessário saber quem realizou uma movimentação, quando ela ocorreu e qual equipamento foi movimentado.

5. **Falta de controle de estoque**
   O sistema precisa controlar a quantidade disponível e alertar quando o estoque atingir o limite mínimo.

---

# ⚙️ Requisitos Funcionais

Os requisitos funcionais representam aquilo que o sistema deve ser capaz de realizar.

| Código   | Funcionalidade                   | Descrição                                                                                                       |
| -------- | -------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **RF01** | Cadastrar equipamentos           | O sistema deve permitir cadastrar equipamentos para manter suas informações armazenadas.                        |
| **RF02** | Consultar equipamentos           | O sistema deve permitir consultar os equipamentos cadastrados e suas quantidades disponíveis.                   |
| **RF03** | Pesquisar equipamentos           | O sistema deve permitir pesquisar equipamentos por diferentes critérios, como nome, categoria, marca ou modelo. |
| **RF04** | Atualizar equipamentos           | O sistema deve permitir alterar as informações dos equipamentos cadastrados.                                    |
| **RF05** | Excluir equipamentos             | O sistema deve permitir excluir equipamentos conforme as regras definidas pelo sistema.                         |
| **RF06** | Registrar entrada                | O sistema deve permitir registrar entradas de equipamentos para atualizar o estoque.                            |
| **RF07** | Registrar saída                  | O sistema deve permitir registrar saídas de equipamentos para controlar as locações.                            |
| **RF08** | Controlar disponibilidade        | O sistema deve verificar se existe quantidade suficiente antes de registrar uma saída.                          |
| **RF09** | Registrar movimentações          | O sistema deve registrar as movimentações de entrada e saída dos equipamentos.                                  |
| **RF10** | Consultar histórico              | O sistema deve permitir consultar o histórico de movimentações para garantir a rastreabilidade.                 |
| **RF11** | Configurar estoque mínimo        | O sistema deve permitir definir a quantidade mínima de cada equipamento.                                        |
| **RF12** | Alertar estoque mínimo           | O sistema deve identificar equipamentos cuja quantidade disponível esteja no limite mínimo ou abaixo dele.      |
| **RF13** | Identificar usuário              | O sistema deve registrar o usuário responsável por cada movimentação.                                           |
| **RF14** | Registrar devolução              | O sistema deve permitir registrar a devolução dos equipamentos e atualizar o estoque.                           |
| **RF15** | Registrar avarias                | O sistema deve permitir registrar equipamentos devolvidos danificados.                                          |
| **RF16** | Identificar indisponibilidade    | O sistema deve identificar equipamentos que não estejam disponíveis para locação.                               |
| **RF17** | Gerar relatório de estoque       | O sistema deve permitir consultar informações relacionadas ao estoque.                                          |
| **RF18** | Gerar relatório de movimentações | O sistema deve permitir consultar as entradas e saídas realizadas em determinado período.                       |

---
<img width="628" height="711" alt="Captura de tela 2026-08-06 103726" src="https://github.com/user-attachments/assets/07aace77-1f0e-4135-b3ef-6a95df150efb" />




---

# 🗄️ Estrutura do Banco de Dados

O banco de dados utilizado no projeto é o **PostgreSQL**.

O banco foi denominado:

```sql
Rental_db
```

## 📊 Tabelas

O banco possui quatro tabelas principais:

### `Usuario`

Armazena os usuários que utilizam o sistema.

Principais informações:

* `id` — identificador do usuário;
* `nome` — nome do usuário;
* `login` — login utilizado para acesso;
* `senha` — senha do usuário.

### `Categoria`

Armazena as categorias dos equipamentos.

Campos:

* `id` — identificador da categoria;
* `nome` — nome da categoria.

### `Equipamento`

Armazena os equipamentos disponíveis para gerenciamento e locação.

Campos:

* `id` — identificador do equipamento;
* `nome` — nome do equipamento;
* `marca` — marca;
* `modelo` — modelo;
* `quantidade` — quantidade disponível;
* `estoque_minimo` — quantidade mínima desejada;
* `categoria_id` — categoria à qual o equipamento pertence.

### `Movimentacao`

Registra as entradas e saídas dos equipamentos.

Campos:

* `id` — identificador da movimentação;
* `tipo` — entrada ou saída;
* `data` — data da movimentação;
* `quantidade` — quantidade movimentada;
* `equipamento_id` — equipamento movimentado;
* `usuario_id` — usuário responsável pela movimentação.

---

# 🔗 Relacionamentos

O banco utiliza **chaves estrangeiras (Foreign Keys)** para relacionar as tabelas.

```text
Categoria
    │
    │ 1:N
    ▼
Equipamento
    │
    │ 1:N
    ▼
Movimentacao
    ▲
    │ N:1
    │
 Usuario
```

### Relacionamentos

* Uma **categoria** pode possuir vários equipamentos.
* Um **equipamento** pode possuir várias movimentações.
* Um **usuário** pode realizar várias movimentações.
* Cada **movimentação** está relacionada a um equipamento e a um usuário.

---

# 🛠️ Tecnologias

* **PostgreSQL**
* **SQL**
* Banco de dados relacional

---

# 💾 Criação do banco

```sql
CREATE DATABASE Rental_db;
```

Após criar o banco, as tabelas devem ser criadas respeitando a ordem de suas dependências.

> **Importante:** `Categoria` deve ser criada antes de `Equipamento`, e `Equipamento` deve ser criada antes de `Movimentacao`, pois existem chaves estrangeiras entre essas tabelas.

---

# 🧱 Criação das tabelas

## 1. Usuário

```sql
CREATE TABLE Usuario (
    id SERIAL PRIMARY KEY,
    nome VARCHAR(30) NOT NULL,
    login VARCHAR(50) NOT NULL,
    senha VARCHAR(8) NOT NULL
);
```

## 2. Categoria

```sql
CREATE TABLE Categoria (
    id SERIAL PRIMARY KEY,
    nome VARCHAR(30) NOT NULL
);
```

## 3. Tipo de movimentação

```sql
CREATE TYPE tipo_enum AS ENUM ('Entrada', 'Saída');
```

## 4. Equipamento

```sql
CREATE TABLE Equipamento (
    id SERIAL PRIMARY KEY,
    nome VARCHAR(30) NOT NULL,
    marca VARCHAR(30) NOT NULL,
    modelo VARCHAR(30) NOT NULL,
    quantidade INT NOT NULL,
    estoque_minimo INT NOT NULL,
    categoria_id INT NOT NULL,
    FOREIGN KEY (categoria_id) REFERENCES Categoria(id)
);
```

## 5. Movimentação

```sql
CREATE TABLE Movimentacao (
    id SERIAL PRIMARY KEY,
    tipo tipo_enum NOT NULL,
    data DATE NOT NULL,
    quantidade INT NOT NULL,
    equipamento_id INT NOT NULL,
    FOREIGN KEY (equipamento_id) REFERENCES Equipamento(id),
    usuario_id INT NOT NULL,
    FOREIGN KEY (usuario_id) REFERENCES Usuario(id)
);
```

---

# 📝 Inserção de dados

## Categorias

As categorias devem ser inseridas antes dos equipamentos.

```sql
INSERT INTO Categoria (nome)
VALUES
('Informática'),
('Periféricos'),
('Eletrônicos');
```

## Usuários

```sql
INSERT INTO Usuario (nome, login, senha)
VALUES
('julia', 'juliademachado@', '1234'),
('maria', 'mariaclre@', '12345'),
('lara', 'flordeliz@', '123456');
```

## Equipamentos

```sql
INSERT INTO Equipamento (
    nome,
    marca,
    modelo,
    quantidade,
    estoque_minimo,
    categoria_id
)
VALUES
('Notebook', 'Dell', 'Inspiron 15', 10, 1, 1),
('Monitor', 'Samsung', 'T350', 15, 2, 2),
('Teclado', 'Logitech', 'K120', 20, 3, 3);
```

> **Importante:** os equipamentos precisam ser cadastrados antes das movimentações, pois a tabela `Movimentacao` possui uma chave estrangeira que referencia `Equipamento`.

## Movimentações

Como os equipamentos cadastrados anteriormente recebem os IDs **1, 2 e 3**, as movimentações devem utilizar esses IDs.

```sql
INSERT INTO Movimentacao (
    tipo,
    data,
    quantidade,
    equipamento_id,
    usuario_id
)
VALUES
('Entrada', '2024-08-01', 12, 1, 1),
('Saída', '2025-07-02', 13, 2, 2),
('Saída', '2026-06-03', 14, 3, 3);
```

---

# ⚠️ Observação sobre os INSERTs

Na versão original, as movimentações utilizavam:

```sql
equipamento_id = 4
equipamento_id = 5
equipamento_id = 6
```

Porém, foram cadastrados somente três equipamentos. Como o `SERIAL` começa normalmente pelo ID `1`, os equipamentos cadastrados recebem:

| ID | Equipamento |
| -: | ----------- |
|  1 | Notebook    |
|  2 | Monitor     |
|  3 | Teclado     |

Por isso, utilizar `4`, `5` e `6` como `equipamento_id` causaria erro de **chave estrangeira**, pois esses equipamentos não existem.

Além disso, os valores de `quantidade` nas movimentações devem respeitar a disponibilidade do estoque. Por exemplo, uma saída de 13 unidades do Monitor somente deve ser permitida se houver pelo menos 13 unidades disponíveis no momento da movimentação.

---

# 📌 Regras importantes do sistema

O sistema deve respeitar algumas regras para manter a consistência dos dados:

1. Um equipamento não deve ser retirado quando a quantidade disponível for insuficiente.
2. Toda movimentação deve estar vinculada a um equipamento existente.
3. Toda movimentação deve estar vinculada a um usuário existente.
4. Toda movimentação deve possuir data, tipo e quantidade.
5. O estoque mínimo deve ser definido para cada equipamento.
6. Equipamentos indisponíveis não devem ser disponibilizados para novas locações.
7. As movimentações devem permanecer registradas para permitir rastreabilidade.
8. Equipamentos devolvidos com avarias devem ser identificados como indisponíveis quando necessário.

---
Criação da API 
# ☕ Passo a Passo — API Java com Spring Boot

Este guia apresenta as etapas para criar uma **API em Java utilizando Spring Boot**, conectá-la ao PostgreSQL e organizar o projeto no GitHub.

---

## 1. Criar uma organização no GitHub

1. Acesse o GitHub.
2. Crie uma **Organization (Organização)**.
3. Dentro da organização, crie um **Repository (Repositório)** para o projeto.
4. Entre no repositório criado.
5. Clique em **Code**.
6. Copie o link do repositório.

---

## 2. Clonar o repositório no VS Code

1. Abra o **Visual Studio Code** vazio.
2. Clique no primeiro ícone da barra lateral, chamado **Explorer**.
3. Clique em **Clone Repository**.
4. Cole o link copiado do GitHub.
5. Escolha a pasta onde deseja salvar o projeto.
6. Abra o repositório clonado no VS Code.

---

## 3. Instalar as extensões

No VS Code, acesse **Extensions** e instale:

* **Extension Pack for Java**
* **Project Manager for Java**
* **Debugger for Java**
* **Remote Repositories**
* **Spring Boot Extension Pack**
* **Spring Initializr Java Support**
* **Git Bash**
* **Git History**
* **Git History Diff**
* **GitHub Repositories**
* **Git Graph**
* **Language Support for Java**
* **Markdown Preview Github Styling**
* **Prettier**
* **Maven for Java**

> Algumas extensões podem já estar incluídas em outros pacotes. Nesse caso, não é necessário instalar novamente.

---

## 4. Criar o projeto Java

No repositório aberto no VS Code:

1. Clique com o botão direito em um espaço vazio abaixo do `README.md`.
2. Selecione **New Project / Novo Projeto Java**.
3. Selecione o framework **Spring Boot**.

---

## 5. Configurar o projeto

### Projeto

Selecione:

```text
Maven Project
```

O Maven será responsável pelo gerenciamento das dependências e pela construção do projeto.

### Versão do Spring Boot

Selecione:

```text
4.0.5
```

> Utilize uma versão estável. Evite versões identificadas como `M`, `SNAPSHOT` ou outras versões de pré-lançamento.

### Linguagem

Selecione:

```text
Java
```

---

## 6. Configurar o Group Id

No campo **Group Id**, é uma boa prática utilizar o domínio ou endereço da organização escrito **de trás para frente**.

### Exemplo

```text
com.exemplo
```

Ou:

```text
br.com.empresa
```

Essa organização ajuda a identificar os pacotes Java do projeto.

---

## 7. Configurar o Artifact Id

No campo **Artifact Id**, informe o nome do projeto.

Utilize:

* Letras minúsculas;
* Sem caracteres especiais;
* Sem espaços;
* Evite acentos.

### Exemplo

```text
rental-api
```

---

## 8. Validar o Package Name

Confira o **Package Name** gerado automaticamente.

Verifique se:

* O `Group Id` está correto;
* O `Artifact Id` está correto;
* Não existem erros de digitação.

Exemplo:

```text
br.com.exemplo.rentalapi
```

---

## 9. Escolher o tipo de empacotamento

Selecione:

```text
Jar
```

O **JAR (Java Archive)** é utilizado para empacotar a aplicação Java e permitir sua execução.

---

## 10. Selecionar a versão do Java

Selecione a versão do Java instalada na máquina.

Neste projeto:

```text
Java 25
```

Para verificar a versão instalada, abra o terminal do VS Code e execute:

```bash
java --version
```

O terminal deverá apresentar a versão instalada.

---

# 11. Adicionar as dependências

No arquivo `pom.xml`, adicione as dependências necessárias para o projeto.

```xml
<dependencies>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter</artifactId>
    </dependency>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-test</artifactId>
        <scope>test</scope>
    </dependency>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>

    <dependency>
        <groupId>org.postgresql</groupId>
        <artifactId>postgresql</artifactId>
        <scope>runtime</scope>
    </dependency>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>

    <dependency>
        <groupId>jakarta.persistence</groupId>
        <artifactId>jakarta.persistence-api</artifactId>
    </dependency>

    <dependency>
        <groupId>org.springdoc</groupId>
        <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
        <version>2.2.0</version>
    </dependency>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-devtools</artifactId>
        <scope>runtime</scope>
        <optional>true</optional>
    </dependency>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-thymeleaf</artifactId>
    </dependency>

</dependencies>
```


# 12. Configurar o banco de dados

Abra o arquivo:

```text
src/main/resources/application.properties
```

Adicione:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/postgres

spring.datasource.username=postgres

spring.datasource.password=aluno

spring.jpa.hibernate.ddl-auto=update

spring.jpa.show-sql=true

spring.datasource.driver-class-name=org.postgresql.Driver
```

Depois pressione:

```text
Ctrl + S
```

para salvar.

> **Atenção:** substitua `postgres`, `aluno` e o nome do banco pelos dados configurados no seu computador, caso sejam diferentes.

---

# 13. Criar os Models

Os **Models** representam as entidades que serão armazenadas no banco de dados.

Crie uma pasta:

```text
model
```

Dentro dela, crie a classe:

```text
Produto.java
```

Exemplo:

```java
package br.com.exemplo.rentalapi.model;

import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;

@Entity
public class Produto {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String nome;

    private Double preco;

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public Double getPreco() {
        return preco;
    }

    public void setPreco(Double preco) {
        this.preco = preco;
    }
}


# ☕ API Java com Spring Boot — Model, Repository e Controller

Depois de criar o projeto Spring Boot, vamos criar as principais partes de uma API de forma simples:

```text
Model → Repository → Controller
```

* **Model:** representa os dados.
* **Repository:** faz a comunicação com o banco.
* **Controller:** recebe as requisições da API.

---

# 1. Gerar o construtor do Model

Depois de criar a classe `Produto.java`, podemos gerar os construtores automaticamente pelo VS Code.

Exemplo inicial:

```java
@Entity
public class Produto {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String nome;
    private Double preco;

}
```

## Gerar construtor vazio

1. Clique com o botão direito em uma linha vazia **dentro da classe**, depois dos atributos e antes da chave `}`.

```java
@Entity
public class Produto {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String nome;
    private Double preco;

    // CLIQUE AQUI
}
```

2. Clique em:

```text
Source Action...
```

3. Selecione:

```text
Generate Constructor
```

4. Na janela que aparecer, **não selecione nenhum atributo**.
5. Clique em **OK**.

O VS Code irá gerar:

```java
public Produto() {
}
```

Esse é o **construtor vazio**.

---

# 2. Gerar construtor com todos os atributos

Repita o processo:

1. Clique em uma linha vazia dentro da classe.
2. Clique em **Source Action...**
3. Clique em **Generate Constructor**.
4. Agora selecione **todos os atributos**.
5. Clique em **OK**.

Será gerado algo parecido com:

```java
public Produto(Long id, String nome, Double preco) {
    this.id = id;
    this.nome = nome;
    this.preco = preco;
}
```

O Model ficará:

```java
@Entity
public class Produto {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String nome;
    private Double preco;

    public Produto() {
    }

    public Produto(Long id, String nome, Double preco) {
        this.id = id;
        this.nome = nome;
        this.preco = preco;
    }
}
```

---

# 3. Gerar Getters e Setters

Também podemos gerar os métodos automaticamente.

1. Clique com o botão direito em uma linha vazia.
2. Clique em **Source Action...**
3. Selecione **Generate Getters and Setters**.
4. Selecione os atributos.
5. Clique em **OK**.

Exemplo:

```java
public String getNome() {
    return nome;
}

public void setNome(String nome) {
    this.nome = nome;
}

public Double getPreco() {
    return preco;
}

public void setPreco(Double preco) {
    this.preco = preco;
}
```

---

# 4. Relacionamentos entre Models

Quando duas tabelas estão relacionadas, podemos representar esse relacionamento nos Models usando JPA.

Por exemplo:

```text
Pauta
  │
  │ 1:N
  ↓
Usuario
```

Isso significa:

> Uma pauta pode estar relacionada a vários usuários.

Nesse caso podemos utilizar:

```java
@OneToMany
```

---

## Exemplo de `Pauta`

```java
@Entity
public class Pauta {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String titulo;

    @OneToMany
    @JoinColumn(name = "pauta_id")
    private List<Usuario> usuarios;

}
```

### O que significa `@OneToMany`?

```java
@OneToMany
```

Significa que **um registro de Pauta pode estar relacionado a vários registros de Usuario**.

Exemplo:

```text
Pauta 1
 ├── Usuário 1
 ├── Usuário 2
 └── Usuário 3
```

### O que significa `@JoinColumn`?

```java
@JoinColumn(name = "pauta_id")
```

Define o nome da coluna utilizada como chave estrangeira na tabela relacionada.

Nesse exemplo, a tabela `usuario` teria uma coluna:

```text
pauta_id
```

---

# 5. Criar o Repository

Depois dos Models, crie uma pasta chamada:

```text
repository
```

Dentro dela, crie:

```text
ProdutoRepository.java
```

Código:

```java
package br.com.exemplo.rentalapi.repository;

import br.com.exemplo.rentalapi.model.Produto;
import org.springframework.data.jpa.repository.JpaRepository;

public interface ProdutoRepository extends JpaRepository<Produto, Long> {

}
```

## Para que serve?

O `Repository` é responsável por facilitar a comunicação entre a aplicação e o banco de dados.

Ao utilizar:

```java
extends JpaRepository<Produto, Long>
```

o Spring já disponibiliza várias operações.

Por exemplo:

```java
findAll()
findById()
save()
deleteById()
```

Assim, não precisamos escrever manualmente o SQL para essas operações básicas.

---

# 6. Criar o Controller

Agora crie uma pasta:

```text
controller
```

Dentro dela:

```text
ProdutoController.java
```

Código básico:

```java
package br.com.exemplo.rentalapi.controller;

import br.com.exemplo.rentalapi.model.Produto;
import br.com.exemplo.rentalapi.repository.ProdutoRepository;

import org.springframework.web.bind.annotation.*;

import java.util.List;

@RestController
@RequestMapping("/produtos")
public class ProdutoController {

    private final ProdutoRepository repository;

    public ProdutoController(ProdutoRepository repository) {
        this.repository = repository;
    }

    @GetMapping
    public List<Produto> listar() {
        return repository.findAll();
    }

    @PostMapping
    public Produto cadastrar(@RequestBody Produto produto) {
        return repository.save(produto);
    }

    @GetMapping("/{id}")
    public Produto buscar(@PathVariable Long id) {
        return repository.findById(id).orElse(null);
    }

    @DeleteMapping("/{id}")
    public void excluir(@PathVariable Long id) {
        repository.deleteById(id);
    }
}
```

---

# 7. Entendendo o Controller

## `@RestController`

```java
@RestController
```

Informa ao Spring que essa classe será responsável por endpoints da API.

---

## `@RequestMapping`

```java
@RequestMapping("/produtos")
```

Define o endereço principal dos endpoints.

Por exemplo:

```text
http://localhost:8080/produtos
```

---

## `@GetMapping`

```java
@GetMapping
public List<Produto> listar() {
    return repository.findAll();
}
```

É utilizado para **buscar informações**.

Exemplo:

```text
GET /produtos
```

Retorno:

```json
[
    {
        "id": 1,
        "nome": "Notebook",
        "preco": 3500
    },
    {
        "id": 2,
        "nome": "Monitor",
        "preco": 1200
    }
]
```

---

# 8. Cadastrar com POST

```java
@PostMapping
public Produto cadastrar(@RequestBody Produto produto) {
    return repository.save(produto);
}
```

O `POST` é utilizado para **cadastrar um novo registro**.

No Postman:

```text
POST http://localhost:8080/produtos
```

Body → JSON:

```json
{
    "nome": "Notebook",
    "preco": 3500
}
```

---

# 9. Buscar pelo ID

```java
@GetMapping("/{id}")
public Produto buscar(@PathVariable Long id) {
    return repository.findById(id).orElse(null);
}
```

Para buscar o produto de ID `1`:

```text
GET http://localhost:8080/produtos/1
```

---

# 10. Excluir

```java
@DeleteMapping("/{id}")
public void excluir(@PathVariable Long id) {
    repository.deleteById(id);
}
```

No Postman:

```text
DELETE http://localhost:8080/produtos/1
```

Isso exclui o produto de ID `1`.

---

# 11. Adicionar PUT para alteração

Para uma API básica, também é interessante ter uma operação de alteração:

```java
@PutMapping("/{id}")
public Produto alterar(
        @PathVariable Long id,
        @RequestBody Produto produto) {

    produto.setId(id);

    return repository.save(produto);
}
```

No Postman:

```text
PUT http://localhost:8080/produtos/1
```

Body:

```json
{
    "nome": "Notebook Dell",
    "preco": 4200
}
```

---

# 12. Os principais métodos da API

Com o Controller acima, teremos:

| Método   | Endpoint         | Função            |
| -------- | ---------------- | ----------------- |
| `GET`    | `/produtos`      | Listar produtos   |
| `GET`    | `/produtos/{id}` | Buscar produto    |
| `POST`   | `/produtos`      | Cadastrar produto |
| `PUT`    | `/produtos/{id}` | Alterar produto   |
| `DELETE` | `/produtos/{id}` | Excluir produto   |

---

# 14. Criar o pacote `configs`

Depois de criar os pacotes `controller`, `model` e `repository`, crie o pacote:

```text
configs
```

A estrutura ficará:

```text
src
└── main
    └── java
        └── br.com.exemplo.rentalapi
            ├── configs
            ├── controller
            ├── model
            └── repository
```

O pacote `configs` será utilizado para colocar **configurações gerais da API**.

---

# 15. Adicionar o Swagger

O **Swagger/OpenAPI** permite visualizar e testar os endpoints da API diretamente pelo navegador.

A dependência utilizada é:

```xml
<dependency>
    <groupId>org.springdoc</groupId>
    <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
    <version>2.2.0</version>
</dependency>
```

Depois de adicionar a dependência, salve o `pom.xml`:

```text
Ctrl + S
```

O Maven irá baixar a dependência automaticamente.

---

# 16. Criar a configuração do Swagger

Dentro do pacote:

```text
configs
```

crie a classe:

```text
SwaggerConfig.java
```

Exemplo:

```java
package br.com.exemplo.rentalapi.configs;

import io.swagger.v3.oas.models.OpenAPI;
import io.swagger.v3.oas.models.info.Info;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
public class SwaggerConfig {

    @Bean
    public OpenAPI customOpenAPI() {
        return new OpenAPI()
                .info(new Info()
                        .title("Rental API")
                        .version("1.0")
                        .description("API para gerenciamento de equipamentos"));
    }
}
```

---

# 17. Executar a API

Execute o projeto pelo VS Code.

Quando aparecer no terminal algo indicando que o Spring Boot iniciou corretamente, a API estará funcionando.

Normalmente ela estará disponível em:

```text
http://localhost:8080
```

---

# 18. Abrir o Swagger

Com a API funcionando, abra o navegador e acesse:

```text
http://localhost:8080/swagger-ui/index.html
```

O Swagger apresentará os endpoints disponíveis.

Por exemplo:

```text
Rental API

Produto

GET     /produtos
POST    /produtos
PUT     /produtos/{id}
DELETE  /produtos/{id}
```

---

# 19. Testar uma API pelo Swagger

Por exemplo, para testar:

```text
GET /produtos
```

1. Clique em **GET /produtos**.
2. Clique em **Try it out**.
3. Clique em **Execute**.
4. O Swagger fará a requisição para a API.
5. O resultado aparecerá na tela.

Para um `POST`:

```text
POST /produtos
```

Clique em:

```text
Try it out
```

Depois informe o JSON:

```json
{
    "nome": "Notebook",
    "preco": 3500
}
```

Clique em:

```text
Execute
```
<!DOCTYPE html>
<html lang="pt-BR">

<head>

    <!-- Configuração dos caracteres -->
    <meta charset="UTF-8">

    <!-- Ajusta a página para celular e computador -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- Título da página -->
    <title>Rental DB</title>

    <!-- Conexão com o arquivo CSS -->
    <link rel="stylesheet" href="style.css">

</head>

<body>

    <!-- Cabeçalho -->
    <header>

        <h1>Rental DB</h1>

        <p>Gerenciamento de equipamentos</p>

    </header>

    <!-- Conteúdo principal -->
    <main>

        <h2>Equipamentos</h2>

        <!-- Botão -->
        <button onclick="cadastrarEquipamento()">
            + Cadastrar equipamento
        </button>

        <!-- Lista de equipamentos -->
        <section class="equipamentos">

            <!-- Card do equipamento -->
            <div class="card">

                <h3>Notebook</h3>

                <p>Marca: Dell</p>

                <p>Modelo: Inspiron 15</p>

                <strong>Quantidade: 10</strong>

            </div>

            <!-- Outro equipamento -->
            <div class="card">

                <h3>Monitor</h3>

                <p>Marca: Samsung</p>

                <p>Modelo: T350</p>

                <strong>Quantidade: 15</strong>

            </div>

        </section>

    </main>

    <!-- Conexão com o JavaScript -->
    <script src="script.js"></script>

</body>

</html>












