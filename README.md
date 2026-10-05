# MeuServidor Android

Aplicativo Android que inicia um servidor HTTP local para gerenciar projetos e arquivos.

## Instalação

1. No celular, abra a aba **Releases** deste repositório.
2. Baixe `app-debug.apk` na versão mais recente.
3. Abra o APK baixado e autorize a instalação para o navegador ou gerenciador de arquivos, se o Android solicitar.
4. Abra o app e defina uma senha administrativa com pelo menos 12 caracteres.

Requer Android 8.0 (API 26) ou superior. Este APK de depuração foi compilado para testes; não é uma versão publicada na Play Store.

## Uso

Toque em **Iniciar servidor** no app e acesse o endereço local mostrado na tela, na porta 8080. O serviço não inicia automaticamente após reiniciar o telefone.

## Segurança

O servidor usa HTTP sem TLS. Use somente em uma rede local confiável ou por VPN privada; não encaminhe a porta 8080 diretamente para a internet. Mantenha a senha administrativa em segurança.
