# adrian-archetype

Exemplo de criacao de um Archetype Maven.

## Como instalar

Baixar o projeto e executar o comando na raiz do mesmo:

```sh
mvn install
```

Este comando vai jogar os arquivos para o repository do maven, normalmente localizado em _%HomePath%\\.m2\repository_

## Usando na linha de comando

Este comando vai criar o projeto no diretorio atual do terminal

```sh
mvn archetype:generate -B \
-DarchetypeGroupId=com.volkmann \
-DarchetypeArtifactId=adrian-archetype \
-DarchetypeVersion=1.0.0  \
-DgroupId=com.testando \
-DartifactId=testeArchetype \
-Dversion=0.0.1-SNAPSHOT
```
## Usando no Eclipse

Para o Eclipse detectar o archetype é necessario criar o catalgo de archetype local. Execute o comando abaixo dentro do projeto baixado.
```
mvn archetype:update-local-catalog
```
Este comando vai gerar o catalago  _archetype-catalog.xml_ dentro de _%HomePath%\\.m2\repository_

Copiar este arquivo e colar em _%_HomePath%\\.m2_

Agora ao criar um novo projeto Maven no eclipse, ao selecionar o _Default Local_ ira aparecer o archetype.