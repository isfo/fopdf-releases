# foPDF — downloads

Builds distribuíveis do **foPDF**, um leitor de PDF para Android que se
registra como handler de PDF do sistema operacional.

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

- tocar em um PDF em qualquer app e escolher o foPDF em "Abrir com";
- compartilhar um PDF de outro app para o foPDF;
- o botão "Abrir PDF" dentro do app, que chama o seletor de arquivos nativo.

## Limitações

- Teto de 64 MB por arquivo.
- PDFs protegidos por senha não abrem.
- Sem seleção de texto, busca ou anotações: o conteúdo é rasterizado.
- Apenas Android.

## Verificando o download

Cada release publica o SHA-256 do APK. Para conferir:

```bash
sha256sum fopdf-1.0.0-debug.apk
```
