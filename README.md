## Cloud Native Buildpacks Demo


Esse repositório contém uma aplicação simples para a realização de uma demonstração do [Cloud Native Buildpacks](https://buildpacks.io/) (CNB).
A aplicação em si não tem nada de mais. Uma aplicação Fastapi que retorna uma menssagem simples.

No diretório da aplicação existe: 
- o `app/` que contem o código fonte. 
- O arquivo `requirement.txt` com a dependências da aplicação
- O arquivo Procfile com a definição do process (entrypoint) que será utilizado.


Para realizar a demo:

- clonar o repositorio

- instalar o CLI [pack](https://buildpacks.io/docs/tools/pack/) de acordo com o seu Sistema Operacional

- entrar no diretório `sample-app` (diretório raiz da aplicação)

- rodar o comando de build:
```
pack build sample-app-test --builder paketobuildpacks/builder:base --workspace app/
```

Será feito o build de uma imagem com o nome `sample-app-test`, 

utilizando o builder `base` da [paketo](https://github.com/paketo-buildpacks) e 

definindo o diretorio raiz do container (workspace) como `app/`


Mais informações sobre argumentos que podem ser utilizados com o CLI pack para configurações adicionais na [doc](https://buildpacks.io/docs/) da CNB
