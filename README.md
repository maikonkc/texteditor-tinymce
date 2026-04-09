# TinyMCE 7 - Google Docs Fix Implementation

Este projeto corrige o erro crítico de vazamento de texto (horizontal overflow) ao copiar e colar conteúdos do Google Docs para o editor TinyMCE.

## Funcionalidades
- **Correção de Overflow:** Remove larguras fixas e margens da régua do Google Docs.
- **Empilhamento Responsivo:** Título e Editor organizados verticalmente e centralizados.
- **Altura Fixa:** Editor configurado com 600px de altura constante.
- **Proteção de API Key:** Lógica para não expor sua credencial no GitHub.

## Como usar
1. Crie um arquivo `config.js`.
2. Adicione sua chave: `const TINY_API_KEY = "SUA_CHAVE";`.
3. Abra o `index.html`.

## Detalhes Técnicos
- **`paste_preprocess`**: Filtra o HTML colado via Regex.
- **`content_style`**: Injeta `white-space: pre-wrap` para forçar a quebra de linha.
- **`onload`**: Garante a inicialização assíncrona do SDK.