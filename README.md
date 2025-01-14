# 🎵 Desafio: Sistema de Cadastro de Artistas e Músicas 🎶

Nesta aplicação, foi desenvolvido um sistema completo para armazenar dados de artistas e suas músicas favoritas em um banco de dados relacional. A aplicação permite o cadastro de artistas, registro de músicas e consultas por artista.

---

##  Funcionalidades Implementadas

- **Cadastro de Artistas:**  
  Implementado o registro de artistas com detalhes completos e classificação pelo tipo (Solo, Dupla ou Banda) utilizando `enum`.

- **Cadastro de Músicas:**  
  Desenvolvido o cadastro de músicas associadas a artistas previamente registrados, garantindo a integridade dos dados.

- **Consulta de Músicas por Artista:**  
  Incluída funcionalidade de pesquisa para listar todas as músicas vinculadas a um artista específico.

- **Menu Interativo:**  
  Criado um menu no console para facilitar a navegação pelas funcionalidades da aplicação.

---

##  Tecnologias Utilizadas

- **Java 17**
- **Spring Boot**
- **Spring Data JPA**
- **PostgreSQL**
- **Maven**

---

##  Detalhes Técnicos

- **Modelagem de Entidades:**
   - A classe `Artista` foi modelada com atributos essenciais e o tipo de artista definido por um `enum` (**SOLO**, **DUPLA**, **BANDA**).
   - A classe `Musica` foi criada com atributos como nome, duração e gênero, com relacionamento direto com a entidade `Artista`.

- **Relacionamento Artista x Música:**
   - Implementada a relação **One-to-Many** entre `Artista` e `Musica`, permitindo que um artista tenha várias músicas associadas.
   - Garantido que uma música só seja cadastrada se o artista já existir no banco.

- **Consultas Personalizadas:**
   - Utilizadas **Derived Queries** e **JPQL** para validar o cadastro de artistas e listar músicas por artista.

- **Menu de Interação:**
   - A classe principal estende `CommandLineRunner` para inicializar o menu de opções e executar as ações escolhidas.

---

##  Como Executar a Aplicação

1. **Clone o repositório:**
   ```bash
   git clone  https://github.com/lurregiabarreto/SoundTrackr.git

   ```

2. **Configure o `application.properties`:**
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/seu_banco
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   ```

3. **Execute o projeto:**
   ```bash
   ./mvnw spring-boot:run
   ```

4. **Utilize o menu interativo** para acessar todas as funcionalidades.

---

## ✅ O que foi aprendido

- Modelagem de entidades e mapeamento de relacionamentos com **Spring Data JPA**.
- Implementação de **Derived Queries** e **JPQL** para consultas eficientes.
- Organização de um fluxo de interação pelo console com **CommandLineRunner**.
