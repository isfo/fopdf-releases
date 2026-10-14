# ViewtifulPDF — downloads

Builds distribuíveis do **ViewtifulPDF**, um leitor de PDF para Android que se
registra como handler de PDF do sistema operacional.

Página do projeto: **https://isfo.github.io/fopdf-releases/**

> Nas versões até a 1.3.0 o app se chamava **foPDF**. O id do pacote Android
> segue `br.com.fopdf`, então atualizar substitui a instalação existente.

Este repositório contém **apenas os binários**. O código-fonte é mantido
separadamente.

## Baixar

A versão mais recente está em **[Releases](../../releases/latest)**.

## Instalação

A partir da 1.5.0 os APKs são **assinados com chave de distribuição**, e uma
versão atualiza a anterior sem desinstalar. (Da 1.4.1 para trás eram builds de
debug; para sair de uma delas é preciso desinstalar antes.)

1. Baixe o `.apk` no aparelho.
2. Autorize a instalação de apps de fontes desconhecidas quando o Android
   pedir (a permissão é concedida ao navegador ou gerenciador de arquivos que
   abriu o arquivo).
3. Abra o arquivo baixado.

**Requisito:** Android 7.0 (API 24) ou superior.

## O que o app faz

Renderização local via [PDF.js](https://mozilla.github.io/pdf.js/) — sem
backend, e nenhum arquivo sai do aparelho. O app não pede permissão de
armazenamento: usa o Storage Access Framework, que concede acesso por arquivo.

Três formas de abrir um PDF:

- tocar em um PDF em qualquer app e escolher o ViewtifulPDF em "Abrir com";
- compartilhar um PDF de outro app para o ViewtifulPDF;
- o botão "Abrir PDF" dentro do app, que chama o seletor de arquivos nativo.

E, com o documento aberto:

- rolagem contínua, com renderização em janela;
- zoom por pinça e duplo toque, ancorado no ponto tocado;
- seleção e cópia de texto;
- busca no documento, com destaque de todas as ocorrências e navegação entre elas;
- links do PDF: internos navegam no documento, externos abrem no navegador;
- PDFs protegidos por senha;
- compartilhar o documento aberto, ou baixar uma cópia.

## Limitações

- Teto de 64 MB por arquivo.
- Não edita: sem anotações, assinatura ou preenchimento de formulário.
- Apenas Android.

## Privacidade

Nenhum dado é coletado. Veja a
[política de privacidade](https://isfo.github.io/fopdf-releases/privacidade.html).

## Verificando o download

```bash
sha256sum viewtifulpdf-1.6.0-release.apk
```

A impressão digital do certificado de assinatura, igual em todas as versões a
partir da 1.5.0:

```
SHA-256: 15:B4:21:B4:DD:F8:E0:88:07:2A:F3:EA:54:43:45:17:F8:6D:E0:28:12:09:E8:27:81:C1:40:03:1A:24:E1:FD
```

Para conferir no APK baixado:

```bash
apksigner verify --print-certs viewtifulpdf-1.6.0-release.apk
```

## Licença

MIT.
