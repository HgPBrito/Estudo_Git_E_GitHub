# Estudo de Git e GitHub
> Lembrete sobre comandos usados no dia a dia, e como usá-los no que for possível. Vou atualizado conforme for usando e aprendendo os comandos, e também vou tentar deixar o mais facil de entender, caso alguem use esse README de refêrencia e encontrar algo que gere dúvida ou esteja errado, entre em contato, vamos aprender juntos!.

## Começando
existe o comando para criar um repositório local na máquina 'git init' caso esteja ja na pasta ou pode se por 'git init /diretório/do/repositório' mas acho mais prático criar um repositório no GitHub e clona-lo.

configurações iniciais para o Git
' git config --global user.name "Your Name" '
- o git necessita de um usuário, comando da um nome a ele.

' git config --global user.email "Your Email" '
- esse da o email de usuário.


' git clone /diretório/do/repositório '
- faz uma cópia do repositório localmente.

## Salvando algo no repositório
' git add *' ou 'git add (arquivo.nn) '
- aqui é como se fazer um pacote e avisar, olha tem coisa pra colocar no repositório local, lembrando que precisa estar na pasta do repositório para salvar.

' git commit -m "comentários de alterações" '
- aqui você envia seu pacote para o repositorio local, e sempre colocando uma descrição sobre o que foi alterado ótimo para versionamento depois.

' git push origin (branch) '
- aqui a gente manda o pacote para o repositório remoto, no caso de versão final sempre deixar na branch main.