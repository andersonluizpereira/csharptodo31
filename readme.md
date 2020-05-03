


#bread crumbs for created project

10448  mkdir todo
10449  cd todo
10450  mkdir Todo.Domain
10451  mkdir Todo.Domain.Tests
10452  mkdir Todo.Domain.Infra
10453  mkdir Todo.Domain.Api
10454  ls
10455  ls -l
10456  cd Todo.Domain
10457  dotnet new classlib
10458  cd ..
10459  cd Todo.Domain.Api
10460  dotnet new webapi
10461  cd ..
10462  cd Todo.Domain.Infra
10463  dotnet new classlib
10464  cd ..
10465  cd Todo.Domain.Tests
10466  dotnet new mstest
10467  cd ..
10468  dotnet new sln
10469  ls
10470  cd ..
10471  mv todo Todo
10472  ls
10473  cd Todo
10474  ls
10475  ls -l
10476  rm -rf todo.sln
10477  dotnet new sln
10478  ls
10479  dotnet sln add Todo.Domain
10480  dotnet sln add Todo.Domain.Api
10481  dotnet sln add Todo.Domain.Infra
10482  dotnet sln add Todo.Domain.Tests
10483  dotnet build
10484  cd Todo.Domain
10485  cd ..
10486  cd Todo.Domain.Api
10487  dotnet add reference ../Todo.Domain
10488  dotnet add reference ../Todo.Domain.Infra
10489  cd ..
10490  cd Todo.Domain.Infra
10491  dotnet add reference ../Todo.Domain
10492  cd ..
10493  cd Todo.Domain.Tests
10494  dotnet add reference ../Todo.Domain
10495  cd ..
10496  ls
10497  dotnet build
10498  dotnet --version
10499  code .

Instalar dependências 
dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer 
dotnet add package Microsoft.AspNetCore.Authentication 
dotnet add package Microsoft.EntityFrameworkCore.Design 
dotnet add package Microsoft.EntityFrameworkCoreSqlServer
dotnet add package Microsoft.EntityFrameworkCore.InMemory 
dotnet add package Microsoft.EntityFrameworkCore.Relational
dotnet tool install --global dotnet-ef 
dotnet ef migrations

dotnet ef migrations add InitialCreate --startup-project ../Todo.Domain.Api

swagger

 dotnet add Swashbuckle.AspNetCore -v 5.0.0-rc4
 dotnet add package Swashbuckle.AspNetCore -v 5.0.0-rc4

 #Documentação
 https://localhost:5001/swagger/index.html