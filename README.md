# ViewtifulPDF — downloads

Builds distribuíveis do **ViewtifulPDF**, um leitor de PDF para Android que
se registra como handler de PDF do sistema operacional.

> Nas versões até a 1.3.0 o app se chamava **foPDF**. O id do pacote Android
> segue `br.com.fopdf`, então atualizar substitui a instalação existente.

Este repositório contém **apenas os binários**. O código-fonte é mantido
separadamente.

## Baixar

A versão mais recente está em **[Releases](../../releases/latest)**.

## Instalação

Os APKs publicados aqui são builds de **debug**, assinados com a chave de
debug do Android — não com uma chave de distribuição. Para instalar:

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

## Também disponível

- Zoom por pinça e duplo toque.
- Seleção e cópia de texto.
- Busca no documento, com destaque e navegação entre as ocorrências.
- Links do PDF: internos navegam, externos abrem no navegador do sistema.
- PDFs protegidos por senha.
- Compartilhar o documento, ou baixar uma cópia.

## Limitações

- Teto de 64 MB por arquivo.
- PDFs protegidos por senha não abrem.
- Sem seleção de texto, busca ou anotações: o conteúdo é rasterizado.
- Apenas Android.

## Verificando o download

Cada release publica o SHA-256 do APK. Para conferir:

```bash
sha256sum viewtifulpdf-1.4.0-debug.apk
```
