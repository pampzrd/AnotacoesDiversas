# Anotação ComandosUteisDotnet

Para criar um arquivo solution no terminal:
//Ele nomeará com o nome da pasta raíz.
dotnet new sln

Para adicionar o projeto na solution:
//ele vai pegar o meuProj.csproj e adicionar 
dotnet sln add partaRaiz/meuProj

Para criar um projeto de testes no terminal:
//-n (name) pede o nome do arquivo/proj e -o (output/saída) qual será a pasta.
dotnet new xunit -n meuProj.tests -o tests/meuProj.testes

dotnet sln add testes/meuProj.testes


Para referenciar o proj no proj.teste:
//Primeiro o que vai pegar a referência e segundo o que vai ser visitado/referenciado.

dotnet add test/meuProj.tests/ reference pastaRaiz/meuProj

Para adicionar um pacote do nuget? no teste:
dotnet add tests/meuProj.tests/ package FluentAssertions

Usando a Solution não precisa compilar projeto por projeto separadamente. Ele constrói tudo de uma vez se estiver na pastaRaiz da Solution.
dotnet build

(Pesquisar a diferença entre dotnet run e dotnet build)

https://learn.microsoft.com/en-us/dotnet/standard/commandline/syntax#short-form-aliases  POSIX short.