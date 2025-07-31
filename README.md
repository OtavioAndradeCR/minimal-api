Minimal API
API minimal em .NET 6+, construída com a abordagem Minimal API, usando Entity Framework Core, Swagger/OpenAPI e arquitetura limpa com organização modular de endpoints.

🚀 Funcionalidades
Endpoints REST simplificados com MapGet, MapPost, MapPut, MapDelete

Integração com Entity Framework Core para persistência de dados

Documentação interativa via Swagger/OpenAPI

Estrutura organizada com classes e grupos de rotas separados para manter o Program.cs limpo 
Reddit
+10
Medium
+10
GitHub
+10
Thwani Sithole
+6
Medium
+6
Reddit
+6
macoratti.net
+1
Thwani Sithole
+1
GitHub
+3
Medium
+3
Medium
+3

Práticas modernas de clean code, injeção de dependência, e separação de responsabilidade

🧭 Estrutura do projeto
markdown
Copiar
Editar
/Api
  Program.cs
  /Endpoints
    EntityEndpoints.cs
  /Models
    Entity.cs
  /Data
    AppDbContext.cs
/Test
  EntityServiceTests.cs
Program.cs — Configuração da API, injeções e registro de endpoints

/Endpoints — Classes estáticas com métodos de extensão para mapear rotas 
Reddit
+2
GitHub
+2
Medium
+2
Medium

/Data — Configuração do DbContext do EF Core

/Models — Modelos de domínio e DTOs

/Test — Testes unitários, por ex. com xUnit, MSTest ou NUnit

⚙️ Pré-requisitos
.NET SDK 6.0 ou superior

Banco de dados (p. ex. SQL Server, SQLite ou InMemory)

SQL Server ou outro para persistência real (opcional)

NuGet instalado

📦 Instalação e execução
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/OtavioAndradeCR/minimal-api.git
cd minimal-api/Api
Restaure dependências:

bash
Copiar
Editar
dotnet restore
Configure a string de conexão em appsettings.json.

Aplicar migrações do EF (se houver):

bash
Copiar
Editar
dotnet ef database update
Rode a aplicação:

bash
Copiar
Editar
dotnet run
Acesse Swagger em https://localhost:5001/swagger ou similar.

🧪 Testes
Caso exista uma pasta de testes:

bash
Copiar
Editar
cd minimal-api/Test
dotnet test
✍️ Exemplo de uso
bash
Copiar
Editar
GET    /entities           → retorna a lista de entidades
GET    /entities/{id}      → retorna uma entidade específica
POST   /entities           → cria uma entidade (passa JSON no Body)
PUT    /entities/{id}      → atualiza uma entidade
DELETE /entities/{id}      → deleta uma entidade
✅ Boas práticas aplicadas
CamelCase em JSON (ex: firstName), com padrão consistente 
GitHub
+2
GitHub
+2
Reddit
+2

Uso correto dos métodos HTTP e códigos de status (200 OK, 201 Created, 204 No Content, 404 NotFound) 
Reddit
+3
balta.io
+3
GitHub
+3

Padrões como Repository/Service para separar lógica de domínio, seguindo princípios de DDD (ex.: Classe de serviço chama repositório) 
freecodecamp.org

🛠 Como contribuir
Crie uma branch: git checkout -b feature/exemplo

Faça commits significativos com mensagens claras

Envie um pull request descrevendo sua mudança

Sinta-se livre para abrir issues com sugestões ou correções

📄 Licença
Este projeto está licenciado sob a MIT License.

