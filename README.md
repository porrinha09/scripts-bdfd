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
















































































