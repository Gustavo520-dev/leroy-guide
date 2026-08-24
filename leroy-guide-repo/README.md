# Leroy Guide

Assistente de loja com IA, acessado por QR Code nos corredores da Leroy Merlin.

**Demo online:** https://leroy-guide-porto-serrano.vercel.app

Projeto acadêmico — Challenge Leroy Merlin · FIAP · 3º Semestre · 2026.

---

## O problema

O cliente entra na loja sabendo *o que quer fazer*, mas não *o que precisa comprar*.
Ele se perde entre corredores, não encontra vendedor livre e desiste ou compra errado.

## A solução

Um QR Code em cada corredor abre um assistente conversacional que responde em segundos:

| | |
|---|---|
| **Corredor Exato** | Diz onde o produto está — corredor, seção e estoque |
| **IA Técnica** | Explica qual broca, qual tinta, qual bitola de fio usar |
| **Lista Personalizada** | Monta a lista completa do projeto com quantidades e preço |
| **Sem Fila** | Atendimento imediato, sem depender de vendedor disponível |

## O MVP

Protótipo navegável do fluxo completo **QR Code → Chat**, com três cenários roteirizados:

1. **Buscar um produto** — localização, preço e estoque
2. **Montar um projeto** — pintura de quarto, troca de box, piso
3. **Dúvida técnica** — broca para parede, tinta para banheiro, bitola de fio

Toda a conversa é guiada por chips de resposta rápida, então a demonstração roda
sem depender de digitação. O campo de texto livre também funciona, com roteamento
por palavra-chave.

## Stack

Página única, sem build e sem dependências: HTML + CSS + JavaScript puro em `index.html`.
Só as fontes vêm de fora (Google Fonts). Deploy estático na Vercel.

> As respostas do assistente são simuladas. O MVP demonstra a experiência e o fluxo
> de conversa — não há modelo de linguagem nem catálogo real conectado.

## Rodando localmente

```bash
git clone <url-do-repositorio>
cd leroy-guide
python3 -m http.server 8000
```

Abra http://localhost:8000 — de preferência com o DevTools em modo mobile.

## Deploy

Qualquer push na branch `main` publica automaticamente na Vercel.
Não há configuração necessária: a raiz do repositório é servida como site estático.
