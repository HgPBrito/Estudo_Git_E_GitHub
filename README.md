# Estudo de Git e GitHub
> Lembrete sobre comandos usados no dia a dia, e como usá-los no que for possível. Vou atualizado conforme for usando e aprendendo os comandos, e também vou tentar deixar o mais facil de entender, caso alguem use esse README de refêrencia e encontrar algo que gere dúvida ou esteja errado, entre em contato, vamos aprender juntos! [Entre em contato](https://hgpbrito.github.io/curriculo/).

## Começando com o Git
Primeiramente baixando o git para sua máquina referente ao seu sistema usado [Git Downloads](https://git-scm.com/downloads).

Depois de instalado aconselho ter no favoritos as referências da documentação [Git Reference](https://git-scm.com/docs) e materiais como [Git Book](http://git-scm.com/book/pt-br/v2) usado para esse estudo, mas não se preocupe como já disse é uma referência, bom para consultas futuras, mas vamos abordar o básico que se pode ser usado em um dia dia de trabalho.

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

```
git status
ou
git status -s
```
- ele retorna o estado do seu repositório, se tem arquivo modificado, se esse arquivo ja foi adicionado ao "pacote" de envio ou não, se so falta fazer commit e muitas outras informações úteis para o seu projeto.

## Arquivo .gitignore
Normalmente temos arquivos que queremos que o Git não coloque no repositótio, pra isso existe o .gitignore é um arquivo que colocamos o diretório epronto aquele arquivo não subirá mais.

Exemplo tirado do [Git Book - alteração no repositório](http://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio).
> As regras para os padrões que podem ser usados no arquivo .gitignore são as seguintes:

> Linhas em branco ou começando com # são ignoradas.

> Os padrões que normalmente são usados para nomes de arquivos funcionam.

> Você pode iniciar padrões com uma barra (/) para evitar recursividade.

> Você pode terminar padrões com uma barra (/) para especificar um diretório.

> Você pode negar um padrão ao fazê-lo iniciar com um ponto de exclamação (!).

> Padrões de nome de arquivo são como expressões regulares simplificadas usadas em ambiente shell. Um asterisco (*) casa com zero ou mais caracteres; [abc] casa com qualquer caracter dentro dos colchetes (neste caso, a, b ou c); um ponto de interrogação (?) casa com um único caracter qualquer; e caracteres entre colchetes separados por hífen ([0-9]) casam com qualquer caracter entre eles (neste caso, de 0 a 9). Você também pode usar dois asteriscos para criar uma expressão que case com diretórios aninhados; a/**/z casaria com a/z, a/b/z, a/b/c/z, e assim por diante.

> Aqui está outro exemplo de arquivo .gitignore:
``` 
# ignorar arquivos com extensão .a
*.a

# mas rastrear o arquivo lib.a, mesmo que você esteja ignorando os arquivos .a acima
!lib.a

# ignorar o arquivo TODO apenas no diretório atual, mas não em subdir/TODO
/TODO

# ignorar todos os arquivos no diretório build/
build/

# ignorar doc/notes.txt, mas não doc/server/arch.txt
doc/*.txt

# ignorar todos os arquivos .pdf no diretório doc/
doc/**/*.pdf
``` 

## Salvando algo no repositório
``` 
git add *
ou
git add *.nn
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
git branch 
```
- lista as branchs existentes e em qual você está trabalhando.

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
 As vezes, acho que a maioria das vezes trabalhamos em equipe e as vezes até na mesma branch, e ai como fica a questão do código quando é compartilhado? bom temos como atualizar para a versão da branch local com a versão do remoto e também temos como unir branchs mergiando elas. Lembrando que ele tenta fazer a junção automaticamente, mas se ouver comflito ele deixa ao seu cargo fazer essa junção de comflitos manualmente.

```
git pull
```
- Atualiza sua branch local com as informações que estão no repositório remoto.

```
git merge (branch)
```
- Ele faz a junção da branch mensionada a sua branch atual.