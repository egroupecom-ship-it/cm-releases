# Calculadora para Marketplaces — instaladores

Este repositório guarda **só os arquivos de instalação** do app Calculadora para
Marketplaces, usado internamente na Egroup.

Ele é público porque o app precisa alcançar o arquivo `latest.json` de cada release
para saber se existe versão nova. É assim que ele se atualiza sozinho, sem que
ninguém precise baixar instalador à mão.

## O que tem aqui

Em cada release:

- `CM_X.Y.Z_x64-setup.exe` — o instalador (Windows, 64 bits)
- `latest.json` — o aviso de versão que o app lê na abertura

Cada pacote é assinado. O app instalado confere a assinatura e recusa qualquer
arquivo que não tenha vindo daqui.

## O que NÃO tem aqui

O código-fonte, que fica em repositório privado.

Baixar o instalador não dá acesso a nada: sem uma conta autorizada, o app abre na
tela de login e não lê nenhum dado.

## Para quem cuida do projeto

Não suba nada neste repositório à mão. Tudo aqui é gerado por
`npm run publicar-versao`, do repositório do código.
