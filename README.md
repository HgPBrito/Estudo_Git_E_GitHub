# Estudo de Git e GitHub
> Lembrete sobre comandos usados no dia a dia, e como usá-los no que for possível. Vou atualizado conforme for usando e aprendendo os comandos, e também vou tentar deixar o mais facil de entender, caso alguem use esse README de refêrencia e encontrar algo que gere dúvida ou esteja errado, entre em contato, vamos aprender juntos! [Entre em contato](https://hgpbrito.github.io/curriculo/).

## Começando com o Git
Primeiramente baixando o git para sua máquina referente ao seu sistema usado [Git Downloads](https://git-scm.com/downloads).

Depois de instalado aconselho ter no favoritos as referencias da documentação [Git Reference](https://git-scm.com/docs), mas não se preocupe como já diz é uma referência bom para consultas futuras, mas vamos abordar o básico que se pode ser usado em um dia dia de trabalho.

### Configurações iniciais
```
git config --global user.name "Your Name"
```
- o git necessita de um usuário, comando da um nome a ele.

```
git config --global user.email "Your Email"
```
- esse da o email de usuário.

### Comandos
Existe o comando para criar um repositório local na máquina 'git init' caso esteja ja na pasta ou pode se por 'git init /diretório/da/pasta/para/o/repositório' mas acho mais prático criar um repositório no GitHub e clona-lo.

```
git clone /diretório/do/repositório
```
- faz uma cópia do repositório localmente.

## Salvando algo no repositório
``` 
git add *
ou
git add (arquivo.nn) 
```
- aqui é como se fazer um pacote e avisar, olha tem coisa pra colocar no repositório local, lembrando que precisa estar na pasta do repositório para salvar.

```
git commit -m "comentários de alterações"
```
- aqui você envia seu pacote para o repositorio local, e sempre colocando uma descrição sobre o que foi alterado ótimo para versionamento depois.

```
git push origin (branch)
```
- aqui a gente manda o pacote para o repositório remoto, no caso de versão final sempre deixar na branch main.

## Trabalhando com Branchs
O Porque usar branchs..... ela ajuda a manter um fluxo de trabalho um termo usado para pesquisas futuras **Gitflow**, ajuda a manter o código versionado, um jeito de usar é colocar a branch main como principal com o código com sua versão final e atualizada, uma branch dev para o código que está sendo modificado e caso esteja trabalhando em equipe podemos também ter uma branch de cada desenvolvedor. Aqui é somente uma idéia lembrando sempre da herarquia, de sempre manter a branch atualizada.

```
git checkout -b (nome)
```
- cria uma nova Branch com o nome especificado localmente, então não se esqueça de dar um 'git push origin (branch)' no final caso queira subir a nova branch para o repositório remoto.

```
git checkout (branch)
```
- troca de branch, precisa irde uma branch para outra é esse comando que vai usar.

```
git branch -d (branch)
```
- não quer mais a branch então so deletar.

## Como atualizar e mesclar branchs


```
git diff (branch origem) (branch destino)
```

```
git pull
```

```
git merge (branch)
```