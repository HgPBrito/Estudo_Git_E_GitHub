# Estudo de Git e GitHub
> Lembrete sobre comandos usados no dia a dia, e como usá-los no que for possível. Vou atualizado conforme for usando e aprendendo os comandos, e também vou tentar deixar o mais facil de entender, caso alguem use esse README de refêrencia e encontrar algo que gere dúvida ou esteja errado, entre em contato, vamos aprender juntos!.

## Começando
existe o comando para criar um repositório local na máquina 'git init' caso esteja ja na pasta ou pode se por 'git init /diretório/do/repositório' mas acho mais prático criar um repositório no GitHub e clona-lo.

'git clone /diretório/do/repositório'
    faz uma cópia do repositório localmente.

## Salvando algo no repositório
'git add *' ou 'git add <arquivo>'
    aqui é como se fazer um pacote e avisar, olha tem coisa pra colocar no repositório local.

'git commit -m "comentários de alterações"'
    aqui você envia seu pacote para o repositorio local, e sempre colocando uma descrição sobre o que foi alterado ótimo para versionamento depois.

git push origin <Branch>
    aqui a gente manda o pacote para o repositório remoto, no caso de versão final sempre deixar na branch master.