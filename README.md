# Arena Fighter API 🥊

Uma API RESTful robusta desenvolvida com **Spring Boot** para a gestão técnica de um ecossistema de jogos de luta. O projeto demonstra o domínio de arquitetura em camadas, persistência de dados com JPA/Hibernate e boas práticas de desenvolvimento Java.

## 🚀 Sobre o Projeto

O **Arena Fighter API** oferece um backend completo para gerir os três pilares de um jogo de combate:
- **Lutadores:** Gestão de atributos físicos (peso, altura) e categorias.
- **Jogadores (Players):** Monitorização de performance, níveis e histórico de combates.
- **Cenários:** Configuração de ambientes de luta, períodos e modalidades.

## 🛠️ Tecnologias Utilizadas

- **Java 17**
- **Spring Boot 3**
- **Spring Data JPA** (Persistência)
- **MySQL** (Base de Dados)
- **Bean Validation** (Validação com `@Valid`)
- **Maven** (Gestão de dependências)

## 🏗️ Arquitetura e Boas Práticas

O projeto foi construído seguindo padrões de mercado para garantir código limpo e manutenível:
- **Camada de Controller:** Endpoints REST padronizados.
- **Camada de Service:** Centralização da lógica de negócio.
- **DTO Pattern:** Separação entre as entidades da base de dados e os dados da API (Request/Response).
- **Tratamento Global de Exceções:** Uso de `@RestControllerAdvice` para respostas de erro amigáveis e padronizadas.

## 🛣️ Endpoints da API (CRUD Completo)

### 🥊 Lutadores (`/lutadores`)
- `GET /lutadores` - Lista todos os lutadores cadastrados.
- `POST /lutadores` - Regista um novo lutador (valida nome de combate único).
- `PUT /lutadores/{id}` - Atualiza os dados de um lutador existente.
- `DELETE /lutadores/{id}` - Remove um lutador do sistema.

### 🎮 Jogadores (`/jogadores`)
- `GET /jogadores` - Lista todos os jogadores e as suas estatísticas.
- `POST /jogadores` - Regista um novo perfil de jogador.
- `PUT /jogadores/{id}` - Atualiza o nível ou estatísticas de um jogador.
- `DELETE /jogadores/{id}` - Elimina um perfil de jogador.

### 🏟️ Cenários (`/cenarios`)
- `GET /cenarios` - Lista todos os locais de combate.
- `POST /cenarios` - Cadastra um novo cenário.
- `PUT /cenarios/{id}` - Modifica detalhes do cenário (ex: período ou tipo de local).
- `DELETE /cenarios/{id}` - Remove um cenário do sistema.
