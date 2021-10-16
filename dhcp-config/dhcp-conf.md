# Configuração Servidor DHCP

## Atribuir o diretório _/sbin_ a variável PATH do sistema


Visando simplicar a utilização de comandos que possam estar contidos dentro 
do diretório _/SBIN_, de modo que não exista necessidade de referenciar esse path
sempre que algum comando relativo a ele for executado. 
## Maneira temporária
Conforme exemplificado [DEV-TO-PATH], para configurar de maneira temporária o _/sbin_ precisamos 
utilizar o seguinte comando:
```
export PATH="$PATH:/sbin"
```
Desta forma esse diretório agora ficará salvo no seu PATH enquanto a sua sessão estiver ativa.

## Maneira Definitiva
Para que não exista a necessidade de a cada sessão configurar manualmente o PATH o diretório _/sbin_ e outros do seu interesse é necessário incluir a seguinte linha  no arquivo **"~/.bashrc"**

```
PATH="$PATH:/sbin"
```

Você pode abrir esse arquivo com o editor de sua preferência, um dos possíveis é o **nano**. Para abrir o arquivos com esse editor você deve combinar o nome do editor "nano" + "nome do arquivio", exemplo:
```
nano ~/.bashrc
```
Para consultar como a variável $PATH está atualmente utilize o seguinte comando:
```
echo $PATH
```
#### Considerações
> O comando PATH="$PATH:/diretorio" concatena diretórios aos que já estão salvos no $PATH.
> Edite o arquivo **"~/.bashrc"** com permissões de usuário apenas para que tudo ocorra com corretamente.
> A diferença da maneira temporária para definitiva é que na definitiva toda vez que é startada sua sessão o sistema faz a leitura e execução dos comandos contidos no arquivo **"~/.bashrc"**, não havendo necessidade de que você mesmo o faça sempre que iniciar uma nova sessão.
> Os caminhos no $PATH são separados com **:** e cada caminho atribuído a essa variável deve estar completo, por exemplo: se você possui o caminho **/sbin** e **/sbin/etc** e deseja incoporar esses dois diretórios ao $PATH deve incluir eles de maneira completa: **_PATH="$PATH:/sbin:/sbin/etc"_**


# Continuem...


[//]: # (Esses são links de referência usados no corpo desta MD e são removidos quando o processador de remarcação faz seu trabalho. Não há necessidade de aplicar alguma formatação aos [] pois eles não são renderizados. Créditos: http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [DEV-TO-PATH]: <https://dev.to/reginadiana/como-escrever-um-readme-md-sensacional-no-github-4509> 
