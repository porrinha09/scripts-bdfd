# scripts-bdfd
meus scripts para bot com a linguagem bd script (discord)
obs: nem todos meus comandos então aqui, só deixei uns comandos básicos para ajudar vcs
(eu atualizo a metade dos scripts)

## ;avatar
```bd
$nomention
$argsCheck[>1;❌ | Você Precisa Mencionar Alguém!]
$title[Avatar:]
$color[a6d189]
$description[Aqui está]
$image[$userAvatar[$mentioned[<]]]
$nomention
$footer[Pedido por: $username]
```

## ;clear
```bd
$nomention
$deletecommand
$onlyPerms[managemessages;Você não tem a permissão necessária para executar esse comando. **Requer:** __Gerenciar Mensagens__.]
$onlyIf[$isNumber[$noMentionMessage]==true;Não entendi a quantidade de mensagens que você quer que eu apague. use :clear --numero @user]
$onlyIf[$noMentionMessage<=100;Eu só consigo apagar de 2 a 100 mensagens por comando.]
$argsCheck[>1;**Use:** `!limpar <quantidade> {@user}`]
$onlyIf[$noMentionMessage>=2;Eu só consigo apagar de 2 a 100 mensagens por comando.]
$nomention
$onlyIf[$noMentionMessage!=;Você não colocou a quantidade de mensagens a ser apagada. **Use:** `!limpar <quantidade> {@user}`]
$title[clear:]
$description[Deletando mensagens...]
$editIn[1s;
Sucesso, apagado $noMentionMessage $replaceText[$replaceText[&$mentioned[1]&;&&;últimas mensagens do chat.;1];&$mentioned[1]&;últimas mensagens de;1] $replaceText[$replaceText[&$mentioned[1]&;&&;;1];&$mentioned[1]&;<@$mentioned[1]>;1]]
$clear[$noMentionMessage;$replaceText[$replaceText[&$mentioned[1]&;&&;;1];&$mentioned[1]&;$mentioned[1];1];no]
$color[a6d189]
$deleteIn[11s]
$deletecommand
$cooldown[11s;<@$authorID> aguarde __%time%__ para usar esse comando novamente.]
$footer[Limpo por: $username[$authorID]#$discriminator[$authorID]]
$footerIcon[$userAvatar[$authorID]]
$embedSuppressErrors[❌ ERROR ❌; Relate esse erro ao meu criador; FF0000; ; ; ]
$onlyBotPerms[managemessages;Eu não tenho permissão de **Gerenciar mensagens**, por tanto não posso executar esse comando.]
```

## ;say1
```bd
$nomention
$deletecommand
$message
```

## ;say2
```bd
$nomention
$deletecommand
$title[$message]
$color[D47AAD]
```

## ;numero random
```bd
$nomention
$title[número aleatório:]
$description[$randomText[0;10;20;30;40;50;60;70;80;90;100]]
$color[a6d189]
$footer[Pedido por: $username]
```

## ;server info
```bd
$nomention
$title[informações server:]
$color[a6d189]
$description[
quantidade e membros: $membersCount
quantidade e cargos: $roleCount 
quantidade e emojis: $emoteCount
quantidade e canais: $channelCount
quantidade e categorias: $categoryCount
quantidade e boost: $boostCount
dono: <@$serverOwner>

e eu estou em $serverCount servidores]
$footer[Pedido por: $username]
```


## ;help
```bd
$nomention
$title[comandos:]
$color[a6d189]
$description[$botCommands[ ] ]
$footer[Pedido por: $username]
```

## ;transar
```bd
$nomention
$randomText[vc fez sexo com <@$mentioned[1]>;putz ficou mole💀;vc gozou na <@$mentioned[1]>;vc gozou dentro💦💦]
```

## ;fumar
```bd
$nomention
🚬💨💨💨
```

## ;lock
```bd
$nomention
$onlyAdmin[Apenas para admins!]
$modifyChannelPerms[$channelID;-sendmessages;$guildID]
$title[Canal de texto:]
$description[Este canal foi trancado]
$footer[Pedido por: $username]
```

## ;unlock
```bd
$nomention
$onlyAdmin[Apenas para admins!]
$modifyChannelPerms[$channelID;+sendmessages;$guildID]
$title[Canal de texto]
$description[Este canal foi destrancado]
$footer[Pedido por: $username]
```
## ;tabuada
```bd
$nomention
$title[Tabuada:]
$color[a6d189]
$description[
1 x 1 = 1
1 x 2 = 2
1 x 3 = 3
1 x 4 = 4
1 x 5 = 5
1 x 6 = 6
1 x 7 = 7
1 x 8 = 8
1 x 9 = 9
1 x 10 = 1

2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20

3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
3 x 6 = 18
3 x 7 = 21
3 x 8 = 24
3 x 9 = 27
3 x 10 = 30

4 x 1 = 4
4 x 2 = 8
4 x 3 = 12
4 x 4 = 16
4 x 5 = 20
4 x 6 = 24
4 x 7 = 28
4 x 8 = 32
4 x 9 = 36
4 x 10 = 40

5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50

6 x 1 = 6
6 x 2 = 12
6 x 3 = 18
6 x 4 = 24
6 x 5 = 30
6 x 6 = 36
6 x 7 = 42
6 x 8 = 48
6 x 9 = 54
6 x 10 = 60

7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
7 x 4 = 28
7 x 5 = 35
7 x 6 = 42
7 x 7 = 49
7 x 8 = 56
7 x 9 = 63
7 x 10 = 7

8 x 1 = 8
8 x 2 = 16
8 x 3 = 24
8 x 4 = 32
8 x 5 = 40
8 x 6 = 48
8 x 7 = 56
8 x 8 = 64
8 x 9 = 72
8 x 10 = 80

9 x 1 = 9
9 x 2 = 18
9 x 3 = 27
9 x 4 = 36
9 x 5 = 45
9 x 6 = 54
9 x 7 = 63
9 x 8 = 72
9 x 9 = 81
9 x 10 = 90

10 x 1 = 10
10 x 2 = 20
10 x 3 = 30
10 x 4 = 40
10 x 5 = 50
10 x 6 = 60
10 x 7 = 70
10 x 8 = 80
10 x 9 = 90
10 x 10 = 100]
$footer[Pedido por: $username]
```













































































