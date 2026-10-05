# MeuServidor Android

Servidor Android em Kotlin para gerenciar e publicar projetos pessoais.

## Instalar

- [Baixar o APK mais recente](https://github.com/andrejvines-commits/serv_cell/releases/latest/download/app-debug.apk) ou abrir a [lista de Releases](https://github.com/andrejvines-commits/serv_cell/releases).
- Instale o APK no Android 8.0 ou superior e configure uma senha administrativa com pelo menos 12 caracteres.
- O app é distribuído como APK de depuração para testes; não é publicado na Play Store.

Para atualizações futuras, toque em **Verificar atualização** no app. Ele consulta a Release pública, valida o SHA-256 do APK e abre o instalador Android. O sistema requer permissão para instalar apps desconhecidos e confirmação da instalação.

## Publicar um projeto

Inicie o servidor no app, crie e envie um projeto pela API administrativa e marque-o como publicado. Projetos publicados são servidos sem autenticação em:

`http://IP_DO_TELEFONE:8081/p/slug-do-projeto/`

A porta `8081` é somente leitura e serve apenas projetos publicados. Para acesso pela internet sem VPN, configure no roteador um encaminhamento TCP da porta `8081` para o IP local do telefone, porta `8081`. O telefone e o servidor precisam permanecer ligados e conectados à internet. Se o provedor usar CGNAT, o encaminhamento IPv4 pode não funcionar.

## Segurança

**Nunca encaminhe a porta `8080` para a internet.** Ela oferece a API administrativa. Encaminhe somente TCP `8081` e confira também o firewall IPv6 do roteador.

O acesso público usa HTTP sem HTTPS. Publique somente arquivos que possam ser vistos sem criptografia. Não use páginas com login, pagamentos ou dados pessoais. O app não configura o roteador nem garante acesso quando o provedor bloqueia conexões externas.
