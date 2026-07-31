# 4Bet Table Manager

Organizador de mesas de poker para Windows. Este repositório serve apenas à
**distribuição**: o instalador e o aviso de atualização. O código-fonte não fica aqui.

## Baixar

O instalador está em [Releases](../../releases/latest) — o arquivo
`4Bet Table Manager Setup.exe`.

O programa exige uma **licença** para funcionar. Ao abrir pela primeira vez ele mostra um
código da máquina; envie esse código para receber a sua.

Instruções completas de instalação vêm junto com o instalador.

## atualizacao.txt

O aplicativo lê este arquivo toda vez que abre, para saber se existe versão nova.

Ele é um documento **assinado**: contém a versão publicada, o endereço do instalador e o
SHA-256 dele. O aplicativo traz a chave pública embutida e recusa qualquer aviso que não
tenha sido assinado com a chave privada correspondente — editar o conteúdo, inclusive a
URL, invalida a assinatura.

Isso importa porque um atualizador baixa e **executa** código na máquina de todos os
usuários. HTTPS sozinho protegeria o transporte, não o arquivo parado num servidor que
pode ser invadido.

O endereço deste arquivo é gravado dentro do executável e nunca muda, então ele mora no
repositório e não numa release — URLs de asset carregam a tag e mudariam a cada versão.
